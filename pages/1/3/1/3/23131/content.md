+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A **strong profunctor** or **strong distributor** is a [[profunctor]] endowed with additional [[mathematical structure|structure]] that makes it interact nicely with the [[action]] of a [[monoidal category]]. In other words, strong profunctors generalize profunctors from [[categories]] to [[actegories]]. Strong profunctors are used in the theory of [[optics (in computer science)]], where they are often called **Tambara modules** (after [Tambara 2006](#Tamb06), although Tambara was not the first to study them).


## Definition

\begin{definition}
Let $(\mathbf M, i, \odot)$ be a [[monoidal category]], let $\mathbf C$ and $\mathbf D$ be two [[actegory|left $\mathbf M$-actegories]] (in other terminology, left $\mathbf M$-modules). We denote $\mathbf M$ actions by $(-)\cdot (-)$.

A (left) **strong profunctor** is a [[profunctor]] $P \,\colon\, \mathbf C^{op} \times \mathbf D \to \mathbf{Set}$ equipped with a [[indexed set|family]] of [[morphisms]] called (left) *strength*
$$
   s_{a,b,m} \,\colon\, P(a,b) \longrightarrow P(m \cdot a, m \cdot b)
$$
which is [[natural transformation|natural]] in $a$ and $b$ and [[dinatural transformation|dinatural]] in $m$, and satisfies two [[coherence laws]]:

1. $s_{a,b,i} = P(\rho_a, \rho_b^{-1})$, where $\rho$ comes with the [[actegory|module structures]] of $\mathbf C$ and $\mathbf D$.

2. $s_{a,b,m \odot n} = P(\mu^{-1}_{m,n,a}, \mu_{m,n,b}) \circ s_{a,b,m} \circ s_{a,b,n}$ where $\mu$ comes with the [[actegory|module structures]] of $\mathbf C$ and $\mathbf D$.

\end{definition}

A right strong profunctor is defined in almost the exact same way except $\mathbf C$ and $\mathbf D$ are assumed to be right $\mathbf M$-actegories and everything is correspondingly 'done on the other side'.

\begin{definition}
  Suppose now $\mathbf C$ and $\mathbf D$ have both left and right $\mathbf M$-actegories structures.
  A **(bi)strong profunctor** is a profunctor $P : \mathbf C^{op} \times \mathbf D \to \mathbf{Set}$ equipped with compatible left and right strong profunctor structures $s$ and $s'$, i.e. such that they satisfy
  $$
    s'_{m \cdot a, m \cdot b, n} \circ s_{a,b,m} = s_{a \cdot n, b \cdot n, m} \circ s'_{a,b,n}
  $$
\end{definition}

\begin{definition}
  Let $P, Q: \mathbf C^{op} \times \mathbf D \to \mathbf{Set}$ be (left) profunctor.
  A **morphism of profunctors** $\alpha : P \to Q$ is a natural transformation $P \Rightarrow Q$ that commutes with $P$ and $Q$'s strengths:
$$
\alpha_{a,b} \circ s^P_{a,b,m} = s^Q_{a,b,m} \circ \alpha_{m \cdot a,m \cdot b}
$$
\end{definition}

\begin{remark}
  The terminology "Tambara modules" are named after [[Daisuke Tambara]] who studied them in [Tamb06](#Tamb06) to prove that for a [[enriched category|$\mathbf V$-enriched]] category $\mathbf A$, $Z(\mathbf A^{op}, \mathbf V) \cong \mathbf{Tamb}(\mathbf A, \mathbf A)$. However, they have been studied earlier, e.g. see [Paré and Roman 1998](#PareRoman98).
\end{remark}

\begin{remark}
  Both [Tamb06](#Tamb06) and [PS07](#PS07) define "Tambara module" to mean Tambara bimodule. In the optical literature, however, left Tambara modules are called simply modules and they are the one used. This doesn't pose any problem when $\mathbf M$ is *symmetric* monoidal since it's evident how, in that case, any left module structure can be made into a right module structure, so that any left/right module is automatically a bimodule.
\end{remark}

## References

Strong profunctors were defined in:

* {#PareRoman98} [[Robert Paré]] and Leopoldo Rom&#225;n, *Dinatural numbers* (1998), [JPAA](http://www.sciencedirect.com/science/article/pii/S0022404997000364)

* {#Tamb06} [[Daisuke Tambara]], _Distributors on a tensor category_, Hokkaido mathematical journal, 35(2):379–425, 2006.

* [[Bartosz Milewski]], _Profunctor optics: the categorical view_ ([blog post](https://bartoszmilewski.com/2017/07/07/profunctor-optics-the-categorical-view/))

* {#Rom20} [[Mario Román]], _Profunctor optics and traversals_, 2020 ([arXiv](https://arxiv.org/abs/2001.08045))

* {#PS07} [[Craig Pastro]], [[Ross Street]], _Doubles for monoidal categories_, 2007 ([arXiv](https://arxiv.org/abs/0711.1859))

[[!redirects Tambara module]]
[[!redirects Tambara modules]]
[[!redirects Tambara bimodule]]
[[!redirects Tambara bimodules]]
[[!redirects strong profunctors]]
[[!redirects strong distributor]]
[[!redirects strong distributors]]