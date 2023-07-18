+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Objective type theory is a [[dependent type theory]] without [[judgmental equality]]. 

This means that the computation and uniqueness rules ([[beta-reduction]] and [[eta-conversion]]) for each type in the type theory are all typal computational and uniqueness rules using the [[identity type]], and in particular means that the identity type has to be introduced at the same time the dependent function type is introduced. As a result, the results in objective type theory are more general than in models which use judgmental equality for computational and uniqueness rules, since judgmental equality implies typal equality, while the converse isn't necessarily the case. 

In addition, objective type theory is similar to other non-type theory foundations such as the various flavors of set theory, since it also only has one notion of equality, propositional equality, and uses propositional equality in [[definitions]]. 

Objective type theory has [[decidable]] [[type checking]], and the type checking can be done in quadratic time. 

## Syntax

### Judgments and contexts

Objective type theory consists of the following judgments: 

* Type judgments, where we judge $A$ to be a type, $A \; \mathrm{type}$

* Type definition judgments, where we judge $B$ to be defined as the type $A$, $B \coloneqq A \; \mathrm{type}$

* Element judgments, where we judge $a$ to be an element of $A$, $a:A$

* Element definition judgments, where we judge $b$ to be defined as the term $a:A$, $b \coloneqq a:A$

* Context judgments, where we judge $\Gamma$ to be a context, $\Gamma \; \mathrm{ctx}$. 

Contexts are lists of element judgments $a:A$, $b:B$, $c:C$, et cetera, and are formalized by the rules for the empty context and extending the context by a element judgment

$$\frac{}{() \; \mathrm{ctx}} \qquad \frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash A \; \mathrm{type}}{(\Gamma, a:A) \; \mathrm{ctx}}$$

Note that type and element definition judgments are not judgmental equalities; the former are [[single assignment operators]] while the latter are [[equivalence relations]]. 

### Structural rules

There are three structural rules in objective type theory, the [[variable rule]], the [[weakening rule]], and the [[substitution rule]]. 

The variable rule states that we may derive a element judgment if the element judgment is in the context already:

$$\frac{\Gamma, a:A, \Delta \; \mathrm{ctx}}{\Gamma, a:A, \Delta \vdash a:A}$$

Let $\mathcal{J}$ be any arbitrary judgment. Then we have the following rules:

The weakening rule:

$$\frac{\Gamma, \Delta \vdash \mathcal{J} \quad \Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, \Delta \vdash \mathcal{J}}$$

The substitution rule:

$$\frac{\Gamma \vdash a:A \quad \Gamma, b:A, \Delta(b) \vdash \mathcal{J}(b)}{\Gamma, \Delta(a) \vdash \mathcal{J}(a)}$$

The weakening and substitution rules are admissible rules: they do not need to be explicitly included in the type theory as they could be proven by induction on the structure of all possible derivations. 

### Families of types and elements

A family of types is a type $B$ in the context of the element judgment $x:A$, $x:A \vdash B \; \mathrm{type}$, they are usually written as $B(x)$ to indicate its dependence upon $x$. Given a particular element $a:A$, the type $B(a)$ is a type dependent upon $a:A$. 

A family of terms is a term $b:B$ in the context of the variable judgment $x:A$, $x:A \vdash b:B$. They are likewise usually written as $b(x)$ to indicate its dependence upon $x$. Given a particular element $a:A$, the element $b(a)$ is an element dependent upon $a:A$. 

### Basic type formers - identification types and dependent function types

In this section, we give the rules for the basic type formers of type theory, which are [[identification types]] and [[dependent function types]]. 

Formation rules for identification types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, b:A \vdash a =_A b \; \mathrm{type}}$$

Formation rules for dependent function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \prod_{x:A} B(x) \; \mathrm{type}}$$

Introduction rules for identification types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A \vdash \mathrm{refl}_A(a) : a =_A a}$$

Introduction rules for dependent function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma \vdash \lambda(x:A).b(x):\prod_{x:A} B(x)}$$

Elimination rule for identification types:
$$\frac{\Gamma, x:A, y:A, p:x =_A y \vdash C(x, y, p) \; \mathrm{type}}{\Gamma, t:\prod_{a:A} C(a, a, \mathrm{refl}_A(a)), x:A, y:A, p:x =_A y \vdash J_A(t, x, y, p):C(x, y, p)}$$

Elimination rules for dependent function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:\prod_{x:A} B(x), a:A \vdash \mathrm{ind}_{\prod_{x:A} B(x)}(f, a):B(a)}$$

Computation rules for identification types:
$$\frac{\Gamma, x:A, y:A, p:x =_A y \vdash C(x, y, p) \; \mathrm{type}}{\Gamma, t:\prod_{a:A} C(a, a, \mathrm{refl}_A(a)), x:A \vdash \beta_{=_A}(t, x):\mathrm{ind}_{=_A}(t, x, x, \mathrm{refl}_A(x)) =_{C(x, x, \mathrm{refl}_A(x))} t(x)}$$

Computation rules for dependent function types
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma, a:A \vdash \beta_{\prod_{x:A} B(x)}(a):\mathrm{ind}_{\prod_{x:A} B(x)}(\lambda(x:A).b(x), a) =_{B(a)} b(a)}$$

Uniqueness rules for identification types
$$\frac{\Gamma, x:A, y:A, p:x =_A y \vdash C(x, y, p) \; \mathrm{type}}{\Gamma, t:\prod_{a:A} C(a, a, \mathrm{refl}_A(a)), x:A, y:A, p:x =_A y, q:C(x, y, p) \vdash \eta_{=_A}(t, x, y, p, q):J_A(t, x, y, p) =_{C(x, y, p)} q}$$

Uniqueness rules for dependent function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:\prod_{x:A} B(x) \vdash \eta_{\prod_{x:A} B(x)}(f):f =_{\prod_{x:A} B(x)} \lambda(x).f(x)}$$

### Function types

Formation rules for function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \to B \; \mathrm{type}}$$

Introduction rules for function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B}{\Gamma \vdash \lambda(x:A).b(x):A \to B}$$

Elimination rules for function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B, a:A \vdash \mathrm{ind}_{A \to B}(f, a):B}$$

Computation rules for function types
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B}{\Gamma, a:A \vdash \beta_{A \to B}(a):\mathrm{ind}_{A \to B}(\lambda(x:A).b(x), a) =_{B} b(a)}$$

Uniqueness rules for function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B \vdash \eta_{A \to B}(f):f =_{A \to B} \lambda(x).f(x)}$$

### Pair types

Formation rules for pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \times B \; \mathrm{type}}$$

Introduction rules for pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, x:A, y:B \vdash \mathrm{in}(x, y):A \times B}$$

Elimination rules for pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, z:A \times B \vdash \mathrm{ind}_{A \times B}^A(z):A} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, z:A \times B \vdash \mathrm{ind}_{A \times B}^B(z):B}$$

Computation rules for pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, x:A, y:B \vdash \beta_{A \times B}^A(x, y):\mathrm{ind}_{A \times B}^A(\mathrm{in}(x, y)) =_A x}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, x:A, y:B \vdash \beta_{A \times B}^B(x, y):\mathrm{ind}_{A \times B}^B(\mathrm{in}(x, y)) =_B y}$$

Uniqueness rules for pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, z:A \times B \vdash \eta_{A \times B}(z):z =_{A \times B} \mathrm{in}(\mathrm{ind}_{A \times B}^A(z), \mathrm{ind}_{A \times B}^B(z))}$$

### Dependent pair types

Formation rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \sum_{x:A} B(x) \; \mathrm{type}}$$

Introduction rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, y:B(x) \vdash \mathrm{in}(x, y):\sum_{x:A} B(x)}$$

Elimination rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{ind}_{\sum_{x:A} B(x)}^A:\left(\sum_{x:A} B(x)\right) \to A} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{ind}_{\sum_{x:A} B(x)}^B:\prod_{z:\sum_{x:A} B(x)} B(\mathrm{ind}_{\sum_{x:A} B(x)}^A(z))}$$

Computation rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, y:B(x) \vdash \beta_{\sum_{x:A} B(x)}^A(x, y):\mathrm{ind}_{\sum_{x:A} B(x)}^A(\mathrm{in}(x, y)) =_A x}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, y:B(x) \vdash \beta_{\Sigma(x:A).B(x)}^B(x, y):\mathrm{ind}_{\sum_{x:A} B(x)}^B(\mathrm{in}(x, y)) =_{B(\mathrm{ind}_{\sum_{x:A} B(x)}^A(\mathrm{in}(x, y)))} y}$$

Uniqueness rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, z:\sum_{x:A} B(x) \vdash \eta_{\sum_{x:A} B(x)}(z):z =_{\sum_{x:A} B(x)} \mathrm{in}(\mathrm{ind}_{\sum_{x:A} B(x))}^A(z), \mathrm{ind}_{\sum_{x:A} B(x)}^B(z))}$$

### Structural rules for definitions

Now that we have finally defined identification types, we can define the structural rules for term definitions. The structural rules for term definitions say that given a term $a:A$ and a term definition $b \coloneqq a:A$, one could derive that $b$ is a term of $A$, and that there is an identification between $b$ and $a$:

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash a:A \quad \Gamma \vdash b \coloneqq a:A}{\Gamma \vdash \delta_A(a, b):a =_A b}$$

Similarly, now that we have finally defined identification types, dependent function types, function types, and dependent pair types, we can define the structural rules for type definitions. The structural rules for type definitions say that given a type $A$ and a type definition $B \coloneqq A \; \mathrm{type}$, one could derive that $B$ is a type and that there is an equivalence between $A$ and $B$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash \delta_{A, B}:\sum_{f:A \to B} \prod_{y:B} \sum_{p:\sum_{x:A} f(x) =_B y} \prod_{q:\sum_{x:A} f(x) =_B y} p =_{\sum_{x:A} f(x) =_B y} q}$$

### Positive types

Now that we have [[identification types]], [[equivalence types]], [[dependent sum types]], and [[dependent product types]], we can use that to define the [[equivalence type]], the [[isContr]] [[modality]], the [[uniqueness quantifier]]
$$\mathrm{isContr}(A) \coloneqq \sum_{y:A} \prod_{z:A} y =_{A} z$$

$$\exists!x:A.B(x) \coloneqq \mathrm{isContr}\left(\sum_{x:A} B(x)\right)$$

$$A \simeq B \coloneqq \sum_{f:A \to B} \prod_{y:B}\exists!x:A.f(x) =_{B} y$$
and combine the [[elimination rule]], the [[computation rule]], and the [[uniqueness rule]] for any [[positive type]] into one rule, the [[induction]] rule. 

#### Unit type

Formation rules for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{1} \; \mathrm{type}}$$

Introduction rules for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{pt}:\mathbb{1}}$$

Induction rule for the unit type:
$$\frac{\Gamma, x:\mathbb{1} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{pt}:C(\mathrm{pt})}{\Gamma \vdash \mathrm{up}_\mathbb{1}^C(c_\mathrm{pt}):\exists!c:\prod_{x:\mathbb{1}} C(x).(c(\mathrm{pt}) =_{C(\mathrm{pt})} c_\mathrm{pt})}$$

#### Empty type

Formation rules for the empty type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{0} \; \mathrm{type}}$$

Induction rule for the empty type:
$$\frac{\Gamma, x:\mathbb{0} \vdash C(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{up}_\mathbb{0}^C:\mathrm{isContr}\left(\prod_{x:\mathbb{0}} C(x)\right)}$$

#### Booleans type

Formation rules for the booleans type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{2} \; \mathrm{type}}$$

Introduction rules for the booleans type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{2}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 1:\mathbb{2}}$$

Induction rule for the booleans type:
$$\frac{\Gamma, x:\mathbb{2} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_1:C(1)}{\Gamma \vdash \mathrm{up}_\mathbb{2}^C(c_0, c_1):\exists!c:\prod_{x:\mathbb{2}} C(x).(c(0) =_{C(0)} c_0) \times (c(1) =_{C(1)} c_1)}$$

#### Natural numbers type

Formation rules for the natural numbers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{N} \; \mathrm{type}}$$

Introduction rules for the natural numbers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{N}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash s:\mathbb{N} \to \mathbb{N}}$$

Induction rule for the natural numbers type:
$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x))}{\Gamma \vdash \mathrm{up}_\mathbb{N}^C(c_0, c_s):\exists!c:\prod_{x:\mathbb{N}} C(x).(c(0) =_{C(0)} c_0) \times \prod_{x:\mathbb{N}} c(s(x)) =_{C(s(x))} c_s(c(x))}$$

#### Integers type

Formation rules for the integers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{Z} \; \mathrm{type}}$$

Introduction rules for the integers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{Z}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash s:\mathbb{Z} \simeq \mathbb{Z}}$$

Induction rule for the integers type:
$$\frac{\Gamma, x:\mathbb{Z} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_s:\prod_{x:\mathbb{Z}} C(x) \simeq C(s(x))}{\Gamma \vdash \mathrm{up}_\mathbb{Z}^C(c_0, c_s):\exists!c:\prod_{x:\mathbb{Z}} C(x).(c(0) =_{C(0)} c_0) \times \prod_{x:\mathbb{Z}} c(s(x)) =_{C(s(x))} c_s(c(x))}$$

## Categorical semantics

The fragment of objective type theory consisting of only [[identity types]] and [[dependent product types]] can be interpreted in any [[path category]] with weak homotopy $\Pi$-types. 

## Open problems

There are plenty of questions which are currently unresolved in objective type theory. Van der Berg and Besten in particular listed the following problems in their article:

* Does [[univalence]] imply [[function extensionality]] for types in the universe in [[objective type theory]]?

* Is (the [[homotopy type theory]] based upon) [[Martin-Löf type theory]] conservative over (the [[homotopy type theory]] based upon) [[objective type theory]]?

* How much of the [[HoTT book]] could be done in [[objective type theory]]?

* Does [[objective type theory]] have [[homotopy canonicity]] and [[normalization]]?

Other problems include

* What is the [[categorical semantics]] of the [[homotopy type theory]] based upon [[objective type theory]], with all [[higher inductive types]] and [[weakly Tarski]] [[univalent universes]]? 

* Is [[weak function extensionality]] equivalent to [[function extensionality]] in [[objective type theory]]?

* Does [[product extensionality]] hold in [[objective type theory]]? Namely, given types $A$ and $B$ and elements $a:A \times B$ and $b:A \times B$, is the canonical function $\mathrm{idtoprojectionids}:(a =_{A \times B} b) \to (\pi_1(a) \simeq \pi_1(b)) \times (\pi_2(a) \simeq \pi_2(b))$ an [[equivalence of types]]?

See also [[open problems in homotopy type theory]]

## See also

* [[judgmental equality]], [[identity type]]

* [[dependent type theory]], [[Martin-Löf type theory]], [[homotopy type theory]]

## References

* [[Benno van den Berg]], [[Martijn den Besten]], *Quadratic type checking for objective type theory* ([arXiv:2102.00905](https://arxiv.org/abs/2102.00905))

* [[Mike Shulman]], Towards a Third-Generation HOTT Part 1 ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA))

* *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]], *[[Symmetry]]* (2021) $[$[pdf](https://unimath.github.io/SymmetryBook/book.pdf)$]$ 

[[!redirects objective type theories]]