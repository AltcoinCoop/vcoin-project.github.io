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
          <h3>The mortgage market’s big unanswered question…</h3>
          <img src="/assets/images/avatar/stephen.jpg" style="float:left; padding: 0.6rem; margin:0;" alt="Stephen Smith of Legal &amp; General"/>
          <p>Most of the issues that intermediaries are thinking about on MMR come directly from the regulator’s rules. But there is one which sits squarely with the mortgage lenders. And we need an answer on it pretty fast.</p>
          <p>Under MMR, mortgage intermediaries are responsible for ensuring mortgage applications are submitted which meet the ‘lender’s expected affordability criteria’. This term is not defined – so what are we to think? Does it mean simply the criteria by which sourcing systems operate – LTV limits for example?</p>
          <p>Probably not – that is too basic. So does it more likely mean <span style="color:#ff9e04"><strong><em>the criteria of a lender which sit behind the headline product – what income, debt and expenditure requirements there are, whether the product is available to first time buyers, etc?</em></strong></span> If it is this latter, more likely requirement, <span style="color:red"><strong><em>exactly where does an intermediary get this information and how can they prove these were the criteria in place at this exact time on this exact date?</em></strong></span></p>
          <p>At present, an intermediary wishing to have a complete file to be able to demonstrate to the FCA they have chosen the best deal for his client, can take <span style="color:red"><strong><em>a screen shot of the sourcing results. This will show, date and time stamped, where the top products were selected from. A clear, date stamped record, which can be held on file.</em></strong></span></p>
          <p>No such ability exists for ‘lender’s expected affordability criteria’. <span style="color:#FF9E04"><strong><em>Lenders are inconsistent. They publish their criteria in different formats and on different systems – some on the sourcing system notes pages, some on their own websites. There is no industry standard format. Some are short and succinct and some are very long and detailed. Some, very few in our experience, are dated. And the situation is worse where the notes say ‘refer to lender’ – for more complicated affordability issues.</em></strong></span></p>
          <p>So here we are, five months away from MMR day and we do not have the answer to this question.</p>
          <p>There are some further issues stem from this – for example, how will an intermediary record a case where, after discussion, the lender has accepted it, but outside their ‘expected criteria’? What will the lender give the intermediary to show they were happy with this case?</p>
          <p>So, <span style="color:#0BAD14"><strong><em>a plea to the lender fraternity: can you please start talking to each other about this and come up with a simple, industry view and ideally, a standard format for publishing your criteria?</em></strong></span> It’s not much to ask.</p>
          <p>From <a href="http://www.mortgagesolutions.co.uk/news/the-mortgage-market-s-big-unanswered-question-l-g/">The mortgage market’s big unanswered question…</a>, a post by Stephen Smith, director of housing and external affairs at Legal &amp; General.</p>
        </blockquote>
      </div>
      <div class="four wide right floated column">
        <img src="/assets/images/wireframe/square-image.png" class="ui large bordered rounded image">
      </div>
    </div>
  </div>
</div>

---

We are less than a month into Mortgage Market Review regime and it is therefore logical that there are initial teething troubles.

The one that is really starting to stand out however is the issue of stress testing. It is not stress testing per se that is the issue, it is the fact that so many lenders are withholding the stress test criteria that they are using so that broker do not have a fair representation of what measures the lenders are using.

As a result, when working out affordability for their clients the broker can only base their affordability checks on the published rate, but we know that lenders are using stress tests that vary from +1% to +8% of the published rate.

The consequence for the borrower is that despite meeting all affordability criteria asked for, applications are coming back as declined or for much lower amounts than the borrower has requested.

It hardly meets with the treating customers fairly guidelines to hide criteria on which a loan decision is made, especially if it leads to different lenders carrying out a number of credit checks that could then damage a borrower’s credit rating.

There is also a danger to brokers in the quality metrics stakes; this cloak and dagger approach to stress testing will inevitably lead to more DIPs being declined as brokers do not have full information before placing a client’s application with a lender.

As many lenders base their quality judgements – of both brokers and networks – on the level of DIPs that do not go through to completion, it could reflect negatively on their ratings and ultimately affect the level of proc fees that someone receives.

How can a broker make a qualified decision on where to place their client’s mortgage application if part of the information being used to judge whether the client qualifies is hidden from them? In order to treat both customers and brokers fairly, all stress testing information and criteria should be in the public domain and published on every lender’s website. Without it a broker is advising in the dark without all of the information to do their job.

Toni Smith is sales operations director at First Complete



---

The day has come and passed, the Mortgage Market Review rules are formally enforceable and the only thing left to do now is knuckle under and get used to them.

Networks and lenders have been carrying out extensive training to get the industry ready for a new era of forensic customer assessments.

They are designed to force borrowers to consider the reality of their spending habits rather than a superficial box ticking exercise of what they would like them to be.

Personal Touch Financial Services invited Mortgage Solutions to one of its broker MMR-training session where Neil Hoare, head of commercial relationships, dissected bank statements as an underwriter would.

While the responsibility for assessing the applicant’s affordability rests with the lender it is better to avoid a frustrating game of ping pong with your underwriter.

In the first of two-part feature PTFS reveals how an underwriter tackles bank statement assessments.

PTFS’ tips on bank statement assessments:

## Regular annual spending

Be prepared to push customers on their spending over birthdays, holidays and Christmas.

These are permanent expenses which must be be broken down into a monthly spend and included on the application form as if they were saving for the events on a monthly basis.

These are areas of spending where borrowers are often forced to go overdrawn or use a credit card which they cannot afford to pay off.

Holidays fall into this category too. Question applicants on how they will pay for their annual holiday.

Bank statements may reveal travel insurance payments or spending abroad which will throw into question an applicant’s insistence they don’t go on holiday.

## Erratic and frequent cash withdrawals

A succession of cash withdrawals staggered throughout the same evening, for example on a Friday night, suggest a lack of discipline over spending.

And while this may not be a reason on its own to knock back the mortgage it could be helping to build a picture of erratic or irresponsible spending behaviour.

If the withdrawals cause the applicant’s other bills to bounce it will not bode well for the applicant’s chance of getting approved.

## Vices

There will probably be space on the application form for tobacco or alcohol spending.

Check what the applicant is telling you against pub debit card payments. Particularly high pub spending one month may be due to a one-off event.

If this is apparent by comparing spending on the other two months then it would be plausible to use an average and explain why. 

Gambling is a different story. Payments to gambling outlets will not be viewed positively, particularly if they are frequent.

Do not fall into the trap of thinking any wins will be taken into consideration.

Despite your applicant’s insistence they have ‘foolproof system’ your underwriter will not share the same view. Frequent gambling suggests a lack of self-control.

## Unusual or non-descript regular transactions

Magazine or newspaper subscriptions, lottery payments, hobby memberships, union subs, pet insurance, gym membership and insurance for appliances may not fit neatly into the boxes on an application form.

If it is not completely clear where these payments have been added include a note at the back of the application to clarify where they have been included.

It is important to consider if any of these direct debits have related regular costs associated with them for example pet food if there is pet insurance.

Some direct debits may not be indicative of the product or service they are paying for.

Some gym memberships look like payments for council tax if the gym is run by the local authority. Help the underwriter out by adding a line of clarification.

Paypal payments can be a red herring as they show up as direct debit transaction.

Payments out to another account may indicate the applicant has another account which they have not disclosed to you.

## Informal sources of income

Is the applicant receiving regular deposits from a source which is not their employment? The source could be a parent.

Check to see if the bank account is being propped up by these deposits which would indicate the applicant is unable to maintain their lifestyle based on their own salary.

The regular transfers may indicate the applicant may have another account they have not disclosed to you.

## Plausibility of outgoings and the inclusion of plausibility statements

Some lenders are using average spending habits based figures from the Office of National Statistics as plausibility indicators regardless of what figures are entered into the affordability calculator.

Carry out a sense check when your applicant discloses their outgoings. Is a family of five spending £30 a month on electricity realistic?

Where the monthly spend on a particular item is lower than average include a plausibility explanation with the reason why.

Familiarise yourself with the ONS figures – do not use them instead of your applicant’s outgoings but use them as your own plausibility indicator if preferred.

For the ONS average household outgoings click [HERE](http://www.ons.gov.uk/ons/rel/family-spending/family-spending/2013-edition/family-spending---list-of-tables-appendix-a--2013-edition.html#tab-List-of-Tables--Appendix-A).

---

Santander for Intermediaries has tightened its Help to Buy and general affordability criteria while paring back its interest-only policy three months after the launch of the Mortgage Market Review.

Borrowers using the Help to Buy mortgage indemnity guarantee scheme must be using less than four-and-half times their income to support the application.

For all applications, Santander’s online affordability calculator will now display a single maximum loan amount rather than different amounts for low, medium and high credit scores.

To coincide with this change the lender will be updating its Office of National Statistics data which it uses to verify a clients’ stated expenditure.

Applicants taking out an interest-only mortgage will need to have £150,000 equity in their property where the sale of the property is their exit strategy.

In a broker alert the lender said: “As a responsible lender we want to ensure that customers have sufficient equity in their property to enable them to sell and downsize at the end of the mortgage term.”

The maximum age of interest-only or part-and-part borrowers has now been restricted to 65 on maturity of the mortgage.

The maximum mortgage term for the Help to Buy equity loan scheme has been increased from 25 to 35 years.

The maximum loan-to-value for new build flats has been increased from 75% to 80%.

The changes take effect from Friday 25 July this week

---

Nationwide has increased its stressed rate for all affordability calculations to 6.99% and imposed an income multiple cap of 4.75 times gross income for all employed applications from today.

The building society said it had made the changes following the Financial Policy Committee’s (FPC) guidance.

In June the FPC announced all lenders should apply a stressed rate which assumed a growth in base rate of 3% and placed a restriction on lending above 4.5 times gross income.

It said lenders could hold up to 15% of their new mortgage book on high loan-to-income (LTI) ratios, loans above 4.5 times a borrower’s income.

The rule does not come into force until October 1 but any mortgages written after June 26 will count towards this quota.

But despite the high LTI allowance Nationwide has decided to impose a blanket 4.75 times cap across all employed applications.

The move has caused brokers to question the purpose of the rigourous affordability checks improsed by the Mortgage Market Review (MMR).

Ashley Brown, director of brokerage Moneysprite, said: “The MMR was introduced so lenders could make sensible lending decisions based on individual circumstances with a built in stress test.

“The BoE has decided that because the London property market is running ‘hot’ borrowers in all parts of the country should be restrained with an arbitrary multiple. This must be a regressive step and questions why we all bothered with much of the MMR.”

Brown suggested Nationwide may use its high LTI quota to boost branch network business which he said would disadvantage customers looking for advice from brokers.

Dean Mason, owner of Masons Financial Planning, blamed the regulators for targeting the wrong mechanism to cool down a housing bubble.

He said: “I can’t understand why the powers that be are trying to kerb the perceived ‘housing bubble’ by making it harder for borrowers when the real problem lies with agents over inflating prices, misleading vendors on expectations and intimidating buyers into committing.”

Mason praised Nationwide for being a ‘haven’ for sensible lending decisions where others have missed the point of the MMR.

“A maximum 4.75 times income is still generous compared to most if it is actually prepared to lend to this level where client circumstances allow,” he said.

Brown said he feared the self-employed would be the most affected by the the income cap measures.

“Already they are heavily penalised by affordability calculators and I suspect the new rules will continue and exacerbate this situation.”

But Colin Chapman, director of intermediary firm Genesis, said the restrictions were a positive measure which would not prove to be prohibitive in many cases.

“Whilst the obvious broker view point maybe to be vent frustration at what seems to be another lender retreating to ultra conservative stress testing, the overall impact will not be too troublesome. This is especially true in my local area which isn’t that affluent with very high property prices.

“I think long term the cautious approach is better than the unchecked boom times of the mid 2000s. No one wants a return to the broker dark days of 2008 to 2012.”

Cases where the initial decision in principle was keyed before 5.00pm Monday 21 July will be assessed under current affordability rules.

From Thursday 21 August 2014 any case that requires a reprocess will be assessed under the new affordability calculation.

---

Following a Mortgage Solutions report on the unintended underwriting fallout of the Mortgage Market Review, appalled brokers flagged yet more outlandish underwriting roadblocks thrown in front of mortgage applicants.

After a Mortgage Solutions question at the FCA’s annual public meeting, CEO Martin Wheatley dismissed lender product and underwriting clamp downs as ‘teething problems’ adding unintended consequences of the new lending rules are being ironed out.

Mortgage advisers rushed to disagree, outlining a rash of illogical lender mortgage decisions.

One broker said after a valuation delay the lender requested an updated pay slip. In the interim the client had a pay rise which the lender ignored, but due to the increased pension payments, the lender cut the mortgage offer by five pounds.

Elsewhere, a lender spotted a regular payment in an applicant’s account for £10 a month to pay a neighbouring child for walking the dog. After the lender’s insistence, the sum was included as a household bill and the mortgage offer was reduced.

Another adviser said: “I had a case of a client on £130,000 per annum and the lender [wanted] a disposable income of over £2,000 per month, which is more than the average wage earner in the UK earns net of tax and before their bills. He was doing a pound for pound remortgage with no debt problems, so [had already] evidenced the fact he lives off a lower disposable income.”

Arron from Temple Capital said: “Most lenders need to revisit their criteria and perhaps gather some brokers together to ensure their criteria is more realistic. The FCA is right to be concerned that unintended consequences have stemmed from isolated compliance departments not being able to see reality.”

---

The Association of Mortgage Intermediaries (AMI) has been in talks with the Council of Mortgage Lenders (CML) to feedback broker concerns over how the Mortgage Market Review (MMR) has been implemented.

Robert Sinclair, chief executive of AMI, said: “We have been having discussions about how well the MMR has landed and clearly there have been words around how different lenders have interpreted the affordability requirements.”

Last month Martin Wheatley, chief executive of the Financial Conduct Authority, said in response to a Mortgage Solutions question that it was in talks with lenders which were being ‘too assidious’ in their assessment of a borrower’s affordability.

But Wheatley said it was too strong to say that lenders’ overzealous underwriting of borrowers’ expenditure was an unintended consequence, as brokers had suggested.

He said it was more accurate to refer to it as a ‘teething problem’.

Wheatley brushed off the severity of the issue, which triggered a flood of broker comments to Mortgage Solutions about instances where lenders had nit-picked over trivial expenses causing delays and stress to mortgage customers.

Dominik Lipnicki, director of broker firm Your Mortgage Decisions, wants to see the current fragmented approach joined together.

“Why don’t we have a universal budget planner? A broker will know that as long as they ask certain questions they could be confident that they have covered everything the lender wanted to see. That would make total sense.

“But instead what we have is a totally fragmented market with different ways of looking at things.”

Lipnicki said that while all lenders had different exposures to risk and different niches, some uniformity would help.

But Sinclair said it was these difference which allowed a broker to show their worth to the customer.

“If a customer tried to find their way round this it would be impossible which is why intermediaries exist,” he added.

Steve Smith, AMI board member and mortgage consultant for Springtide Capital, agreed that the complexities and variances of lenders’ approaches to affordability offered brokers an opportunity to attract more clients.

“The range of lender approaches give the broker more value to add to the offering since we typically know what lender to use in which circumstance.”

Smith said if a universal budget planner were introduced it may result in more questions rather than less.

“Can you imagine what it would like? My guess is that it would be a lot longer than most of those being used today,” he said.

A spokeswoman for the CML said: “Individual approaches by lenders to affordability assessments, in line with FCA rules, are not a matter for the CML.

“However, as the MMR beds down we have fed back in general terms to our members that brokers note there are differences between lenders. It is early days, and it will not be surprising if practices continue to evolve as the new regime beds in.”

AMI plans to meet with the CML later this year to discuss how the market has moved on.

---

Lenders want an injection of common sense into the Mortgage Market Review (MMR) rules on execution-only sales which they say are causing frustration among borrowers.

Under the new rules if a borrower choses to take out a mortgage without advice using the execution-only route, the lender is not allowed to have any interaction with the customer.

But lenders want the option to give borrowers information to make sure the mortgage they pick for themselves is the most suitable option available.

The frustration was brought to light after the Council of Mortgage Lenders (CML) opened discussions with lenders to find out what issues have arisen as a consequence of implementing the MMR rules.

A spokesman for the CML said: “In cases where the customer opts for an execution-only sale, lenders have to be sure that the borrower is choosing from a complete and up-to-date list of products.

“If the customer wants to do this on the phone or in a branch, lenders would like to be able to make sure the customer has all the appropriate product information without straying into the advised sales option.”

He said currently, if a new rate has been added to the lender’s website, the adviser can only ask the borrower to revisit the website but cannot say why, which is causing customers to become frustrated.

The CML intends to raise the issue with the Financial Conduct Authority when it begins its review of the MMR and the unintended consequences of its implementation, later this year.

---

The Council of Mortgage Lenders (CML) is concerned that the Mortgage Market Review (MMR) has created an unnecessary barrier for homeowners wishing to switch their mortgage to a cheaper rate.

Borrowers on a Standard Variable Rate who want to apply for new deal on similar terms are being held back by the tough new affordability requirements even if the switch can lower their monthly payments.

In its newsletter, the CML said it was preparing to address the issue with the Financial Conduct Authority (FCA) when it carries out a thematic review on the unintended consequences of the MMR later this year.

It said: “…we remain concerned about the level of bureaucracy in areas such as product switches.”

Ahead of the FCA’s review the CML has begun talks with members to find out which areas have proved most problematic to implement resulting in unintended consequences.

It emerged that lenders wanted clarity on what checks needed to be carried out if a borrower switches to a new deal and the mortgage balance increases slightly due to administration fees incurred by the switch.

Currently lenders are subjecting borrowers to a full affordability assessment which many are failing to pass.

A spokesman for the CML said that while the MMR was not put in place to create mortgage business it should not create mortgage prisoners asa result of minor loan size changes.

He said it wants the FCA to provide more guidance in this area so lenders have the confidence to simplify the process for borrowers without the fear of falling foul of the rulebook.

---

## Due Diligence Compliance Analyst, First Guaranty Mortgage Corporation - Remote

How it is under U.S. credit regulations ...

### Position Purpose 

Under general supervision and working within the Correspondent Division, analyze and validate the accuracy of financial information reported on the Loan Estimate (LE) and create the Closing Disclosure (CD) to ensure compliance with the Consumer Financial Protection Bureau’s (CFPB) rules and regulations. In addition, audit loan files to ensure that other federal and state requirements have been met. Report identified issues to management. 

### Key Job Functions 
- Audit mortgage loan files for compliance with the CFPB rules for the Loan Estimate, Closing Disclosure, and other required disclosures.
- Verify the accuracy of the Loan Estimate to ensure the following: APR, Tolerance Cures, Detailed Category Labels, etc.
- Ensure integrity of the Loan Estimate and Closing Disclosure and resolve issues timely in order to minimize impacts to the business processing timelines, clients, and affected consumers.
- Monitor other required disclosures to ensure that information has been provided timely and properly in accordance with federal and state guidelines, including Mortgage Broker disclosures and timely delivery of the appraisals.
- Follow up with business teams on recurring discrepancies, propose solutions, and support implementation as necessary.
- Analyze process controls to ensure accurate, complete, and timely transaction processing; and bring inconsistencies and problems to the attention of management.
- Recommend technological enhancements and process improvements.
- Perform special projects of low to moderate complexity, or participate as a team member on more complex projects.

### Minimum Experience 
- 3-5 years of related experience in the Mortgage Industry or equivalent work experience.
- Prior experience in the mortgage industry as a processor, underwriter, quality control auditor, or closer is ideal.

### Specialized Knowledge & Skills 
- Knowledge of mortgage industry guidelines associated with federal and state regulations including the TILA-RESPA Integrated Disclosure Rule.
- Strong analytical and problem solving skills.
- Excellent time management and follow up skills required.
- Ability to work effectively with business teams, clients, and vendors to build strong relationships.
- Working knowledge of Microsoft Office, and strong Excel spreadsheet skills required.
- Experience with Ellie Mae Encompass is a plus.

---

# Cloning Litecoin

1. Pre Installers.
    - 1a. Winrar
    - 1b. Compression
    - 1c. MinGW
2. Windows Deps.
    - 2a. OpenSSL
    - 2b.Berkeley DB
    - 2c. Boost
    - 2d. MiniUPNP
    - 2e. Protoc and Libprotobuf
    - 2f. Libpng
    - 2g. qrencode
3. Download and Compile QT.
4. The Clone
    - 4a. Source Code
    - 4b. Copy and Replace Litecoin
    - 4c. Copy and Replace LTC
    - 4d. Change rpc and port numbers. 
    - 4e. Change starting letter for addresses.
    - 4f. Update client version number.
    - 4g. Change Litecoin example addresses to Clonecoin Addresses. 
    - 4h. Change char pchMessageStart and ParseHex. 
    - 4i. Change alert keys. 
    - 4j. Remove Merkel root and Genesis Block.
    - 4k. Remove Nonce and testnet genesis. 
    - 4l. Add Epoochtime and Timestamp.
    - 4m. Fixing the checkpoints.
    - 4n. Change max money supply and coinbase maturity.
    - 4o. Change block times from 2.5 minutes to 30 seconds.
    - 4p. Change re-targeting
    - 4q. Add premine and change block rewards. 
    - 4r. Update Images.
    - 4s. Update Seed node/ AWS Seed node guide.
5. Hashing the Genesis Block and Merkel Root.
    - 5a. Ability to hash Genesis Block.
    - 5b. Compiling Clonecoin Windows QT.
    - 5c. Generating Merkel Root
    - 5d. Hashing the Genesis Block.
6. Connecting your nodes.
    - 6a. Create a conf.
    - 6b. Connect- server and home network.
7. Checkpointing the premine.
8. Clean up Your Code.
9. Compiling Clonecoind.
    - 9a. Compile Clonecoind.
    - 9b. Remove and cleanup.
10. Github for release, made easy.
    - 10a. Easy Pushing Commits/Launch code.
    - 10b. Easy Revert Commits
    - 10c. Easy Pushing Updates.
11. Common Errors
12. Quick Logos
13. The Website.
    - 13a. The Template.
    - 13b. Upload to a website.
14. The Launch. Ninja vs Pumped vs ICO.
    - 14a. Prelaunch
    - 14b. The Ninja
    - 14c. The Pumped.
    - 14d. The ICO.


## 1. Pre Installers.

### 1a. File Compressor/Extractor

Download and install Winrar or an alternate file compression tool. 
[http://www.rarlab.com/download.htm](http://www.rarlab.com/download.htm)

### 1b. Text Editor.

Download and install a text editor such as [Sublime Text](http://www.sublimetext.com/). You need a text editor that can easily search and replace case sensitive text.

### 1c. Download and install MingW

[http://sourceforge.net/projects/mingw/files/Installer/mingw-get-setup.exe/download](http://sourceforge.net/projects/mingw/files/Installer/mingw-get-setup.exe/download)

Double click to install, keep the checkbox for the GUI checked and make sure to install in ``C:\MinGW``. Press continue. From the MinGW GUI interface, go to ``all packages -> MYSYS``
Right click on the following installations and mark for installation.

- ``msys-base-bin`` (may highlight other checkboxes which is fine)
- ``msys-autoconf-bin``
- ``msys-automake-bin``
- ``msys-libtool-bin``

Click on ``Installation -> Apply changes``. MinGW will now download the remaining packages. Make sure to remove any previous installs of MinGW before starting. 

Once complete, navigate to ``C:\MinGW\bin`` and you should only have a ``mingw-get`` application. If you have ``msys-gcc`` and ``msys-w32api`` you need to delete MinGW and check the correct install packages are selected above.

Download and extract mingw32 to ``C:\mingw32``, [http://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win32/Personal%20Builds/mingw-builds/4.9.1/theads-posix/dwarf/i686-4.9.1-release-posix-dwarf-rt_v3-rev1.7z/download](http://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win32/Personal%20Builds/mingw-builds/4.9.1/theads-posix/dwarf/i686-4.9.1-release-posix-dwarf-rt_v3-rev1.7z/download)

You now need to change the path variables. Go to ``control panel->system`` and ``security->system``. Click on ``advanced system properties->environmental variables``. In the top box navigate to PATH and change to 

    > C:\mingw32\bin;%SystemRoot%\system32;%SystemRoot%;%SystemRoot%\System32\Wbem;%SYSTEMROOT%\System32\WindowsPowerShell\v1.0\


Checking your MingW install.

To start the MingW app navigate to ``C:\MinGW\msys\1.0\msys.bat``, create a desktop shortcut as you will use the ``msys`` command as well as the windows command prompts. Double click to start and enter the following to display the version and correct paths.

    $ gcc -v

Your ``msys`` output should look like the following code.

    $ gcc -v
    Using built-in specs.
    COLLECT_GCC=c:\mingw32\bin\gcc.exe
    COLLECT_LTO_WRAPPER=c:/mingw32/bin/../libexec/gcc/i686-w64-mingw32/4.9.1/lto-wrapper.exe
    Target: i686-w64-mingw32
    Configured with: ../../../src/gcc-4.9.1/configure --host=i686-w64-mingw32 --build=i686-w64-mingw32 --target=i686-w64-mingw32 --prefix=/
    mingw32 --with-sysroot=/c/mingw491/i686-491-posix-dwarf-rt_v3-rev1/mingw32 --with-gxx-include-dir=/mingw32/i686-w64-mingw32/include/c++
     --enable-shared --enable-static --disable-multilib --enable-languages=ada,c,c++,fortran,objc,obj-c++,lto --enable-libstdcxx-time=yes -
    -enable-threads=posix --enable-libgomp --enable-libatomic --enable-lto --enable-graphite --enable-checking=release --enable-fully-dynam
    ic-string --enable-version-specific-runtime-libs --disable-sjlj-exceptions --with-dwarf2 --disable-isl-version-check --disable-cloog-ve
    rsion-check --disable-libstdcxx-pch --disable-libstdcxx-debug --enable-bootstrap --disable-rpath --disable-win32-registry --disable-nls
     --disable-werror --disable-symvers --with-gnu-as --with-gnu-ld --with-arch=i686 --with-tune=generic --with-libiconv --with-system-zlib
     --with-gmp=/c/mingw491/prerequisites/i686-w64-mingw32-static --with-mpfr=/c/mingw491/prerequisites/i686-w64-mingw32-static --with-mpc=
    /c/mingw491/prerequisites/i686-w64-mingw32-static --with-isl=/c/mingw491/prerequisites/i686-w64-mingw32-static --with-cloog=/c/mingw491
    /prerequisites/i686-w64-mingw32-static --enable-cloog-backend=isl --with-pkgversion='i686-posix-dwarf-rev1, Built by MinGW-W64 project'
     --with-bugurl=http://sourceforge.net/projects/mingw-w64 CFLAGS='-O2 -pipe -I/c/mingw491/i686-491-posix-dwarf-rt_v3-rev1/mingw32/opt/in
    clude -I/c/mingw491/prerequisites/i686-zlib-static/include -I/c/mingw491/prerequisites/i686-w64-mingw32-static/include' CXXFLAGS='-O2 -
    pipe -I/c/mingw491/i686-491-posix-dwarf-rt_v3-rev1/mingw32/opt/include -I/c/mingw491/prerequisites/i686-zlib-static/include -I/c/mingw4
    91/prerequisites/i686-w64-mingw32-static/include' CPPFLAGS= LDFLAGS='-pipe -L/c/mingw491/i686-491-posix-dwarf-rt_v3-rev1/mingw32/opt/li
    b -L/c/mingw491/prerequisites/i686-zlib-static/lib -L/c/mingw491/prerequisites/i686-w64-mingw32-static/lib -Wl,--large-address-aware'
    Thread model: posix
    gcc version 4.9.1 (i686-posix-dwarf-rev1, Built by MinGW-W64 project)

If you are having issues I have uploaded a MinGW install [here](https://howtocloneanaltcoin.com/downloads/MinGW.rar)
 
## 2. Download and Install Dependencies.

Create a deps folder at ``C:\deps``.  If you want to cheat you can download the pre-built dependencies [here](http://www.mediafire.com/download/y89546s65sf8de5/deps.zip), though it is recommended to build your own.

### 2a. OpenSLL

Install OpenSSL dependencies on Windows.

Download the latest version of OpenSSL [https://www.openssl.org/source/openssl-1.0.1j.tar.gz](https://www.openssl.org/source/openssl-1.0.1j.tar.gz) to your deps folder.

Open the MinGW shell at ``C:\MinGW\msys\1.0\msys.bat`` 

    $ cd /c/deps/
    $ tar xvfz openssl-1.0.1j.tar.gz
    $ cd openssl-1.0.1j
    $ ./Configure no-zlib no-shared no-dso no-krb5 no-camellia no-capieng no-cast no-cms no-dtls1 no-gost no-gmp no-heartbeats no-idea no-jpake no-md2 no-mdc2 no-rc5 no-rdrand no-rfc3779 no-rsax no-sctp no-seed no-sha0 no-static_engine no-whirlpool no-rc2 no-rc4 no-ssl2 no-ssl3 mingw
    $ make


### 2b. Berkeley DB

Download [http://download.oracle.com/berkeley-db/db-4.8.30.NC.tar.gz](http://download.oracle.com/berkeley-db/db-4.8.30.NC.tar.gz) and place in your deps folder.

In the MinGW shell use the following code.

    $ cd /c/deps/
    $ tar xvfz db-4.8.30.NC.tar.gz
    $ cd db-4.8.30.NC/build_unix
    $ ../dist/configure --enable-mingw --enable-cxx --disable-shared --disable-replication
    $ make


### 2c. Boost

Download Boost to your deps folder. [http://sourceforge.net/projects/boost/files/boost/1.55.0/boost_1_55_0.zip/download](http://sourceforge.net/projects/boost/files/boost/1.55.0/boost_1_55_0.zip/download)
 
Make sure to download either the 7z or zip versions. Double click on the folder to extract ``boost_1_55_0`` in your deps folder. This may take several minutes depending on your PC's speed. 

Using the Windows command prompt, bootstrap and compile boost. To bring up the windows command prompt just type ``cmd`` in the windows search bar.


    > cd C:\deps\boost_1_55_0\
    > bootstrap.bat mingw
    > b2 --build-type=complete --with-chrono --with-filesystem --with-program_options --with-system --with-thread toolset=gcc variant=release link=static threading=multi runtime-link=static stage


### 2d. Mini UPNP

Download and extract MiniUPNP [http://miniupnp.free.fr/files/download.php?file=miniupnpc-1.9.20140911.tar.gz](http://miniupnp.free.fr/files/download.php?file=miniupnpc-1.9.20140911.tar.gz) to your deps folder. 

Rename  folder from ``miniupnpc-1.9.20140911`` to ``miniupnpc`` then from a Windows command prompt:

    $ cd C:\deps\miniupnpc
    $ mingw32-make -f Makefile.mingw init upnpc-static


### 2e. Protoc and Libprotobuf:

Download and extract [http://protobuf.googlecode.com/files/protobuf-2.5.0.zip](http://protobuf.googlecode.com/files/protobuf-2.5.0.zip) to your deps folder.

In the ``msys`` shell run

    $ cd /c/deps/protobuf-2.5.0
    $ configure --disable-shared
    $ make


### 2f. libpng

Download and extract [http://prdownloads.sourceforge.net/libpng/libpng-1.6.14.tar.gz?download](http://prdownloads.sourceforge.net/libpng/libpng-1.6.14.tar.gz?download) to your deps folder. Extract.

In ``msys`` shell run 

    $ cd /c/deps/libpng-1.6.14
    $ configure --disable-shared
    $ make
    $ cp .libs/libpng16.a .libs/libpng.a


### 2g. qrencode

Download and extract [http://fukuchi.org/works/qrencode/qrencode-3.4.4.tar.gz](http://fukuchi.org/works/qrencode/qrencode-3.4.4.tar.gz) to your deps folder.

In ``msys`` shell run 

    $ cd /c/deps/qrencode-3.4.4

    $ LIBS="../libpng-1.6.14/.libs/libpng.a ../../mingw32/i686-w64-mingw32/lib/libz.a" \
    png_CFLAGS="-I../libpng-1.6.14" \
    png_LIBS="-L../libpng-1.6.14/.libs" \
    configure --enable-static --disable-shared --without-tools

    $ make

## 3. Download and Compile QT.

Download and uncompress [http://download.qt-project.org/official_releases/qt/4.8/4.8.6/qt-everywhere-opensource-src-4.8.6.zip](http://download.qt-project.org/official_releases/qt/4.8/4.8.6/qt-everywhere-opensource-src-4.8.6.zip) to ``C:\Qt\4.8.6``.

 Once again check it resides in ``C:\Qt\4.8.6`` not ``C:\Qt\4.8.6\4.8.6``. Due to a bug in 4.8.6 you will need to apply the patch available [here](https://codereview.qt-project.org/#/c/84567/3/tools/configure/configureapp.cpp).

 For those who can't find or work it out, you need to change the following lines in ``C:\Qt\4.8.6\tools\configure\configureapp.cpp`` or download the patched file [here](https://www.mediafire.com/?y4urdzfp0k0j0gm)
 and replace it in C:\Qt\4.8.6\tools\configure\configureapp.cpp


    2180  |  -  const QString mingwPath = dictionary["QMAKESPEC"].endsWith("-g++") ?
    2180  |  +  const QString mingwPath = dictionary["QMAKESPEC"].contains("-g++") ?
    2252  |  -  if (dictionary["QMAKESPEC"].endsWith("-g++")+
    2252  |  +  if (dictionary["QMAKESPEC"].contains("-g++")+


From your Windows command prompt run 

    $ cd C:\Qt\4.8.6
    $ configure -release -opensource -confirm-license -static -no-sql-sqlite -no-qt3support -no-opengl -qt-zlib -no-gif -qt-libpng -qt-libmng -no-libtiff -qt-libjpeg -no-dsp -no-vcproj -no-openssl -no-dbus -no-phonon -no-phonon-backend -no-multimedia -no-audio-backend -no-webkit -no-script -no-scripttools -no-declarative -no-declarative-debug -qt-style-windows -qt-style-windowsxp -qt-style-windowsvista -no-style-plastique -no-style-cleanlooks -no-style-motif -no-style-cde -nomake demos -nomake examples
    $ mingw32-make


Now we are ready to start the cloning process.

If you are worried about compilation, it would be wise to jump ahead and ensure everything is working with compiling the client  before working with the clone.

## 4. The Clone

In this guide we will be cloning Litecoin. Litecoin is a Scrypt based coin and the original altcoin. I will be calling this coin “Clonecoin” (CLN).

### 4a. Download and extract the Litecoin source.
 
[https://github.com/litecoin-project/litecoin](https://github.com/litecoin-project/litecoin)

In this guide I will be placing the source code in ``C:\Clonecoin``

### 4b. Copy and Replace Litecoin 

Using your test editor, search out and replace all instances of “Litecoin” with “Clonecoin”. Make sure your search is case sensitive and search for all instances, replace “Litecoin” with “Clonecoin”, “litecoin” with “clonecoin” etc. Run a search without case sensitivity before continuing to ensure you have all instances.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/61a9b7b8ea5db179b30f979d109847e473d0de81](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/61a9b7b8ea5db179b30f979d109847e473d0de81)


### 4c. Copy and Replace LTC.
 
Using your test editor, search out and replace all instances of “LTC” with “CLN”.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/7b6a2ad68deb97caab802c460ebfe5104fa72e2c](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/7b6a2ad68deb97caab802c460ebfe5104fa72e2c)


### 4d. Change rpc and port numbers.

Search for an appropriate port and rpc number [http://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers](http://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers).

Litecoin uses  port 9333 testnet 19333, rpcport 9332 testnet 19332. We will change them to port 10333 testnet 11333, rpcport 10332 testnet 11332

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/7f149b069f77b3e174ca8a7b10b98287c3e663a9](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/7f149b069f77b3e174ca8a7b10b98287c3e663a9)


### 4e. Change starting letter for addresses.
 
In this case we change the 48 to 28, therefore all addresses will start with “C”.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/d0621b86a358e93495658d564640144458aab8ee](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/d0621b86a358e93495658d564640144458aab8ee)


### 4f. Update client version number. 

Since its really a fork of Litecoin we will bring the version numbers up to 1.0.0.0.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/95d0bef6e6a7bf27f3ed6d8153fccf8275524ba9](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/95d0bef6e6a7bf27f3ed6d8153fccf8275524ba9)


### 4g. Change Litecoin example addresses to Clonecoin Addresses. 

Here we change the LTC addresss ``Ler4HNAEfwYhBmGXcFP2Po1NpRUEiK8km2`` to a Clonecoin mystery address starting with c. (see step 6d)

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/9a5321bfb9b0482ed3b435edb815d8eee268b949](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/9a5321bfb9b0482ed3b435edb815d8eee268b949)


### 4h. Change char pchMessageStart and ParseHex.
 
We want these to be unique to Clonecoin. Be wary of changing ``pchMessageStart`` to to letters other than ``a-f``. All numbers are fine to use.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/011b9a8e713821d8010a827f7aeacf09c772a267](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/011b9a8e713821d8010a827f7aeacf09c772a267)


### 4i. Change alert keys
. 
We just change these to be different from Litecoin to avoid the Litecoin messages.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/0798f246007c9196bcfcf39c2ef2222a660d59d2](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/0798f246007c9196bcfcf39c2ef2222a660d59d2)


### 4j. Remove Merkel root and Genesis Block.

These will be replaced later on. Though for now and in the near future they are no longer needed.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/46bbcb1377ac2db0f8dabc19faffb9ab6f989cb6](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/46bbcb1377ac2db0f8dabc19faffb9ab6f989cb6)

### 4k. Remove Nonce and testnet genesis. 

We remove the testnet genesis block and nonce.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/24cf6793c02369fc60a8b67645818f0cf7d1252a](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/24cf6793c02369fc60a8b67645818f0cf7d1252a)

### 4l. Add Epochtime and Timestamp.
 
To create a genesis block we need an epoch time and a verbal timestamp. The current epoch time can be obtained from [http://www.epochconverter.com/](http://www.epochconverter.com/) and the latest news headline can be used for the verbal timestamp. We also replace the testnet timestamp.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/790f9964abdb0543abe1ee1801562a004349e719](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/790f9964abdb0543abe1ee1801562a004349e719)


### 4m. Fixing the checkpoints.
 
We comment out the hardcoded checkpoint and change the genesis block checkpoint.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/fe0d86a278f4d6470bee697a25256b0340cfc9fd](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/fe0d86a278f4d6470bee697a25256b0340cfc9fd)


### 4n. Change max money supply and coinbase maturity.
 
We just multiplied total coins by 10 and reduced coin based maturity. The higher the number of confirmations the better for the network.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/c43361429062f04b5697f9e9fca19e2f15d2e634](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/c43361429062f04b5697f9e9fca19e2f15d2e634)


### 4o. Change block times from 2.5 minutes to 30 seconds.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/8796946bd1d3d5d15d06ba0e72e4b6bbf1fe1d06](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/8796946bd1d3d5d15d06ba0e72e4b6bbf1fe1d06)


### 4p. Change re-targeting from the ridiculous 2.5 days to every 5 minutes.
 
This is cutting out a small portion of instamining. 

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/a3df6e9dc15009bdb22c60a496c109334cc55864](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/a3df6e9dc15009bdb22c60a496c109334cc55864)


### 4q. Add premine and change block rewards.
 
Since we initially increased block rewards by x10, we will increase the base reward from 50 to 500. We then add a premine on block 2 as well as a staggered decrease in block sizes.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/ddc36732b46fbc38ca06012be127ff994177192d](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/ddc36732b46fbc38ca06012be127ff994177192d)


### 4r. Update Images.

If you have not already, you will need a splash and logo.
You will need to update ``src/rec/icons`` - ``bitcoin.png``, ``bitcoin_testnet.png``, ``bitcoin.icon``, ``bitcoin_testnet.icon`` (all 256x256 pixels), ``toolbar.png`` and ``toolbar_testnet.png`` (16x16 pixels).

Also update ``src/res/images``, ``splash.png``, ``splash_testnet.png`` and ``about.png``.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/08edb2f2648acc373e60c44fbd0558c514697ff7](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/08edb2f2648acc373e60c44fbd0558c514697ff7)


### 4s. Update Seed node- 

First you will need to create a dedicated node. This is a quick easy guide.

Head to [Amazon AWS console](https://console.aws.amazon.com) and create an account. Click on the EC2 link on the left. See [AWS pricing](http://aws.amazon.com/ec2/pricing/)

Create and instance, select ``Microsoft Windows Server 2012 R2 Base``, select your server preference - we chose ``t2.micro`` which is free tier eligible.

Click ``Next: Configure Instance Details``, highlight ``Protect against accidental termination``, click review and launch.

Go to security settings, open all ports and click launch. Create a security key pair and make sure to download it and keep it safe. Launch your instance.

On the aws instance home screen click the Elastic IP tab, click ``allocate Ip address`` and confirm. While still in the Elastic IP tab, click ``allocate`` and allocate to the instance by clicking the top checkbox and identifying your server. Confirm. Your instance will take around 15 minutes to launch.

To connect. Click the instance tab, highlight your instance and press ``connect``. Using your key from earlier, you are now able to download a server shortcut and server password.

Using your new Elastic IP, replace your new IP removing Litecoin old seed nodes. 

``src/net.cpp``

    static const char *strMainNetDNSSeed[][2] = {
       {"clonecointools.com", "54.232.218.200"},
       {NULL, NULL}
    };

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/92e520e8a80294a1964bca707ddca704c2c0bdc9](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/92e520e8a80294a1964bca707ddca704c2c0bdc9)


### 4.t Change the name of the ``bitcoin-qt.pro`` file to ``clonecoin-qt.pro``

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/d309822b3b6519ca6424ac74df054ad351db1d88](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/d309822b3b6519ca6424ac74df054ad351db1d88)



## 5. Hashing the Genesis Block and Merkel Root. 

### 5a. Ability to hash Genesis Block.

We now need to add the ability to hash a new genesis block so we add the following code to main.cpp.

``main.cpp``

    if (true && block.GetHash() != hashGenesisBlock)
    {
        printf("Searching for genesis block...\n");
        // This will figure out a valid hash and Nonce if you're
        // creating a different genesis block:
        uint256 hashTarget = CBigNum().SetCompact(block.nBits).getuint256();
        uint256 thash;
        char scratchpad[SCRYPT_SCRATCHPAD_SIZE];

        loop
        {
            scrypt_1024_1_1_256_sp(BEGIN(block.nVersion), BEGIN(thash), scratchpad);
            if (thash <= hashTarget)
                break;
            if ((block.nNonce & 0xFFF) == 0)
            {
                printf("nonce %08X: hash = %s (target = %s)\n", block.nNonce, thash.ToString().c_str(), hashTarget.ToString().c_str());
            }
            ++block.nNonce;
            if (block.nNonce == 0)
            {
                printf("NONCE WRAPPED, incrementing time\n");
                ++block.nTime;
            }
        }
        printf("block.nTime = %u \n", block.nTime);
        printf("block.nNonce = %u \n", block.nNonce);
        printf("block.GetHash = %s\n", block.GetHash().ToString().c_str());
      
    }

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/8b2e543c6f9c6dde0ebb8a7b73fd06c6d7de18ec](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/8b2e543c6f9c6dde0ebb8a7b73fd06c6d7de18ec)


### 5b. Compiling Clonecoin Windows QT.

Create ``libleveldb.a`` and ``libmemenv.a``. 

Using Msys shell, run. For this we have Clonecoin in ``C:/Clonecoin``

    $ cd /C/clonecoin/src/leveldb
    $ TARGET_OS=NATIVE_WINDOWS make libleveldb.a libmemenv.a

If the file already exists, Msys will inform you so.

Open your ``Clonecoin-qt.pro`` file.

We now need to change the dependency directory locations 

    # Dependency library locations can be customized with:
    #   BOOST_INCLUDE_PATH, BOOST_LIB_PATH, BDB_INCLUDE_PATH,
    #   BDB_LIB_PATH, OPENSSL_INCLUDE_PATH and OPENSSL_LIB_PATH respectively

    OBJECTS_DIR = build
    MOC_DIR = build
    UI_DIR = build


to


    # Dependency library locations can be customized with:
    #   BOOST_INCLUDE_PATH, BOOST_LIB_PATH, BDB_INCLUDE_PATH,
    #   BDB_LIB_PATH, OPENSSL_INCLUDE_PATH and OPENSSL_LIB_PATH respectively
    BOOST_LIB_SUFFIX=-mgw49-mt-s-1_55
    BOOST_INCLUDE_PATH=C:/deps/boost_1_55_0
    BOOST_LIB_PATH=C:/deps/boost_1_55_0/stage/lib
    BDB_INCLUDE_PATH=C:/deps/db-4.8.30.NC/build_unix
    BDB_LIB_PATH=C:/deps/db-4.8.30.NC/build_unix
    OPENSSL_INCLUDE_PATH=C:/deps/openssl-1.0.1j/include
    OPENSSL_LIB_PATH=C:/deps/openssl-1.0.1j
    MINIUPNPC_INCLUDE_PATH=C:/deps/
    MINIUPNPC_LIB_PATH=C:/deps/miniupnpc
    QRENCODE_INCLUDE_PATH=C:/deps/qrencode-3.4.4
    QRENCODE_LIB_PATH=C:/deps/qrencode-3.4.4/.libs
    OBJECTS_DIR = build
    MOC_DIR = build
    UI_DIR = build


and comment out the ``genleveldb`` command


    genleveldb.commands = cd $$PWD/src/leveldb && CC=$$QMAKE_CC CXX=$$QMAKE_CXX $(MAKE) OPT=\"$$QMAKE_CXXFLAGS 


to


    #genleveldb.commands = cd $$PWD/src/leveldb && CC=$$QMAKE_CC CXX=$$QMAKE_CXX $(MAKE) OPT=\"$$QMAKE_CXXFLAGS 


and add the flags for a static build.

Add


    CONFIG += static


to 


    CONFIG += thread
    CONFIG += static


and 
 

    win32:QMAKE_LFLAGS *= -Wl,--large-address-aware


to


    win32:QMAKE_LFLAGS *= -Wl,--large-address-aware  -static


Now from the Windows cmd, run  


    > set PATH=%PATH%;C:\Qt\4.8.6\bin
    > cd C:\clonecoin\
    > qmake "USE_QRCODE=1" "USE_UPNP=1" "USE_IPV6=1" clonecoin-qt.pro
    > mingw32-make -f Makefile.Release

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/5c82150b6d017412f6df4f06f86941de2bebae83](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/5c82150b6d017412f6df4f06f86941de2bebae83)


Your ``Clonecoin-qt`` should now be available in your ``C:\clonecoin\release`` folder after around 5 minutes. If errors occur, scroll up and read them try to identify and fix.

### 5c. Generating Merkel Root

Start your ``Clonecoin-qt``. You should see an error Assertion failed! 

Navigate to your Clonecoin appdata folder ``C:\Users\(YOUR*PC*NAME)\AppData\Roaming\Clonecoin`` and open the debug log in a text editor. The folder is hidden by default, so typing ``%appdata%`` in the Windows search bar will bring up access to the roaming\clonecoin folder.

Scroll to the bottom of the text to find the following lines.

    2014-11-06 17:00:04 LoadBlockIndexDB(): last block file = 0
    2014-11-06 17:00:04 LoadBlockIndexDB(): transaction index disabled
    2014-11-06 17:00:04 Initializing databases...
    2014-11-06 17:00:04 71154501f2bb79422cb9d06775463810e8ae59243460250f6c942ebd3a9712dd
    2014-11-06 17:00:04 0000000000000000000000000000000000000000000000000000000000000000
    2014-11-06 17:00:04 d010ddcc6651af0e28e50ee36096e438b7974da9d58f1be95a968b180756a0c8


The bottom hash is the merkel root, we take this and add it to ``main.cpp``

    assert(block.hashMerkleRoot == uint256("0xd010ddcc6651af0e28e50ee36096e438b7974da9d58f1be95a968b180756a0c8"));

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/c776fb6da5599cc9a3bde9749880d9a1f9a1222a](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/c776fb6da5599cc9a3bde9749880d9a1f9a1222a)


### 5d. Hashing the Genesis Block.

We now need to recompile the client in Windows ``cmd``. You can remove the path and directory if you still have the client open.

    > set PATH=%PATH%;C:\Qt\4.8.6\bin
    > cd C:\clonecoin\
    > qmake "USE_QRCODE=1" "USE_UPNP=1" "USE_IPV6=1" clonecoin-qt.pro
    > mingw32-make -f Makefile.Release


Restart the client. The previous Merkel error should  not occur and the client should appear to hang on launch. It is now hashing your genesis block.

How long this takes can vary from a few seconds to minutes. Once the client hangs with a genesis block error, open your debug text file again in your Clonecoin appdata folder ``C:\Users\(YOUR*PC*NAME)\AppData\Roaming\Clonecoin``

    2014-11-05 18:29:11 block.nNonce = 2110551 
    2014-11-05 18:29:11 block.GetHash = 235b6e7fa788b4a0914a959c7ccb38f6cb2706a4c5bd68c0d64f22ba7772baf9

We will now add these to ``main.ccp``.

    @@ -35,7 +35,7 @@ CTxMemPool mempool;
    unsigned int nTransactionsUpdated = 0;

    map<uint256, CBlockIndex*> mapBlockIndex;
    uint256 hashGenesisBlock("0x");
    uint256 hashGenesisBlock("0x235b6e7fa788b4a0914a959c7ccb38f6cb2706a4c5bd68c0d64f22ba7772baf9");
    static CBigNum bnProofOfWorkLimit(~uint256(0) >> 20); // Clonecoin: starting difficulty is 1 / 2^12
    CBlockIndex* pindexGenesisBlock = NULL;
    int nBestHeight = -1;
    @@ -2757,7 +2757,7 @@ bool LoadBlockIndex()
         pchMessageStart[1] = 0xb2;
         pchMessageStart[2] = 0xa4;
         pchMessageStart[3] = 0xdc;
         hashGenesisBlock = uint256("0x");
         hashGenesisBlock = uint256("0x235b6e7fa788b4a0914a959c7ccb38f6cb2706a4c5bd68c0d64f22ba7772baf9");
       }

       //
    @@ -2804,12 +2804,12 @@ bool InitBlockIndex() {
         block.nVersion = 1;
         block.nTime   = 1415210670;
         block.nBits   = 0x1e0ffff0;
         block.nNonce  = 0;
         block.nNonce  = 2110551;

         if (fTestNet)
         {
           block.nTime   = 1415210670;
           block.nNonce  = 0;
           block.nNonce  = 2110551;
         }

         //// debug print

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/789abc8f316efe9026a781c28934e3d3df69f57a](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/789abc8f316efe9026a781c28934e3d3df69f57a)


Recompile the Windows QT. From the Windows ``cmd``, run  

    > set PATH=%PATH%;C:\Qt\4.8.6\bin
    > cd C:\clonecoin\
    > qmake "USE_QRCODE=1" "USE_UPNP=1" "USE_IPV6=1" clonecoin-qt.pro
    > mingw32-make -f Makefile.Release


Your ``Clonecoin-qt`` should now be available in your ``C:\clonecoin\release`` folder.

## 6. Connecting your nodes.

Now you have your client we need to connect the nodes to check everything is working. You can use testnet though its just as easy to use mainnet. 

Connect to your server we set up earlier or use another local machine.

### 6a. Create a conf. file.

We only create this now to enable mining to check the network.

Your conf. file should be placed in ``C:\Users\(YOUR**PC**NAME)\AppData\Roaming\clonecoin``.

To create a conf file, right click ``new->text document``. Copy and paste the code below replacing a suitable username and password. Click ``save``, change file type to ``all`` and save as ``clonecoin.conf``. Or just [download this one](https://www.mediafire.com/?taozsy80yaay1bz)


    rpcuser=Yourusername
    rpcpassword=Yourpassword
    rpcallowip=127.0.0.1
    daemon=1
    server=1
    listen=1
    port=10333
    rpcport=10332
    addnode=54.232.218.200


### 6b. Connect

#### Server

Upload your client to the server and start the client. The two clients should connect. 

#### Home Network

You may need to add your local IPs to the conf file. To do this type ``cmd`` to bring up command prompt, type ``ipconfig`` and use the IPv4 address in your ``addnode`` settings on both machines.


    rpcuser=Yourusername
    rpcpassword=Yourpassword
    rpcallowip=127.0.0.1
    daemon=1
    server=1
    listen=1
    port=10333
    rpcport=10332
    addnode=10.0.0.18
    addnode=10.0.0.31


Once both clients are connected you can start to mine blocks.

You can either use the traditional Scrypt miner or type ``setgenerate true -1`` into your main console.

Mine as many blocks as you want, checking diff adjustment and ensure block rewards are correct. It is advised to confirm some transactions, send some coins and check the client for any errors or adjustments.

In this case I missed the toolbar.png and testnet_toolbar.png as a deliberate example of why you "SHOULD ALWAYS CHECK YOUR CLIENT BEFORE RELEASE"

If you want to restart the chain you need to delete the chain by going to your Clonecoin roaming folder on both machines and deleting everything. 

## 7. Checkpointing the premine.

If you followed all the steps above you should be sitting with a lovely source code and compiled client.

We have a few things to finish and checkpointing the premine is highly important.

Many coin launches have been lost by people not knowing or forgetting to do this step. Without a checkpoint you can very likely kiss your premine goodbye to a hash attack on launch.

Start your compiled clients on both machines. Since we deleted the blockchain earlier mine your premine, plus 2-3 blocks.

Open the concole on the clonecoin client and type; ``getblockhash 1``, ``getblockhash 2``, ``getblockhash 3``. We will use these three hashes to checkpoint the premine.

We also need some data from the ``C:\Users\(YOUR**PC**NAME)\AppData\Roaming\clonecoin\debug`` file. 

We are looking for the details of the highest checkpointed block, in this case block 3. 

    2014-11-11 15:02:57 SetBestChain: new best=718732cb3323ceaa46c8fc5fd521e7f7e31e424c59cc2a02e4e39c2c7306a649  height=3 log2_work=22.000022 tx=4 date=2014-11-11 15:02:57 progress=1.000000

You will need to convert the last block time to an epochtime date i.e. in this instance, from 2014-11-11 15:02:57 to 1415718177. [Use epochconverter for convenience](http://www.epochconverter.com/)

Now we add the block hashes for blocks 1, 2 and 3 and insert the highest block (block 3) details into the  checkpoint block details. We also add the estimated number of transactions per day after the checkpoint.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/d5e61c1d0e7678cc165acf9dc1a27c6d23200030.](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/d5e61c1d0e7678cc165acf9dc1a27c6d23200030.)


Recompile your client.

Back up your  ``C:\Users\(YOUR**PC**NAME)\AppData\Roaming\clonecoin`` folder. This now has your premine. 

You now need to check the checkpoints are correct. On the client that does not have the premine, navigate to ``C:\Users\(YOUR**PC**NAME)\AppData\Roaming\clonecoin`` and delete everything EXCEPT ``wallet.dat`` (very important, DO NOT DELETE) and ``clonecoin.conf`` files.

Restart the client. If your checkpoints are correct the client should update and sync without issues. 


## 8. Clean up your code.

Clean up your ``README`` with your new specifications, rewards, website etc.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/13fc52d07ed55d5b95071a043e88b13a6ad92a67](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/13fc52d07ed55d5b95071a043e88b13a6ad92a67)


Remove your build deps and changes from ``clonecoin-qt.pro``

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/437d50f106d588edd95fd35eec06b2da7cf3d49e](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/437d50f106d588edd95fd35eec06b2da7cf3d49e)



## 9. Compiling Clonecoind.

### 9a. Compile Clonecoind

Navigate to  ``C:\clonecoin\src\makefile.mingw`` and open with your text editor. You will see:


    USE_UPNP:=-
    USE_IPV6:=1

    DEPSDIR?=/usr/local
    BOOST_SUFFIX?=-mgw46-mt-sd-1_52

    INCLUDEPATHS= \
     -I"$(CURDIR)" \
     -I"$(DEPSDIR)/include"

    LIBPATHS= \
     -L"$(CURDIR)/leveldb" \
     -L"$(DEPSDIR)/lib"

    LIBS= \
     -l leveldb \
     -l memenv \
     -l boost_system$(BOOST_SUFFIX) \
     -l boost_filesystem$(BOOST_SUFFIX) \
     -l boost_program_options$(BOOST_SUFFIX) \
     -l boost_thread$(BOOST_SUFFIX) \
     -l boost_chrono$(BOOST_SUFFIX) \
     -l db_cxx \
     -l ssl \
     -l crypto

    DEFS=-D_MT -DWIN32 -D_WINDOWS -DBOOST_THREAD_USE_LIB -DBOOST_SPIRIT_THREADSAFE
    DEBUGFLAGS=-g
    CFLAGS=-mthreads -O2 -w -Wall -Wextra -Wformat -Wformat-security -Wno-unused-parameter $(DEBUGFLAGS) $(DEFS) $(INCLUDEPATHS)
    # enable: ASLR, DEP and large address aware
    LDFLAGS=-Wl,--dynamicbase -Wl,--nxcompat -Wl,--large-address-aware


change it to read:


    USE_UPNP:=1
    USE_IPV6:=1

    DEPSDIR?=/usr/local
    BOOST_SUFFIX?=-mgw49-mt-s-1_55

    INCLUDEPATHS= \
     -I"$(CURDIR)" \
     -I"/c/deps/boost_1_55_0" \
     -I"/c/deps" \
     -I"/c/deps/db-4.8.30.NC/build_unix" \
     -I"/c/deps/openssl-1.0.1j/include"
     
    LIBPATHS= \
     -L"$(CURDIR)/leveldb" \
     -L"/c/deps/boost_1_55_0/stage/lib" \
     -L"/c/deps/miniupnpc" \
     -L"/c/deps/db-4.8.30.NC/build_unix" \
     -L"/c/deps/openssl-1.0.1j"

    LIBS= \
     -l leveldb \
     -l memenv \
     -l boost_system$(BOOST_SUFFIX) \
     -l boost_filesystem$(BOOST_SUFFIX) \
     -l boost_program_options$(BOOST_SUFFIX) \
     -l boost_thread$(BOOST_SUFFIX) \
     -l boost_chrono$(BOOST_SUFFIX) \
     -l db_cxx \
     -l ssl \
     -l crypto

    DEFS=-D_MT -DWIN32 -D_WINDOWS -DBOOST_THREAD_USE_LIB -DBOOST_SPIRIT_THREADSAFE
    DEBUGFLAGS=-g
    CFLAGS=-mthreads -O2 -w -Wall -Wextra -Wformat -Wformat-security -Wno-unused-parameter $(DEBUGFLAGS) $(DEFS) $(INCLUDEPATHS)
    # enable: ASLR, DEP and large address aware
    LDFLAGS=-Wl,--dynamicbase -Wl,--nxcompat -Wl,--large-address-aware -static


We change the deps to point to the deps we created earlier. If you chose to place your deps in a different folder, change the code to point to your folders. We also used ``-static`` in ``LDFLAGS=-Wl,--dynamicbase -Wl,--nxcompat -Wl,--large-address-aware -static`` for a static linked exe,  updated UPNP Includes and Lib paths to enable UPNP.

In the Msys shell, you can now compile litecoind.

    cd /c/clonecoin/src
    make -f makefile.mingw
    strip clonecoind.exe


Your clonecoind should now be in your C:\clonecoin\src folder.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/6b124d98f059fb42b2b8837b520b6a626ec6f5ef](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/6b124d98f059fb42b2b8837b520b6a626ec6f5ef)


### 9b. Remove libleveldb.a and libmemev.a from C:\Clonecoin\src\leveldb.

Remove your ``Clonecoin-qt`` from the release folder and zip for release. 

Delete the release, debug and build folders. This is your code for release.


## 10. Github for release, made easy.

1. Create a Github account.
2. Download the [latest Github Windows client](https://windows.github.com/). Then run the Github install and use your login details from Github to log into the client.
3. Navigate to you Github account, click ``repositories->new``. Enter the repository name, description and public or private. “Public” allows everyone to see your code and is recommended for advanced users who can push codes quickly. Most launches will choose a paid private account, allowing them to pre-load the release source code and open the repository from public to private instantly. Click done, then on the next screen click the green “Set up in Desktop” button. Allow the browser to launch the Github client, select the location of your Github depositories, usually in the Github folder of your documents. Click “OK”. You now have a folder that you can update your source code and easily push commits to Github.

### 10a. Easy Pushing Commits/Launch Code.

Copy and paste your source code into the ``documents/github/yourcoinnamefolder``. In your Windows Github client, click on your client name on the left hand side.

Your Github client should recognise a host of changes if present. Fill in the commit details, select the files that need to be committed, usually all and on by default and press commit. 

On the top right hand side will be a publish or sync box, click that and the Github Windows client will push the changes and source code to your repository on Github.

### 10b. Easy Revert Commits.

Open your Github client and ensure it's sync'd. Highlight your repository. Click on the commit to you wish to rollback, then revert.

On the top right hand side will be a publish or sync box, click that and the Github Windows client will push the revert to your repository on Github.

### 10c. Easy Pushing Updates.

Log into your Github Windows client. Click on the altcoin tab in the left and click sync to ensure your local code is up to date.

Edit your local code in your ``documents/github/yourcoinname`` folder.

Once your Github client picks up the changes enter the commit details and commit to Github.

## 11. Common Errors/Mistakes.

### I am getting "this" error.

Most errors can be solved with a little effort. The compiler will usually display an error message or warning. Read it.

If it's UPNP error check your directories in your pro file, then check your UPNP deps, rebuild them.

Google it. Most things can be solved far quicker with a little investigation into the errors vs posting in a forum and awaiting reply.

### I am still seeing the old logos on my desktop shortcuts.

Windows cache has cached the image. The easiest way to solve this is run a program such as Glarys Utilities to clear your PC. Also delete the build folder in between builds to ensure your builds are clean.

### Makefile.Release:291: recipe for target 'release\clonecoin-qt.exe' failed

Close your client.


## 12. Creating your own logo.

There are a few easy ways to get a logo. If you have Photoshop and want a easy template try [http://apsdfile.com/coin-generator-for-photoshop/](http://apsdfile.com/coin-generator-for-photoshop/).

Install GIMP. GIMP is a free utility available to download from [http://www.gimp.org/](http://www.gimp.org/) and try youtube vids. 

For those looking for an even faster alternative try tools like [http://www.onlinebadgemaker.com/3d-badge-maker](http://www.onlinebadgemaker.com/3d-badge-maker).

These can be used for quick launches or temporary images while you wait, purchase or make an official one.

## 13. The Website.

### 13a. The Template.

Download and install a free website editor, [Bluegriffon](http://bluegriffon.org/) is a prime example.

Find yourself a [suitable template](http://www.freshdesignweb.com/free-html5-css3-templates.html). Download and edit the template with all your coin details. 

### 13b. Upload to a website.

Create an account at [Namecheap](http://www.namecheap.com/), they accept BTC.

Register the domain and commission hosting at the same time, that way there is no DNS delay.

Usually you can pick up a year hosting with domain and SSL if you want for under .15 BTC.

If this is a one-off coin launch then a simple hosting plan will suffice. If you're looking to launch more coins, choose a dedicated server or reseller plan.

Once your order is confirmed log into cpanel with the details provided, enable cloudflare and ssl of you purchased it.

Single hosting plans will require support for SSL, dedicated or reseller accounts have the ability to self enable through WHM.

In CPanel, go to file manager and upload your site to the public_html folder. Your website should be now viewable on your domain.


## 14. The Launch. Ninja vs Pumped vs ICO.

Launching a coin is the make or break point. The style of launch will dictate how to prepare.

### 14a. Prelaunch.

The key to a good launch is timing and consistency. Don't release the code early and make sure it works.

Create your Bitcointalk account. The earlier the better to get rid of posting restrictions on new accounts.

Create accounts on Twitter, Facebook, cryptocointalk, IRC, Reddit and all the usual channels.

### 14b. The Ninja

This gives the developer more time, no restrictions with no one looking or ready. With these coins you can set the network up early and don't have people looking for the code.

Uploading the code to github a minute easily will likely be enough time to stop anyone searching. Website can go live early and some argue it gives miners a better chance.

Usually a ninja launch involves a instamine allowing the developers to mine many blocks.

### 14c. The Pumped.

Harder to do. The pre-hype means you will have people looking for the code on Github and websites.

Your code needs to be solid to handle a massive intake of hashing power and be prepared for the harshest critics.

### 14d. The ICO.

An advanced pump coin that needs a reliable escrow, good hype and delivery of goods.

Most ICO's deliver nothing but BTC to the developer and broken promises to the users.

Find a good escrow, take time with your code and remember to keep an open and clear communication.

---

## What do we call this time? - [George Monbiot, the Guardian](http://www.theguardian.com/commentisfree/2014/oct/14/age-of-loneliness-killing-us)

It’s not the information age: the collapse of popular education movements left a void filled by marketing and conspiracy theories. Like the stone age, iron age and space age, the digital age says plenty about our artefacts but little about society. The anthropocene, in which humans exert a major impact on the biosphere, fails to distinguish this century from the previous 20. What clear social change marks out our time from those that precede it? To me it’s obvious. This is the Age of Loneliness.

When Thomas Hobbes claimed that in the state of nature, before authority arose to keep us in check, we were engaged in a war “of every man against every man”, he could not have been more wrong. We were social creatures from the start, mammalian bees, who depended entirely on each other. The hominins of east Africa could not have survived one night alone. **We are shaped, to a greater extent than almost any other species, by contact with others.** The age we are entering, in which we exist apart, is unlike any that has gone before.

Three months ago we read that loneliness has become an epidemic among young adults. Now we learn that it is just as great an affliction of older people. A study by Independent Age shows that severe loneliness in England blights the lives of 700,000 men and 1.1m women over 50, and is rising with astonishing speed.

Ebola is unlikely ever to kill as many people as this disease strikes down. Social isolation is as potent a cause of early death as smoking 15 cigarettes a day; loneliness, research suggests, is twice as deadly as obesity. Dementia, high blood pressure, alcoholism and accidents – all these, like depression, paranoia, anxiety and suicide, become more prevalent when connections are cut. We cannot cope alone.

Yes, factories have closed, people travel by car instead of buses, use YouTube rather than the cinema. But these shifts alone fail to explain the speed of our social collapse. These structural changes have been accompanied by a life-denying ideology, which enforces and celebrates our social isolation. **The war of every man against every man – competition and individualism, in other words – is the religion of our time, justified by a mythology of lone rangers, sole traders, self-starters, self-made men and women, going it alone.** For the most social of creatures, who cannot prosper without love, there is no such thing as society, only heroic individualism. What counts is to win. The rest is collateral damage.

British children no longer aspire to be train drivers or nurses – more than a fifth say they “just want to be rich”: wealth and fame are the sole ambitions of 40% of those surveyed. A government study in June revealed that Britain is the loneliness capital of Europe. We are less likely than other Europeans to have close friends or to know our neighbours. Who can be surprised, when everywhere we are urged to fight like stray dogs over a dustbin?

We have changed our language to reflect this shift. Our most cutting insult is “loser”. We no longer talk about people. Now we call them individuals. So pervasive has this alienating, atomising term become that even the charities fighting loneliness use it to describe the bipedal entities formerly known as human beings. We can scarcely complete a sentence without getting personal. Personally speaking (to distinguish myself from a ventriloquist’s dummy), I prefer personal friends to the impersonal variety and personal belongings to the kind that don’t belong to me. Though that’s just my personal preference, otherwise known as my preference.

One of the tragic outcomes of loneliness is that people turn to their televisions for consolation: two-fifths of older people report that the one-eyed god is their principal company. This self-medication aggravates the disease. Research by economists at the University of Milan suggests that television helps to drive competitive aspiration. It strongly reinforces the income-happiness paradox: the fact that, as national incomes rise, happiness does not rise with them.

Aspiration, which increases with income, ensures that the point of arrival, of sustained satisfaction, retreats before us. The researchers found that those who watch a lot of TV derive less satisfaction from a given level of income than those who watch only a little. TV speeds up the hedonic treadmill, forcing us to strive even harder to sustain the same level of satisfaction. You have only to think of the wall-to-wall auctions on daytime TV, Dragon’s Den, the Apprentice and the myriad forms of career-making competition the medium celebrates, the generalised obsession with fame and wealth, the pervasive sense, in watching it, that life is somewhere other than where you are, to see why this might be.

So what’s the point? What do we gain from this war of all against all? Competition drives growth, but growth no longer makes us wealthier. Figures published this week show that, while the income of company directors has risen by more than a fifth, wages for the workforce as a whole have fallen in real terms over the past year. The bosses earn – sorry, I mean take – 120 times more than the average full-time worker. (In 2000, it was 47 times). And even if competition did make us richer, it would make us no happier, as the satisfaction derived from a rise in income would be undermined by the aspirational impacts of competition.

The top 1% own 48% of global wealth, but even they aren’t happy. A survey by Boston College of people with an average net worth of $78m found that they too were assailed by anxiety, dissatisfaction and loneliness. Many of them reported feeling financially insecure: to reach safe ground, they believed, they would need, on average, about 25% more money. (And if they got it? They’d doubtless need another 25%). One respondent said he wouldn’t get there until he had $1bn in the bank.

For this, we have ripped the natural world apart, degraded our conditions of life, surrendered our freedoms and prospects of contentment to a compulsive, atomising, joyless hedonism, in which, having consumed all else, we start to prey upon ourselves. For this, we have destroyed the essence of humanity: our connectedness.

Yes, there are palliatives, clever and delightful schemes like Men in Sheds and Walking Football developed by charities for isolated older people. But **if we are to break this cycle and come together once more, we must confront the world-eating, flesh-eating system into which we have been forced**.

Hobbes’s pre-social condition was a myth. But we are entering a post-social condition our ancestors would have believed impossible. Our lives are becoming nasty, brutish and long.

---

## 21 Bitcoin computer

### 1.
My theory is that their real motivation is to ensure that there continues to be a robust mining ecosystem when the block reward falls off to the point that nobody wants to mine anymore without high transaction fees. So they proliferate a bunch of low cost mining gadgets that people will use primarily for the convenience it offers in making micropayments and in verifying identity, while they also do mining to ensure the health of the network but not actually make any significant money for the owner.

This would be the first iteration of their first gadget, which isn't cheap yet but could be if volumes are high enough, and future iterations would be cheaper and better.

The identity feature is my speculation based on tweets by the CEO about the need for better identity solutions and the enormous market for solving identity fraud problems. Not sure how a gadget like this addresses that but I think it is part of their plan.

### 2.

The three most difficult questions with blockchain technology are "where is the blockchain data?", "where are the keys that represent my wallet?" and "how do I get my initial bitcoin?"

This product very succinctly answers both questions in a reliable way.

It looks like they've got some basic ability to write to the blockchain, and since this only costs a few thousand satoshis, the very small amounts of Bitcoin that this device mine will be useful.

It looks like they're hoping that further profits can be driven back to the address that wrote to the blockchain.

This is a really good idea but fully dependent on how hackable this is.

Like, do I get the full Bitcoin JSON-RPC interface?

This would let me use this device as a pretty reliable source of identification, using Bitcoin's public key infrastructure to sign and authenticate messages.

It would also let me write client software on behalf of the physical device that could read and write arbitrary messages to the Bitcoin blockchain, allowing for custom colored coins, but with keychain ownership contained only within the physical device, instead of on an external server or running on a laptop.

Do I have direct programmable access to the SHA-256 ASIC?

This would help with content-addressable distributions systems like IPFS.

It would be great if the device could expose an interface that was compatible with both Common Wallet and Common Blockchain.

Common Blockchain[1] is a protocol that aims to make an abstraction of queries against the blockchain, allowing devices like the 21 Bitcoin Computer, the Bitcoin Core software, and web services like Blockcypher to expose a single interface to client software and Blockchain meta-protocols like Open Assets, Blockcast [2] and Open Publish [3].

Likewise, Common Wallet is a protocol that aims to make an abstraction for wallets and key signing devices like the 21 Bitcoin Computer, Trezor, Mycellium, or Bitcoin Core, so all of these devices can sign custom transactions that were built by external libraries like Open Publish and to sign authentication messages for services like Bitstore [5].

There is a very big problem with interoperability between various Bitcoin wallets, protocols, and services, and there is really no reason for this to be the case if everyone were to expose the proper interfaces, which roughly model the Bitcoin JSON-RPC.

[1] https://github.com/blockai/abstract-common-blockchain
[2] https://github.com/blockai/blockcast
[3] https://github.com/blockai/openpublish
[4] https://github.com/blockai/abstract-common-wallet
[5] https://github.com/blockai/bitstore-client

---

## BOA patent

The [Bank of America patent application](http://pdfaiw.uspto.gov/.aiw?Docid=20150262173&homeurl=http%3A%2F%2Fappft.uspto.gov%2Fnetacgi%2Fnph-Parser%3FSect1%3DPTO2%2526Sect2%3DHITOFF%2526p%3D1%2526u%3D%25252Fnetahtml%25252FPTO%25252Fsearch-bool.html%2526r%3D7%2526f%3DG%2526l%3D50%2526co1%3DAND%2526d%3DPG01%2526s1%3Dbitcoin%2526OS%3Dbitcoin%2526RS%3Dbitcoin&PageNum=&Rtype=&SectionNum=&idkey=E2F1CFDFD16C) makes not one single mention of the blockchain. 

BOA are just getting their oar in first, staking a claim to be able to optionally use their current system to route wire transfers via existing cryptocurrency networks when reliability/time/control factors are an economic factor.

![Image](http://i.imgur.com/D4X01Po.png)

> FIG. 1 illustrates an example cryptocurrency wire transfer environment 100 according to certain embodiments. In general, wire transfers are used by enterprises, such as financial institutions, to transfer funds from one customer account to another customer account. Some wire transfers may move funds from a customer account in one country to a customer account in another country. In response, the enterprise may decide to use a cryptocurrency to transfer the funds. A cryptocurrency is typically a peer-to-peer, decentralized, digital currency whose implementation relies on the principles of cryptography to validate transactions and generate the currency itself. Some examples of cryptocurrencies are: Bitcoin, Litecoin, Ripple, Peercoin, and Dogecoin. In some instances, a cryptocurrency, such as MintChip, may be backed by a government (e.g., Canada). To transfer funds using cryptocurrency, an enterprise may receive payment from a customer and purchase a quantity of a chosen cryptocurrency, at a local cryptocurrency exchange, in an amount equivalent to the received payment. Essentially simultaneously or shortly thereafter, the enterprise may sell the quantity of the chosen cryptocurrency at a foreign cryptocurrency exchange, resulting in a foreign currency that is used by the country in which the recipient account is located. The enterprise may also transfer the quantity of the chosen cryptocurrency from the local cryptocurrency exchange to the foreign cryptocurrency exchange. 


It’s just another app that makes calls on the API of a (dynamically-selected) cryptocurrency in order to effect wire transfers of fiat. In the BOA model, the  cryptocurrency simply acts as a carrier for any run-of-the-mill wire transfer, BOA’s system instructs the exchanges on the fiat-to-crypto-and-back conversions, effects the transfer and makes the final delivery of fiat to the recipient.

The really valuable take-home from this is a US retail bank’s sober assessment of the advantages of using cryptocurrency, a useful arrow for the quiver of anyone making a cryptocurrency business pitch.

And, peering ahead, a pointer to one possible future as envisaged by BOA bankers in which Bitcoin is but one cryptocurrency amongst many (or at least, several)


And in which cryptocurrency exchanges are hosted in jurisdictions all over the globe.

> wherein the first cryptocurrency exchange is located in a first country and the second cryptocurrency exchange is located in a second 

## Marks out of 10

### Methods

Factors to consider when choosing amongst transfer methods.

> consider time factors, price factors associated with particular currencies, price factors associated with particular cryptocurrencies, fees charged by third parties, volatility of particular currencies, volatility of particular cryptocurrencies, economic risk factors, currency exchange rates, or any other information that may facilitate determining one method of transfer is should be used over another method.


### Cryptocurrency

Factors to consider when choosing amongst cryptocurrencies.

> Determine which cryptocurrency to use is based on cryptocurrency price, volatility of the cryptocurrency, popularity of the cryptocurrency, availability of the cryptocurrency at a local cryptocurrency exchange, availability of the cryptocurrency at a foreign cryptocurrency exchange, or any potential risk factor that may be associated with a particular cryptocurrency.


### Cryptocurrency exchanges

Factors to consider when choosing amongst cryptocurrency exchanges.

> determining whether using cryptocurrency is optimal is based at least in part upon an exchange rate associated with the cryptocurrency

> May choose a particular cryptocurrency exchange because the cryptocurrency is priced favorably (e.g., cheap if purchasing, expensive if selling) or because the cryptocurrency exchange has a relationship with the enterprise.

“Examples of cryptocurrency exchanges are OKCoin, BitStamp, BTCChina, Cryptsy, CoinMarket, Justcoin.”

“The local cryptocurrency exchange that is associated with local exchange server may be associated with the same jurisdiction (e.g., country, economic union, political union, etc.) with which a particular customer account may be associated or conducts transactions in a currency associated with the jurisdiction associated with a particular customer account”

---

## SOIL

SOIL is an Ethereum-platform based cryptographic smart contract information and user-created application service, built directly on top of a viable digital currency. 

It will be a consensus-driven and community-managed currency, with a democratically-realized stakeholder input towards further evolution of the system and its applications.

Through the use of the decentralized blockchain, there will be no single individual or small group of individuals with control of the currency, the overall decision making will be achieved through consultation of fair voting by the people who invest in it. The maturation of the system, with a progression of the core devopment can be suggested, voted upon and acted upon by a fair consensus of the community which remains involved with the project, in a transparent and open process.

At it's heart will be **SOIL**, a currency that will be traded as any other digital currency, on major altcoin exchanges online, and on top of this currency will be a decentralized user-created application platform ensuring a global network of computers handling the simple or complex automative needs of a growing industry.

**SOIL** will focus the delivery of smart contracts to a specific sector of industry, thus building a trusted brand. **SOIL** will approach the ecological and agricultural stratum of the commercial world, bridging the gap between cryptocurrency and real-world applications of a progressively automated business sector.

Farmers and ranchers worldwide are migrating towards precision agricultural methods, creating efficiency and efficacy for agricultural inputs and the spatial and temporal management of agricultural systems. [url=http://www.researchmoz.us/]ResearchMoz [/url]has predicted that the agricultural autonomous project market will grow from $817 million from 2013 to a staggering $16.3 BILLION by 2020.

Modern farms are increasingly taking advantage of automated harvesting and tractors, which can operate around the clock and ensure tight operational windows can be achieved, especially for seeding and other time-sensitive activities. Nursery operations rely on automation for planting, pruning, grafting, etc. Weeding and thinning operations are now more and more automated. Crop inspection, data collection and manipulation are controlled by centralized computers to increase the productivity of modern farms. Dairy and poultry farms rely on heavily automated controls to work with their flocks and herds. Unmanned drones are used to inspect crops, sending data back to a centralized hub to be sorted into data and real-time 3D maps
the farmer can use to adjust his operations and produces previously unknown adaptability.

Many of these processes are controlled by centralized servers which are subject to real world hardware failures which cost productivity and affect the bottom line.

By placing these applications in a cryptographically secure and globally decentralized environment, this will remove another risk factor facing the agricultural business, and will, as the system evolves, exponentially increase the base value of **SOIL**, both as a speculative currency and as a platform for automated agricultural practices.

By being the first cryptocurrency based application to tackle these problems, we will be at the forefront of a revolution in both the altcoin world but in a future for real world applications in a automatic ecological and agricultural industry.

---

## Specs

- Mining Algorithm: dagger, Proof-of-Work
- Target Block Time: democratic vote
- Reserve Information (Current pool): 
  - [Info](https://bitcointalk.org/index.php?topic=1176709.msg12455831#msg12455831)
  - [Info](https://bitcointalk.org/index.php?topic=1176709.msg12456330#msg12456330)
- Mining: Block reward established by democratic vote

## Social

- [Twitter](http://twitter.com/SOILcoin)
- [slack](url=http://SOIL-team.slack.com)
- [Facebook](http://facebook.com/groups/SOILcoin)

---

### Testnet setup for Ubuntu 14.04

    apt-get update
    apt-get dist-upgrade
    apt-get install git binutils bison gcc make libgmp3-dev build-essential
    bash < <(curl -s -S -L https://raw.githubusercontent.com/moovweb/gvm/master/binscripts/gvm-installer)
    echo "[[ -s \"$HOME/.gvm/scripts/gvm\" ]] && source \"$HOME/.gvm/scripts/gvm\"" >> ~/.bashrc
    source ~/.bashrc
    gvm install go1.4
    gvm use go1.4 --default
    git clone https://github.com/soilcurrency/go-ethereum.git
    cd go-ethereum
    make gsoil


Create your account:

    build/bin/gsoil account new


Boostrap - load the genesis file:

    build/bin/gsoil --genesis test-net-genesis.json

(wait a few seconds - then use ctrc+c to interrupt)

Start the client:

    build/bin/gsoil --rpc console

Start mining on our testnet:

    miner.start()
    miner.stop()

To increase the number of threads used for mining: ``miner.start(amount of threads)`` i.e.

    miner.start(4)

### Testnet setup for Windows x64

If you never have started gsoil before:

1. Extract the package (e.g. to Desktop: ``C:\Users\username\Desktop\soil_win_x64_v5_alpha``)
2. Doubleclick “new_account.bat” - Set a password. The window should be closing automatically.
3. Doubleclick “genesis.bat”. Wait a few seconds and close the window.
4. Doubleclick “soil.bat” - wait until sync.
5. Doubleclick “SOILsafe.bat” for Gui Wallet

Old hand:

1. Doubleclick “soil.bat”
2. Doubleclick “SOILsafe.bat”

Hooray, we are connected to the testnet! Now you can start to mine on our testnet:

    miner.start()
    miner.stop()

GPU mining:

1. Doubleclick “gpu_mining_solo.bat”

### Nodes:

    admin.addPeer('enode://0c0ce5d1b95de13732faa98d0ea5d6acafabdf2ec56104a52ffb7f34ee2fa08bb09524cd6e9c28ba5a57a84ec0352fd52a3065ea6af51967afba78537412b3c4@45.63.84.6:39338')
    admin.addPeer('enode://20b058d1e867b665f6e698100325f68e07ebface3ebef6aaacc5b00b7b77c10fc338e7863e933a497ae1b85d2f2a7b7b59d18d0eb48f05eb92d7d1a947399b31@113.161.82.243:39338')
    admin.addPeer('enode://24e1e3b7bba2b0de7707dcc957faf541b87e99a665ff6cf93a1d6b60c2f65603dc69b14e97eb1e3219fa52bd26a27bb26957c0126da154a4895fc4ef873bac54@45.32.239.236:39338')
    admin.addPeer('enode://a076e6e4f86f00074729a8473e3b3799208648f5952b1cd8df2c8b61816f44289b1cc6bb4d6116d0f48447f38540d5b2891aaea8062895c9867a0818bb6ec2f5@138.128.169.51:39338')
    admin.addPeer('enode://2214963c7bb2fb98c0edefa09ebc46c5fbcb5055c7fdd884d90e6b8ed8acb6568f1f035b25e609346e09f681323be60b5998dc49f02582dd78f766e31679e2e5@45.32.232.65:39338')
    admin.addPeer('enode://30bd5e679759792be064edef05d5195889337294af1788072e4ad8bed6ea8bb559f00e8a43f275e945aacc5aed8117d950f79057bc7675742eacbf937f68393e@52.25.0.225:39338')
    admin.addPeer('enode://fb2bc8add1af21cb0f34710a3ded14a003da44a5e7cc80f963e46f417fc0a31d94bb5a25b62ff13b3e07df950028b85f0589e7eef3d46d5abeb2a32b0d051475@46.101.231.134:39338')
    admin.addPeer('enode://d482c87d6085fe3f303d2a3a8d25937eda09f75713610dd68c475031c110e658da78fa207574c370e4f6121aed21d77a2e73a4ddab8af50aaeb6cf4672f5fe5c@178.62.133.174:39338')
    admin.addPeer('enode://5daffbd838b3745d17b202505f3c5d89f4926e5b0642123c1fbd1f0ce655c83242514ce13dc9ab4d7a0fa612ab8934525eec6265eaf19c7b3c10a61f77869a1e@95.170.180.71:39338')

### Cheat Sheet for Gsoil:

- List all accounts: ``personal.listAccounts``
- Unlock the account: ``personal.unlockAccount(addr, passwd, duration)``
- BlockHeight: ``eth.blockNumber``
- Node information: ``admin.nodeInfo``
- Information about connected peers: ``admin.peers``
- Adding a node: ``admin.addPeer("enode://nodekey:ipaddress@port")``
- Balance: ``web3.fromWei(eth.getBalance("address"), "soil")``

---
