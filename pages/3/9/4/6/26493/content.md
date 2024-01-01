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

A multicategory isomorphic to one induced by the discrete cocones construction is called a **sequential multicategory** (since its multimorphisms are sequences of unary morphisms).

## Properties

- Every sequential multicategory is [[symmetric multicategory|symmetric]].

- A sequential multicategory $C_\blacktriangleright$ is [[representable multicategory|representable]] if and only if $C$ has coproducts (Example 8.8(2) of [Hermida 2000](#Hermida)).

- A category $C$ is [[preadditive category|preadditive]] if and only if its corresponding sequential multicategory $C_\blacktriangleright$ is [[cartesian multicategory|cartesian]] (see [Pisani 2013](#Pisani13) and [Pisani 2014](#Pisani14)); and is hence [[additive category|additive]] if and only if its corresponding multicategory is cartesian and representable.

- The discrete cocones construction $(-)_\blacktriangleright : Cat \to Multicat$ is left adjoint to the [[category of monoids]] construction $Mon : Multicat \to Cat$, and this restricts to [[cartesian multicategories]]. In fact, this is a consequence of the more general fact that $Multicat$ is [[copowered]] over $Cat$: see [Pisani 2013](#Pisani13) and [Pisani 2014](#Pisani14).

## References

The discrete cocones construction was introduced in Example 2.2(2) of:

* {#Hermida} [[Claudio Hermida]], _Representable multicategories_, Adv. Math. 151 (2000), no. 2, 164-225 ([pdf](http://wslc.math.ist.utl.pt/s84.www/cs/claudio/articles/rep-mult.pdf))

and studied extensively in:

* {#Pisani13} [[Claudio Pisani]], _Some remarks on multicategories and additive categories,_ [arXiv:1304.3033](https://arxiv.org/abs/1304.3033) (2013).

* {#Pisani14} [[Claudio Pisani]], _Sequential multicategories_, Theory and Applications of Categories 29.19 (2014), [arXiv:1402.0253](https://arxiv.org/abs/1402.0253)

The discrete cocones construction is also discussed in Example 2.1.6 of [[Higher Operads, Higher Categories]].


[[!redirects sequential multicategories]]
