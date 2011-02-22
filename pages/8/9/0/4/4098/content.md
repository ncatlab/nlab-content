
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

An **absolute colimit** is a [[colimit]] which is [[preserved limit|preserved]] by any [[functor]] whatsoever.  In general this happens because the colimit is a colimit for purely "diagrammatic" reasons.

Absolute colimits are also called **Cauchy colimits**.  A [[category]] which admits all absolute colimits (and equivalently, all absolute limits) is called [[Cauchy complete category|Cauchy complete]].

## Examples

In ordinary category theory there are not very many absolute colimits, but we have

* [[absolute coequalizers]] and
* [[split idempotents]].

The latter example is "universal," in that an ordinary category is Cauchy complete iff it has split idempotents, although not every absolute colimit "is" the splitting of an idempotent.

In [[enriched category theory]] there can be more types of absolute colimits.  For instance:

* in [[Ab-enriched categories]], finite [[biproducts]] are absolute.  Finite biproducts and splitting of idempotents together are "universal" absolute colimits for Ab-enrichment.
* in [[SupLat]]-enriched categories, arbitrary small biproducts are absolute, and together with splitting of idempotents these generate all absolute colimits.
* in [[dg-categories]] and [[spectral category|spectral categories]], *shifts/suspensions* are absolute.
* in Lawvere [[metric spaces]], limits of Cauchy sequences are absolute.  This is the origin of the name "Cauchy colimit."

[[!redirects absolute colimits]]
[[!redirects absolute limit]]
[[!redirects absolute limits]]
[[!redirects Cauchy colimit]]
[[!redirects Cauchy colimits]]
