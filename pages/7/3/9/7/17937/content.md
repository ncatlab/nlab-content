
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A fundamental theorem of [[topology]]: for $n_1, n_2 \in \mathbb{N}$ two different natural numbers, $n_1 \neq n_2$, then the [[Cartesian spaces]] $\mathbb{R}^{n_1}$ and $\mathbb{R}^{n_2}$ of [[dimension]] $n_1$ and $n_2$, respectively, are _not_ [[homeomorphism|homeomorphic]] (while for $n_1 = n_2$ then of course they are). Hence [[dimension]] of [[topological manifolds]] is a _topological [[invariant]]_.

This seems intuitively obvious, but the [[formal proof]] (due to [[Brouwer]] around 1910) is comparatively hard, and the problem was an important open problem in the 19th century. To appreciate that the problem is harder than it may superficially seem it serves to notice that for every $n \in \mathbb{N}$ are [[surjective]] [[continuous maps]] $\mathbb{R}^1 \to \mathbb{R}^n$ (the [[Peano curves]]).


## Statement

+-- {: .num_theorem}
###### Theorem
**(Brouwer invariance of domain theorem)**

For $U \subset \mathbb{R}^n$ an [[open subset]] of a [[Cartesian space]], for any $n \in \mathbb{N}$, and for $f \colon U \to \mathbb{R}^n$ a [[continuous map|continuous]] [[injective map]], then its [[image]] $f(U)$ is also an [[open subset]].

=--

This is proven with tools from [[algebraic topology]], notably with the [[Brouwer fixed point theorem]].

+-- {: .num_cor}
###### Corollary
**(topological invariance of dimension)**

For $n_1, n_2 \in \mathbb{N}$ then the [[Cartesian spaces]] $\mathbb{R}^{n_1}$ and $\mathbb{R}^{n_2}$ are [[homeomorphism|homeomorphic]] precisely only if $n_1 = n_2$.

=--


## References

The first proof is due to [[Brouwer]] around 1910.

* [[Terry Tao]], _[Brouwer's fixed point and invariance of domain theorems, and Hilbert's fifth problem](https://terrytao.wordpress.com/2011/06/13/brouwers-fixed-point-and-invariance-of-domain-theorems-and-hilberts-fifth-problem/)_


* Wikipedia, _[Invariance of domain](https://en.wikipedia.org/wiki/Invariance_of_domain)_

[[!redirects invariance of domain]]