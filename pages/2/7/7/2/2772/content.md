
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
* automatic table of contents goes here
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

## References ##

This appears as definition 1.2.10 in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects full and faithful (∞,1)-functor]]
[[!redirects fully faithful (infinity,1)-fu
nctor]]
[[!redirects fully faithful (∞,1)-functor]]