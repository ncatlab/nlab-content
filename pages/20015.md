
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


# Categories with arities

* table of contents
{:toc}

## Idea

A *category with arities* is a category equipped with a "small presentation" of its objects.

## Definition

A **category with arities** is a [[locally small category]] $\mathcal{E}$ equipped with a [[small category|small]] [[full subcategory]] $\mathcal{A} \subseteq \mathcal{E}$ which is [[dense subcategory|dense]], in the sense that the [[restricted Yoneda embedding]] $\mathcal{E} \to [\mathcal{A}^{op},Set]$ is [[fully faithful]].

A **functor with arities** or **arity-respecting functor** $F : (\mathcal{E},\mathcal{A}) \to (\mathcal{F},\mathcal{B})$ is a functor $F:\mathcal{E}\to\mathcal{F}$ such that the composite $\mathcal{E} \xrightarrow{F} \mathcal{F} \to [\mathcal{B}^{op},Set]$ preserves the density colimits for $\mathcal{A}$ in $\mathcal{E}$, i.e. such that for any $X\in\mathcal{E}$ and $B\in\mathcal{B}$ the canonical map $\colim^{A\in \mathcal{A} \atop A \to X} \mathcal{F}(B,F A) \to \mathcal{E}(B,F X)$ is an isomorphism of sets.

A **natural transformation with arities** is just an ordinary natural transformation between functors with arities.

This defines the 2-category of categories with arities.  Note that since a natural transformation with arities is determined by its action on the generating objects $\mathcal{A}$, there is only a small set of natural transformations between any two functors with arities.  Thus, even though the 2-category of categories with arities is "very large", its hom-categories are locally small.


## Related pages

* A monad in the 2-category of categories with arities is a [[monad with arities]].  In [BMW](#BMW) it is claimed that the nerve theorem for monads with arities constructs an [[Eilenberg-Moore object]] in this 2-category.

## References

* {#BMW} [[Clemens Berger]], [[Paul-André Melliès]], [[Mark Weber]], _Monads with Arities and their Associated Theories_ (2011) ([arXiv:1101.3064](http://arxiv.org/abs/1101.3064))

[[!redirects categories with arities]]
[[!redirects functor with arities]]
[[!redirects functors with arities]]
[[!redirects arity-respecting functor]]
[[!redirects arity-respecting functors]]
