
Prep Notes:
- AA seems like a bit of a tool.
- 


1. Introduction


------


2.  How Bitcoin Works
- Uses, Users, Stories

Low Value Retail
High Value Retail
Offshore contract services
Charitable Donations
Import/Export
Mining for Bitcoin


Transactions:
  - Types:
    - Common
    - Aggregating (exchange)
    - Distributing (payroll)
  - How it's added to the blockchain
  - How is it mined/propagated
------



3. The Bitcoin Client *
- Bitcoin Core:
  - old
  - not that important now
  - needs the whole blockchain

- bx - bitcoin explorer
  - encoding and decoding addresses
  - base16, base58, base58Check, base64

- Go ecosystem:
  - btcd
  - btcwallet
  - btcgui

------



4. Keys, Addresses, Wallets **
- elliptic curve multiplication is the basis of BTC's public key cryptography
  - explained with math to generate a public key
- Paper wallets, passphrase protection

------



5. Transactions **
(Technical++)
- Propagation
- Inputs, Fees, UTXO
  - unspent transaction outputs
- Script is turing incomplete
- Multisig transactions
- pay-to-script-hash

------

6. The Bitcoin Network ***
(Technical++)
"Node Role Types"
  Full Node
  SPV
  Tourist Analogy
  Peer to Peer architecture, diagrams.
  - network discovery

Bloom Filters, "Inventory"
  - Transaction Pools
  - Alert Messages?


  



------



7. The BlockChain ***
(Technical+++)
How blocks work, structure of a a block
- Genesis Block

Merkle Tree
Merkle Path
Simplified Payment Verification




------



8. Mining and Consensus ***
(Technical, Accessible)
Mining is the process by which the decentralized clearinghouse runs, by which transactions are validated and cleared.

Mining secures the bitcoin system and enables the emergence of network-wide consensus without a central authority.

Deflationary Money: not the greatest argument against hoarding instinct being problematic.

Fork Event: blue-green-pink analogy

Hashing Race: 
  2009
  2010
  2011
  2012 - 9 TH/sec
  2013 - 23TH/sec
  2014 - 10PH/sec


Consensus Attacks:
  - Consensus attacks do not affect the security of private keys and signing algorithm.
  - Cannot steal bitcoins, spend bitcoins without signatures, redirect bitcoins, or otherwise changep ast transactions or ownership records.
  - A consensus attack can only affec the most recent blocks and cause denial of service distruptions on the creation of future blocks.

Much less than 51% is needed.
  - 51% threshold is simply the level at which such an attack is almost guaranteed to succeed.
  - A consensus attack is essentially a tug of war for the next block..


------



9. Alternative Chains, Currencies, and Applications *

altcoin
metacount
countryparty - protocol layer on top of BTC
- alt coins:
   - namecoin: decentralized key-value registration and transfer platform using a blockchain

- evaluating an alt coin:
  - significant innovation?
  - compelling value prop? Attract users away from BTC?
  - niche  market or application?
  - attract enough minors to be secured against consensus attacks?

- total market cap of coin?
- how many estimated users/wallets does the alt coin have?
- how many merchants accept the alt coin?
- daily transaction volume?
- how much transaction VALUE daily?


Freicoin: demurrange currency.
  - Encourage spending.
  - 4.5% interest rate for stored value.

 Annonymity: 
  - CryptoNote -> Monero

- The future of cryptographic curerncies overall is brighter than the future of bitcoin.
- Will affect broad sectors of the economy, from distributed systems science to finance, economics, currencies, central banking, and corporate governance.
- Many human activities that previously required centralized institutions or organizations to function as authorative or trusted points of control can now be decentralized.
- The invention of the blockchain and consensus system will significantly reduce the cost of organization and coordination on large-scale systems, while removing opporutinites for concentration of power, corruption, and regulatory capture.


------



10. Bitcoin Security **

Best Practices:
  - Multiple Wallets
  - Multi-sig wallets
  - Survivability: death/executor



------



10A) Transaction Script Language Operators.
  - for pushing values onto stack, conditional control flow, string ops, binary math ops, numeric ops, cryptographic funciton ops, nonops symbols,

10B) Bitcoin Improvement Proposals
  https://medium.com/@jacob.eliosoff/bip148-0-down-51-to-go-5540b38f1a49

BIP148 - What's next?


BIP0001 BIP - Purpose and Guidelines
https://github.com/bitcoin/bips/blob/master/bip-0001.mediawiki
  - accepted
  - rejected
  - deferred



Segwit deployment:
https://github.com/sdtsui/bips/blob/master/bip-0148.mediawiki


- Understanding the most technical portions of this book will generate technical wealth. 
- Add to bedtime reading.

Three Kinds of BIP:
  - Standard: change to network protocol, block/transaction validity rules, or any change that affects the interop of applications using BTC
  - Informational: design issue, guidelines, information. Do not necessarily represent a bitcoin community consensus or recommendation
  - Process: describes a process, or proposes a change to (or an event in) process
    - applies outside of BTC protocol, implemention, not to btc's codebase.
      - procedures, guidelines, changes to decision-making process, changes to tools or env used in BTC development.
      - "Meta-BIP" == process BIP.

  pycoin - python based library that supports manipulation of BTC keys and transactions, supporting the scripting langugage enough to properly deal with nonstandard transactions.
https://github.com/richardkiss/pycoin


https://github.com/richardkiss/pycoin/blob/master/COMMAND-LINE-TOOLS.md
  ku - key util, for manipulating keys

  bx - 


10 C. pycoin, ku, tx

10 D. Bitcoin Explorer (bx) Commands

https://blockexplorer.com/


Notes: aug1st.
https://medium.com/@jacob.eliosoff/bip148-0-down-51-to-go-5540b38f1a49
------


Index


------



Colophon/Copyright

