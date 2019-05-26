
In the wide sense, one can use the definition from English wikipedia: A smart contract is a computer protocol intended to digitally facilitate, verify, or enforce the negotiation or performance of a contract. 

The main variety are the smart contracts in the context of the distributed ledger technology and [[blockchain]] in particular.

The smart contract on the blockchain typically consists of a code written for the blockchain-supported virtual machine. In the dominant scenario, the miners are the only parties which strictly execute the smart contract code. The main function of the code is handling assets in a deterministic way, e.g. cryptocurrencies or other tokens, as well as triggering or controlling the operations on off-chain assets (the latter being harder to enforce). Part of the true content of the smart contract is however off-chain. Various software and other agents verify the milestones happening off-chain or trigger changes in off-chain state. Sometimes an external legal action may be necessary, thus some smart contracts contain legal prose which explains both the code contained in the manner understandable to legal system as well as various contract externalities.  

### Blockchain virtual machine and supported languages

In most reincarnations the virtual machine supports a Turing complete language.
In practice, there are limits on the level of complexity of the code and computer resources it may require, and the spending of resources is controlled by cryptoassets ("gas") held by the smart contract viewed as an account on blockchain. The efficiency is important because the same code has to be executed/verified by virtually all nodes in the blockchain protocol.
 
Regarding that the smart contracts on blockchain by their nature are likely to often handle additional cryptographic steps, and 256-bit hashes are common in use most blockchain virtual machines (Ethereum Virtual Machine (EVM), TON Virtual Machine etc.). This is elegant but nonefficient, as 256-byte register is expensive for too small operations and does not map directly to most machines. Thus some machines pack several "bytecode" operations into a very long instruction word. Substrate project (and there are some plans by Ethereum community to go the same way) rather implements WebAssembly (Wasm) bytecode which is very efficient and the same code is used on non-blockchain platforms (emerging browser for efficient common virtual machine of web browsers!), what gives access to quality compiler, debugger and other development tools. Ethereum community plan to establish a WebAssembly virtual machine on Ethereum in future (eWasm, for Ethereum Wasm).

In all case above, higher level languages are used, which compile to the blockchain virtual machine language. For example, Solidity (introduced by Gavin Wood in Aug 2014) is the common choice for a higher language on Ethereum blockchain, and compiles to EVM bytecode. Solidity is specially designed for blockchain use. Its design (which is intended to be Javascript-like, with some influence of C and Python; with later specific improvements/versions) is not considered very successful. Some later languages include (Python-like) Serpent and Viper. For WebAssembly,
there are now compilers from C, C++, Rust, Lua, while the compiler for GoLang is in the development. Substrate blockchain project is itself mainly written in [[Rust]], which is a relatively low level language designed for clarity and security, what makes it suitable for critical applications like blockchain. Moreover both WebAssembly is a quite well performing language, and Rust creates rather small runtime and has no need for garbage collection, the features which make them very suitable for resource expensive blockchain execution.

[Tezos](https://tezos.com) uses OCaml (a functional language). A major functional language on Cardano is [plutus](https://cardanodocs.com/technical/plutus/introduction), Haskell like functional language with eager rather than laisy execution. 

[Accordproject](https://www.accordproject.org) develops open source framework to generate the blockchain smart contracts from source which is closer to the working needs of legal teams and is accompanied with careful creation protocols and sufficient legal prose to make the off-chain effects legally enforceable. 

[[zoranskoda:Hyperledger]] Fabric supports smart contracts in Go programming language and in Javascript. Hyperledger Sawtooth allows adding new language frameworks and it included [[Rust]] in December 2018.

"[Scilla](https://scilla-lang.org), short for Smart Contract Intermediate-Level Language, is an intermediate-level smart contract language being developed for Zilliqa. Scilla has been designed as a principled language with smart contract safety in mind"..."developed hand-in-hand with formalization of its semantics and its embedding into the [[nLab:Coq]] proof assistant."

[[Nikolai Durov]] has recently designed a Forth-like stack based efficient language Fift for low level access and debugging to [[TON]] VM.

### Literature

* wikipedia [smart contract](https://en.wikipedia.org/wiki/Smart_contract)

A much longer list of references is at [[zoranskoda:smart contract]] (at zoranskoda).

Related pages at $n$Lab include [[distributed computing]], [[arithmetic cryptography]]

The idea of a smart contract is from

* N. Szabo,The idea of smart contracts, 1997 [html](http://szabo.best.vwh.net/idea.html)

and a full-fledged [[blockchain]] implementation started with the Ethereum blockchain.

* [[Vitalik Buterin]], _Ethereum: A next-generation smart contract and decentralized application platform_, [pdf](https://github.com/ethereum/wiki/wiki/White-Paper.pdf)



category: computer science, applications

[[!redirects smart contracts]]