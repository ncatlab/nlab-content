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

This means that the computation and uniqueness rules ([[beta-reduction]] and [[eta-conversion]]) for each type in the type theory are all propositional computational and uniqueness rules using the [[identity type]], and in particular means that the identity type has to be introduced first before any other type is introduced. As a result, the results in objective type theory are more general than in models which use judgmental equality for computational and uniqueness rules, since judgmental equality implies propositional equality, while the converse isn't necessarily the case. 

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

$$\frac{\vdash \Gamma, a:A, \Delta \; \mathrm{ctx}}{\vdash \Gamma, a:A, \Delta \vdash a:A}$$

Let $\mathcal{J}$ be any arbitrary judgment. Then we have the following rules:

The weakening rule:

$$\frac{\Gamma, \Delta \vdash \mathcal{J} \quad \Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, \Delta \vdash \mathcal{J}}$$

The substitution rule:

$$\frac{\Gamma \vdash a:A \quad \Gamma, b:A, \Delta \vdash \mathcal{J}}{\Gamma, \Delta[a/b] \vdash \mathcal{J}[a/b]}$$

The weakening and substitution rules are admissible rules: they do not need to be explicitly included in the type theory as they could be proven by induction on the structure of all possible derivations. 

### Families of types and elements

A family of types is a type $B$ in the context of the element judgment $x:A$, $x:A \vdash B \; \mathrm{type}$, they are usually written as $B(x)$ to indicate its dependence upon $x$. Given a particular element $a:A$, the type $B(a)$ is a type dependent upon $a:A$. 

A family of terms is a term $b:B$ in the context of the variable judgment $x:A$, $x:A \vdash b:B$. They are likewise usually written as $b(x)$ to indicate its dependence upon $x$. Given a particular element $a:A$, the element $b(a)$ is an element dependent upon $a:A$. 

### Identity types

Equality in objective type theory is represented by the [[identity type]], which is also called the path type or identification type. The terms of the identity type could be called paths or identifications. 

Equality comes with a formation rule, an introduction rule, an elimination rule, and a computation rule:

Formation rule for identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, b:A \vdash a =_A b \; \mathrm{type}}$$

Introduction rule for identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A \vdash \mathrm{refl}_A(a) : a =_A a}$$

Elimination rule for identity types:
$$\frac{\Gamma, x:A, y:A, p:x =_A y \vdash C \mathrm{type} \quad \Gamma, a:A \vdash t:C[a, a, \mathrm{refl}_A(a)/x, y, p]}{\Gamma, x:A, y:A, p:x =_A y \vdash J(t, x, y, p):C}$$

Computation rules for identity types:
$$\frac{\Gamma, x:A, y:A, p:x =_A y \vdash C \mathrm{type} \quad \Gamma, a:A \vdash t:C[a, a, \mathrm{refl}_A(a)/x, y, p]}{\Gamma, a:A \vdash \beta_{=_A}(a) : J(t, a, a, \mathrm{refl}(a)) =_{C[a, a, \mathrm{refl}_A(a)/x, y, p]} t}$$

Optional uniqueness rules for identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash p:a =_A a}{\Gamma\vdash K(a, p):p =_{a =_A a} refl_A(a)}$$

The uniqueness rule for identity types is usually not included in objective type theory. However, if it were included in objective type theory it turns the type theory into a [[set-level type theory]]. 

### Structural rules for definitions

Now that we have finally defined identity types, we can define the structural rules for definitions. The structural rules for term definitions say that given a term $a:A$ and a term definition $b \coloneqq a:A$, one could derive that $b$ is a term of $A$, and that there is an identification between $b$ and $a$:

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash a:A \quad \Gamma \vdash b \coloneqq a:A}{\Gamma \vdash \delta_A(a, b):b =_A a}$$

The structural rules for type definitions are the natural deduction rules for [[copying]] types, with formation and introduction rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{copy}(a):B}$$

elimination rules:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type} \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:B}{\Gamma \vdash \mathrm{ind}_{B}^C(c, e):C[e/z]}$$

computation rules:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type} \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_B:\mathrm{ind}_{B}^C(c, \mathrm{copy}(a)) =_{C[\mathrm{copy}(a)/z]} c[a/x]}$$

and uniqueness rules:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type} \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:B \quad \Gamma, y:B \vdash u:C \quad \Gamma, a:A \vdash i_\mathrm{copy}(u):u[\mathrm{copy}(a)/y] =_{C[\mathrm{copy}(a)/y]} c[a/x]}{\Gamma \vdash \eta_{B}:u[e/z] =_{C[e/z]} \mathrm{ind}_{B}^C(c, e)}$$

Suppose one takes the type family $C$ in the elimination, computation, and uniqueness rules to be the type family $\sum_{x:A} \mathrm{copy}(x) =_B (-)$. Then the elimination rule states that $\sum_{x:A} \mathrm{copy}(x) =_B b$ has an element for all elements $b:B$, the computation rule states that given all elements $a:A$ the type $\sum_{x:A} \mathrm{copy}(x) =_B \mathrm{copy}(a)$ is contractible, and the uniqueness rule states that if the type $\sum_{x:A} \mathrm{copy}(x) =_B \mathrm{copy}(a)$ is contractible for all elements $a:A$, then the type $\sum_{x:A} \mathrm{copy}(x) =_B b$ is contractible for all elements $b:B$. Thus, $\mathrm{copy}$ is an [[equivalence of types]], since the type $\sum_{x:A} \mathrm{copy}(x) =_B b$ is contractible for all elements $b:B$. 

### Subsingletons and singletons

Identity types allow us to establish when a type is a subsingleton and singletons. 

A subsingleton is a type $A$ with a family of identities $a:A, b:B \vdash \mathrm{trunc}(a, b):a =_A b$. Subsingletons are important because they are used to build the logic in objective type theory, and thus are also called [[propositions]]. 

A singleton is a type $A$ with an element $a:A$ and either 

* a family of identities $b:A \vdash \eta_A(b):a =_A b$ stating that $a$ is a [[center of contraction]] of $A$ (axiom K style)
* a family of identities $b:A, c:B \vdash \mathrm{trunc}(b, c):b =_A c$ stating that $A$ is a [[subsingleton]] (UIP style)

Singletons are also called [[contractible types]] or [[true]] types. Equivalently, a singleton is a type $A$ with 

### Unit type

We specify a particular singleton called the [[unit type]], which comes with rules stating that one could form the unit type $\mathbb{1}$, the generic element $*:\mathbb{1}$, and a family of identities stating that $\mathbb{1}$ is a singleton: 

Formation rule for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{1} \; \mathrm{type}}$$

Introduction rule for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash *:\mathbb{1}}$$

Uniqueness rules for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, p:\mathbb{1} \vdash \eta_\mathbb{1}(p):* =_\mathbb{1} p}$$

### Empty type

Formation rules for the empty type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{0} \; \mathrm{type}}$$

Elimination rules for the empty type:
$$\frac{\Gamma, x:\mathbb{0} \vdash C \; \mathrm{type} \quad \Gamma \vdash p:\mathbb{0}}{\Gamma \vdash \mathrm{ind}_\mathbb{0}^C(p):C(p)}$$

Uniqueness rules for the empty type:
$$\frac{\Gamma, x:\mathbb{0} \vdash C \; \mathrm{type} \quad \Gamma \vdash p:\mathbb{0} \quad \Gamma, x:\mathbb{0} \vdash u:C}{\Gamma \vdash \eta_\mathbb{0}(p, u):u[p/x] =_{C[p/x]} \mathrm{ind}_\mathbb{0}^{C}(p)}$$

### Function types

Formation rules for function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \to B \; \mathrm{type}}$$

Introduction rules for function types:
$$\frac{\Gamma, x:A \vdash b(x):B}{\Gamma \vdash (x \mapsto b(x)):A \to B}$$

Elimination rules for function types:
$$\frac{\Gamma \vdash f:A \to B \quad \Gamma \vdash a:A}{\Gamma \vdash f(a):B}$$

Computation rules for function types:
$$\frac{\Gamma, x:A \vdash b(x):B \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_{\to}:(x \mapsto b(x))(a) =_{B} b}$$

Uniqueness rules for function types:
$$\frac{\Gamma \vdash f:A \to B}{\Gamma \vdash \eta_{\to}:f =_{A \to B} (x \to f(x))}$$

### Pi types

Formation rules for Pi types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \prod_{x:A} B(x) \; \mathrm{type}}$$

Introduction rules for Pi types:
$$\frac{\Gamma, x:A \vdash b(x):B(x)}{\Gamma \vdash \lambda(x:A).b(x):\prod_{x:A} B(x)}$$

Elimination rules for Pi types:
$$\frac{\Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash f(a):B[a/x]}$$

Computation rules for Pi types:
$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_\Pi:\lambda(x:A).b(x)(a) =_{B[a/x]} b[a/x]}$$

Uniqueness rules for Pi types:
$$\frac{\Gamma \vdash f:\prod_{x:A} B(x)}{\Gamma \vdash \eta_\Pi:f =_{\prod_{x:A} B(x)} \lambda(x).f(x)}$$

### Product types

We use the positive presentation for product types. 

Formation rules for product types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \times B \; \mathrm{type}}$$

Introduction rules for product types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma\vdash B \; \mathrm{type}}{\Gamma, x:A, y:B \vdash (x, y):A \times B}$$

Elimination rules for product types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, z:A \times B \vdash C \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash c:C[(x, y)/z]}{\Gamma, z:A \times B \vdash \mathrm{ind}_{A \times B}^C(c):C}$$

Computation rules for product types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, z:A \times B \vdash C \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash c:C[(x, y)/z]}{\Gamma, x:A, y:B \vdash \beta_{A \times B}^C(c):\mathrm{ind}_{A \times B}^C(c)[(x, y)/z] =_{C[(x, y)/z]} c}$$

Uniqueness rules for product types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma\vdash B \; \mathrm{type} \quad \Gamma, z:A \times B \vdash C \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash c:C[(x, y)/z] \quad \Gamma, z:A \times B \vdash u:C \quad \Gamma, x:A, y:B \vdash i_{(-,-)}(u):u[(x, y)/z] =_{C[(x, y)/z]} c}{\Gamma, z:A \times B \vdash \eta_{A \times B}^C(c):u =_{C} \mathrm{ind}_{A \times B}^C(c)}$$

### Sigma types

We use the positive presentation for sigma types. 

Formation rules for sigma types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type}}{\Gamma \vdash \Sigma (x:A).B(x) \; \mathrm{type}}$$

Introduction rules for sigma types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type}}{\Gamma, x:A, y:B \vdash \mathrm{in}(x, y):\Sigma (x:A).B(x)}$$

Elimination rules for sigma types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type} \quad \Gamma, z:\Sigma (x:A).B(x) \vdash C \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash c:C[\mathrm{in}(x, y)/z]}{\Gamma, z:\Sigma (x:A).B(x) \vdash \mathrm{ind}_{\Sigma (x:A).B(x)}^C(c):C}$$

Computation rules for sigma types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type} \quad \Gamma, z:\Sigma (x:A).B(x) \vdash C \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash c:C[\mathrm{in}(x, y)/z]}{\Gamma, x:A, y:B \vdash \beta_{\Sigma (x:A).B(x)}^C(c):\mathrm{ind}_{\Sigma (x:A).B(x)}^C(c)[\mathrm{in}(x, y)/z] =_{C[\mathrm{in}(x, y)/z]} c}$$

Uniqueness rules for sigma types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type} \quad \Gamma, z:\Sigma (x:A).B(x) \vdash C \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash c:C[\mathrm{in}(x, y)/z] \quad \Gamma, z:\Sigma (x:A).B(x) \vdash u:C \quad \Gamma, x:A, y:B \vdash i_\mathrm{in}(u):u[\mathrm{in}(x, y)/z] =_{C[\mathrm{in}(x, y)/z]} c}{\Gamma, e:\Sigma (x:A).B(x) \vdash \eta_{\Sigma (x:A).B(x)}^C(c):u[e/z] =_{C[e/z]} \mathrm{ind}_{\Sigma (x:A).B(x)}^C(c)[e/z]}$$

### Sum types

Formation rules for sum types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A + B \; \mathrm{type}}$$

Introduction rules for sum types:
$$\frac{\Gamma \vdash a:A}{\Gamma \vdash \mathrm{inl}(a):A + B} \qquad \frac{\Gamma \vdash b:B}{\Gamma \vdash \mathrm{inr}(b):A + B}$$

Elimination rules for sum types:
$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c(x):C(\mathrm{inl}(x)) \quad \Gamma, y:B \vdash d(y):C(\mathrm{inr}(y))}{\Gamma, z:A + B \vdash \mathrm{ind}_{A + B}^C(c(x), d(y)):C}$$

Computation rules for sum types:
$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c(x):C(\mathrm{inl}(x)) \quad \Gamma, y:B \vdash d(y):C(\mathrm{inr}(y)) \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_1:\mathrm{ind}_{A + B}^C(c(x), d(y))(\mathrm{inl}(a)) =_{C(\mathrm{inl}(a))} c(a)}$$
$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c(x):C(\mathrm{inl}(x)) \quad \Gamma, y:B \vdash d(y):C(\mathrm{inr}(y)) \quad \Gamma \vdash b:B}{\Gamma \vdash \beta_2:\mathrm{ind}_{A + B}^C(c(x), d(y))(\mathrm{inr}(b)) =_{C(\mathrm{inr}(b))} d(b)}$$

Uniqueness rules for sum types:
$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c(x):C(\mathrm{inl}(x)) \quad \Gamma, y:B \vdash d(y):C(\mathrm{inr}(y)) \quad \Gamma, x:A + B \vdash u:C \quad \Gamma, a:A \vdash i_\mathrm{inl}(u):u(\mathrm{inl}(a)) =_{C(\mathrm{inl}(a))} c(a) \quad \Gamma, b:B \vdash i_\mathrm{inr}(u):u(\mathrm{inr}(b)) =_{C(\mathrm{inr}(b))} d(b)}{\Gamma, z:A + B \vdash \eta_{A + B}:u(z) =_{C(z)} \mathrm{ind}_{A + B}^C(c(\mathrm{inl}(z)), d(\mathrm{inl}(z)))(z)}$$

### Booleans

Formation rules for the booleans:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{2} \; \mathrm{type}}$$

Introduction rules for the booleans:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{2}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 1:\mathbb{2}}$$

Elimination rules for the booleans:
$$\frac{\Gamma, x:\mathbb{2} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma \vdash c_1:C[1/x] \quad \Gamma \vdash p:\mathbb{2}}{\Gamma \vdash \mathrm{ind}_\mathbb{2}^{C}(p, c_0, c_1):C[p/x]}$$

Computation rules for the booleans:
$$\frac{\Gamma, x:\mathbb{2} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma \vdash c_1:C[1/x]}{\Gamma \vdash \beta_\mathbb{2}^{0}: \mathrm{ind}_\mathbb{2}^{C}(0, c_0, c_1) =_{C[0/x]} c_0}$$

$$\frac{\Gamma, x:\mathbb{2} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma \vdash c_1:C[1/x]}{\Gamma \vdash \beta_\mathbb{2}^{1}: \mathrm{ind}_\mathbb{2}^{C}(1, c_0, c_1) =_{C[1/x]} c_1}$$

Uniqueness rules for the booleans:
$$\frac{\Gamma, x:\mathbb{2} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma \vdash c_1:C[1/x] \quad \Gamma \vdash p:\mathbb{2} \quad \Gamma, x:\mathbb{2} \vdash u:C \quad \Gamma \vdash i_0(u):u[0/x] =_{C[0/x]} c_0 \quad \Gamma \vdash i_1(u):u[1/x] =_{C[1/x]} c_1}{\Gamma \vdash \eta_\mathbb{2}(p, u):u[p/x] =_{C[p/x]} \mathrm{ind}_\mathbb{2}^{C}(p, c_0, c_1)}$$

### Natural numbers

Formation rules for the natural numbers:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{N} \; \mathrm{type}}$$

Introduction rules for the natural numbers:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{N}} \qquad \frac{\Gamma \vdash n:\mathbb{N}}{\Gamma \vdash s(n):\mathbb{N}}$$

Elimination rules for the natural numbers:
$$\frac{\Gamma, x:\mathbb{N} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma, x:\mathbb{N}, c:C \vdash c_s:C[s(x)/x] \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^C(n, c_0, c_s):C[n/x]}$$

Computation rules for the natural numbers:
$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma, x:\mathbb{N}, c:C \vdash c_s:C[s(x)/x]}{\Gamma \vdash \beta_\mathbb{N}^{0}: \mathrm{ind}_\mathbb{N}^C(0, c_0, c_s) =_{C[0/x]} c_0}$$

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma, x:\mathbb{N}, c:C \vdash c_s:C[s(x)/x]}{\Gamma \vdash \beta_\mathbb{N}^{s(n)}: \mathrm{ind}_\mathbb{N}^C(s(n), c_0, c_s) =_{C[s(n)/x]} c_s(n, \mathrm{ind}_\mathbb{N}^C(n, c_0, c_s))}$$

Uniqueness rules for the natural numbers:
$$\frac{\Gamma, x:\mathbb{N} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma, x:\mathbb{N}, c:C \vdash c_s:C[s(x)/x] \quad \Gamma \vdash n:\mathbb{N} \quad \Gamma, x:\mathbb{N} \vdash u:C \quad \Gamma \vdash i_0(u):u[0/x] =_{C[0/x]} c_0 \quad \Gamma, x:\mathbb{N} \vdash i_s(u):u[s(x)/x] =_{C[s(x)/x]} c_s[u/c]}{\Gamma \vdash \eta_\mathbb{N}(n, u):u[n/x] =_{C[n/x]} \mathrm{ind}_\mathbb{N}^{C}(p, c_0, c_s)}$$

### Equivalence types

Given a type $A$, we define the type $\mathrm{isContr}(A)$ representing whether $A$ is a [[contractible type]] as 
$$\mathrm{isContr}(A) \coloneqq \sum_{a:A} \prod_{b:A} a =_A b$$

Given types $A$ and $B$, function $f:A \to B$, and element $b:B$, we define the [[fiber]] of $f$ at $b$  $\mathrm{fiber}_{A, B}(f, y)$ as
$$\mathrm{fiber}_{A, B}(f, y) \coloneqq \sum_{a:A} f(a) =_B b$$

Given types $A$ and $B$ and function $f:A \to B$, we define the type $\mathrm{isEquiv}(f)$ representing whether $f$ is a [[equivalence of types]] as 
$$\mathrm{isEquiv}(f) \coloneqq \prod_{b:B} \mathrm{isContr}(\mathrm{fiber}_{A, B}(f, b))$$

Given types $A$ and $B$, we define the type of equivalences $A \simeq B$ as
$$A \simeq B \coloneqq \sum_{f:A \to B} \mathrm{isEquiv}(f)$$

The equivalence types between two types $A$ and $B$ behaves as the equality between $A$ and $B$, in the same way that the identity type between two terms $a:A$ and $b:A$ behaves as the equality between $a$ and $b$. This is similar to [[structural set theory]] whose type of sets have no primitive equality relation, where [[bijection]] behaves as the equality between sets $A$ and $B$. 

### Transport

Transport is the statement that given a type family $P$ indexed by $A$ and elements $a:A$ and $b:A$, there is a function $\mathrm{trans}^P(a, b):(a =_A b) \to (P(a) \simeq P(b))$ from the identity type of $a$ and $b$ to the type of equivalences between the types $P(a)$ and $P(b)$. This is inductively defined on reflexivity on $a:A$, which transport takes to the identity function on $P(a)$, $\mathrm{trans}^P(a, a, \mathrm{refl}_A(a)) =_{P(a) \simeq P(a)} id_{P(a)}$. 

Transport is given by the following rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash P \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A}{\Gamma \vdash \mathrm{trans}^P(a, b):(a =_A b) \to (P[a/x] \simeq P[b/x])}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash P \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{ind}_{\mathrm{trans}^P}^{\mathrm{refl}}:\mathrm{trans}^P(a, a)(\mathrm{refl}_A(a)) =_{P[a/x] \simeq P[a/x]} \mathrm{id}_{P[a/x]}}$$

Transport is very important in defining [[univalent Tarski universes]] as well as [[dependent identity types]], which in turn are important in defining [[higher inductive types]], in objective type theory. 

### Dependent identity types

We define the [[dependent identity type]] as follows:

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma \vdash x:P(a) \quad \Gamma \vdash y:P(b)}{\Gamma \vdash x =_P^p y \coloneqq \mathrm{trans}^P(p)(x) =_{P(b)} y \; \mathrm{type}}$$

### Dependent actions on identifications

Additionally, for a term $f:P$ in the context of $x:A$, there is a [[dependent identification]] called the [[dependent action on identifications]] $\mathrm{apd}(f)(p):f(x) =_P^p f(y)$ for all $x:A$, $y:A$, and $p:x =_A y$, inductively defined by reflexivity for all $x:A$. 
$$\mathrm{apd}(f)(\mathrm{refl}_A(x)):f(x) =_P^{\mathrm{refl}_A(x)} f(x)$$

The rules for $\mathrm{apd}$ are as follows
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash f:P}{\Gamma, x:A, y:A, p:x =_A y \vdash \mathrm{apd}(f)(p):f(x) =_P^p f(y)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash f:P}{\Gamma, x:A \vdash \mathrm{apd}(f)(\mathrm{refl}_A(x)):f(x) =_P^{\mathrm{refl}_A(x)} f(x)}$$

### Universes

Universes are internal models of [[dependent type theory]] inside of the type theory itself. An universe consists of a type of encodings for types $\mathcal{U}$ and a universal type family $\mathcal{T}$ which takes the encodings and returns an actual type, resulting in the formation and type reflection rules for universes:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathcal{U} \; \mathrm{type}} \qquad \frac{\Gamma \vdash A:\mathcal{U}}{\Gamma \vdash \mathcal{T}(A) \; \mathrm{type}}$$

Given an encoding $A:\mathcal{U}$, an internal type family indexed by $A$ is a function $B:\mathcal{T}(A) \to \mathcal{U}$. 

#### Univalence

There are two ways to say that $A:\mathcal{U}$ and $B:\mathcal{U}$ are the same, by way of the identity type of the universe $A =_\mathcal{U} B$, and by way of the type of equivalences between the type reflections of $A:\mathcal{U}$ and $B:\mathcal{U}$, $\mathcal{T}(A) \simeq \mathcal{T}(B)$. By [[transport]], there is a canonical function 
$$\mathrm{trans}^{\mathcal{T}}(A, B):(A =_\mathcal{U} B) \to (\mathcal{T}(A) \simeq \mathcal{T}(B))$$
The universe $\mathcal{U}$ is then said to be a [[univalent universe]] if the transport function $\mathrm{trans}^{\mathcal{T}}(A, B)$ is an equivalence of types
$$\mathrm{univalence}(A, B):\mathrm{isEquiv}(\mathrm{trans}^{\mathcal{T}}(A, B))$$
for all encodings $A:\mathcal{U}$ and $B:\mathcal{U}$. This is given by the following rule

$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash B:\mathcal{U}}{\Gamma \vdash \mathrm{univalence}(A, B):\mathrm{isEquiv}(\mathrm{trans}^{\mathcal{T}}(A, B))}$$

Universes are usually also required to be closed under all the type formers introduced previously.

#### Internal identity types

A universe $\mathcal{U}$ is closed under identity types if it has an internal encoding of identity types in the universe: Given an element $A:\mathcal{U}$, there is a function $\mathrm{Id}^\mathcal{U}(A):\mathcal{T}(A) \times \mathcal{T}(A) \to \mathcal{U}$ and for all elements $a:\mathcal{T}(A)$ and $b:\mathcal{T}(A)$ an equivalence 
$$\mathrm{canonical}_{\mathrm{Id}}^{\mathcal{U}}(A)(a, b):\mathcal{T}(\mathrm{Id}^\mathcal{U}(A)(a, b)) \simeq (a =_{\mathcal{T}(A)} b)$$

The rules for the internal identity types are thus given by

$$\frac{\Gamma \vdash A:\mathcal{U}}{\Gamma \vdash \mathrm{Id}^\mathcal{U}(A):\mathcal{T}(A) \times \mathcal{T}(A) \to \mathcal{U}} \qquad \frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash a:\mathcal{T}(A) \quad \Gamma \vdash b:\mathcal{T}(A)}{\Gamma \vdash \mathrm{canonical}_{\mathrm{Id}}^{\mathcal{U}}(A)(a, b):\mathcal{T}(\mathrm{Id}^\mathcal{U}(A)(a, b)) \simeq (a =_{\mathcal{T}(A)} b)}$$

#### Internal function types

A universe $\mathcal{U}$ is closed under function types if it has an internal encoding of function types in the universe: given an element $A:\mathcal{U}$ and an element $B:\mathcal{U}$, there is an element $A \to_\mathcal{U} B:\mathcal{U}$, and an equivalence
$$\mathrm{canonical}_{\to}^{\mathcal{U}}(A, B):\mathcal{T}(A \to_\mathcal{U} B) \simeq \mathcal{T}(A) \to \mathcal{T}(B)$$

The rules for the internal function types are thus given by

$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash B:\mathcal{U}}{\Gamma \vdash A \to_\mathcal{U} B:\mathcal{U}} \qquad \frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash B:\mathcal{U}}{\Gamma \vdash \mathrm{canonical}_{\to}^{\mathcal{U}}(A, B):\mathcal{T}(A \to_\mathcal{U} B) \simeq \mathcal{T}(A) \to \mathcal{T}(B)}$$

#### Internal pi types

A universe $\mathcal{U}$ is closed under pi types if it has an internal encoding of pi types in the universe: given an element $A:\mathcal{U}$ and a function $B:\mathcal{T}(A) \to \mathcal{U}$, there is an element $\Pi_\mathcal{U}(x:A).B(x):\mathcal{U}$, and an equivalence
$$\mathrm{canonical}_\Pi^{\mathcal{U}}(A, B):\mathcal{T}(\Pi_\mathcal{U}(x:A).B(x)) \simeq \prod_{x:\mathcal{T}(A)} \mathcal{T}(B(x))$$

The rules for the internal pi types are thus given by

$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash B:\mathcal{T}(A) \to \mathcal{U}}{\Gamma \vdash \Pi_\mathcal{U}(x:A).B(x):\mathcal{U}} \qquad \frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash B:\mathcal{T}(A) \to \mathcal{U}}{\Gamma \vdash \mathrm{canonical}_\Pi^{\mathcal{U}}(A, B):\mathcal{T}(\Pi_\mathcal{U}(x:A).B(x)) \simeq \prod_{x:\mathcal{T}(A)} \mathcal{T}(B(x))}$$

#### Internal product types

A universe $\mathcal{U}$ is closed under product types if it has an internal encoding of product types in the universe: given an element $A:\mathcal{U}$ and an element $B:\mathcal{U}$, there is an element $A \times_\mathcal{U} B:\mathcal{U}$, and an equivalence
$$\mathrm{canonical}_{\times}^{\mathcal{U}}(A, B):\mathcal{T}(A \times_\mathcal{U} B) \simeq \mathcal{T}(A) \times \mathcal{T}(B)$$

The rules for the internal product types are thus given by

$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash B:\mathcal{U}}{\Gamma \vdash A \times_\mathcal{U} B:\mathcal{U}} \qquad \frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash B:\mathcal{U}}{\Gamma \vdash \mathrm{canonical}_{\to}^{\mathcal{U}}(A, B):\mathcal{T}(A \times_\mathcal{U} B) \simeq \mathcal{T}(A) \times \mathcal{T}(B)}$$

#### Internal sigma types

A universe $\mathcal{U}$ is closed under sigma types if it has an internal encoding of sigma types in the universe: given an element $A:\mathcal{U}$ and a function $B:\mathcal{T}(A) \to \mathcal{U}$, there is an element $\Sigma_\mathcal{U}(x:A).B(x):\mathcal{U}$, and an equivalence
$$\mathrm{canonical}_\Sigma^{\mathcal{U}}(A, B):\mathcal{T}(\Sigma_\mathcal{U}(x:A).B(x)) \simeq \sum_{x:\mathcal{T}(A)} \mathcal{T}(B(x))$$

The rules for the internal sigma types are thus given by

$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash B:\mathcal{T}(A) \to \mathcal{U}}{\Gamma \vdash \Sigma_\mathcal{U}(x:A).B(x):\mathcal{U}} \qquad \frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash B:\mathcal{T}(A) \to \mathcal{U}}{\Gamma \vdash \mathrm{canonical}_\Sigma^{\mathcal{U}}(A, B):\mathcal{T}(\Pi_\mathcal{U}(x:A).B(x)) \simeq \sum_{x:\mathcal{T}(A)} \mathcal{T}(B(x))}$$

#### Internal sum types

A universe $\mathcal{U}$ is closed under sum types if it has an internal encoding of sum types in the universe: given an element $A:\mathcal{U}$ and an element $B:\mathcal{U}$, there is an element $A +_\mathcal{U} B:\mathcal{U}$, and an equivalence
$$\mathrm{canonical}_{+}^{\mathcal{U}}(A, B):\mathcal{T}(A +_\mathcal{U} B) \simeq \mathcal{T}(A) + \mathcal{T}(B)$$

The rules for the internal sum types are thus given by

$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash B:\mathcal{U}}{\Gamma \vdash A +_\mathcal{U} B:\mathcal{U}} \qquad \frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash B:\mathcal{U}}{\Gamma \vdash \mathrm{canonical}_{+}^{\mathcal{U}}(A, B):\mathcal{T}(A +_\mathcal{U} B) \simeq \mathcal{T}(A) + \mathcal{T}(B)}$$

#### Internal empty type

A universe $\mathcal{U}$ is closed under the empty type if it has an internal encoding of the empty type in the universe: there is an element $\mathbb{0}_\mathcal{U}:\mathcal{U}$, and an equivalence
$$\mathrm{canonical}_{\mathbb{0}}^{\mathcal{U}}:\mathcal{T}(\mathbb{0}_\mathcal{U}) \simeq \mathbb{0}$$

The rules for the internal empty type are thus given by

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{0}_\mathcal{U}:\mathcal{U}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{canonical}_{\mathbb{0}}^{\mathcal{U}}:\mathcal{T}(\mathbb{0}_\mathcal{U}) \simeq \mathbb{0}}$$

#### Internal unit type

A universe $\mathcal{U}$ is closed under the unit type if it has an internal encoding of the unit type in the universe: there is an element $\mathbb{1}_\mathcal{U}:\mathcal{U}$, and an equivalence
$$\mathrm{canonical}_{\mathbb{1}}^{\mathcal{U}}:\mathcal{T}(\mathbb{1}_\mathcal{U}) \simeq \mathbb{1}$$

The rules for the internal unit type are thus given by

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{1}_\mathcal{U}:\mathcal{U}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{canonical}_{\mathbb{1}}^{\mathcal{U}}:\mathcal{T}(\mathbb{1}_\mathcal{U}) \simeq \mathbb{1}}$$

#### Internal booleans type

A universe $\mathcal{U}$ is closed under the booleans type if it has an internal encoding of the booleans type in the universe: there is an element $\mathbb{2}_\mathcal{U}:\mathcal{U}$, and an equivalence
$$\mathrm{canonical}_{\mathbb{2}}^{\mathcal{U}}:\mathcal{T}(\mathbb{2}_\mathcal{U}) \simeq \mathbb{2}$$

The rules for the internal booleans type are thus given by

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{2}_\mathcal{U}:\mathcal{U}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{canonical}_{\mathbb{2}}^{\mathcal{U}}:\mathcal{T}(\mathbb{2}_\mathcal{U}) \simeq \mathbb{2}}$$

#### Internal natural numbers type

A universe $\mathcal{U}$ is closed under the natural numbers type if it has an internal encoding of the natural numbers type in the universe: there is an element $\mathbb{N}_\mathcal{U}:\mathcal{U}$, and an equivalence
$$\mathrm{canonical}_{\mathbb{N}}^{\mathcal{U}}:\mathcal{T}(\mathbb{N}_\mathcal{U}) \simeq \mathbb{N}$$

The rules for the internal natural numbers type are thus given by

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{N}_\mathcal{U}:\mathcal{U}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{canonical}_{\mathbb{N}}^{\mathcal{U}}:\mathcal{T}(\mathbb{N}_\mathcal{U}) \simeq \mathbb{N}}$$

## Categorical semantics

The fragment of objective type theory consisting of only [[identity types]] and [[dependent product types]] can be interpreted in any [[path category]] with weak homotopy $\Pi$-types. 

## Open problems

There are plenty of questions which are currently unresolved in objective type theory. Van der Berg and Besten in particular listed the following problems in their article:

* Does [[univalence]] imply [[function extensionality]] in [[objective type theory]]?

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

* *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([pdf](https://raw.githubusercontent.com/martinescardo/HoTTEST-Summer-School/main/HoTT/hott-intro.pdf)) (478 pages)

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]], *[[Symmetry]]* (2021) $[$[pdf](https://unimath.github.io/SymmetryBook/book.pdf)$]$ 

[[!redirects objective type theory]]
[[!redirects objective type theories]]