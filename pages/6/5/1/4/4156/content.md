
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

This page is about PCT theorems in [[quantum field theory]]. PCT stands for parity, charge and [[time-reversal symmetry]] (warning: the order of the letters P, C and T varies, some authors use CPT, for example). The laws of nature as described by [[quantum field theory]] are believed to be invariant if one simultaneously reverses the arrow of time, conjugates all charges and reverses all chiral properties. PCT theorems try to make this belief precise by defining the appropriate operators and showing that certain expressions remain constant. Both the statements and the proofs depend on the framework for [[quantum field theory]] one uses.

Being "invariant" means that every process that can be observerd in our universe can be observed identically in the "mirror" universe, that is there is no experiment in our universe that cannot be duplicated in the mirror universe. 

For some time physicists believed that subsets of the PCT symmetry are respected by nature, but today there are counterexamples known for every subset, for example:

* The [[weak nuclear force]] violates parity symmetry.

* Charge symmetry would violate the observation that the universe consists mostly of matter and not of matter and antimatter.

* For CP symmetry violation see Wikipedia: [CP violation](http://en.wikipedia.org/wiki/CP_violation)

* All known physical laws are time symmetric, but since PCT symmetry is believed to hold and CP symmetry does not hold, there has to be a process that breaks T symmetry. As of today there is no consenus about what that process may be (there are good reasons to believe that it has nothing to do with the second law of thermodynamics).  

## Abstract ##
...

## Definition ##

### Definition in the Wightman approach ###

The PCT theorem for Wightman fields (see [[Wightman axioms]]) was proved by Res Jost, see references.

This proof clarified the different conditions one has to impose, these are:

1. Covariance of the theory under the (connected part of the) [[Poincare group]].

2. Positivity of the energy.

3. There are only fields, which transform with respect to finite dimensional representations of the [[Lorentz group]]. (Transformation of the index space.)

4. Locality, which means that for spacelike distances the Bose fields commute with all other fields and the Fermi fields anticommute with each other.

5. The [[Minkowski space]] has even dimensions.

6. To every field in the theory appears its conjugate complex partner.

### Definition in the Haag-Kastler approach ###

Let $\mathcal{M}(\mathcal{J})$ be a [[AQFT|Haag-Kastler net]] on [[Minkowski spacetime]].

+-- {: .un_defn}
###### Definition

A **PCT operator** $\Theta$ on the local net is an anti-linear [[automorphism]], that is for every local algebra $\mathcal{M}(\mathcal{O})$, elements $A, B \in \mathcal{M}(\mathcal{O})$ and $\lambda \in \mathbb{C}$ we have the relations

1. $\Theta(A B) = \Theta(A) \Theta(B)$;

1. $\Theta(\lambda A) = \overline \lambda \Theta(A)$;

1. $\Theta(\mathcal{M}(\mathcal{O})) = \mathcal{M}(-\mathcal{O})$;

such that for $(\Lambda,a) \mapsto U(\Lambda, a)$ the given [[representation]] of the [[Poincare group]] on $\mathcal{M}$ we have 

1. $\Theta U(\Lambda, a) A = U(\Lambda, -a) \Theta A$;

1. $\Theta$ transforms every [[charge sector]] into its conjugate sector.

=--

A **PCT theorem** in this context is a theorem that states sufficient conditions such that a PCT operator $\Theta$ exists.

## Properties ##
...

## Examples ##
...

## Related concepts

* [[spin-statistics theorem]]

* [[antiparticle]], 

* [[charge sector]], [[DHR category]]

## References ##

Review for the [[standard model of particle physics]]:

* Robert S. Thorne, *The Standard Model Parity, Charge Conjugation and Time Reversal* &lbrack;[pdf](https://www.hep.ucl.ac.uk/postgrad/teaching/sm/SMIIL4.pdf), [[Thorne-StandardModelPCT.pdf:file]]&rbrack;

See also:

* Wikipedia: [CPT symmetry](http://en.wikipedia.org/wiki/CPT_symmetry)

Proof from the [[Wightman axioms]]:

* Res Jost: _Eine Bemerkung zum CPT Theorem_ Helv. Phys. Acta 30 (1957), p.409-416

Monographs on this formulation in [[algebraic quantum field theory]]:

* [[Raymond F. Streater]], [[Arthur S. Wightman]], *PCT, Spin and Statistics, and All That*, Princeton University Press (1989, 2000) &lbrack;[ISBN:9780691070629](https://press.princeton.edu/books/paperback/9780691070629/pct-spin-and-statistics-and-all-that), [jstor:j.ctt1cx3vcq](https://www.jstor.org/stable/j.ctt1cx3vcq)&rbrack;

* {#Strocchi13} [[Franco Strocchi]], §4.3 in: _An Introduction to Non-Perturbative Foundations of Quantum Field Theory_, Oxford University Press (2013) &lbrack;[doi:10.1093/acprof:oso/9780199671571.001.0001](https://doi.org/10.1093/acprof:oso/9780199671571.001.0001)&rbrack;

See also:

* [[Jonathan Bain]]: *CPT Invariance and the Spin-Statistics Connection*, Oxford University Press (2016) \[<a href="https://global.oup.com/academic/product/cpt-invariance-and-the-spin-statistics-connection-9780198728801">ISBN:9780198728801</a>, <a href="https://doi.org/10.1093/acprof:oso/9780198728801.001.0001">doi:10.1093/acprof:oso/9780198728801.001.0001</a>\]

On the [[PCT theorem]] for [[local observables]] in [[algebraic quantum field theory]]:

* [[Hans-Jürgen Borchers]], [[Jakob Yngvason]], *On the PCT--Theorem in the Theory of Local Observables*, in: *Mathematical physics in mathematics and physics: Quantum and operator algebraic aspects*, Fields Inst. Commun. **30** (2001) 39-64  &lbrack;[arXiv:math-ph/0012020](http://arxiv.org/abs/math-ph/0012020), [spire:538524](https://inspirehep.net/literature/538524)&rbrack;

Proof for [[Lagrangian]] field theory (not falling back to the [[AQFT]] axiomatics):

* Hilary Greaves, [[Teruji Thomas]], _The CPT theorem_, Studies in History and Philosophy of Modern Physics 45 (2014) 46-66 ([arXiv:1204.4674](http://arxiv.org/abs/1204.4674))


Discussion for [[curved spacetimes]]:

* [[M. D. Pollock]], *On the Dirac equation in curved space-time*, Acta Physica Polonica B **41** (2010) &lbrack;[InSpire:874211](https://inspirehep.net/literature/874211), [pdf](https://www.actaphys.uj.edu.pl/fulltext?series=Reg&vol=41&page=1827)&rbrack;

Discussion in for [[chiral fermions]] ([[Weyl spinors]]):

* I. P-Castro, J. L. Díaz-Cruz, A. Pérez-Lorenzana: *Discrete Symmetries in the Chiral Fermion Formalism* &lbrack;[arXiv:2504.02849](https://arxiv.org/abs/2504.02849)&rbrack;



See also:

* [[Juven Wang]], *C-P-T Fractionalization*, Phys. Rev. D **106** (2022) 105009 &lbrack;[arXiv:2109.15320](https://arxiv.org/abs/2109.15320), [doi:10.1103/PhysRevD.106.105009](https://doi.org/10.1103/PhysRevD.106.105009)&rbrack;

* I. P-Castro, J. L. Díaz-Cruz, A. Pérez-Lorenzana: *CPT Symmetry and its Breaking in the chiral fermion formalism* &lbrack;[arXiv:2411.05242](https://arxiv.org/abs/2411.05242)&rbrack;




[[!redirects PCT]]
[[!redirects PCT symmetry]]
[[!redirects CPT]]
[[!redirects CPT symmetry]]
[[!redirects CPT theorem]]

[[!redirects CPT-theorem]]

[[!redirects TCP theorem]]

