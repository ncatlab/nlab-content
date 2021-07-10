
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}
 
##Idea

The term 'shuffle' conjures up the idea of shuffling a pack of cards. In fact the mathematical idea is nearer to shuffling two packs of cards one through the other. Suppose we have a pack of $p$ cards and a pack of $q$ cards and we build a pack of $p+q$ cards, whilst retaining the order on the two 'sub-packs'.  The result is a $(p,q)$-shuffle. 

##Definitions

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

###Equivalent characterizations

Two other equivalent (and dual) ways of defining the notion of $(p,q)$-shuffle are as follows (e.g. [Hoffbeck-Moerdijk 17, section 1.1](#HoffbeckMoerdijk17)):

* Consider $p$ and $q$ as the [[linear orders]] $(p) = \{ 1 \lt \dots \lt p \}$ and $(q) = \{ 1 \lt \dots \lt q \}$. Then a $(p,q)$-shuffle is a way of extending the [[partial order]] on the [[coproduct]] $(p) + (q)$ to a linear order, or equivalently, a [[surjective]] [[monotone function]]
$$(p) + (q) \to (p+q).$$
* Consider $p$ and $q$ as [[non-empty]] [[linear orders]] $[p] = \{ 0 \lt \dots \lt p \}$ and $[q] = \{ 0 \lt \dots \lt q \}$. Then a $(p,q)$-shuffle is a [[maximal chain]] within the [[product]] [[partial order]] $[p] \times [q]$, or equivalently, an [[injective]] [[monotone function]]
$$[p+q] \to [p] \times [q].$$

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

### In $L_\infty$-algebras ###

In the definition of [[L-∞ algebras]]
the _unshuffle_ side of shuffles is used.

## Related concepts

* [[shuffles of trees]]

* [[Eilenberg-Zilber map]]

* [[Eilenberg-Zilber theorem]]

## References

Original articles:

* [[Samuel Eilenberg]], [[Saunders MacLane]], On the groups $H(\Pi,n)$, I, Ann. of Math. (2) 58, (1953), 55&#8211;106. ([jstor](https://www.jstor.org/stable/1969820))

Review:

* {#AguiarMahajan10} [[Marcelo Aguiar]], [[Swapneel Mahajan]], Section 2.2.3 in: _[[Monoidal Functors, Species and Hopf Algebras]]_, With forewords by [[Kenneth Brown]], [[Stephen Chase]], [[André Joyal]]. CRM Monograph Series __29__ Amer. Math. Soc. 2010. lii+784 pp. ([author pdf](http://www.math.cornell.edu/~maguiar/a.pdf))

* [[Kerodon]], 2.5.7.2 *$(p,q)$-Shuffles* ([00RH](https://kerodon.net/tag/00RH))

The two dual equivalent characterizations of $(p,q)$-shuffles (called _shuffles of linear trees_ or _shuffles of linear orders_) are discussed in section 1.1 of

* {#HoffbeckMoerdijk17} [[Eric Hoffbeck]], [[Ieke Moerdijk]], _Shuffles of trees_, ([arXiv:1705.03638](https://arxiv.org/abs/1705.03638)).

[[!redirects shuffles]]
[[!redirects unshuffle]]
[[!redirects unshuffles]]