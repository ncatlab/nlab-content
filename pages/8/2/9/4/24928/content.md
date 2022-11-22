
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

For brevity, given a scheme $X$ with associated adic space $X$, let us define $D(\mathcal{O}_{X,\square}):=D((\mathcal{O}_{X^{\mathrm{ad}}},\mathcal{O}_{X^{\mathrm{ad}}}^{+})_{\square})$.

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

The category $D(\mathcal{O}_{X,\square})$ admits the [[six operations]] ([ScholzeLCM](#ScholzeLCM), Lecture XI).

## Related concepts

* [[condensed mathematics]]

* [[analytic ring]]

* [[six operations]]

## References

* {#Mann22} [[Lucas Mann]], *A p-Adic 6-Functor Formalism in Rigid-Analytic Geometry* &lbrack;[arXiv:2206.02022](https://arxiv.org/abs/2206.02022)&rbrack;

* {#ScholzeLCM} [[Peter Scholze]], _Lectures on condensed mathematics_, [pdf](https://www.math.uni-bonn.de/people/scholze/Condensed.pdf)


[[!redirects solid modules]]
