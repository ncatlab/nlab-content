
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

An __adjoint triple__ of functors $F\dashv G\dashv H$, is a triple of [[functor]]s $(F,G,H)$ together with [[adjunction]] data $F\dashv G$ and $G\dashv H$. 

The two adjunctions imply of course that $G$ preserves all small [[limit]]s and [[colimit]]s. Then also the [[monad]] $G F$ has a [[right adjoint]] and the comonad $G H$ has a [[left adjoint]]. In general there is a duality (an anti[[equivalence of categories]]) between the category of monads having right adjoint and comonads having left adjoints.  

For an adjoint triple $F\dashv G\dashv H$ it is known that $F$ is fully faithful iff
$H$ is fully faithful. 

## Example

Example. Given any ring homomorphism $f^\circ: R\to S$ (in commutative case dual to s an affine morphism $f: Spec S\to Spec R$ of affine schemes), there is an adjoint triple $f^*\dashv f_*\dashv f^*$ where $f^*: {}_R Mod\to {}_S Mod$ is an extension of scalars, $f_*: {}_S Mod\to {}_R Mod$ the restriction of scalars and $f^! : M\mapsto Hom_R ({}_R S, {}_R M)$ its right adjoint. 

## Related concepts

* [[adjoint quadruple]], [[cohesive topos]]

* [[affine morphism]], [[affine localization]] 


[[!redirects adjoint triples]]
