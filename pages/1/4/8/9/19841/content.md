\tableofcontents

\section{Introduction}

The notion of a _blockchain_, originating with Wei Dai, 1996 ([web](http://www.weidai.com/bmoney.txt), wikipedia [B-money](https://en.bitcoin.it/wiki/B-money)) and [(Nakamoto2008)](#NakamotoBitcoinAPeerToPeerElectronicCashSystem), allows for the creation of a linear log which can be added to, but is extremely difficult to otherwise modify, in a [[undirected graph|network]] with multiple nodes, without any central authority.

Blockchain can be considered as certain data structure -- chain of blocks -- which are cryptographically "sealed" by hashes which are for each block added to the next block and which is incremented by one of many parties called nodes
which follow a commonly accepted algorithm and each contains a copy of the blockchain (full node) or its essential part. Who adds a block, or whose added block is respected by other nodes is a part of the algorithm (blockchain protocol) and is desirable to be byzantine fault tolerant. The securest algorithm in nontrusted environment (public blockchain) is the proof of work algorithm. Regarding that blockchain is a tool to establish noncentralized record verification it is common to use blockchains to carry records of assets, including cryptocurrencies and other token, off chain assets, credential records, verification proofs and so on. These data and transaction steps belong and are authorized by accounts. Modern blockchain protocols
assume also that code handling assets in deterministic manner may be part of the account, when the nodes add new blocks they should also execute the code of the contract, within a blockchain virtual machine; such accounts are called [[smart contract]]s and realize in a specific way the idea of smart contracts outlined in theoretical computer science before the blockchain era. 

The phrase _distributed ledger_ is sometimes viewed as a synonym. Technically,
distributed ledger is the same idea realized in a more general setup where the record may be organized in non-linear structure, for example when the blocks form a DAG (directed acyclic graph) rather than a single chain, with appropriate protocol. 

\section{Proof of work}

The key idea is that of _proof of work_. Think of a blockchain simply as a [[list]] $[ B_{1}, B_{2}, \ldots ]$ of 'blocks'. A _block_ $B$ is an _unencrypted block_ of content, which could be anything, together with a _cryptographic hash_ of it ('signature') with certain properties.

The key points are the following.

1. The cryptographic hash with the required properties is hard to create, where 'hard' means requiring significant computational resources and taking time (e.g. something like [[prime]] factorisation). Use of these computational resources to create the hash is referred to as 'proof of work'.

1. The hash of $B_{i+1}$ depends on the hash of $B_{i}$. 

1. The hash of a block depends exactly on its contents: any change in contents will lead to a significantly different hash.

1. It is easy (requires little resources and time) to check that a particular hash has the required properties. 

Suppose that we have $n$ nodes in a network. Each node accepts as the current blockchain the longest valid blockchain which it knows of. If a node $X$ adds a block $B$ to a blockchain $L = [ B_1, \ldots, B_m ]$, i.e. succeeds in a creating a hash of some unencrypted block of content, it sends $L' = [B_1, \ldots, B_m, B]$ out to all nodes listening to/connected to it. If longest blockchain $L''$ which a node $Y$ knows of has length $m$, then upon receiving $L'$ it drops any attempts it is currently making to add a block to $L''$, checks the validity of $L'$, and if it is valid accepts it as the current blockchain.

In such a system, it is extremely difficult for any node to tamper with the  blockchain. This is because if it wishes to change the content of a particular block, then because of 2. and 3. it must not only re-create the hash of the tampered block, but also the hash of all blocks after it, as well as the hash of a new block. If any honest node creates the hash of just one new block in the meantime and sends it out to the network, the tampering attempt now has still another block to hash. Because of the computational resources required to create even one valid hash, it is thus highly unlikely that tampering will succeed, and thus a tamperer may soon use up great amounts of resources for no gain. If successful adding of blocks is incentivised appropriately, it is thus more sensible to act honestly.

There are various further details, but this is the rough idea.

\section{Criticisms}

While in its way ingenious, the use of proof of work underlying the notion of a blockchain is rather crude. Enormous amounts of electricity, for example, are [being consumed](https://digiconomist.net/bitcoin-energy-consumption) by large blockchain networks such as bitcoin during proof of work, whilst the outcome of that proof of work is typically useless. This is not sustainable. 

A different criticism regards the algorithm itself. If nodes were to co-operate in such a way that they controlled over 50% of the computational power on the network, a tampering attempt would eventually be able to 'catch up' with the honest additions to the blockchain. 

\section{References}

* this wiki: [[smart contract]], [[Ethereum]], [[computer science]], [[high performance distributed ledger]], [[Telegram Open Network]], [[virtual machine]]

* {#NakamotoBitcoinAPeerToPeerElectronicCashSystem} Satoshi Nakamoto, _Bitcoin: A peer-to-peer electronic cash system_, 2008 [pdf](https://bitcoin.org/bitcoin.pdf) 

A foundational/mathematical introductory book from the point of view of (building) a distributed computing system is

* Roger Wattenhofer, _The science of the blockchain_, 115 pp. Inverted Forest Publishing 2016

A comprehensive guide for architects of blockchain applications with an attempt at certain level of abstraction of central concepts is

* Xiwei Xu, Ingo Weber, Mark Staples, _Architecture for blockchain applications_, Springer 2019

The following systematic book written by a several authors offers pretty rigorous handbook on blockchain security issues

* Sachin S. Shetty, Charles A. Kamhoua, Laurent L. Njilla (eds.) _Blockchain for distributed systems security_, 324 pp. IEEE Press, SMTE Books 2019

See also:

* [[Melanie Swan]], [[Renato P dos Santos]], [[Frank Witte]], Between Science and Economics, Volume 2: *Quantum Computing Physics, Blockchains, and Deep Learning Smart Networks*, World Scientific 2020 ([doi:10.1142/q0243](https://doi.org/10.1142/q0243))


Some key papers in [[zoranskoda:distributed consensus]] include

* M. J. Fischer, N. Lynch, M. S. Paterson, _Impossibility of distributed con-
sensus with one faulty process_, JACM 32:2, 374-382 (1985)
* M. Castro, B. Liskov, et al., _Practical byzantine fault tolerance_, Proc. 3rd
Symposium on Operating Systems Design and Implementation (1999) 173–186.
* L. Lamport, R. Shostak, M. Pease, _The byzantine generals problem_, ACM
Transactions on Programming Languages and Systems, 4/3 (1982), p. 382–401.

Other references on distributed ledgers

* [[Vitalik Buterin]], _Ethereum: A next-generation smart contract and decentralized application platform_, [pdf](https://github.com/ethereum/wiki/wiki/White-Paper.pdf)
* Gavin Wood, _Ethereum: a secure decentralised generalised transaction
ledger_, Ethereum, Tech. Rep. 2017
* Gavin Wood, _PolkaDot: vision for a heterogeneous multi-chain framework_ [pdf](https://github.com/w3f/polkadot-white-paper/raw/master/PolkaDotPaper.pdf)
* Joseph Poon, Vitalik Buterin, _Plasma: scalable autonomous smart contracts_,
[pdf](https://www.plasma.io/plasma.pdf)
* Joseph Poon, Tadge Dryja, _Lightning network_, [pdf](https://lightning.network/lightning-network-paper.pdf) Mar 2015.
* [[Vitalik Buterin]], _Chain interoperability_, R3 reports, Sep 2016 [pdf](https://www.r3.com/wp-content/uploads/2018/04/Chain_Interoperability_R3.pdf)
* Tier Nolan, _Re: Alt chains and atomic transfers_, 2013, bitcointalk discussion [post](https://bitcointalk.org/index.php?topic=193281.msg2224949#msg2224949)
* [[Nikolai Durov]], _Telegram Open Network_, 132 pp. Dec 2017 [pdf](https://toncoin.tech/TON-official-whitepaper.pdf), mirror [pdf](https://www.kriptovaluta.hr/wp-content/uploads/2018/03/TON-Technology.pdf); _Telegram Open Network Blockchain_, Sep 2018, 121 pp. [pdf](https://www.docdroid.net/qY4sQEv/telegram-open-network-blockchain-september-5-2018.pdf); _Telegram Open Network Virtual Machine_, Sep. 2018, 148 pp. [pdf](https://www.docdroid.net/R3vEKBY/telegram-open-network-virtual-machine-september-5-2018.pdf); _Fift: a brief introduction_ (about a new programming language on TON), May 23, 2019, 87 pp. pdf is at channel [t.me/Tgram/170](https://t.me/Tgram/170)
* L. Baird, _The Swirlds hashgraph consensus algorithm: fair, fast, byzantine fault tolerance_, [pdf](https://www.swirlds.com/downloads/SWIRLDS-TR-2016-01.pdf) (May 2016); _Hashgraph consensus: detailed examples_ [pdf](https://www.swirlds.com/downloads/SWIRLDS-TR-2016-02.pdf); _Overview of Swirlds Hashgraph: An Introduction To The Hashgraph (SDK Available Now)_ [online](https://steemit.com/technology/@swirlds/overview-of-swirlds-hashgraph-an-introduction-to-the-hashgraph-sdk-available-now); [Hedera](https://www.hedera.com/whitepaper) Hashgraph whitepaper [pdf](https://www.hedera.com/hh-whitepaper-v1.5-190219.pdf); intro to whitepaper [web](https://www.hedera.com/whitepaper)
* Aggelos Kiayias, Andrew Miller, Dionysis Zindros, _Non-interactive proofs of proof-of-work_, IACR preprint 2017 [pdf](https://eprint.iacr.org/2017/963.pdf) (see also [here](https://ambcrypto.com/pewdiepie-forays-into-cryptospace-by-partnering-with-dlive-a-blockchain-based-live-streaming-platform) and Cardano, IOHK)
* Mike Hearn, _Corda -- a distributed ledger_ (technical whitepaper, 2016) [pdf](https://docs.corda.net/_static/corda-technical-whitepaper.pdf); Brown et al. _Corda - an introduction_, whitepaper 2016, [pdf](https://docs.corda.net/_static/corda-introductory-whitepaper.pdf); Brown, _Corda - an introduction_ platform whitepaper 2018 [pdf](https://www.corda.net/content/corda-platform-whitepaper.pdf)
* Ittay Eyal, Emin Gün Sirer, _Majority is not enough: Bitcoin mining is vulnerable_, in: Financial Cryptography and Data Security 436–454, Springer 2014 [pdf](http://fc14.ifca.ai/papers/fc14_submission_82.pdf)

For an extended list of references see [[zoranskoda:blockchain]] (at zoranskoda). 

category: computer science, applications

[[!redirects blockchains]]

[[!redirects proof of work]]


