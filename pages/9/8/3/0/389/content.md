

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
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

There is an [[orthogonal factorization system]] on the category [[Cat]], whose left class is the class of [[bo functor|bijective-on-objects functors]], or "bo functors" and whose right class is the class of [[full and faithful functor|full and faithful functors]], or "ff functors".

This means that each functor $f$ decomposes as a composition of the form $j e$, where $e$ is bijective on objects and $j$ fully faithful; and if 

$$\array{
A &\stackrel{u}\longrightarrow& C
\\
e\downarrow &&\downarrow j
\\
B &\stackrel{v}\longrightarrow& D
}$$

is a commutative diagram with $e$ bijective on objects and $j$ fully faithful, then there is a unique functor $h \colon B\to C$ such that $h e = u$ and $j h = v$. The object $C$, through which $f$ factors, is called the [[full image]] of $f$.

In fact, this can be generalized to a square commuting up to invertible [[natural transformation]], in which case one still concludes that $h e = u$ but that $j h \cong v$, with the isomorphism composing with $e$ to give the original isomorphism.  This means that this is an [[enhanced factorization system]].

## Properties

This factorization system can be constructed using [[generalized kernels]].

For [[essentially surjective functors]], one can relax both the commuting and the uniqueness to obtain a [[factorization system in a 2-category]].

[[!redirects (bo,ff) factorization system]]
[[!redirects bo-ff factorization system]]
