+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

The _circle type_ is an [[axiom|axiomatization]] of the [[homotopy type]] of the ([[shape modality|shape]] of) the [[circle]] in the context of [[homotopy type theory]].

## Definition

As a [[higher inductive type]], the circle is given by

    Inductive Circle : Type
      | base : Circle
      | loop : Id Circle base base

This says that the type is inductively constructed from 

1. a [[term]] of circle type whose [[semantics|interpretation]] is as the [[base point]] of the circle, 

1. a term of the [[identity type]] of paths between these two terms, which interprets as the 1-cell of the circle

   $$
     base \stackrel{loop}{\to} base
     \,
   $$

   Hence a non-constant path from the base point to itself.

### In natural deduction

Let $\mathrm{Id}_A(a, b)$ denote the [[identification type]] between elements $a:A$ and $b:A$ of type $A$, and let $\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)$ denote the [[heterogeneous identification type]] between elements $y:B(a)$ and $z:B(b)$ of type family $x:A \vdash B(x)$, given elements $a:A$ and $b:A$ and [[identification]] $p:\mathrm{Id}_A(a, b)$. Let $\mathrm{apd}_{x:A.B(x)}(f, a, b, p)$ denote the [[dependent function application]] of the [[dependent function]] $f:\prod_{x:A} B(x)$ to the [[identification]] $p:\mathrm{Id}_A(a, b)$

In the [[natural deduction]] formulation of [[dependent type theory]], the circle type is given by the following [[inference rules]]:

Formation rules for the circle type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash S^1 \; \mathrm{type}}$$

Introduction rules for the circle type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash *:S^1} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathcal{l}:\mathrm{Id}_{S^1}(*,*)}$$

Elimination rules for the circle type:
$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_*:C(*) \quad \Gamma \vdash c_\mathcal{l}:\mathrm{hId}_{x:S^1.C(x)}(*, *, \mathcal{l}, c_*, c_*)}{\Gamma, x:S^1 \vdash \mathrm{ind}_{S^1}^{x:S^1.C(x)}(c_*, c_\mathcal{l})(x):C(x)}$$

Computation rules for the circle type:

* Judgmental computation rules
$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_*:C(*) \quad \Gamma \vdash c_\mathcal{l}:\mathrm{hId}_{x:S^1.C(x)}(*, *, \mathcal{l}, c_*, c_*)}{\Gamma \vdash \mathrm{ind}_{S^1}^{x:S^1.C(x)}(c_*, c_\mathcal{l})(*) \equiv c_*:C(*)}$$

$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_*:C(*) \quad \Gamma \vdash c_\mathcal{l}:\mathrm{hId}_{x:S^1.C(x)}(*, *, \mathcal{l}, c_*, c_*)}{\Gamma \vdash \mathrm{apd}_{x:S^1.C(x)}(\mathrm{ind}_{S^1}^{x:S^1.C(x)}(c_*, c_\mathcal{l}), *, *, \mathcal{l}) \equiv c_\mathcal{l}:\mathrm{hId}_{x:S^1.C(x)}(*, *, \mathcal{l}, c_*, c_*)}$$

* Propositional computation rules
$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_*:C(*) \quad \Gamma \vdash c_\mathcal{l}:\mathrm{hId}_{x:S^1.C(x)}(*, *, \mathcal{l}, c_*, c_*)}{\Gamma \vdash \beta_{S^1}^{*}(c_*, c_\mathcal{l}):\mathrm{Id}_{C(*)}(\mathrm{ind}_{S^1}^{x:S^1.C(x)}(c_*, c_\mathcal{l})(*), c_*)}$$

$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_*:C(*) \quad \Gamma \vdash c_\mathcal{l}:\mathrm{hId}_{x:S^1.C(x)}(*, *, \mathcal{l}, c_*, c_*)}{\Gamma \vdash \beta_{S^1}^{\mathcal{l}}(c_*, c_\mathcal{l}):\mathrm{Id}_{\mathrm{hId}_{x:S^1.C(x)}(*, *, \mathcal{l}, c_*, c_*)}(\mathrm{apd}_{x:S^1.C(x)}(\mathrm{ind}_{S^1}^{x:S^1.C(x)}(c_*, c_\mathcal{l}), *, *, \mathcal{l}), c_\mathcal{l})}$$

Uniqueness rules for the circle type:
$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c:\prod_{x:S^1} C(x) \quad \Gamma \vdash p:S^1 \quad \Gamma \vdash l:\mathrm{Id}_{S^1}(p, p)}{\Gamma\vdash \eta_{S^1}(c, p, l):\mathrm{Id}_{C(p)}(c,\mathrm{ind}_{S^1}^{x:S^1.C(x)}(c(p), \mathrm{apd}_{x:S^1.C(x)}(c, p, p, l))}$$

The elimination rules and the propositional computation and uniqueness rules for the circle type state that the circle type satisfy the **dependent universal property of the circle type**. If the dependent type theory also has [[dependent sum types]] and [[product types]], allowing one to define the [[uniqueness quantifier]], the dependent universal property of the circle type could be simplified to the following rule:

$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_*:C(*) \quad \Gamma \vdash c_\mathcal{l}:\mathrm{hId}_{x:S^1.C(x)}(*, *, \mathcal{l}, c_*, c_*)}{\Gamma \vdash \mathrm{up}_{S^1}^{x:S^1.C(x)}(c_*, c_\mathcal{l}):\exists!c:\prod_{x:S^1} C(x).\mathrm{Id}_{C(*)}(c(*), c_*) \times \mathrm{Id}_{\mathrm{hId}_{x:S^1.C(x)}(*, *, \mathcal{l}, c_*, c_*)}(\mathrm{apd}_{x:S^1.C(x)}(c, c_*, c_*, c_\mathcal{l}), c_\mathcal{l})}$$

### As a suspension

The circle type could also be defined as the [[suspension type]] $\Sigma \mathbf{2}$ of the type of [[booleans]] $\mathbf{2}$. 

### As a coequalizer

The circle type could also be defined as the [[coequalizer type]] of any two [[endofunctions]] on the [[unit type]]

$$\mathbf{1} \rightrightarrows \mathbf{1} \to S^1$$

Also, following [[synthetic homotopy theory]], the [[circle type]] $S^1$ is the [[coequalizer type]] of the pair of functions on the [[homotopical real numbers type]]

$$
R\underoverset{\quad s \quad}{\mathrm{id}_R}{\rightrightarrows}R \to S^1
$$

### Using torsors 

The circle can also be defined without HITs using only univalence, as the type of $\mathbb{Z}$-torsors.  One can then prove that this type satisfies the same induction principle (propositionally).  This is due to [[Dan Grayson]].

## Properties 
 {#Properties}

### Induction and recursion principles

Its [[induction principle]] says (e.g. [UFP13, p. 177](#UFP13)) that for 

* any $P \colon S^1 \to Type$ 

* equipped with a point $base' \colon P(base)$ 

* and a [[dependent identification|dependent path]] $loop' \,\colon\, base' =_{loop} base'$, 

there is $f:\prod_{(x:S^1)} P(x)$ such that:

$$f(base)=base'\qquad apd_f(loop) = loop'$$

As a special case, its [[recursion principle]] says that given any type $X$ with a point $x:X$ and a loop $l:x=x$, there is $f:S^1 \to X$ with 

$$f(base)=x\qquad ap_f(loop)=l$$

### Extensionality principle of the circle type

The extensionality principle of the circle type says that there is an equivalence of types between the identification type $\mathrm{Id}_S^1(*,*)$ and the type of integers $\mathbb{Z}$:

$$\mathrm{ext}_S^1:\mathrm{Id}_S^1(*,*) \simeq \mathbb{Z}$$

Equivalently, that the [[loop space type]] $\Omega(S^1, *)$ is equivalent to the [[integers]]. 

Thus, the extensionality principle of the circle type implies that the integers and thus the natural numbers are [[contractible types]] if [[axiom K]] or [[uniqueness of identity proofs]] hold for the entire type theory. If the extensionality principle of the natural numbers also hold in the type theory, then every type is contractible. 

One could prove the extensionality principle of the circle type, given a [[univalent universe]] where the circle is small relative to the universe. The [[HoTT book]] provides a number of such proofs. 

### H-space structures on the circle type

The type of [[H-spaces]] on the circle type is a [[contractible type]]. 

## Related concepts

* [[circle]], [[unit circle]], [[circle group]], [[circle object]]

* [[interval type]]

* [[homotopical real numbers type]]

* [[minimal simplicial circle]]

* [[suspension type]]

* [[sphere type]]

* [[homotopy groups of spheres]]

* [[Jordan curve]]

* [[lemniscate type]]


## References
 {#References}

The formalization of the [[shape modality|shape]] [[homotopy type]] $&#643; S^1 \simeq \mathbf{B}\mathbb{Z}$ of the circle as a [[higher inductive type]] in [[homotopy type theory]], along with a proof that $\Omega &#643;S^1\simeq {\mathbb{Z}}$ (and hence $\pi_1(&#643;S^1) \simeq \mathbb{Z}$):

* {#LicataShulman13} [[Dan Licata]], [[Mike Shulman]], *Calculating the Fundamental Group of the Circle in Homotopy Type Theory*, LICS '13: Proceedings of the 2013 28th Annual ACM/IEEE Symposium on Logic in Computer Science June 2013 ([arXiv:1301.3443](http://arxiv.org/abs/1301.3443), [doi:10.1109/LICS.2013.28](https://doi.org/10.1109/LICS.2013.28))

  > blog announcements: 

  > [A formal proof that $\pi_1(S^1) = \mathbb{Z}$](https://homotopytypetheory.org/2011/04/29/a-formal-proof-that-pi1s1-is-z/)

  > [A simpler proof that $\pi_1(S^1) = \mathbb{Z}$](http://homotopytypetheory.org/2012/06/07/a-simpler-proof-that-%cf%80%e2%82%81s%c2%b9-is-z/)

Formalization in [[proof assistants]]:

in [[Coq]]:

* The HoTT Coq library: [theories/hit/Circle.v](https://github.com/HoTT/HoTT/blob/master/theories/hit/Circle.v)

in [[Agda]]:

* The HoTT Agda library: [homotopy/LoopSpaceCircle.agda](https://github.com/HoTT/HoTT-Agda/blob/2.0/homotopy/LoopSpaceCircle.agda)

Exposition and review:

* {#UFP13} [[Univalent Foundations Project]], §8.1 *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

Alternative construction of the circle type as the type of $\mathbb{Z}$-torsors:

* {#BezemBuchholtzGraysonShulman19} [[Marc Bezem]], [[Ulrik Buchholtz]], [[Daniel Grayson]], [[Michael Shulman]], _Construction of the Circle in UniMath_, Journal of Pure and Applied Algebra Volume 225, Issue 10, October 2021, 106687 ([arXiv:1910.01856](https://arxiv.org/abs/1910.01856))

Alternative construction of the circle type as a coequalizer:

* {#Shulman15} [[Mike Shulman]], Section 9 of  _Brouwer's fixed-point theorem in real-cohesive homotopy type theory_, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

For the fact that the type of H-space structures on a circle type is contractible:

* [[Ulrik Buchholtz]], [[J. Daniel Christensen]], [[Jarl G. Taxerås Flaten]], [[Egbert Rijke]], *Central H-spaces and banded types* &lbrack;[arXiv:2301.02636](https://arxiv.org/abs/2301.02636)&rbrack;

[[!redirects circle type]]
[[!redirects circle types]]

[[!redirects dependent universal property of the circle type]]
[[!redirects dependent universal property of circle types]]