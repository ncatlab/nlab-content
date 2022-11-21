

# Contents
* table of contents
{: toc}

## Definition

\begin{definition}
([Mann (2022)](#Mann22), Definition 1.6.3)
\linebreak
Let $A$ be a [[ring]] and let $\mathcal{D}(A)$ be the derived [[(infinity,1)-category|$\infty$-category]] of [[condensed module|condensed $A$-modules]]. For any [[profinite set]] $S=\underset{\underset{i}{\leftarrow}}\lim S_{i}$ let
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

An [[object]] $M\in\mathcal{D}(A)$ is _solid_ if for any [[profinite set]] $S$ the canonical [[map]]
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
is an [[isomorphism]] in $\mathcal{D}(A)$. 

The [[full subcategory]] of solid modules in $\mathcal{D}(A)$ is denoted $\mathcal{D}_{\square}(A)$.

\end{definition}

## Related concepts

* [[condensed mathematics]]

## References

* {#Mann22} Lucas Mann, _A p-Adic 6-Functor Formalism in Rigid-Analytic Geometry_ ([arXiv:2206.02022](https://arxiv.org/abs/2206.02022))