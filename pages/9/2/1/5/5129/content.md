[[!redirects shuffles]]


#Contents#
* table of contents
{:toc}
 
##Idea

The term 'shuffle' conjures up the idea of shuffling a pack of cards. In fact the mathematical idea is nearer to shuffling two packs of cards one through the other. Suppose we have a pack of $p$ cards and a pack of $q$ cards and we build a pack of $p+q$ cards, whilst retaining the order on the two 'sub-packs'.  The result is a $(p,q)$-shuffle. 

##Definition

###Shuffles

+-- {: .un_defn}
###### Definition

For $p,q \in \mathbb{N}$ two [[natural number]]s, a **$(p,q)$-shuffle** is a [[permutation]]

$$
  (\mu_1, \cdots, \mu_p, \nu_1, \cdots, \nu_q)
$$

of $(1,2, \cdots, p+q)$ subject to the condition that

$$  
  \mu_1 \lt \mu_2 \lt \cdots \lt \mu_p
$$

and

$$  
  \nu_1 \lt \nu_2 \lt \cdots \lt \nu_q
  \,.
$$

The **signature** of a $(p,q)$-shuffle is the [[signature of a permutation|signature]] of the corresponding permutation.

=--

### Unshuffles 

The same concept viewed from the other end leads to _unshuffles_ .  These are just shuffles but are used in dual situations in the applications. The definition that follows is 'from the literature'. It is equivalent to that of shuffle that we gave above. (Although not needed, it is important to note the different terminology used in certain applications of the idea for when original source material is consulted.)


+-- {: .un_defn}
###### Definition
We say that a permutation $\sigma\in S_n$ is a $(j,n-j)$-unshuffle, $o\leq j\leq n$ if $\sigma(1)\lt \ldots \sigma(j)$ and $\sigma(j+1)\lt \ldots \lt \sigma(n)$.
=--
You can also say that $\sigma$ is a $(j,n-j)$-unshuffle if $\sigma(i) \lt \sigma(i+1)$ when $i\neq j$.


## Applications 

### Products of simplices

Shuffles control the combinatorics of [[product]]s of [[simplices]]. See [[products of simplices]] for details.

### Eilenberg-Zilber map

Related to the product of simplices: shuffles control the [[Eilenberg-Zilber map]]. See there for details.

###Differential graded coalgebras

Shuffles are used in defining the pre-cgc structure on $\bigwedge V$ in the theory of [[differential graded coalgebras]]

###Differential graded Hopf algebras
Shuffles are also used for defining the shuffle product on $T(V)$, see [[differential graded Hopf algebra]].

### In $L_\infty$- and $A_\infty$-algebras [[L-infinity algebras]]

In the definitions of [[A-∞ algebras]] and [[L-∞ algebras]]
the _unshuffle_ side of shuffles is used.

[[!redirects shuffles]]
[[!redirects unshuffle]]
[[!redirects unshuffles]]