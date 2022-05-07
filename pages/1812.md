
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A **cosmos** is a "good place in which to do category theory," including both ordinary [[category theory]] as well as [[enriched category]] theory.

The word is chosen by analogy with [[topos]] which can be regarded as "a good place to do set theory," but there are notable differences between the two situations; a more direct [[vertical categorification|categorification]] of a topos is, unsurprisingly, a [[2-topos]].  In contrast, cosmoi also include [[enriched category]] theory, while toposes do not allow non-[[cartesian monoidal category|cartesian]] enrichment.

There are a number of different, inequivalent, definitions of "cosmos" in the literature.

## Bénabou cosmoi

A [[Bénabou cosmos]] (see [Street 74, p. 1](#Street74)) is a [[complete category|complete]] and [[cocomplete category|cocomplete]] (hence [[bicomplete category|bicomplete]]) [[closed monoidal category|closed]] [[symmetric monoidal category]].  

This is the ideal situation for for $V$-[[enriched category theory]].


## Indexed Bénabou cosmoi

[Shulman 2013](#Shulman13) introduced an [[indexed category|indexed]] generalization of [[Bénabou cosmoi]], appropriate for studying enriched [[indexed categories]] over a base category.  Notably, while the definition of [[Bénabou cosmoi]] is not "[[elementary topos|elementary]]" (it involves infinitary (non-[[finite limit|finite]]) [[limits]] and [[colimits]]), the indexed version is elementary; the infinitary structure is folded into the indexing base category.  The notion of [[Bénabou cosmoi]] is recovered as particular cosmoi indexed over [[Set]].


## Street's "fibrational cosmoi"

[[Ross Street]] has taken a different tack, defining a "cosmos" to be the collection of (enriched) categories and relevant structure for doing category theory, rather than the "base" category $V$ over which the enrichment occurs.

In his paper "Elementary cosmoi," Street defined a **(fibrational) cosmos** to be a 2-category in which internal [[Grothendieck fibrations|fibrations]] are well-behaved and representable by a structure of "presheaf objects" (later realized to be a special sort of [[Yoneda structure]]).  Note that while this includes $Cat$, it does *not* include $V$-$Cat$ for non-cartesian $V$, since internal fibrations are poorly behaved there. The definition is given in the paper "Cosmoi of internal categories": a fibrational cosmos is a 2-category $K$ such that

* finite limits exist in $K$;
* there is a 2-adjunction $P^* : K \leftrightarrows K^{\text{coop}} : P$;
* each object $A$ admits a discrete fibration from $PA$ satisfying two technical properties. 

The objects $PA$ are the "presheaf objects" that represent fibrations.

## Street's second definition

In his paper "Cauchy characterization of enriched categories," Street instead defined a cosmos to be a [[2-category]] that "behaves like the 2-category $V$-$Mod$ of enriched categories and [[profunctors]]".  The precise definition: a cosmos is a 2-category (or [[bicategory]]) such that:

* Small ([[2-limit|weak, or bi-]]) [[coproduct]]s exist.
* Each [[monad]] admits a [[Kleisli construction]] (analogous to the [[exact category|exactness]] of a topos).

* It is locally small-[[cocomplete category|cocomplete]], i.e. its hom-categories have small colimits that are preserved by composition on each side.

* There exists a small "Cauchy generator".

These hypotheses imply that it is equivalent to the bicategory of categories and [[profunctors]] [[enriched category|enriched]] over some "base" *bicategory*.  (Note the generalization from enrichment over a monoidal category to enrichment over a bicategory.)

Defined in this way, cosmoi are closed under [[opposite category|dualization]], parametrization and [[localization]], suitably defined.

## Related notions

* An [[infinity-cosmos]] is a "good place in which to do higher category theory" as axiomatized by Riehl and Verity in their work on the foundations of $(\infty,1)$- and $(\infty,n)$-category theory.

## Bibliography

Apparently there is no written account by [[Jean Bénabou]] of his definition of cosmos. One finds it recounted in [Street 74, p. 1](#Street74):

> to J. Benabou the word means "bicomplete symmetric monoidal category", such categories $\mathcal{V}$ being rich enough so that the theory of categories enriched in  $\mathcal{V}$ develops to a large extent just as the theory of ordinary categories.

* {#Street74} [[Ross Street]],  _Elementary cosmoi I.  *Category Seminar*. Springer, Berlin, Heidelberg, 1974. ([doi:10.1007%2FBFb0063103](https://link.springer.com/chapter/10.1007%2FBFb0063103))

* [[Ross Street]],  _Cosmoi of internal categories_, Transactions of the American Mathematical Society 258.2 (1980): 271-318.

* [[Ross Street]], _Cauchy characterization of enriched categories_, Rend. Sem. Mat. Fis. Milano 51 (1981): 217-233. ([pdf](http://emis.ams.org/journals/TAC/reprints/articles/4/tr4.pdf))

* {#Shulman13} [[Mike Shulman]], *Enriched indexed categories*, Theory and Applications of Categories, **28** 21 (2013) 616-695 ([tac:28-21](http://www.tac.mta.ca/tac/volumes/28/21/28-21abs.html)) 
 


[[!redirects cosmoi]]


