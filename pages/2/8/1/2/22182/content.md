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

1. a term of the [[identification type]] between these two terms, whose interpretation is as the 1-cell of the circle

   $$
     base \stackrel{loop}{\to} base
     \,
   $$

   Hence as a non-constant path from the base point to itself.

### In natural deduction

Let $a =_A b$ denote the [[identification type]] between elements $a:A$ and $b:A$ of type $A$, and let $y =_{x:A.B(x)}^{(a, b, p)} z$ denote the [[heterogeneous identification type]] between elements $y:B(a)$ and $z:B(b)$ of type family $x:A \vdash B(x)$, given elements $a:A$ and $b:A$ and [[identification]] $p:a =_A b$. Let $\mathrm{apd}_f(a, b, p)$ denote the [[dependent function application]] of the [[dependent function]] $f:\prod_{x:A} B(x)$ to the [[identification]] $p:a =_A b$

In the [[natural deduction]] formulation of [[dependent type theory]], the circle type is given by the following [[inference rules]]:

First the rule that defines the circle type itself in some context $\Gamma$.

**[[type formation]]**
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash S^1 \; \mathrm{type}}$$

Now the basic “introduction” rule, which says that the circle type consists of a base point $\mathrm{base}:S^1$ and a loop identification $\mathrm{loop}:\mathrm{base} =_{S^1} \mathrm{base}$.

**[[term introduction]]**:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{base}:S^1} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{loop}:\mathrm{base} =_{S^1} \mathrm{base}}$$

#### Induction principle of the circle type

Then there are the “elimination” rule and the “computation” or [[beta-reduction|β-reduction]] rule of the circle type, which together result in the induction principle of circle types. 

Elimination rules for the circle type:
$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}{\Gamma \vdash \mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop}):\prod_{x:S^1} C(x)}$$

The elimination rule states that if:

1. For any term $x:S^1$, we have a type $C(x)$

1. For any term $c_\mathrm{base}:C(\mathrm{base})$ and any heterogeneous identification $c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}$ that $c_\mathrm{base}$ is equal to itself across $\mathrm{loop}$

we can construct a canonically defined dependent function $\mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop}):\prod_{x:S^1} C(x)$. 

Finally, we have the “computation” or [[beta-reduction|β-reduction]] rule. There are two possible computation rules, judgmental computation rules and propositional computation rules, which result in strict and weak circle types respectively. 

The judgmental computation rules for the circle type says that 

1. if we evaluate the dependent function $\mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})$ at the base point of $S^1$, we get the term $c_\mathrm{base}$, and 
1. if we apply the dependent function $\mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})$ to the loop identification of $S^1$, we get the term $c_\mathrm{loop}$. 

**Judgmental computation rules for the circle type**
$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}{\Gamma \vdash \mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})(\mathrm{base}) \equiv c_\mathrm{base}:C(\mathrm{base})}$$

$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}{\Gamma \vdash \mathrm{apd}_{\mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})}(\mathrm{base}, \mathrm{base}, \mathrm{loop}) \equiv c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}$$

The propositional computation rules for the circle type says that 

1. we have an identification $\beta_{S^1}^{\mathrm{base}}(c_\mathrm{base}, c_\mathrm{loop})$ indicating that the evaluation of the dependent function $\mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})$ at the base point of $S^1$ is equal to the term $c_\mathrm{base}$, and 
1. we have a heterogeneous identification $\beta_{S^1}^{\mathrm{loop}}(c_\mathrm{base}, c_\mathrm{loop})$ indicating that the application of the dependent function $\mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})$ to the loop identification of $S^1$, is equal to the term $c_\mathrm{loop}$ across the identification $\beta_{S^1}^{\mathrm{base}}(c_\mathrm{base}, c_\mathrm{loop})$. 

**Propositional computation rules for the circle type**
$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}{\Gamma \vdash \beta_{S^1}^{\mathrm{base}}(c_\mathrm{base}, c_\mathrm{loop}):\mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})(\mathrm{base}) =_{C(\mathrm{base})} c_\mathrm{base}}$$

$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}{\Gamma \vdash \beta_{S^1}^{\mathrm{loop}}(c_\mathrm{base}, c_\mathrm{loop}):\mathrm{apd}_{\mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})}(\mathrm{base}, \mathrm{base}, \mathrm{loop}) =_{z:C(\mathrm{base}).z =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} z}^{(\mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})(\mathrm{base}), c_\mathrm{base}, \beta_{S^1}^{\mathrm{base}}(c_\mathrm{base}, c_\mathrm{loop}))} c_\mathrm{loop}}$$

For weak circle types, we could package the elimination and propositional computation rules together using [[dependent sum types]] to get a single rule for the induction principle of the circle type:

$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}{\Gamma \vdash \mathrm{ind}_{S^1}^{x:S^1.C(x)}(c_\mathrm{base}, c_\mathrm{loop}):\sum_{c:\prod_{x:S^1} C(x)} \sum_{p:c(\mathrm{base}) =_{C(\mathrm{base})} c_\mathrm{base}} \mathrm{apd}_c(\mathrm{base}, \mathrm{base}, \mathrm{loop}) =_{z:C(\mathrm{base}).z =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} z}^{(c(\mathrm{base}), c_\mathrm{base}, p)} c_\mathrm{loop}}$$

Since the [[circle type]] is a [[positive type]], it is not necessary to include a [[uniqueness rule]] for the induction principle circle types, since the propositional uniqueness rule can be proven from the the other inference rules for the circle type. Nevertheless, one could include the uniqueness rule in the combined single induction rule by turning the dependent sum type into a [[uniqueness quantifier]], resulting in the **dependent universal property of the circle type**. 

$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}{\Gamma \vdash \mathrm{ind}_{S^1}^{x:S^1.C(x)}(c_\mathrm{base}, c_\mathrm{loop}):\exists!c:\prod_{x:S^1} C(x).\sum_{p:c(\mathrm{base}) =_{C(\mathrm{base})} c_\mathrm{base}} \mathrm{apd}_c(\mathrm{base}, \mathrm{base}, \mathrm{loop}) =_{z:C(\mathrm{base}).z =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} z}^{(c(\mathrm{base}), c_\mathrm{base}, p)} c_\mathrm{loop}}$$

#### Recursion principle of the circle type

In general, given a type $C$, by the [[weakening rule]] of [[dependent type theory]], one could form the constant type family $C$ indexed by $x:S^1$; then one could get the recursion principle of the circle type from induction on $C$ regarded as a constant type family, allowing for definitions of (non-dependent) functions from the circle type $S^1$ to $C$. This results in the following non-dependent elimination and computation rules associated with the recursion principle:

Non-dependent elimination rules for the circle type:
$$\frac{\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{C} c_\mathrm{base}}{\Gamma \vdash \mathrm{rec}_{S^1}(c_\mathrm{base}, c_\mathrm{loop}):S^1 \to C}$$

The non-dependent elimination rule states that if:

1. We have a type $C$

1. For any term $c_\mathrm{base}:C$ and any identification $c_\mathrm{loop}:c_\mathrm{base} =_{C} c_\mathrm{base}$ that $c_\mathrm{base}$ is equal to itself

we can construct a canonically defined function $\mathrm{rec}_{S^1}(c_\mathrm{base}, c_\mathrm{loop}):S^1 \to C$. 

Similarly to the case for the induction principle, there are two possible non-dependent computation rules for the recursion principle, judgmental computation rules and propositional computation rules, which result in strict and weak circle types respectively. 

The non-dependent judgmental computation rules for the circle type says that 

1. if we evaluate the function $\mathrm{rec}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})$ at the base point of $S^1$, we get the term $c_\mathrm{base}$, and 
1. if we apply the function $\mathrm{rec}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})$ to the loop identification of $S^1$, we get the term $c_\mathrm{loop}$. 

**non-dependent judgmental computation rules for the circle type**
$$\frac{\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{C} c_\mathrm{base}}{\Gamma \vdash \mathrm{rec}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})(\mathrm{base}) \equiv c_\mathrm{base}:C}$$

$$\frac{\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{C} c_\mathrm{base}}{\Gamma \vdash \mathrm{ap}_{\mathrm{rec}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})}(\mathrm{base}, \mathrm{base}, \mathrm{loop}) \equiv c_\mathrm{loop}:c_\mathrm{base} =_{C} c_\mathrm{base}}$$

The non-dependent propositional computation rules for the circle type says that 

1. we have an identification $\beta_{S^1}^{\mathrm{base}}(c_\mathrm{base}, c_\mathrm{loop})$ indicating that the evaluation of the dependent function $\mathrm{rec}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})$ at the base point of $S^1$ is equal to the term $c_\mathrm{base}$, and 
1. we have a heterogeneous identification $\beta_{S^1}^{\mathrm{loop}}(c_\mathrm{base}, c_\mathrm{loop})$ indicating that the application of the dependent function $\mathrm{rec}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})$ to the loop identification of $S^1$, is equal to the term $c_\mathrm{loop}$ across the identification $\beta_{S^1}^{\mathrm{base}}(c_\mathrm{base}, c_\mathrm{loop})$. 

**non-dependent propositional computation rules for the circle type**
$$\frac{\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{C} c_\mathrm{base}}{\Gamma \vdash \beta_{S^1}^{\mathrm{base}}(c_\mathrm{base}, c_\mathrm{loop}):\mathrm{rec}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})(\mathrm{base}) =_{C(\mathrm{base})} c_\mathrm{base}}$$

$$\frac{\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{C} c_\mathrm{base}}{\Gamma \vdash \beta_{S^1}^{\mathrm{loop}}(c_\mathrm{base}, c_\mathrm{loop}):\mathrm{ap}_{\mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})}(\mathrm{base}, \mathrm{base}, \mathrm{loop}) =_{z:C(\mathrm{base}).z =_{C} z}^{(\mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})(\mathrm{base}), c_\mathrm{base}, \beta_{S^1}^{\mathrm{base}}(c_\mathrm{base}, c_\mathrm{loop}))} c_\mathrm{loop}}$$

For weak circle types, we could similarly package the elimination and propositional computation rules together using [[dependent sum types]] to get a single rule for the recursion principle of the circle type:

$$\frac{\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C \quad \Gamma \vdash c_\mathrm{loop}:\mathrm{Id}_{C}(c_\mathrm{base}, c_\mathrm{base})}{\Gamma \vdash \mathrm{rec}_{S^1}^{C}(c_\mathrm{base}, c_\mathrm{loop}):\sum_{c:S^1 \to C} \sum_{p:c(\mathrm{base}) =_{C(\mathrm{base})} c_\mathrm{base}} \mathrm{ap}_c(\mathrm{base}, \mathrm{base}, \mathrm{loop}) =_{z:C.z =_{C} z}^{(c(\mathrm{base}), c_\mathrm{base}, p)} c_\mathrm{loop}}$$

### As a suspension

The circle type could also be defined as the [[suspension type]] $\Sigma \mathbf{2}$ of the type of [[booleans]] $\mathbf{2}$. 

### As a coequalizer

The circle type could also be defined as the [[coequalizer type]] of any two [[endofunctions]] on the [[unit type]]

$$\mathbf{1} \rightrightarrows \mathbf{1} \to S^1$$

Also, following [[synthetic homotopy theory]], the [[circle type]] $S^1$ is the [[coequalizer type]] of the pair of functions on the [[line type]]

$$
A^1\underoverset{\quad s \quad}{\mathrm{id}_{A^1}}{\rightrightarrows}A^1 \to S^1
$$

### Using torsors 

The circle can also be defined without HITs using only univalence, as the type of $\mathbb{Z}$-torsors.  One can then prove that this type satisfies the same induction principle (propositionally).  This is due to [[Dan Grayson]].

## Properties 
 {#Properties}

### Induction and recursion principles

Its [[induction principle]] says (e.g. [UFP13, p. 177](#UFP13)) that for 

* any $P \colon S^1 \to Type$ 

* equipped with a point $base' \colon P(base)$ 

* and a [[dependent identification]] $loop' \,\colon\, base' =_{loop} base'$, 

there is $f:\prod_{(x:S^1)} P(x)$ such that:

$$f(base)=base'\qquad apd_f(loop) = loop'$$

As a special case, its [[recursion principle]] says that given any type $X$ with a point $x:X$ and a loop $l:x=x$, there is $f:S^1 \to X$ with 

$$f(base)=x\qquad ap_f(loop)=l$$

### Extensionality principle of the circle type

The extensionality principle of the circle type says that there is an equivalence of types between the identification type $\mathrm{base} =_{S^1} \mathrm{base}$ and the type of integers $\mathbb{Z}$:

$$\mathrm{ext}_{S^1}:(\mathrm{base} =_{S^1} \mathrm{base}) \simeq \mathbb{Z}$$

Equivalently, that the [[loop space type]] $\Omega(S^1, \mathrm{base})$ is equivalent to the [[integers]]. 

Thus, the extensionality principle of the circle type implies that the integers and thus the natural numbers are [[contractible types]] if [[axiom K]] or [[uniqueness of identity proofs]] hold for the entire type theory. If the extensionality principle of the natural numbers also hold in the type theory, then every type is contractible. 

One could prove the extensionality principle of the circle type, given a [[univalent universe]] where the circle is small relative to the universe. The [[HoTT book]] provides a number of such proofs. 

### H-space structures on the circle type

The type of [[H-spaces]] on the circle type is a [[contractible type]]. 

## Related concepts

* [[circle]], [[unit circle]], [[circle group]], [[circle object]]

* [[interval type]]

* [[line type]]

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