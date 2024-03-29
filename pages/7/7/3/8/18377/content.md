
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

* table of contents
{: toc}

## Idea

The notion of a **pseudo-distributive law** is a [[vertical categorification]] of that of a [[distributive law]], relating two [[pseudomonads]] on a [[bicategory]]. There are various different levels of weakness that such a thing can exist at.  As with ordinary distributive laws, a pseudo-distributive law governs the lifting of one pseudomonad to the Eilenberg-Moore and Kleisli bicategories of the other.

## Definition

See any of the references, particularly [(Walker)](#Decagons), who simplified the definition of Marmolejo (reducing from 8 conditions to 5).

## Examples

* If $T$ is a [[pseudo-commutative 2-monad|pseudo-commutative]] [[2-monad]] on [[Cat]], then there is a pseudo-distributive law between $T$ and the 2-monad whose algebras are [[symmetric monoidal categories]]; see [(Kelly)](#Kelly).

* [[Grothendieck fibrations]] and opfibrations on a [[category]] $C$ (or more generally an object of a suitable 2-category) are the algebras for a pair of pseudomonads.  If $C$ has pullbacks, there is a pseudo-distributive law between these pseudomonads, whose joint algebras are the [[bifibrations]] satisfying the [[Beck-Chevalley condition]]; see [(von Glehn)](#vonGlehn).

* [[generalized polycategories]] are naturally defined relative to a pseudo-distributive law on a [[Prof]]-like bicategory; see [(Garner)](#Garner) for the canonical example of ordinary (symmetric) [[polycategories]].

* Pseudo-distributive laws involving [[lax-idempotent 2-monads]] have an especially nice form; see [(Marmolejo)](#MarmolejoDL) and [(Walker)](#Walker).

## Related pages

* [[distributive law]]

* [[pseudomonad]], [[relative pseudomonad]]

## References

* [[Eugenia Cheng]], [[Martin Hyland]], and [[John Power]].  _Pseudo-distributive laws_, [pdf](http://www.entcs.org/files/mfps19/83010.pdf)
 {#CHP}

* [[Max Kelly]], _Coherence theorems for lax algebras and for distributive laws_, Proceedings of the Sydney Category Seminar 1972-73.
 {#Kelly}

* [[Tamara von Glehn]], *Polynomials and models of type theory*, [PhD thesis](https://www.repository.cam.ac.uk/handle/1810/254394)
 {#vonGlehn}

* [[Richard Garner]], *Polycategories via pseudo-distributive laws*, [arXiv:math/0606735](http://arxiv.org/abs/math/0606735)
 {#Garner}

* Francisco Marmolejo, *Distributive laws for pseudomonads*, [TAC](http://tac.mta.ca/tac/volumes/1999/n5/5-05abs.html)
 {#MarmolejoDL}

* Charles Walker, *Distributive laws via admissibility*, [arXiv:1706.09575](https://arxiv.org/abs/1706.09575)
 {#Walker}

* Charles Walker. _Distributive laws, pseudodistributive laws and decagons_. [arXiv:2102.12468](https://arxiv.org/abs/2102.12468) (2021). {#Decagons}

[[!redirects pseudo-distributive laws]]
[[!redirects pseudodistributive law]]
[[!redirects pseudodistributive laws]]
[[!redirects pseudo distributive law]]
[[!redirects pseudo distributive laws]]
[[!redirects distributive law between pseudomonads]]
[[!redirects distributive law between pseudo-monads]]
