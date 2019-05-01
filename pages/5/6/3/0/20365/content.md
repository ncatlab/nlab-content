Bitcoin with only about 8 transaction per second (TPS) and also big latency times (for final confirmations) is not very suitable for most [[blockchain]] applications. Similarly with most early generation distributed ledgers. Important things for performance include also the efficiency of [[virtual machine]] employed (trend is that the newest projects go toward versions of [[WebAssembly]] VM).

Faster and even scalable solutions are now in works. 
We first describe improvements on Bitcoin and Ethernet 
networks in the form of lightning and plasma networks on top of those, and then various projects which claim to be scalable, "3rd generation" etc. Essential improvements are various algorithms trying to go beyond linearity of classical blockchain projects, especially those relying on DAGs (directed acyclic graphs) and on so called sharding. As far as consensus algorithms there are scalability improvements with many new algorithms, while PoW is in a way most secure (for public blockchains). 

### Lightning network

Bitcoin solves some of the problems with   so called lightning network on top of it, which makes temporary transactions with lots of intermediate transfers only off chain and only small footprint on the main chain, ensuring small price of transactions. 

* [lightning.network](https://lightning.network)
* Joseph Poon, Tadge Dryja, _Lightning Network_, [pdf](https://lightning.network/
lightning-network-paper.pdf) Mar 2015.
* A van Wirdum _Understanding the lightning network [1](https://bitcoinmagazine.com/articles/understanding-the-lightning-network-part-building-a-bidirectional-payment-channel-1464710791) [2](https://bitcoinmagazine.com/articles/understanding-the-lightning-network-part-creating-the-network-1465326903)
* Amazon using lightning network for e-commerce, April 2019
[news](https://www.coindesk.com/you-can-now-shop-with-bitcoin-on-amazon-using-lightning)

### Ethernet improvements and plasma 

Ethernet recognizes the same problem as Bitcoin, but has significant plans of substantial upgrades of its Mainnet, namely the new Casper protocol, plans for deployment of [[WebAssembly]] virtual machine and sharding which, according to Buterin, could together bring million TPS when all employed as planned. 

In addition, there is an analogue algorithm to lightning network targeted to Ethereum, with substantial new ideas in the algorithm, called plasma network. 

* Joseph Poon, Vitalik Buterin, _Plasma: scalable autonomous smart contracts_
[pdf](https://www.plasma.io/plasma.pdf) draft whitepaper

There are several realizations of plasma, mostly used being the Loom network.

### Projects based on DAGs

There are several major algorithms. Several projects are based on "hashgraph" paper

* Leemon Baird, _The Swirlds hashgraph consensus algorithm: fair, fast, byzantine fault tolerance_, [pdf](https://www.swirlds.com/downloads/SWIRLDS-TR-2016-01.pdf) (May 2016); _Hashgraph consensus: detailed examples_ [pdf](https://www.swirlds.com/downloads/SWIRLDS-TR-2016-02.pdf); _Overview of Swirlds Hashgraph: An Introduction To The Hashgraph (SDK Available Now)_ [online](https://steemit.com/technology/@swirlds/overview-of-swirlds-hashgraph-an-introduction-to-the-hashgraph-sdk-available-now)

including [Hedera](https://www.hedera.com/whitepaper) which claims 50000 to 500000 TPS tested,

* Hedera Hashgraph whitepaper [pdf](https://www.hedera.com/hh-whitepaper-v1.5-190219.pdf); intro to whitepaper [web](https://www.hedera.com/whitepaper); 

then so called Consensus project etc.

Somewhat similar but with a new innovative algorithm is [Tolar Hashnet](https://www.tolar.io), see whitepaper [pdf](https://www.tolar.io/static/media/Whitepaper-Tolar.2f13a40e.pdf) with around 150000 TPS achieved on testnet and low power consumption. 

Another kind of scalable algorithms using DAGs is the tangle blockchain (of the [iota](https://www.iota.org) project)

* Serguei Popov, _The tangle_ [pdf](https://www.iotatoken.com/IOTA_Whitepaper.pdf), 2016


### Telegram Open Network

[Telegram](https://telegram.org) (see [FAQ](https://telegram.org/faq) and [wikipedia](https://en.wikipedia.org/wiki/Telegram_(messaging_service)) is developing Telegram Open Network (TON) centered around a new generation blockchain project. Besides the blockchain and user interfaces, including on Telegram, it will contain analogues of other parts of the internet structure including TON proxy, TON DNS and TON storage. The blockchain uses delegated proof of stake with a number of innovations including infinite sharding paradigm and instant hypercube rooting. The whitepaper predicts that the platform will be able to support millions of TPS (private access to testnet allegedly given in April 2019). For more details see [[Telegram Open Network]] in this wiki and original

* TON whitepaper, 23 page [pdf](https://cdn.crowdfundinsider.com/wp-content/uploads/2018/03/TON-White-Paper-Telegram-ICO.pdf), mirrors [pdf](https://drive.google.com/file/d/1ucUeKg_NiR8RxNAonb8Q55jZha03WC0O/view) [pdf](https://icorating.com/upload/whitepaper/gNQ7e9z3lCGi519Wz8mmC0Kg8aA0goeZKAQ802vo.pdf)
* [[nlab:Nikolai Durov]]'s 132-page technical overview _Telegram Open Network_, Dec 2017 [pdf](https://toncoin.tech/TON-official-whitepaper.pdf), mirror [pdf](https://www.kriptovaluta.hr/wp-content/uploads/2018/03/TON-Technology.pdf); _Telegram Open Network Blockchain_, Sep 2018, 121 pp. [pdf](https://www.docdroid.net/qY4sQEv/telegram-open-network-blockchain-september-5-2018.pdf); _Telegram Open Network Virtual Machine_, Sep. 2018, 148 pp. [pdf](https://www.docdroid.net/R3vEKBY/telegram-open-network-virtual-machine-september-5-2018.pdf)

### RedBelly

Australian academic [RedBelly](https://redbellyblockchain.io) blockchain (also referred as CSIRO) has confirmed 40000 TPS with Amazon platform worldwide testing. Since mid 2017 it had local tests which could achieve up to 400000 but with all nodes in the same location; see the paper about various performance experiments (the largest performance experiment, with measuring various parameters, with up to 1000 nodes in 10 countries!), 

* Concurrent Systems Research Group, University of Sydney, Data61-CSIRO, _The Red Belly Blockchain Experiments_, [pdf](https://redbellyblockchain.io/papers/redbellyblockchain-experiments.pdf) 

and selection of [news](https://redbellyblockchain.io/Press.html). The academic group behind the projects has also a number of interesting [research papers](https://redbellyblockchain.io/Research.html).

### MIT Vault

* Derek Leung, Adam Suhl, Yossi Gilad, Nickolai Zeldovich (MIT CSAIL), _Vault: fast bootstrapping for cryptocurrencies_, Jan 2019, preprint [pdf](http://people.csail.mit.edu/nickolai/papers/leung-vault-eprint.pdf)
* [news.mit.edu:faster-more-efficient-cryptocurrency](https://news.mit.edu/2019/vault-faster-more-efficient-cryptocurrency-0124)


### Other projects which claim to be very fast or scalable

* [bitconch](https://bitconch.io) claims 120000 TPS
* [Futurepia](https://futurepia.io) uses Double Delegated Proof of Stake. "KOLAS (Korea Laboratory Accreditation Scheme) has assessed and certified FUTUREPIA’s Social Media Mainnet transaction speed as 300,000 TPS".
* [[EOS]] is a high performance blockchain using [[WebAssembly]] [[virtual machine]] for [[smart contract]]s. [eos.io](https://eos.io) claims speeds up to 300000 TPS.  [eos.io](https://eos.io) claims speeds up to 300000 TPS. EOS technical white paper v2 (March 2018) is at github, [md](https://github.com/EOSIO/Documentation/blob/master/TechnicalWhitePaper.md). 
* NEO "smart economy" [neo.org](http://neo.org) claims 1000-10000 TPS with plans to go to 100000 in 2020
* Ripple [XRP](https://ripple.com/xrp) blockchain has over 1700 TPS in regular usage. They claim to test speeds up to 50000

There is a theoretical proposal to scale up by 3 
orders of magnitude by the BlockReduce algorithm "which only segments consistency". The paper shortly reflects on other approaches

* K. J. Kreder III, _BlockReduce: scaling blockchain to human commerce_, [arxiv/1811.00125](https://arxiv.org/abs/1811.00125)

[[!redirects high performance DL]]
[[!redirects high performance blockchain]]
[[!redirects high performance DLs]]