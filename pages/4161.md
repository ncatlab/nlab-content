

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
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

## Idea ##
In [[quantum field theory]] on [[Minkowski space]] all fields must transform according to a definite (finite dimensional) [[representation]] of the universal cover of the [[Poincare group]], which determines the [[spin]] of each field. From the [[representation theory]] of the [[Poincare group]] it is known that the spin $s$ is a number $s = \frac{n}{2}$ with $n \in \mathbb{N}$.

On the other hand, if we take fields to be pointwise localized in the sense of the [[Wightman axioms]], then the locality axiom (also known as _Einstein microcausality_ ) says that spacelike separated field operators either commute or anticommute: Two [[Fermionic field]]s anticommute, two [[Bosonic field]]s commute, a Fermionic and a Bosonic field commute.

The **spin-statistics theorem** states that fields with integer spin $s$ (n  is even) are Bosonic fields, fields with half-integer spin (n is uneven) are [[Fermionic field]]s. A better name for the theorem would therefore be spin- _commutation_ theorem, the name spin- _statistics_ theorem stems from the fact that [[Boson]]s (the particles associated to [[Bosonic field]]s) are social, multiple particles can exist in the same quantum state, while [[Fermion]]s are not social: The [[Pauli exclusion principle]] says maximally one [[Fermion]] can exist in a given quantum state. This leads to different [[partition functions]] in [[statistical mechanics]] of systems consisting of [[Boson]]s only and of [[Fermion]]s only, hence the name.

The statement and proof of the theorem depend on the framework for [[quantum field theory]] that is used, therefore there are, strictly speaking, several versions of the spin-statistics theorem, but the _physical interpretation_ is always the same. 

## Statement

### In Algebraic quantum field theory

In the [[Haag-Kastler approach]] ("[[algebraic quantum field theory]]") the [[Bisognano-Wichmann theorem]] states a relation of the representation of the Poincare group on certain local algebras of [[local nets of algebras of observables]] and their [[modular groups]]. If this relation holds for a given net, then this net is said to fulfill the Bisognano-Wichmann property.

([GuidoLongo 94](#GuidoLongo94), [Verch 01](#Verch01))

...

## Related concepts

* [[Atiyah-Sutcliffe conjecture]]

## References

The original formulation of the spin-statistics theorem:

* {#Fierz39} [[Markus Fierz]],  _&#220;ber die relativistische Theorie kr&#228;ftefreier Teilchen mit beliebigem Spin_. Helvetica Physica Acta. 12 (1): 3&#8211;37. (1939) [doi:10.5169/seals-110930](https://dx.doi.org/10.5169%2Fseals-110930)

* {#Pauli40} [[Wolfgang Pauli]], _The connection between spin and statistics_, Phys. Rev. 58, 716&#8211;722 (1940)

Textbook account:

* R. F. Streater and A. S. Wightman, _PCT, Spin and Statistics, and All That_ , reprinted by Addison-Wesley, New York, 1989. 

The proof, which goes back originally to Fermi. There is also a more intuitive approach based on topology. One can see hints of it in Feynman's lecture here:

* [[Richard Feynman]] and [[Steven Weinberg]], _Elementary Particles and the Laws of Physics_ , the 1986 Dirac Memorial Lectures, Cambridge U. Press, Cambridge, 1987. 

Exposition:

* [[John Baez]], _Spin, Statistics, CPT and All That Jazz_ ([web](http://math.ucr.edu/home/baez/spin_stat.html))
 
A statement and proof of both a spin-statistics and a [[PCT theorem]] in the [[axiom|axiomatic]] of [[algebraic quantum field theory]] is in

* {#GuidoLongo94} [[Daniele Guido]], [[Roberto Longo]], _An Algebraic Spin and Statistics Theorem_ ([arXiv:funct-an/9406005] (http://arxiv.org/abs/funct-an/9406005))

Geometric proofs of spin-statistics via [[configuration spaces of points]] (related to the [[Atiyah-Sutcliffe conjecture]]):

* {#BerryRobbins97} [[Michael V. Berry]], [[Jonathan M. Robbins]], *Indistinguishability for quantum particles: spin, statistics and the geometric phase*, Proceedings of the Royal Society A **453** 1963 (1997) 1771-1790 ([doi:10.1098/rspa.1997.0096](https://doi.org/10.1098/rspa.1997.0096))

* A.F. Reyes-Lega, C. Benavides, *Remarks on the Configuration Space Approach to Spin-Statistics*,  Found Phys (2010) 40: 1004-1029 ([arXiv:0911.0579](https://arxiv.org/abs/0911.0579))


Generalization for [[AQFT on curved spacetime]] is in 

* {#Verch01} [[Rainer Verch]], _A spin-statistics theorem for quantum fields on curved spacetime manifolds in a generally covariant framework_, Communications in Mathematical Physics October 2001, Volume 223, Issue 2, pp 261&#8211;288 ([arXiv:math-ph/0102035](http://arxiv.org/abs/math-ph/0102035), [doi:10.1007/s002200100526](http://dx.doi.org/10.1007/s002200100526))

Discussion relating the spin-statistics theorem to [[extended topological field theory]], [[categorification]] (via [[2-rings]]) and [[Deligne's theorem on tensor categories]] is in 

* {#JohnsonFreyd15} [[Theo Johnson-Freyd]], _Spin, statistics, orientations, unitarity_, Algebraic and Geometric Topology ([arXiv:1507.06297](https://arxiv.org/abs/1507.06297))
