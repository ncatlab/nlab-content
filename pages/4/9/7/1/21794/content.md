

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


##Idea

For a [[commutative ring]] $R$ and a [[finitely generated module|finitely generated]] [[ideal]] $I$, the [[category]] of $I$-[[adic completion|adically complete modules]] is not [[abelian category|abelian]]. The category of _$L$-complete modules_ is, in some precise sense, the smallest abelian [[subcategory]] of [[RMod]] which contains the $I$-[[adic completion|adically complete modules]]. Roughly speaking, it is obtained by formally adjoining [[cokernels]] of [[morphisms]] between $I$-[[adic completion|adically complete modules]].

## Motivation and definition##

Let $R$ be a [[commutative ring]] and $I \subset R$ a [[finitely generated module|finitely generated]] [[ideal]]. The $I$-[[adic completion]] of an $R$-[[module]] $M$ is the [[inverse limit]]

$$
  \hat M
  =
  \lim_{\leftarrow} M/I^n M
  \,.
$$

Let $i:M\rightarrow \hat M$ be the canonical map.

\begin{definition}
An $R$-module $M$ is said to be

1. quasi-complete if $i$ is surjective
1. separated if $i$ is injective
1. complete if $i$ is bijective.

\end{definition}

The completion functor is idempotent (warning: this is not true in general if $I$ is not finitely generated), hence induces an [[idempotent monad]] on $R$-mod, and is [[left adjoint]] to the inclusion of the category $\widehat{R-mod}$ of complete modules into all modules. Hence, $\widehat{R-mod}$ is a [[reflective subcategory]] of $R$-mod. It is not, however, an [[abelian subcategory]]: the [[quotient]] of two complete modules is not, in general, complete.

A key observation is that the completion functor is not [[right exact functor|right exact]] when seen as an [[endofunctor]] of [[RMod]]. Hence, let $L$ be the 0th [[left derived functor]] of the completion functor, which is right exact by definition.

\begin{definition}
An $R$-module $M$ is called $L$-complete if the canonical map
$$M\rightarrow L(M)$$
is an isomorphism.
\end{definition}

\begin{proposition}([Salch](#Salch16))
The category of $L$-complete modules is the smallest abelian [[full subcategory]] of [[RMod]] which contains the $I$-[[adic completion|adically complete modules]].
\end{proposition}

##References##

* {#Salch16} [[Andrew Salch]], Approximation of subcategories by abelian subcategories ([arXiv:2011.01827](https://arxiv.org/abs/2011.01827))
* [[Charles Rezk]], _Analytic completion_ ([pdf](http://www.math.uiuc.edu/~rezk/analytic-paper.pdf))

[[!redirects L-complete modules]]

