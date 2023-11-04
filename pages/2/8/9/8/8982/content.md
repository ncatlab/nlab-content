


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

There are multiple ways to define the flat modality in type theory, by using [[axioms]] and unjustified inference rules, and by using [[natural deduction]] [[inference rules]]. There are advantages and disadvantages to both:

* The [[natural deduction]] [[inference rules]] for flat modalities are simple; they involve the usual 4 rules for positive types: [[formation rules]], [[introduction rules]], [[elimination rules]], and [[computation rules]], and they could be constructed for all types. However, the syntax of the type theory itself becomes significantly more complex compared to vanilla [[dependent type theory]]. One needs, in addition to element judgments $x:A$, crisp element judgments $x::A$, as well as some way of distinguishing between element judgments and crisp element judgments in the [[context]] such as [[split contexts]]. 

* When using [[axioms]] or unjustified inference rules, the flat modality could be defined in vanilla [[dependent type theory]]. However, one needs the [[sharp modality]] and a [[type universe]] $U$ already defined in the dependent type theory, and the flat modality is only defined for types in the universe $\sharp U$, rather than all possible types. 

#### Natural deduction inference rules

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

#### Axioms for the flat modality

See [Shulman & Schreiber 2014](#ShulmanSchreiber14) for the time being.

...

We assume that the dependent type theory has the [[sharp modality]] $\sharp$ defined by natural deduction inference rules and a [[Tarski universe]] $(U, T)$. The codiscrete universe is given by the type $\sharp U$ with type families $A:\sharp U \vdash \sharp(T)(A)$ The axioms are given by 

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, A:\sharp U \vdash \mathrm{escape}(A):U} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma, A:\sharp U \vdash T(\mathrm{escape}(A)) \equiv \sum_{B:\sharp \sum_{X:U} T(X)} \sharp(\pi_1)(B) =_{\sharp U} A}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, A:\sharp U \vdash \mathrm{eIsDisc}(A) \; \mathrm{type}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma, A:\sharp U \vdash \mathrm{eIsDiscIsProp}(A):\mathrm{isProp}(\mathrm{eIsDisc}(A))}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, A:\sharp U \vdash \flat A:\sharp U}$$ 

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, A:\sharp U \vdash \mathrm{flatIsDisc}(A):\mathrm{eIsDisc}(\sharp(T)(\flat A))}$$ 

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, A:\sharp U \vdash \epsilon(A):T(\mathrm{escape}(\sharp(\flat A \to A)))}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, A:\sharp U, B:\sharp U \vdash \mathrm{flr}(A, B):\mathrm{eIsDisc}(A) \to \mathrm{isEquiv}(\lambda f:T(\mathrm{escape}(\sharp(A \to \flat B))).\epsilon(B) \circ f)}$$ 

...

## Properties

### Relation to discrete and codiscrete objects

* The [[codiscrete objects]] in a local topos are the [[modal types]] for the [[sharp modality]].

* The [[discrete objects]] in a local topos are the [[modal types]] for the flat modality.

## Related concepts

[[!include cohesion - table]]

## References

The terminology of the flat-modality in the above sense was introduced -- in the language of [[(infinity,1)-toposes|$(\infty,1)$-toposes]] and as part of the axioms on "[[cohesive (infinity,1)-toposes|cohesive $(\infty,1)$-toposes]]" -- in:

* [[Zoran Škoda]], [[Urs Schreiber]], [§7.4.2](https://arxiv.org/pdf/1004.2472.pdf#page=31) of: *Categorified symmetries* &lbrack;[arXiv:1004.2472](https://arxiv.org/abs/1004.2472)&rbrack;

* [[Urs Schreiber]], *[[schreiber:differential cohomology in a cohesive topos|Differential cohomology in a cohesive $\infty$-topos]]* (2013)

See also the references at _[[local topos]]_.

Early discussion in view of [[homotopy type theory|homotopy]] [[type theory]] and as part of a set of  axioms for [[cohesive homotopy type theory]] is in

* {#ShulmanSchreiber14} [[Mike Shulman]], [[Urs Schreiber]], *[[schreiber:Quantum gauge field theory in Cohesive homotopy type theory]]* (2014)

The dedicated type theory formulation with "crisp" types, as part of the formulation of [[real cohesive homotopy type theory]], is due to:

* [[Mike Shulman]], *Brouwer's fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

[[!redirects flat modality]]
[[!redirects flat type]]
[[!redirects flat types]]

[[!redirects strict flat modality]]
[[!redirects strict flat type]]
[[!redirects strict flat types]]

[[!redirects weak flat modality]]
[[!redirects weak flat type]]
[[!redirects weak flat types]]