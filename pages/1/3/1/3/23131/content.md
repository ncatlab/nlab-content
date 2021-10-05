
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

A **Tambara module** is a [[profunctor]] endowed with additional [[mathematical structure|structure]] that makes it interplay nicely with a [[monoidal category|monoidal]] [[action]]. Tambara modules are used in the theory of [[optics (in computer science)]].


## Definition

\begin{definition}
Let $(\mathbf M, i, \odot)$ be a [[monoidal category]], let $\mathbf C$ and $\mathbf D$ be two [[actegory|left $\mathbf M$-actegories]] (in other terminology, left $\mathbf M$-modules). We denote $\mathbf M$ actions by $(-)\cdot (-)$.

A (left) **Tambara module** is a [[profunctor]] $P \,\colon\, \mathbf C^{op} \times \mathbf D \to \mathbf{Set}$ equipped with a [[indexed set|family]] of [[morphisms]] called (left) *strength*
$$
   s_{a,b,m} \,\colon\, P(a,b) \longrightarrow P(m \cdot a, m \cdot b)
$$
which is [[natural transformation|natural]] in $a$ and $b$ and [[dinatural transformation|dinatural]] in $m$, and satisfies two [[coherence laws]]:

1. $s_{a,b,i} = P(\rho_a, \rho_b^{-1})$, where $\rho$ comes with the [[actegory|module structures]] of $\mathbf C$ and $\mathbf D$.

2. $s_{a,b,m \odot n} = P(\mu^{-1}_{m,n,a}, \mu_{m,n,b}) \circ s_{a,b,m} \circ s_{a,b,n}$ where $\mu$ comes with the [[actegory|module structures]] of $\mathbf C$ and $\mathbf D$.

\end{definition}

This is same thing as (left) **strong profunctors**. 

A right Tambara module is defined in the exact way except $\mathbf C$ and $\mathbf D$ are assumed to be right $\mathbf M$-actegories and everything is correspondigly 'done on the other side'.

\begin{definition}
  Suppose now $\mathbf C$ and $\mathbf D$ have both left and right $\mathbf M$-actegories structures.
  A **Tambara bimodule** is a profunctor $P : \mathbf C^{op} \times \mathbf D \to \mathbf{Set}$ equipped with compatible left and right Tambara module structures $s$ and $s'$, i.e. such that they satisfy
  $$
    s'_{m \cdot a, m \cdot b, n} \circ s_{a,b,m} = s_{a \cdot n, b \cdot n, m} \circ s'_{a,b,n}
  $$
\end{definition}

\begin{definition}
  Let $P, Q: \mathbf C^{op} \times \mathbf D \to \mathbf{Set}$ be (left) Tambara modules.
  A **morphism of Tambara modules** $\alpha : P \to Q$ is a natural transformation $P \Rightarrow Q$ that commutes with $P$ and $Q$'s strenghts:
$$
\alpha_{a,b} \circ s^P_{a,b,m} = s^Q_{a,b,m} \circ \alpha_{m \cdot a,m \cdot b}
$$
\end{definition}

\begin{remark}
  Tambara modules are named after [[Daisuke Tambara]] who introduced them in [Tamb06](#Tamb06) to prove that for a [[enriched category|$\mathbf V$-enriched]] category $\mathbf A$, $Z(\mathbf A^{op}, \mathbf V) \cong \mathbf{Tamb}(\mathbf A, \mathbf A)$.
\end{remark}

\begin{remark}
  Both [Tamb06](#Tamb06) and [PS07](#PS07) define Tambara module to mean Tambara bimodule. In the optical literature, however, left Tambara modules are called simply modules and they are the one used. This doesn't pose any problem when $\mathbf M$ is *symmetric* monoidal since it's evident how, in that case, any left module structure can be made into a right module structure, so that any left/right module is automatically a bimodule.
\end{remark}

## References

* {#Tamb06} [[Daisuke Tambara]], _Distributors on a tensor category_, Hokkaido mathematical journal, 35(2):379–425, 2006.

* [[Bartosz Milewski]], _Profunctor optics: the categorical view_ ([blog post](https://bartoszmilewski.com/2017/07/07/profunctor-optics-the-categorical-view/))

* {#Rom20} [[Mario Román]], _Profunctor optics and traversals_, 2020 ([arXiv](https://arxiv.org/abs/2001.08045))

* {#PS07} [[Craig Pastro]], [[Ross Street]], _Doubles for monoidal categories_, 2007 ([arXiv](https://arxiv.org/abs/0711.1859))
