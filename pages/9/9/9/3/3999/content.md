
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea 

A [[topological space]] is called _sequentially compact_ if every [[sequence]] of points in that space has a sub-sequence which [[convergence|converges]]. In general this concept neither implies nor is implied by that of actual [[compact space|compactness]], but for some types of [[topological spaces]], such as [[metric spaces]], it is equivalent.

[[compact space|Compactness]] is an extremely useful concept in [[topology]].  The basic idea is that a [[topological space]] is [[compact space|compact]] if it isn't "fuzzy around the edges".

Whilst one can study a topological space by itself, it is often useful to probe it with known spaces.  A common choice for topological spaces, and in particular metric spaces, is to use the natural numbers $\mathbb{N}$, and the [[one-point compactification]] $\mathbb{N} \cup \{*\}$ of the natural numbers.  This is more traditionally known as studying the topology using sequences and convergent sequences.

Thus one can ask, "Can I detect compactness using probes from $\mathbb{N}$, and $\mathbb{N} \cup \{*\}$?".  The short answer to this is "No", but that just reveals that the question was too restrictive.  Rather, one should ask "What does compactness look like if all I'm allowed to use are probes from $\mathbb{N}$ and $\mathbb{N} \cup \{*\}$?".  The answer to that question is "sequential compactness".

Thus **sequential compactness** is what [[compact space|compactness]] looks like if all one has to test it are sequences.

## Definition 

+-- {: .num_defn #seqcpt}
###### Definition ######
A topological space is **sequentially compact** if every [[sequence]] in it has a [[convergence|convergent]] [[subsequence]].
=--



## Properties 

The following is a list of properties of and pertaining to sequentially compact spaces.


1. For a [[metric space]], the notions of sequential compactness and compactness coincide. See at _[[sequentially compact metric spaces are equivalently compact metric spaces]]_.

2. The [[Eberlein-Smulian theorem|Eberlein–Šmulian theorem]] states that in a [[Banach space]], for a subset with regard to the [[weak topology]], compactness and sequentially compactness are both equivalent to the weaker notion of [[countably compact space|countable compactness]].

3. A [[countable set|countable]] product of sequentially compact spaces is again sequentially compact.
+-- {: .proof} 
###### Proof 
Let $\{X_j\}$ be a countable family of sequentially compact spaces.  Let 
$$\pi_k: \prod_j X_j \to X_k$$ 
denote the $k^{th}$ projection, and let $(x(n))$ be a sequence in $\prod X_j$. We build a sequence of nested subsequences $S_j = x_j(n)$ as follows. For $j = 1$, choose a subsequence $S_1$ of the given sequence $(x_n)$ such that $x_1(1) = x(1)$ and such that $\pi_1(S_1)$ converges to a point $y_1 \in X_1$. Then, supposing that $S_j$ has been constructed, choose S_{j+1}$ to be a subsequence of $S_j$ that starts off the same way as $S_j$, 
$$x_{j+1}(1) = x_j(1), \ldots, x_{j+1}(j) = x_j(j),$$ 
and such that $\pi_{j+1}(S_{j+1})$ converges to $y_{j+1} \in X_{j+1}$. By the [[axiom of dependent choice]], we may suppose these choices have been made for all $j$, and then we form the diagonal sequence $S$ given by $x_j(j)$. This is a subsequence of each $S_j$, and so $\pi_j(S)$ converges to $y_j$ for every $j$, hence $S$ converges to the point $(y_j) \in \prod_j X_j$, and we have produced the desired convergent subsequence. 
=-- 

   This shows that the example of a compact space that is not sequentially compact is about as simple as can be.

4. The theorem that a continuous bijection from a compact space to a Hausdorff space is a homeomorphism has a counterpart for sequentially compact spaces.

   +-- {: .num_theorem #SeqCptReg}
   ###### Theorem
   Let $\mathcal{T}_1$ and $\mathcal{T}_2$ be two topologies on a set $X$ such that:

   1. $\mathcal{T}_1 \supseteq \mathcal{T}_2$ (equivalently, the identity map on $X$ is continuous as a map $(X,\mathcal{T}_1) \to (X, \mathcal{T}_2)$)
   2. $\mathcal{T}_1$ is sequentially compact
   3. $\mathcal{T}_2$ is [[completely regular space|completely regular]] and singleton sets are $G_\delta$-[[G-delta set|sets]],

   then $\mathcal{T}_1 = \mathcal{T}_2$.
   =--

   +-- {: .proof}
   ###### Proof
   Let $V \subseteq X$ be such that $V \notin \mathcal{T}_2$.  Then it must be non-empty and there must be a point $v \in V$ such that $V$ is not a neighbourhood of $v$.  As $\mathcal{T}_2$ is completely regular and singleton sets are $G_\delta$ sets, there is a continuous function $g \colon (X, \mathcal{T}_2) \to \mathcal{R}$ such that $g^{-1}(0) = \{v\}$.  Since $V$ is not a neighbourhood of $v$, for each $n \in \mathbb{N}$, the set $g^{-1}(-\frac1n, \frac1n)$ is not wholly contained in $V$.  Thus for each $n$ there is a point $x_n \in X$ such that $x_n \notin V$ and $|g(x_n)| \lt \frac1n$.  As $\mathcal{T}_1$ is sequentially compact, this sequence has a $\mathcal{T}_1$-convergent subsequence, say $(x_{n_k})$ converging to $y$.  Since $g(x_n) \to 0$, $g(x_{n_k}) \to 0$ and thus $g(y) = 0$.  Thus $y = v$ and so $(x_{n_k}) \to v$ in $\mathcal{T}_1$.  As $x_{n_k}
 \notin V$ for all $n_k$, and $v \in V$, it must be the case that $V$ is not a $\mathcal{T}_1$-neighbourhood of $v$.  Hence $V \notin \mathcal{T}_1$.  Thus $\mathcal{T}_1 \subseteq \mathcal{T}_2$, whence they are equal.
   =--

5. The [[image]] of a sequentially compact space $X$ under a continuous map $f: X \to Y$ is also sequentially compact. For suppose $y_n$ is a sequence in $f(X)$, say $y_n = f(x_n)$. Then $x_n$ has a convergent subsequence $x_{n_j}$, converging to $x$ say, and by continuity $y_{n_j} = f(x_{n_j})$ converges to $f(x)$. 


### Relationship to Compactness 

[[compact space|Compactness]] does not imply sequentially compactness, nor does sequentially compactness imply compactness, without further assumptions, see at _[Examples and counter-examples](#Examples)_ below.

In [[metric spaces]] for example both notions coincide, see at [[sequentially compact metric spaces are equivalently compact metric spaces]]. (This is a consequence of the [[Lebesgue number lemma]] and the fact that  [[sequentially compact metric spaces are totally bounded]].)

This is _not_ a contradiction to the statement that compact is equivalent to every [[net]] having a convergent subnet: Given a sequence in a compact space, its convergent _subnet_ need not be a _subsequence_ (see [[net]] for a definition of subnet).

## Examples and counter-examples 
 {#Examples}

A [[metric space]] is sequentially compact precisely if it is [[compact topological space|compact]]. See at _[[sequentially compact metric spaces are equivalently compact metric spaces]]_.

In general neither of these two properties implies the other:

* Examples of a sequentially compact spaces which are not compact are given in in ([Buskes-Rooij 97, example 13.5](#BuskesRooij97), [Patty 08, chapter 4, example 13](#Patty08), [Vermeeren 10, prop. 18](#Vermeeren10)). The [[long line]] is such an example. 

* An example of a [[compact topological space]] which is not sequentially compact is given in ([Steen-Seebach 70, item 105](#SteenSeebach70)), recalled at [Vermeeren 10, prop. 17](#Vermeeren10). See at [compact space -- Compact spaces which are not sequentially compact](compact+space#CompactSpacesWhichAreNotSequentiallyCompact).

+-- {: .num_example #ACompactSpaceNotSequentiallyCompact}
###### Example
**(a compact space which is not sequentially compact)**

Consider the following uncountable power of the [[discrete space]] $2$, namely the [[product topological space]] (with its [[Tychonoff topology]])

$$
  X \coloneqq \underset{f: \mathbb{N} \to 2}{\prod} Disc(\{0,1\})
$$

of copies of the discrete space on two elements, indexed by functions $f: \mathbb{N} \to \{0, 1\}$. Since $Disc(\{0,1\})$ is a [[finite topological space|finite]] [[discrete topological space]] it is clearly compact. Therefore the [[Tychonoff theorem]] says that also $X$ is compact.

Let $(x_n)_{n: \mathbb{N}}$ be the sequence in $X$ given by the [[duality|double-dual embedding]] 

$$\mathbb{N} \to 2^{2^\mathbb{N}},$$ 

i.e., define $x_n$ to have coordinate at $f: \mathbb{N} \to 2$ given by $(x_n)_f = f(n)$. We claim this sequence has no subsequence that converges in $X$, so that $X$ is not sequentially compact. We will argue by contradiction. (This [[refutation by contradiction]], refuting sequential compactness, is [[constructive logic|constructively valid]]. The argument above that affirms compactness, via the Tychonoff theorem, is not constructive.) 

Suppose instead some subsequence $(x_{(n_k)})_{k \in \mathbb{N}}$ converges to some $x \in X$. Choose any $f: \mathbb{N} \to 2$ that is not eventually constant on the subsequence $(n_k)_{k: \mathbb{N}}$; for example, define $f: \mathbb{N} \to 2$ by $f(n_k) = k\; mod\; 2$, else $f(n) = 0$ if $n$ does not appear in the subsequence. Consider the open set $U_f = \{x_f\} \times \prod_{g: g \neq f} \{0, 1\}$, which is an open neighborhood of $x$. In order to have $x_{n_k} \in U_f$ for all $k \geq k_0$, we'd have to have $f(n_k) = x_f$ for all $k \geq k_0$, in other words $f$ would be eventually constant on the subsequence $n_k$. Contradiction.

=--



## Related concepts

* [[compact topological space]]

* [[countably compact topological space]]

* [[paracompact topological space]]

* [[locally compact topological space]]

* [[compactly generated topological space]]


## References 

* {#BuskesRooij97} Buskes, van Rooij, _Topological Spaces: From  Distance to Neighbourhood_, Springer 1997

* {#SteenSeebach70} Lynn Steen, J. Arthur Seebach, _Counterexamples in Topology_, Springer-Verlag, New York (1970) 2nd edition,  (1978), Reprinted by Dover Publications, New York, 1995

* {#Patty08} Wayne Patty, _Foundations of Topology_, Jones and Bartlett Publishers (2008)

* {#Vermeeren10} [[Stijn Vermeeren]], _Sequences and nets in topology_, 2010 ([pdf](http://stijnvermeeren.be/download/mathematics/nets.pdf))


See also

* Wikipedia, _[Sequentially compact space](https://en.wikipedia.org/wiki/Sequentially_compact_space)_



[[!redirects sequentially compact space]]
[[!redirects sequentially compact spaces]]

[[!redirects sequentially compact]]
[[!redirects sequential compactness]]


[[!redirects sequentially compact metric space]]
[[!redirects sequentially compact metric spaces]]
