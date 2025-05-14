
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Wick's lemma_ is a [[combinatorics|combinatorial]] formula for the product in [[associative algebras]] that appear in the context of [[free field theory]].

From the point of view of [[path integral quantization]], Wick's lemma is about the [[moments]] of [[Gaussian probability distributions]]. See at _[[Feynman diagram]]_ for more on this.


From the point of view of [[causal perturbation theory]] Wick's lemma expresses the [[Moyal deformation quantization]] of a [[free field theory]] ([[Wick algebras]]) in terms of [[operator products]] on.

[[!include Wick algebra -- table]]

From the point of view of [[BV-quantization]] Wick's lemma arises as a consequence of the [[homological perturbation lemma]]  ([Gwilliam, section 2.3](#Gwilliam)).

## Statement

Let $\mathcal{W}$ be the [[Wick algebra]] of the [[free field theory|free]] [[scalar field]], hence the space of [[microcausal observables]] with product the [[star product]] induced by the [[Wightman propagator]]:

$$
  \mathcal{W}
  \;\coloneqq\;
  \left(
    PolyObs(E,\mathbf{L})_{mc}, \star_{\Delta_H}
  \right)
$$

Then the evident map from $\mathcal{W}$ to [[linear operators]] on the [[Fock space]] equipped with their [[operator product]] $\circ$ is an [[associative algebra]] [[isomorphism]] onto its image:

$$
  \left(
    PolyObs(E,\mathbf{L})_{mc}, \star_{\Delta_H}
  \right)
    \underoverset{\simeq}{\text{Wick's lemma}}{\hookrightarrow}  
  \left(
    End(FockSpace), \circ
  \right) 
$$

([Dütsch 18, theorem 2.17](#Duetsch18), following [Dütsch-Fredenhagen 00,, pages 10-11](#DuetschFredenhagen00), [Dütsch-Fredenhagen 01](#DuetschFredenhagen01))

## Related concepts

* [[perturbation theory]]

* [[Feynman diagram]]

## References

Original articles include

* {#Wick50} [[Gian-Carlo Wick]], _The evaluation of the collision matrix_, Phys. Rev. 80, 268-272 (1950)

* {#Hepp69} [[Klaus Hepp]], _Th&#233;orie de la Renormalisation_ Lect. Notes in Physics, Springer 1969

* {#BrunettiFredenhagenVerch03} [[Romeo Brunetti]], [[Klaus Fredenhagen]], [[Rainer Verch]], theorem 2.4 in _The generally covariant locality principle -- A new paradigm for local quantum physics_, Commun.Math.Phys.237:31-68, 2003 ([arXiv:math-ph/0112041](https://arxiv.org/abs/math-ph/0112041))

The interpretation as an algebra isomorphism to the [[star product]] with respect to the [[Wightman propagator]] is made explicit in

* {#DuetschFredenhagen00} [[Michael Dütsch]], [[Klaus Fredenhagen]], pages 10-11 of _Algebraic Quantum Field Theory, Perturbation Theory, and the Loop Expansion_, Commun.Math.Phys. 219 (2001) 5-30 ([arXiv:hep-th/0001129](https://arxiv.org/abs/hep-th/0001129))

* {#DuetschFredenhagen01} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative algebraic quantum field theory and deformation quantization_, Proceedings of the Conference on Mathematical Physics in Mathematics and Physics, Siena June 20-25 (2000) ([arXiv:hep-th/0101079](http://xxx.uni-augsburg.de/abs/hep-th/0101079))

and [Dütsch 18, theorem 2.17](#Duetsch18)

Textbook accounts include

* {#Scharf95} [[Günter Scharf]], theorem 3.1 in _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Berlin: Springer-Verlag, 1995, 2nd edition

* {#Duetsch18} [[Michael Dütsch]], E.26 - E.30 in _[[From classical field theory to perturbative quantum field theory]]_, 2018


See also

* Wikipedia, _[Wick's theorem](https://en.wikipedia.org/wiki/Wick%27s_theorem)_

Discussion of Wick's lemma as a consequence of the [[homological perturbation lemma]] for [[BV-complexes]] is in 

* {#Gwilliam} [[Owen Gwilliam]], section 2.3 _Factorization algebras and free field theories_ PhD thesis ([pdf](http://math.berkeley.edu/~gwilliam/thesis.pdf))


Formalization of Wick's theorem in the [[proof assistant]] [[Lean]]:

* [[Joseph Tooby-Smith]]: *Digitalizing Wick's theorem* &lbrack;[arXiv:2505.07939](https://arxiv.org/abs/2505.07939)&rbrack;

 

[[!redirects Wick lemma]]
[[!redirects Wick's theorem]]
[[!redirects Wick theorem]]
