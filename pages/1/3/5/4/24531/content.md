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

A _second-order algebraic theory_ is a generalization of the notion of [[Lawvere theory]] to describe algebraic structures with variable binding.

While single-sorted Lawvere theories are [[cartesian monoidal categories]] generated from a single object, single-sorted second-order algebraic theories are [[cartesian monoidal categories]] generated from a single [[exponentiable object]].

## Definition

A second-order algebraic theory is a category $T$ with cartesian products and an exponentiable object $o$ such that every object of $T$ is isomorphic to a finite cartesian product of objects of the form $o \Rightarrow \cdots o$. 

## Multicategory

Just as Lawvere theories can be identified with [[cartesian multicategories]], there should be a similar correspondence between second-order theories and some notion of second-order cartesian multicategory.

## Examples

* The [[untyped lambda calculus]] can be described as a second-order algebraic theory, and [[simply typed lambda calculus]] as a multi-sorted second-order theory.

* The calculus of [[derivatives]] or more generally [[partial derivatives]].

## References

* [[Marcelo Fiore]] and Ola Mahmoud, _Second-order Algebraic Theories_, MFCS 2010, [arxiv](https://arxiv.org/abs/1308.5409)

A formalization in [[Agda]] by Marcelo Fiore and Dmitrij Szamozvancev: [webpage](https://www.cl.cam.ac.uk/~ds709/agda-soas/) with an [accompanying talk](https://www.youtube.com/watch?v=nP2J9SJ9DVM).