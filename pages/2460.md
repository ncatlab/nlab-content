
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The notion _universal localization_ or _Cohn localization_ of a [[ring]] is a variant of the notion of [[localization of a ring]] which forces not just elements of the ring to become invertible (which one may think of as $1 \times 1$-[[matrices]]) but forces more general [[matrices]] with [[coefficients]] in the ring to become invertible.

## Definition

Let $\Sigma$ be a set of finite square [[matrices]] (of different sizes) over a (typically noncommutative) [[ring]] $R$. Without loss of generality, one assumes that $\Sigma$ is left or right multiplicative. It is left multiplicative if for any matrices $A,B,C$ of right sizes such that $A,B\in\Sigma$ and $C$ fits into matrix $New = \left(\array{ A & 0\\ C & B}\right)$, matrix $New$ is also in $\Sigma$.

We say that a [[homomorphism]] of rings $f: R\to S$ is _$\Sigma$-inverting_ if all matrices $f(A)$ over $S$ where $A\in \Sigma$ are invertible in $S$.
The Cohn localization of a ring $R$, is a homomorphism of rings $R\to \Sigma^{-1} R$ which is initial in the category of all $\Sigma$-inverting maps (which is the subcategory of coslice category $R/Ring$). In the left hand version, the elements in the localized ring are thought of as solutions of linear equations $A x = b$ where $b$ is a column vector with elements in $R$ and $A\in\Sigma$. 

### More general definition 

Given a [[ring]] $R$ and a family $S$ of morphisms in the [[category]] $R$[[Mod]] of (say left) [[finitely generated module|finitely generated]] [[projective module|projective]] $R$-[[modules]], we say that a morphism of rings $f:R\to T$ is **$S$-inverting** if the [[extension of scalars]] from $R$ to $T$ along $f$

$$
  T \otimes_R (-) \colon R Mod \to T Mod
$$

sends all morphisms of $S$ into [[isomorphism]] in the category of left $T$-modules. 

P. M. Cohn has shown that there is a universal object $R\to Q_S R$ in the category of $S$-inverting morphisms. The ring $Q_S R$ (and more precisely the universal morphism itself) are called the **universal localization** or **Cohn localization** of the ring $R$ at $S$.   


## Properties


Cohn localization induces a hereditary torsion theory, i.e. a localization endofunctor on the category of all modules, but it lacks good flatness properties at the level of full module category. However when restricted to the subcategory of finite-dimensional projectives it has all good properties -- it is not any worse than [[Ore localization]]. 

Universal localization is much used in algebraic K-theory, algebraic L-theory and surgery theory -- see [[Andrew Ranicki]]'s slides in the references at Cohn localization and his papers, specially the series with Amnon Neeman.

## References

Original articles include

* [[P. M. Cohn]], _Inversive localization in noetherian rings_, Communications on Pure and Applied Mathematics __26__:5-6, pp. 679&#8211;691, 1973 [doi](http://dx.doi.org/10.1002/cpa.3160260510) 

Reviews and lecture notes include

* [[V. Retakh]], R. Wilson, _Advanced course on quasideterminants and universal localization_, [pdf](http://castellet.cat/Publications/quaderns/Quadern41.pdf) 


* (NLOC) _Noncommutative localization in algebra and topology_,
(Proceedings of Conference at ICMS, Edinburgh, 29-30 April 2002),
London Math. Soc. Lecture Notes Series 330 ([pdf](http://www.maths.ed.ac.uk/~aar/books/nlat.pdf)), ed. [[Andrew Ranicki]], Cambridge University Press (2006) 

* [[Z. Škoda]], _Noncommutative localization in noncommutative geometry_, in (NLOC, above) pp. 220--313, [math.QA/0403276](http://arxiv.org/abs/math.QA/0403276)

* [[Andrew Ranicki]], _Noncommutative localization in algebra and topology_, talk at Knot theory meeting, 2008, slides [pdf](http://www.maths.ed.ac.uk/~aar/slides/heidel2.pdf); _Noncommutative localization_, [[Pierre Vogel]] 65th birthday conference, Paris, 27 October 2010, [slides pdf](http://www.maths.ed.ac.uk/~aar/slides/vogel.pdf)


One can also look at localization with inverses just from one side:

* [[P. M. Cohn]], _One-sided localization in rings_, J. Pure Appl. Algebra __88__ (1993), no. 1-3, 37&#8211;42 []()

Universal localization of [[group rings]] (and connections to certain noncommutative rational function rings and [[Fox derivative]]s) is discussed in

* [[M. Farber]], [[Pierre Vogel]], _The Cohn localization of the free group ring_, Math. Proc.  Camb. Phil. Soc. (1992) 111, 433  ([pdf](http://www.maths.ed.ac.uk/~aar/papers/fv.pdf))


[[!redirects Cohn localization]]
[[!redirects Cohn universal localization]]
   