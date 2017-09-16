#Definition#

An **additive category** is a category 

* is an [[Ab-enriched category]]
(sometimes called a [[pre-additive category]]--this means that each [[hom-set]] is an abelian group and composition is bilinear)

* which admits finite [[product]]s (and hence finite [[coproduct]]s).

# Remarks 

* In any Ab-enriched category, any finite product is also a coproduct, and dually.  This includes the zero-ary case: any [[terminal object]] is also an [[initial object], hence a [[zero object]] (and dually).  Such products are sometimes called [[biproduct]]s and sometimes [[direct sum]]s; they are [[Cauchy colimit]]s for Ab-enrichment.  (This does not extend to infinite products and coproducts, or to any other sort of limit.)

* The Ab-enrichment of an additive category does not have to be given a priori.  Any category with finite biproducts is automatically enriched over abelian [[monoid]]s (as described at [[biproduct]]), so an additive category may be defined as a category with finite biproducts whose [[hom-object|hom-monoids]] happen to be [[group]]s.  (The requirement that the hom-monoids be groups can even be stated in elementary terms without discussing enrichment at all, but that\'s not very enlightening.)

+--{: .query}
_Mike_: Can someone fill in the precise conditions on a category that make it additive?  It is easy to see how coincidence of finite products and coproducts makes it enriched over abelian _monoids_, as discussed at [[biproduct]]; is there a natural condition supplying inverses, other than assuming directly that they exist?

_Toby_:  As far as I know, you can\'t do it any more naturally than I\'ve written it just now.  If I were king of the world, then I\'d redefine 'additive category' to mean simply a category with finite biproducts; that the hom-monoids are groups will naturally follow if (as in an abelian category) we have sufficient properties of (co)kernels, but otherwise the general theory works quite well for the monoid-enriched version.
=--

* Some authors use **additive category** to simply mean an Ab-enriched category, with no further assumptions.

* A [[pre-abelian category]] is an additive category which also has [[kernel]]s and [[cokernel]]s.  Equivalently, it is an Ab-enriched category with all finite limits and colimits.  An especially important sort of additive category is an [[abelian category]], which is a pre-abelian one satisfying the extra exactness property that all monos are kernels and all epis are cokernels.  See [[additive and abelian categories]].

* The natural [[morphism]]s *between* additive categories are the [[additive functor]]s.