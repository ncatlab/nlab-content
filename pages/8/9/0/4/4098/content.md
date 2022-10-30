
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

An **absolute colimit** is a [[colimit]] which is [[preserved limit|preserved]] by any [[functor]] whatsoever.  In general this happens because the colimit is a colimit for purely "diagrammatic" reasons.  The notion is most important in [[enriched category theory]].

Absolute colimits are also called **Cauchy colimits**.  A [[category]] which admits all absolute colimits (and equivalently, all absolute limits) is called [[Cauchy complete category|Cauchy complete]].

## Characterizations

Let $V$ be a B&#233;nabou [[cosmos]] and $J\colon K &#8696; A$ a $V$-[[profunctor]].  Then the following are equivalent:

* $J$-[[weighted limit|weighted]] colimits are absolute (i.e. preserved by all $V$-functors)

* $J$ has a [[right adjoint]] $J^*$ in the [[bicategory]] $V$-[[Prof]].

* There is a weight $J^*\colon A &#8696; K$ such that $J$-weighted colimits coincide naturally with $J^*$-weighted limits.

## Examples

In ordinary category theory there are not very many absolute colimits, but we have

* [[absolute coequalizers]] and
* [[split idempotents]].

The latter example is "universal," in that an ordinary category is Cauchy complete iff it has split idempotents, although not every absolute colimit "is" the splitting of an idempotent.  More precisely, the class of absolute $Set$-limits is the [[saturated class of limits|saturation]] of idempotent-splittings.

In [[enriched category theory]] there can be more types of absolute colimits.  For instance:

* in categories with [[zero morphisms]] (that is, enriched over [[pointed sets]]), [[initial objects]] are absolute.

* in [[Ab-enriched categories]] (or, more generally, categories enriched over commutative [[monoids]]), finite [[biproducts]] are absolute.  Finite biproducts and splitting of idempotents together are "universal" absolute colimits for Ab-enrichment.

* in [[SupLat]]-enriched categories, arbitrary small biproducts are absolute, and together with splitting of idempotents these generate all absolute colimits.

* in [[dg-categories]] (or more generally, categories enriched over [[graded set|graded sets]]), *shifts/suspensions* are absolute.

* in Lawvere [[metric spaces]], limits of Cauchy sequences are absolute.  This is the origin of the name "Cauchy colimit."

* in categories [[bicategory-enriched category|enriched]] over the [[bicategory]] (or [[double category]]) of relations in a [[site]], *gluings* are absolute.  In this case the enriched categories can roughly be identified with [[separated presheaves]] and the Cauchy-complete ones with [[sheaves]].

* in categories enriched over [[rational number|rational]] [[vector spaces]], quotients by finite [[group actions]] are absolute.

New kinds of absolute (co)limits also arise in [[higher category theory]].

* for [[(∞,1)-categories]], splitting of idempotents is a universal absolute colimit.

* in [[stable (∞,1)-categories]] (which are enriched, in the $(\infty,1)$-categorical sense, over the $(\infty,1)$-category of [[spectra]]), initial objects and [[pushouts]] are absolute, and therefore so are all finite colimits.

## References

* [[Ross Street]], *Absolute colimits in enriched categories*, [Cahiers 1983](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1983__24_4_377_0)

[[!redirects absolute colimits]]
[[!redirects absolute limit]]
[[!redirects absolute limits]]
[[!redirects Cauchy colimit]]
[[!redirects Cauchy colimits]]
