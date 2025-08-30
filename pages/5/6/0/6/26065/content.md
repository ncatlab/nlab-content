

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea
A *monoidal double category* is a [[double category]] equipped with a [[tensor product]] (cf. *[[monoidal 2-category]]*), compatible with both tight and loose morphisms.

Formally, a monoidal double category is a [[pseudomonoid]] in the ([[product of categories|cartesian]] [[monoidal 2-category|monoidal]]) [[2-category]] $\mathbf{DblCat}$ of double categories, [[double functor|(lax) double functors]] and [[double natural transformation|loose natural transformations]].

## Definition

Recall a double category $\mathbb{D}$ is an [[internal category|internal (pseudo)category]] in [[Cat]], hence is given by two categories $\mathbb{D}_1$ (category of loose arrows) and $\mathbb{D}_0$ (category of objects), plus *source* and *target* functors $s,t:\mathbb{D}_1 \to \mathbb{D}_0$, a *loose identity* functor $U:\mathbb{D}_0 \to \mathbb{D}_1$, and a *loose composition* functor $\odot  : \mathbb{D}_1 {}_s\times_t \mathbb{D}_1 \to \mathbb{D}_0$.
Clearly this data has to satisfy the properties of the composition of a category, thus $U$ provides identities for the $\odot$, which in turn is associative. In [Shulman 2010](#Shulman10) moreover, these properties are only satisfied up to coherent isomorphism, making loose arrows form a [[bicategory]].

\begin{definition}
A monoidal double category is a double category $\mathbb{D}$ equipped with [[double functors]]
$$I: \mathbb{1} \to \mathbb{D}\quad \text{and} \quad \otimes : \mathbb{D} \times \mathbb{D} \to \mathbb{D}$$
and with [[double natural transformations]] $\alpha : (\otimes\otimes)\otimes \cong \otimes(\otimes\otimes)$, $\lambda : (I \times \mathbb{D})\otimes \cong \otimes$, $\rho : (\mathbb{D} \times I)\otimes \cong \otimes$ satisfying the usual coherence laws of a pseudomonoid (pentagon and triangle, see [[monoidal category]]).
\end{definition}

\begin{remark}
As often happens for structure on internal categories, these arise as structures on the categories of loose arrows $\mathbb{D}_1$ and that of objects $\mathbb{D}_0$ when the source, identity and target maps respect it.

Specifically, a monoidal double category arises when both $\mathbb{D}_1$ and $\mathbb{D}_0$ are [[monoidal categories]] and

1.  $s,t:\mathbb{D}_1\to\mathbb{D}_0$ are strict monoidal, meaning if $p:A \nrightarrow B$ and $q:A' \nrightarrow B'$ are loose arrows, $p \otimes q$ is a loose arrow $A \otimes A' \nrightarrow B \otimes B'$,
2. $U:\mathbb{D}_0 \to \mathbb{D}_1$ is strong monoidal, meaning $U_1 : I \nrightarrow I$ is the monoidal unit for $\mathbb{D}_1$ and there is an iso $U_{A \otimes B} \cong U_A \otimes U_B$ for all $A,B:\mathbb{D}_0$.
3. $\odot  : \mathbb{D}_1 {}_s\times_t \mathbb{D}_1 \to \mathbb{D}_0$ is monoidal, meaning there is an iso $(p \otimes q) \odot (p' \otimes q') \cong (p \odot p') \otimes (q \odot q')$ for any suitably composable loose arrows $p,p',q',q' : \mathbb{D}_1$.

and of course these isomorphisms satisfy coherence axioms one can find in [Shulman'10](#Shulman10).
\end{remark}

\begin{definition}
A **braiding** on a monoidal double category is a natural transformation $\tau : \otimes \cong \mathrm{swap}\otimes$ which satisfies the coherence laws of the braiding of a pseudomonoid (see [[braided monoidal category]])
\end{definition}

\begin{definition}
A symmetric monoidal double category is a braided monoidal double category whose braiding $\tau$ satisfies $\tau\tau = 1$.
\end{definition}

## Related concepts

* [[monoidal 2-category]]

## References

* {#Shulman10} [[Mike Shulman]], Def. 2.9 in: _Constructing Symmetric Monoidal Double Categories_ (2010) &lbrack;[arxiv:1004.0993](https://arxiv.org/abs/1004.0993)&rbrack;

* Linde Wester Hansen and [[Mike Shulman]]. _Constructing symmetric monoidal bicategories functorially_ (2019) &lbrack;[arxiv:1910.09240](https://arxiv.org/abs/1910.09240)&rbrack;

* [[Nathanael Arkor]], [[John Bourke]], and [[Joanna Ko]], _Enhanced 2-categorical structures, two-dimensional limit sketches and the symmetry of internalisation_, [arXiv:2412.07475](https://arxiv.org/abs/2412.07475) (2024).

[[!redirects monoidal double categories]]
[[!redirects symmetric monoidal double category]]
[[!redirects symmetric monoidal double categories]]
[[!redirects braided monoidal double category]]
[[!redirects braided monoidal double categories]]