
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

An _inductive definition_ is a [[definition]] by [[induction]]/[[recursion]].

## Definition

In [[type theory]], inductive and recursive definitions are made on [[inductive types]] through the [[computation rules]] for the inductive type. However, since there are multiple possible [[equalities]] which could be used for [[computation rules]], there are multiple computation rules which could be used in inductive definitions: computation rules involving [[judgmental equality]], [[propositional equality]], and [[typal equality]] are all possible. For example, addition is usually defined by recursion on the natural numbers, and since the natural numbers comes with two computation rules, addition comes with an introduction rule and two computation rules, one for the base case $0$ and one for the inductive case $s$ the successor function: 

* Introduction and judgmental computation rules for addition $+$:

$$\frac{\Gamma \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vdash m:\mathbb{N} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash m + n:\mathbb{N}} \qquad \frac{\Gamma \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash 0 + n = n:\mathbb{N}} \qquad \frac{\Gamma \vdash \mathbb{N} \; \mathrm{type}\quad \Gamma \vdash m:\mathbb{N} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash s(m) + n = s(m + n):\mathbb{N}}$$

* Introduction and propositional computation rules for addition $+$:

$$\frac{\Gamma \vert \Phi \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vert \Phi \vdash m:\mathbb{N} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vert \Phi \vdash m + n:\mathbb{N}} \qquad \frac{\Gamma \vert \Phi \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vert \Phi \vdash n:\mathbb{N}}{\Gamma \vert \Phi \vdash 0 + n =_\mathbb{N} n \; \mathrm{true}} \qquad \frac{\Gamma \vert \Phi \vdash \mathbb{N} \; \mathrm{type}\quad \Gamma \vert \Phi \vdash m:\mathbb{N} \quad \Gamma \vert \Phi \vdash n:\mathbb{N}}{\Gamma \vert \Phi \vdash s(m) + n =_\mathbb{N} s(m + n) \; \mathrm{true}}$$

* Introduction and typal computation rules for addition $+$:

$$\frac{\Gamma \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vdash m:\mathbb{N} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash m + n:\mathbb{N}} \qquad \frac{\Gamma \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \beta_{+}^0(n):0 + n =_\mathbb{N} n} \qquad \frac{\Gamma \vdash \mathbb{N} \; \mathrm{type}\quad \Gamma \vdash m:\mathbb{N} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \beta_{+}^s(m, n):s(m) + n =_\mathbb{N} s(m + n)}$$

Another example of an inductive definition is the definition of the [[transport]] function, which is given by the following introduction and computation rules:

* Introduction and judgmental computation rules for the transport function $\mathrm{tr}$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta[b/x] \vdash \mathrm{tr}(x.B, a, b, p):B[a/x] \simeq B[b/x]}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta[a/x] \vdash \mathrm{tr}(x.B, a, a, \mathrm{refl}_A(a)) = \mathrm{id}_{B[a/x]}:B[a/x] \simeq B[a/x]}$$

* Introduction and propositional computation rules for the transport function $\mathrm{tr}$:

$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type} \quad \Gamma \vert \Phi \vdash a:A \quad \Gamma \vert \Phi \vdash b:A \quad \Gamma \vert \Phi \vdash p:a =_A b \quad \Gamma, x:A, \Delta \vert \Phi \vdash B \; \mathrm{type}}{\Gamma, \Delta[b/x] \vert \Phi[b/x] \vdash \mathrm{tr}(x.B, a, b, p):B[a/x] \simeq B[b/x]}$$

$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type} \quad \Gamma \vert \Phi \vdash a:A \quad \Gamma, x:A, \Delta \vert \Phi \vdash B \; \mathrm{type}}{\Gamma, \Delta[a/x] \vert \Phi[a/x] \vdash \mathrm{tr}(x.B, a, a, \mathrm{refl}_A(a)) =_{B[a/x] \simeq B[a/x]} \mathrm{id}_{B[a/x]} \; \mathrm{true}}$$

* Introduction and typal computation rules for the transport function $\mathrm{tr}$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta[b/x] \vdash \mathrm{tr}(x.B, a, b, p):B[a/x] \simeq B[b/x]}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta[a/x] \vdash \beta_\mathrm{tr}^{\mathrm{refl}_A}(x.B, a):\mathrm{tr}(x.B, a, a, \mathrm{refl}_A(a)) =_{B[a/x] \simeq B[a/x]} \mathrm{id}_{B[a/x]}}$$

## Related concepts

* [[inductive type]]

* [[computation rule]]

* [[coinductive definition]]

## References

* [[Peter Aczel]], _An introduction to inductive definitions_ In Jon Barwise, editor, _Handbook of Mathematical Logic_, chapter C.7, pages 783&#8211;818. North-Holland, 1977.

A textbook account is in section I.2 of 

* [[Robert Harper]], _[[Practical Foundations for Programming Languages]]_


[[!redirects inductive definition]]
[[!redirects inductive definitions]]
