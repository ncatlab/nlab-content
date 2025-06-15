
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

The usual notion of equality in [[mathematics]] as a [[proposition]] or a [[predicate]] in [[predicate logic]]. This notion of equality can be formalized in [[predicate logic over type theory]] and in [[dependent type theory]]. 

Propositional equality is most commonly used in [[set theories]] like [[ZFC]] and [[ETCS]] and [[dependently sorted set theories]]. 

Propositional equality can be contrasted with [[judgmental equality]], where equality is a [[judgment]], and [[typal equality]], where equality is a [[type]]. 

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

### In dependent type theory

Historically in the [[dependent type theory]] community, the term **propositional equality** was used for the [[identity type]] in the sense of [[typal equality]]. This was because under the principle of [[propositions as types]], one interprets all types in a single-layer type theory as being propositions. 

However, we choose to make a distinction between propositional equality and typal equality in dependent type theory, because in the advent of [[homotopy type theory]] and other [[intensional type theories]], [[typal equality]] is no longer required to be a [[subsingleton]] or [[h-proposition]], and the alternative principle of [[propositions as some types]] has become the primary interpretation of [[dependent type theory]], where only the [[subsingletons]] or [[h-propositions]] are interpreted as [[propositions]]. 

In the [[propositions as some types]] interpretation of dependent type theory, the notion of "propositional equality" does have an interpretation in terms of identity types: two elements $x$ and $y$ of a type $A$ are **propositionally equal** or perhaps just **equal** if $x$ and $y$ are [[uniquely]] [[identified]]; the identity type $\mathrm{Id}_A(x, y)$ is a [[contractible type]]. 

$$x = y \coloneqq \mathrm{isContr}(\mathrm{Id}_A(x, y))$$

By this definition of equality, equality is always a [[binary relation]], because [[isContr]] is always a [[proposition]] in [[dependent type theory]]. We say that all identifications between $x:A$ and $y:A$ are propositional equalities if $\mathrm{Id}_A(x, y) \to x = y$. A **set** is then precisely a type where all identifications are propositional equalities, and coincide with the usual definition that identity types $\mathrm{Id}_A(x, y)$ are propositions for all $x:A$ and $y:A$. 

The [[uniqueness of identity proofs]] can then be represented by a propositional equality analogue of [[equality reflection]] for [[extensional type theory]]:
$$\frac{\Gamma \vdash p:\mathrm{Id}_A(x, y)}{\Gamma \vdash \mathrm{UIP}(p):x = y}$$

Propositional equality in this manner coincides with the common notion of equality found elsewhere in mathematics, as well as the unique isomorphisms and unique equivalences discussed in [Buzzard24](#Buzzard24) if one assumes [[univalence]]. 

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

## Propositional equality internal to a set theory

Relations and propositional equality could be [[internal logic of set theory|internalized in any set theory]]: the internal propositional equality in set theory is the smallest internal [[reflexive relation]] on $S$, and it is in fact an internal [[equivalence relation]]; it is the only internal equivalence relation on $S$ that is also a [[partial order]] (although that fact is somewhat circular).  This relation is often called the __identity relation__ on $S$, either because 'identity' can mean 'equality' or because it is the [[identity]] for [[composition]] of relations. 

In the [[category]] of reflexive relations on $S$, the [[equality relation]] on $S$ is an [[initial object|initial reflexive relation]]; when the equality relation is a [[type family]] instead of a family of propositions, then the equality relation is the initial type generated by reflexivity or the [[first law of thought]].

As a [[subset]] of $S \times S$, the equality relation is often called the __[[diagonal]]__ and written $\Delta_S$ or similarly.  As an abstract set, this subset is [[isomorphism|isomorphic]] to $S$ itself, so one also sees the diagonal as a map, the [[diagonal function]] $S \overset{\Delta_S}\to S \times S$, which maps $x$ to $(x,x)$; note that $x = x$.  This is in [[Set]]; analogous [[diagonal morphisms]] exist in any [[cartesian monoidal category]].

## See also

* [[equality]], [[equality in type theory]]

* [[judgmental equality]], [[typal equality]]

* [[logic over dependent type theory]]

* [[dependently sorted set theory]]

[[!include logic symbols -- table]]

## References

The usual notion of equality as a proposition is discussed in 

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Equality_(mathematics)">Equality (mathematics)</a>*

* {#Buzzard24} [[Kevin Buzzard]], *Grothendieck's use of equality* ([arXiv:2405.10387](https://arxiv.org/abs/2405.10387))

[[!redirects propositional equality]]
[[!redirects propositional equalities]]
[[!redirects propositionally equal]]

[[!redirects equality predicate]]
[[!redirects equality predicates]]

[[!redirects equality relation]]
[[!redirects equality relations]]
[[!redirects identity relation]]
[[!redirects identity relations]]
[[!redirects diagonal relation]]
[[!redirects diagonal relations]]

[[!redirects contractible identity type]]
[[!redirects contractible identity types]]
