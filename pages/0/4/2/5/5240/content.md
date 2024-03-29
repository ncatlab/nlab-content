

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--





#Contents#
* table of contents
{:toc}


## Idea

The _monoid axiom_ is an extra condition on a [[monoidal model category]] that helps to make its [[model structure on monoids in a monoidal model category]] exist and be well behaved.

## Definition

+-- {: .num_defn #MonoidAxiom}
###### Definition

We say a [[monoidal model category]] satisfies the **monoid axiom** if every morphism that is obtained as a [[transfinite composition]] of [[pushouts]] of [[tensor products]] of acyclic cofibrations with any object is a weak equivalence.

=--

([Schwede-Shipley 00, def. 3.3.](#SchwedeShipley)).

+-- {: .num_remark}
###### Remark

In particular, the axiom in def. \ref{MonoidAxiom} says that for every object $X$ the functor $X \otimes (-)$ sends acyclic cofibrations to weak equivalences.

=--



## Properties 

+-- {: .num_lemma}
###### Lemma

Let $C$ be a 

* [[cofibrantly generated model category]];

* [[symmetric monoidal category]];

* [[monoidal model category]].

Then if the monoid axiom holds for the set of generating acyclic cofibrations it holds for all acyclic cofibrations.

=--

([Schwede-Shipley 00, lemma 3.5](#SchwedeShipley)).

+-- {: .num_theorem #ExistenceOfModelstructureOnMonoids}
###### Theorem

If a [[monoidal model category]] satisfies the monoid axiom and 

* it is a [[cofibrantly generated model category]];

* all objects are [[small objects]],

then the [[transferred model structure]] along the [[free-forgetful adjunction]] $(F \dashv U) : Mon(C) \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} C$ exists on its [[category of monoids]] and hence provides a [[model structure on monoids in a monoidal model category|model structure on monoids]].

=--

([Schwede-Shipley 00, theorem 4.1](#SchwedeShipley))

## Examples

+-- {: .num_prop}
###### Proposition

Monoidal model categories that satisfy the monoid axiom (as well as the other conditions sufficient for the [above theorem](#ExistenceOfModelstructureOnMonoids) on the existence of transferred model structures on categories of monoids) include

with respect to [[Cartesian product]]

* the standard [[model structure on simplicial sets]];

with respect to [[tensor product of chain complexes]]:

* the projective [[model structure on chain complexes]] for connective chanin complexes with fibrations the surjections in positive degree

and with respect to a [[symmetric monoidal smash product of spectra]]:

* the [[model structure on symmetric spectra]]

* the [[model structure on orthogonal spectra]]

* the [[model structure for excisive functors]]

* the [[model structure on Gamma-spaces]]

=--

([Schwede-Shipley 00, section 5](#SchwedeShipley), [MMSS 00, theorem 12.1 (iii)](#MMSS00))

## References

* {#SchwedeShipley} [[Stefan Schwede]], [[Brooke Shipley]], _Algebras and modules in monoidal model categories_ Proc. London Math. Soc. (2000) 80(2): 491-511  ([pdf](http://www.math.uic.edu/~bshipley/monoidal.pdf)) 

* {#MMSS00} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], part III of _[[Model categories of diagram spectra]]_, Proceedings London Mathematical Society Volume 82, Issue 2, 2000 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf), [publisher](http://plms.oxfordjournals.org/content/82/2/441.short?rss=1&ssource=mfc))


[[!redirects model structure on monoids]]


[[!redirects monoid axiom]]


