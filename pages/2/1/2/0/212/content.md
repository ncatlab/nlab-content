

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

By _Alg_ is usually meant a [[category]] with [[associative algebras]] as [[objects]] and [[algebra homomorphisms]] as [[morphisms]].

(This depends on a choice of [[ground field]] or even [[ground ring]], which is often left implicit and determined by the context. Over the [[ground ring]] $\mathbb{Z}$ of [[integers]], $Alg_{\mathbb{Z}} \simeq$ [[Ring]] is the category of [[rings]].)

Beware that many other types of algebras exist besides [[associative algebras]] (e.g. [[Lie algebras]] or generally [[algebras over an operad]] or [[algebras over a monad]]) and all of them form categories which may in corresponding contexts be denoted "$Alg$" or similar.



## Properties

### Relation with Bimod

Since [[associative algebras]] may be identified with one-object [[categories]] [[enriched category|enriched]] in [[modules]] over the [[ground ring]]), it is sometimes useful to regard $Alg$ as the [[strict 2-category|strict]] [[full sub-2-category]] of the [[2-category]] [[VCat|$Mod Cat$]] of [[Mod]]-[[enriched categories]]. In this case the [[2-morphisms]] between morphisms of algebras come from "[[intertwiners]]": inner [[endomorphisms]] of the [[codomain]] algebra. 

(Analogous statements hold for the category [[Grp]] of groups when the latter are regarded as their [[delooping groupoids]].)

With $Alg$ regarded as a strict 2-category this way there is a canonical 2-functor 

$$
  Alg \hookrightarrow Bimod
$$

to the category [[Bimod]] of [[bimodules]], which sends algebra homomorphisms $f : A \to B$ to the $A$-$B$ bimodule ${}_f B$.  This exhibits $Bimod$ as a [[framed bicategory]] in the sense of Shulman.

## Related concepts

* [[Vect]]

* [[Mod]], [[2Mod]], [[nMod]]

* [[dgcAlg]]

* [[Eilenberg-Moore category]]

category: category

[[!redirects Algebras]]

[[!redirects category of algebras]]
[[!redirects categories of algebras]]
