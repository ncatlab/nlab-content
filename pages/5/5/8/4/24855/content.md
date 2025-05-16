
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

In any [[predicate logic over type theory]], **propositional equality** is the notion of [[equality]] which is defined to be a proposition. Propositional equality is most commonly used in [[set theories]] like [[ZFC]] and [[ETCS]] and [[dependently sorted set theories]], but it could also be used for [[definitional equality]] and [[conversional equality]] in [[logic over dependent type theory]] in place of [[judgmental equality]]. 

Propositional equality can be contrasted with [[judgmental equality]], where equality is a [[judgment]], and [[typal equality]], where equality is a [[type]].

### Note on terminology

Historically in the [[dependent type theory]] community, the term *propositional equality* was used for [[typal equality]]. This was because under the principle of [[propositions as types]], one interprets all types in a single-layer type theory as being propositions. However, we choose to make a distinction between propositional equality and typal equality. First, propositional equality as defined in this article is used in the most common [[foundations of mathematics]], such as [[ZFC]] and [[ETCS]], and is clearly not a type. Additionally, in some [[logics over type theory]], one can have three distinct notions of equality: [[judgmental equality]], [[propositional equality]], and [[typal equality]]. Finally, in the advent of [[homotopy type theory]] and other type theoretic [[higher foundations]], [[typal equality]] is no longer required to be a [[subsingleton]] or [[h-proposition]], and the alternative principle of [[propositions as some types]] has become the primary interpretation of [[dependent type theory]], where only the [[subsingletons]] or [[h-propositions]] are interpreted as [[propositions]]. 

## Definition

### Typed first-order logic

In any two-layer type theory with a layer of [[types]] and a layer of [[propositions]], or equivalently a [[first order logic]] over [[type theory]] or a [[first-order theory]], every type $A$ has a binary [[relation]] according to which two elements $x$ and $y$ of $A$ are related if and only if they are equal; in this case we write $x =_A y$. Since relations are propositions in the context of a term variable judgment in the type layer, this is called **[[propositional equality]]**. The formation and introduction rules for propositional equality is as follows

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A, y:A \vdash x =_A y \; \mathrm{prop}} \quad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A \vdash x =_A x \; \mathrm{true}}$$

Then we have the elimination rules for propositional equality:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A, y:A \vdash P(x, y) \; \mathrm{prop}}{\Gamma \vdash \left(\forall x:A.P(x, x)\right) \implies \left(\forall x:A.\forall y:A.x =_A y \implies P(x, y)\right) \; \mathrm{true}}$$

### Untyped first-order logic

Something similar occurs in untyped [[first-order logic]], where the [[domain of discourse]] has a binary [[relation]] according to which two elements $x$ and $y$ are related if and only if they are equal; in this case we write $x = y$. Since relations are propositions in the context of a term variable judgment in the type layer, this is similarly called **[[propositional equality]]**. The formation and introduction rules for propositional equality is as follows

$$\frac{\Gamma \vdash x \quad \Gamma \vdash y}{\Gamma \vdash x = y \; \mathrm{prop}} \quad \frac{\Gamma \vdash x}{\Gamma \vdash x = x \; \mathrm{true}}$$

Then we have the elimination rules for propositional equality:

$$\frac{\Gamma, x, y \vdash P(x, y) \; \mathrm{prop}}{\Gamma \vdash \left(\forall x.P(x, x)\right) \implies \left(\forall x.\forall y.x = y \implies P(x, y)\right) \; \mathrm{true}}$$

## Properties

### Propositional equality is an equivalence relation

The introduction rule of propositional equality says that propositional equality is reflexive. 

We can show that propositional equality is symmetric, that for all $x:A$ and $y:A$ such that $x =_A y$, we have $y =_A x$. By the introduction rule, we have that for all $x:A$, we have that $x =_A x$, and because all propositions imply themselves, we have that $x =_A x$ implies $x =_A x$. Thus, by the elimination rules for propositional equality, for all $x:A$ and $y:A$ such that $x =_A y$, we have $y =_A x$. 

We can also show that propositional equality is transitive, that for all $x:A$, $y:A$, and $z:A$ such that $x =_A y$, $y =_A z$ implies that $x =_A z$. By the introduction rule, we have that for all $x:A$ and $a:B(x)$, we have that $x =_A x$, and because all propositions imply themselves, we have that $x =_A z$ implies $y =_A z$, and because true propositions imply true propositions, we have that $x =_A x$ implies that $x =_A z$ implies $x =_A z$. Thus, by the elimination rules for propositional equality, for all $x:A$, $y:A$, and $z:A$ such that $x =_A y$, $y =_A z$ implies that $x =_A z$. 

Thus, propositional equality is an equivalence relation. 

### Functions are extensional

For all function $f:A \to B$ and elements $x:A$ and $y:A$ such that $x =_A y$, $f(x) =_{B} f(y)$:

$$\forall f:A \to B.\forall x:A.\forall y:A.x =_A y \implies f(x) =_{B} f(y)$$

This is because for all functions $f:A \to B$, by the introduction rule for propositional equality, for all elements $x:A$, $f(x) =_{B} f(x)$, and the elimination rule for propositional equality states that if for all elements $x:A$, $f(x) =_{B} f(x)$, then for all elements $x:A$ and $y:A$ such that $x =_A y$, $f(x) =_{B} f(y)$. 

### Function extensionality

The extensionality principle for [[function types]] ([[function extensionality]]) states that for all functions $f:A \to B$ and $g:A \to B$, $f =_{A \to B} g$ if and only if for all $a:A$ and $b:A$ such that $a =_A b$, $f(a) =_{B} g(b)$

$$\forall f:A \to B.\forall g:A \to B.f =_{A \to B} g \iff \forall a:A. \forall b:A.a =_A b \implies (f(a) =_{B} g(b))$$

### Transport and heterogeneous propositional equality

Given a set $A$ and elements $x \in A$ and $y \in A$ and a family of sets $(B(x))_{x \in A}$, $a \in B(x)$ and $b \in B(y)$, if $x =_A y$, then we can define [[transport]] functions $\mathrm{tr}_{A, B}(x, y):B(x) \to B(y)$ whose [[inverse function]] is $\mathrm{tr}_{A, B}(y, x)$ by symmetry of propositional equality. 

The heterogeneous propositional equality is given by the [[logically equivalent]] relations 
$$\mathrm{tr}_{A, B}(x, y, a) =_{B(y)} b \quad \mathrm{or} \quad a =_{B(x)} \mathrm{tr}_{A, B}(y, x, b)$$

Transport and heterogeneous propositional equality are important in some [[set theories]] which do not have equality between sets themselves, and the only way to compare sets for equality is through [[isomorphisms]]. The same is true of [[logic over dependent type theory]] which do not have definitional equality between types, and one has to use [[definitional isomorphisms]] instead. In the presence of equality between sets, transport is simply the [[identity function]] on the equal set. 

### In computation and uniqueness rules

Propositional equality can be used in the [[computation rules]] and [[uniqueness rules]] of types in [[logic over dependent type theory]]: 

* Computation rules for dependent product types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \lambda(x:A).b(x)(a) =_{B(a)} b(a) \; \mathrm{true}}$$

* Uniqueness rules for dependent product types:

$$\frac{\Gamma \vdash f:\prod_{x:A} B(x)}{\Gamma \vdash f =_{\prod_{x:A} B(x)} \lambda(x).f(x) \; \mathrm{true}}$$

* Computation rules for negative dependent sum types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \pi_1(a, b) =_A a \; \mathrm{true}} \qquad \frac{\Gamma, x:A \vdash b:B \quad \Gamma \vdash a:A}{\Gamma \vdash \pi_2(a, b) =_{B(\pi_1(a, b))} b \; \mathrm{true}}$$

* Uniqueness rules for negative dependent sum types:

$$\frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash z =_{\sum_{x:A} B(x)} (\pi_1(z), \pi_2(z)) \; \mathrm{true}}$$

* Computation rules for identity types:

$$\frac{\Gamma, a:A, b:A, p:a =_A b \vdash C \; \mathrm{type} \quad \Gamma \vdash t:\prod_{x:A} C(x, x, \mathrm{refl}_A(x)) \quad \Gamma \vdash c:A}{\Gamma \vdash J(t, c, c, \mathrm{refl}(c)) =_{C(c, c, \mathrm{refl}_A(c))} t(c) \; \mathrm{true}}$$

## See also

* [[equality]]

* [[judgmental equality]], [[typal equality]]

* [[logic over dependent type theory]]

* [[dependently sorted set theory]]

## References

The usual notion of equality as a proposition is discussed in 

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Equality_(mathematics)">Equality (mathematics)</a>*

[[!redirects propositional equality]]
[[!redirects propositional equalities]]
[[!redirects propositionally equal]]