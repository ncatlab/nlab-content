

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of _noncommutative probability space_ or _quantum probability space_ is the generalization of that of _[[probability space]]_ as the concept of "space" is generalized to [[non-commutative geometry]].

The basic idea is to encode a would-be [[probability space]] dually in its [[algebra of functions]] $\mathcal{A}$, typically regarded as a [[star algebra]], andencode the [[probability measure]] as a [[state on a star-algebra|state on this star algebra]] 

$$
  \langle
    (-) 
  \rangle
  \;\colon\;
  \mathcal{A}
    \longrightarrow
  \mathbb{C}
  \,.
$$

Hence this primarily [[axiom|axiomatizes]] the concept of _[[expectation values]]_ $\langle A\rangle$ ([Whittle 92](#Whittle92)) while leaving the nature of the underlying [[probability space]] more implicit.

Often $\mathcal{A}$ is assumed/required to be a [[von Neumann algebra]] (e.g. [Kuperberg 05, section 1.8](#Kuperberg05)). Often $\mathcal{A}$ is taken to be the full algebra of [[bounded operators]] on some [[Hilbert space]] (e.g. [Attal, def. 7.1](#Attal)).

In [[quantum physics]] $\mathcal{A}$ is an [[algebra of observables]] (or a [[local net of observables|local net]] thereof) and $\langle (-)\rangle$ is a particular [[quantum state]], for instance a [[vacuum state]].

## Related concepts

* [[quantum logic]]

* [[interpretation of quantum mechanics]]

## References

The axiomatization of [[probability theory]] in terms of the concept of [[expectation values]] (instead of underlying [[probability spaces]]) was amplified in

* {#Whittle92} [[Peter Whittle]], _Probability via expectation_, Springer 1992

Introduction to quantum probability theory includes

* {#Kuperberg05} [[Greg Kuperberg]], _A concise introduction to quantum probability, quantum mechanics, and quantum computation_, 2005 ([pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf))

* Miklos Redei, Stephen J. Summers, _Quantum Probability Theory_ ([arXiv:quant-ph/0601158](https://arxiv.org/abs/quant-ph/0601158))

* {#Attal} S. Attal, _Quantum probability_ ([pdf](http://math.univ-lyon1.fr/~attal/Quantum_Probability.pdf))


[[!redirects quantum probability theory]]

[[!redirects quantum probability space]]
[[!redirects quantum probability spaces]]

[[!redirects noncommutative probability space]]
[[!redirects noncommutative probability spaces]]

[[!redirects non-commutative probability space]]
[[!redirects non-commutative probability spaces]]

