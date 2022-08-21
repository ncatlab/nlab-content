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

While single-sorted Lawvere theories are categories with [[cartesian products]] generated from a single object, single-orted second-order algebraic theories are cartesian categories generated from an [[exponentiable object]].

## Examples

* The [[untyped lambda calculus]] can be described as a second-order algebraic theory, and [[simply typed lambda calculus]] as a multi-sorted second-order theory.

* The calculus of [[derivatives]] or more generally [[partial derivatives]].

## References

* [[Marcelo Fiore]] and Ola Mahmoud, _Second-order Algebraic Theories_, MFCS 2010, [arxiv](https://arxiv.org/abs/1308.5409)

A formalization in [[Agda]] by Marcelo Fiore and Dmitrij Szamozvancev: https://www.cl.cam.ac.uk/~ds709/agda-soas/ with an [accompanying talk](https://www.youtube.com/watch?v=nP2J9SJ9DVM).