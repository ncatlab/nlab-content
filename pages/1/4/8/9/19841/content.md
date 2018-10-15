\tableofcontents

\section{Introduction}

The notion of a _blockchain_, originating with [(Nakomoto2008)](#NakomotoBitcoinAPeerToPeerElectronicCashSystem), allows for the creation of a linear log which can be added to, but is extremely difficult to otherwise modify, in a [[undirected graph|network]] with multiple nodes, without any central authority.

\section{Proof of work}

The key idea is that of _proof of work_. Think of a blockchain simply as a [[list]] $[ B_{1}, B_{2}, \ldots ]$ of 'blocks'. A _block_ $B$ is an _unencrypted block_ of content, which could be anything, together with a _cryptographic hash_ of it ('signature') with certain properties.

The key points are the following.

1. The cryptographic hash with the required properties is hard to create, where 'hard' means requiring significant computational resources and takes time (e.g. something like [[prime]] factorisation). Use of these computational resources to create the hash is referred to as 'proof of work'.

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

{#NakomotoBitcoinAPeerToPeerElectronicCashSystem} Satoshi Nakomoto, _Bitcoin: A peer-to-peer electronic cash system_, 2008 [pdf](https://bitcoin.org/bitcoin.pdf) 

[[!redirects proof of work]]