
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

A [[topological space]] is called _sequentially compact_ if every [[sequence]] of points in that space has a sub-sequence which [[convergence|converges]]. In general this concept is weaker than that of actual [[compact space|compactness]], but for some types of [[topological spaces]], such as [[metric spaces]], it is equivalent.

[[compact space|Compactness]] is an extremely useful concept in [[topology]].  The basic idea is that a [[topological space]] is [[compact space|compact]] if it isn't "fuzzy around the edges".

Whilst one can study a topological space by itself, it is often useful to probe it with known spaces.  A common choice for topological spaces, and in particular metric spaces, is to use the natural numbers, and the 1-point compactification of the natural numbers.  This is more traditionally known as studying the topology using sequences and convergent sequences.

Thus one can ask, "Can I detect compactness using probes from $\mathbb{N}$, and $\mathbb{N} \cup \{*\}$?".  The short answer to this is "No", but that just reveals that the question was too restrictive.  Rather, one should ask "What does compactness look like if all I'm allowed to use are probes from $\mathbb{N}$ and $\mathbb{N} \cup \{*\}$?".  The answer to that question is "sequential compactness".

Thus **sequential compactness** is what [[compact space|compactness]] looks like if all one has to test it are sequences.

## Definition 

+-- {: .num_defn #seqcpt}
###### Definition ######
A topological space is **sequentially compact** if every [[sequence]] in it has a [[convergence|convergent]] [[subsequence]].
=--



## Properties 

The following is a list of properties of and pertaining to sequentially compact spaces.


1. For a [[metric space]], the notions of sequential compactness and compactness coincide.

2. The [[Eberlein-Smulian theorem|Eberlein–Šmulian theorem]] states that in a [[Banach space]], for a subset with regard to the [[weak topology]], compactness and sequentially compactness are both equivalent to the weaker notion of [[countably compact space|countable compactness]].

3. A [[countable set|countable]] product of sequentially compact spaces is again sequentially compact.

   Let $\{X_k\}$ be a countable family of sequentially compact spaces.  Let $(a_l)$ be a sequence in $\prod X_k$.  For each $m$ we recursively define an infinite subset $A_m \subseteq A_{m-1} \subseteq \mathbb{N}$ with the property that the sequence $(a_l)_{l \in A_m}$ converges when projected down to $\prod_{k=1}^m X_k$.  Let $l_m = \min\{A_l\}$.  Consider the sequence $(a_{l_m})$.  For each $k$, we choose a limit $x_k$ of the projection of $(a_l)_{l \in A_k}$ to $X_k$.  Let $x = (x_k) \in \prod X_k$.  Let $U$ be a neighbourhood of $x$.  Then there is some $n \in \mathbb{N}$ and neighbourhood $U_n \subseteq \prod_{k=1}^n X_k$ of $(x_k)_{k=1}^n$ such that $U$ contains the preimage of $U_n$.  For $m \ge n$, the sequence $(l_m)$ is contained in $A_n$ and so the image of $(a_{l_m})$ converges to $(x_k)_{k=1}^n$.  Hence there is some $r$ such that for $m \ge r$, the projection of $a_{l_m}$ lies in $U_n$.  Hence for $m \ge r$, $a_{l_m} \in U$.  Thus $(a_{l_m})$ converges to $(x_k)$ and so $\prod X_k$ is sequentially compact.

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

### Relationship to Compactness 

[[compact space|Compactness]] does not imply sequentially compactness, nor does sequentially compactness imply compactness, without further assumptions (see for example wikipedia: [compact spaces](http://en.wikipedia.org/wiki/Compact_space)).
In [[metric spaces]] for example both notions coincide.

This is _not_ a contradiction to the statement that compact is equivalent to every [[net]] having a convergent subnet: Given a sequence in a compact space, its convergent _subnet_ need not be a _subsequence_ (see [[net]] for a definition of subnet).

## Examples and counter-examples

### A Compact Space that is not Sequentially Compact 

This counter-example is based on [Steen-Seebach, item 105](#SteenSeebach)

A famous example of a space that is compact, but not sequentially compact, is the product space
$$
    \{0,1\}^{I} := \{0, 1\}^{[0, 1]}
$$
with the [[product topology]]. It is compact by the [[Tychonoff theorem]]. 

Points of $\{0,1\}^{I}$ are functions $I \to \{0,1\}$, and the product topology is the topology of pointwise convergence.

Define a sequence $(a_n)$ in $I^{I}$ with $a_n(x)$ being the nth digit in the binary expansion of $x$ (we make the convention that binary expansions do not end in sequences of $1$s).  Let $a \coloneqq (a_{n_k})$ be a subsequence and define $p_a \in I$ by the binary expansion that has a $0$ in the $n_k$th position if $k$ is even and a $1$ if $k$ is odd (and, for definiteness and to ensure that this fits with our convention, define it to be $0$ elsewhere).  Then the projection of $(a_{n_k})$ at the $p_a$th coordinate is $1, 0, 1,0,...$ which is not convergent.  Hence $(a_{n_k})$ is not convergent.

(Basically that's the diagonal trick of [[Cantor's theorem]]).

However, as $\{0,1\}^I$ is compact, $a$ has a convergent subnet.  An explicit construction of a convergent subset, given a cluster point $a$, is as follows.  A function $a \colon I \to \{0,1\}$ is a cluster point of $(a_n)$ if, for any $p_1, \dots, p_n \in I$ the set

$$
A(p_1,\dots,p_n) \coloneqq \{k \in \mathbb{R} : a_k(p_i) = a(p_i) \forall i\}
$$

is infinite.  We index our subnet by the family of finite subsets of $I$ and define the subnet function $\mathcal{F}(I) \to \mathbb{N}$ to be

$$
\{p_1,\dots,p_n\} \mapsto \min A(p_1,\dots,p_n)
$$

This is a convergent subnet.

## References 

* Wikipedia, _[Sequentially compact space](https://en.wikipedia.org/wiki/Sequentially_compact_space)_

* {#SteenSeebach} Steen, Seebach: _Counterexamples in Topology_


[[!redirects sequentially compact]]
[[!redirects sequential compactness]]
[[!redirects sequentially compact space]]
[[!redirects sequentially compact spaces]]
