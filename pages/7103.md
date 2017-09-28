
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Finite $(\infty,1)$-limits
* table of contents
{: toc}

## Definition

A **finite $(\infty,1)$-limit** is an [[(∞,1)-limit]] over a finitely presented [[(∞,1)-category]] -- a [[finite (∞,1)-category]].

If we model our (∞,1)-categories by [[quasicategories]], then this can be made precise by saying it is a limit over some [[simplicial set]] with finitely many nondegenerate [[simplices]].  Note that such a simplicial set is rarely itself a quasicategory; we regard it instead as a finite presentation of a quasicategory.

## Properties

### Preservation of finite $(\infty,1)$-limits
 {#Preservation}

+-- {: .num_prop}
###### Proposition

An [[(∞,1)-functor]] $F : C \to D$ out of an [[(∞,1)-category]] $C$ that has all finite $(\infty,1)$-limits preserves these finite $(\infty,1)$-limits as soon as it preserves [[(∞,1)-pullbacks]] and the [[terminal object]].

=--

This appears as ([Lurie, cor. 4.4.2.5](#Lurie)).

+-- {: .num_prop #PreservationOutOfPresheaves}
###### Proposition

Let $C$ be a [[small (∞,1)-category]] with finite $(\infty,1)$-limits, and $\mathbf{H}$ an [[(∞,1)-topos]]. Write $PSh(C)$ for the [[(∞,1)-category of (∞,1)-presheaves]] on $C$. 

If a functor $F : PSh_\infty(C) \to \mathbf{H}$ preserves [[(∞,1)-colimits]] and finite $(\infty,1)$-limits of [[representable functor|representables]], then it preserves all finite $(\infty,1)$-limits.

=--

This appears as ([Lurie, prop. 6.1.5.2](#Lurie)).

## Examples

* Binary products, pullbacks, and terminal objects are all finite $(\infty,1)$-limits.

* Unlike the case in [[1-category]] theory, the [[split idempotent|splitting of idempotents]] is *not* a finite $(\infty,1)$-limit.

## Related pages

* [[finite limit]]
* [[(∞,1)-limit]]


## References

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_


Relation to [[homotopy type theory]]:

* [[Chris Kapulkin]], [[Karol Szumiło]], _Internal Language of Finitely Complete $(\infty,1)$-categories_ ([arXiv:1709.09519](https://arxiv.org/abs/1709.09519))


[[!redirects finite (infinity,1)-limit]]
[[!redirects finite (infinity,1)-limits]]
[[!redirects finite (∞,1)-limit]]
[[!redirects finite (∞,1)-limits]]
[[!redirects finite (infinity,1)-colimit]]
[[!redirects finite (infinity,1)-colimits]]
[[!redirects finite (∞,1)-colimit]]
[[!redirects finite (∞,1)-colimits]]
