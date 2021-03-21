
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Separable spaces
* table of contents
{: toc}

## Definitions

A [[topological space]] is __separable__ if it has a [[countable set|countable]] [[dense subspace|dense]] subset.

To be explicit, $X$ is __separable__ if there exists an [[infinite sequence]] $a\colon \mathbb{N} \to X$ such that, given any point $b$ in $X$ and any [[neighbourhood]] $U$ of $b$, we have $a_i \in U$ for some $i$.


## Properties

A [[second-countable space]] is separable (and trivially it is 
[[first-countable space|first-countable]]). However, first-countability plus separability do not imply second-countability; a counterexample is $\mathbb{R}$ with the half-open topology (see [Munkres](#Munk), page 192), denoted $\mathbb{R}_l$. 

An arbitrary [[product]] of separable spaces need not be separable, but a product of as many as a continuum number of separable spaces _is_ separable (with the product computed in [[Top]]); a proof of the more general Hewitt-Marczewski-Pondiczery theorem can be found [here](#Brandsma). In particular, the space $\mathbb{R}^\mathbb{R}$ of _all_ [[functions]] $\mathbb{R} \to \mathbb{R}$ under pointwise convergence is separable, but is not even first-countable (and thus not second-countable either). A first-countable space need not be separable; a simple example of that is a [[discrete space]] of uncountable cardinality. 

+-- {: .num_remark} 
###### Remark 
Although an arbitrary product of separable spaces need not be separable, an arbitrary product of separable spaces does satisfy the [[countable chain condition]] (see there for more discussion). This is somewhat remarkable, since it is not necessarily true that even a finite product of spaces satisfying the countable chain condition also satisfies the countable chain condition (whether it does is independent of [[ZFC]]). 
=-- 

Subspaces of separable spaces need not be separable. Example: the product $\mathbb{R}_l \times \mathbb{R}_l$, also called the [[Sorgenfrey plane]], is separable, but the subspace defined by the equation $y = -x$ is uncountable and discrete and therefore not separable. However, open subspaces of separable spaces are separable. 

Many results in [[analysis]] are easiest for separable spaces.  This is particularly true if one wishes to avoid using strong forms of the [[axiom of choice]], or to use arguments [[predicative mathematics|predicative]] over the natural numbers. For example, the [[Hahn-Banach theorem]] for _separable_ [[Banach spaces]] can be established using only mild forms of choice, e.g., [[dependent choice]]. More precisely, it can be established in the weak subsystem $WKL_0$ of [[second-order arithmetic]]; see [Brown-Simpson](#BS). 

## Separable metric spaces 

A classical fact is 

+-- {: .num_theorem #classical} 
###### Theorem 
Using [[countable choice]], then:

For a metric space $X$ the following are equivalent

1. $X$ is separable;
1. $X$ is [[second-countable space|second-countable]];
1. $X$ is [[Lindelöf space|Lindelöf]], i.e. any open cover admits a countable subcover.
=--

+-- {: .proof} 
###### Proof 
The second property is implied by the first: given any dense subset $\{x_n \mid n\in \mathbb{N}\}$, form the countable system of sets $\{B_{1/m}(x_n) \mid n,m\in\mathbb{N}\}$. To see that this is indeed a [[base]] for the topology of $X$, take any open set $U\subset X$, a point $x\in U$ and a radius $1/k$ such that $B_{1/k}(x)\subset U$. By separability there is some $n$ such that $x_n\in B_{1/(2k)}(x)$ and therefore $x\in B_{1/(2k)}(x_i)\subset U$.

To show (2) implies (3), let $\{U_n\}$ be a countable base of the topology.
Given any open cover $\{V_\lambda\}$ of $X$, we can form the index set $I\subset \mathbb{N}$ of those $n$ that are contained in some $V_\lambda$.
By assumption $\bigcup_{i\in I} U_{i} = \bigcup_\lambda V_\lambda = X$.
The axiom of [[countable choice]] provides now a section of $\bigsqcup_{i\in I} \{\lambda \mid U_i \subset V_\lambda\}\to I$.

Finally, we prove that (3) implies (1).
Consider the open covers $\{B_{1/1}(x) \mid x\in X\}$, $\{B_{1/2}(x) \mid x\in X\}$, ...
From each extract a countable subcover corresponding to collection of centers $A_1, A_2, \ldots$. We claim that that the union $A_1\cup A_2\cup\ldots$ forms a dense set.
Indeed, given any $y\in X$ and $n$ the point $x$ has to be contained in some $B_{1/n}(x)$ for some $x\in A_n$.
=-- 

\begin{remark}
In the proof any variant of the [[axiom of choice]] is only used for the implication $(2)\Rightarrow(3)$. On the other hand, assuming [[countable choice]], this implication [[second-countable spaces are Lindelöf|holds in every topological space]].
The implication $(2)\Rightarrow(1)$ holds in any topological space as well (see Example \ref{2ndCountablImplSeparable})
\end{remark}

Similar in spirit to (1)$\Leftrightarrow$(2) but less well-known is the following. 

+-- {: .num_theorem} 
###### Theorem 
A [[metric space]] $X$ is separable iff every open set is a countable union of balls. 
=-- 

+-- {: .proof} 
###### Proof 
One direction is not hard: if $x_i$ is a countable dense subset of $X$ and $r_j$ is an enumeration of the rationals, then according to the proof of Theorem \ref{classical}, the balls $B_{r_j}(x_i)$ form a countable base ($X$ is a [[second-countable space]]). Hence every open set is a union of a family of such balls that is at most countable. 

The other direction is trickier. (This is based on a [MathOverflow discussion](http://mathoverflow.net/questions/181226/if-any-open-set-is-a-countable-union-of-balls-does-it-imply-separability), which for the moment we record with little adaptation.) Suppose $X$ is not separable; construct by recursion a sequence $x_\beta$ of length $\omega_1$ such that no $x_\beta$ lies in the closure of the set of its predecessors $x_\alpha$ (each such set is countable and therefore not dense, so such $x_\beta$ outside its closure can be found at each stage). 

Therefore, for each $x_\beta$ we may choose a rational radius $r_\beta$ such that the ball $B_{r_\beta}(x_\beta)$ contains no predecessor $x_\alpha$. There are uncountably many $\beta$, so some rational radius $r$ was used uncountably many times. The collection of $x_\beta$ for which $r_\beta = r$ forms another $\omega_1$-sequence which we now use instead of the first; since all the radii are the same, this sequence has the property that each $B_r(x_\beta)$ contains no other $x_\alpha$, no matter whether $\alpha$ appears before or after $\beta$ in the sequence. 

Provided that there uncountably many such $x_\alpha$ that are non-isolated in $X$, we can construct an open set $U$ that is not a countable union of balls. For around each such $x_\alpha$ we can find a point $p_\alpha \neq x_\alpha$ within distance $r/4$ of $x_\alpha$; put $U = \bigcup_\alpha B_{d(x_\alpha, p_\alpha)}(x_\alpha)$. Notice that $p_\alpha \notin U$. If $B_s(x)$ is any ball contained in $U$, then $d(x, x_\gamma) \lt r/4$ for some $\gamma$. Supposing we have distinct $x_\alpha, x_\beta \in B_s(x)$, then $r \lt d(x_\alpha, x_\beta) \leq d(x_\alpha, x) + d(x, x_\beta) \lt s + s$, so $r/2 \lt s$. But then from $d(x_\gamma, p_\gamma) \lt r/4$ and $d(x, x_\gamma) \lt r/4$, we have $d(x, p_\gamma) \lt r/2 \lt s$ so that $p_\gamma \in B_s(x) \subset U$, a contradiction. We conclude that any ball contained in $U$ contains at most one $x_\alpha$, and so $U$ cannot be covered by countably many balls. 

We are therefore left to deal with the case where there are at most countably many non-isolated $x_\beta$. Discard these, so without loss of generality we may suppose all the $x_\beta$ are isolated points of $X$ and that for some fixed $r$ the ball $B_r(x_\beta)$ contains no other $x_\alpha$. Let $Z$ be this set of $x_\beta$. For each $\beta$, let $t_\beta$ be the supremum over all $t$ such that $B_t(x_\beta) \cap Z$ is countable. It follows that $B_{t_\beta}(x_\beta) \cap Z$ is itself countable, as is $\{\alpha: \alpha \lt \beta\}$. At each stage $\beta$, there is a countable set $C_\beta \subset Z$ disjoint from $B_{t_\beta}(x_\beta) \cup \{x_\alpha: \alpha \lt \beta\}$ such that for each $s \gt t_\beta$, there exists $y \in C_\beta$ with $d(x_\beta, y) \lt s$. By transfinite induction, we can construct a cofinal subset $I$ of $\omega_1$ such that $x_\beta \notin C_\alpha$ whenever $\alpha, \beta \in I$ and $\alpha \lt \beta$. The set $Y = \{x_\alpha: \alpha \in I\}$ is open in $X$, and we claim that it is not a countable union of balls. For suppose otherwise. Let $F$ be such a countable family of balls; then there is some minimal $\alpha$ for which $B_t(x_\alpha) \in F$ is uncountable, so that $t \gt t_\alpha$. By construction of $C_\alpha$, there exists $z \in C_\alpha \cap B_t(x_\alpha)$. But since $Y = \bigcup F$, we have that $z = x_\beta$ for some $\beta \in I$, and this contradicts our condition on $I$. 
=-- 

## Examples

\begin{example}\label{2ndCountablImplSeparable}
Every [[second-countable topological space]] is separable.
To see this take a countable cover and select a point in each member of the cover (using [[countable choice]]).
\end{example}

## Related countability properties

[[!include topology - countability axioms]]

## Related concepts

* [[separable metric space]]

* [[separable Hilbert space]]

* [[Hausdorff topological space]] 

## References 

* {#Munk} [[James Munkres]], _Topology, a first course_, Prentice-Hall (1975). 
 

* {#BS} D. K. Brown and S. G. Simpson, _Which set existence axioms are needed to prove the separable Hahn-Banach theorem?_, Annals of Pure and Applied Logic 31 (1986), pp. 123-144. 
 

* {#Brandsma} Henno Brandsma, Thread on Hewitt-Marczewski theorem, Ask a Topologist (2010) ([link](http://at.yorku.ca/cgi-bin/bbqa?forum=ask_a_topologist_2010;task=show_msg;msg=0487.0001)) 
  


[[!redirects separable space]]
[[!redirects separable spaces]]

[[!redirects separable topological space]]
[[!redirects separable topological spaces]]
