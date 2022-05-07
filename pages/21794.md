

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

1. _quasi-complete_ if $i$ is [[surjective]]

1. _separated_ if $i$ is [[injective]]

1. _complete_ if $i$ is [[bijective]].

\end{definition}

The completion functor is idempotent (warning: this is not true in general if $I$ is not finitely generated), hence induces an [[idempotent monad]] on the category [[RMod]], and is [[left adjoint]] to the inclusion of the category $\widehat{R Mod}$ of complete modules into all modules. Hence, $\widehat{R Mod}$ is a [[reflective subcategory]] of $R Mod$. It is not, however, an [[abelian subcategory]]: the [[quotient]] of two complete modules is not, in general, complete.

A key observation is that the completion functor is not [[right exact functor|right exact]] when seen as an [[endofunctor]] of $R Mod$. Hence, let $L$ be the 0th [[left derived functor]] of the completion functor, which is right exact by definition.

\begin{definition}
An $R$-module $M$ is called $L$-complete if the canonical map
$$M\rightarrow L(M)$$
is an isomorphism.
\end{definition}
\begin{proposition}
Let $M$ be an $R$-module.

* If $M$ is finitely generated, then $\hat M=L(M)$.
* If $M$ is complete, then it is $L$-complete.
* The canonical map $M\rightarrow \hat M$ factor through the canonical map $M\rightarrow L(M)$, and the map $L(M)\rightarrow \hat M$ is surjective. In particular, an $L$-complete module is always quasi-complete.

\end{proposition}

Let $(m_i)_{i\in \mathbb{N}}$ be a sequence of elements in $M$ such that for all $n$, all but finitely many of the $m_i$'s belong to $I^n$. Then $M$ is complete if and only if for every such sequence, the partial sums $\sum_{i\leq k} m_i$ have a well-defined limit in $M$. The above proposition shows an $L$-complete needs not to be separated, hence, this limit might not exists. However, informally speaking, $L$-complete modules are those for which we can still make sense of some sort of limit.

\begin{proposition}([Salch 20](#Salch20))

The [[category]] of $L$-complete modules is the smallest abelian [[full subcategory]] of [[RMod]] which contains the $I$-[[adic completion|adically complete modules]].

\end{proposition}

##References##

* {#Salch20} [[Andrew Salch]], Approximation of subcategories by abelian subcategories ([arXiv:2011.01827](https://arxiv.org/abs/2011.01827))

* [[Charles Rezk]], _Analytic completion_ ([pdf](http://www.math.uiuc.edu/~rezk/analytic-paper.pdf))

[[!redirects L-complete modules]]

