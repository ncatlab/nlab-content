
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

In general, given a [[category]] $\mathcal{C}$ and a [[class]] $W$ of [[morphisms]], one may ask for the _[[localization]]_ $\mathcal{C}[W^{-1}]$, or more specifically for the [[reflective subcategory]] of $W$-[[local objects]] (the [[reflective localization]]). Similarly for variants in [[higher category]], such as _[[localization of an (∞,1)-category]]_.

If $\mathcal{C}$ has [[finite products]], then for a given [[object]] $\mathbb{A} \in \mathcal{C}$, one may take $W \coloneqq W_{\mathbb{A}}$ to be the class of morphisms of the form 

$$
  X \times (\mathbb{A} \overset{\exists!}{\to} \ast)
  \;\;\colon\;\;
  X \times \mathbb{A}
    \overset{p_1}{\longrightarrow}
  X
  \,,
$$

where $X$ is any [[object]], and where $\ast$ is the [[terminal object]], and where $(-) \times (-) \colon \mathcal{C} \times \mathcal{C} \to \mathcal{C}$ denotes the [[Cartesian product]] [[functor]]. 

The [[reflective localization]] at such a class of morphisms $W_{\mathbb{A}}$ is often referred to as _homotopy localization at the object $\mathbb{A}$_ or similar. 

The idea is that if $\mathbb{A}$ is, or is regarded as, an [[interval object]], then [[left homotopies]] between morphisms $X \to Y$ are, or would be, given by morphisms out of $X \times \mathbb{A}$, and hence forcing the projections $X \times \mathbb{A} \to X$ to be equivalences means forcing all morphisms to be _[[homotopy invariance|homotopy invariant]]_ with respect to $\mathbb{A}$.

Typically this is considered in the case that $\mathcal{C}$ is a [[locally presentable category]] with a [[small set]] of [[generators and relations|generating objects]] $G_i$ such that it becomes sufficient to enforce the localization only on the resulting [[small set]] of [[morphisms]] of the form $G_i \times (\mathbb{A} \to \ast)$.

## Examples

* The localization of [[smooth ∞-groupoids]] at the [[real line]] $\mathbb{R}^1$ is equivalently ([[geometrically discrete ∞-groupoids|geometrically discrete]]) [[∞-groupoids]].

* The localization of the [[(∞,1)-category of (∞,1)-sheaves]] on the [[Nisnevich site]] at the [[affine line]] $\mathbb{A}^1$ is known as  _[[A1-homotopy theory]]_.

[[!redirects homotopy localizations]]

[[!redirects homotopy localization at an object]]
[[!redirects homotopy localizations at an object]]

[[!redirects localization at an object]]
[[!redirects localizations at an object]]

[[!redirects localization at objects]]
[[!redirects localizations at objects]]
