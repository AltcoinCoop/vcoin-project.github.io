---
layout: engpage
title: Script
excerpt: Bitcoin transaction scripting language guide
image:
  feature:
---

<script src="/assets/js/vendor/library/raphael.min.js"></script>
<script src="/assets/js/vendor/library/underscore.min.js"></script>
<script src="/assets/js/vendor/library/sequence-diagram-min.js"></script>


<!--<div id="diagram"></div>-->

<!--<div class="diagram">
title: Pay-to-Bob script
Alice->Bob: Authentication Request
Bob->Alice: Authentication Response
</div>-->

<div class="diagram">
title: Deposit
Alice-->Bob: APK
Bob-->Alice: BPK
Note over Alice: Tx1 = APK+[10.0]+BPK
Note over Alice: HTx1 = Hash(Tx1)
Alice-->Bob: HTx1
Note over Bob: Tx2 = (0,+HTx1+BPK+DATE)
Bob-->Alice: Tx2
Alice->Bob: Tx1
Alice->Bob: APK+Tx2
Note over Alice,Bob: (0,APK+HTx1+BPK+DATE)
</div>

## Example 1: Providing a deposit

Alice opens an account with Bob’s Betting and wishes to establish her trustworthiness with Bob, but she doesn't have any pre-existing reputation to leverage. One solution is to buy trust by paying Bob some money. But if at some point Alice closes her account, she'd probably like that money back. Alice may not trust Bob enough to give him a deposit that he might be tempted to spend. Another risk is that Bob might just disappear one day.

Alice’s goal is to prove that she made a sacrifice of some kind so Bob knows she’s not a timewaster, but Alice doesn't want Bob to be able to spend the money. And if Bob disappears, Alice'd eventually like the coins back without needing anything from him.

We can solve this problem with a contract:

- Alice and Bob send each other a newly-generated public key.
- Alice creates transaction Tx1 (the payment) putting 10 BTC into an output that requires both her and Bob to sign, but does not broadcast it. Alice uses the key Bob sent her in the previous step.
- Alice sends the hash of Tx1 to Bob.
- Bob creates a transaction Tx2 (the contract). Tx2 spends Tx1 and pays it back to Alice via the address she provided in the first step. Note that Tx1 requires two signatures, so this transaction can't be complete. nLockTime is set to some date in the future (eg, six months). The sequence number on the input is set to zero.
- Finally, Bob sends the incomplete (half-signed) transaction back to Alice. She checks that the contract is as expected - that the coins will eventually come back to her - but, unless things are changed, only after six months. Because the sequence number is zero, the contract can be amended in future if both parties agree. The script in the input isn't finished though; there are only zeros where Alice’s signature should be. She fixes that by signing the contract and putting the new signature in the appropriate spot.
- Alice broadcasts Tx1 (which Bob sees), then broadcasts Tx2 (also seen by Bob).
- At this stage, the 10 BTC are in a state where neither Alice nor Bob can spend them independently. After six months, the contract will complete and Alice will get her 10 BTC back, even if Bob disappears.

#### What if Alice wishes to close her account early?
Bob creates a new version of Tx2 with nLockTime set to zero and the input sequence number set to UINT_MAX, then he re-signs it. He then hands the tx back to Alice, who signs it as well. Alice then broadcasts the transaction, terminating the contract early and releasing the coins.

#### What if the six months is nearly up and Alice wishes to keep her account?
The same thing applies: the contract can be re-signed with a newer nLockTime, a sequence number 1 higher than the previous and rebroadcast 2^32 times. No matter what happens, both parties must agree for the contract to change.

#### What if Alice turns out to be a numpty?
Bob will not allow an early close of the contract, Alice will have to wait for her coins. If Alice‘s need for support becomes disproportionate, the size of the deposit can be raised or the length of the contract can be increased.

---

See also: [Secure Multiparty Computations on Bitcoin](http://eprint.iacr.org/2013/784.pdf)


# Script language

Defined for [Bitcoin Core 0.11](https://github.com/bitcoin/bitcoin/blob/0.11/src/script/script.cpp).

## Constants

When talking about scripts, these value-pushing words are usually omitted.

<table class="ui compact single line table" style="font-size:50%">
<thead><tr><th>Word</th><th>Opcode</th><th>Hex</th><th>Input</th><th>Output</th><th>Description</th></tr></thead>
<tbody>
<tr><td>OP_0, OP_FALSE</td><td>0</td><td>0x00</td><td>Nothing.</td><td>(empty value)</td><td>An empty array of bytes is pushed onto the stack. (Not a no-op: an item is added to the stack.)</td></tr>
<tr><td>N/A</td><td>1-75</td><td>0x01-0x4b</td><td>(special)</td><td>data</td><td>The next <i>opcode</i> bytes is data to be pushed onto the stack</td></tr>
<tr><td>OP_PUSHDATA1</td><td>76</td><td>0x4c</td><td>(special)</td><td>data</td><td>The next byte contains the number of bytes to be pushed onto the stack.</td></tr>
<tr><td>OP_PUSHDATA2</td><td>77</td><td>0x4d</td><td>(special)</td><td>data</td><td>The next two bytes contain the number of bytes to be pushed onto the stack.</td></tr>
<tr><td>OP_PUSHDATA4</td><td>78</td><td>0x4e</td><td>(special)</td><td>data</td><td>The next four bytes contain the number of bytes to be pushed onto the stack.</td></tr>
<tr><td>OP_1NEGATE</td><td>79</td><td>0x4f</td><td>Nothing.</td><td> -1</td><td>The number -1 is pushed onto the stack.</td></tr>
<tr><td>OP_1, OP_TRUE</td><td>81</td><td>0x51</td><td>Nothing.</td><td>1</td><td>The number 1 is pushed onto the stack.</td></tr>
<tr><td>OP_2-OP_16</td><td>82-96</td><td>0x52-0x60</td><td>Nothing.</td><td>2-16</td><td>The number in the word name (2-16) is pushed onto the stack.</td></tr>
</tbody>
</table>

## Flow control

<table class="ui compact single line table" style="font-size:50%">
<thead><tr><th>Word</th><th>Opcode</th><th>Hex</th><th>Input</th><th>Output</th><th>Description</th></tr></thead>
<tbody>
<tr><td>OP_NOP</td><td>97</td><td>0x61</td><td>Nothing</td><td>Nothing</td><td>Does nothing.</td></tr>
<tr><td>OP_IF</td><td>99</td><td>0x63</td><td colspan="2">&lt;expression&gt; if [statements] [else [statements]]* endif</td><td>If the top stack value is not 0, the statements are executed. The top stack value is removed.</td></tr>
<tr><td>OP_NOTIF</td><td>100</td><td>0x64</td><td colspan="2">&lt;expression&gt; if [statements] [else [statements]]* endif</td><td>If the top stack value is 0, the statements are executed. The top stack value is removed.</td></tr>
<tr><td>OP_ELSE</td><td>103</td><td>0x67</td><td colspan="2">&lt;expression&gt; if [statements] [else [statements]]* endif</td><td>If the preceding OP_IF or OP_NOTIF or OP_ELSE was not executed then these statements are.*</td></tr>
<tr><td>OP_ENDIF</td><td>104</td><td>0x68</td><td colspan="2">&lt;expression&gt; if [statements] [else [statements]]* endif</td><td>Ends an if/else block. All blocks must end, or the transaction is <b>invalid</b>. An OP_ENDIF without OP_IF earlier is also <b>invalid</b>.</td></tr>
<tr><td>OP_VERIFY</td><td>105</td><td>0x69</td><td>True / false</td><td>Nothing / False</td><td><b>Marks transaction as invalid</b> if top stack value is not true.</td></tr>
<tr><td>OP_RETURN</td><td>106</td><td>0x6a</td><td>Nothing</td><td>Nothing</td><td><b>Marks transaction as invalid</b>. **</td></tr></tbody>
</tbody>
</table>

<small>(*) and if the preceding OP_IF or OP_NOTIF or OP_ELSE was executed then these statements are not</small>

<small>(**) A standard way of attaching extra data to transactions is to add a zero-value output with a scriptPubKey consisting of OP_RETURN followed by exactly one pushdata op. Such outputs are provably unspendable, reducing their cost to the network. Currently it is usually considered non-standard (though valid) for a transaction to have more than one OP_RETURN output or an OP_RETURN output with more than one pushdata op.</small>

## Stack

<table class="ui compact single line table" style="font-size:50%">
<thead><tr><th>Word</th><th>Opcode</th><th>Hex</th><th>Input</th><th>Output</th><th>Description</th></tr></thead>
<tbody>
<tr><td>OP_TOALTSTACK</td><td>107</td><td>0x6b</td><td>x1</td><td>(alt)x1</td><td>Puts the input onto the top of the alt stack. Removes it from the main stack.</td></tr>
<tr><td>OP_FROMALTSTACK</td><td>108</td><td>0x6c</td><td>(alt)x1</td><td>x1</td><td>Puts the input onto the top of the main stack. Removes it from the alt stack.</td></tr>
<tr><td>OP_IFDUP</td><td>115</td><td>0x73</td><td>x</td><td>x / x x</td><td>If the top stack value is not 0, duplicate it.</td></tr>
<tr><td>OP_DEPTH</td><td>116</td><td>0x74</td><td>Nothing</td><td>&lt;Stack size&gt;</td><td>Puts the number of stack items onto the stack.</td></tr>
<tr><td>OP_DROP</td><td>117</td><td>0x75</td><td>x</td><td>Nothing</td><td>Removes the top stack item.</td></tr>
<tr><td>OP_DUP</td><td>118</td><td>0x76</td><td>x</td><td>x x</td><td>Duplicates the top stack item.</td></tr>
<tr><td>OP_NIP</td><td>119</td><td>0x77</td><td>x1 x2</td><td>x2</td><td>Removes the second-to-top stack item.</td></tr>
<tr><td>OP_OVER</td><td>120</td><td>0x78</td><td>x1 x2</td><td>x1 x2 x1</td><td>Copies the second-to-top stack item to the top.</td></tr>
<tr><td>OP_PICK</td><td>121</td><td>0x79</td><td>xn ... x2 x1 x0 &lt;n&gt;</td><td>xn ... x2 x1 x0 xn</td><td>The item <i>n</i> back in the stack is copied to the top.</td></tr>
<tr><td>OP_ROLL</td><td>122</td><td>0x7a</td><td>xn ... x2 x1 x0 &lt;n&gt;</td><td>... x2 x1 x0 xn</td><td>The item <i>n</i> back in the stack is moved to the top.</td></tr>
<tr><td>OP_ROT</td><td>123</td><td>0x7b</td><td>x1 x2 x3</td><td>x2 x3 x1</td><td>The top three items on the stack are rotated to the left.</td></tr>
<tr><td>OP_SWAP</td><td>124</td><td>0x7c</td><td>x1 x2</td><td>x2 x1</td><td>The top two items on the stack are swapped.</td></tr>
<tr><td>OP_TUCK</td><td>125</td><td>0x7d</td><td>x1 x2</td><td>x2 x1 x2</td><td>The item at the top of the stack is copied and inserted before the second-to-top item.</td></tr>
<tr><td>OP_2DROP</td><td>109</td><td>0x6d</td><td>x1 x2</td><td>Nothing</td><td>Removes the top two stack items.</td></tr>
<tr><td>OP_2DUP</td><td>110</td><td>0x6e</td><td>x1 x2</td><td>x1 x2 x1 x2</td><td>Duplicates the top two stack items.</td></tr>
<tr><td>OP_3DUP</td><td>111</td><td>0x6f</td><td>x1 x2 x3</td><td>x1 x2 x3 x1 x2 x3</td><td>Duplicates the top three stack items.</td></tr>
<tr><td>OP_2OVER</td><td>112</td><td>0x70</td><td>x1 x2 x3 x4</td><td>x1 x2 x3 x4 x1 x2</td><td>Copies the pair of items two spaces back in the stack to the front.</td></tr>
<tr><td>OP_2ROT</td><td>113</td><td>0x71</td><td>x1 x2 x3 x4 x5 x6</td><td>x3 x4 x5 x6 x1 x2</td><td>The fifth and sixth items back are moved to the top of the stack.</td></tr>
<tr><td>OP_2SWAP</td><td>114</td><td>0x72</td><td>x1 x2 x3 x4</td><td>x3 x4 x1 x2</td><td>Swaps the top two pairs of items.</td></tr>
</tbody>
</table>


## Splice
If any opcode marked as disabled is present in a script, it must abort and fail.

<table class="ui compact single line table" style="font-size:50%">
<thead><tr><th>Word</th><th>Opcode</th><th>Hex</th><th>Input</th><th>Output</th><th>Description</th></tr></thead>
<tbody>
<tr><td>OP_CAT</td><td>126</td><td>0x7e</td><td>x1 x2</td><td>out</td>
<td style="background:#D97171;">Concatenates two strings. <i>disabled.</i></td></tr>
<tr><td>OP_SUBSTR</td><td>127</td><td>0x7f</td><td>in begin size</td><td>out</td>
<td style="background:#D97171;">Returns a section of a string. <i>disabled.</i></td></tr>
<tr><td>OP_LEFT</td><td>128</td><td>0x80</td><td>in size</td><td>out</td>
<td style="background:#D97171;">Keeps only characters left of the specified point in a string. <i>disabled.</i></td></tr>
<tr><td>OP_RIGHT</td><td>129</td><td>0x81</td><td>in size</td><td>out</td>
<td style="background:#D97171;">Keeps only characters right of the specified point in a string. <i>disabled.</i></td></tr>
<tr><td>OP_SIZE</td><td>130</td><td>0x82</td><td>in</td><td>in size</td><td>Pushes the string length of the top element of the stack (without popping it).</td></tr>
</tbody>
</table>

## Bitwise logic
If any opcode marked as disabled is present in a script, it must abort and fail.

<table class="ui compact single line table" style="font-size:50%">
<thead><tr><th>Word</th><th>Opcode</th><th>Hex</th><th>Input</th><th>Output</th><th>Description</th></tr></thead>
<tbody>
<tr><td>OP_INVERT</td><td>131</td><td>0x83</td><td>in</td><td>out</td>
<td style="background:#D97171;">Flips all of the bits in the input. <i>disabled.</i></td></tr>
<tr><td>OP_AND</td><td>132</td><td>0x84</td><td>x1 x2</td><td>out</td>
<td style="background:#D97171;">Boolean <i>and</i> between each bit in the inputs. <i>disabled.</i></td></tr>
<tr><td>OP_OR</td><td>133</td><td>0x85</td><td>x1 x2</td><td>out</td>
<td style="background:#D97171;">Boolean <i>or</i> between each bit in the inputs. <i>disabled.</i></td></tr>
<tr><td>OP_XOR</td><td>134</td><td>0x86</td><td>x1 x2</td><td>out</td>
<td style="background:#D97171;">Boolean <i>exclusive or</i> between each bit in the inputs. <i>disabled.</i></td></tr>
<tr><td>OP_EQUAL</td><td>135</td><td>0x87</td><td>x1 x2</td><td>True / false</td><td>Returns 1 if the inputs are exactly equal, 0 otherwise.</td></tr>
<tr><td>OP_EQUALVERIFY</td><td>136</td><td>0x88</td><td>x1 x2</td><td>True / false</td><td>Same as OP_EQUAL, but runs OP_VERIFY afterward.</td></tr>
</tbody>
</table>

## Arithmetic
Note: Arithmetic inputs are limited to signed 32-bit integers, but may overflow their output.

If any input value for any of these commands is longer than 4 bytes, the script must abort and fail. If any opcode marked as disabled is present in a script - it must also abort and fail.

<table class="ui compact single line table" style="font-size:50%">
<thead><tr><th>Word</th><th>Opcode</th><th>Hex</th><th>Input</th><th>Output</th><th>Description</th></tr></thead>
<tbody>
<tr><td>OP_1ADD</td><td>139</td><td>0x8b</td><td>in</td><td>out</td><td>1 is added to the input.</td></tr>
<tr><td>OP_1SUB</td><td>140</td><td>0x8c</td><td>in</td><td>out</td><td>1 is subtracted from the input.</td></tr>
<tr><td>OP_2MUL</td><td>141</td><td>0x8d</td><td>in</td><td>out</td>
<td style="background:#D97171;">The input is multiplied by 2. <i>disabled.</i></td></tr>
<tr><td>OP_2DIV</td><td>142</td><td>0x8e</td><td>in</td><td>out</td>
<td style="background:#D97171;">The input is divided by 2. <i>disabled.</i></td></tr>
<tr><td>OP_NEGATE</td><td>143</td><td>0x8f</td><td>in</td><td>out</td><td>The sign of the input is flipped.</td></tr>
<tr><td>OP_ABS</td><td>144</td><td>0x90</td><td>in</td><td>out</td><td>The input is made positive.</td></tr>
<tr><td>OP_NOT</td><td>145</td><td>0x91</td><td>in</td><td>out</td><td>If the input is 0 or 1, it is flipped. Otherwise the output will be 0.</td></tr>
<tr><td>OP_0NOTEQUAL</td><td>146</td><td>0x92</td><td>in</td><td>out</td><td>Returns 0 if the input is 0. 1 otherwise.</td></tr>
<tr><td>OP_ADD</td><td>147</td><td>0x93</td><td>a b</td><td>out</td><td>a is added to b.</td></tr>
<tr><td>OP_SUB</td><td>148</td><td>0x94</td><td>a b</td><td>out</td><td>b is subtracted from a.</td></tr>
<tr><td>OP_MUL</td><td>149</td><td>0x95</td><td>a b</td><td>out</td>
<td style="background:#D97171;">a is multiplied by b. <i>disabled.</i></td></tr>
<tr><td>OP_DIV</td><td>150</td><td>0x96</td><td>a b</td><td>out</td>
<td style="background:#D97171;">a is divided by b. <i>disabled.</i></td></tr>
<tr><td>OP_MOD</td><td>151</td><td>0x97</td><td>a b</td><td>out</td>
<td style="background:#D97171;">Returns the remainder after dividing a by b. <i>disabled.</i></td></tr>
<tr><td>OP_LSHIFT</td><td>152</td><td>0x98</td><td>a b</td><td>out</td>
<td style="background:#D97171;">Shifts a left b bits, preserving sign. <i>disabled.</i></td></tr>
<tr><td>OP_RSHIFT</td><td>153</td><td>0x99</td><td>a b</td><td>out</td>
<td style="background:#D97171;">Shifts a right b bits, preserving sign. <i>disabled.</i></td></tr>
<tr><td>OP_BOOLAND</td><td>154</td><td>0x9a</td><td>a b</td><td>out</td><td>If both a and b are not 0, the output is 1. Otherwise 0.</td></tr>
<tr><td>OP_BOOLOR</td><td>155</td><td>0x9b</td><td>a b</td><td>out</td><td>If a or b is not 0, the output is 1. Otherwise 0.</td></tr>
<tr><td>OP_NUMEQUAL</td><td>156</td><td>0x9c</td><td>a b</td><td>out</td><td>Returns 1 if the numbers are equal, 0 otherwise.</td></tr>
<tr><td>OP_NUMEQUALVERIFY</td><td>157</td><td>0x9d</td><td>a b</td><td>out</td><td>Same as OP_NUMEQUAL, but runs OP_VERIFY afterward.</td></tr>
<tr><td>OP_NUMNOTEQUAL</td><td>158</td><td>0x9e</td><td>a b</td><td>out</td><td>Returns 1 if the numbers are not equal, 0 otherwise.</td></tr>
<tr><td>OP_LESSTHAN</td><td>159</td><td>0x9f</td><td>a b</td><td>out</td><td>Returns 1 if a is less than b, 0 otherwise.</td></tr>
<tr><td>OP_GREATERTHAN</td><td>160</td><td>0xa0</td><td>a b</td><td>out</td><td>Returns 1 if a is greater than b, 0 otherwise.</td></tr>
<tr><td>OP_LESSTHANOREQUAL</td><td>161</td><td>0xa1</td><td>a b</td><td>out</td><td>Returns 1 if a is less than or equal to b, 0 otherwise.</td></tr>
<tr><td>OP_GREATERTHANOREQUAL</td><td>162</td><td>0xa2</td><td>a b</td><td>out</td><td>Returns 1 if a is greater than or equal to b, 0 otherwise.</td></tr>
<tr><td>OP_MIN</td><td>163</td><td>0xa3</td><td>a b</td><td>out</td><td>Returns the smaller of a and b.</td></tr>
<tr><td>OP_MAX</td><td>164</td><td>0xa4</td><td>a b</td><td>out</td><td>Returns the larger of a and b.</td></tr>
<tr><td>OP_WITHIN</td><td>165</td><td>0xa5</td><td>x min max</td><td>out</td><td>Returns 1 if x is within the specified range (left-inclusive), 0 otherwise.</td></tr>
</tbody>
</table>

## Crypto

<table class="ui compact single line table" style="font-size:50%">
<thead><tr><th>Word</th><th>Opcode</th><th>Hex</th><th>Input</th><th>Output</th><th>Description</th></tr></thead>
<tbody>
<tr><td>OP_RIPEMD160</td><td>166</td><td>0xa6</td><td>in</td><td>hash</td><td>The input is hashed using RIPEMD-160.</td></tr>
<tr><td>OP_SHA1</td><td>167</td><td>0xa7</td><td>in</td><td>hash</td><td>The input is hashed using SHA-1.</td></tr>
<tr><td>OP_SHA256</td><td>168</td><td>0xa8</td><td>in</td><td>hash</td><td>The input is hashed using SHA-256.</td></tr>
<tr><td>OP_HASH160</td><td>169</td><td>0xa9</td><td>in</td><td>hash</td><td>The input is hashed twice: first with SHA-256 and then with RIPEMD-160.</td></tr>
<tr><td>OP_HASH256</td><td>170</td><td>0xaa</td><td>in</td><td>hash</td><td>The input is hashed two times with SHA-256.</td></tr>
<tr><td>OP_CODESEPARATOR</td><td>171</td><td>0xab</td><td>Nothing</td><td>Nothing</td><td>Signature checking words will only match sigs to data after the most recently-executed OP_CODESEPARATOR.</td></tr>
<tr><td><a href="/wiki/OP_CHECKSIG" title="OP CHECKSIG">OP_CHECKSIG</a></td><td>172</td><td>0xac</td><td>sig pubkey</td><td>True / false</td><td>The entire transaction's outputs, inputs, and script are hashed.*</td></tr>
<tr><td>OP_CHECKSIGVERIFY</td><td>173</td><td>0xad</td><td>sig pubkey</td><td>True / false</td><td>Same as OP_CHECKSIG, but OP_VERIFY is executed afterward.</td></tr>
<tr><td>OP_CHECKMULTISIG</td><td>174</td><td>0xae</td><td>x sig1 sig2 ... &lt;#sigs&gt; pub1 pub2 &lt;#keys&gt;</td><td>True / False</td><td>Compares the first signature against each public key until it finds an ECDSA match.**</td></tr>
<tr><td>OP_CHECKMULTISIGVERIFY</td><td>175</td><td>0xaf</td><td>x sig1 sig2 ... &lt;#sigs&gt; pub1 pub2 ... &lt;#keys&gt;</td><td>True / False</td><td>Same as OP_CHECKMULTISIG, but OP_VERIFY is executed afterward.</td></tr>
</tbody>
</table>

<small>(*) (i.e.from the most recently-executed OP_CODESEPARATOR to the end) The signature used by OP_CHECKSIG must be a valid signature for this hash and public key. If it is, 1 is returned, 0 otherwise.</small>

<small>(**) Starting with the subsequent public key, it compares the second signature against each remaining public key until it finds an ECDSA match. The process is repeated until all signatures have been checked or not enough public keys remain to produce a successful result. All signatures need to match a public key. Because public keys are not checked again if they fail any signature comparison, signatures must be placed in the scriptSig using the same order as their corresponding public keys were placed in the scriptPubKey or redeemScript. If all signatures are valid, 1 is returned, 0 otherwise. Due to a bug, one extra unused value is removed from the stack.</small>

## Pseudo-words
These words are used internally for assisting with transaction matching. They are invalid if used in actual scripts.

<table class="ui compact single line table" style="font-size:50%">
<thead><tr><th>Word</th><th>Opcode</th><th>Hex</th><th>Description</th></tr></thead>
<tbody>
<tr><td>OP_PUBKEYHASH</td><td>253</td><td>0xfd</td><td>Represents a public key hashed with OP_HASH160.</td></tr>
<tr><td>OP_PUBKEY</td><td>254</td><td>0xfe</td><td>Represents a public key compatible with OP_CHECKSIG.</td></tr>
<tr><td>OP_INVALIDOPCODE</td><td>255</td><td>0xff</td><td>Matches any opcode that is not yet assigned.</td></tr>
</tbody>
</table>

## Reserved words
Any opcode not assigned is also reserved. Using an unassigned opcode makes the transaction **invalid**.

<table class="ui compact single line table" style="font-size:50%">
<thead><tr><th>Word</th><th>Opcode</th><th>Hex</th><th>When used...</th></tr></thead>
<tbody>
<tr><td>OP_RESERVED</td><td>80</td><td>0x50</td><td><b>Transaction is invalid</b> unless occuring in an unexecuted OP_IF branch</td></tr>
<tr><td>OP_VER</td><td>98</td><td>0x62</td><td><b>Transaction is invalid</b> unless occuring in an unexecuted OP_IF branch</td></tr>
<tr><td>OP_VERIF</td><td>101</td><td>0x65</td><td><b>Transaction is invalid even when occuring in an unexecuted OP_IF branch</b></td></tr>
<tr><td>OP_VERNOTIF</td><td>102</td><td>0x66</td><td><b>Transaction is invalid even when occuring in an unexecuted OP_IF branch</b></td></tr>
<tr><td>OP_RESERVED1</td><td>137</td><td>0x89</td><td><b>Transaction is invalid</b> unless occuring in an unexecuted OP_IF branch</td></tr>
<tr><td>OP_RESERVED2</td><td>138</td><td>0x8a</td><td><b>Transaction is invalid</b> unless occuring in an unexecuted OP_IF branch</td></tr>
<tr><td>OP_NOP1-OP_NOP10</td><td>176-185</td><td>0xb0-0xb9</td><td>The word is ignored. Does not mark transaction as invalid.</td></tr>
</tbody>
</table>


# Scripts

This is a list of interesting scripts. Keep in mind that all constants actually use the data-pushing commands above. Note that there is a small number of standard script forms that are relayed from node to node; non-standard scripts are accepted if they are in a block, but nodes will not relay them.

### Standard Transaction to Bitcoin address (pay-to-pubkey-hash)

    scriptPubKey: OP_DUP OP_HASH160 <pubKeyHash> OP_EQUALVERIFY OP_CHECKSIG
    scriptSig: <sig> <pubKey>


Note: `scriptSig` is in the input of the spending transaction and `scriptPubKey` is in the output of the previously unspent i.e. "available" transaction.

### Obsolete pay-to-pubkey transaction

`OP_CHECKSIG` is used directly without first hashing the public key.

This was used by early versions of Bitcoin where people paid directly to IP addresses, before Bitcoin addresses were introduced.

The scriptPubKeys of this transaction form are still recognized as payments to user by Bitcoin Core.

The disadvantage of this transaction form is that the whole public key needs to be known in advance, implying longer payment addresses, and that it provides less protection in the event of a break in the ECDSA signature algorithm.

    scriptPubKey: <pubKey> OP_CHECKSIG
    scriptSig: <sig>

### Provably Unspendable/Prunable Outputs

The standard way to mark a transaction as provably unspendable is with a `scriptPubKey` of the following form:

    scriptPubKey: OP_RETURN {zero or more ops}

`OP_RETURN` immediately marks the script as invalid, guaranteeing that no `scriptSig` exists that could possibly spend that output. Thus the output can be immediately pruned from the UTXO set even if it has not been spent.

[eb31ca1a4cbd97c2770983164d7560d2d03276ae1aee26f12d7c2c6424252f29](http://blockexplorer.com/tx/eb31ca1a4cbd97c2770983164d7560d2d03276ae1aee26f12d7c2c6424252f29) is an example:
it has a single output of zero value, thus giving the full 0.125BTC fee to the miner who mined the transaction without adding an entry to the UTXO set.

You can also use `OP_RETURN` to add data to a transaction without the data ever appearing in the UTXO set, as seen in
[1a2e22a717d626fc5db363582007c46924ae6b28319f07cb1b907776bd8293fc](http://blockexplorer.com/tx/1a2e22a717d626fc5db363582007c46924ae6b28319f07cb1b907776bd8293fc); does this with the share chain hash txout in the coinbase of blocks it creates.


#### Input Script

    3044022055bcb36c829a614451787fe8c9bfb3798b683809b65b92037a015e \
    ccb5ff659702202461d2c708a4fd57c839e43634e8c02935d7b7d1db5b9784 \
    32b0674c44645ed101 
    032c1ea520c25c4e66831cd395a3cd26f0e0a1472a3103fc8a4a63ef10e92d123c

####Output script

    OP_RETURN 215477656e74792062797465206469676573742e 


### Anyone-Can-Spend Outputs

Conversely a transaction can be made spendable by anyone at all:

    scriptPubKey: (empty)
    scriptSig: OP_TRUE

With some software changes such transactions can be used as a way to donate funds to miners in addition to transaction fees: any miner who mines such a transaction can also include an additional one after it sending the funds to an address they control. This mechanism may be used in the future for fidelity bonds to sacrifice funds in a provable way.

Anyone-Can-Spend outputs are currently considered non-standard, and are not relayed on the P2P network.

### Transaction puzzle

Transaction *a4bfa8ab6435ae5f25dae9d89e4eb67dfa94283ca751f393c1ddc5a837bbc31b* is an interesting puzzle.

    scriptPubKey: OP_HASH256 6fe28c0ab6f1b372c1a6a246ae63f74f931e8365e15a089c68d6190000000000 OP_EQUAL
    scriptSig: <data>


To spend the transaction you need to come up with some data such that hashing the data twice results in the given hash.

Data goes on the stack, as do results. Instructions operate on the stack.

<table class="ui compact single line table" style="font-size:50%"><thead><tr><th>Stack</th><th>Script</th><th>Description</th></tr></thead>
<tbody>
<tr><td>Empty.</td><td>&lt;data&gt; OP_HASH256 &lt;given_hash&gt; OP_EQUAL</td><td></td></tr>
<tr><td>&lt;data&gt;</td><td>OP_HASH256 &lt;given_hash&gt; OP_EQUAL</td><td>scriptSig added to the stack.</td></tr>
<tr><td>&lt;data_hash&gt;</td><td>&lt;given_hash&gt; OP_EQUAL</td><td>The data is hashed.</td></tr>
<tr><td>&lt;data_hash&gt; &lt;given_hash&gt;</td><td>OP_EQUAL</td><td>The given hash is pushed to the stack.</td></tr>
<tr><td>true</td><td>Empty.</td><td>The hashes are compared, leaving true on the stack.</td></tr>
</tbody>
</table>

This transaction was successfully spent by *09f691b2263260e71f363d1db51ff3100d285956a40cc0e4f8c8c2c4a80559b1*. The required data happened to be the Genesis block, and the given hash was the genesis block hash.

Note that while transactions like this are fun, they are not secure, because they do not contain any signatures and thus any transaction attempting to spend them can be replaced with a different transaction sending the funds somewhere else.

---


<!--
<script>
  var diagram = Diagram.parse("title: Pay-to-Bob script\nAlice->Bob: Authentication Request\nBob->Alice: Authentication Response");
  diagram.drawSVG("diagram", {theme: 'hand'});
</script>
-->

<script>
  $(".diagram").sequenceDiagram({theme: 'simple'});
</script>


