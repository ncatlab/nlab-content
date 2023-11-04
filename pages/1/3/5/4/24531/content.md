+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea

A _second-order algebraic theory_ is a generalization of the notion of [[Lawvere theory]] to describe algebraic structures with [[bound variable|variable binding]].

While single-sorted Lawvere theories are [[cartesian monoidal categories]] generated from a single object, single-sorted second-order algebraic theories are [[cartesian monoidal categories]] generated from a single [[exponentiable object]].

## Definition

A second-order algebraic theory is a category $T$ with cartesian products and an exponentiable object $o$ such that every object of $T$ is isomorphic to a finite cartesian product of objects of the form $o^n \Rightarrow o$.

A model of a theory $T$ is given by a functor $M : T \to \Set$ that preserves cartesian products (not necessarily exponentials). On objects, such a functor must give for each $o^n \Rightarrow o$ a set $M(n)$ and the functoriality determines a first-order Lawvere theory/cartesian multicategory structure on $M$. So models of second order algebraic theories are first order algebraic theories with additional structure.

## Multicategory

Just as Lawvere theories can be identified with [[cartesian multicategories]], there should be a similar correspondence between second-order theories and some notion of second-order cartesian multicategory.

## Examples

* The [[untyped lambda calculus]] can be described as a second-order algebraic theory, and [[simply typed lambda calculus]] as a multi-sorted second-order theory.

* The calculus of [[derivatives]] or more generally [[partial derivatives]].

## References

* [[Marcelo Fiore]] and Chung-Kil Hur, _Term Equational Systems and Logics_, MFPS XXIV, [doi](https://doi.org/10.1016/j.entcs.2008.10.011)

* [[Marcelo Fiore]] and Ola Mahmoud, _Second-order Algebraic Theories_, MFCS 2010, [arxiv](https://arxiv.org/abs/1308.5409)

A formalization in [[Agda]]:

* Marcelo Fiore and Dmitrij Szamozvancev: [webpage](https://www.cl.cam.ac.uk/~ds709/agda-soas/) with an [accompanying talk](https://www.youtube.com/watch?v=nP2J9SJ9DVM).


Discussion via [[monads]]:

* [[Nathanael Arkor]], *Monadic and Higher-Order Structure*, PhD thesis, Cambridge (2022) &lbrack;[doi:10.17863/CAM.86347](https://doi.org/10.17863/CAM.86347), [pdf](https://www.repository.cam.ac.uk/bitstreams/666be4fb-957b-4c2e-83fc-8124621f0c43/download), [[Arkor-MonadicAndHigherStructure.pdf:file]]&rbrack;


[[!redirects second-order algebraic theory]]
[[!redirects second order algebraic theories]]
[[!redirects second-order algebraic theories]]

[[!redirects higher-order algebraic theory]]
[[!redirects higher-order algebraic theories]]


