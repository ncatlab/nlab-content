
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _simplicial model category_ is a model or presentation for an [[(∞,1)-category]] that is half way in between a bare [[model category]] and a [[Kan complex]]-[[enriched category]].

Specifically, a simplicial model category is an [[sSet]]-[[enriched category]] $C$ together with the structure of a [[model category]] on its underlying [[category]] $C_0$ such that both structures are compatible in a reasonable way.

One important use of simplicial model categories comes from the fact that the full [[sSet]]-subcategory $C^\circ \hookrightarrow C$ on the fibrant-cofibrant objects -- which is not just [[sSet]]-enriched but actually [[Kan complex]]-enriched -- is the [[(∞,1)-category]]-enhancement of the [[homotopy category]] of the [[model category]] $C_0$.

For generalizations of this construction with [[sSet]] replaced by another [[monoidal model category]] see [[enriched homotopical category]].



## Definition

A **simplicial model category** is an [[enriched model category]] which is enriched over $sSet_{Quillen}$: the category [[sSet]] equipped with its standard [[model structure on simplicial sets]].


This means that a simplicial model category is

* an [[sSet]]-[[enriched category]]

  * which is [[power]]ed and [[copower]]ed over [[sSet]]

* with the structure of a [[model category]] on the underlying category $C_0$

* such that for every cofibration $i : A \to B$ and every fibration $p : X \to Y$ in $C_0$ the morphism of [[simplicial set]]s $C(B,X) \stackrel{i^* \times p_*}{\to} C(A,X) \times_{C(A,Y)} C(B,Y)$ is a fibration;

* and such that this fibration is an acyclic fibration whenever either $i$ or $p$ are acyclic.

## Properties

### Enrichment, tensoring, and cotensoring 
 {#EnrichmentTensoringCotensoring}

Let $\mathcal{C}$ be a category equipped with the structure of a [[model category]] and with that of an [[sSet]]-[[enriched category]] with is [[tensoring|tensored]] and [[cotensoring|cotensored]] over [[sSet]].

+-- {: .num_prop #EquivalenceOfConditions}
###### Proposition

The following condition that each make $\mathcal{C}$ into a _simplicial model category_ are equivalent

1. the [[tensoring]] $\otimes : \mathcal{C} \times sSet \to \mathcal{C}$ is a left [[Quillen bifunctor]];

1. for any cofibration $X \to Y$ and fibration $A \to B$ in $\mathcal{C}$, the induced morphism 

   $$
     \mathcal{C}(Y, A) \to \mathcal{C}(X, A) \times_{\mathcal{C}(X,B)} \mathcal{C}(Y,B)
   $$

   is a fibration, and is in addition a weak equivalence if either of the two morphisms is;


1. for any cofibration $X \to Y$ in $sSet$ and fibration $A \to B$ in $\mathcal{C}$, the induced morphism 

   $$
     A^Y \to A^X \times_{B^X} B^Y
   $$

   is a fibration, and is in addition a weak equivalence if either of the two morphisms is.

=--

This follows directly from the defining properties of [[tensoring]] and [[cotensoring]].

We list in the following some implications of these equivalent conditions.

Let $\mathcal{C}$ now be a simplicial model category. 

+-- {: .num_cor}
###### Corollary

If $A \in \mathcal{C}$ is fibrant, and $X \hookrightarrow Y$ is a cofibration in [[sSet]], then 

$$
  X^Y \to X^A
$$

is a fibration in $\mathcal{C}$.

=--

+-- {: .proof}
###### Proof

Apply prop. \ref{EquivalenceOfConditions} to the case
of the cofibration $X \to Y$ and the fibration $A \to *$, where "$*$" denotes the [[terminal object]]. This yields that

$$
  A^Y \to A^X \times_{{*}^X} {*}^Y
$$

is a fibration. But ${*}^Y = {*}^X =  {*}$ and hence the claim follows.

=--

Similarly we have

+-- {: .num_cor}
###### Corollary

If $X \in \mathcal{C}$ is cofibrant and $A \in \mathcal{C}$ is fibrant, then $\mathcal{C}(Y,X)$ is fibrant in [[sSet]], hence is a [[Kan complex]].

=--

+-- {: .proof}
###### Proof

Apply prop. \ref{EquivalenceOfConditions} to the cofibration $\emptyset \to X$, where "$\emptyset$" denotes the [[initial object]], and to the fibration $A \to *$ to find that 

$$
  \mathcal{C}(X, A) \to \mathcal{C}(\emptyset, A) \times_{\mathcal{C}(\emptyset,*)} \mathcal{C}(X,*)
$$

is a fibration. But since $\emptyset$ is initial and $*$ is terminal, all three simplicial sets in the fiber product on the right are the point, hence this is a fibration

$$
  \mathcal{C}(X,A) \to *
  \,.
$$

=--

+-- {: .num_remark}
###### Remark


For $X$ and $A$ any two objects and $Q X $ and $P A$ a cofibrant and fibrant replacement, respectively, $\mathcal{C}(Q X, P A)$ is the correct [[derived hom-space]] between $X$ and $A$. In particular the full $sSet$-enriched [[subcategory]] on cofibrant fibrant objects is therefore an [[simplicially enriched category|sSet-enriched category]] which is fibrant in the [[model structure on simplicially enriched categories]]. Its [[homotopy coherent nerve]] is a [[quasi-category]]. All this are intrinsic incarnatons of the [[(∞,1)-category]] that is [[presentable (∞,1)-category|presented]] by $C$.

=--


## Examples

The category $sSet_{Quillen}$ is a [[monoidal model category]] and is hence naturally enriched, as a model category, over itself. This is the archetypical simplicial model category.

For $C$ any small [[sSet]]-[[enriched category]] and $A$ [[simplicial combinatorial model category]], the [[global model structure on functors]] $[C^{op}, A]_{proj}$ and $[C^{op},A]_{inj}$ are themselved simplicial combinatorial model categories.

The [[Bousfield localization of model categories|left Bousfield localization]] of these at any set of morphisms is again a combinatorial simplicial model category. Large clases of examples arise this way. In particular for $A = sSet_{Quillen}$ itself this yields the [[model structure on simplicial presheaves]].

### Combinatorial simplicial model categories

A particularly important type of simplicial model categories are those that are also [[combinatorial model category|combinatorial model categories]].

A [[combinatorial simplicial model category]] is precisely a _presentation_ for a [[locally presentable (∞,1)-category]]. See there for more details.

## Simplicial Quillen equivalent models {#SimpEquivMods}

While some model categories do not admit an $sSet_{Quillen}$-enrichment, for large classes of model categories one can find an [[Quillen equivalence]] to a model cateory that does have an $sSet_{Quillen}$-enrichment.


+-- {: .num_theorem }
###### Theorem

Every left proper combinatorial model category is Quillen equivalent to a simplicial model category.

More precisely: let $A$ be a 

* [[proper model category|left proper]];

* [[combinatorial model category|combinatorial]] or [[cellular model category|cellular]]

model category. Then the category $sA := [\Delta^{op}, A]$ of [[simplicial object]]s in $A$ carries the structure of a simplicial model category with respect to its canonical $sSet$-enrichment, such that the functor $ev_0 : sA \to A$ that sends a simplicial object to its degree 0 piece exhibits a [[Quillen equivalence]]

$$
  c_* : A \stackrel{\to}{\leftarrow} : ev_0
  \,.
$$

In $sA$ we have

* the weak equivalences are those morphisms that induce weak equivalences in $A$ under [[homotopy colimit]] over $\Delta$;

* the cofibrations are cofibrations in the [[Reedy model structure]] on $[\Delta^{op}, A]$.

* the fibrant objects are precisely the Reedy-fibrant objects all whose face and degenarcy maps are weak equivalences in $A$.

=--

+-- {: .proof}
###### Proof

This is theorem 1.2 of

* [[Dan Dugger]], _Replacing model categories with simplicial ones_ Trans. Amer. Math. Soc. vol. 353 (2001), #12, 5003-5027. ([web](http://www.uoregon.edu/~ddugger/smod.html))

The simplicial enrichment is theorem 6.1

The characterization of the fibrant objects is theorem 5.7.

=--


+-- {: .num_theorem }
###### Theorem


There is a similar model structure on $sA$ where instead the cofibrations are the cofibrations with respect to the  projective [[global model structure on functors]] on $[\Delta^{op}, A]$.

In this the fibrant objects are precisely the simplicial objects that are degreewise fibrant in $A$, and for which all face and degeneracy maps are weak equivalences in $A$. 

The identity functor established a [[Quillen equivalence]] between this model structure and the one discussed above

$$
  s A_{Reedy, loc} \stackrel{\leftarrow}{\to} sA_{proj, loc}
  \,.
$$


=--

+-- {: .proof}
###### Proof


This is theorem 1.3 in the above article.


=--


There is also a version for stable model categories:

+-- {: .num_theorem }
###### Theorem

Every [[proper model category|proper]] [[cofibrantly generated model category|cofibrantly generated]] [[stable model category]] is [[Quillen equivalence|Quillen equivalent]] to a simplicial model category

=--

This is ([RezkSchwedeShipley,prop 1.3](#RezkSchwedeShipley)).



+-- {: .num_theorem }
###### Theorem
**(uniqueness)**

Let $A$ be a [[model category]]. Then there is at most one model category 
structure on $s A = [\Delta^{op}, A]$ such that

* every morphism that is degreewise a weak equivalence in $A$ is a weak equivalence;

* the cofibrations are those of the [[Reedy model structure]];

* the fibrant objects are the Reedy-fibrant objects whose face and
  degeneracy maps are weak equivalences in $A$.

=--


This is ([RezkSchwedeShipley, theorm 3.1](#RezkSchwedeShipley)).



## Warning on terminology

The term _simplicial model category_ for the notion described here is entirely standard, but in itself a bit suboptimal. More properly one would speak of [[simplicially enriched category]], which is different (though not much) from a [[simplicial object]] in [[Cat]]. 

The other caveat is that there are different model category structures on [[sSet]] and hence even the term $sSet$-[[enriched model category]] is ambiguous.

For instance the [[Andre Joyal]]-[[model structure for quasi-categories]] is an $sSet$-enriched model category, but not for the standard Quillen model structure on the enriching category: since $sSet_{Joyal}$ is a closed [[monoidal model category]] it is enriched over itself, hence is a $sSet_{Joyal}$-enriched model category, not an $sSet_{Quillen}$-enriched one. So in the standrt terminology, $sSet_{Joyal}$ is _not_ a "simplicial model category".
 

## References

section 9.1.5 of

* [[Philip Hirschhorn|P. Hirschhorn]],  _Model categories and their localizations_, volume 99 
of Mathematical Surveys and Monographs , American Mathematical Society, 
2009.

* [[Charles Rezk]], [[Stefan Schwede]], [[Brooke Shipley]], _Simplicial structures on model categories and functors_ American Journal of Mathematics, Vol. 123, No. 3 (Jun., 2001), pp. 551-575  ([jstor](http://www.jstor.org/stable/pdfplus/25099071.pdf))
 {#RezkSchwedeShipley}

section A.3 in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects simplicial model categories]]
[[!redirects sSet-model category]]
[[!redirects sSet-model categories]]