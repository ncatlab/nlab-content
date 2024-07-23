+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Equivariant higher algebra
+--{: .hide}
[[!include equivariant higher algebra - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Content#
* table of contents
{:toc}

## Idea

An _equivariant symmetric monoidal category_ ([Hill-Hopkins 16](#HillHopkins16)) is like a [[symmetric monoidal category]] but with the symmetric monoidal [[tensor product]] generalized to symmetric monoidal powers indexed by [[finite set|finite]] [[G-sets]], for some [[group]] $G$.

Motivating applications come from [[equivariant homotopy theory]].

## Definition in terms of $\infty$-categories

\begin{definition}
  If $\mathcal{T}$ is an [[orbital ∞-category]] and $\mathrm{Span}(\mathbb{F}_{\mathcal{T}})$ its [[Burnside category]], then the $\infty$-category of **small $\mathcal{T}$-symmetric monoidal $\infty$-categories** is
  $$
    \mathrm{Cat}_{\mathcal{T}}^{\otimes} := \mathrm{Fun}^{\times}(\mathrm{Span}(\mathbb{F}_{\mathcal{T}}), \mathrm{Cat}_{\infty}).
  $$
  More generally, if $I \subset \mathbb{F}_{\mathcal{T}}$ is a [[indexing system|weak indexing category]], then $(\mathbb{F}_{\mathcal{T}}, \mathbb{F}_{\mathcal{T}}, I) \subset (\mathbb{F}_{\mathcal{T}}, \mathbb{F}_{\mathcal{T}}, \mathbb{F}_{\mathcal{T}})$ is a sub-algebraic triple in the sense of [Barwick](#Barwick14), so there is a [[Burnside category]] $\mathrm{Span}_I(\mathbb{F}_{\mathcal{T}}) \subset \mathrm{Span}(\mathbb{F}_{\mathcal{T}})$ whose forward maps are in $I$, and we define the $\infty$-category of **small $I$-symmetric monoidal $\infty$-categories** to be
  $$
    \mathrm{Cat}_{I}^{\otimes} := \mathrm{Fun}^{\times}(\mathrm{Span}_I(\mathbb{F}_{\mathcal{T}}), \mathrm{Cat}_{\infty}).
  $$
\end{definition}
In particular, $\mathcal{T}$-symmetric monoidal $\infty$-categories are simply $\mathcal{T}$-commutative monoids in $\mathrm{Cat}_\infty$.

\begin{remark}
  In the case $\mathcal{T} = \mathcal{O}_G$ is the [[orbit category]] of a finite group, these are called _$G$-symmetric monoidal $\infty$-categories_, which is a source of potential confusion, as they are homotopical lifts of the symmetric monoidal [[Mackey functors]] considered in ([Hill-Hopkins 16](#HillHopkins16)).
\end{remark}



## Related concepts

* [[G-commutative monoid]]

* [[G-operad]]

* [[Parametrized Higher Category Theory and Higher Algebra]]

## References

* {#Barwick14} [[Clark Barwick]], _Spectral Mackey functors and equivariant algebraic K-theory (I)_, Adv. Math., 304:646–727,  2017 ([doi:10.1016/j.aim.2016.08.043](https://doi.org/10.1016/j.aim.2016.08.043), [arXiv:1404.0108](http://arxiv.org/abs/1404.0108))

* {#HillHopkins16} [[Michael Hill]], [[Michael Hopkins]], _Equivariant symmetric monoidal structures_ ([arXiv:1610.03114](https://arxiv.org/abs/1610.03114))

* [[Denis Nardin]], [[Jay Shah]], _Parametrized and equivariant higher algebra_, (2022) ([arxiv:2203.00072](https://arxiv.org/abs/2203.00072))



[[!redirects equivariant symmetric monoidal categories]]

[[!redirects G-symmetric monoidal category]]
[[!redirects G-symmetric monoidal ∞-category]]
[[!redirects G-symmetric monoidal ∞-categories]]