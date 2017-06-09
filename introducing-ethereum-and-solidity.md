-----
Ethereal Summit:
https://www.youtube.com/playlist?list=PL4CxcnSy5_bjbJsPktNfX7BsCl90i8Err

Supply Chain:
https://www.youtube.com/watch?v=kMNeXUqzLrs&list=PL4CxcnSy5_bjbJsPktNfX7BsCl90i8Err&index=20


1 - 
----
# 1 - Bridging the Blockchain Knowledge Gap

The term "Ethereum" can be used to refer to three distinct things:
  - The Ethereum Protocol
  - The Etherem Network created by computers using the protocol
  - The Ethereum Project funding development of the aforementioned two

VB - 
  The key component is this idea of a Turing-complete blockchain. ...As a data structure, it works the same way that Bitcoin works, except the difference in Ethereum is, it has this built-in programming language.

Protocol: system of rules that describes how boxes communicate.


What the blockchain is:
  - p2p networking
  - asymmetric cryptography
  - cryptographic hashing

Ethereum was built with the assumption that copycats are a foregone conclusion -- many blockchains --- common protocol by which they can communicate.


The Ethereum network allows anyone to write a trustworthy, self-executing financial contract that will move ether in the future.

Conceivably, this could allow financial contracts that project far into the future, giving stakeholders in the contract a reason to hold and use ether as a store of value.
  - for decentralized smart contracts are in business today
  - can crypto ever be real money, and will it be better than the money to which we are accustomed?



Ether is fuel.
  - it can pay to run programs on Ethereum's network
  - these programs can move ether now, or in the future, when certain conditions are met
  - because of its ability to pay for the execution of transactions in the future, ether can also be considered a commodity -- dimension of intrinsic value over bitcoins; it is not just a store of value (it is valuable, as a rental token for running programs on the ethereum network)

One reason to bring up currencies and commidities in the discussion of smart contracts is to train yourself to think in terms of building economic systems in pure software. That's the promise of Ethereum.

What makes systems like ETH and BTC secure is not that they are based on any hack-proof technology, but rather rely on powerful financial incentives and diseincentives to keep malefactors at bay.

EVM - Changes to the EVM are achieved through hard forking
  - How is this process of pursuation completed?

The protocol:
  - e.x.
    - TCP/IP - transmission control
    - HTTP: transfer
    - SMTP: mail
  - Ethereum Protocol Links:
    https://github.com/ethereum/wiki/wiki/Ethereum-Wire-Protocol
    https://github.com/ethereum/wiki/wiki/Block-Protocol-2.0
    https://github.com/ethereum/go-ethereum/wiki/Ethereum-Specification
  - Application layer is thin because the protocol gives you a lot.
  - Minimal layers on top of what is already an incredibly effective payments network.
    - Result: no startp explosion.

Ethereum Design Doc:
https://github.com/ethereum/wiki/wiki/Design-Rationale
  - Principle 4: we have no features:
    ```
    We Have No Features: as a corollary to generalization, we often refuse to build in even very common high-level use cases as intrinsic parts of the protocol, with the understanding that if people really want to do it they can always create a sub-protocol (eg. ether-backed subcurrency, bitcoin/litecoin/dogecoin sidechain, etc) inside of a contract. An example of this is the lack of a Bitcoin-like "locktime" feature in Ethereum, as such a feature can be simulated via a protocol where users send "signed data packets" and those data packets can be fed into a specialized contract that processes them and performs some corresponding function if the data packet is in some contract-specific sense valid.
    ```

At Scale:
  - traditional web apps are costly in large part because they must be engineered to store and exchange user data, and thus must have systems in place to isolate bad actors in order to elicit trust.
  - e.x. private datacenters
  - When the securty offered by a decentralized network is high enough, online businesses experience drastically lower overhead costs, which they can then pass on to customers to disrupt legacy players.
  - Blockchain-based apps and services are disruptive not only because of their securite nature, but because of how economical they can be to operate at scale.

Ethereum is suited to building economic systems in pure software. 
  - It's software for business logic, wherin people (users) can move money (data representing value) around with the speed and scale that we normally get with data.
  - Not the three-to-seven-day floating period you get with the commercial banking system.
  - Or the fees w/ Visa, MasterCard, Paypal.

With an Ethereum program, it's fairly trivial to pay hundreds of thousands of people in hundreds of countries, small amounts every few minutes, wheras in the legacy banking system you would need an entire payroll department working overtime to constantly rebalance your account ledgers and deal with cross-border issues.

-----

# 2 - The Mist Browser
mist, applications, encryption intro
https://github.com/sdtsui/mist


Encryption Intro:

https://puu.sh/waag0/79e2db5de2.png

Symmetric Encryption: both parties must have the same key.

Asymmetic cryptography:
  - don't trust the channel of communication
  - each person has a PAIR of different, but mathematically related keys
    - Public key cryptography: wartime communications
    - 'computational complexity involved in encrypting the data makes it useful only for small data objects, like the alphanumeic string that becomes your private key'

Symmetric Encryption:
  - Bob and Alice has the same encryption key.
  - It is used to encrypt a message, and decrypt the ciphertext output.

Asymmetric encryption:
  - Public Key: can list on website
    - public keys are used to send message / encrypt info
  - Private key: 
    - private keys are used to decrypt info

Secure Messaging: 
  - Alice encrypts using Bob's public key.
  - Bob decrypts using his matching private key.
  Secure, BUT, anyone could send a message claiming to be Alice.

Secure and Signed Message:
  - Encrypt Alice's plaintext message using her private key.
  - Then Encrypt it again using Bob's public key.
  - When Bob receives, he decrypts using his private key.
  - He must decrypt using Alice's public key.
    - Assures that Alice is the one that originally encrypted using her private key.

Public <> Private, corresponding to
  Q: Is it true that public keys and private keys have the property that ONE can be used to decrypt messages encrypted by the other, and vice-versa?

-----------

If Alice were to only encrypt her plaintext using her own private key, then anyone with her public key could decrypt it. "Open Message Format".  (for leaks/info dumps, etc.)

Digital Signature:
  - Alice hashes plaintext of her message
  - Attach it along with message
  - Encrpyt bundle with own private key.
  - Encrpyt bundle with Bob's public key.

  - When Bob decrypts the ciphertext he can run Alice's plaintext message through the same hashing algorithm Alice used. 
  - Ensures that the message can't be modified, because of the additional step of 
  [HashedPlaintext + Plaintext]

Pretty important to mining.



-----

# 3 - The EVM
how the EVM works

3 - EVM


EVM Opcodes in Ethereum development are roughly equivalent to HTTP verbs.
  e.x.
    STOP/ADD
    LT/GT
    ADDRESS/BALANCE/ORIGIN/CALLVAUE/CODESIZE/CODECOPY/GASPRICE
    LOG0, LOG1/LOG4
    SUICIDE (halt exec and register account for later deletion)

HTTP verb semantics are reliable and well-known.
In Ethereum and Bitcoin, things work differently. Because the network is also a global machine, the "methods" you use to make calls across the network are just machine-language codes, of the ilk used inside an indivudal computer.

Running programs on the EVM:
  - writing and depoying smart contracts, which work in concert to form distributed applications (DApps)
  - each contract has its own address with storage, where it can hold any arbitrary code
  - when a transaction hits this address (Eth transferred) or the contract is called by another contract, its code springs to life inside every node on the EVM, leading to further message passing or ether transactions
  - the instructions that make up smart contracts are stored in EVM bytecode
  - before they are compiled into bytecode, they are written by a human, in the Solidity programming language (next chapter)_

-----

# 4 - Solidity Programming
how to build things
  - develop contracts that compile to EVM bytecode
    - edge out serpent
    -LLL (lisp)
    - Mutan(deprecated)
  - Enables you to move tokens of value in any ethereum based system
  - Private groups altered, re-released, and deployed the source code (Ch11)


Smart contracts are distinct from distributed applications or dapps, even though both are distributed and application-like. A dapp is a GUI application that uses Ethereum smart contracts on the back end, in lieu of a conventional database and web application hosting provider. Dapps may be accessed through the Mist browser, or over the web.

TESTING:
The Ethereum network comes with a testnet called Ropsten: sandbox-like environment. Separate chain, just like in Chapter 8.


  We've only touched briefly on the formal mathematics that make these programs so exciting for enterprise IT. But with any luck, you've seen enough to motivate you to dig deeper into the Ethereum White Paper and Yellow Paper and see for yourself how the EVM reaches provable consensus.

CH5: deploy first token contract on EVM.
Social and cultural history of monetary instruments, and what it means for your understanding of the potential of Ethereum.
-----

# 5 - Smart Contracts and Tokens
- Smart contracts are reusable classes...bid system, section bid system, polling system...
  - Secure IM system...
  ???

-----

# 6 - Mining Ether
  - understand how mining works, so you can point your rigs at new cryptocurrencies in the future

-----

# 7 - Cryptoeconomics Survey
- hashing vs encryption
- we need to defend our public networks from attackers...

-----
 
# 8 - Dapp Deployment
  - running blockchain based applications >>> managing clients in a cloud-hosted paradigm

  - hub-and-spoke webapps scale vertically, reflecting the load of a sever
    - ETH apps scale horizontally...

  -components of the protocol will mature, things are limited now but will get faster

Prototyping Areas:
  - accounting system for something in the real world, or for other contracts
  - create forwarding contracts, such as a savings account that resends income to a separate bucket automatically
  - manage a relationship between several parties, such as freelancer agreement or payroll
  - act as a software library for other contracts
  - act as controllers for other systems or sets of contracts
  -serve as application-speciifc logic for a communal web service
  -serve as a utility that developers can use on a single-serving basis, such as a random number generator

-----

# 9 - Creating Private Chains
  - they have merit as learning tools
  - may have uses for large corps, identity, etc

  - Why blockchains are not better for all dbs and networks


  - Trustworthy chains: lots of proof of work.

  - creating your blockchain genesis file...

-----

# 10 - Use Cases*****

- Generalist learning, what you make with different chains...

------

# 11 - Advanced Concepts***
  - Private groups altered, re-released, and deployed the source code (Ch11)

  FULL ETHEREUM ROADMAP:
    - Frontier - 2015

    - Homestead - 2016

    - Metropolis - 2017
      - Mist will look like a cross between ChromeOS and iOS app store

    - Serenity - 2018
      - proof of stake algorithm
      - confidence a breakthrough is near

  #Future:
    - Ronald coase - economist - "firms exist to avoid the 'transaction costs' of going to the market every day lookin for workers.."
    - firms create long-term employement agreements that increase efficiency
    - processes that increase efficiency among a group of a few dozen workers can become a hindrance at scale...making large firms slow and uncompetitive
    - Equilibrium point: minimal bureaucracy, maximum efficients....
    - Temporary workers enable companies to spin up teams quickly when demand arises, spin them back down without needing to lay off FTE.

    "When comp packages can easily be composed of a series of if-then statements in a smart contract, the distinction between a salary and a bonus become blurred. The size, age, or location of a company may no longer carry cultural connotations about its trustworthiness or importance."
    - "THe boundaries of the modern company are becoming more permeable"

A paradigm shift may be in store: first, a period of flux as individuals and business come to grips with their freedom to engage in business agreements -> deals inked on pen and paper, but smaller deals handled by Eth machines running on boilerplate policies.

- No notaries.
- No HR sign-off.
- How many years out is this?

How many business agreements might be made more fair and enforaceable?
-----
# 11+ - Backmatter*?
------XXX
------
# (ROLLING) TODOs:
  - eth.guide
  - Review etherium roadmap.

VB - Proof of stake design philosophy:
https://medium.com/@VitalikButerin/a-proof-of-stake-design-philosophy-506585978d51#.7n3x85gvs
- Address typo: Main PAge of ch8.

-----

