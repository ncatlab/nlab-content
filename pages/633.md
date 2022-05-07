
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc} 

## Definition

Let $K$ be a [[2-category]].

A [[morphism]] $f:A\to B$ in $K$ is called **(representably) fully-faithful** (or sometimes just **ff**) if for all [[object]]s $X \in K$ , the [[functor]]
$$K(X,A) \to K(X,B)$$
is [[full and faithful functor|full and faithful]].  


## Remarks

* Fully faithful morphisms in a 2-category may also be called **1-monic**, and be said to make their source into a **1-subobject** of their target.  See [[subcategory]] for some discussion.

* Fully faithful morphisms are often the right class of a [[factorization system in a 2-category|factorization system]].  The left class in $Cat$ consists of [[essentially surjective functors]]; in a [[regular 2-category]] it consists of the [[eso morphisms]].

* Just as in a 1-category any [[equalizer]] is [[monic]], in a 2-category any [[inverter]] or [[equifier]] is fully faithful.

## Variations

This is not always the "right" notion of fully-faithfulness in a 2-category.  In particular, in [[enriched category theory]] this definition does not recapture the correct notion of enriched fully-faithfulness.  It is possible, however, to characterize $V$-fully-faithful functors 2-categorically; see [[codiscrete cofibration]]. In general, fully faithful morphisms should be defined with respect to a [[proarrow equipment]]: in particular, this recovers $V$-fully-faithfulness. A 1-cell $f : A \to B$ in a proarrow equipment is **fully faithful** if the [[unit of an adjunction|unit of the adjunction]] $\eta \colon 1 \to f^* f_*$ is invertible.

## Examples

In the [[2-category]] [[Cat]] the full and faithful morphisms are precisely the [[full and faithful functor]]s.



## Related pages

* [[subcategory]]
* [[faithful morphism]]
* [[conservative morphism]]
* [[pseudomonic morphism]]
* [[discrete morphism]]
* [[eso morphism]]

[[!redirects ff morphism]]
[[!redirects ff morphisms]]
[[!redirects fully faithful morphism]]
[[!redirects fully faithful morphisms]]
[[!redirects representably fully faithful morphism]]
[[!redirects representably fully faithful morphisms]]
[[!redirects 1-monic morphism]]
[[!redirects 1-monic morphisms]]
[[!redirects 1-subobject]]
[[!redirects 1-subobjects]]
