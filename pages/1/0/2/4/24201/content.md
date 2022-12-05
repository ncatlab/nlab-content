
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


#Contents#
* table of contents
{:toc}

## Idea

On [[localization]] in [[homotopy type theory]].

## Definition

### For a function

Consider a [[function]] $F:S \to T$. We say that a [[type]] $X$ is **$F$-local** if the function

$$\lambda g . g (F) : (S \to X) \to (T \to X)$$

is an [[equivalence of types]].

### For a family of functions

Consider a [[family]] $F:\prod_{(i:I)} S(i) \to T(i)$ of functions. We say that a [[type]] $X$ is **$F$-local** if the function

$$\lambda g . g (F(i)) : (S(i) \to X) \to (T(i) \to X)$$

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

## See also

* [[higher inductive type]]

* [[localization]]

* [[shape modality]], [[axiom of cohesion]]

* [[bracket type]], [[n-truncation modality]]

## References

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* [[Egbert Rijke]], [[Michael Shulman]], [[Bas Spitters]], *Modalities in homotopy type theory* ([arXiv:1706.07526](https://arxiv.org/abs/1706.07526))

* [[Daniel Christensen]], [[Morgan Opie]], [[Egbert Rijke]], [[Luis Scoccola]], *Localization in Homotopy Type Theory* ([arXiv:1807.04155](https://arxiv.org/abs/1807.04155))

[[!redirects localization of a type at a function]]
[[!redirects localization of a type at a family of functions]]