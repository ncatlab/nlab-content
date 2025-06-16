
> This article is about the notion of [[equality]] as a [[proposition]] or [[predicate]]. For [[equality]] as a [[judgment]], see [[judgmental equality]]. For [[equality]] as a [[type]], see [[typal equality]]. For other notions of equality, see [[equality]]. 

---

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

The usual notion of equality in [[mathematics]] as a [[proposition]] or a [[predicate]]. This notion of equality can be formalized in [[predicate logic over type theory]] and in [[dependent type theory]]. 

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

In [[logic over dependent type theory]], propositional equality can be used in the [[computation rules]] and [[uniqueness rules]] of types: 

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

## In constructive and classical mathematics

Constructive mathematics is mathematics in which the law of excluded middle does not necessarily hold for [[propositions]], [[subsingletons]], or [[h-propositions]]. Classical mathematics is mathematics in which the law of excluded middle does hold for [[propositions]], [[subsingletons]], or [[h-propositions]]. 

In classical mathematics, propositional equality of sets is a [[stable relation|stable]] [[equivalence relation]], and [[denial inequality]] of sets is a [[tight apartness relation]]. However, in constructive mathematics, propositional equality cannot be proven to be stable for all sets, and denial inequality cannot be proven to be a tight apartness relation for all sets. Instead, one could distinguish between 4 different notions of propositional equality and [[inequality]]:

* [[tight apartness relations]]. However, not all sets have tight apartness relations. 

* propositional equality, which is an [[equivalence relation]]; set with [[tight apartness relations]] have [[stable equality]]. 

* [[denial inequality]], which can only be proven to be a [[weakly tight]] [[irreflexive symmetric relation]]. However, all statements in classical mathematics involving only denial inequalities hold in constructive mathematics, by the [[double negation translation]] and the property that for any proposition $P$, $\neg \neg \neg P$ if and only if $\neg P$. 

* the [[double negation]] of propositional equality, which can only be proven to be a [[stable relation|stable]] [[reflexive symmetric relation]]. However, all statements in classical mathematics involving only equality hold in constructive mathematics with the equality replaced by its double negation, by the [[double negation translation]]. 

The sets in which propositional equality and inequality behaves as it does in [[classical mathematics]] are the [[classical sets]], the sets with an [[apartness relation]] such that every pair of elements are either equal or apart from each other. 

As a result, in constructive mathematics, sometimes one takes sets with [[tight apartness relations]] instead of general [[sets]] to be the foundational primitive concept. In classical mathematics, this is unnecessary, because every [[set]] has a [[tight apartness relation]]. 

## In dependent type theory
  {#InDependentTypeTheory}

In [[dependent type theory]], the term *propositional equality* is used to describe a notion of [[equality]] [[type]] different from that of [[judgmental equality]]. 

More specifically, there are two interpretations of [[propositions]] and [[logic]] in [[dependent type theory]]:

* The [[propositions as types]] interpretation, which says that all types are propositions. The term **propositional equality** is used as a synonym of typal equality in referring to [[identifications]] or [[identity types]]. 

* The [[propositions as some types]] interpretation, which says that only the [[subsingletons]] or [[h-propositions]] are propositions. The term *propositional equality* in this interpretation is not a synonym of typal equality in referring to [[identifications]] or [[identity types]]. 

Instead, in [[propositions as some types]], two elements $x$ and $y$ of a type $A$ are **propositionally equal** if $x$ and $y$ are [[uniquely]] [[identified]]; the identity type $\mathrm{Id}_A(x, y)$ is a [[contractible type]]. 

$$x = y \coloneqq \mathrm{isContr}(\mathrm{Id}_A(x, y))$$

Expanding out the definition of a [[contractible type]], a witness of propositional equality consists of an [[identification]] and a [[contraction]] showing that the identification is the [[center of contraction]] of the [[identity type]]. 

By this definition of equality, propositional equality is always a [[binary relation]], because [[isContr]] is always a [[proposition]] in [[dependent type theory]]. In fact, if all identifications in an [[identity type]] are unique (i.e. there is a function $\mathrm{Id}_A(x, y) \to x = y$), then the identity type is an [[h-proposition]], and if the identity type is an [[h-proposition]], then all identifications in the identity type are unique; hence the name *[[propositional equality]]* for unique identifications and the relation $x = y$ for the type $\mathrm{isContr}(\mathrm{Id}_A(x, y))$. 

An [[h-set]] is then precisely a type where all identifications are unique, and the [[uniqueness of identity proofs]] can then be represented by a propositional analogue of [[equality reflection]] for [[extensional type theory]]:
$$\frac{\Gamma \vdash p:\mathrm{Id}_A(x, y)}{\Gamma \vdash \mathrm{UIP}(p):x = y}$$
making typal equality and propositional equality synonyms of each other again, because then all identity types are propositions and all identifications are unique. 

Propositional equality defined in this manner is similar to the [[preset]] and [[setoid]] approaches to foundations of mathematics.

Propositional equality satisfies the [[principle of substitution]] by [[transport]] of the unique identification across [[predicates]], and satisifes the [[identity of indiscernibles]] because propositional equality is always a proposition, and so we have:

$$\prod_{x:A} \prod_{y:A} \mathrm{isContr}(\mathrm{Id}_A(x, y)) \simeq \prod_{x:A \to \mathrm{Prop}} P(x) \simeq P(y)$$

The [[identity of indiscernibles]] doesn't work for arbitrary identity types of a type $A$ because the type $\prod_{x:A \to \mathrm{Prop}} P(x) \simeq P(y)$ on the right hand side of the [[equivalence of types]] is always a [[proposition]], and so if it were true, it would imply that $A$ is an [[h-set]]; hence the necessity to restrict to identity types with a unique identification. 

However, propositional equality defined in this manner is not an [[equivalence relation]] because it is not a [[reflexive relation]]: for any [[loop space type]] which is not a [[contractible type]], the proposition $\mathrm{isContr}(\mathrm{Id}_A(x, x))$ is an [[empty type]]. The only such types with a reflexive propositional equality are thus those that satisfy [[axiom K]]: the [[h-sets]], thus making non-set types [[presets]]. 

Furthermore, the type-theoretic functions are [[prefunctions]] with respect to propositional equality. While functions do preserve identifications, they do not preserve propositional equality in the sense of the uniqueness of identifications. *Any* [[identification]] is given by a function out of the [[interval type]] $\mathbb{I}$, and the inductively generated identification $p:\mathrm{Id}_\mathbb{I}(0, 1)$ in the interval type is unique in $\mathrm{Id}_\mathbb{I}(0, 1)$, but not all identifications are unique in the absence of [[uniqueness of identity proofs]]. One can define an [[extensional function]] as one that does preserve the uniqueness of identifications, and prove that functions between [[h-sets]] preserve the uniqueness of identifications, and that h-sets are precisely the types between which all functions preserve uniqueness of identifications. To say that all functions are extensional along the lines of the [[preset]] approach to [[set theory]] is equivalent to the [[uniqueness of identity proofs]] that implies that all types are [[h-sets]].  

Most homotopy type theorists use the [[propositions as types]] interpretation of [[propositional equality]] as a synonym of [[typal equality]], even by those who use the [[propositions as some types]] interpretation for everything else. [[Kevin Buzzard]] in [Buzzard 2024](#Buzzard24) has used this fact and how that contradicts the interpretation of [[propositional equality]] elsewhere in mathematics as an argument for adopting a [[set-level type theory]] instead of [[homotopy type theory]]. 

By Buzzard's argument, homotopy type theorists should not be using the term "equality" to refer to arbitrary identifications or identity types, whether in its bare form or as "[[propositional equality]]" or "[[typal equality]]", instead restricting the use of equality / [[propositional equality]] for only the unique identifications, and using a suitable alternative for "[[typal equality]]", such as "[[identification]]" and "[[identified]]" and "[[identity type]]". On the other hand, the fact that [[propositional equality]] defined as having a unique identification is not a [[reflexive relation]] for non-set types means that perhaps it is not suitable for the bare term "equality", and perhaps the bare term "equality" and even the term "propositional equality" *should* refer to [[typal equality]] which is always reflexive. 

Either way, in the absence of [[uniqueness of identity proofs]], one has to give up either the notion of propositional equality as unique identification satisfying the [[identity of indiscernibles]] or the notion of propositional equality satisfying the [[first law of thought]]. 

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

[[!redirects unique equality]]
[[!redirects unique equalities]]
[[!redirects unique identity]]
[[!redirects unique identities]]
[[!redirects unique identification]]
[[!redirects unique identifications]]
[[!redirects unique path]]
[[!redirects unique paths]]

[[!redirects uniquely equal]]
[[!redirects uniquely identified]]