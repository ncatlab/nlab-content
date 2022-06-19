+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A **modelizer** is a presentation of the [[(infinity,1)-category|(∞,1)-category]] of [[infinity-groupoid|∞-groupoids]], or at least, the [[homotopy category]] thereof. 

## Definition

A **modelizer** is a [[category]] $M$ and a subcategory $W$ satisfying these conditions:
* $(M, W)$ is a saturated [[homotopical category]], meaning $W$ is precisely the class of morphisms in $M$ that become invertible in the [[localization]] $M [W^{-1}]$.
* $M [W^{-1}]$ is [[equivalence of categories|equivalent]] to the category of weak [[homotopy types]], i.e. [[Ho(Top)]] (with respect to [[weak homotopy equivalences]]).

More precisely, it is a category $M$ equipped with a functor $\pi : M \to Ho(Top)$ such that, for $W$ the class of morphisms inverted by $\pi$, the induced functor $M [W^{-1}] \to Ho(Top)$ is an equivalence of categories.

A **morphism of modelizers** $(M, W) \to (M', W')$ is a functor $F : M \to M'$ such that:
* $F$ sends morphisms in $W$ to morphisms in $W'$.
* The functor $M [W^{-1}] \to M' [W'^{-1}]$ so induced is an equivalence of categories.
* The composite $M \overset{F}{\to} M' \overset{\pi}{\to} Ho(Top)$ is isomorphic to $M \overset{\pi}{\to} Ho(Top)$.

An **elementary modelizer** is a modelizer whose underlying category is the [[category of presheaves]] on a [[test category]], with the weak equivalences the ones described at the linked page.

## Examples

The main examples turn out to be [[model categories]]:

* Tautologically, [[Top]] (with weak homotopy equivalences) is a modelizer. This extends to a [[model structure on topological spaces]].
* Quillen showed that there is a [[model structure on simplicial sets]] that is [[Quillen equivalence|Quillen-equivalent]] to the previous one; in particular, $sSet$ (with weak homotopy equivaleces) is a modelizer.
* Thomason showed that [[Cat]] (with nerve equivalences) is a modelizer by exhibiting a [[Thomason model structure|model structure]] Quillen-equivalent to the on $sSet$.

## Cisinski's theorem

+-- {: .num_theorem}
###### Theorem (Cisinski)

If $A$ is a test category, then there exists a [[model structure on presheaves over a test category|model structure]] on $[A^{op}, Set]$ that is Quillen-equivalent to the standard model structure on $sSet$.

=--

## Related concepts

* [[category with weak equivalences]]

* [[localizer]]

## References

* [[Alexander Grothendieck|Grothendieck, A.]] (1983) [[Pursuing stacks]], &#167;28.
* [[Denis-Charles Cisinski|Cisinski, D.-C.]] (2002, 2006) _Les pr&#233;faisceaux comme mod&#232;les des types d'homotopie_.

[[!redirects modelizers]]