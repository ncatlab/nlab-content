

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


# Model structure on sections

* table of contents
{: toc}

## Definitions

### Sections

Let $K$ be a [[small category]] and $F:K\to ModelCat$ a [[pseudofunctor]], where $ModelCat$ is the 2-category of [[model categories]], [[Quillen adjunctions]] pointing in the direction of their left adjoints, and [[mate]]-pairs of natural isomorphisms.  This is sometimes called a **Quillen presheaf** (with "right" or "left" attached according to whether one is thinking about the left adjoints or the right adjoints in the Quillen adjunctions); we denote the Quillen adjunction $F(f)$ by $f_! \dashv f^*$.

The category of **sections** of $F$ is the category of [[sections]] $K \to \int F$ of its [[Grothendieck construction]].  Explictly, a section of $F$ consists of, for each $k\in K$ an object $X_k\in F_k$, and for each $f:\ell\to k$ in $K$ a morphism $X_\ell \to f^* X_k$ (or equivalently $f_! X_\ell \to X_k$) satisfying a functoriality condition.  The category $Sect(F)$ is the [[lax limit]] of the diagram $K\to Cat$ consisting of the left Quillen functors $f_!$, and also the [[colax limit]] of the analogous diagram consisting of the right Quillen functors.  Accordingly, it is [[locally presentable]] if each category $F_k$ is.

### Projective and injective model structures

\begin{theorem}
  If each $F_k$ is a [[combinatorial model category]], [[accessible model category]], or [[tractable model category]], then $Sect(F)$ has two model structures that are also combinatorial, accessible, or tractable respectively:

1. A **projective model structure** in which a morphism $X\to Y$ is a fibration or weak equivalence if each $f_k : X_k\to Y_k$ is such in $F_k$.
1. An **injective model structure** in which a morphism $X\to Y$ is a cofibration or weak equivalence if each $f_k : X_k\to Y_k$ is such in $F_k$.

\end{theorem}
\begin{proof}
  The combinatorial and tractable cases are [Barwick, 2.28 and 2.30](#Barwick10).  They are a straightforward application of [[transferred model structures]], generalizing the usual constructions of [[model structures on functors]].  The accessible case follows similarly using the accessible version of transfer.
\end{proof}

These model structures are a presentation of the $(\infty,1)$-categorical *lax limit* of $F$.  To present the *pseudo (homotopy) limit* of $F$ we have to localize them:

\begin{theorem}
  The above projective model structure has a [[left Bousfield localization]], called the **(projective) homotopy limit model structure**, in which the fibrant objects are the projectively fibrant ones that are **homotopy cartesian**, i.e. for each $f:\ell\to k$ in $K$ the induced map $X_\ell \to f^*(X_k) \to f^*(R X_k)$ is a weak equivalence, where $R$ denotes a fibrant replacement.
\end{theorem}
\begin{proof}
  This is [Barwick, 4.38](#Barwick10).
\end{proof}

### Reedy model structures

If each $F_k$ is a model category (not even necessarily cofibrantly generated) and $K$ is a [[Reedy category]], then there is also a **Reedy model structure** on $Sect(F)$ defined analogously to the ordinary case.  This is in [Balzin18](#Balzin18), together with a generalization to any "admissible model semifibration" over a Reedy category.


## Properties

* These model structures are presentations of the $(\infty,1)$-category of sections (i.e. (co)lax limit) of the induced functor of $(\infty,1)$-categories.  For the projective model structure this is shown in [Harpaz18](#Harpaz18) (hence also for the injective model structure, since they have the same weak equivalences), which considers more generally sections defined on a [[simplicial category]].  For the Reedy model structure it is shown in [Balzin18](#Balzin18), with the special case of an [[inverse category]] being in [Spitzweck10](#Spitzweck10).

* A subcategory of the injective model structure analogous to the homotopy limit model structure is shown in [Bergner10](#Bergner10) to present the homotopy limit of the corresponding diagram of [[complete Segal spaces]].


## Related pages

* The dual construction is the [[Grothendieck construction for model categories]] (a lax colimit).

## References

* {#Barwick10} [[Clark Barwick]], _On left and right model categories and left and right Bousfield localizations_.  Homology, Homotopy and Applications, 12.2, 2010, p. 245-320.  [pdf](https://core.ac.uk/download/pdf/16520637.pdf), [related arxiv preprint](https://arxiv.org/abs/0708.2067)

* {#Bergner10} [[Julia E. Bergner]], _Homotopy limits of model categories and more general homotopy theories_, [arXiv:1010.0717](https://arxiv.org/abs/1010.0717)

* {#Spitzweck10} [[Markus Spitzweck]], _Homotopy limits of model categories over inverse index categories_, 2010, [doi](https://doi.org/10.1016/j.jpaa.2009.08.001)

* Johnson, Mark W. _On modified Reedy and modified projective model structures_. Theory Appl. Categ. 24 (2010), No. 8, 179–208.

* {#Harpaz18} [[Yonatan Harpaz]], _Lax limits of model categories_, [pdf](https://www.math.univ-paris13.fr/~harpaz/lax_limits.pdf)

* {#Balzin18} Edouard Balzin, _Reedy Model Structures in Families_, [arXiv:1803.00681](https://arxiv.org/abs/1803.00681)


[[!redirects model structures on sections]]
[[!redirects model structure for sections]]
[[!redirects model structures for sections]]
[[!redirects lax limit model structure]]
[[!redirects lax limit model structures]]
[[!redirects lax limit of model categories]]
[[!redirects lax limits of model categories]]
[[!redirects colax limit model structure]]
[[!redirects colax limit model structures]]
[[!redirects colax limit of model categories]]
[[!redirects colax limits of model categories]]
[[!redirects oplax limit model structure]]
[[!redirects oplax limit model structures]]
[[!redirects oplax limit of model categories]]
[[!redirects oplax limits of model categories]]
[[!redirects homotopy limit model structure]]
[[!redirects homotopy limit model structures]]
[[!redirects homotopy limit of model categories]]
[[!redirects homotopy limits of model categories]]
