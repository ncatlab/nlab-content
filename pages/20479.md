
__Ethereum__ is a public [[blockchain]] which is established as a sequel to [[bitcoin]] with intention to include [[smart contract]]s and distributed applications as envisioned by [[Vitalik Buterin]] in 2013. This platform is considered as the main platform of blockchain 2.0 stage in blockchain technology development; as of 2019 it still uses proof of work. 
As of 2019, Ethereum mainnet, which supports the Ether cryptocurrency is still officially beta and many improvements in 2019 and 2020 are planned, called Ethereum 1.x, including replacing the present Ethereum virtual machine (EVM) with ewasm virtual machine for [[WebAssembly]] bytecode. Somewhere in 2020 or 2021, a new release of Ethereum based on proof of stake with sharding and many other improvements (including a rent for smart contracts) is planned to be created; the new platform is called Ethereum 2.0 and will qualify for 3rd generation blockchain platform in terms of scalability and speed, and possibly some level of interoperability. Migration of users from the Ethereum 1.x beta chain will be performed via smart contracting, without hard forks. The old net is likely to stay as a read only record of old history and be attached to the new net as a shardchain. The implementations of Ethereum 2.0 are being coded simultaneously by 9 different teams in several different programming languages. 

Ethereum 1.0 platform has largely influenced development of many subsequent platforms; in particular, [[zoranskoda:Hyperledger]] Fabric is a permissioned blockchain  developed by IBM and Linux Foundation on the basis of Ethereum.

Most important clients for Ethereum are (see also [here](https://github.com/ethereumbook/ethereumbook/blob/develop/03clients.asciidoc))

* Metamask  (Chrome extension) [metamask.io](https://metamask.io); source at [github](https://github.com/MetaMask/metamask-plugin)
* Mist browser (web3.js based browser for DApps) is now [deprecated](https://medium.com/@avsa/sunsetting-mist-da21c8e943d2); [github](https://github.com/ethereum/mist), [investopedia](https://www.investopedia.com/terms/m/mist-browser.asp)
* parity (node software written in [[Rust]]) [setup](https://wiki.parity.io/Setup)
* Geth (Go Ethereum, node software written in GoLang)

See also about setting your own private Ethereum net in {this tutorial](https://www.edureka.co/blog/ethereum-private-network-tutorial). A comprehensive book on Ethereum is  


* Andreas M. Antonopoulos, Gavin Wood, _Mastering Ethereum: building smart contracts and DApps_, O’Reilly Media, 2018. The book is also on [github](https://github.com/ethereumbook/ethereumbook) together with the sourcecode

## Literature

See also [[blockchain]], [[smart contract]] and wikipedia article [Ethereum](https://en.wikipedia.org/wiki/Ethereum).

Official page [ethereum.org](https://www.ethereum.org) and [developer resources](https://www.ethereum.org/developers) there.

### General

*  V. Buterin, _Ethereum in 25 minutes_, [youtube](https://www.youtube.com/watch?v=66SaEDzlmP4); _Blockchain and Ethereum security on the higher level_, [youtube](https://www.youtube.com/watch?v=UFDAtStVXbc) 1:21h
* [[Vitalik Buterin]], Ethereum: A next-generation smart contract and decentralized application platform, [pdf](https://github.com/ethereum/wiki/wiki/White-Paper.pdf)
* Gavin Wood, _Ethereum: a secure decentralised generalised transaction
ledger_, Ethereum, Tech. Rep. 2017. [pdf](https://ethereum.github.io/yellowpaper/paper.pdf)
* [parity](https://www.parity.io) blockchain infrastructure for the decentralised web 
* [Enterprise Ethereum Alliance](https://entethalliance.org)

Plans for Ethereum future from Ethereum Foundation as of May 2019:

* [blog.ethereum.org/2019/05/21/ethereum-foundation-spring-2019-update](https://blog.ethereum.org/2019/05/21/ethereum-foundation-spring-2019-update)
* A journey through phase 2 of Ethereum 2.0 [medium](https://medium.com/@william.j.villanueva/a-journey-through-phase-2-of-ethereum-2-0-c7a2397a36cb)
* Phase 2 proposal 1 [hackmd](https://notes.ethereum.org/s/HylpjAWsE#)
* V. Buterin, [A layer-1-minimizing phase 2 state execution proposal](https://ethresear.ch/t/a-layer-1-minimizing-phase-2-state-execution-proposal/5397/4), [Proposed further simplifications/abstraction for phase 2](https://ethresear.ch/t/proposed-further-simplifications-abstraction-for-phase-2/5445)

### Protocol improvements
 
* Vlad Zamfir, Nate Rush, Aditya Asgaonkar, Georgios Piliouras, _Introducing the “Minimal CBC Casper” family of consensus protocols_, [pdf](https://github.com/cbc-casper/cbc-casper-paper/blob/master/cbc-casper-paper-draft.pdf)
* [how ethereum works](https://www.coindesk.com/information/how-ethereum-works)
* Andrew Ashikhmin, Alexey Akhunov, _Red queen's sync protocol for Ethereum_, github/[pdf](https://github.com/yperbasis/silkworm/raw/master/doc/sync_protocol_v1.pdf)
* [cointelegraph.com/news/an-ethereum-20-proof-of-stake-testnet-blockchain-is-now-live](https://cointelegraph.com/news/an-ethereum-20-proof-of-stake-testnet-blockchain-is-now-live)

### Whisper

According to Mukhapadhyay, _Ethereum smart contract development_

> When [[Gavin Wood]] laid down the specifications for whisper as a peer-to-peer communication protocol, in his whitepaper on [GitHub](https://github.com/ethereum/wiki/wiki/Whisper-PoC-2-Protocol-Spec), he designed one of the most interesting technologies in the field of cryptography. At a considerable cost of bandwidth and latency, whisper is able to deliver a 100% dark operation. By completely dark operations, we mean that there is zero leakage of metadata during peer-to-peer By technical definition, whisper is a messaging system with multi distributed hash table (DHT), with routing privacy acting as a
companion protocol to the Ethereum blockchain. 

> Whisper operates in a user-configurable manner with regard to how much information the communicating nodes are willing to leak concerning the decentralized application content that ultimately tracks the user activities. 

> Whisper is based on two key concepts: messages and envelopes. If whisper is considered a datagram messaging service, then an envelope represents an un-encrypted data format, comprehensible by a node, which carries the encrypted message datagram inside it. An envelope consists of original time to live (TTL, in seconds), the absolute time to expiry (UNIX system time), the encrypted message data field, which is the actual payload, topics (cryptographically secure, probabilistic partial classifications of message), and nonce, an arbitrary value. This nonce is used for the PoW to judge the efforts of a peer. The message has a binary flag for signature with an unfixed payload.

### Ethereum virtual machine, storage and smart contracting

* EVM [storage layout](https://medium.com/@hayeah/diving-into-the-ethereum-vm-part-2-storage-layout-bc5349cb11b7)
* [2018/03/09/understanding-ethereum-smart-contract-storage](https://programtheblockchain.com/posts/2018/03/09/understanding-ethereum-smart-contract-storage)
* solidity [docs](https://solidity.readthedocs.io)
* solidity "guide", [bitdegree](https://www.bitdegree.org/learn/solidity)
* [stm](https://abhiroop.github.io/BlockChain-STM), [smart contract misconceptions](https://www.coindesk.com/three-smart-contract-misconceptions), [more storage](https://applicature.com/blog/blockchain-technology/ethereum-smart-contract-storage), [contract call at later time](https://ethereum.stackexchange.com/questions/42/how-can-a-contract-run-itself-at-a-later-time), Where do smart contracts reside in blockchain [stackoverflow](https://stackoverflow.com/questions/42081194/where-do-smart-contracts-reside-in-blockchain-ethereum-or-hyperledger), [chronos](https://www.stateofthedapps.com/dapps/chronos)
* [viper](https://ethereumclassic.github.io/blog/2017-03-13-viper)
* A. Unterweger et al. _Lessons learned from implementing a privacy-preserving
smart contract in Ethereum”_, 2018 9th IFIP Intern. Conf. on
New Technologies, Mobility and Security (NTMS) Feb. 2018, pp. 1–5
[doi](https://doi.org/10.1109/NTMS.2018.8328739)
* Ethereum Alarm Clock [documentation](http://docs.ethereum-alarm-clock.com/en/latest)
* _How can a contract run itself at a later time?_, [
ethereum.stackexchange](https://ethereum.stackexchange.com/questions/42/how-can-a-contract-run-itself-at-a-later-time)
* how-data-is-stored-in-ethereum [hackernoon](https://hackernoon.com/getting-deep-into-ethereum-how-data-is-stored-in-ethereum-e3f669d96033)

### Others

Vitalik proposed a privacy mixer for Ethereum to enhance anonymity via groupings

* _Minimal mixer design_, proposal at [hackmd](https://hackmd.io/s/rJj9hEJTN); [news at coindesk](https://www.coindesk.com/vitalik-roposes-mixer-to-anonymize-one-off-transactions-on-ethereum)