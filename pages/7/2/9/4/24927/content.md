#Contents#
* table of contents
{:toc}

## Definition

\begin{definition}([ScholzeLCM](#ScholzeLCM), Definition 7.1)

A _pre-analytic ring_ is a condensed ring $\underline{A}$ together with a functor $S\mapsto\mathcal{A}[S]$ from extremally disconnected sets to $\underline{\mathcal{A}}$-modules in condensed abelian groups taking finite disjoint unions to products, and a natural transformation $S \to\mathcal{A}[S]$.
\end{definition}

\begin{definition}([ScholzeLCM](#ScholzeLCM), Definition 7.4)
An _analytic ring_ is a pre-analytic ring $\mathcal{A}$ such that for any complex $C$ of $\underline{\mathcal{A}}$-modules in condensed abelian groups such that all $C_{i}$ are direct sums of objects of the form $\mathcal{A}[T]$ for varying extremally disconnected $T$, the map
$$R\underline{\Hom}_{\underline{\mathcal{A}}}(\mathcal{A}[S],C)\to R\underline{\Hom}_{\underline{\mathcal{A}}}(\mathcal{A}[S],C)$$
of condensed abelian groups is an isomorphism for all extremally disconnected $S$.

\end{definition}

## Examples

The following examples come from [ScholzeLCM](#ScholzeLCM), Examples 7.3, as examples of pre-analytic rings. They are shown to be analytic rings as well later on in the same reference.

* The analytic ring $\mathbb{Z}_{\square}$ is given by $\underline{\mathcal{A}}=\mathbb{Z}$ and $S\mapsto \mathbb{Z}[S]^{\square}$ (in the notation of [[solid abelian group]]).

* For $A$ a discrete ring, the analytic ring $(A,\mathbb{Z})_{\square}$ is given by $\underline{\mathcal{A}}=A$ as a condensed ring and $S\mapsto \mathbb{Z}_{\square}[S]\otimes_{\mathbb{Z}} A$.

* For $A$ a finitely generated $\mathbb{Z}$-algebra, the condensed ring $A_{\square}$ is given by $\underline{\mathcal{A}}=A$ as a condensed ring and $S\mapsto
  A_{\square}[S]
  \;\coloneqq\;
  \underset
    {\underset{i}{\leftarrow}}
    {\lim}
  \;
  A\big[S_{i}\big]
  \,
$.

## Related concepts

* [[condensed mathematics]]

* [[solid module]]

## References

* {#ScholzeLCM} [[Peter Scholze]], _Lectures on condensed mathematics_, [pdf](https://www.math.uni-bonn.de/people/scholze/Condensed.pdf)