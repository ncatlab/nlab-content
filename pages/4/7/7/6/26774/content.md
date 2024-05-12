[[!redirects indexing systems]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Content#
* table of contents
{:toc}

## Idea

An __indexing system__  is a combinatorial datum which uniquely determines an [[N-∞ operad]].

## Definition

In the following definition, fix $\mathcal{T}$ an [[orbital ∞-category]] and $\mathbb{F}_{\mathcal{T}} \coloneqq \mathcal{T}^{\amalg}$ its finite-coproduct closure;
for instance, $\mathcal{T}$ may be the [[orbit category]] of a finite group, in which case $\mathbb{F}_{\mathcal{O}_G}$ is the category of finite [[G-sets]].

\begin{definition}
  A subcategory $I \subset \mathbb{F}_{\mathcal{T}}$ is called an __indexing system__ if 

1. ($\Sigma$-action) $I$ contains the [[core]] $\mathbb{F}_{\mathcal{T}}^{\simeq}$.

2. (Segal condition and restrictions) $I$ is stable under binary coproducts and pullbacks along arbitrary morphisms.

3. (Binary multiplications) $I$ contains the fold map $\nabla:2 \cdot V \rightarrow V$ for all $V \in \mathcal{T}$.

\end{definition}

## Equivalent characterizations
### Sub-symmetric monoidal categories
Recall that [[induced representation |induction]] yields an equivalence $\mathbb{F}_H \simeq \mathbb{F}_{G, /[G/H]}$ for each subgroup $H \subset G$.
Given $I \subset \mathbb{F}_G$ an indexing system, and $H \subset G$ we refer to the corresponding subcategory 
$$
  \mathbb{F}_{I,H} \coloneqq I_{/[G/H]} \simeq \mathbb{F}_{G, /[G/H]} \simeq \mathbb{F}_H.
$$
The following was proved in [Blumberg-Hill 16](#Blumberg16).
\begin{theorem}
  There is a unique $G$-subcategory $\underline{\mathbb{F}}_I \subset \underline{\mathbb{F}}_G$;
  furthermore, this outlines an equivalence between the poset of indexing systems and the poset of full $G$-subcategories which contain trivial $H$-sets and are closed under coproducts, finite limits, and self-induction.
\end{theorem}

### Transfer systems
Let $\mathrm{Sub}(G)$ be the subgroup lattice of $G$.
We say that a subposet $R \subset \mathrm{Sub}(G)$ is a \emph{transfer system} if it is closed under conjugation and restriction.

Given $I \subset \mathbb{F}_G$ an indexing system, we let $T(I) \subset \mathrm{Sub}(G)$ denote the subposet consisting of inclusions $K \subset H$ such that the corresponding map $G/K \rightarrow G/H$ is in $I$.
The following theorem was independently proved by [Rubin](#Rubin17) and [Balchin-Barnes-Roitzheim](#Balchin19).
\begin{theorem}
  $T(I)$ is a transfer system, and this outlines an equivalence of posets
$$
  \mathrm{Index}_{G} \simeq \mathrm{Transfer}_G.
$$
\end{theorem}

### $N_\infty$-operads.
The poset of subcommutative [[G-∞ operads]] containing $\mathbb{E}_\infty$ corresponds with $\mathrm{Index}_G$; these are called [[N-∞ operads]] (see the linked page for details).

## Properties
(...)


## Related concepts

(...)

## References

Originally,

* {#Blumberg13} [[Andrew Blumberg]], [[Michael Hill]], _Operadic multiplications in equivariant spectra, norms, and transfers_, ([arXiv:1309.1750](https://arxiv.org/abs/1309.1750))

Further characterization,

* {#Blumberg16} [[Andrew Blumberg]], [[Michael Hill]], _Incomplete Tambara functors_, ([arXiv:1603.03292](https://arxiv.org/abs/1603.03292))

* {#Rubin17} [[Jonathan Rubin]], _Characterizations of equivariant Steiner and linear isometries operads_, ([ arXiv:1903.08723v2](https://arxiv.org/abs/1903.08723v2))

* {#Balchin19} [[Scott Balchin]], [[David Barnes]], [[Constanze Roitzheim]], _$N_\infty$-operads and associahedra_, ([arXiv:1905.03797](https://arxiv.org/abs/1905.03797))

Over [[orbital categories]],

* [[Denis Nardin]], [[Jay Shah]], _Parametrized and equivariant higher algebra_, (2022) ([arxiv:2203.00072](https://arxiv.org/abs/2203.00072))
[[!redirects equivariant symmetric monoidal categories]]


[[!redirects indexing systems]]