

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

* [[PCT theorem]]

## References

The original formulation of the spin-statistics theorem:

* {#Fierz39} [[Markus Fierz]],  *Über die relativistische Theorie kräftefreier Teilchen mit beliebigem Spin*, Helvetica Physica Acta. **12** 1 (1939) 3-37 &lbrack;[doi:10.5169/seals-110930](https://doi.org/10.5169/seals-110930), [[Fierz-SpinStatistics.pdf:file]]&rbrack;

* {#Pauli40} [[Wolfgang Pauli]], *The connection between spin and statistics*, Phys. Rev. **58** (1940) 716-722 &lbrack;[doi:10.1103/PhysRev.58.716](https://doi.org/10.1103/PhysRev.58.716)&rbrack;

An argument via [[Dirac charge quantization]] is offered in:

* [[Richard Feynman]], pp. 48 in: *The reason for antiparticles*, in: [[Richard Feynman]] and [[Steven Weinberg]]: *Elementary Particles and the Laws of Physics: The 1986 Dirac Memorial Lectures*, Cambridge U. Press (1987) &lbrack;[doi:10.1017/CBO9781107590076](https://doi.org/10.1017/CBO9781107590076)&rbrack; 


Monographs:

* [[Raymond F. Streater]], [[Arthur S. Wightman]], *PCT, Spin and Statistics, and All That*, Princeton University Press (1989, 2000) &lbrack;[ISBN:9780691070629](https://press.princeton.edu/books/paperback/9780691070629/pct-spin-and-statistics-and-all-that), [jstor:j.ctt1cx3vcq](https://www.jstor.org/stable/j.ctt1cx3vcq)&rbrack;

* {#Strocchi13} [[Franco Strocchi]], §4.2 in: _An Introduction to Non-Perturbative Foundations of Quantum Field Theory_, Oxford University Press (2013) &lbrack;[doi:10.1093/acprof:oso/9780199671571.001.0001](https://doi.org/10.1093/acprof:oso/9780199671571.001.0001)&rbrack;

A statement and proof of both a spin-statistics and a [[PCT theorem]] in the [[axiom|axiomatics]] of [[algebraic quantum field theory]]:

* {#GuidoLongo94} [[Daniele Guido]], [[Roberto Longo]], *An Algebraic Spin and Statistics Theorem*, Commun. Math.Phys. **172** (1995) 517-534 &lbrack;[arXiv:funct-an/9406005] (http://arxiv.org/abs/funct-an/9406005), [doi:10.1007/BF02101806](https://doi.org/10.1007/BF02101806)&rbrack;

Geometric proofs of spin-statistics via [[configuration spaces of points]] (related to the [[Atiyah-Sutcliffe conjecture]]):

* {#BerryRobbins97} [[Michael V. Berry]], [[Jonathan M. Robbins]], *Indistinguishability for quantum particles: spin, statistics and the geometric phase*, Proceedings of the Royal Society A **453** 1963 (1997) 1771-1790 &lbrack;[doi:10.1098/rspa.1997.0096](https://doi.org/10.1098/rspa.1997.0096)&rbrack;

* A. F. Reyes-Lega, C. Benavides, *Remarks on the Configuration Space Approach to Spin-Statistics*,  Found Phys **40** (2010) 1004-1029 &lbrack;[arXiv:0911.0579](https://arxiv.org/abs/0911.0579), [doi:10.1007/s10701-009-9397-3](https://doi.org/10.1007/s10701-009-9397-3)&rbrack;

Generalization for [[AQFT on curved spacetime]] is in 

* {#Verch01} [[Rainer Verch]], _A spin-statistics theorem for quantum fields on curved spacetime manifolds in a generally covariant framework_, Communications in Mathematical Physics, **223** 2 (2001) 261-288 &lbrack;[arXiv:math-ph/0102035](http://arxiv.org/abs/math-ph/0102035), [doi:10.1007/s002200100526](http://dx.doi.org/10.1007/s002200100526)&rbrack;

Some brief exposition:

* [[John Baez]], *Spin, Statistics, CPT and All That Jazz* (2012) &lbrack;[web](http://math.ucr.edu/home/baez/spin_stat.html)&rbrack;
 

Discussion relating the spin-statistics theorem to [[extended topological field theory]], [[categorification]] (via [[2-rings]]) and [[Deligne's theorem on tensor categories]]:

* {#JohnsonFreyd15} [[Theo Johnson-Freyd]], _Spin, statistics, orientations, unitarity_, Algebraic and Geometric Topology &lbrack;[arXiv:1507.06297](https://arxiv.org/abs/1507.06297)&rbrack;

and via [[hermitian functorial field theory]]:

* [[Lukas Müller]], [[Luuk Stehouwer]], _Reflection Structures and Spin Statistics in Low Dimensions_ &lbrack;[arXiv:2301.06664](https://arxiv.org/abs/2301.06664)&rbrack;

* [[Luuk Stehouwer]], _The categorical spin-statistics theorem_ &lbrack;[arXiv:2403.02282](https://arxiv.org/abs/2403.02282)&rbrack;

[[!redirects spin-statistics theorems]]
