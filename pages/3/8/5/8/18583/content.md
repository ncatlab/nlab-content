
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


* table of contents
{: toc}


## Idea
 {#Idea}


__$Inj$__ (or __$Set_inj$__) is the [[wide subcategory]] of the [[topos]] [[Set]] with its [[morphisms]] restricted to [[monomorphisms]] ([[injective functions]]).

*  The [[arrow category]] $Inj^\to$ of $Inj$ is, in turn, a [[wide subcategory]] of the [quasitopos](quasitopos#mono) [[M-category#mono|Mono]] of set monomorphisms.  The two categories have the same objects, namely injective functions, but in [[Mono]] the morphism are arbitrary commutative squares from one injection to another, whereas in $Inj^\to$ the other two arrows in the commutative square must also be injective.  Note that $Mono$ is a [[reflective subcategory]] of the [[category of presheaves|presheaf topos]] $Set^{\to}$ (the [[Sierpinski topos]]), and the category of [[separated presheaves]] for the [[double negation#topology|double negation topology]] on $Set^\to$.

* For a set $S$, its [[power set]] ($\mathcal{P}S$ or $2^S$) is the [[slice category]] $Inj/S$ which has  objects that are injections to $S$ and morphisms that are injections of injections that form commuting triangles.  $2^S$ is a
quasitopos because it is a  [[Heyting algebra]].

## Related concepts

* [[Surj]]
