
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

\tableofcontents

## Idea

In any [[type theory]], judgmental equality is the notion of [[equality]] which is defined to be a [[judgment]]. Judgmental equality is most commonly used in single-level type theories like [[Martin-Löf type theory]] or [[higher observational type theory]] for making [[inductive definitions]], but it is also used in [[cubical type theory]] and [[simplicial type theory]] to define probe shapes for [[(infinity,1)-category theory|(infinity,1)-categorical]] types which could not be coherently defined in vanilla dependent type theory. 

Judgmental equality can be contrasted with [[propositional equality]], where equality is a [[proposition]], and [[typal equality]], where equality is a [[type]].

## Definition and structural rules

In the model of [[dependent type theory]] which uses [[judgmental equality]] for [[definitional equality]], judgmental equality of types and terms are given by the following [[judgments]]:

* $\Gamma \vdash A \equiv A' \; \mathrm{type}$ - $A$ and $A'$ are judgementally equal well-typed types in context $\Gamma$.
* $\Gamma \vdash a \equiv a' : A$ - $a$ and $a'$ are judgementally equal well-typed terms of type $A$ in context $\Gamma$.

Judgmental equality has its own structural rules: reflexivity, symmetry, transitivity, the principle of substitution, and the variable conversion rule. 

* Reflexivity of judgmental equality

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash A \equiv A \; \mathrm{type}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash a \equiv a:A}$$

* Symmetry of judgmental equality
$$\frac{\Gamma \vdash A \equiv B \; \mathrm{type}}{\Gamma \vdash B \equiv A \; \mathrm{type}}$$ 
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b:A}{\Gamma \vdash b \equiv a:A}$$

* Transitivity of judgmental equality
$$\frac{\Gamma \vdash A \equiv B \; \mathrm{type} \quad \Gamma \vdash B \equiv C \; \mathrm{type} }{\Gamma \vdash A \equiv C \; \mathrm{type}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b:A \quad b \equiv c:A }{\Gamma \vdash a \equiv c:A}$$

* Principle of substitution of judgmentally equal terms:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b : A \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta[b/x] \vdash B[a/x] \equiv B[b/x] \; \mathrm{type}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b : A \quad \Gamma, x:A, \Delta \vdash c:B}{\Gamma, \Delta[b/x] \vdash c[a/x] \equiv c[b/x]: B[b/x]}$$

* The variable conversion rule for judgmentally equal types:
$$\frac{\Gamma \vdash A \equiv B \; \mathrm{type} \quad \Gamma, x:A, \Delta \vdash \mathcal{J}}{\Gamma, x:B, \Delta \vdash \mathcal{J}}$$

In addition, if the dependent type theory has [[type definition judgments]] $B \coloneqq A \; \mathrm{type}$ and [[term definition judgments]] $b \coloneqq a:A$, then judgmental equality is used in the following rules:

* Formation and judgmental equality reflection rules for type definition:
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \equiv A\; \mathrm{type}}$$

* Introduction and judgmental equality reflection rules for term definition:
$$\frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b \equiv a:A}$$

## In computation and uniqueness rules

Judgmental equality can be used in the [[computation rules]] and [[uniqueness rules]] of types: 

* Computation rules for dependent product types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \lambda(x:A).b(x)(a) \equiv b[a/x]:B[a/x]}$$

* Uniqueness rules for dependent product types:

$$\frac{\Gamma \vdash f:\prod_{x:A} B(x)}{\Gamma \vdash f \equiv \lambda(x).f(x):\prod_{x:A} B(x)}$$

* Computation rules for dependent sum types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \pi_1(a, b) \equiv a:A} \qquad \frac{\Gamma, x:A \vdash b:B \quad \Gamma \vdash a:A}{\Gamma \vdash \pi_2(a, b) \equiv b:B(\pi_1(a, b))}$$

* Uniqueness rules for dependent sum types:

$$\frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash z \equiv (\pi_1(z), \pi_2(z)):\sum_{x:A} B(x)}$$

* Computation rules for identity types:
$$\frac{\Gamma, a:A, b:A, p:a =_A b \vdash C \; \mathrm{type} \quad \Gamma, c:A \vdash t:C[c/a, c/b, \mathrm{refl}_A(c)/p]}{\Gamma, c:A \vdash J(t, c, c, \mathrm{refl}(c)) \equiv t:C[c/a, c/b, \mathrm{refl}_A(c)/p]}$$

## See also

* [[equality]]

* [[propositional equality]], [[typal equality]]

## References

* Robin Adams, _Pure type systems with judgemental equality_, Journal of Functional Programming, Volume 16 Issue 2(2006)   ([web](http://dl.acm.org/citation.cfm?id=1114675))

* Vincent Siles, Hugo Herbelin, _Equality is typable in semi-full pure type systems_ ([pdf](http://pauillac.inria.fr/~herbelin/publis/lics-SilHer10-pts-typed-conv.pdf))

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([pdf](https://raw.githubusercontent.com/martinescardo/HoTTEST-Summer-School/main/HoTT/hott-intro.pdf)) (478 pages)

[[!redirects judgmental equality]]
[[!redirects judgmental equalities]]

[[!redirects judgemental equality]]
[[!redirects judgemental equalities]]
