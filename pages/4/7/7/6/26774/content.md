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

__this is under construction__

## Idea

An __indexing system__  is a combinatorial datum which uniquely determines an [[N-∞ operad]].

## Definitions

### Indexing systems
In the following definition, fix $\mathcal{T}$ an [[orbital ∞-category]] and $\mathbb{F}_{\mathcal{T}} \coloneqq \mathcal{T}^{\amalg}$ its finite-coproduct closure;
for instance, $\mathcal{T}$ may be the [[orbit category]] of a finite group, in which case $\mathbb{F}_{\mathcal{O}_G}$ is the category of finite [[G-sets]].

\begin{definition}
  A full $G$-subcategory $\underline{\mathbb{F}}_I \subset \underline{\mathbb{F}}_{\mathcal{T}}$ is called a __weak indexing system__ if

1. (objects) whenever the $V$-value $\mathbb{F}_{I,V}$ is nonempty, it contains the $V$-set $*_V$.

2. (composition) for all $S \in \underline{\mathbb{F}}_I$, $\underline{\mathbb{F}}_I \subset \underline{\mathbb{F}}_{\mathcal{T}}$ is closed under $S$-indexed coproducts.

    $\underline{\mathbb{F}}_I$ is called an __indexing system__ if, additionally,

3. (coproducts) for all $n \in \mathbb{N}$ and $V \in \mathcal{T}$, $n \cdot *_V \in \mathbb{F}_{I,V}$

\end{definition}

###Indexing categories
\begin{definition}
  A subcategory $I \subset \mathbb{F}_{\mathcal{T}}$ is called a __weak indexing category__ if it satisfies the following conditions:

1. (restriction-stability) morphisms in $I$ is stable under pullbacks along arbitrary maps in $\mathbb{F}_{\mathcal{T}}$. 

2. (Segal condition) A pair of maps $T \rightarrow S$ and $T' \rightarrow S'$ are in $I$ if and only if their coproduct $T \sqcup T' \rightarrow S \sqcup S'$ is in $I$; and

3. ($\Sigma$-action) $I$ contains all automorphisms of its objects.

A weak indexing category $I \subset \mathbb{F}_{\mathcal{T}}$ is called an __indexing category__ if it contains the fold map $n \cdot V \rightarrow V$ for all $V \in \cT$ and $n \in \mathbb{N}$.
\end{definition}

Given $I$ a weak indexing category, we may define a full $\mathcal{T}$-subcategory 
\[
  (\underline{\mathbb{F}}_I)_V \coloneqq \{S \mid \Ind_V^{\mathcal{T}} S \rightarrow V \in I\} \subset \mathbb{F}_{V}.
\]

\begin{theorem}
  The assignment $I \mapsto \underline{\mathbb{F}}_I$ furnishes an equivalence between the posets of weak indexing categories and weak indexing systems;
   this restricts to an equivalence between indexing categories and indexing systems.
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



## Properties
### $N_\infty$-operads.
The poset of subcommutative [[G-∞ operads]] containing $\mathbb{E}_\infty$ corresponds with $\mathrm{Index}_G$; these are called [[N-∞ operads]] (see the linked page for details).

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

* [[Natalie Stewart]], _Orbital categories and weak indexing systems_ [(draft)](https://nataliesstewart.github.io/files/windex_draft.pdf) 

[[!redirects indexing systems]]