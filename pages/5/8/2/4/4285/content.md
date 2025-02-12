
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Definition

+-- {: .num_defn #Gdelta}
###### Definition
A **G-delta**, $G_\delta$, subset of a [[topological space]] is a set that can be written as the intersection of a [[countable family]] of open sets.
=--

## Results

One place where $G_\delta$-subsets occur is when looking at [[continuous maps]] from an arbitrary [[topological space]] to a [[metric space]] (or, more generally, a [[first countable space]]).  In particular, when considering continuous real-valued functions.  Thus we have the following connections to the [[separation axioms]].

+-- {: .num_theorem #PerNorm}
###### Theorem
A [[normal space]] in which every closed set is a $G_\delta$-set is [[perfectly normal space|perfectly normal]].
=--

+-- {: .num_theorem #ComReg}
###### Theorem
In a [[completely regular space]], every singleton set that is a $G_\delta$-set is the unique global maximum of a continuous real-valued function.
=--

+-- {: .proof}
###### Proof
One direction is obvious.  For the other, let $v$ be a point in a completely regular space $X$ such that $\{v\}$ is a $G_\delta$-set.  Let $\{V_n\}$ be a sequence of open sets such that $\bigcap V_n = \{v\}$.  We now define a sequence of functions $(f_n)$ recursively with the properties:

1. $f_n \colon X \to [0,1]$ is a continuous function,
1. $f_n(v) = 1$,
1. $f_n^{-1}(1)$ is a neighbourhood of $v$,
1. for $n \gt 1$, $f_n$ has support in $V_n \cap f_{n-1}^{-1}(1)$ whilst $f_1$ has support in $V_1$,

Having defined $f_1, \dots, f_{n-1}$, we define $f_n$ as follows.  Since $V_n \cap f_{n-1}^{-1}(1)$ is a neighbourhood of $v$ and $X$ is completely regular, there is a continuous function $\tilde{f}_n \colon X \to [0,1]$ with support in this neighbourhood and such that $\tilde{f}_n(v) = 1$.  We then compose with a continuous, increasing surjection $[0,1] \to [0,1]$ which maps $[\frac12,1]$ to $1$.  The resulting function is the required $f_n$.

We then define a function $f \colon X \to [0,1]$ by

$$
f(x) \coloneqq \sum_{n=1}^\infty \frac1{2^n} f_n(x).
$$

By construction, $f^{-1}(1) = \{v\}$.

We need to prove that this is continuous.  First, note that if $f_n(x) \ne 0$ then $f_k(x) = 1$ for $k \lt n$ and if $f_n(x) \ne 1$ then $f_k(x) = 0$ for $k \gt n$.  Hence the preimage under $f$ of $(\frac{2^k-1}{2^k}, \frac{2^{k+1}-1}{2^{k+1}})$ is $f_n^{-1}(0,1)$ and $f$ restricted to this preimage is a scaled translate of $f_n$.
From this, we deduce that the preimage of any open set not containing $1$ is open.  Thus $f$ is continuous everywhere except possibly at $v$.  Continuity at $v$ is similarly simple: given a set of the form $(1 -\epsilon,1]$ then there is some $n$ such that $2^{-n} \lt \epsilon$, whence $f^{-1}(1-\epsilon,1]$ contains all points such that $f_k(x) = 1$ for $k \le n$, which by construction is a neighbourhood of $v$.  Hence $f$ is continuous and has a single global maximum at $v$.
=--

+-- {: .un_theorem}
###### Mazurkiewicz theorem

In a [[metric space]], every [[completely metrizable space|completely metrizable]] subset is a $G_\delta$ subspace.

=--

([Mazurkiewicz 16](#Mazurkiewicz16))

+-- {: .un_theorem}
###### Hausdorff Gδ theorem

In a [[completely metrizable space]], every $G_\delta$ subspace is [[completely metrizable space|completely metrizable]].

=--

([Hausdorff 24](#Hausdorff24))

## Related concepts

* [[P-space]]

## References

* {#Mazurkiewicz16} [[Stefan Mazurkiewicz]], _Über Borelsche Mengen_, Bulletin International de l'Académie des Sciences de Cracovie, Classe des Sciences Mathématiques et Naturelles. Série A: Sciences Mathématiques. 1916, ZDB-ID 761846-3, S. 490–494.

* {#Hausdorff24} [[Felix Hausdorff]], _Die Mengen $G_\delta$ in vollständigen Räumen_, Fundamenta Mathematicae. Bd. 6, 1924, S. 146–148.

See also 

* Wikipedia _[Gδ space](https://en.wikipedia.org/wiki/G%CE%B4_space)_

[[!redirects G-delta]]
[[!redirects G-∞]]
[[!redirects Gδ]]
[[!redirects G-delta subspace]]
[[!redirects Gδ subspace]]
[[!redirects Gδ subspace]]
[[!redirects G-delta subspaces]]
[[!redirects G-∞ subspaces]]
[[!redirects Gδ subspaces]]
[[!redirects G-delta subset]]
[[!redirects G-∞ subset]]
[[!redirects Gδ subset]]
[[!redirects G-delta subsets]]
[[!redirects G-∞ subsets]]
[[!redirects Gδ subsets]]
[[!redirects G-delta set]]
[[!redirects G-∞ set]]
[[!redirects Gδ set]]
[[!redirects G-delta sets]]
[[!redirects G-∞ sets]]
[[!redirects Gδ sets]]
[[!redirects G-delta subset of a topological space]]
[[!redirects G-∞ subset of a topological space]]
[[!redirects Gδ subset of a topological space]]
[[!redirects G-delta subsets of a topological space]]
[[!redirects G-∞ subsets of a topological space]]
[[!redirects Gδ subsets of a topological space]]
[[!redirects G-delta subsets of topological spaces]]
[[!redirects G-∞ subsets of topological spaces]]
[[!redirects Gδ subsets of topological spaces]]
