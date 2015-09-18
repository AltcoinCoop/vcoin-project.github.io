---
layout: socpage
title: School
excerpt: Some more formally-presented information
image:
  feature:
---

# [Title]()

## Header

How does Bitcoin work? What makes Bitcoin different? How secure are your Bitcoins? How anonymous are Bitcoin users? What determines the price of Bitcoins? Can cryptocurrencies be regulated? What might the future hold?

https://piazza.com/princeton/spring2015/btctech/home

- [Lecture 1 — Intro to Crypto and Cryptocurrencies](https://www.youtube.com/watch?v=fOMVZXLjKYo)
- [Lecture 2 — How Bitcoin Achieves Decentralization](https://www.youtube.com/watch?v=q5GWwTgRIT4)
- [Lecture 3 — Mechanics of Bitcoin](https://www.youtube.com/watch?v=t3hJsFpPmXs)
- [Lecture 4 — How to Store and Use Bitcoins](https://www.youtube.com/watch?v=NKqHXoYZvMg)
- [Lecture 5 — Bitcoin Mining](https://www.youtube.com/watch?v=jXerV3f5jN8)
- [Lecture 6 — Bitcoin and anonymity](https://www.youtube.com/watch?v=glyQy_e5LmM)
- [Lecture 7 — Community, Politics, and Regulation](https://www.youtube.com/watch?v=IRbgZUGHn9g)
- [Lecture 8 — Alternative Mining Puzzles](https://www.youtube.com/watch?v=TipGy2bOVL4)
- [Lecture 9 — Bitcoin as a Platform](https://www.youtube.com/watch?v=aM3OP4gazWw)
- [Lecture 10 — Altcoins and the Cryptocurrency Ecosystem](https://www.youtube.com/watch?v=l-3kOuF0dts)
- [Lecture 11 — The Future of Bitcoin?](https://www.youtube.com/watch?v=YG7l0XPtzD4)
- [Lecture 12 — The History of Cryptocurrencies [Bonus lecture]](https://www.youtube.com/watch?v=1VYs_zZsorU")

## Blockchain-based services

### [Applied Blockchain](http://appliedblockchain.com/)

#### TRUST

If two or more organizations exchange information that requires a level of trust between them (e.g. transactions, legal contracts), then a distributed blockchain solution allows this to be achieved without the need for a trusted intermediary.

#### DATABASE

Store data in the blockchain using smart contracts. Once stored and confirmed by the blockchain, the data is distributed across the participating nodes, and the fact that the data was stored cannot be refuted. Add permissions to the smart contract, and only specified parties can see, modify or transact with the data.

#### WORKFLOW

Design workflow to run in the blockchain using smart contracts. Allow specific participants to perform tasks in a predetermined sequence. Each activity is distributed to participating blockchain nodes, and recorded in the immutable history of the blockchain.

#### END TO END

We design and build end-to-end smart contract applications that run on private / consortium blockchains. These include using smart contracts to store and share data, as well as running complex workflow. Blockchain applications can be integrated with enterprise applications using standard REST, SOAP, or files. Our solutions integrate web and mobile applications directly with the blockchain.

#### AGNOSTIC

Although we love Ethereum-style smart contracts, we are blockchain agnostic, and develop solutions using a number of different blockchain implementations. We also compare the different platforms' performance and attributes in our lab, and provide impartial advice on the best fit for a project.

#### TALLYSTICKS

Our very own Tallysticks framework enables fast delivery of smart contract applications that can be managed and scaled in an enterprise environment.

---

### [Augur](http://www.augur.net/)

#### Prediction Markets
Prediction markets allow their users to buy and sell shares in the outcome of an event. The current market price of a share is an estimate of the probability of an event occurring.
 
If there's a prediction market on whether Hillary Clinton will win the 2016 election, a share of yes that costs 60 cents means she has a 60% chance of winning according to the market.
 
The Iowa Electronic Market allows its users to wager on the outcomes of U.S. political events. It typically predicts elections within one percent, more accurate than polls or expert opinions. Since 1988 it has correctly predicted the outcome of every U.S. presidential election.


#### Why decentralize?
Historically, prediction markets have fallen short due to dated jurisdictional regulation, lack of volume due to limited payment options, a paltry number of markets, and sometimes even paying out the wrong people!
 
The root of these problems stems from centralization — an issue solved by blockchain technology. Our prediction markets eliminate counterparty risks, centralized servers, and create a global market by employing cryptocurrencies including bitcoin, ether, and stable cryptocurrencies. All funds are stored in smart contracts, and no one can steal the money. 
 
Augur's interface is currently in English, but we have plans to make it available in other common languages, starting with Chinese and Spanish.

### Demonstration runthrough

When you load the alpha in your browser you'll see a few things.  

- On the top right is your play money “Cash” in Augur right now, it should say 0.  
- On the left hand side there is a menu along with some information about the Ethereum network.

#### Let's get you some money!  

1. Click on “Account” on the left hand side, then you'll see a few buttons.  

2. Click on “Faucet”, which is next to cash.  

    - Here you can send cash, reputation, and ether.  

    - You'll also notice your “Reputation” and “Ether” balance.  

3. If you want some reputation, click on that faucet button as well.

Now you're ready to create a market or participate in one!  

#### Let's participate first:

1. Click on “Markets” on the left hand side.

2. A bunch of events should load.  

3. Click on one that seems appealing.  

4. Now you can buy shares in an event.  

5. If you think the event is going to happen, buy “yes” shares, otherwise buy “no.”  

6. Input the number of shares you want to buy.  

    - You'll see the current price per share of each outcome; if you buy at, say, 40¢, and you are correct, later on each share you buy will be worth $1.00.  

7. Depending on how many shares you buy, you will be told how much you're moving the odds by purchasing, as well as how much you're purchasing.  

    - If you buy 5 shares, and it costs something like $3, if you're, right you'll get $5 once the market closes, for a profit of $2!

8. Now that you own shares you can sell them if you like.  

#### Now, let's make a market!:

1. Choose “Submit a Market” on the top right

2. Input a description/question you want that market to be on.

    - It should be a yes or no question.  

3. Input how much initial liquidity you want to provide and set a trading fee.  

    - If you provide a lot of liquidity but few people use your market, you'll probably lose some money.  

    - If you provide liquidity and a lot of people use your market, you'll make money off trading fees.  

    - Too little liquidity and people won't trade (due to buying a few shares moving the price a lot). 

    - Too much liquidity and you won't make enough money on trading fees to earn a profit.  It's a delicate balance.  

4. Choose an expiration date for your market.  

    - This should be sometime after your event occurs.  

5. Submit it!  

6. After a couple of blocks, your market will be ready for trading.

#### Reporting (Ballot in UI):

To initiate payouts for markets on Augur, we need a way to distribute funds from losers to winners and to determine what the correct outcome is.  To determine the outcome we use reporting.  Holders of our token, “Reputation”, or “REP”, report on the outcomes of events.  

1. To try this out, click on “Reporting” on the left hand side. If there are events that have expired which haven't been reported on yet they'll show up here.

2. For each question, choose either "Yes" (meaning it happened), "No" (meaning it didn't), or "Indeterminate" (meaning you're not sure if it happened or it's impossible to determine if it happened, or the market is unethical.)

3. When you're done, click “Submit Ballot” on the bottom right.  

    - Note that your client has to be on during the ballot reveal period (when the bar at the top is in the second half) for your report to be submitted and counted.  

4. Consensus will be done and we're ready to close the markets whose outcomes have been decided.

#### Market Closing:

1. To close a market (if you created it or wagered in it) go to the “Markets” page.

2. Find the respective market.

3. Click “close.”

     - You will also be able to close markets from the “Accounts” page where it shows your holdings.  

4. Then the market will be closed and payouts will be done.  Congratulations if you participated and won, and better odds next time if you didn't!

---

### [Bitnation](http://bitnation.co/)

BITNATION is a decentralized, open-source movement, powered by the Bitcoin blockchain 2.0 technology, in an attempt to foster a peer-to-peer voluntary governance system, rather than the current ‘top-down’, ‘one-size-fits-all’ model, restrained by the current nation-state-engineered geographical apartheid, where your quality of life is defined by where you were arbitrarily born.

We’re a holacratic organization and we strive to become a fully functional Decentralized Autonomous Organization (DAO). In non-geek terms, this means that there are no formal management structures, there are no barriers to entry, and everyone can join and create their own operational centers (“holons”) whether for-profit or nonprofit, or join an existing one, all while benefiting from the greater support and technology from the BITNATION community.

---

### [Bitproof.io](https://bitproof.io/)

#### Prove, protect.

We live in a broken world. From finance to private property, major parts of our lives rely on easy-to-forge pieces of paper called contracts.

Bitproof created SealX, a tool that lets you create frosted contracts. They're sealed forever and valid worldwide.

#### Be a genius, be safe.
Entrepreneurs create ideas. Engineers create products. Artists create dreams. All of this can be protected.

Bitproof created GeniusX, a tool that lets you protect your Intellectual Property. Drag and drop, boom, you're done.

#### Valid in court worldwide.
Your certificates are stored in a super secure database replicated all around the world. As a result, they are valid everywhere.

With Bitproof, International Business becomes easier.

---

### [BlockVerify](http://www.blockverify.io/)

#### We Can Verify The Following

- **Counterfeit Products** A product that is already in possession and is determined to be counterfeit

- **Diverted Goods** The system is able to identify if a product was diverted from its original destination

- **Stolen Merchandise** The system can easily trace and locate stolen merchandise

- **Fraudulent Transactions** Block Verify can track fraudulent transactions of any type throughout the system

#### Use Cases

- **Pharmaceuticals** Solution to track pharmaceuticals throughout the supply chain and to ensure the consumers receive an authentic product

- **Luxury Items** We work directly with luxury manufacturers to build a system of verifying luxury goods. This will provide quality assurance for all parties

- **Diamonds** We created a system that can enhance trust in diamonds certificates and prevent fraud

- **Electronics** We work directly with manufacturers to make sure that customers are getting original equipment

#### How Blockverify Works
The process a product goes through to ensure authenticity:

- **Product Labelling**: Each product is labelled with Block Verify tag

- **Verified Supply** Each product is verified along the supply line. Supply chain becomes transparent to the extent we want it to be

- **Consumer Verified**
When the consumer purchases a product he/she is able to verify that the product is genuine and activate it

- **Anti-corruptible**
We ensure that each product is validated and recorded prevent even companies from counterfeiting their own goods

- **Retail Verification**
Retail locations can use mobile devices for verification. They can be assured that the goods they receive are genuine

- **Block Verified**
Each product has a recorded history permanently recorded in the blockchain. We can provide verified history for each product

---

### [Chimera](http://www.chimera-inc.io/)

We are the missing puzzle in connecting your home, office, garden, car and appliances to the Internet of Things. We built our infrastructure robustly, from the ground up, using secure cryptography networks, enabling you to connect with your devices from wherever you are, while enjoying higher reliability, lower latency, and world-class security.


#### SMART REMOTE

Use your smartphone like a regular remote control. No more hide and seek with all your remotes. Control all appliances in style, and impress your friends!!

- JANUARY: Development of the Operating System. Linux KVM with custom packages.
 
- FEBRUARY: Native mobile apps. Android and Windows. And Web App.
 
- MARCH: System Security, Node JS with bitcoin Crypto-Currency. Web backend and Backend.
 
- APRIL: IOS App. Hybrid. Frontend Web. Artificial Intelligence

---

### [Colu](http://colu.co/)

- **Colu Engine**: Create your digital assets, attach a value and integrate them with your project.

- **Reducing Bitcoin Complexity**:

    - Quick issuance on top of Bitcoin's Blockchain using the Colored Coins protocol. 
    - The Engine funds the transaction for you - your users don't need to hold bitcoins!

- **Easy Integration**: Powerful RESTful API and SDK for easy integration with the Colu platform.

- **Enterprise Oriented**: Reliable, fast and secure infrastructure ready for high volume usage.

---

### [Etherparty](http://etherparty.io/)

We are a Platform as a Service managing and executing Smart Contracts.

Etherparty is a platform that removes the complexity and management of creating and executing smart contracts

Etherparty is a PaaS with a process model designed to fit a wide range of distributed applications allowing for quick deployments.

- Visual Editor: No programming required.
- Contract Library: A community curated Library.
- Dashboard: Monitor everything in one place.

##### INFINITELY SCALABLE

Etherparty framework allows for infinite scalability to match the needs of the Smart Contract as necessary. For distributed computation this is extremely useful for resource allocation.

##### PROCESS AUTOMATION

Deploying Smart Contracts relies on a back end of packages, modules, and libraries. Etherparty automates this process by preconfiguring these dependencies to just a few clicks of a button.

##### CONNECT YOUR DATA

Our focus is workflow management regardless of the data source being used for the Smart Contract - connect your CRM or Accounting API. We bring the power of Smart Contracts to the Web.

##### CLICK TO DEPLOY

Execute Smart Contracts in less time without the hassle and complexity of setting up and maintaining the source code and infrastructure beneath it. We bundled and tested it so you don't have to.

---

###[everledger](http://www.everledger.io/)

We are a fraud detection system overlaying big data from closed sources like insurers and law enforcement.

Everledger is a permanent ledger for diamond certification & related transaction history. Verification for insurance companies, owners, claimants and law enforcement.

Our technology can be extended to track any asset that carries a unique identifier which is difficult to destroy or replicate.


#### What is a smart contract?

Smart contracts are computer protocols that facilitate, verify and enforce the performance or negotiation of a contract.

Think of a traditional legal contract where there is no need for a third party to enforce the clauses within it. It sounds easy, but this is in fact what makes it 'smart’.

For example, if Alice and Bob sign an agreement stating that the ownership of a digital asset, like a song, is transferred only if a certain amount of money is sent from Alice to Bob within day, and Bob pays in time, a smart contract transfers that ownership automatically without the need for any third party.

A smart contract would also decline the transfer of ownership if Bob does not pay in time.

#### What kind of technology do we use?

For our smart contracts, we combine our private blockchain based on the Eris stack with a public blockchain(Bitcoin) in order to achieve a hybrid model; neither fully public, nor fully private.

We do this in order to get the best of both worlds; high security of a public blockchain, and the complexity and amiability of a smart contract enabled private one. Our smart contracts are also Ethereum ready and will be deployed to it when the Ethereum blockchain moves out of test phase.

---

### [Filament](http://filament.com/)

Drop-in wireless infrastructure that's flexible and secure.

**The Filament Tap** lets you deploy a secure, all-range wireless network in seconds.

Taps can talk directly to each other at distances of up to 10 miles, and since each Tap has BLE, you can connect to them directly with your phone, tablet, or computer.

With built-in environmental monitoring, a USB port for your own sensor or device, and a battery life of up to 20 years, it's the perfect grab-and-go connectivity solution.


**The Filament Patch** adds all-range wireless to your own hardware project.

It's a certified, surface-mount module with everything you need to build your own Filament network, including dedicated crypto hardware, sub-GHz and BLE radios, and compact chip antennas.

We've optimized every component for low-power and high-performance, so it's ready for projects at any scale, and in any environment.

Filament gives you standalone wireless networks that don't require any central routing service or "cloud". This lets you deploy secure, decentralized systems in any environment, without depending on WiFi or Cellular coverage.

Our hybrid radio hardware combines a long-range, high-performance sub-GHz radio, with ubiquitous device-range BLE. This let's our products achieve a remarkable wireless range of 10 miles, while remaining accessible from your mobile device.

Combining these radios lets Filament devices perform well in even the most challenging environments. We can cover miles of open air, or cut through multiple city blocks.


- **Remote Monitoring:** Bring your existing equipment online, and monitor your operations remotely. Taps can stay in a low-power mode for years until they detect an alert condition.

- **Data Collection:** Wireless data collection has never been easier. Monitor environmental conditions with the Tap's built-in sensors, or plug in your own.

- **Smart Cities:** Our long-range radios are perfect for city-wide infrastructure projects, where you need to deploy thousands of devices in a dense urban area.


### [Filecoin](http://filecoin.io/)

- Earn Filecoin by renting disk space 

- Use Filecoin to store files in the network or to transact 

- Exchange Filecoin for other currencies, like Bitcoin

---

### [FollowMyVote](https://followmyvote.com/)

Follow My Vote has designed the software for an online voting platform, which is both intuitive and easy to use. Users download the voting booth and get their identity verified by a third party for authorization to cast a ballot. The voter submits their vote to the ballot box which is stored securely on a blockchain. In addition, voters can audit their vote to ensure that their voice has been heard.

Follow My Vote began originally as a polling system designed to ensure that elected representatives were truly voting in the interests of their constituents.

However, Follow My Vote soon entered into a joint venture with BitShares; effectively shifting its focus to the development of a verifiable online voting platform secured with the BitShares blockchain technology.

In order to ensure the success of the venture, Follow My Vote moved from their previous location with NuSpark into a shared space in Virginia Tech's Corporate Research Center.

The blockchain is the PKI in our designs. Using a blockchain as a PKI is a practical scenario, and the BitShares blockchain already does just this by mapping usernames to public keys. What this looks like in the voting context is that a user creates a key pair, and publishes the public key on the blockchain as an identity, then uses that key to sign a request for an ID verifier to certify that on-chain identity as being unique and authorized to vote. The exact procedure by which the verifier determines the identity of the person making the request is out of scope for the voting system, but we have a general procedure outlined which closely mirrors that of getting your identity verified for an SSL certificate today.

In order for votes to be considered official votes within our voting system, voters must have their identities verified prior to casting their ballots. Voters can only request official ballots for elections that meet their account credentials (i.e. country of citizenship, age, etc.) and can only request one ballot per election. During the ballot casting process, voters can rest assured knowing that their ballots will not be tampered with, as cryptography technology prevents voters’ ballots from being intercepted and modified prior to being stored in the blockchain-based ballot box. Once a voter’s vote has been stored in the blockchain-based ballot box, it cannot be changed by any other voter within the system. Finally, all voter’s that participate in an election will have an opportunity to audit the ballot box themselves to ensure that the vote count of the ballots stored in the ballot box match the election results being reported.

---

### [Gems](http://getgems.org/)

GetGems is a free mobile app available for iOS and Android. It makes instant messaging with friends fun, simple, secure and profitable.

- **Fun.** Keep in touch with friends. Free unlimited instant messaging.
- **Simple.** Your passphrase is your wallet. Fully functional in under 30 seconds.
- **Secure.** Be as anonymous as you desire. Communications are always encrypted.
- **Profitable.** Be rewarded for introducing new users to the network.

Daily airdrop of Gems - Every day, ~27,500 Gems are air dropped from the Exodus Address. The ecosystem automatically distributes these Gems between users according to their relative network contribution. Contribution is measured by the number of active daily users which were introduced by you to the network so far.

Since daily airdrop rewards users who introduce other users, who is rewarded for those who come without a special invitation? Uninvited users will be attributed to random Presale buyers. In addition, air drop share is multiplied by total gems owned. The more Gems you own, the more Gems you make - an advantage to those who accumulate Gems first.

100 million Gems is the total currency supply in the GENESIS BLOCK. Eventual supply is achieved as follows: 50 million Gems distributed to stakeholders; 30 million Gems distributed as daily Airdrop rewards during ~3 years after launch; 12 million Gems reserved for bonus block rewards, promotion, marketing, bounties; 8 million Gems + Presale BTC will fund the network R&D and operation costs.

The Gems currency is powered by Counterparty. Every GetGems user automatically gets his own wallet, protected by the passphrase chosen on registration. The social network username is an alias to the GetGems address, making sending & receiving Gems and bitcoins between users as easy as possible.

---

### [Monegraph](https://monegraph.com/)

#### What is Monegraph?
Monegraph is a technology that lets you, in a permanent and public way, claim your work as your own and set its rules for use. Anywhere that work goes, when it is used, you get paid. Built on the oldest and most secure public ledger, Monegraph uses blockchain architecture to establish and link the author of a work to its title of ownership, its constellation of usage rights, and payment terms for handling those rights.

#### What types of digital work can be Monegraphed?
Monegraph was conceptualized by Artist/CEO Kevin McCoy at Rhizome’s Seven on Seven conference in 2014. The initial version supports digital images, photos and animating GIFs. We are working to support many other media types and source file formats in the near future.

#### When can I start using Monegraph?
Beginning July 14, Monegraph is inviting its inaugural group of creators to the platform. Drawn from a range of creative industries spanning art, fashion, photography and design, these pioneers will frame the opportunities that Monegraph brings to their fields. We will be expanding the private beta to a larger user base in August and plans to officially launch to the public in September 2015.

Kevin McCoy: I’m an artist. My artwork is produced in collaboration with my wife Jennifer. For a long time we’ve been doing work that intersects with technology, broadly speaking. I’m also a professor in the art department at NYU. I oversee the digital practices in the art department. In May of last year I presented a concept called Monegraph at Rhizome Seven on Seven at the New Museum and since that time, I have slowly been working to develop it as a platform.

Artist and professor Kevin McCoy's platform Monegraph launches in September. The service offers an online marketplace as well as a licensing system based on similar encryption technology used by Bitcoin and other so-called "cryptocurrencies."

---

### [Onename](https://onename.com/)

Register your blockchain ID with Onename

- **Choose a unique name** This is the name you share so others can find your blockchain ID. If you keep your password safe, no one can take this name from you.

- **Create and verify your profile** Link your blockchain ID and social media profiles together to prove ownership of your blockchain ID and verify it's really you.

- **Start using your blockchain ID** Share your blockchain ID on your website, social media profiles, and business cards so people can easily find you online.


Help others send you Bitcoin:

- Link to your blockchain ID in your email signature
- Embed your blockchain ID on your blog
- Display your blockchain ID on your twitter page


Share your details while maintaining privacy:

- Share your contact info privately with select individuals
- Use stealth addresses for private payments
- Share your PGP Key, OTR Key and BitMessage address for private chat

---

### [Otonomos](http://www.otonomos.com/)


We put your company on digital rails

Open a share wallet to write real-world company shares on the blockchain, transfer equity peer-to-peer, and govern your company using smart contracts.


- **Online Formation** Incorporate in a leading real-world jurisdiction by simply creating an online share wallet, or have us dematerlialize your existing private limited company shares.
- **Peer-to-Peer Funding** Transfer equity peer-to-peer to attract co-founders, remunerate collaborators, invite new investors or the crowd at large. Know you captable at all times.
- **Automated Governance** No matter how dispersed your share ownership, our technology helps you automate governance of your company using self-enforceable, smart contracts.

#### We make this work in leading real-world jurisdictions

Whether you already own a private limited company or need us to help incorporate a new one, Otonomos can help dematerializing your share certificates and write them on the blockchain.


See who your shareholders are at all times. Transfer equity peer-to-peer.
Manage your Boardroom and shareholder voting online. Update your company's constitution in one click

Click here to read more about blockchain, and the Ethereum protocol on which Otonomos is built.


- **No Server Silos:** Blockchain is a distributed ledger that sits on the computers of each participant in the network, who each contribute in the running of the network, without central servers.
- **Cryptography at Work:** By opening a share wallet or making a share transfer, you are writing transactions to the blockchain. Cryptography makes sure these are verified as unique and tamperproof.
- **Smart Shares:** Smart shares emulate a computer executing a program: They have your company's governance protocols embedded and can help execute events on which your Board or your shareholders voted.

---

### [ShoCard](http://www.shocard.com/)

ShoCard is a digital identity that protects consumer privacy and is as easy to understand and use as showing a driver’s license. It’s optimized for mobile and so secure that a bank can rely on it.


- **Consumer-friendly:** No hard-to-remember passwords, no complicated code generators, no obscure challenge questions. ShoCard works on your phone, so it’s always at hand.

- **Secure:** ShoCard protects and verifies identity using strong public/private key encryption with multiple keys, data hashing, out-of-band communication, data matching, and two-factor authentication.

- **Always-on:** ShoCard’s game-changing pricing means almost no marginal cost to our customers for verifying identity. Banks and others can check identity on every transaction, virtually eliminating fraud.

---

### [Storj](http://storj.io/)

Decentralized Cloud Storage

Storj is based on blockchain technology and peer-to-peer protocols to provide the most secure, private, and encrypted cloud storage.


**DriveShare**

Do you have unused internet bandwidth and hard disk space on your computer?

Put your computer to work for you with our desktop application, DriveShare, and earn money for being a part of the Storj network.

Just run our app, DriveShare, and choose the amount of free hard disk space you want to provide.


**MetaDisk**

Using our web application, MetaDisk, you can upload your data to the Storj network with a simple drag and drop.

Your files are protected and encrypted on your computer before they go into the network and only you, with your private key, have access to your data.

You can even earn cloud storage on MetaDisk by sharing your hard drive space with DriveShare.

---

### [Swarm](https://swarm.fund/)

**What is Swarm basic income?**

Every time a project is created through Swarm, a part of that project is automatically given to all Swarm members. This allows all Swarm members to participate in the distributed abundance made possible by the Swarm.


**How can I create my own DCO?**

Check out this [this guide](https://medium.com/@rubenalexander/f443bc686335) to see how you can create your own DCO.

**Why would I want a DCO?**

Setting up a corporation or non-profit is expensive. DCOs cost nothing to set up. Creating or distributing shares is expensive. With DCOs it is practically free. DCOs allow you to organize bottom up instead of top down and distribute abundance to every member who contributes.

**What is Swarm?**

A collaboratively owned membership network decidated to facilitating abundance. You can read about the history of the Swarm [here](https://medium.com/@Swarm/history-of-the-swarm-83ff0fc80a8).

---

### [Synereo](http://www.synereo.com/)

Attention economy

---

### [thingchain](https://thingchain.com/)

Provenance tracking for products from a diverse array of industries.

Popcodes are unique cryptographic QR codes that can be tracked, possessed and transferred with the thingchain API


The Thingchain API makes it easy for developers to build applications to securely track goods as they change ownership.

The underlying architecture that the API exposes is:

- a customized fork of the Bitcoin Blockchain that has been modified to accommodate the specific needs for the tracking of goods
- a searchable index of the blockchain

View the full API reference [here](https://thingchain.com/api).

#### Concepts

##### Identity

Real world identities are represented by a cryptographic key-pair. This key-pair is typically generated by the application on the client device, ensuring that only the client device has possession of the private key. Thingchain offers an in-browser javascript file and a server side nodejs npm package for key generation.

Transactions that transfer ownership on the Thingchain must be signed by the identity key of the individual creating the transaction.

Thingchain maintains a relationship between registered public keys and real world identities.

##### Popcode

A Popcode (Pop == Proof-of-Provenance) is a thing’s unique digital identifier (consisting of a Bitcoin-style private/public key-pair & address) and its associated value, metadata and provenance on the blockchain. For instance, a Popcode may contain 24 bottles or 1 widget or 300 Kgs. The term popcode typically refers to the address.

Popcodes are generated through a secure key derivation function on the thingchain server.

##### Tracking

A thing’s popcode is created, or minted, when user Alice’s identity sends value into the popcode’s public address.

To obtain this value, Alice’s identity address must withdraw it from the thingchain “faucet”, or master address.

When Alice ships the thing to Bob, Bob receives the private key and takes possession of the popcode by sending the value in the popcode address to her identity address. At this stage, the popcode cannot be duplicated and possessed by another user because the address contains no value.

When Bob is ready to ship the thing to Charlie, he releases the popcode by sending the value from his identity address back to the popcode. Charlie is now able to take possession of the popcode and continue the chain of custody.


---

### [Tierion](https://tierion.com/)


Tierion is an engine for collecting data and recording it in the blockchain

Tierion is a simple and powerful way to collect data, record it in the blockchain, and slingshot it to the applications that drive your business. Protect the integrity of your data with the world's most secure and resilient database — the Bitcoin blockchain.

- **Collect Data From Web & Mobile Apps** Submit data to our REST API or via HTML forms.
- **Record Your Data In The Blockchain** Tierion automatically records each record in the blockchain and generates a blockchain receipt.
- **Slingshot Your Data To Other Systems** Automatically send your data to the applications you use to run your business.

#### What is a blockchain receipt?
We’ve developed an open standard called Chainpoint for recording data in the blockchain and generating blockchain receipts. Each receipt contains all the information needed to verify the data without relying on a trusted third party.


Tier 4 - High Volume 150,000 records per month • Unlimited Datastores $199 per month

---

### [Tradle](http://tradle.io/)

We help externalize transactions to scale world commerce

- **Why Bitcoin?** blockchain automatically and irreversibly serializes transactions: Human activities will be more transparent, yet more secure, more automatic, yet touching more people, more coordinated, yet more diverse

- **Non-financial transaction** Bitcoin only carries financial transactions: Tradle extends it to securely externalize ANY transactions, like travel, dating or CRM, ERP, B2B. This creates a new extremely simple way to do commerce globally

- **Network Effect** Transactions often have 2 or more participants: When you send transactions to friends and businesses, it gives them more value if they join in, always widening the circle


HOW DOES TRADLE DO IT?
with an inclusive open source project and proprietary business tools

- **Community effort** Tradle community develops crypto log on blockchain:
 Open source project with highly compartmentalized data encryption, audited dynamic access allocation, irreversibility, with a choice to be more or less transparent

- **Advantage of existing tools** Not just a REST API, full stack tools: Open source mobile framework combined with the business app dev and integration platform allow Tradle build full-stack sophisticated blockchain apps today

- **Unique app concepts** We invite partners to use our ideas for new types of apps: For the first time in history we are able to connect apps, people and businesses without a trusted company in between. Let's build those apps together.

---

### [Trustatom](https://trustatom.com/)

Privacy-respecting identity & smart contract solutions for enabling credibility, trust and safety

#### Next generation multifactor authorization

Trustatom ID mobile workflow relies on strong cryptography for criticial action authorization.

Unlike in traditional "type this number sequence" schemes (TOTP), user's authorization signature can't be forged, enabling higher level of protection and better audit trail. And yes, no need re-type the numbers in the next 5 seconds!

Trustatom ID authentication is a public service, delivered free of charge. Majority of the workflow happens outside of Trustatom servers and Trustatom has no access to private information.


#### Trustworthy identity & credentials

Knowing who is on the other side of the connection has always been a challenge.

What's even more complicated is knowing sufficiently enough about that person to conduct business with her. With Trustatom ID users can easily share isolated pieces of their information (residency, age, banking information, contacts etc.) signed by trusted third parties upon request.


#### Smart Contracts

Our Contract API are designed to help third party applications to use robust, pre-designed building blocks for different kinds of contracts: document certificates, joint escrows, etc. This API is also seamlessly integrated with Trustatom ID, removing the need to reinvent anything.


#### Niche solutions

Trustatom powers highly tailored solutions for specific industries and niches to maximize the potential of the technology.

The first solution is Streamline.VC, an application that helps investors and companies to establish continuous credibility during the due diligence and post investment.

#### Better UX
Nothing replaces a better, smoother user experience. Trustatom ID technology does not use the traditional approach that requires users to enter a number they see on their phone within a very limited period of time (for example, 30 seconds).

Instead of that, user's phone securely stores a master keypair that is used to sign each and every third party authorization request. The workflow the user is exposed to is very simple. It involves scanning a QR code, and authorizing the app to sign an action-specific, clearly rendered request.

#### Secure

We designed our security scheme to have the right balance of usability and security guarantees. It's a combination of such techniques as: "limited gain" first factor authentication, highly guarded privacy, true off-band communication, use of trusted secure hardware open sourcing our mobile app.

Our scheme allows users to clearly see what kind of authorization they are giving to a third party application and these signatures can't be forged by anybody.

Lastly, but not least importantly, Trustatom ID uses state of art cryptography primitives, such as ECDSA, BIP32, ECIES and SHA256. Our scheme is being reviewed by various experts in the field. Our paper will be soon released to the public.

#### Audit Trail

The very nature of authorizations signed by users allows for granular permission grants that can be irrefutably pinpointed in time, when used in conjunction with Trustatom Smart Contracts API. This allows third party application providers to keep a perfect audit trail of all authorizations forever, ensuring their conformance to their processes and compliance level they are regulated by.

#### Trusted credentials

One of the very important features of Trustatom ID is that it allows third party applications to request relevant pieces of information about the user, without being exposed to all of it (thus violating user's privacy). These chunks of information are provably signed by trusted third parties that Trustatom has partnered with.


---

### [Verisart](http://www.verisart.com/)

Verisart is launching soon. Sign up to learn more about a new way to track and verify works of art.

---

Bitcoin as commodity:

Buying with BTC is a breath of fresh air, huh? How about when taxes are due?

If you're a US taxpayer, you are required to report the profit/loss of every single purchase made with bitcoin.

Which means that you need to dutifully look up and record the current price of bitcoin every time you make a purchase, so you can properly report the fair market value, and then copy that information over to Schedule D in the proper format.

And according to the tax rules, if you've made several purchases of bitcoins over time, then you have to separate the purchases into lots. So if you bought 0.3 bitcoin on Mar 1st and 0.2 bitcoin on Mar 31st, and you bought a video card for 0.4 bitcoin on May 2nd, then you have to decide from which of the previous lot(s) you want to take bitcoins on to report the profit/loss at the time when you bought the video card. For each separate lot, a separate line needs to be created (or you may put VARIOUS, and figure the correct gain/loss and just add that to the form, its up to you)

Of course, if its been more than a year between the time you made some of those purchases, you need to separate out the gain/loss into long-term vs short term gains.

And then, if you decide to refill your bitcoin account within 30 days before or after a purchase, and the bitcoin price went down from the time you bought it until the time you made your purchase, then wash sale rules come into play. In those cases, you need to report the sale, and then further mark it as a wash sale, reverting the loss on the form. Then those bitcoins that you sold and rebought have to be put back into your lots of bitcoins to use for further purchases, adding together to the final sale in the future the total loss and gain made by all the wash sales those bitcoins may be a part of (all while respecting the long term/short term gain split).

---

## Key and address specs

case 1:
  * secret (hex): 1111111111111111111111111111111111111111111111111111111111111111
  * uncompressed:
    * secret (base58): 91iS7EZqPeRGqPXcPiKLtbfjfLVUYYj17oQ54H3iFFw3n1UmZSS
    * pubkey (hex): 044f355bdcb7cc0af728ef3cceb9615d90684bb5b2ca5f859ab0f0b704075871aa385b6b1b8ead809ca67454d9683fcf2ba03456d6fe2c4abe2b07f0fbdbb2f1c1
    * address (base58): VXXWS2sMVZnwJE6HqdMPRJvW8ShMT9xKWi
  * compressed:
    * secret (base58): cN9spWsvaxA8taS7DFMxnk1yJD2gaF2PX1npuTpy3vuZFJdwavaw
    * pubkey (hex): 034f355bdcb7cc0af728ef3cceb9615d90684bb5b2ca5f859ab0f0b704075871aa
    * address (base58): VZg39gnYxrfh5mNZ8ivC86B85r8Ron95sz

case 2:
  * secret (hex): dddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddd
  * uncompressed:
    * secret (base58): 93GdT28G5Bm49FCB7n1k449ZCEBefWbhkK4A3zoEEywMmcwU2gm
    * pubkey (hex): 04ed83704c95d829046f1ac27806211132102c34e9ac7ffa1b71110658e5b9d1bdedc416f5cefc1db0625cd0c75de8192d2b592d7e3b00bcfb4a0e860d880fd1fc
    * address (base58): VUdaFXFTTUdjsUVUaCmixdEwDw3XVTj2AY
  * compressed:
    * secret (base58): cV1ysqy3XUVSsPeKeugH2Utm6ZC1EyeArAgvxE73SiJvfa6AJng7
    * pubkey (hex): 02ed83704c95d829046f1ac27806211132102c34e9ac7ffa1b71110658e5b9d1bd
    * address (base58): VXyed2ytF6hnpWRe8TJS8ghEMxusL3G4VB

case 3:
  * secret (hex): 47f7616ea6f9b923076625b4488115de1ef1187f760e65f89eb6f4f7ff04b012
  * uncompressed:
    * secret (base58): 928cSrNCuL6kPYy9EHejxR8v7nHPuXX1X1wH49bPhpeVZjq4b7B
    * pubkey (hex): 042596957532fc37e40486b910802ff45eeaa924548c0e1c080ef804e523ec3ed3ed0a9004acf927666eee18b7f5e8ad72ff100a3bb710a577256fd7ec81eb1cb3
    * address (base58): VZ1G1SrCcZdZExENc69XPggEdtNtH8FFTZ
  * compressed:
    * secret (base58): cPzbT6tbXyJNWY6oKeVabbXwSvsN6qhTHV8ZrtvoDBJV5BRY1G5Q
    * pubkey (hex): 032596957532fc37e40486b910802ff45eeaa924548c0e1c080ef804e523ec3ed3
    * address (base58): VKGy56BMnxAcCkuQ23NXK8Ug7PsHiWy5CJ

-- 
# “Cross my heart and hope to die”
Consider the scenario where Alice makes an important discovery.

It is important to her that she receives recognition for her breakthrough, however she would also like to keep it a secret until she can establish a suitable infrastructure for monetizing it. By forgoing publication of her discovery, she risks Bob independently making the same discovery and publicizing it as his own.

Folklore suggests that Alice might mail herself a copy of her discovery and leave the letter sealed, with the postal service’s timestamp intact, for a later resolution time. If Bob later claims the same discovery, the envelope can be produced and opened.

In reality, this approach does not work as (among other shortcomings) most postal services are pleased to timestamp and deliver unsealed empty envelopes that can be retroactively stuffed with “discoveries.”

## CommitCoin protocol
If Alice can put her commitment value into a Bitcoin transaction, it will be included in the chain of puzzles and the network will provide carbon dating without Alice having to perform the computation herself.

Bob only has to trust that Alice cannot produce a fraudulent block chain, longer than the canonical one and in less time (which would, incidentally, allow Alice to claim all the rewards for the fraudulent portion).

This idea has been considered on the Bitcointalk message board [10] in the context of the distributed network vouching for the timestamp. Our observation is that even if you do not trust the timestamp or any node in the network, the proof of work itself can be used to carbon date the transaction (and thus commitment value).

Alice has control over three parameters in a Bitcoin transaction: her private key(s), her public key(s), and the randomness used in the signature algorithm which, importantly, is ECDSA.

If she sets the receiver’s public key *(technically, the fingerprint of the public key)* to be her commitment value `c` and sends 1 BTC to it, the 1 BTC will be unrecoverable.

We consider this undesirable for two reasons: (a) it is financially wasteful for Alice and (b) it is not being a good citizen of the Bitcoin community.

By setting `c` equal to a private key or the signature randomness and following the protocol, `c` itself will never directly appear in the transcript.

To get around this, Alice sets `c` to the private key of a new account and then purposely leaks the value of the private key by signing two different transactions with the same randomness.

*(The CommitCoin protocol is given in Protocol 2.)*

Since `c` is randomized, it has sufficient entropy to function (temporarily) as a secret key. A few bits of the secret key could be used as a pointer (e.g., URL) to a place to post the opening of the commitment.

- 9
http://deepbit.net; http://blockexplorer.com/q/interval
- 10 http://goo.gl/fBNnA

## CommitCoin proof of concept
We committed to the title and abstract of this paper and, as proof of concept, inserted it into the Bitcoin block chain on September 15, 2011 (the submission deadline for FC 2012). We used a simplified version of CommitCoin, with `c` set to be the public key fingerprint. As noted, this effectively burns the money. A proper implementation using `c` as the private key is forthcoming.

First we ran,

`openssl rand -out random.dat 20`

creating a file containing a 20 byte random factor. [12] Then we concatenated the randomness to the end of the abstract PDF [13] and hashed it using RIPEMD-160,

`cat abstract.pdf random.dat > preimage.dat`
`openssl dgst -ripemd160 preimage.dat`

giving us the result:

`135e3712334428d4061efe4e5ffd5ff817aeb817`

This serves as a basic commitment scheme. We called an online tool [14] to convert this hash into a valid Bitcoin address giving us:

`12mQhpvGYdBrvDJq6sFGwEe3GETaqEM4Jk`

Finally, we used the Bitcoin Faucet[15] to send BTC0.005 to this address. This transaction ostensibly appeared in the Bitcoin blockchain on 2011-09-16 00:24:32 which can be seen in blockexplorer. [16]

However it may be the case that we actually committed to our abstract long after 2011-09-16 00:24:32 and colluded with blockexplorer or the Bitcoin network to display the wrong timestamp. How can you really be sure?

By the time you are reading this, many more blocks will have been added to the blockchain. Each block that is added is a solution to a moderately hard problem.

Suppose we actually committed to the abstract yesterday. That means we would have had to forge the entire chain from Block 145535 [17] to the current block. [18]

Given each block takes on average 10 minutes for the entire Bitcoin network to solve, we could not have solved that many blocks in a single day even if we controlled the whole network.

- 13 [http://people.scs.carleton.ca/~clark/commitcoin/abstract.pdf](http://people.scs.carleton.ca/~clark/commitcoin/abstract.pdf)
- 14 [http://blockexplorer.com/q/hashtoaddress/135e3712334428d4061efe4e5ffd5ff817aeb817](http://blockexplorer.com/q/hashtoaddress/135e3712334428d4061efe4e5ffd5ff817aeb817)
- 15 [https://freebitcoins.appspot.com/](https://freebitcoins.appspot.com/)
- 16 [http://blockexplorer.com/tx/2993c284f0b6838386ddd286af415384560d93cc4e27d25087fd6534f8e0d276](http://blockexplorer.com/tx/2993c284f0b6838386ddd286af415384560d93cc4e27d25087fd6534f8e0d276)
- 17 [http://blockexplorer.com/b/145535](http://blockexplorer.com/b/145535)
- 18 [http://blockexplorer.com/q/getblockcount](http://blockexplorer.com/q/getblockcount)

### References
1. [CommitCoin: Carbon Dating Commitments with Bitcoin](http://eprint.iacr.org/2011/677.pdf)

---

https://github.com/OpenAssets/open-assets-protocol

https://github.com/OpenAssets/open-assets-protocol/issues/6
https://github.com/OpenAssets/open-assets-protocol/issues/15


The standard client will not relay non-standard transactions. However, if you get them directly to a miner that accepts them, clients will process them correctly and the transaction will work.

You can send your transactions to 173.242.112.53. This is a server run by Eligius that will relay all valid transactions and they will include even non-standard transactions in the blocks they mine. Others who are willing to relay or include free and non-standard transactions also tend to link to this node, so it can get your transaction included in blocks mined by other pools as well.

This is for sending transactions directly to Eligius: http://eligius.st/~wizkid057/newstats/pushtxn.php

A completely separate 1995-established PGP+email binary data timestamping service: http://stamper.itconsult.co.uk/stamper-files/index.htm

https://bitcointalk.org/index.php?topic=28811.msg363505#msg363505

>  I think you focus on the downside and miss the upside. Every single one of these things is more robust and secure together than they would be alone. The more processing power going to extend a hash chain, the harder it is to attack that hash chain by accumulating 51% of the power. If all of these things are in the same chain, someone would need the computing power to attack all of them just to attack one of them. If that power is divided over a dozen projects, it becomes much easier.

That kind of gives me an idea for a project -- a generic hash chain system using proof of work just like bitcoin, but that include any data just by keeping its hash. So it can include all of those things. By analogy, you can mine bitcoins without ever seeing a transaction, they just keep a hash -- today's miners typically do just that. If the hash chain included many projects you could keep just a hash of each one. For projects you are interested in, you could keep the transactions data.

This can be incorporated without damage into the existing bitcoin system. Nodes in the timestamp chain, for example, can be included as nothing but transactions in the bitcoin chain (including only their hash). The real underlying transactions themselves need never be seen by the bitcoin system.


> I wonder if it would be feasible to include the hash to timestamp in the input and not in the output.

What like “coin_base”? Where they shove the “it’s a coloured coin” tag? And like - “doacc:D3db0e182-a26f-4083-93ff-de3b5d874d06”, maybe?

---

# Initial description

## Blockchain-Powered Applications

Within circles familiar with Bitcoin, blockchain is known as the foundational infrastructure that supports transactions in the cryptocurrency. However, the capabilities of the blockchain are completely independent of Bitcoin. From a functional standpoint, the blockchain provides the foundation to enable decentralized, secure, and trusted data exchange. By focusing on solving a highly complex problem such as decentralized financial transactions, developers of blockchain technologies have created capabilities that are foundational to many mission-critical applications. From vertical[-specific scenarios like electronic voting or trade settlements to next-generation peer-to-peer messaging applications, the blockchain is definitely an interesting trend in the future of enterprise applications.

# Expansion

## The blockchain in the Enterprise

Bitcoin has become one of the most intriguing and revolutionary technologies created in the last few years. From a functional standpoint, the crypto-currency has challenged the most fundamental principles of the world’s financial systems by providing a decentralized, secured and trusted model to process financial transactions. To enable its magic, Bitcoin relies on an architecture powered by a groundbreaking technology known as the Blockchain.

The blockchain is Bitcoin’s public ledger. From a functional standpoint, the blockchain provides a decentralized, time stamped, ordered record of all transactions in a Bitcoin network that can be verified at any time. These simple capabilities represent the first practical answer to profound computer science problems based on the trust of nodes in a decentralized network.


## Adopting the Blockchain in the Enterprise

Despite its unique value, the process of adopting blockchain solutions in the enterprise is far from easy. Like any other technology trend, the blockchain will have to develop a series of enterprise-ready capabilities to be adopted in business scenarios. The following list includes some of the key capabilities required to adopt the blockchain in mainstream enterprise scenarios.

### Development Platform:

The blockchain is a very complex architecture modeled in terms of transactional exchanges. In order mitigate that complexity, we need programming frameworks and languages that allow average developers to build general-purpose applications against the blockchain.

### Monitoring Tools:

To be adopted in enterprise settings, the blockchain community should produce solutions that can actively monitor the health of a blockchain network and recover from unexpected failures.


### Private Cloud Deployments:

Facilitating the deployment of the blockchain in private cloud topologies using mainstream enterprise infrastructures is a key element to facilitate the wide adoption of blockchain solutions in the enterprise.

### Standards:

As organizations start adopting blockchain solutions, the need to standards to guarantee the interoperability between different platforms will become more relevant.


### Interoperability with Well-Established Enterprise Platforms:

Like any other enterprise software trend, blockchain solutions will be required to integrate with established enterprise platforms like databases, line of business systems, etc. Enabling that interoperability will be essential to power the adoption of blockchain solutions in the enterprise.


## 5 Industry Scenarios That Can be Disrupted By The Blockchain

The decentralized, autonomous, trusted and secured capabilities of the blockchain that can redefine of the foundational patterns of enterprise applications. While the principles of the blockchain are well understood patterns in enterprise solutions, until now we have lacked practical implementations that validate its functionality at an enterprise scale. The blockchain opens a new set of opportunities to enterprise scenarios that weren’t possible before. The following list includes some industry scenarios that can drastically improve by the adoption of blockchain technologies.

### Decentralized IOT

The internet of things (IOT) is becoming one of the most important trends in modern enterprise software. While many IOT platforms are based on a centralized model in which a broker or hub control the interaction between devices, this model has proven to be impractical for many scenarios in which devices need to exchange data between themselves autonomously.

The blockchain provides foundational capabilities of decentralized IOT platforms such as secured and trusted data exchange as well as record keeping. In this type of IOT architectures, the blockchain will serve as the general ledger keeping a trusted record of all the messages exchanged between smart devices in an IOT topology.


### Keyless Signature

Public Key Infrastructure (PKI) has been one of the fundamental technologies powering data signatures. PKI models rely on a central authority to stamp and validate signatures on a data payload.

The characteristics of the blockchain can help to overcome some of the limitations of PKI models with a keyless security infrastructure (KSI). A KSI model uses only hash-function cryptography, allowing verification to rely only on the security of hash-functions and the availability of a public ledger commonly referred to as a blockchain.


### Legal Proof of Existence or Proof of Possession

Validating the existence or the possession of signed documents is an incredibly relevant element of legal solutions. The challenge of traditional document validation models is that they relied on central authorities for storing and validating the documents which presents some obvious security challenges but also becomes more difficult as the documents become older.

The blockchain provides an alternative model to proof of existence and possession of legal documents. By leveraging the blockchain, a user can simply store the signature and timestamp associated with a document in the blockchain and validate it at any point using the native blockchain mechanisms.


### Security Trade Settlement

Central Security Depositories (CSDs), has been an essential element of modern equity and bond trading. The centralized nature of CSDs is essential to a successful bond and equity trades. However, the settlement process via CSDs is incredibly expensive and slow, averaging two or three days per trade settlement.  

The blockchain offers an interesting alternative to traditional CSDs as a decentralized ledger that can keep records of transactions without relying on a central authority. The query capabilities of the blockchain will allow the settlement of trades in minutes or even seconds and at a fraction of the cost of the current CSD solutions.

### Anti-Counterfeiting

Counterfeiting remains as one of the biggest challenges in modern commerce. Segments like luxury goods, pharmaceutical or electronics are constantly affected by counterfeiting. Unfortunately, most solutions in the market require a trust in the third party authority which introduces a logical friction between merchants and consumers.

The decentralized and security capabilities of the blockchain can enable an interesting alternative to traditional anti-counterfeiting platforms. In that sense, we can envision a model in which brands, merchants and marketplaces are part of a blockchain network with nodes storing information to validate the authenticity of specific products. In this model, brands don’t have to trust on a central authority with their product authenticity information and can rely on the security and decentralized trust models of the blockchain.

# Where next?

Broad direction and approach laid out here:

We are SheffieldCrypto, we specialise in developing cutting edge predictive models. These ‘smart models’ utilize machine learning and deep neural networks, they are constantly learning and evolving given new market conditions. Currently we are applying them to various digital currency markets, the results have been very promising. We require a financial expert, specifically an expert in trading systems, to design and implement a system to utilise the signals produced by our models.

#### Job Description

- Design and implementation of a semi-automated/automated trading system utilizing the signals produced by our models.
- Custom indicator/feature design

#### Person Specification

should be experienced or knowledgeable in

- Algorithmic trading
- Machine learning
- Natural Language processing
- Market analytics
- Hedge fund operation
- System Architecture
- Feature/custom indicator design
- Agile software development (CI, TDD, Scrum) Python

#### Additional Info

We need the position filled asap

We will be offering equity in the company for the filled position

#### Model Information and Performance

On one simulation we tested our TA (technical analysis) algorithm with around 30 coins with shared initial parameters over a 3 month period, however many of these coins had little data (small market cap/volume), the results were as followed:

    Start capital: $5,000
    TA trader: $12,706
    Buy and Hold: $-731.79
    Random $-1,145

Buy and hold and random are included as comparisons ie how a portfolio would have performed if one was to 'buy and hold' the commodity.

Another model being developed is based on NLP (natural language processing). This relies on input from social media or ‘text data’, such as bitcointalk threads, reddit, twitter etc. The semantical content is analysed and the algo finds patterns between that and price movements.

We are currently working on combining the output from both algos into a deep neural network.

#### Feature/custom indicator design

Currently the TA algo utilises the output from TA-lib (a library of 150 technical indicators). The design of custom input parameters (or features as they’re known in machine learning) will allow the models to make better predictions by feeding it more relevant market data. However the priority at the moment is the design of a trading system.

Final words We have 2 PhD’s on our team developing these models. The models collectively have had 6 years of development (3 years/ PhD) and we are now ready to implement them into a trading scenario.

If you feel you are suitable for the position please apply via the short application form at http://sheffieldcrypto.com/recruitment Yours sincerely  Dave - marketing and networking

#### Introduction 

Utilising both linear and non-linear processes, such as deep neural networks and gaussian processes, we have been able to develop various predictive models for use within digital currency markets. This relies on exploiting the inefficiencies found within market data. Furthermore we have been developing models which use text data as an input, this would be data from such mediums as: forums, IRC’s, twitter etc. From extracting the semantic content of said social media the models can find patterns between what is being said the price of a particular market.

#### Technical analysis 

The objective of our algorithms is ‘profit maximisation’

The learning algorithm we incorporate evolves continuously over time. This allows it to maintain profitability by adapting to changing market conditions.

Multi task learning is then incorporated to reflect the idiosyncrasies of individual coins. Individual models are built and trained for each ‘coin’, these parameters are then connected to develop a joint model for a collection of or large group of ‘coins’. This allows for any inter market dependences to be recognised and exploited.

On one simulation we tested with around 30 coins with shared initial parameters over a 3 month period, however many of these coins had little data, the results were as followed:

    Start capital: $5,000
    TA trader: $12,706
    Buy and Hold: $-731.79
    Random $-1,145

Buy and hold and random are included as comparisons ie how your portfolio would have performed if you were to ‘buy and hold’ the commodity.

#### Text Analysis 

There is a distinct lack of sentiment indicators within the crypto currency community.

We are currently developing various models which utilises data from forums, IRC’s, twitter, chat boxes etc. See below for a description of each model.

#### Descriptive text analysis

Displays trending words within the crypto community

#### Neural Network

Show words that have had a high impact during a period where the TA module made a prediction, both positive and negative.

#### Activity forecast

Based on historical forum posts this module predicts the future density of threads ie attempts to predict how the popularity of a coin will vary

If you have any questions regarding our models, would like to join our team or think our services would be of value to your operation, please contact us via the contact page.

---

<div class="ui vertical stripe segment">
  <div class="ui middle aligned stackable grid container">
    <div class="row">
      <div class="ten wide column">
        <h3 class="ui header">Brokers vent anger at FCA over opaque UK lending criteria</h3>
        <p>A Financial Conduct Authority mortgage boss has expressed concern after listening to brokers' struggles to meet unpublished and non-transparent lender criteria. <a href="http://www.mortgagesolutions.co.uk/news/brokers-vent-anger-to-fca-on-opaque-lending-criteria/">(link)</a>.</p>
        <p>Mortgage policy manager Lynda Blackwell heard brokers’ tales of frustration with often-unpublished lender affordability criteria at The Mortgage and Protection Event 2013. <strong><em>Having apparently strong cases rejected with no explanation is a particular problem.</em></strong></p>
        <p>Blackwell stressed the regulator only expected brokers to try to meet lenders’ published ‘headline’ criteria. She said <span style="color:red"><strong><em>the lack of explanation around rejected cases is a concern in terms of broker record-keeping: “We would expect the reason the application didn’t proceed to be on file.”</em></strong></span></p>
        <p>Brokers vented their anger at the conference after Blackwell addressed <span style="color:red"><strong><em>the issue of the difference between published headline rates and lenders’ “black box” of internal affordability criteria</em></strong></span> raised by Legal &amp; General housing boss <a href="http://www.mortgagesolutions.co.uk/mortgage-solutions/blog-post/2305067/the-mortgage-market-s-big-unanswered-question-l-g">Stephen Smith in a blog for Mortgage Solutions</a>. Other concerns included the cost to clients if apparently strong applications fail and the impact on broker reputations.</p>
        <p>Having forecast the Mortgage Market Review will increase opportunities for brokers earlier in her talk, she commented: “It seems the MMR is putting a spotlight on the way the relationship [between lenders and brokers] is not working very well at all.”</p>
        <p>The FCA is listening to broker representatives such as the Association of Mortgage Intermediaries and <span style="color:red"><strong><em>proposals such as date stamping cases in order to monitor criteria changes over time</em></strong></span> and more consistent published lender criteria. Blackwell said she is willing to hear from other broker groups as well.</p>
        <p><em>Domain-specific opportunity</em> ^^^^</p>
        <h3 class="ui header">Referenced blog post</h3>
        <blockquote style="font-size:90%; color: #666">
          <p>Most of the issues that intermediaries are thinking about on MMR come directly from the regulator’s rules. But there is one which sits squarely with the mortgage lenders. And we need an answer on it pretty fast.</p>
          <p>Under MMR, mortgage intermediaries are responsible for ensuring mortgage applications are submitted which meet the ‘lender’s expected affordability criteria’. This term is not defined – so what are we to think? Does it mean simply the criteria by which sourcing systems operate – LTV limits for example?</p>
          <p>Probably not – that is too basic. So does it more likely mean <span style="color:#ff9e04"><strong><em>the criteria of a lender which sit behind the headline product – what income, debt and expenditure requirements there are, whether the product is available to first time buyers, etc?</em></strong></span> If it is this latter, more likely requirement, <span style="color:red"><strong><em>exactly where does an intermediary get this information and how can they prove these were the criteria in place at this exact time on this exact date?</em></strong></span></p>
          <p>At present, an intermediary wishing to have a complete file to be able to demonstrate to the FCA they have chosen the best deal for his client, can take <span style="color:red"><strong><em>a screen shot of the sourcing results. This will show, date and time stamped, where the top products were selected from. A clear, date stamped record, which can be held on file.</em></strong></span></p>
          <p>No such ability exists for ‘lender’s expected affordability criteria’. <span style="color:#FF9E04"><strong><em>Lenders are inconsistent. They publish their criteria in different formats and on different systems – some on the sourcing system notes pages, some on their own websites. There is no industry standard format. Some are short and succinct and some are very long and detailed. Some, very few in our experience, are dated. And the situation is worse where the notes say ‘refer to lender’ – for more complicated affordability issues.</em></strong></span></p>
          <p>So here we are, five months away from MMR day and we do not have the answer to this question.</p>
          <p>There are some further issues stem from this – for example, how will an intermediary record a case where, after discussion, the lender has accepted it, but outside their ‘expected criteria’? What will the lender give the intermediary to show they were happy with this case?</p>
          <p>So, <span style="color:#0BAD14"><strong><em>a plea to the lender fraternity: can you please start talking to each other about this and come up with a simple, industry view and ideally, a standard format for publishing your criteria?</em></strong></span> It’s not much to ask.</p>
          <p>Stephen Smith is director of housing and external affairs at Legal &amp; General</p>
        </blockquote>
      </div>
      <div class="four wide right floated column">
        <img src="/assets/images/wireframe/square-image.png" class="ui large bordered rounded image">
      </div>
    </div>
  </div>
</div>
