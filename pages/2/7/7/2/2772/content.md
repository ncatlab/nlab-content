
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}

## Idea ##

The generalization to the context of [[(∞,1)-category]]-theory of the notion of a [[full and faithful functor]] in ordinary [[category theory]].

## Definition ##

An [[(∞,1)-functor]] $F : C \to D$ is **full and faithful** if for all objects $x,y \in C$  it induced an equivalence on the [[hom-object in a quasi-category|hom-∞-groupoids]]

$$
  F_{x,y} : Hom_C(x,y) \stackrel{\simeq}{\to}
   Hom_D(F(x), F(y))
  \,.
$$

A full and faithful $(\infty,1)$-functor $F : C \to D$ exhibits $C$ as a full [[sub-(∞,1)-category]] of $D$ and one tends to write

$$
  F : C \hookrightarrow D
$$

to indicate this.

## Properties

A full and faithful $(\infty,1)$-functor is precisely a [[monomorphism in an (∞,1)-category|monomorphism]] in [[(∞,1)Cat]], hence a [[truncated object in an (∞,1)-category|(-1)-truncated]] morphism.

An [[(∞,1)-functor]] which is both full and faithful as well as an [[essentially surjective (∞,1)-functor]] is an [[equivalence of (∞,1)-categories]].

## Related concepts

* [[full functor]], [[faithful functor]],  [[full and faithful functor]], [[essentially surjective functor]]

* [[essentially surjective (∞,1)-functor]],

* [[equivalence of (∞,1)-categories]]

## References 

This appears as definition 1.2.10 in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects full and faithful (∞,1)-functor]]
[[!redirects full and faithful (∞,1)-functors]]
[[!redirects full and faithful (infinity,1)-functor]]
[[!redirects full and faithful (infinity,1)-functors]]

[[!redirects fully faithful (infinity,1)-functor]]
[[!redirects fully faithful (∞,1)-functor]]
[[!redirects fully faithful (infinity,1)-functors]]
[[!redirects fully faithful (∞,1)-functors]]
