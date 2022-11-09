
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
 {#Idea}

In any two-level type theory with a level of [[types]] and a [[level]] of [[propositions]], **propositional equality** is the notion of [[equality]] which is defined to be a proposition. Propositional equality is most commonly used in [[first order logic]] over [[type theory]], such as in most first order [[set theories]] like [[ZFC]] and [[ETCS]], but it could also be used for [[definitional equality]] and [[conversional equality]] in some presentations of [[dependent type theories]] like [[Martin-Löf type theory]] or [[cubical type theory]] in place of [[judgmental equality]]. 

Propositional equality can be contrasted with [[judgmental equality]], where equality is a [[judgment]], and [[typal equality]], where equality is a [[type]].

### Note on terminology

Historically in the [[dependent type theory]] community, the term *propositional equality* was used for [[typal equality]]. This was because under the principle of [[propositions as types]], one interprets all types in a single-layer type theory as being propositions. However, we choose to make a distinction between propositional equality and typal equality. First, propositional equality as defined in this article is used in the most common [[foundations of mathematics]], such as [[ZFC]] and [[ETCS]], and is clearly not a type. Additionally, in some two-layer type theories consisting of a layer of [[types]] and a layer of [[propositions]], one can have three distinct notions of equality: [[judgmental equality]], [[propositional equality]], and [[typal equality]]. Finally, in the advent of [[homotopy type theory]] and other type theoretic [[higher foundations]], [[typal equality]] is no longer required to be a [[subsingleton]] or [[h-proposition]], and the alternative principle of [[propositions as some types]] has become the primary interpretation of [[dependent type theory]], where only the [[subsingletons]] or [[h-propositions]] are interpreted as [[propositions]]. 

## Definition and structural rules

In the model of [[propositional logic]] over [[dependent type theory]] which uses [[propositional equality]] for [[definitional equality]], propositional equality of types and terms is formed by the following rules:

$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type} \quad \Gamma \vert \Phi \vdash B \; \mathrm{type}}{\Gamma \vert \Phi \vdash A \equiv B \; \mathrm{prop}}$$

$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type} \quad \Gamma \vert \Phi \vdash a:A \quad \Gamma \vert \Phi \vdash b:A}{\Gamma \vert \Phi \vdash a \equiv_A b \; \mathrm{prop}}$$

Propositional equality has its own structural rules:  reflexivity, symmetry, transitivity, the principle of substitution, and the variable conversion rule. 

* Reflexivity of propositional equality

$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type}}{\Gamma \vert \Phi \vdash A \equiv A \; \mathrm{true}}$$
$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type} \quad \Gamma \vert \Phi \vdash a:A}{\Gamma \vert \Phi \vdash a \equiv_A a \; \mathrm{true}}$$

* Symmetry of propositional equality

$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type} \quad \Gamma \vert \Phi \vdash B \; \mathrm{type} \quad \Gamma \vert \Phi \vdash A \equiv B \; \mathrm{true}}{\Gamma \vert \Phi \vdash B \equiv A \; \mathrm{true}}$$
$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type} \quad \Gamma \vert \Phi \vdash a:A \quad \Gamma \vert \Phi \vdash b:A \quad \Gamma \vert \Phi \vdash a \equiv_A b \; \mathrm{true}}{\Gamma \vert \Phi \vdash b \equiv_A a \; \mathrm{true}}$$

* Transitivity of propositional equality

$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type} \quad \Gamma \vert \Phi \vdash B \; \mathrm{type} \quad \Gamma \vert \Phi \vdash C \; \mathrm{type} \quad \Gamma \vert \Phi \vdash A \equiv B \; \mathrm{true} \quad \Gamma \vert \Phi \vdash B \equiv C \; \mathrm{true}}{\Gamma \vert \Phi \vdash A \equiv C \; \mathrm{true}}$$ 
$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type} \quad \Gamma \vert \Phi \vdash a:A \quad \Gamma \vert \Phi \vdash b:A \quad \Gamma \vert \Phi \vdash c:A \quad \Gamma \vert \Phi \vdash a \equiv_A b \; \mathrm{true} \quad \Gamma \vert \Phi \vdash b \equiv_A c \; \mathrm{true}}{\Gamma \vert \Phi \vdash a \equiv_A c \; \mathrm{true}}$$

* Principle of substitution of propositionally equal terms:
$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type} \quad \Gamma \vert \Phi \vdash a : A \quad \Gamma \vert \Phi \vdash b : A \quad \Gamma \vert \Phi \vdash a \equiv_A b \; \mathrm{true} \quad \Gamma, x:A, \Delta \vert \Phi \vdash B \; \mathrm{type}}{\Gamma, \Delta[b/x] \vert \Phi[b/x] \vdash B[a/x] \equiv B[b/x] \; \mathrm{true}}$$
$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type} \quad \Gamma \vert \Phi \vdash a : A \quad \Gamma \vert \Phi \vdash b : A \quad \Gamma \vert \Phi \vdash a \equiv_A b \; \mathrm{true} \quad \Gamma, x:A, \Delta \vert \Phi \vdash c:B}{\Gamma, \Delta[b/x] \vert \Phi[b/x] \vdash c[a/x] \equiv_{B[b/x]} c[b/x] \; \mathrm{true}}$$

* The variable conversion rule for propositionally equal types:

$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type} \quad \Gamma \vert \Phi \vdash B \; \mathrm{type} \quad \Gamma \vert \Phi \vdash A \equiv B \; \mathrm{true} \quad \Gamma, x:A, \Delta \vert \Phi \vdash \mathcal{J}}{\Gamma, x:B, \Delta \vert \Phi \vdash \mathcal{J}}$$

In addition, if the dependent type theory has [[type definition judgments]] $B \coloneqq A \; \mathrm{type}$ and [[term definition judgments]] $b \coloneqq a:A$, then propositional equality is used in the following rules:

* Formation and propositional equality reflection rules for type definition:
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \equiv A\; \mathrm{true}}$$

* Introduction and propositional equality reflection rules for term definition:
$$\frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b \equiv_A a \; \mathrm{true}}$$

## In computation and uniqueness rules

Propositional equality can be used in the [[computation rules]] and [[uniqueness rules]] of types: 

* Computation rules for dependent product types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \lambda(x:A).b(x)(a) \equiv_{B[a/x]} b[a/x] \; \mathrm{true}}$$

* Uniqueness rules for dependent product types:

$$\frac{\Gamma \vdash f:\prod_{x:A} B(x)}{\Gamma \vdash f \equiv_{\prod_{x:A} B(x)} \lambda(x).f(x) \; \mathrm{true}}$$

* Computation rules for dependent sum types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \pi_1(a, b) \equiv_A a \; \mathrm{true}} \qquad \frac{\Gamma, x:A \vdash b:B \quad \Gamma \vdash a:A}{\Gamma \vdash \pi_2(a, b) \equiv_{B(\pi_1(a, b))} b \; \mathrm{true}}$$

* Uniqueness rules for dependent sum types:

$$\frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash z \equiv_{\sum_{x:A} B(x)} (\pi_1(z), \pi_2(z)) \; \mathrm{true}}$$

* Computation rules for identity types:

$$\frac{\Gamma, a:A, b:A, p:a =_A b \vdash C \; \mathrm{type} \quad \Gamma, c:A \vdash t:C[c/a, c/b, \mathrm{refl}_A(c)/p]}{\Gamma, c:A \vdash J(t, c, c, \mathrm{refl}(c)) \equiv_{C[c/a, c/b, \mathrm{refl}_A(c)/p]} t \; \mathrm{true}}$$

## See also

* [[equality]]

* [[judgmental equality]], [[typal equality]]

[[!redirects propositional equality]]
[[!redirects propositionally equal]]