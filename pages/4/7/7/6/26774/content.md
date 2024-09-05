
> this page is under construction


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

## Definitions


### Indexing systems
In the following definition, fix $\mathcal{T}$ an [[orbital ∞-category]] and $\mathbb{F}_{\mathcal{T}} \coloneqq \mathcal{T}^{\amalg}$ its [[finite coproduct|finite-coproduct]] closure.

For instance, $\mathcal{T}$ may be the [[orbit category]] of a [[finite group]], in which case $\mathbb{F}_{\mathcal{O}_G}$ is the category of [[finite set|finite]] [[G-sets]].

\begin{definition}
  A full $\mathcal{T}$-subcategory $\underline{\mathbb{F}}_I \subset \underline{\mathbb{F}}_{\mathcal{T}}$ is called a __weak indexing system__ if

1. (objects) whenever the $V$-value $\mathbb{F}_{I,V}$ is [[inhabited|nonempty]], it contains the $V$-set $*_V$.

2. (composition) for all $S \in \underline{\mathbb{F}}_I$, $\underline{\mathbb{F}}_I \subset \underline{\mathbb{F}}_{\mathcal{T}}$ is closed under $S$-indexed [[coproducts]].

    $\underline{\mathbb{F}}_I$ is called an __indexing system__ if, additionally,

3. (coproducts) for all $n \in \mathbb{N}$ and $V \in \mathcal{T}$, $n \cdot *_V \in \mathbb{F}_{I,V}$

\end{definition}


### Indexing categories

\begin{definition}
  A [[subcategory]] $I \subset \mathbb{F}_{\mathcal{T}}$ is called a __weak indexing category__ if it satisfies the following conditions:

1. (restriction-stability) morphisms in $I$ is stable under [[pullbacks]] along arbitrary maps in $\mathbb{F}_{\mathcal{T}}$. 

2. (Segal condition) A pair of maps $T \rightarrow S$ and $T' \rightarrow S'$ are in $I$ if and only if their coproduct $T \sqcup T' \rightarrow S \sqcup S'$ is in $I$; and

3. ($\Sigma$-action) $I$ contains all [[automorphisms]] of its objects.

A weak indexing category $I \subset \mathbb{F}_{\mathcal{T}}$ is called an __indexing category__ if it contains the fold map $n \cdot V \rightarrow V$ for all $V \in \cT$ and $n \in \mathbb{N}$.
\end{definition}

Given $I$ a weak indexing category, we may define a [[full subcategory|full]] $\mathcal{T}$-subcategory 
\[
  (\underline{\mathbb{F}}_I)_V \coloneqq \{S \mid \Ind_V^{\mathcal{T}} S \rightarrow V \in I\} \subset \mathbb{F}_{V}.
\]

\begin{theorem}
  The assignment $I \mapsto \underline{\mathbb{F}}_I$ furnishes an [[equivalence of categories|equivalence]] between the [[posets]] of weak indexing categories and weak indexing systems;
   this restricts to an [[equivalence of categories|equivalence]] between indexing categories and indexing systems.
\end{theorem}

### Unitality conditions

\begin{definition}

1. A weak indexing system $\underline{\mathbb{F}}_I$ is **almost essentially unital** (or aE-unital) if for all non-contractible $S \in \mathbb{F}_{I,V}$, the empty $V$-set $\emptyset_V$ is in $\mathbb{F}_{I,V}$.

2. A weak indexing system $\underline{\mathbb{F}}_I$ is **unital** if $\emptyset_V \in \mathbb{F}_{I,V}$ for all $V \in \mathcal{T}$.

\end{definition}

### Transfer systems

Let $\mathrm{Sub}(G)$ be the [[subgroup lattice]] of $G$.
We say that a subposet $R \subset \mathrm{Sub}(G)$ is a _transfer system_ if it is closed under [[conjugation]] and [[restriction]].

Given $I \subset \mathbb{F}_G$ an indexing system, we let $T(I) \subset \mathrm{Sub}(G)$ denote the subposet consisting of inclusions $K \subset H$ such that the corresponding map $G/K \rightarrow G/H$ is in $I$.
The following theorem was independently proved by [Rubin 2017](#Rubin17) and by [Balchin, Barnes & Roitzheim 2019](#Balchin19).

\begin{theorem}
  $T(I)$ is a transfer system, and this furnishes an equivalence of posets
$$
  \mathrm{Index}_{G} \simeq \mathrm{Transfer}_G.
$$
\end{theorem}

It is not clear how to generalize the subgroup lattice to orbital $\infty$-categories. 
Instead, one should note that closure under [[conjugation]] implies that a transfer system only depends on its image under the [[coset|homogeneous G-set]] functor $\mathrm{Sub}(G) \rightarrow \mathcal{O}_G$.
Thus we may make the following definition.

\begin{definition}
  A [[core]]-containing [[wide subcategory]] $\mathcal{T}^{\simeq} \subset R \subset \mathcal{T}$ is a \emph{transfer system} if, for all diagrams
      \begin{tikzcd}
	{U'} & U \\
	{V'} & V
	\arrow[from=1-1, to=1-2]
	\arrow["{\alpha'}", from=1-1, to=2-1]
	\arrow["\alpha", from=1-2, to=2-2]
	\arrow[from=2-1, to=2-2]
      \end{tikzcd}
  in $\mathcal{T}$ with $\alpha$ in $R$ and whose map $U' \rightarrow U \times_V V'$ is a summand inclusion, the map $\alpha'$ is in $R$.
\end{definition}

Note that closure under summands implies that, whenever $I$ is a unital weak indexing category, its intersection $\mathfrak{R}(I) \coloneqq I \cap \mathcal{T}$ is a transfer system.
[Nardin-Shah 22](#Nardin22) generalized the correspondence between indexing systems and transfer systems to orbital $\infty$-categories, and [Stewart 24](#Stewart24) generalized this to weak indexing systems as the following.

\begin{proposition}
  The monotone map $\mathfrak{R}\colon \mathrm{wIndex}_{\mathcal{T}}^{\mathrm{uni}} \rightarrow \mathrm{Transf}_{\mathcal{T}}$ has a [[fully faithful]] [[right adjoint]] whose [[essential image]] is spanned by the $\mathcal{T}$-indexing systems.
\end{proposition}



## Properties


### $N_\infty$-operads.

The poset of subcommutative [[G-∞ operads]] containing [[E-infinity operad|$\mathbb{E}_\infty$]] corresponds with $\mathrm{Index}_G$; these are called *[[N-∞ operads]]* (see there for details).

(...)


## Related concepts

* [[G-operad]], [[N-∞ operad]]

* [[equivariant symmetric monoidal category|G-symmetric monoidal category]]

* [[G-semiadditivity]]

## References

Original discussion:

* {#Blumberg13} [[Andrew Blumberg]], [[Michael Hill]], _Operadic multiplications in equivariant spectra, norms, and transfers_, Advances in Mathematics **285** (2015) 658-708 &lbrack;[arXiv:1309.1750](https://arxiv.org/abs/1309.1750), [doi:10.1016/j.aim.2015.07.013](https://doi.org/10.1016/j.aim.2015.07.013)&rbrack;

Further characterization:

* {#Blumberg16} [[Andrew Blumberg]], [[Michael Hill]], _Incomplete Tambara functors_, Algebr. Geom. Topol. **18** (2018) 723-766 &lbrack;[arXiv:1603.03292](https://arxiv.org/abs/1603.03292), [doi:10.2140/agt.2018.18.723](https://doi.org/10.2140/agt.2018.18.723)&rbrack;

* [[Jonathan Rubin]], _Combinatorial $N_\infty$ operads_ &lbrack;[arXiv:1705.03585v3](https://arxiv.org/abs/1705.03585v3)&rbrack;

On those coming from equivariant linear isometries operads:

* {#Rubin17} [[Jonathan Rubin]], _Characterizations of equivariant Steiner and linear isometries operads_ &lbrack;[ arXiv:1903.08723v2](https://arxiv.org/abs/1903.08723v2)&rbrack;

* Usman Hafeez, Peter Marcus, Kyle Orbsby, [[Angélica Osorno]], _Saturated and linear isometric transfer systems for cyclic groups of order $p^m q^n$_,  &lbrack;[ arXiv:2109.08210](https://arxiv.org/abs/2109.08210)&rbrack;

* Ethan MacBrough, _Equivariant linear isometries operads over Abelian groups_,  &lbrack;[arXiv:2311.08797](https://arxiv.org/abs/2311.08797)&rbrack;

* Julie E. M. Bannwart, _Realization of saturated transfer systems on cyclic groups of order $p^{n} q^{m}$ by linear isometries $N_\infty$-operads_ &lbrack;[arXiv:2311.01608](https://arxiv.org/abs/2311.01608)&rbrack;

On enumerating categories of transfer systems

* {#Balchin19} [[Scott Balchin]], [[David Barnes]], [[Constanze Roitzheim]], _$N_\infty$-operads and associahedra_, Pacific J. Math. **315** (2021) 285-304 &lbrack;[arXiv:1905.03797](https://arxiv.org/abs/1905.03797), [doi:10.2140/pjm.2021.315.285](https://doi.org/10.2140/pjm.2021.315.285)&rbrack;

* Evan E. Franchere, Kyle Ormsby, [[Angélica Osorno]], Weihang Qin, Riley Waugh, _Self-duality of the lattice of transfer systems via weak factorization systems_ &lbrack;[arXiv:2102.04415](https://arxiv.org/abs/2102.04415)&rbrack;

* [[Scott Balchin]], Ethan MacBrough, Kyle Ormsby, _Lifting $N_\infty$ operads from conjugacy data_, &lbrack;[arXiv:2209.06798](https://arxiv.org/abs/2209.06798)&rbrack;

* [[Scott Balchin]], Ethan MacBrough, Kyle Ormsby, _The combinatorics of $N_\infty$ operads for $C_{qp^n}$ and $D_{p^n}$_, &lbrack;[arXiv:2209.06992](https://arxiv.org/abs/2209.06992)&rbrack;



Over [[orbital categories]]:

* {#Nardin22} [[Denis Nardin]], [[Jay Shah]], _Parametrized and equivariant higher algebra_ &lbrack;[arxiv:2203.00072](https://arxiv.org/abs/2203.00072)&rbrack;

* {#Stewart24} [[Natalie Stewart]], _Orbital categories and weak indexing systems_ &lbrack;[arXiv:2409.01377](https://arxiv.org/abs/2409.01377)&rbrack;

[[!redirects indexing systems]]