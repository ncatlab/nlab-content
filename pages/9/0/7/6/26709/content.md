+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Let $\mathcal{S}_G$ be the [[(∞,1)-category]] of [[G-spaces]], and let $\mathcal{O}_G$ be the [[orbit category]].
[[Elmendorf's theorem]] provides an equivalence $\mathcal{S}_G \simeq \mathrm{Fun}(\mathcal{O}_G^{\op},\mathcal{S})$. 
The starting point of [[Parametrized Higher Category Theory and Higher Algebra]] is to define $G$-$\infty$-categories so that they satisfy [[Elmendorf's theorem]].

## Definition

\begin{definition}
  The [[∞-category]] of **small $G$-$\infty$-categories** is
  $$ \mathrm{Cat}_{G,\infty} \coloneqq \mathrm{Fun}(\mathcal{O}_G^{\op}, \mathrm{Cat}_\infty).$$
\end{definition}

More generally, often $\mathcal{T}$ will be an [[orbital ∞-category]]; in any case, we make the analogous definition.

\begin{definition}
  If $\mathcal{T}$ is an [[(∞,1)-category]], then the [[(∞,1)-category]] of **small $\mathcal{T}$-$\infty$-categories** is
  $$
     \mathrm{Cat}_{\mathcal{T},\infty} \coloneqq \mathrm{Fun}(\mathcal{T}^{\op}, \mathrm{Cat}_\infty).
  $$
\end{definition}

## Examples

#### (Genuine) $G$-spaces

$G$-set induction furnishes an equivalence of categories $\mathbb{F}_H \xrightarrow\sim \mathbb{F}_{G,/[G/H]}$, which preserves and reflects transitivity;
in particular, it restricts to an equivalence of [[orbit categories]] $\mathcal{O}_H \xrightarrow\sim \mathcal{O}_{G, [G/H]}$, with which we will conflate these two categories.

Using this, the [[universal fibration of (infinity,1)-categories|universal fibration]] functor $\mathcal{O}_{-} = \mathcal{O}_{G, /-}:\mathcal{O} \rightarrow \Cat_{\infty}$ is a $G$-object in whose $H$-value is $\mathcal{O}_H$. 
By passing to presheaves of spaces fiberwise, we use this to define the **$G$-$\infty$-category of $G$-spaces**
$$
  \underline{\mathcal{S}}_G:
    \mathcal{O}_G^{\op} 
      \xrightarrow{\;\;\;\; \mathcal{O}_{(-)} \;\;\;\; } 
    \mathrm{Cat}_\infty^{\op} 
      \xrightarrow{\;\;\;\; \mathrm{Psh}\;\;\;\; } 
    \mathrm{Cat}_\infty.
$$  

Unwinding definitions, the following proposition is a form of [[Elmendorf's theorem]].
\begin{proposition}
  The $H$-value of the [[G-∞-category]] of $G$-spaces is the $\infty$-category $\mathcal{S}_H$ of [[G-space|H-spaces]], and the induced functor $\Res_H^G:\mathcal{S}_G \rightarrow \mathcal{S}_H$ is restriction. 
\end{proposition}

Thus $G$-functors out of $\underline{\mathcal{S}}_G$ are usually interpretable as collections of functors out of $(\mathcal{S}_H)$ which intertwine with restriction. 


## Related concepts

* [[G-space]]

* [[equivariant homotopy theory]]

* [[Parametrized Higher Category Theory and Higher Algebra]], [[orbital ∞-category]], [[equivariant symmetric monoidal category]]

## References

* {#PHCTI} [[Clark Barwick]], Emanuele Dotto, [[Saul Glasman]], [[Denis Nardin]], [[Jay Shah]], _Parametrized higher category theory and higher algebra: Expos&#233; I &#8211; Elements of parametrized higher category theory_, ([arXiv:1608.03657](https://arxiv.org/abs/1608.03657))

* {#Shah18} [[Jay Shah]], _Parametrized higher category theory_, ([arXiv:1809.05892](https://arxiv.org/abs/1809.05892))

* [[Jay Shah]], _Parametrized higher category theory II: Universal constructions_, ([arXiv:2109.11954](https://arxiv.org/abs/2109.11954))

[[!redirects G-∞-categories]]

[[!redirects G-category]]
[[!redirects G-categories]]