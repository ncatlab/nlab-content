
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[1-morphism]] in a [[2-category]] is an [[equivalence]] if there exists another 1-morphism the other way around, such that the two are [[inverses]] of each other up to invertible [[2-morphisms]].  

## Definition

A 1-morphism $f: x \to y$ in a 2-category is called an _equivalence_ if there exists a 1-morphism $g: y \to x$ and invertible 2-morphisms $\eta : 1_y \xrightarrow{\sim} f g$, $\epsilon: g f \xrightarrow{\sim} 1_x$.   

Alternatively, some use _equivalence_ to denote the whole 4-tuple 

$$(f: x \to y, g: y \to x, \eta : 1_y \xrightarrow{\sim} f g, \epsilon: g f \xrightarrow{\sim} 1_x)$$

Then being an equivalence is an extra structure put on a 1-morphism $f: x \to y$ in a 2-category, not merely an extra property.

Such a 4-tuple is called an [[adjoint equivalence]] if it obeys the [[zigzag identities]], and in that case (and only in that case) $\eta$ is called the _unit_ and $\epsilon$ is called the _counit_.  Given an equivalence in a 2-category, it can always be 'improved' to become an adjoint equivalence, simply by redefining $\epsilon$ or $\eta$.  



Equivalences in a 2-category are sometimes also called "1-equivalences", to distinguish them from invertible [[2-morphisms]], which are also called "2-isomorphisms".

## Examples

* An equivalence in a [[1-category]] regarded as a [[2-category]] with only trivial [[2-morphisms]] is just an _[[isomorphism]]_.

* An equivalence in the 2-category [[Cat]] of all [[categories]] is an _[[equivalence of categories]]_.

* An equivalence in the 2-category of [[algebras]] with [[bimodules]] as 1-morphisms and [[intertwiners]] as 2-morphisms (see [here](bimodule#AsMorphismsInA2Category)) is a _[[Morita equivalence]]_.

## Related concepts

* [[homotopy equivalence]]

* [[equivalence in an (infinity,1)-category]]

[[!redirects equivalences in a 2-category]]
[[!redirects equivalences in 2-categories]]

[[!redirects 1-equivalence]]
[[!redirects 1-equivalences]]

