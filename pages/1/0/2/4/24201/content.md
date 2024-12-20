
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--


\tableofcontents

## Idea

On [[localization]] in [[homotopy type theory]].

## Definition

### Localization at a function

Consider a [[function]] $f:S \to T$. We say that a [[type]] $X$ is **$f$-local** if the function

$$\lambda g . g (f) : (T \to X) \to (S \to X)$$

is an [[equivalence of types]].

The localization of a type $X$ at $f$, $L_f(X)$, is the [[higher inductive type]] generated by 

* the function $\mathrm{tolocal}:X \to L_f(X)$
* the function $\mathrm{localextend}: (S \to L_f(X)) \to (T \to L_f(X))$
* the dependent function 
$$\mathrm{localextension}:\prod_{h:S \to L_f(X)} \prod_{s:S} \mathrm{localextend}(h)(f(s)) = h(s)$$
* the dependent function 
$$\mathrm{localunextension}:\prod_{g:T \to L_f(X)} \prod_{t:T} \mathrm{localextend}(g \circ f)(t) = g(t)$$
* the dependent function 
$$\mathrm{localtriangle}:\prod_{g:T \to L_f(X)} \prod_{s:S} \mathrm{localunextension}(g)(f(s)) = \mathrm{localextension}(g \circ f)(s)$$

### Localization at a type

The localization $L_S(X)$ of a type $X$ at a type $S$ is the localization $L_{u_S^\mathbb{1}}$ of $X$ at the unique function $u_S^\mathbb{1}:S \to \mathbb{1}$ from $S$ to the [[unit type]] $\mathbb{1}$, or equivalently, is the type $L_S(X)$ for which the canonical function $\mathrm{const}:L_S(X) \to (S \to L_S(X))$ is an [[equivalence of types]]. 

### Localization at a family of functions

Consider a [[family]] $f:\prod_{(i:I)} S(i) \to T(i)$ of functions. We say that a [[type]] $X$ is **$F$-local** if the function

$$\lambda g . g (f(i)) : (S(i) \to X) \to (T(i) \to X)$$

is an [[equivalence of types]] for all (i : I).

The following [[higher inductive type]] can be shown to be a [[reflection]] of all types into the local types, constructing the [[localization]] of the category of types at the given family of functions.

    Inductive localize X :=
    | to_local : X -> localize X
    | local_extend : forall (i:I) (h : S i -> localize X),
        T i -> localize X
    | local_extension : forall (i:I) (h : S i -> localize X) (s : S i),
        local_extend i h (f i s) == h s
    | local_unextension : forall (i:I) (g : T i -> localize X) (t : T i),
        local_extend i (g o f i) t == g t
    | local_triangle : forall (i:I) (g : T i -> localize X) (s : S i),
        local_unextension i g (f i s) == local_extension i (g o f i) s.

The first constructor gives a function from `X` to `localize X`, while the other four specify exactly that `localize X` is local (by giving adjoint equivalence data to the function that we want to become an equivalence).  See [this blog post](http://homotopytypetheory.org/2011/12/06/inductive-localization/) for details.  This construction is also already interesting in extensional type theory.

### Localization at a family of types

The localization $L_F(X)$ of a type $X$ at a family of types $F:\prod_{i:I} S(i)$ is the family of localizations $L_F(-) \coloneqq \prod_{i:I} L_{u_{S(i)}^\mathbb{1}}(-)$ of $X$ at the family of unique functions $u_{S(i)}^\mathbb{1}:S(i) \to \mathbb{1}$ from $S(i)$ to the [[unit type]] $\mathbb{1}$, or equivalently, is the family of types $L_{S(i)}(X)$ for which each canonical function $\mathrm{const}:L_{S(i)}(X) \to (S(i) \to L_{S(i)}(X))$ is an [[equivalence of types]]. 

## Examples

* The [[bracket type]] is the localization at the unique function $\mathbb{2} \to \mathbb{1}$ from the [[two-valued type]] to the [[unit type]].

* More generally, the [[n-truncation modality]] is the localization at the unique function $S^{n + 1} \to \mathbb{1}$ from the $(n + 1)$-dimensional [[sphere type]] to the [[unit type]].

* The [[shape modality]] which expresses [[real cohesion]] is the localization at the unique function $\mathbb{R} \to \mathbb{1}$ from the [[Dedekind real numbers]] to the [[unit type]]. 

* The $n$-[[shape modality]] is the localization at the two unique functions $\mathbb{R} \to \mathbb{1}$ and $S^{n + 1} \to \mathbb{1}$. 

* Let $\mathcal{R}$ be an [[Archimedean ordered Artinian local ring]] whose Archimedean subfield $\mathbb{R} \subseteq \mathcal{R}$ is the [[Dedekind real numbers]], and let $\mathcal{D}$ be the type of all [[infinitesimals]] in $\mathcal{R}$. The [[infinitesimal shape modality]] is the localization at the unique function $\mathcal{D} \to \mathbb{1}$. 

## See also

* [[higher inductive type]]

* [[localization]]

* [[shape modality]], [[axiom of cohesion]]

* [[bracket type]], [[set truncation]], [[n-truncation modality]]

* [[localization at an object]]

* [[null type]]

## References

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* [[Egbert Rijke]], [[Michael Shulman]], [[Bas Spitters]], *Modalities in homotopy type theory* ([arXiv:1706.07526](https://arxiv.org/abs/1706.07526))

* [[Daniel Christensen]], [[Morgan Opie]], [[Egbert Rijke]], [[Luis Scoccola]], *Localization in Homotopy Type Theory* ([arXiv:1807.04155](https://arxiv.org/abs/1807.04155))

* [[David Jaz Myers]], Orbifolds as microlinear types in synthetic differential cohesive homotopy type theory ([arXiv:2205.15887](https://arxiv.org/abs/2205.15887))


[[!redirects localization of a type]]
[[!redirects localizations of a type]]

[[!redirects localization of a type at a function]]
[[!redirects localizations of a type at a function]]

[[!redirects localization of a type at a type]]
[[!redirects localizations of a type at a type]]

[[!redirects localization of a type at a family of functions]]
[[!redirects localizations of a type at a family of functions]]