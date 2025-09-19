+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

##  Idea 

The 2-category [[Cat|$Cat$]] of [[categories]] embeds [[fully faithfully]] into the 2-category $Multicat$ of [[multicategories]] in two ways:

1. As the unary multicategories (i.e. in which every multimorphism has unary domain).
2. Via the "discrete cocones" construction, in which we define the multimorphisms of the multicategory $C_\blacktriangleright$ induced by a category $C$ by
\begin{equation}
C_\blacktriangleright(X_1, \ldots, X_n; Y) := C(X_1, Y) \times \cdots \times C(X_n, Y)
\end{equation}

A multicategory is isomorphic to one induced by the discrete cocones construction exactly when it is a [[generalized multicategory]] relative to the [[monad]] on [[Prof]] whose algebras are categories with (strict) finite coproducts, i.e. a "virtual cocartesian category".  Thus, such a multicategory is called a a *cocartesian multicategory**.

An older name for a cocartesian multicategory is a **sequential multicategory**, since its multimorphisms are sequences of unary morphisms.

## Equivalence of definitions

\begin{theorem}
For a [[symmetric multicategory]] $E$ the following are equivalent.

1. $E \cong C_\blacktriangleright$ for some category $C$ (which then must be the category of unary morphisms in $E$).
2. Every object of $E$ is a [[monoid object]], in a way that commutes with all the multimorphisms of $E$.
3. $E$ is equipped with

   * "coduplication" or "codiagonal" or "cocontraction" operations
     $$E(\dots, X, \dots) \to E(\dots, X,X,\dots)$$
   * "insertion" or "strengthening" operations
     $$E(\dots, X,\dots) \to E(\dots, \dots)$$

   satisfying certain evident axioms.
4. $E$ has the structure of a virtual $T$-algebra, where $T$ is the monad on [[Prof]] whose algebras are cocartesian strict monoidal categories.

\end{theorem}

## Properties

- Being cocartesian is a *property* of a multicategory, in contrast to being a [[cartesian multicategory]], which is *structure*.

- Every cocartesian multicategory has the structure of a [[symmetric multicategory]].

- A cocartesian multicategory $C_\blacktriangleright$ is [[representable multicategory|representable]] if and only if $C$ has coproducts (Example 8.8(2) of [Hermida 2000](#Hermida)). This is another motivation for the terminology.

- A category $C$ is [[preadditive category|preadditive]] if and only if its corresponding cocartesian multicategory $C_\blacktriangleright$ is [[cartesian multicategory|cartesian]] (see [Pisani 2013](#Pisani13) and [Pisani 2014](#Pisani14)); and is hence [[additive category|additive]] if and only if its corresponding multicategory is cartesian and representable.

- The discrete cocones construction $(-)_\blacktriangleright : Cat \to Multicat$ is left adjoint to the [[category of monoids]] construction $Mon : Multicat \to Cat$, and this restricts to [[cartesian multicategories]]. In fact, this is a consequence of the more general fact that $Multicat$ is [[copowered]] over $Cat$: see [Pisani 2013](#Pisani13) and [Pisani 2014](#Pisani14).

## References

The discrete cocones construction was introduced in Example 2.2(2) of:

* {#Hermida} [[Claudio Hermida]], _Representable multicategories_, Adv. Math. 151 (2000), no. 2, 164-225 ([pdf](http://wslc.math.ist.utl.pt/s84.www/cs/claudio/articles/rep-mult.pdf))

and studied extensively in the following papers, where the terminology **sequential multicategory** is introduced:

* {#Pisani13} [[Claudio Pisani]], _Some remarks on multicategories and additive categories,_ [arXiv:1304.3033](https://arxiv.org/abs/1304.3033) (2013).

* {#Pisani14} [[Claudio Pisani]], _Sequential multicategories_, Theory and Applications of Categories 29.19 (2014), [arXiv:1402.0253](https://arxiv.org/abs/1402.0253)

It is further studied, under the name **cocartesian multicategory** in:

* {#Pisani25} [[Claudio Pisani]], _Unbiased multicategory theory_, Theory and Applications of Categories, Vol. 44, 2025, No. 28, pp 826-868. [web](http://tac.mta.ca/tac/volumes/44/28/44-28abs.html)

The discrete cocones construction is also discussed in Example 2.1.6 of [[Higher Operads, Higher Categories]].

An analogue of sequential multicategories for [[(infinity, 1)-categories]] is contained in §2.4.3 of [[Higher Algebra]].

The sequential multicategory structure was rediscovered in the one-object setting as the "T construction" of:

* Samuele Giraudo, _Combinatorial operads from monoids_, Journal of Algebraic Combinatorics 41 (2015): 493-538.

A generalisation of the concept to [[generalised multicategories]] is given in:

* Alex Cebrian, _Plethysms and operads_, Collectanea Mathematica 75.1 (2024): 247-303.

[[!redirects sequential multicategory]]
[[!redirects sequential multicategories]]
[[!redirects cocartesian multicategories]]
[[!redirects discrete cocones construction]]
