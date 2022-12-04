
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
 
## Idea

In [[mathematics]], by "shuffles" or "un-shuffles" one means  certain [[permutations]] , namely those which (when thought of as permuting the [[natural numbers]] $\{1, 2, \cdots, n \}$) are [[linear order]]-preserving along the first $p$ steps and then again along the remaining $q = n - p$ steps. 

The term 'shuffle' conjures up the idea of shuffling a pack of cards. In fact the mathematical idea is nearer to shuffling two packs of cards one through the other. Suppose we have a pack of $p$ cards and a pack of $q$ cards and we build a pack of $p+q$ cards, whilst retaining the order on the two 'sub-packs'.  The result is a $(p,q)$-shuffle. 

Or rather, the permutation in question may be seen as describing the un-doing of such a shuffling, whence some authors say "un-shuffle" for the same concept. 

{#Illustration} In this vein, the following graphics shows an illustration of an example of a $(4,3)$-(un-)shuffle of an ordered list of 7 elements:

\begin{tikzcd}[
  row sep=0pt
  ]
  7 &[-20pt] 
  {} \ar[rr, -, line width=5pt, blue, opacity=.3] &[-10pt] {}  &[+25pt] {} &[-10pt] {}
  &[+30pt]
  5 &[-20pt] {} &[-10pt] {} \ar[rr, -, line width=5pt, blue, opacity=.3] &[+25pt] {} &[-10pt] {}
  \\
  6 & {} \ar[rr, -, line width=5pt, blue, opacity=.3] & {}  & {} & {}
  &
  3 & {} & {} \ar[rr, -, line width=5pt, blue, opacity=.3] & {} & {}
  \\
  5 & {} & {} \ar[rr, -, line width=5pt, blue, opacity=.3] & {} & {}
  &
  2 & {} & {} \ar[rr, -, line width=5pt, blue, opacity=.3] & {} & {}
  \\
  4 & {}  \ar[rr, -, line width=5pt, blue, opacity=.3] & {} & {} & {}
  &
  7 &
  {} \ar[rr, -, line width=5pt, blue, opacity=.3] & {}  & {} & {}
  \\
  3 & {} & {} \ar[rr, -, line width=5pt, blue, opacity=.3] & {} & {}
  &
  6 & {} \ar[rr, -, line width=5pt, blue, opacity=.3] & {}  & {} & {}
  \\
  2 & {} & {} \ar[rr, -, line width=5pt, blue, opacity=.3] & {} & {}
  &
  4 & {}  \ar[rr, -, line width=5pt, blue, opacity=.3] & {} & {} & {}
  \\
  1 & {} \ar[rr, -, line width=5pt, blue, opacity=.3]  & {} & {} & {} 
  &
  1 & {} \ar[rr, -, line width=5pt, blue, opacity=.3]  & {} & {} & {} 
\end{tikzcd}



## Definitions

\begin{definition}

For $p,q \in \mathbb{N}$ two [[natural numbers]], a **$(p,q)$-shuffle** is a [[permutation]]

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

In more formal terms, a $(p,q)$-shuffle is a [[permutation]] $\sigma \,\in\, \Sigma_{p + q}$ (an [[element]] of the [[symmetric group]] [[group action|acting]] on the [[finite set]] $\{1, \cdots, p + q\}$ of $p + q$ [[elements]]), such that 

$$
  \sigma(1)
  \lt
  \sigma(2)
  \lt 
  \cdots
  \lt
  \sigma(p)
  \;\;\;\;\;\;\;\;
  \text{and}
  \;\;\;\;\;\;\;\;
  \sigma(p+1)
  \lt
  \sigma(p+2)
  \lt 
  \cdots
  \lt
  \sigma(p+q)
  \,;
$$

hence, equivalently, such that 

$$  
  \underset{1 \leq i \lt p+q}{\forall}
  \;\;\;\;\;\;\;\;\;\;
  i \neq p
    \;\;\;\;
      \Rightarrow
    \;\;\;\;
  \sigma(i) \lt \sigma(i + 1)
  \,.
$$

The **signature** of a $(p,q)$-shuffle is the [[signature of a permutation|signature]] of the corresponding permutation.

\end{definition}

Two other equivalent (and dual) ways of defining the notion of $(p,q)$-shuffle are as follows (e.g. [Hoffbeck-Moerdijk 17, section 1.1](#HoffbeckMoerdijk17)), naturally understood as characterizing the non-degenerate [[simplices]] in a [[product of simplices]] (e.g. [Kerodon 2.5.7.2](#Kerodon): [00RH](https://kerodon.net/tag/00RH)):

* Consider $p$ and $q$ as the [[linear orders]] $(p) = \{ 1 \lt \dots \lt p \}$ and $(q) = \{ 1 \lt \dots \lt q \}$. Then a $(p,q)$-shuffle is a way of extending the [[partial order]] on the [[coproduct]] $(p) + (q)$ to a linear order, or equivalently, a [[surjective]] [[monotone function]]

   $$
     (p) + (q) \to (p+q)
   $$

* Consider $p$ and $q$ as [[non-empty]] [[linear orders]] $[p] = \{ 0 \lt \dots \lt p \}$ and $[q] = \{ 0 \lt \dots \lt q \}$. Then a $(p,q)$-shuffle is a [[maximum|maximal]] [[chain]] within the [[product]] [[partial order]] $[p] \times [q]$, or equivalently, an [[injective]] [[monotone function]]:

  $$
    [p + q] \to [p] \times [q]
    \,.
  $$

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