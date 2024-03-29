
# Contents
* table of contents
{: toc}

## Definition

\begin{definition}
([Mann (2022)](#Mann22), Definition 1.6.3)
\linebreak
Let $A$ be a [[ring]] and let $\mathcal{D}(A)$ be the ("[[derived category|derived]]") [[(infinity,1)-category|$\infty$-category]] [[(infinity,1)-category of chain complexes|of chain complexes of]] [[condensed module|condensed $A$-modules]]. For any [[profinite set]] $S=\underset{\underset{i}{\leftarrow}}\lim S_{i}$ consider the [[limit in an (infinity,1)-category|$\infty$-(co)limit]]
$$
  A_{\square}[S]
  \;\coloneqq\;
  \underset
    {\underset{ A'\subseteq A }{\rightarrow}}
    {\lim}
  \;
  \underset
    {\underset{i}{\leftarrow}}
    {\lim}
  \;
  A'\big[S_{i}\big]
  \,,
$$
where $A'$ ranges over all [[subrings]] of $A$ which are of [[finite type]] over [[integers|$\mathbb{Z}$]]. 

An [[object]] $M \in \mathcal{D}(A)$ is called _solid_ if for any [[profinite set]] $S$ the canonical [[map]] of [[enriched (infinity,1)-category|mapping objects]]
$$
  \underline{Hom}
  \big(
    A_{\square}[S]
    ,\,
    M
  \big)
  \longrightarrow
  \underline{Hom}
  \big(
    A[S]
    ,\,
    M
  \big)
$$
is an [[equivalence in an (infinity,1)-category|equivalence]] in $\mathcal{D}(A)$. 

The [[full subcategory]] of solid modules in $\mathcal{D}(A)$ is denoted $\mathcal{D}_{\square}(A)$.

\end{definition}

## Globalization

Using the notion of [[adic spaces]], we can glue together solid modules and consider the derived category $\mathcal{D}((\mathcal{O}_{X},\mathcal{O}_{X}^{+})_{\square})$, for $X$ an adic space. By passing to the homotopy category we get the triangulated category $D((\mathcal{O}_{X},\mathcal{O}_{X}^{+})_{\square})$ ([ScholzeLCM](#ScholzeLCM), Lectures IX and X).

## Coherent duality

There exists a notion of coherent duality (analogous to [[Grothendieck duality]]) for solid modules ([ScholzeLCM](#ScholzeLCM), Theorem 11.1).

For brevity, given a scheme $X$ with associated adic space $X^{\ad}$, let us define $D(\mathcal{O}_{X,\square}):=D((\mathcal{O}_{X^{\ad}},\mathcal{O}_{X^{\ad}}^{+})_{\square})$.

\begin{theorem}
Let $F:X\to \mathrm{Spec}(R)$ be a separated and smooth map of finite type, of dimension $d$. Let $\omega_{X/R}=\bigwedge^{d}\Omega_{X/R}^{1}$. There is a canonical functor

$$f_{!}:D(\mathcal{O}_{X,\square})\to D(R_{\square})$$

that agrees with $R\Gamma(X,-)$ in the case that $f$ is proper. It preserves compact objects. There is a natural trace map

$$f_{!}\omega_{X/R}[d]\to R$$

such that for all $C\in D(\mathcal{O}_{X,\square})$, the natural map

$$R\Hom_{\mathcal{O}_{X}}(C,\omega_{X/R})[d]\to R\Hom_{R}(f_{!}C,R)$$ 

is an isomorphism.
\end{theorem}

## Six-functor formalism

The category $D(\mathcal{O}_{X,\square})$ admits the [[six operations]] ([ScholzeLCM](#ScholzeLCM), Lecture XI). The first four functors $-\otimes -$, $\Hom(-,-)$, $f_{*}$, $f^{*}$ are classical and do not require condensed mathematics. The functor $f_{!}$ has to be constructed, and $f^{!}$ will be defined to be its [[right adjoint]].

Let $f:X\to Y$ be a separated map of finite type. Then the corresponding map of [[adic spaces]] $f_{\ad}:X^{\ad}\to Y^{\ad}$ factors as $f_{\ad}:X^{\ad}\xrightarrow{j} X^{\ad/ Y} \xrightarrow{f^{\ad /Y}} Y^{\ad}$, where the map $j$ is an open immersion and an isomorphism if $f$ is proper.

\begin{proposition}([ScholzeLCM](#ScholzeLCM) Proposition 11.2)

The functor

$$j^{*}:D(\mathcal{O}_{X^{\ad /Y}},\mathcal{O}_{X^{\ad /Y}}^{+})\to D(\mathcal{O}_{X^{\ad}},\mathcal{O}_{X^{\ad}}^{+})$$

admits a left adjoint

$$j_{!}:D((\mathcal{O}_{X^{\ad}},\mathcal{O}_{X^{\ad }}^{+})_{\square})\to D(\mathcal{O}_{X^{\ad} /Y},\mathcal{O}_{X^{\ad /Y}}^{+})_{\square}).$$

\end{proposition}

\begin{definition}([ScholzeLCM](#ScholzeLCM) Definition 11.3)
The functor $f_{!}:D(\mathcal{O}_{X},\square)\to D(\mathcal{O}_{Y,\square})$ is defined to be the composition

$$f_{!}=f_{*}^{\ad /Y}\circ j_{!}.$$
\end{definition}

It turns out that the functor $f_{!}$ commutes with all direct sums and therefore admits a right adjoint, which will be the sixth functor we call $f^{!}$.

## Solid $\mathcal{O}_{X}^{+}/\pi$ almost-modules

In [Mann22](#Mann22), Mann combines the theory of solid modules with the theory of [[almost modules]] to construct the derived $\infty$-category (in the sense of 1.3.2 of [LurieHA](#LurieHA)) $\mathcal{D}_{\square}^{\a}(\mathcal{O}_{X}^{+}/ \pi)$ of solid $\mathcal{O}_{X}^{+}/ \pi$ [[almost modules]] and with it the [[six operations]] on [[rigid analytic spaces]], in order to prove the following "mod p" version of [[Poincare duality]]:

\begin{proposition} ([Mann22](#Mann22), Theorem 1.1.1)

Let $K$ be an algebraically closed field of characteristic $0$ whose residue field is of characteristic $p$. Let $X$ be a proper smooth rigid-analytic variety of pure dimension $d$ over $K$. Then for all $i\in\mathbb{Z}$ there is a natural perfect pairing

$$H_{et}^{i}(X,\mathbb{F}_{p})\otimes_{\mathbb{F}}H_{et}^{2d-i}(X,\mathbb{F}_{p})\to\mathbb{F}_{p}(-d).$$
\end{proposition}

"mod p" Poincare duality for rigid analytic spaces had also previously been proven by Zavyalov in [Zavyalov21](#Zavyalov21), using different methods.

The theory of [[almost modules]] is necessary in order to make the structure sheaf $\mathcal{O}_{X}^{+}/\pi$ [[acyclic]] on [[affinoid]] [[perfectoid spaces]] (compare the analogous classical situation for [[abelian sheaf cohomology]] or [[Cech cohomology]] for [[schemes]]).

In the course of proving Poincare duality for rigid analytic spaces, Mann also proves a version of a p-torsion [[Riemann-Hilbert correspondence]] for small v-stacks ([Mann22](#Mann22), Theorem 3.9.23). 

## Related concepts

* [[condensed mathematics]]

* [[analytic ring]]

* [[six operations]]

## References

* {#Mann22} [[Lucas Mann]], *A p-Adic 6-Functor Formalism in Rigid-Analytic Geometry* &lbrack;[arXiv:2206.02022](https://arxiv.org/abs/2206.02022)&rbrack;

* {#ScholzeLCM} [[Peter Scholze]], _Lectures on condensed mathematics_, [pdf](https://www.math.uni-bonn.de/people/scholze/Condensed.pdf)

Zavyalov's proof of Poincare duality for rigid analytic spaces can be found in

* {#Zavyalov21} Bogdan Zavyalov, _Mod-p Poincaré Duality in p-adic Analytic Geometry_, [arXiv:2111.01830](https://arxiv.org/abs/2111.01830)

* {#LurieHA} [[Jacob Lurie]], _Higher Algebra_, ([pdf](https://people.math.harvard.edu/~lurie/papers/HA.pdf))

[[!redirects solid modules]]
