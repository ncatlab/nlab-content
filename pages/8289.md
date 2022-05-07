
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}


## Disambiguation

This article is about functors of two variables.  Possibly the term 'bifunctor' has been used for a [[functor]] between [[bicategories]] (citation?), but such usage (if it exists) seems to be rare; the usual term for that is _'[[pseudo functor]]'_.[^fine] 

## Definition

A **bifunctor** (short for __binary functor__, that is $2$-ary) or **functor of two variables** is simply a _[[functor]]_ whose [[domain]] is the [[product]] of two [[categories]].

For $C_1$, $C_2$ and $D$ [[categories]], a functor

$$
  F : C_1 \times C_2 \to D
$$

is also called a _bifunctor_ from $C_1$ and $C_2$ to $D$.


## Examples

Famous bifunctors are 

* the [[hom functor]]

  $$
    Hom(-,-) : C^{op} \times C \to Set
  $$

  on any [[locally small category]] $C$, or if $C$ is a [[closed category]], the [[internal hom]] functor

  $$
    [-,-] : C^{op} \times C \to C
    \,.
  $$

* on every [[monoidal category]] $(C, \otimes)$ the [[tensor product]] functor

  $$
    \otimes : C \times C \to C
  $$


## Related concepts

* [[binary function]], [[bilinear map]], [[multilinear map]]

* [[binary morphism]]

* **bifunctor**, [[two-variable adjunction]], [[Quillen bifunctor]] 

  [[end]]/[[coend]]

[^fine]: Outside of certain computer science contexts, it is not clear that the term 'bifunctor' is used frequently nowadays, even for the sense of a functor of two variables. It is used more frequently in older texts. 

[[!redirects bifunctor]]
[[!redirects bifunctors]]
[[!redirects binary functor]]
[[!redirects binary functors]]
[[!redirects 2-ary functor]]
[[!redirects 2-ary functors]]
[[!redirects functor of two variables]]
[[!redirects functors of two variables]]
[[!redirects functor of 2 variables]]
[[!redirects functors of 2 variables]]
