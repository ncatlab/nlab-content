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

## Definition

In a [[dependent type theory]] with [[identity types]], a term $a:A$ is a **center of contraction** or a **centre of contraction** if in the context of a variable $b:A$ there is an [[identification]] $p(b):a =_A b$. If the type theory also has [[dependent product types]], the above is equivalent to having a dependent function
$$p:\prod_{b:A} a =_A b$$
called a **contraction** of $A$ at $a$. Thus, contractons of $A$ at $a$ are witnesses that $a:A$ is a center of contraction. 

We then define the type of contractions of $A$ at $a$ as
$$\mathrm{Contr}_A(a) \coloneqq \prod_{b:A} a =_A b$$ 

### Rules for contraction types

If the dependent type theory does not have [[dependent product types]], contraction types could still be defined by adding the formation, introduction, elimination, computation, and uniqueness types for contraction types

Formation rules for contraction types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, a:A, x:A \vdash a =_A x \; \mathrm{type}}{\Gamma, a:A \vdash \mathrm{Contr}_A(a) \; \mathrm{type}}$$

Introduction rules for contraction types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, a:A, x:A \vdash a =_A x}{\Gamma, a:A \vdash \lambda(x).p(x):\mathrm{Contr}_A(a)}$$

Elimination rules for contraction types:
$$\frac{\Gamma, a:A \vdash p:\mathrm{Contr}_A(a) \quad \Gamma \vdash b:A}{\Gamma \vdash p(b):a =_A b}$$

Computation rules for contraction types:
$$\frac{\Gamma, a:A, x:A \vdash p(x):a =_A x \quad \Gamma \vdash b:A}{\Gamma \vdash \beta_\mathrm{Contr}:(\lambda(x).p(x))(b) =_{a =_A b} p(b)}$$

Uniqueness rules for contraction types:
$$\frac{\Gamma, a:A \vdash p:\mathrm{Contr}_A(a)}{\Gamma \vdash \eta_\mathrm{Contr}:p =_{\mathrm{Contr}_A(a)} \lambda(x).p(x)}$$

## Properties

A type $A$ is a [[contractible type]] if there exists a center of contraction
$$isContr(A) = \sum_{a:A} \mathrm{Contr}_A(a)$$
and a type $A$ is an [[h-proposition]] if every element in $A$ is a center of contraction 
$$isProp(A) = \prod_{a:A} \mathrm{Contr}_A(a)$$

The [[axiom K]] on a type states that for every element $a:A$, [[reflexivity]] $\mathrm{refl}_A(a)$ is the [[center of contraction]] of the [[loop space type]] of $a$. 

## See also

* [[contractible type]]
* [[h-proposition]]

## References

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

[[!redirects center of contraction]]
[[!redirects centers of contraction]]

[[!redirects centre of contraction]]
[[!redirects centres of contraction]]

[[!redirects type of contractions]]
[[!redirects types of contractions]]

[[!redirects contraction type]]
[[!redirects contraction types]]

[[!redirects Contr]]