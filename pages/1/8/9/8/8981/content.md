

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
#### Type theory
+--{: .hide}
[[!include type theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

On a [[local topos]]/[[local (∞,1)-topos]] $\mathbf{H}$, hence equipped with a [[full and faithful (∞,1)-functor|fully faithful]] extra [[right adjoint]] $coDisc$ to the [[global section]] [[geometric morphism]] $(Disc \dashv \Gamma)$,  is induced an  [[idempotent monad]] $\sharp \coloneqq coDisc \circ \Gamma$, a [[modality]] which we call the _sharp modality_. This is itself the [[right adjoint]] in an [[adjoint modality]] with the [[flat modality]] $\flat \coloneqq Disc \circ \Gamma$.

### In type theory

We assume a [[dependent type theory]] with crisp term judgments $a::A$ in addition to the usual (cohesive) type and term judgments $A \; \mathrm{type}$ and $a:A$, as well as context judgments $\Xi \vert \Gamma \; \mathrm{ctx}$ where $\Xi$ is a list of crisp term judgments, and $\Gamma$ is a list of cohesive term judgments. A crisp type is a type in the context $\Xi \vert ()$, where $()$ is the empty list of cohesive term judgments. In addition, we also assume the dependent type theory has [[typal equality]] and [[judgmental equality]]. 

From here, there are two different notions of the sharp modality which could be defined in the type theory, the **strict sharp modality**, which uses [[judgmental equality]] in the [[computation rule]] and [[uniqueness rule]], and the **weak sharp modality**, which uses [[typal equality]] in the [[computation rule]] and [[uniqueness rule]]. When applied to a type they result in **strict sharp types** and **weak sharp types** respectively. The [[natural deduction]] rules for strict and weak sharp types are provided as follows:

* Formation rule for weak and strict sharp types:

$$\frac{\Xi, \Gamma \vert () \vdash A \; \mathrm{type}}{\Xi \vert \Gamma \vdash \sharp A \; \mathrm{type}}\sharp-\mathrm{form}$$

* Introduction rule for weak and strict sharp types:

$$\frac{\Xi, \Gamma \vert () \vdash a:A}{\Xi \vert \Gamma \vdash a^\sharp:\sharp A}\sharp-\mathrm{intro}$$

* Elimination rule for weak and strict sharp types:

$$\frac{\Xi \vert () \vdash a:\sharp A}{\Xi \vert \Gamma \vdash a_\sharp:A}\sharp-\mathrm{elim}$$

* Computation rule for weak and strict sharp types respectively:

$$\frac{\Xi \vert () \vdash a:A}{\Xi \vert \Gamma \vdash \beta_{\sharp A}(a):(a^\sharp)_\sharp =_A a}\sharp-\mathrm{comp}\mathrm{weak} \qquad \frac{\Xi \vert () \vdash a:A}{\Xi \vert \Gamma \vdash (a^\sharp)_\sharp \equiv a:A}\sharp-\mathrm{comp}\mathrm{strict}$$

* Uniqueness rule for weak and strict sharp types respectively:

$$\frac{\Xi \vert () \vdash a:\sharp A}{\Xi \vert \Gamma \vdash \eta_{\sharp A}(a):(a_\sharp)^\sharp =_{\sharp A} a}\sharp-\mathrm{uniq}{weak} \qquad \frac{\Xi \vert () \vdash a:\sharp A}{\Xi \vert \Gamma \vdash (a_\sharp)^\sharp \equiv a:\sharp A}\sharp-\mathrm{uniq}\mathrm{strict}$$

Weak sharp modalities are primarily used in cohesive [[weak type theories]], while strict sharp modalities are typically used in cohesive type theories which are not weak, such as cohesive [[Martin-Löf type theory]] ([[cohesive homotopy type theory]] or cohesive [[higher observational type theory]]. 

## Properties

### Relation to discrete and codiscrete objects

* The [[codiscrete objects]] in a local topos are the [[modal types]] for the sharp modality.

* The [[discrete objects]] in a local topos are the [[modal types]] for the [[flat modality]].

## Related concepts

* [[sharp excluded middle]]

[[!include cohesion - table]]

## References
 {#References}

The terminology of the sharp-modality in the above sense was introduced -- in the language of [[(infinity,1)-toposes|$(\infty,1)$-toposes]] and as part of the axioms on "[[cohesive (infinity,1)-toposes|cohesive $(\infty,1)$-toposes]]" -- in:

* [[Urs Schreiber]], *[[schreiber:differential cohomology in a cohesive topos|Differential cohomology in a cohesive $\infty$-topos]]* (2013)

See also the references at _[[local topos]]_.

Early discussion in view of [[homotopy type theory|homotopy]] [[type theory]] and as part of a set of  axioms for [[cohesive homotopy type theory]] is in

* [[Mike Shulman]], [[Urs Schreiber]], *[[schreiber:Quantum gauge field theory in Cohesive homotopy type theory]]* (2014)

The dedicated type theory formulation with "crisp" types, as part of the formulation of [[real cohesive homotopy type theory]], is due to:

* [[Mike Shulman]], *Brouwer's fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))



[[!redirects sharp modality]]
[[!redirects strict sharp modality]]
[[!redirects weak sharp modality]]

[[!redirects sharp type]]
[[!redirects sharp types]]
[[!redirects strict sharp type]]
[[!redirects strict sharp types]]
[[!redirects weak sharp type]]
[[!redirects weak sharp types]]