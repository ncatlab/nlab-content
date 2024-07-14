

#Content#
* table of contents
{:toc}

## Idea

$d$-operads are to [[∞-operads]] as $d$-categories are to [[∞-categories]];
just as $d$-categories are simply $\infty$-categories whose mapping spaces are [[homotopy n-type|$(d-1)$-truncated]], $d$-operads are simply $\infty$-categories whose (multi)morphism spaces are [[homotopy n-type|$(d-1)$-truncated]].

## Definitions

\begin{definition}
  Fix $n \in \mathbb{N}$ a [[natural number]]
  An [[∞-operad|$\infty$-operad]] $\mathcal{O}^{\otimes}$ is **essentially $d$** (or a **$d$-operad**) if, for all colors $X_1,\dots,X_n,Y \in \mathcal{O}$, the space $\mathrm{Mul}_{\mathcal{O}}(X_1,\dots,X_n;Y)$ is [[homotopy n-type|$(d-1)$-truncated]] 
\end{definition}

Let $\mathrm{Op}_d \subset \mathrm{Op}_{\infty}$ be the [[full subcategory]] spanned by [[d-operads]].

\begin{proposition}
  $\mathrm{Op}_d \subset \mathrm{Op}_\infty$ is a [[reflective sub-(infinity,1)-category|localizing subcategory]].
\end{proposition}

We refer to the localization functor $h_d:\mathrm{Op}_\infty \rightarrow \mathrm{Op}_d$ as the **homotopy $d$-operad functor**.

## Properties

\begin{proposition}
  A [[symmetric monoidal ∞-category]] is essentially $d$ when regarded as an [[∞-operad]] if and only if its underlying $\infty$-category is a $d$-category.
\end{proposition}

\begin{proposition}
  An $\infty$-operad $\mathcal{O}^{\otimes}$ is $d+1$-connected if and only if the canonical map $h_{d} \mathcal{O}^{\otimes} \rightarrow \mathbb{E}_\infty^{\otimes}$ is an equivalence.
\end{proposition}

## Examples

* [[En-operad|$\mathbb{E}_0$]] and [[En-operad|$\mathbb{E}_\infty$]] are 0-operads. 
* the operadic nerve of an [[operad]] is a $1$-operad.
* [[En-operad|$\mathbb{E}_2$]] is a $2$-operad. 

## Related concepts

* [[∞-operad]]

## References


* [[Tomer Schlank]], [[Lior Yanovski]]: _On d-Categories and d-Operads_ ([arXiv:1902.04061v1](https://arxiv.org/abs/1902.04061v1))

[[!redirects d-operads]]