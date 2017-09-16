#Definition#

An **additive category** is a category 

* is an [[Ab-enriched category]]
(sometimes called a [[pre-additive category]]--this means that each [[hom-set]] is an abelian group and composition is bilinear)

* which admits finite [[product]]s (and hence finite [[coproduct]]s).

# Remarks 

* In any Ab-enriched category, any finite product is also a coproduct, and dually.  This includes the zero-ary case: any [[terminal object]] is also an [[initial object], hence a [[zero object]] (and dually).  Such products are sometimes called [[biproduct]]s and sometimes [[direct sum]]s; they are [[Cauchy colimit]]s for Ab-enrichment.  (This does not extend to infinite products and coproducts, or to any other sort of limit.)

* The Ab-enrichment of an additive category does not have to be given a priori: it can be recovered uniquely from the behavior of limits and colimits (in particular, the coincidence of finite products and coproducts) in the underlying ordinary category.

+--{: .query}
_Mike_: Can someone fill in the precise conditions on a category that make it additive?  It is easy to see how coincidence of finite products and coproducts makes it enriched over abelian _monoids_, as discussed at [[biproduct]]; is there a natural condition supplying inverses, other than assuming directly that they exist?
=--

* Some authors use **additive category** to simply mean an Ab-enriched category, with no further assumptions.

* A [[pre-abelian category]] is an additive category which also has [[kernel]]s and [[cokernel]]s.  Equivalently, it is an Ab-enriched category with all finite limits and colimits.  An especially important sort of additive category is an [[abelian category]], which is a pre-abelian one satisfying the extra exactness property that all monos are kernels and all epis are cokernels.  See [[additive and abelian categories]].
