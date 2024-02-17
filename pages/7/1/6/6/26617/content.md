
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

__$Field$__ is the [[category]] with [[field|fields]] as [[objects]] and [[field homomorphism|field homomorphisms]] as [[morphisms]]. It is a [[full subcategory]] of [[CRing]], the more general category of [[commutative rings]], which is more often considered. This is due to $Field$ not being a very well-behaved category.

##Properties

* $Field$ is neither [[finitely complete category|finitely complete]] nor [[finitely cocomplete category|finitely cocomplete]], meaning in particular, that it has neither [[products]] nor [[coproducts]]. ([Riehl 17, p. 126](#RiehlCTInContext))
* The [[forgetful functor]] $U\colon Field\to Set$ does not have a [[left adjoint]] (hence $Field$ is not a [[reflective subcategory]] of $Set$), hence there is no free field construction (contrary to many [[free functors]] for other [[algebraic categories]]). The same holds for weaker forgetful functors like $U\colon Field\to Ring$, $U\colon Field\to Ab$ or the [[group of units]] $-^\times\colon Field\to Ab$. ([Riehl 17, Example 4.1.11.](#RiehlCTInContext))
* Every morphism in $Field$ is a [[monomorphism]].
* The isomorphisms in $Field$ are the bijective homomorphisms. ([Riehl 17, Examples 1.1.6. (ii)](#RiehlCTInContext))

## Subcategories

$Field$ is not [[connected category|connected]] as there are no [[field homomorphism|field homomorphisms]] between fields of different characteristic. The connected component ([[full subcategory]] of $Field$) corresponding to [[characteristic]] $p$ (with $p=0$ or $p$ [[prime]]) is denoted $Field_p$.

The [[field]] of [[rational numbers]] $\mathbb{Q}$ is the [[initial object]] of $Field_0$ and the [[prime field]] $\mathbb{F}_p$ is the [[initial object]] of $Field_p$, but none are in $Field$, which has neither an initial nor [[terminal object]]. ([Riehl 17, Examples 1.6.18. (vi)](#RiehlCTInContext))

## References

* {#RiehlCTInContext} [[Emily Riehl]], _[[Category Theory in Context]]_, Dover Publications (2017) &lbrack;[pdf](http://www.math.jhu.edu/~eriehl/context.pdf)&rbrack;