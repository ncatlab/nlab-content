[[!redirects operator-valued distributions]]




+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
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

In mathematically rigorous constructions of [[perturbative quantum field theory]] -- such as via the [[Wightman axioms]] or [[causal perturbation theory]] -- the [[quantum observables]] which naively would be represented by would-be [[linear operators]] on some [[Hilbert space]] assigned to single points of [[spacetime]], such as the field operator "$\Phi(x)$" in [[scalar field theory]], are understood to yield such operators only after "smearing" or "[[adiabatic switching]]", namely after "integrating" them against a [[bump function]] on [[spacetime]]. This realizes these objects as [[continuous linear functionals]] on the space of bump functions with values in [[linear operators]], and hence as [[distributions]] with values not in the real numbers (as for ordinary distributions) but with values in operators. Where an ordinary distribution may be thought of as a "[[generalized function]] with values in the real numbers", such an "operator valued distribution" may be thought of as a "generalized function with values in linear operators". For example the object denoted $\Phi(x)$ is understood as really being a distribution which to a [[bump function]] $b$ assigns the (well-defined) operator traditionally written $\int_X b(x) \Phi(x) dvol$.

In [[causal perturbation theory]]/[[locally covariant perturbative AQFT]] these operator-valued distributions are just a means to an end: the actual [[algebra of observables]] is the [[Wick algebra]] of the [[free fields]] and its deformation to the [[interacting field algebra]], both of which are ([[Fedosov deformation quantization|Fedosov-]])[[formal deformation quantizations]]  of algebras of ordinary [[smooth functions]] on [[phase space]]. But since the [[phase space]] in field theory is itself a [[mapping space]] (for the [[scalar field]]) or more generally a [[space of sections]], such functions are conveniently expressed or constructed in terms of distributions.

Indeed the realization of these algebras via distributions makes transparent that 

1. the restriction of the [[free field]]'s [[Wick algebra]] to [[microcausal functionals]] is governed by the [[wave front set]] condition for the [[multiplication of distributions]];

1.  the [[renormalization]] freedom in defining the [[S-matrix]]/[[interacting field algebra]] is governed by the freedom of performing [[point-extensions of distributions]] .

This way the theory of [[distributions]] serves to give a mathematically rigorous construction of [[perturbative quantum field theory]]. The notorious "infinities" that allegedly "plague" perturbative quantum field theory in other approaches may be argued (vividly so in [Scharf 95, p. 181-182](#Scharf95)) to be just mathematical errors in handling distributions properly.

Incidentally, in the context of [[causal perturbation theory]]/[[locally covariant perturbative AQFT]] the "operator-valued distributions" are in general just _algebra-valued distributions_, since a [[representation]] of these algebra elements ([[quantum observables]]) as actual [[linear operators]] on some [[Hilbert space]] is not required, in fact it may not generally exists in a suitably invariant sense on [[AQFT on curved spacetimes|on curved spacetimes]] and if it exists it will not be unique, and even if a choice is made, most quantities of physical interest may be computed more directly from the algebra and a algebraic choice of [[state on an operator algebra|state]].

## Definition

Let $V$ be a [[topological vector space]] and $M$ a smooth manifold. A $V$-valued distribution on $M$ is a continuous linear function from the Schwarz space of test functions $\mathcal{S}(M)$ to $V$. 

Sometimes of course we use different spaces of test functions. 

## References

An early use of the concept of operator-valued distributions in [[perturbative quantum field theory]] is in the foundations of [[causal perturbation theory]] in

* {#EpsteinGlaser73} [[Henri Epstein]], [[Vladimir Glaser]], _[[The Role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211.

For review see

* Pierre Ca Grange, Ernst Werner, _Quantum fields as operator valued distributions and causality_ ([arXiv:math-ph/0612011](https://arxiv.org/abs/math-ph/0612011))

* {#Scharf95} [[Günter Scharf]], _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Berlin: Springer-Verlag, 1995, 2nd edition

* {#Scharf01} [[Günter Scharf]], _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001

* N. N. Bogoliubov, A. A. Logunov, A. I. Oksak, I. T. Todorov, _General principles of quantum field theory_, Kluwer 1990
