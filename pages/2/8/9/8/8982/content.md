


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

On a [[local topos]]/[[local (∞,1)-topos]] $\mathbf{H}$, hence with extra [[full and faithful (infinity,1)-functor|fully faithful]] [[right adjoint]] $coDisc$ to the [[global section geometric morphism]] $(Disc \dashv \Gamma)$, is canonically induced the [[idempotent monad|idempotent]] [[comonad]] $\flat \coloneqq Disc\circ \Gamma$. This [[modality]] sends for instance pointed [[connected]] objects $\mathbf{B}G$ to [[coefficients]] $\flat \mathbf{B}G$ for [[flat principal ∞-connections]], and may therefore be referred to as the _flat modality_. It is itself the [[left adjoint]] in an [[adjoint modality]] with the [[sharp modality]] $\sharp \coloneqq coDisc \circ \Gamma$. If $\mathbf{H}$ is in addition a [[cohesive (∞,1)-topos]] then it is also the [[right adjoint]] in an [[adjoint modality]] with the [[shape modality]] $\int$.

### In type theory

We assume a [[dependent type theory]] with crisp term judgments $a::A$ in addition to the usual (cohesive) type and term judgments $A \; \mathrm{type}$ and $a:A$, as well as context judgments $\Xi \vert \Gamma \; \mathrm{ctx}$ where $\Xi$ is a list of crisp term judgments, and $\Gamma$ is a list of cohesive term judgments. A crisp type is a type in the context $\Xi \vert ()$, where $()$ is the empty list of cohesive term judgments. In addition, we also assume the dependent type theory has [[typal equality]] and [[judgmental equality]]. 

From here, there are two different notions of the flat modality which could be defined in the type theory, the **strict flat modality**, which uses [[judgmental equality]] in the [[computation rule]] and [[uniqueness rule]], and the **weak flat modality**, which uses [[typal equality]] in the [[computation rule]] and [[uniqueness rule]]. When applied to a type they result in **strict flat types** and **weak flat types** respectively. The [[natural deduction]] rules for strict and weak flat types are provided as follows:

* Formation rule for weak and strict flat types:

$$\frac{\Xi, \Gamma \vert () \vdash A \; \mathrm{type}}{\Xi \vert \Gamma \vdash \flat A \; \mathrm{type}}\flat-\mathrm{form}$$

* Introduction rule for weak and strict flat types:

$$\frac{\Xi, \Gamma \vert () \vdash a:A}{\Xi \vert \Gamma \vdash a^\flat:\flat A}\flat-\mathrm{intro}$$

* Elimination rule for weak and strict flat types:

$$\frac{\Xi \vert \Gamma, x:\flat A \vdash C \; \mathrm{type} \quad \Xi \vert \Gamma \vdash M:\flat A \quad \Xi, u::A \vert \Gamma \vdash N : C[u^\flat/x]}{\Xi \vert \Gamma \vdash (\mathrm{let}\; u^\flat \coloneqq M \;\mathrm{in}\; n):C[M/x]}\flat-\mathrm{elim}$$

* Computation rule for weak and strict flat types respectively:

$$\frac{\Xi \vert \Gamma, x:\flat A \vdash C \; \mathrm{type} \quad \Xi \vert () \vdash M:\flat A \quad \Xi, u::A \vert \Gamma \vdash N : C[u^\flat/x]}{\Xi \vert \Gamma \vdash (\mathrm{let}\; u^\flat \coloneqq M \;\mathrm{in}\; N) \equiv N[M/u]:C[M^\flat/x]}\flat-\mathrm{comp}\mathrm{strict}$$

$$\frac{\Xi \vert \Gamma, x:\flat A \vdash C \; \mathrm{type} \quad \Xi \vert () \vdash M:\flat A \quad \Xi, u::A \vert \Gamma \vdash N : C[u^\flat/x]}{\Xi \vert \Gamma \vdash \beta_{\flat}(M, N):(\mathrm{let}\; u^\flat \coloneqq M \;\mathrm{in}\; N) =_{C[M^\flat/x]} N[M/u]}\flat-\mathrm{comp}\mathrm{weak}$$

Weak flat modalities are primarily used in cohesive [[objective type theories]], while strict flat modalities are typically used in cohesive type theories with [[judgmental equality]], such as cohesive [[Martin-Löf type theory]] ([[cohesive homotopy type theory]] or cohesive [[higher observational type theory]]. 

## Properties

### Relation to discrete and codiscrete objects

* The [[codiscrete objects]] in a local topos are the [[modal types]] for the [[sharp modality]].

* The [[discrete objects]] in a local topos are the [[modal types]] for the flat modality.

## Related concepts

[[!include cohesion - table]]

## References

The terminology of the flat-modality in the above sense was introduced -- in the language of [[(infinity,1)-toposes|$(\infty,1)$-toposes]] and as part of the axioms on "[[cohesive (infinity,1)-toposes|cohesive $(\infty,1)$-toposes]]" -- in:

* [[Urs Schreiber]], *[[schreiber:differential cohomology in a cohesive topos|Differential cohomology in a cohesive $\infty$-topos]]* (2013)

See also the references at _[[local topos]]_.

Early discussion in view of [[homotopy type theory|homotopy]] [[type theory]] and as part of a set of  axioms for [[cohesive homotopy type theory]] is in

* [[Mike Shulman]], [[Urs Schreiber]], *[[schreiber:Quantum gauge field theory in Cohesive homotopy type theory]]* (2014)

The dedicated type theory formulation with "crisp" types, as part of the formulation of [[real cohesive homotopy type theory]], is due to:

* [[Mike Shulman]], *Brouwer's fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))