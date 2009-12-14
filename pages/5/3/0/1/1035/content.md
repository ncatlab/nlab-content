#Definition#

An **additive category** is

* an [[Ab-enriched category]]
(sometimes called a [[pre-additive category]]--this means that each [[hom-set]] is an abelian group and composition is bilinear)

* which admits finite [[products]] (and hence finite [[coproducts]]).

# Remarks 

* In any Ab-enriched category, any finite product is also a coproduct, and dually.  This includes the zero-ary case: any [[terminal object]] is also an [[initial object], hence a [[zero object]] (and dually).  Such products are sometimes called [[biproducts]] and sometimes [[direct sums]]; they are [[absolute limit|absolute limits]] for Ab-enrichment.  (This does not extend to infinite products and coproducts.)  In fact, an Ab-enriched category is [[Cauchy complete category|Cauchy complete]] just when it is additive and moreover its [[idempotents]] split.

* A [[pre-abelian category]] is an additive category which also has [[kernels]] and [[cokernels]].  Equivalently, it is an Ab-enriched category with all finite limits and colimits.  An especially important sort of additive category is an [[abelian category]], which is a pre-abelian one satisfying the extra exactness property that all monos are kernels and all epis are cokernels.  See [[additive and abelian categories]].

* The Ab-enrichment of an additive category does not have to be given a priori.  Any category with finite biproducts is automatically enriched over abelian [[monoids]] (as described at [[biproduct]]), so an additive category may be defined as a category with finite biproducts whose [[hom-object|hom-monoids]] happen to be [[groups]].  (The requirement that the hom-monoids be groups can even be stated in elementary terms without discussing enrichment at all, but to do so is not very enlightening.)  Note that the entire $Ab$-enriched structure follows automatically for [[abelian category|abelian categories]].

* Some authors use **additive category** to simply mean an Ab-enriched category, with no further assumptions.

* The natural [[morphisms]] *between* additive categories are the [[additive functors]].


[[!redirects additive categories]]