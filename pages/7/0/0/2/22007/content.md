

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

... [[idempotent]] [[semigroup]] ...

## Definition 

Recall that a _[[band]]_ is a [[semigroup]] in which every [[element]] is [[idempotent]]. 

[[commutative magma|Commutative]] bands are usually known as _[[semilattices]]_. This is the semigroup theoretic definition, but there is also an order theoretic definition: given a semilattice $L$ in this semigroup-theoretic sense, it has a canonical [[partial order]] given by $e\precreq f$ when $e f = e$. So semilattices are also [[posets]].

Finitely generated bands are finite: see [Howie 76, Section IV.4](#Howie76).

Now a _rectangular band_ may be described as a [[semigroup]] satisfying the identity $a b a = a$ for all elements $a$ and $b$. 

## Properties

If $S$ is a rectangular band, then there exist [[inhabited set|non-empty sets]] $I$ and $J$ such that $S$ is [[isomorphism|isomorphic]] as a [[semigroup]] to $I\times J$ equipped with the [[multiplication]]
$(i, j)(p,q) = (i,q)$ for $i,p\in I$ and $j,q\in J$.

Every [[band]] $S$ has a decomposition as a [[disjoint union]] $\coprod_{x\in L} R_x$ where $L$ is a semilattice, each $R_x$ is a [[subobject|sub]]-semigroup that is a rectangular band, and $R_x R_y \subseteq R_{x y}$ for every $x$ and $y$. This is a bit weaker than saying we have a [[functor]] from the [[poset]] $L$ to the [[category]] of rectangular bands, because we lack connecting morphisms $R_x \to R_y$.

A band $S$ satisfying the identity $x y x = x y$ for all $x$ and $y$ is said to be _left-regular_. Left-regular bands can arise from hyperplane arrangements and there has been work studying [[random walks]] on these hyperplane arrangements by analysing the semigroup algebras of the associated bands: see [Brown 00](#Brown00) and [Margolis-Saliola-Steinberg 15](#MargolisSaliolaSteinberg15)

## Related concepts

* [[distributive category]]

* [[reader monad]]

## References

* {#Howie76} J. Howie, _An introduction to semigroup theory_, Academic Press 1976.

* {#Brown00} Kenneth S. Brown, _Semigroups, rings, and Markov chains_ ([arXiv:math/0006145](https://arxiv.org/abs/math/0006145))

* {#MargolisSaliolaSteinberg15} Stuart Margolis, Franco Saliola, Benjamin Steinberg, _Cell complexes, poset topology and the representation theory of algebras arising in algebraic combinatorics and discrete geometry_ ([arXiv:1508.05446](https://arxiv.org/abs/1508.05446))



[[!redirects rectangular bands]]

[[!redirects band]]
[[!redirects bands]]
