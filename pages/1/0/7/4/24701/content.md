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

This means that the computation and uniqueness rules ([[beta-reduction]] and [[eta-conversion]]) for each type in the type theory are all propositional computational and uniqueness rules using the [[identity type]], and in particular means that the identity type has to be introduced first before any other type is introduced. 

Objective type theory has [[decidable]] [[type checking]], and the type checking can be done in quadratic time. 

## Syntax

### Judgments and contexts

Objective type theory consists of three judgments: type judgments $A \; \mathrm{type}$, where we judge $A$ to be a type, typing judgments, where we judge $a$ to be an element of $A$, $a:A$, and context judgments, where we judge $\Gamma$ to be a context, $\Gamma \; \mathrm{ctx}$. Contexts are lists of typing judgments $a:A$, $b:B$, $c:C$, et cetera, and are formalized by the rules for the empty context and extending the context by a typing judgment

$$\frac{}{() \; \mathrm{ctx}} \qquad \frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash A \; \mathrm{type}}{(\Gamma, a:A) \; \mathrm{ctx}}$$

### Structural rules

There are three structural rules in objective type theory, the [[variable rule]], the [[weakening rule]], and the [[substitution rule]]. 

The variable rule states that we may derive a typing judgment if the typing judgment is in the context already:

$$\frac{\Gamma, a:A, \Delta \; \mathrm{ctx}}{\Gamma, a:A, \Delta \vdash a:A}$$

Let $\mathcal{J}$ be any arbitrary judgment. Then we have the following rules:

The weakening rule:

$$\frac{\Gamma, \Delta \vdash \mathcal{J} \quad \Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, \Delta \vdash \mathcal{J}}$$

The substitution rule:

$$\frac{\Gamma \vdash a:A \quad \Gamma, b:A, \Delta \vdash \mathcal{J}}{\Gamma, \Delta[a/b] \vdash \mathcal{J}[a/b]}$$

The weakening and substitution rules are admissible rules: they do not need to be explicitly included in the type theory as they could be proven by induction on the structure of all possible derivations. 

### Dependent types and sections

A dependent type is a type $B$ in the context of the variable judgment $x:A$, $x:A \vdash B \; \mathrm{type}$, they are usually written as $B(x)$ to indicate its dependence upon $x$. 

A section or dependent term is a term $b:B$ in the context of the variable judgment $x:A$, $x:A \vdash b:B$. Sections are likewise usually written as $b(x)$ to indicate its dependence upon $x$. 

### Identity types

Equality in objective type theory is represented by the [[identity type]], which is also called the path type or identification type. The terms of the identity type could be called paths or identifications. 

Equality comes with a formation rule, an introduction rule, an elimination rule, and a computation rule:

Formation rule for identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, b:A \vdash a =_A b \; \mathrm{type}}$$

Introduction rule for identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A \vdash \mathrm{refl}_A(a) : a =_A a}$$

Elimination rule for identity types:
$$\frac{\Gamma, a:A, b:A, p:a =_A b, \Delta(a, b, p) \vdash C(a, b, p) \mathrm{type} \quad \Gamma, a:A, \Delta(a, a, \mathrm{refl}_A(a)) \vdash t:C(a, a, \mathrm{refl}_A(a))}{\Gamma, a:A, b:A, p:a =_A b, \Delta(a, b, p) \vdash J(t, a, b, p):C(a, b, p)}$$

Computation rules for identity types:
$$\frac{\Gamma, a:A, b:A, p:a =_A b, \Delta(a, b, p) \vdash C(a, b, p) \; \mathrm{type} \quad \Gamma, a:A, \Delta(a, a, \mathrm{refl}_A(a)) \vdash t:C(a, a, \mathrm{refl}_A(a))}{\Gamma, a:A, b:A, p:a =_A b, \Delta(a, b, p) \vdash \beta_{=_A}(a) : J(t, a, a, \mathrm{refl}(a)) =_{C(a, a, \mathrm{refl}_A(a))} t}$$

The [[uniqueness of identity proofs|uniqueness rule for identity types]] is usually not included in objective type theory. However, if it were included in objective type theory it turns the type theory into a [[set-level type theory]]. 

### Definitions of elements

Parts of the following section is adapted from [[Egbert Rijke]]'s [[Introduction to Homotopy Type Theory]]:

We can make definitions at the end of a derivation if the conclusion is a certain term of a type in context, where we have a derivation 
$$\frac{\mathcal{D}}{\Gamma \vdash a:A}$$
if we wish to make a definition $b \coloneqq a$, then we can extend the derivation tree with 
$$\frac{\Gamma \vdash a:A}{\Gamma \vdash b \coloneqq a:A}$$
The effect of such a definition is that we have extended our type theory with a new constant $b$, for which the following inference rules are valid 
$$\frac{\mathcal{D}}{b:A} \qquad \frac{\mathcal{D}}{\mathrm{defeq}(a, b):b =_A a}$$

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

### Definitions of types

Suppose that one wants to define the symbol $B$ as the type $A$. This is done by defining $B$ as the [[inductive type]] generated by the function $\mathrm{copy}:A \to B$. The rules for defining $B$ are then given as follows:

Formation rules for the symbol $B$:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash B \; \mathrm{type}}$$

Introduction rules for the symbol $B$:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{copy}(a):B}$$

Elimination rules for the symbol $B$:
$$\frac{\Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:B}{\Gamma \vdash \mathrm{ind}_{B}^C(c, e):C[e/z]}$$

Computation rules for the symbol $B$:
$$\frac{\Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_B:\mathrm{ind}_{B}^C(c, \mathrm{copy}(a)) =_{C[\mathrm{copy}(a)/z]} c[a/x]}$$

Uniqueness rules for the symbol $B$:
$$\frac{\Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:B \quad \Gamma, y:B \vdash u:C \quad \Gamma, a:A \vdash i_\mathrm{copy}(u):u[\mathrm{copy}(a)/y] =_{C[\mathrm{copy}(a)/y]} c[a/x]}{\Gamma \vdash \eta_{B}:u[e/z] =_{C[e/z]} \mathrm{ind}_{B}^C(c, e)}$$

Examples given later include [[isContr]], [[fiber types]], [[isEquiv]], and the [[type of equivalences]]. 

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

We use the negative presentation for product types. 

Formation rules for product types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \times B \; \mathrm{type}}$$

Introduction rules for product types:
$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B}{\Gamma \vdash (a, b):A \times B}$$

Elimination rules for product types:
$$\frac{\Gamma \vdash z:A \times B}{\Gamma \vdash \pi_1(z):A} \qquad \frac{\Gamma \vdash z:A \times B}{\Gamma \vdash \pi_2(z):B}$$

Computation rules for product types:
$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B}{\Gamma \vdash \beta_{\times 1}:\pi_1(a, b) =_A a} \qquad \frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B}{\Gamma \vdash \beta_{\times 2}:\pi_2(a, b) =_B b}$$

Uniqueness rules for product types:
$$\frac{\Gamma \vdash z:A \times B}{\Gamma \vdash \eta_\times:z =_{A \times B} (\pi_1(z), \pi_2(z))}$$

### Sigma types

We use the negative presentation for sigma types. 

Formation rules for Sigma types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \sum_{x:A} B(x) \; \mathrm{type}}$$

Introduction rules for Sigma types:
$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A \quad \Gamma \vdash b:B[a/x]}{\Gamma \vdash (a, b):\sum_{x:A} B(x)}$$

Elimination rules for Sigma types:
$$\frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash \pi_1(z):A} \qquad \frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash \pi_2(z):B(\pi_1(z))}$$

Computation rules for Sigma types:
$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_{\Sigma 1}:\pi_1(a, b) =_A a} \qquad \frac{\Gamma, x:A \vdash b:B \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_{\Sigma 2}:\pi_2(a, b) =_{B\pi_1(a, b)} b}$$

Uniqueness rules for Sigma types:
$$\frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash \eta_\Sigma:z =_{\sum_{x:A} B(x)} (\pi_1(z), \pi_2(z))}$$

### Sum types

Formation rules for sum types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A + B \; \mathrm{type}}$$

Introduction rules for sum types:
$$\frac{\Gamma \vdash a:A}{\Gamma \vdash \mathrm{inl}(a):A + B} \qquad \frac{\Gamma \vdash b:B}{\Gamma \vdash \mathrm{inr}(b):A + B}$$

Elimination rules for sum types:
$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c(x):C(\mathrm{inl}(x)) \quad \Gamma, y:B \vdash d(y):C(\mathrm{inr}(y)) \quad \Gamma \vdash e:A + B}{\Gamma \vdash \mathrm{ind}_{A + B}^C(c(x), d(y), e):C(e)}$$

Computation rules for sum types:
$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c(x):C(\mathrm{inl}(x)) \quad \Gamma, y:B \vdash d(y):C(\mathrm{inr}(y)) \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_1:\mathrm{ind}_{A + B}^C(c(x), d(y), \mathrm{inl}(a)) =_{C(\mathrm{inl}(a))} c(a)}$$
$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c(x):C(\mathrm{inl}(x)) \quad \Gamma, y:B \vdash d(y):C(\mathrm{inr}(y)) \quad \Gamma \vdash b:B}{\Gamma \vdash \beta_2:\mathrm{ind}_{A + B}^C(c(x), d(y), \mathrm{inr}(b)) =_{C(\mathrm{inr}(b))} d(b)}$$

Uniqueness rules for sum types:
$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c(x):C(\mathrm{inl}(x)) \quad \Gamma, y:B \vdash d(y):C(\mathrm{inr}(y)) \quad \Gamma \vdash e:A + B \quad \Gamma, x:A + B \vdash u:C \quad \Gamma, a:A \vdash i_\mathrm{inl}(u):u(\mathrm{inl}(a)) =_{C(\mathrm{inl}(a))} c(a) \quad \Gamma, b:B \vdash i_\mathrm{inr}(u):u(\mathrm{inr}(b)) =_{C(\mathrm{inr}(b))} d(b)}{\Gamma \vdash \eta_{A + B}:u(e) =_{C(e)} \mathrm{ind}_{A + B}^C(c(\mathrm{inl}(e)), d(\mathrm{inl}(e)), e)}$$

### Empty type

Formation rules for the empty type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{0} \; \mathrm{type}}$$

Elimination rules for the empty type:
$$\frac{\Gamma, x:\mathbb{0} \vdash C \; \mathrm{type} \quad \Gamma \vdash p:\mathbb{0}}{\Gamma \vdash \mathrm{ind}_\mathbb{0}^C(p):C(p)}$$

Uniqueness rules for the empty type:
$$\frac{\Gamma, x:\mathbb{0} \vdash C \; \mathrm{type} \quad \Gamma \vdash p:\mathbb{0} \quad \Gamma, x:\mathbb{0} \vdash u:C}{\Gamma \vdash \eta_\mathbb{0}(p, u):u[p/x] =_{C[p/x]} \mathrm{ind}_\mathbb{0}^{C}(p)}$$

### Unit type

Formation rules for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{1} \; \mathrm{type}}$$

Introduction rules for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash *:\mathbb{1}}$$

Elimination rules for the unit type:
$$\frac{\Gamma, x:\mathbb{1} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_*:C[*/x] \quad \Gamma \vdash p:\mathbb{1}}{\Gamma \vdash \mathrm{ind}_\mathbb{1}^C(p, c_*):C[p/x]}$$

Computation rules for the unit type:
$$\frac{\Gamma, x:\mathbb{1} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_*:C[*/x]}{\Gamma \vdash \beta_\mathbb{1}: \mathrm{ind}_\mathbb{1}^C(*, c_*) =_{C[*/x]} c_*}$$

Uniqueness rules for the unit type:
$$\frac{\Gamma, x:\mathbb{1} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_*:C[*/x] \quad \Gamma \vdash p:\mathbb{1} \quad \Gamma, x:\mathbb{1} \vdash u:C \quad \Gamma \vdash i_*(u):u[*/x] =_{C[*/x]} c_* }{\Gamma \vdash \eta_\mathbb{1}(p, u):u[p/x] =_{C[p/x]} \mathrm{ind}_\mathbb{1}^{C}(p, c_*)}$$

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

### isContr types

Given a type $A$, we define the type $\mathrm{isContr}(A)$ representing whether $A$ is a [[contractible type]] to be 
$$\sum_{a:A} \prod_{b:A} a =_A b$$
$\mathrm{isContr}(A)$ is given by the following rules:

Formation rules for $\mathrm{isContr}(A)$:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{isContr}(A) \; \mathrm{type}}$$

Introduction rules for $\mathrm{isContr}(A)$:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:\sum_{a:A} \prod_{b:A} a =_A b}{\Gamma \vdash \mathrm{copy}(a):\mathrm{isContr}(A)}$$

Elimination rules for $\mathrm{isContr}(A)$:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, z:\mathrm{isContr}(A) \vdash C \; \mathrm{type} \quad \Gamma, x:\sum_{a:A} \prod_{b:A} a =_A b \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:\mathrm{isContr}(A)}{\Gamma \vdash \mathrm{ind}_{\mathrm{isContr}(A)}^C(c, e):C[e/z]}$$

Computation rules for $\mathrm{isContr}(A)$:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, z:\mathrm{isContr}(A) \vdash C \; \mathrm{type} \quad \Gamma, x:\sum_{a:A} \prod_{b:A} a =_A b \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash a:\sum_{a:A} \prod_{b:A} a =_A b}{\Gamma \vdash \beta_{\mathrm{isContr}(A)}:\mathrm{ind}_{\mathrm{isContr}(A)}^C(c, \mathrm{copy}(a)) =_{C[\mathrm{copy}(a)/z]} c[a/x]}$$

Uniqueness rules for $\mathrm{isContr}(A)$:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, z:\mathrm{isContr}(A) \vdash C \; \mathrm{type} \quad \Gamma, x:\sum_{a:A} \prod_{b:A} a =_A b \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:\mathrm{isContr}(A) \quad \Gamma, y:\mathrm{isContr}(A) \vdash u:C \quad \Gamma, a:\sum_{a:A} \prod_{b:A} a =_A b \vdash i_\mathrm{copy}(u):u[\mathrm{copy}(a)/y] =_{C[\mathrm{copy}(a)/y]} c[a/x]}{\Gamma \vdash \eta_{\mathrm{isContr}(A)}:u[e/z] =_{C[e/z]} \mathrm{ind}_{\mathrm{isContr}(A)}^C(c, e)}$$

### Fiber types

In set theory, the [[fiber]] of a function $f$ with [[domain]] $A$ and [[codomain]] $B$ at an element $b$ in $B$ is the indexed [[disjoint union]] of all elements $a:A$ such that $f(a) = b$. This definition could also be translated into objective type theory: the fiber of a function $f:A \to B$ at the element $b:B$ is the type 
$$\sum_{a:A} f(a) =_B b$$
The elements $p:\sum_{a:A} f(a) =_B b$ are the fibers of the function $f:A \to B$ at element $y:B$. We write $\mathrm{fiber}_{A, B}(f, y)$ for $\sum_{a:A} f(a) =_B b$, which is given by the following rules:

Formation rules for fiber types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash b:B}{\Gamma \vdash \mathrm{fiber}_{A, B}(f, b) \; \mathrm{type}}$$

Introduction rules for fiber types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash b:B \quad \Gamma \vdash a:\sum_{x:A} f(x) =_B b}{\Gamma \vdash \mathrm{copy}(f, b, a):\mathrm{fiber}_{A, B}(f, b)}$$

Elimination rules for fiber types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash b:B \quad \Gamma, z:\mathrm{fiber}_{A, B}(f, b) \vdash C \; \mathrm{type} \quad \Gamma, x:\sum_{a:A} f(a) =_B b \vdash c:C[\mathrm{copy}(f, b, x)/z] \quad \Gamma \vdash e:\mathrm{fiber}_{A, B}(f, b)}{\Gamma \vdash \mathrm{ind}_{\mathrm{fiber}_{A, B}(f, b)}^C(c, e):C[e/z]}$$

Computation rules for fiber types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash b:B \quad \Gamma, z:\mathrm{fiber}_{A, B}(f, b) \vdash C \; \mathrm{type} \quad \Gamma, x:\sum_{a:A} f(a) =_B b \vdash c:C[\mathrm{copy}(f, b, x)/z] \quad \Gamma \vdash a:\sum_{a:A} f(a) =_B b}{\Gamma \vdash \beta_{\mathrm{fiber}_{A, B}(f, y)}:\mathrm{ind}_{\mathrm{fiber}_{A, B}(f, b)}^C(c, \mathrm{copy}(f, b, a)) =_{C[\mathrm{copy}(f, b, a)/z]} c[a/x]}$$

Uniqueness rules for fiber types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash b:B \quad \Gamma, z:\mathrm{fiber}_{A, B}(f, b) \vdash C \; \mathrm{type} \quad \Gamma, x:\sum_{a:A} f(a) =_B b \vdash c:C[\mathrm{copy}(f, b, x)/z] \quad \Gamma \vdash e:\mathrm{fiber}_{A, B}(f, b) \quad \Gamma, y:\mathrm{fiber}_{A, B}(f, b) \vdash u:C \quad \Gamma, a:\sum_{a:A} f(a) =_B b \vdash i_{\mathrm{copy}(f, b)}(u):u[\mathrm{copy}(a)/y] =_{C[\mathrm{copy}(f, b, a)/y]} c[a/x]}{\Gamma \vdash \eta_{\mathrm{fiber}_{A, B}(f, b)}:u[e/z] =_{C[e/z]} \mathrm{ind}_{\mathrm{fiber}_{A, B}(f, b)}^C(c, e)}$$

### isEquiv types

In set theory, a function is a [[bijection]] if all its fibers at every element of the codomain are singletons. This definition can be translated over to objective type theory, as the type 
$$\prod_{b:B} \mathrm{isContr}(\mathrm{fiber}_{A, B}(f, b)$$
but the name used for such a function in objective type theory is [[equivalence in homotopy type theory|equivalence]], rather than bijection. The above type is written as $\mathrm{isEquiv}(f)$, and is given by the following rules:

Formation rules for isEquiv types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B}{\Gamma \vdash \mathrm{isEquiv}(f) \; \mathrm{type}}$$

Introduction rules for isEquiv types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash \prod_{b:B} \mathrm{isContr}(\mathrm{fiber}_{A, B}(f, b) \; \mathrm{type} \quad \Gamma \vdash a:\prod_{b:B} \mathrm{isContr}(\mathrm{fiber}_{A, B}(f, b))}{\Gamma \vdash \mathrm{copy}(a):\mathrm{isEquiv}(f)}$$

Elimination rules for isEquiv types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma, z:\mathrm{isEquiv}(f) \vdash C \; \mathrm{type} \quad \Gamma, x:\prod_{b:B} \mathrm{isContr}(\mathrm{fiber}_{A, B}(f, b)) \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:\mathrm{isEquiv}(f)}{\Gamma \vdash \mathrm{ind}_{\mathrm{isEquiv}(f)}^C(c, e):C[e/z]}$$

Computation rules for isEquiv types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma, z:\mathrm{isEquiv}(f) \vdash C \; \mathrm{type} \quad \Gamma, x:\prod_{b:B} \mathrm{isContr}(\mathrm{fiber}_{A, B}(f, b)) \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash a:\prod_{b:B} \mathrm{isContr}(\mathrm{fiber}_{A, B}(f, b))}{\Gamma \vdash \beta_{\mathrm{isEquiv}(f)}:\mathrm{ind}_{\mathrm{isEquiv}(f)}^C(c, \mathrm{copy}(a)) =_{C[\mathrm{copy}(a)/z]} c[a/x]}$$

Uniqueness rules for isEquiv types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma, z:\mathrm{isEquiv}(f) \vdash C \; \mathrm{type} \quad \Gamma, x:\prod_{b:B} \mathrm{isContr}(\mathrm{fiber}_{A, B}(f, b)) \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:\mathrm{isEquiv}(f) \quad \Gamma, y:\mathrm{isEquiv}(f) \vdash u:C \quad \Gamma, a:\prod_{b:B} \mathrm{isContr}(\mathrm{fiber}_{A, B}(f, b)) \vdash i_\mathrm{copy}(u):u[\mathrm{copy}(a)/y] =_{C[\mathrm{copy}(a)/y]} c[a/x]}{\Gamma \vdash \eta_{\mathrm{isEquiv}(f)}:u[e/z] =_{C[e/z]} \mathrm{ind}_{\mathrm{isEquiv}(f)}^C(c, e)}$$

### Equivalence types

The type of equivalences is given by the type
$$\sum_{f:A \to B} \mathrm{isEquiv}(f)$$
The above type is written as $A \simeq B$, and is given by the following rules:

Formation rules for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \simeq B \; \mathrm{type}}$$

Introduction rules for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash a:\sum_{f:A \to B} \mathrm{isEquiv}(f)}{\Gamma \vdash \mathrm{copy}(a):A \simeq B}$$

Elimination rules for equivalence types:
$$\frac{\Gamma, z:A \simeq B \vdash C \; \mathrm{type} \quad \Gamma, x:\sum_{f:A \to B} \mathrm{isEquiv}(f) \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{ind}_{A \simeq B}^C(c, e):C[e/z]}$$

Computation rules for equivalence types:
$$\frac{\Gamma, z:\sum_{f:A \to B} \mathrm{isEquiv}(f) \simeq B \vdash C \; \mathrm{type} \quad \Gamma, x:\sum_{f:A \to B} \mathrm{isEquiv}(f) \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_{A \simeq B}:\mathrm{ind}_{A \simeq B}^C(c, \mathrm{copy}(a)) =_{C[\mathrm{copy}(a)/z]} c[a/x]}$$

Uniqueness rules for equivalence types:
$$\frac{\Gamma, z:A \simeq B \vdash C \; \mathrm{type} \quad \Gamma, x:\sum_{f:A \to B} \mathrm{isEquiv}(f) \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:A \simeq B \quad \Gamma, y:A \simeq B \vdash u:C \quad \Gamma, a:\sum_{f:A \to B} \mathrm{isEquiv}(f) \vdash i_\mathrm{copy}(u):u[\mathrm{copy}(a)/y] =_{C[\mathrm{copy}(a)/y]} c[a/x]}{\Gamma \vdash \eta_{A \simeq B}:u[e/z] =_{C[e/z]} \mathrm{ind}_{A \simeq B}^C(c, e)}$$

### Definitions of types II

There is an alternate way of defining types which uses equivalence of types. 

Parts of the following section is adapted from [[Egbert Rijke]]'s [[Introduction to Homotopy Type Theory]]:

We can make definitions at the end of a derivation if the conclusion is a certain type in context, where we have a derivation 
$$\frac{\mathcal{D}}{\Gamma \vdash A \; \mathrm{type}}$$
if we wish to make a definition $B \coloneqq A$, then we can similarly extend the derivation tree with 
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash B \coloneqq A \; \mathrm{type}}$$
The effect of such a definition in this case is that we have extended our type theory with a new constant $B$, for which the following inference rules are valid 
$$\frac{\mathcal{D}}{B \; \mathrm{type}} \qquad \frac{\mathcal{D}}{\mathrm{defequiv}(B, A): B \simeq A}$$

In essence, we define an element $b$ to be equal to $a$, and a type $B$ to be equivalent to $A$, in the same way that in [[structural set theory]], which usually also doesn't have [[judgmental equality]], one would define element $b$ to be equal to $a$ and set $B$ to be in [[bijection]] with $A$. 

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

See also [[open problems in homotopy type theory]]

## See also

* [[judgmental equality]], [[identity type]]

* [[dependent type theory]], [[Martin-Löf type theory]], [[homotopy type theory]]

## References

* [[Benno van den Berg]], [[Martijn den Besten]], *Quadratic type checking for objective type theory* ([arXiv:2102.00905](https://arxiv.org/abs/2102.00905))

* *Homotopy Type Theory: Univalent Foundations of Mathematics*,
The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([pdf](https://raw.githubusercontent.com/martinescardo/HoTTEST-Summer-School/main/HoTT/hott-intro.pdf)) (478 pages)

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]], *[[Symmetry]]* (2021) $[$[pdf](https://unimath.github.io/SymmetryBook/book.pdf)$]$ 

[[!redirects objective type theory]]
[[!redirects objective type theories]]