
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



## Properties
 {#Properties}

### Basic properties

\begin{remark}\label{NumberOfShuffles}
**(number of shuffles)**
\linebreak
  The number of $(p,q)$-shuffles is given by the [[binomial coefficient]] 
$$
  #
  Sh(p,q)
  \;\;=\;\;
  \left(
    {p + q} \atop p
  \right)
  \,.
$$
Because, due to the preservation of order in the two "decks", a shuffle $\sigma \in Sh(p,q)  \subset Aut\big(\{1, \cdots, p + q\}\big)$ is fully determined by which $p$ elements of $\{1, \cdots, p + q\}$ are in the  image of $\{1, \cdots p\}$, which is the number of choices of $p$ out of $p + q$ elements.
\end{remark}

### The poset of $(p,q)$-shuffles 

Any pair $(p,q)$ yields a [[poset]] relating the various $(p,q)$-[[shuffles]].  

For example, consider this $(2,1)$-shuffle:
$$
  \begin{matrix} 
    (0\lt 1) &-& (0\lt 2) &-& (1\lt 2)
  \end{matrix}
$$

(This [[Hasse diagram]] has been laid out horizontally to save space.  The bottom is to the left. The vertex $(0\lt 1)$ corresponds to the shuffle with $\mu_1 = 0, \mu_1 = 1$, and so on.)
 
We need here to explain the partial order.  We take the '$\mu$-signature' of the shuffle, that is, the ordered set $\mu_1\lt\ldots \lt \mu_p$. (Of course, this determines the $\nu$-signature as that is the complement of $\mu$.)

+--{: .num_defn}
######Definition######
Given two $(p,q)$-shuffles, represented by $(\mu, \nu)$ and $(\mu\prime,\nu\prime)$, we set 

$$(\mu, \nu) \leq (\mu\prime,\nu\prime)$$

if, for each $i$ in the range $1\leq i\leq p$, $\mu_i \leq \mu_i\prime.$  We refer to this poset as $(Shuff(p,q),\leq)$.
=--

Going to  $(Shuff(3,1),\leq)$, the poset for $(3,1)$-shuffles,  the fact that $q = 1$ will mean that this poset is again [[linear order|linear]]:
$$\begin{matrix}
(0 \lt 1 \lt 2) &-& (0 \lt 1 \lt 3)& - &(0 \lt 2 \lt 3)& - &(1 \lt 2 \lt 3)
\end{matrix}$$

This is true in general:

+--{: .num_lemma}
######Lemma
If $p = 1$ or $q = 1$, then  $(Shuff(p,q),\leq)$ is a [[linear order|linear poset]].
=--

+-- {: .proof}
######Proof######
If $p = 1$, $\mu = (\mu_1)$ is a singleton, and the poset will be:

$$\begin{matrix}
(0) & - & (1) & - & \ldots & - & (q).
\end{matrix}$$

For $q = 1$, $\nu = (\nu_1)$, and the poset is 

$$\begin{matrix}
(0 \lt 1 \lt \ldots \lt p-1) & - & (0 \lt 1 \lt \ldots \lt p-2 \lt p) & - & \ldots & - & (1 \lt \ldots \lt p),
\end{matrix}$$
where at each stage one misses out the single $\nu$-value.
=--

In all cases, each position is obtained from the one immediately to its 'left' by increasing _one_ value, yet remaining with a shuffle.  This is more clearly seen in the (2,2) example, which is no longer [[linear order|linear]].  First we display the grid in which things are happening.
$$\begin{matrix}
(0,2) & - & (1,2) & - & (2,2) \\
| & & | & & | \\
(0,1) & - & (1,1) & - & (2,1) \\
| & & | & & | \\
(0,0) & - & (1,0) & - & (2,0)
\end{matrix}$$

We can then look at the shuffle poset, noting again that it is not [[linear order|linear]]:


\begin{xymatrix@=1.5em}&&(1<2)\ar@{-}[dr]&&\\
(0<1)\ar@{-}[r]&(0<2)\ar@{-}[ur]\ar@{-}[dr]&&(1<3)\ar@{-}[r]&(2<3)\\
&&(0<3)\ar@{-}[ur]&&\end{xymatrix}


The left hand shuffle, labelled $(0\lt1)$, corresponds to $\left(\begin{array}{ccccc}0&1&2&2&2\\0&0&0&1&2\end{array}\right)$, so gives the path along the bottom of the square and then up the right hand side. 

\begin{xymatrix@=1.5em}&&(2,2)\ar@{-}[d]\\
&&(2,1)\ar@{-}[d]\\
(0,0)\ar@{-}[r]&(1,0)\ar@{-}[r]&(2,0)\end{xymatrix}

The first change goes to $(0\lt 2)$ and gives a path with 2 steps,

\begin{xymatrix@=1.5em}&&(2,2)\ar@{-}[d]\\
&(1,1)\ar@{-}[r]\ar@{-}[d]&(2,1)\\
(0,0)\ar@{-}[r]&(1,0)&\end{xymatrix}

and corresponds to the shuffle, $\left(\begin{array}{ccccc}0&1&1&2&2\\0&0&1&1&2\end{array}\right)$,
so at this position, $(0\lt2)$, there is a choice, either increase 0 by 1 to get $(1\lt 2)$ or increase 2 by 1 to get $(0\lt3)$. In the first case, we get the path  

\begin{xymatrix@=1.5em}&&(2,2)\ar@{-}[d]\\
(0,1)\ar@{-}[d]\ar@{-}[r]&(1,1)\ar@{-}[r]&(2,1)\\
(0,0)&&\end{xymatrix}

going horizontally across the square,
and the shuffle, $\left(\begin{array}{ccccc}0&0&1&2&2\\0&1&1&1&2\end{array}\right)$, 
and in the second case, we get the shuffle:
 $\left(\begin{array}{ccccc}0&1&1&1&2\\0&0&1&2&2\end{array}\right)$, and the obvious path up the middle of the square:

\begin{xymatrix@=1.5em}&(1,2)\ar@{-}[r]\ar@{-}[d]&(2,2)\\
&(1,1)\ar@{-}[d]&\\
(0,0)\ar@{-}[r]&(1,0)&\end{xymatrix}

From $(1 \lt 2)$ or $(0\lt3)$, there is only one way to go, namely to $(1 \lt 3)$ and a 2-step path (left to you), and, finally it is just one step from  $(1 \lt 3)$ to $(2 \lt 3)$ and the other extremal path.


\linebreak

In summary, each path corresponds to a simplex of maximal dimension in the product. The poset encodes the simplest relationships between those paths with the links in the Hasse diagram corresponding to simple changes in the path, and adjacency of the two simplices in the product, but note that the poset is usually not linear.

### The Anti-Lex order

There is a total order on $Shuff(p,q)$ related to the above partial order and which is useful when checking cancellation of terms in non-commutative contexts, as occurs in the Whitehead product formula given by Curtis and attributed to Kan.  This is the **anti-lexicographic order.


We  represent   a $(p,q)$-shuffle $(\mu,\nu)$ by an increasing $\mu$-sequence $\mu_1\lt \ldots \lt \mu_p$, (so with complementary $\nu$-sequence $\nu_1\lt \ldots \lt \nu_q$). 

We order the $(\mu,\nu)$ using just the $\mu$-sequence as, of course, that determines the $\nu$-sequence completely.  Inductively in $p$, we set 


$$\mu = (\mu_1,\ldots, \mu_p)\prec \mu\prime = (\mu\prime_1,\ldots, \mu\prime_p),$$

(i) if $\mu_p\lt \mu\prime_p$,

or

(ii) if $\mu_p = \mu\prime_p$ and $\mu_p$ is odd, 

$$(\mu_1,\ldots, \mu_{p-1})\prec (\mu\prime_1,\ldots, \mu\prime_{p-1}),$$

whilst if $\mu_p = \mu\prime_p$ and $\mu_p$ is even, 

$$(\mu_1,\ldots, \mu_{p-1})\succ (\mu\prime_1,\ldots, \mu\prime_{p-1}),$$ 

where we adopt the notation $(\mu_1,\ldots, \mu_p)$ instead of $(\mu_1\lt\ldots \lt \mu_p)$.

For example, on our (2,2)-shuffles, the total order is 

$$(0,1) - (1,2) - (0,2) - (0,3) - (1,3) - (2,3). $$

We note the lexicographic order on the sector with $\mu_2 = 2$ is reversed.

For illustrative purposes, we will look at two other examples. 

 First a generic $(p,1)$ case:  the shuffle poset for $(p,1)$ is, more or less, 

$$(0,\ldots , p-2) - (0,\ldots, p-4,p-3,p-1) - (0, \ldots, p-4,p-2,p-1) - 
 \ldots  -  (1, \ldots , p-1)$$

as, at each position, there is only one transposition that can be applied.  The anti-lex total order will correspond _exactly_ to this if $p-1$ is odd, but, if $p-1$ is even, it will reverse the order on the last $p-1$ positions giving 

$$(0,\ldots , p-2) - (1, \ldots , p-1) - (0,2, \ldots, p-1) -  \ldots  - (0,\ldots, p-3,p-1).$$

There are various points to note.  Firstly that if $p$ is even, the permutation corresponding to $(1, \ldots , p-1)$ is odd.  Secondly, the geometric picture is simply a prism, $\Delta[p]\times \Delta[1]$, and we can easily interpret the above order as a filling scheme for the simplices of $(\Delta[p]\times \Delta[1])\times \Delta[1]$, starting with the empty shell of 

$$(\Delta[p]\times \Delta[1])\times \{0\} \cup \partial(\Delta[p]\times \Delta[1])\times \Delta[1],$$ 

together with part of the top of the 'canister'.  (In general the total order seems to correspond to some sort of filling scheme although this is not always as clear as here.)

Our second case will be (3,2).  Again we will write $(i,j,k)$ instead of $i\lt j\lt k$ in order to save confusion over the various different orders being considered.  The shuffle poset, $\mathrm{Shuff}(3,2)$, has Hasse diagram given below:

\begin{xymatrix@=1.5em}&&(2,3,4)\ar@{-}[d]&\\
&&(1,3,4)\ar@{-}[dl]\ar@{-}[dr]&\\
&(1,2,4)\ar@{-}[dl]\ar@{-}[dr]&&(0,3,4)\ar@{-}[dl]\\
(1,2,3)\ar@{-}[dr]&&(0,2,4)\ar@{-}[dl]\ar@{-}[dr]&\\
&(0,2,3)\ar@{-}[dr]&&(0,1,4)\ar@{-}[dl]\\
&&(0,1,3)\ar@{-}[d]&\\
&&(0,1,2)&\end{xymatrix}

The subgraph of those with $\mu_3 = 4$, of course, is a copy of our earlier $(2,2)$-example, whilst that with $\mu_3 = 3$, is a copy of $Shuff(3,1)$.  Within that we have, on deleting the 3s from the final positions, a copy of $Shuff(2,1)$ and so on.  Taking $Shuff(2,1) \times \{3\}$, we can match it with a $Shuff(2,1) \times \{4\}$ within the $\mu_3 = 4$ block, the matching being given by, for instance, $(0,1,3)\leftrightarrow(0,1,4)$, etc.  The anti-lex order gives
\[
(0,1,2)-(0,1,3) - (1,2,3)-(0,2,3)-(2,3,4)-(1,3,4)-(0,3,4) - (0,2,4) - (1,2,4) - (0,1,4),\]

which is 
$$Shuff(3,1)\oplus Shuff(2,2)^{op}\times \{4\},$$
the ordinal sum, or join, of the anti-lex ordered shuffle sets.  This sort of decomposition is quite general.



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