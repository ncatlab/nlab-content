
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

\tableofcontents

## Idea

A [[modal type theory|modal]] [[dependent type theory]] with the [[sharp modality]] $\sharp$ and the [[flat modality]] $\flat$. Spatial type theory which is also a [[homotopy type theory]] is called **spatial homotopy type theory**. 

## Presentation

In this presentation of [[spatial type theory]], we assume a [[dependent type theory]] with crisp term judgments $a::A$ in addition to the usual (cohesive) type and term judgments $A \; \mathrm{type}$ and $a:A$, as well as context judgments $\Xi \vert \Gamma \; \mathrm{ctx}$ where $\Xi$ is a list of crisp term judgments, and $\Gamma$ is a list of cohesive term judgments. A crisp type is a type in the context $\Xi \vert ()$, where $()$ is the empty list of cohesive term judgments. 

### Identity types

In addition, we also assume the dependent type theory has [[typal equality]]:

* Formation rule for identity types:
$$\frac{\Xi \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi \vert \Gamma \vdash a:A \quad \Xi \vert \Gamma \vdash b:A}{\Xi \vert \Gamma \vdash a =_A b \; \mathrm{type}}$$

* Introduction rule for identity types:
$$\frac{\Xi \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi \vert \Gamma \vdash a:A}{\Xi \vert \Gamma \vdash \mathrm{refl}_A(a) : a =_A a}$$

* Elimination rule for identity types:
$$\frac{\Xi \vert \Gamma, x:A, y:A, p:a =_A b \vdash C \; \mathrm{type} \quad \Xi \vert \Gamma, z:A \vdash t:C[z/a, z/b, \mathrm{refl}_A(z)/p] \quad \Xi \vert \Gamma \vdash a:A \quad \Xi \vert \Gamma \vdash b:A \quad \Xi \vert \Gamma \vdash q:a =_A b}{\Xi \vert \Gamma \vdash \mathrm{ind}_{=_A}^{x,y,p.C}(z.t, a, b, q):C[a, b, q/x, y, p]}$$

* Computation rules for identity types:
$$\frac{\Xi \vert \Gamma, x:A, y:A, p:a =_A b \vdash C \; \mathrm{type} \quad \Xi \vert \Gamma, z:A \vdash t:C[z/a, z/b, \mathrm{refl}_A(z)/p] \quad \Xi \vert \Gamma \vdash a:A}{\Xi \vert \Gamma \vdash \beta_{=_A}^{x,y,p.C}(a):\mathrm{ind}_{=_A}^{x,y,p.C}(z.t, a, a, \mathrm{refl}(a)) =_{C[a, a, \mathrm{refl}_A(a)/x, y, p]} t}$$

### Sharp modality

The [[sharp modality]] is given by the following rules:

* Formation rule for sharp types:

$$\frac{\Xi, \Gamma \vert () \vdash A \; \mathrm{type}}{\Xi \vert \Gamma \vdash \sharp A \; \mathrm{type}}\sharp-\mathrm{form}$$

* Introduction rule for sharp types:

$$\frac{\Xi, \Gamma \vert () \vdash a:A}{\Xi \vert \Gamma \vdash a^\sharp:\sharp A}\sharp-\mathrm{intro}$$

* Elimination rule for sharp types:

$$\frac{\Xi \vert () \vdash a:\sharp A}{\Xi \vert \Gamma \vdash a_\sharp:A}\sharp-\mathrm{elim}$$

* Computation rule for sharp types:

$$\frac{\Xi \vert () \vdash a:A}{\Xi \vert \Gamma \vdash \beta_{\sharp A}(a):(a^\sharp)_\sharp =_A a}\sharp-\mathrm{comp}$$

* Uniqueness rule for sharp types:

$$\frac{\Xi \vert () \vdash a:\sharp A}{\Xi \vert \Gamma \vdash \eta_{\sharp A}(a):(a_\sharp)^\sharp =_{\sharp A} a}\sharp-\mathrm{uniq}$$

### Flat modality

The [[flat modality]] is given by the following rules:

* Formation rule for flat types:

$$\frac{\Xi, \Gamma \vert () \vdash A \; \mathrm{type}}{\Xi \vert \Gamma \vdash \flat A \; \mathrm{type}}\flat-\mathrm{form}$$

* Introduction rule for flat types:

$$\frac{\Xi, \Gamma \vert () \vdash a:A}{\Xi \vert \Gamma \vdash a^\flat:\flat A}\flat-\mathrm{intro}$$

* Elimination rule for flat types:

$$\frac{\Xi \vert \Gamma, x:\flat A \vdash C \; \mathrm{type} \quad \Xi \vert \Gamma \vdash M:\flat A \quad \Xi, u::A \vert \Gamma \vdash N : C[u^\flat/x]}{\Xi \vert \Gamma \vdash (\mathrm{let}\; u^\flat \coloneqq M \;\mathrm{in}\; n):C[M/x]}\flat-\mathrm{elim}$$

* Computation rule for flat types:

$$\frac{\Xi \vert \Gamma, x:\flat A \vdash C \; \mathrm{type} \quad \Xi \vert () \vdash M:\flat A \quad \Xi, u::A \vert \Gamma \vdash N : C[u^\flat/x]}{\Xi \vert \Gamma \vdash \beta_{\flat}(M, N):(\mathrm{let}\; u^\flat \coloneqq M \;\mathrm{in}\; N) =_{C[M^\flat/x]} N[M/u]}\flat-\mathrm{comp}$$

## Examples

* [[homotopy type theory]] is trivially a spatial type theory where every type is [[discrete]]

* Some versions of [[simplicial type theory]] are a spatial type theory with an [[op modality]] and a [[twisted arrows modality]]. 

A [[cohesive homotopy type theory]] is a spatial homotopy type theory which additionally has an [[axiom of cohesion]] and a [[shape modality]]. Examples of this include

* [[real-cohesive homotopy type theory]]

## See also

* [[dependent type theory]]

* [[modal type theory]]

* [[cohesive homotopy type theory]]

## References

* [[David Corfield]], *Modal Homotopy Type Theory*, ... [reference to be completed]

* {#GWB25} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *The Yoneda embedding in simplicial type theory* ([arXiv:2501.13229](https://arxiv.org/abs/2501.13229))

A formal presentation of spatial type theory is found in 

* [[Mike Shulman]], *Brouwer's fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))