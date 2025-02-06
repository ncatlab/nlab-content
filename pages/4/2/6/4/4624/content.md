
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given any [[object]] $X$ in any [[category]] $C$, the [[subobjects]] of $X$ form a [[poset]] (though in general it may be a [[large category|large]] one, i.e. a partially ordered [[proper class]]; cf. [[well-powered category]]). This is called, naturally enough, the __poset of subobjects__ of $X$, or the __subobject poset__ of $X$.

Sometimes it is the __poset of [[regular subobjects]]__ that really matters (although these are the same in any ([[pretopos|pre]])[[topos]]).

## Properties

If $C$ is [[finitely complete category|finitely complete]], then the subobjects form a meet-[[semilattice]], so we may speak of the __semilattice of subobjects__.  

In any [[coherent category]] (such as a [[pretopos]]), the subobjects form a distributive [[lattice]], so we may speak of the __lattice of subobjects__.  

In any [[Heyting category]] (such as an [[elementary topos]]), the subobjects of $X$ form a [[Heyting algebra]], so we may speak of the __algebra of subobjects__.  

In any [[geometric category]] (such as a [[Grothendieck topos]]), the subobjects of $X$ form a [[frame]], so we may speak of the __frame of subobjects__.  

The reader can probably think of other variations on this theme.

If $f : X \to Y$ is a morphism that has pullbacks along monomorphisms, then pullback along $f$ induces a poset morphism $f^* : Sub(Y) \to Sub(X)$, called the **[[preimage]]** or **[[inverse image]]**. This is functorial in the sense that if $g : Y \to Z$ also has this property, then $f^* \circ g^* = (g \circ f)^*$.

If $C$ has pullbacks of monomorphisms, $Sub$ is often used to denote the contravariant functor $C^{op} \to Poset$ whose action on morphisms is $Sub(f) = f^*$.

## Relation to the preorder of monomorphisms

The *poset* of [[subobjects]] $Sub(X)$ is the posetal reflection of the [[preorder]] $Mono(X)$ of [[monomorphisms]] into $X$. 

If one opts for the alternative[^1] definition that subobjects _are_ monomorphisms into the object (not isomorphism classes thereof), then the reflection quotient map $Mono(X) \to Sub(X)$ is an [[equivalence]]. 

[^1]: Discussions of this can be found in [A.1.3](#Johnstone) of Johnstone's Elephant, and also [this MO discussion](#MO). 

## Subobject poset functor and relation to hyperdoctrines

* Every [[category]] with pullbacks of monomorphisms has a contravariant functor $\mathrm{Sub}:C^\op \to Pos$ to the category of [[posets]] called the **subobject poset functor**, making it into a [[hyperdoctrine]]. 

* Every [[finitely complete category]] has a subobject poset functor $\mathrm{Sub}:C^\op \to SemiLat$ to the category of [[semilattices]]. 

* Every [[regular category]] $C$ is a [[regular hyperdoctrine]] induced by the subobject poset functor, where the subobject poset functor has codomain the [[subcategory]] of [[infimum]]-[[semilattices]] $\mathrm{Sub}:C^\op \to InfSemiLat$. 

* Every [[coherent category]] $C$ is a [[coherent hyperdoctrine]] induced by the subobject poset functor, where the subobject poset functor has codomain the [[subcategory]] of [[distributive lattices]] $\mathrm{Sub}:C^\op \to DistLat$. 

* Every [[geometric category]] $C$ is a [[geometric hyperdoctrine]] induced by the subobject poset functor, where the subobject poset functor has codomain the [[subcategory]] of [[frames]] $\mathrm{Sub}:C^\op \to Frm$. 

* Every [[Heyting category]] $C$ is a [[first-order hyperdoctrine]] induced by the subobject poset functor, where the subobject poset functor has codomain the [[subcategory]] of [[Heyting algebras]] $\mathrm{Sub}:C^\op \to HeytAlg$. 

* Every [[Boolean category]] $C$ is a [[Boolean hyperdoctrine]] induced by the subobject poset functor, where the subobject poset functor has codomain the [[subcategory]] of [[Boolean algebras]] $\mathrm{Sub}:C^\op \to BoolAlg$. 

## Related concepts

* [[subobject]]

* [[lattice of subgroups]] 

* [[well-powered category]] 

* [[(n+1,1)-category of n-truncated objects]]

## References

* {#Johnstone}  [[Elephant]] 

* {#MO} Martin Brandenburg, _Concise definition of subobjects_ ([mathoverflow:184196](https://mathoverflow.net/q/184196))




[[!redirects groupoid of subobjects]]

[[!redirects category of subobjects]]
[[!redirects categories of subobjects]]
[[!redirects subobject category]]
[[!redirects subobject categoriess]]

[[!redirects preorder of subobjects]]
[[!redirects preorders of subobjects]]
[[!redirects subobject preorder]]
[[!redirects subobject preorders]]

[[!redirects proset of subobjects]]
[[!redirects prosets of subobjects]]
[[!redirects subobject proset]]
[[!redirects subobject prosets]]

[[!redirects poset of subobjects]]
[[!redirects posets of subobjects]]
[[!redirects subobject poset]]
[[!redirects subobject posets]]

[[!redirects semilattice of subobjects]]
[[!redirects semilattices of subobjects]]
[[!redirects subobject semilattice]]
[[!redirects subobject semilattices]]

[[!redirects lattice of subobjects]]
[[!redirects lattices of subobjects]]
[[!redirects subobject lattice]]
[[!redirects subobject lattices]]

[[!redirects algebra of subobjects]]
[[!redirects algebras of subobjects]]
[[!redirects subobject algebra]]
[[!redirects subobject algebras]]

[[!redirects frame of subobjects]]
[[!redirects frame of subobjects]]
[[!redirects subobject frame]]
[[!redirects subobject frame]]
