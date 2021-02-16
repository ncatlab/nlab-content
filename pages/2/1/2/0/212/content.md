

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

_Alg_ is the [[category]] with [[algebra|algebras]] as [[object|objects]] and algebra homomorphisms as [[morphism]]s.

More abstractly, we can think of $Alg$ as the [[category|full subcategory]] of $Cat(Vect)$, [[internal category|internal categories]] in [[Vect]], with algebras as objects.

In case of [[Ab]], this gives us Category of Rings, namely, $Alg_Z$.

## Properties

### Relation to algebras with bimodules

Since algebras may be identified with one-object [[category|categories]] [[internalization|internal to]] vector spaces, it is sometimes useful to regard $Alg$ as a strict 2-category, namely as a full sub-2-category of the 2-category $Cat(Vect)$. In this case the 2-morphisms between morphisms of algebras come from "intertwiners": inner endomorphisms of the target algebra.

Precisely analogous statements hold for the category [[Grp]] of groups.

With $Alg$ regarded as a strict 2-category this way there is a canonical 2-functor 

$$
  Alg \hookrightarrow Bimod
$$

to the category [[Bimod]], which sends algebra homomorphisms $f : A \to B$ to the $A$-$B$ bimodule ${}_f B$.  This exhibits $Bimod$ as a [[framed bicategory]] in the sense of Shulman.

## Related concepts

* [[Vect]]

* [[Mod]], [[2Mod]], [[nMod]]

* [[dgcAlg]]

* [[Eilenberg-Moore category]]

category: category

[[!redirects Algebras]]

[[!redirects category of algebras]]
[[!redirects categories of algebras]]
