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
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A, p:x =_A x, \vdash K(x, p):p =_{x =_A x} refl_A(x)}$$

The uniqueness rule for identity types is usually not included in objective type theory. However, if it were included in objective type theory it turns the type theory into a [[set-level type theory]]. 

### Structural rules for definitions

Now that we have finally defined identity types, we can define the structural rules for term definitions. The structural rules for term definitions say that given a term $a:A$ and a term definition $b \coloneqq a:A$, one could derive that $b$ is a term of $A$, and that there is an identification between $b$ and $a$:

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash a:A \quad \Gamma \vdash b \coloneqq a:A}{\Gamma \vdash \delta_A(a, b):b =_A a}$$

The structural rules for type definitions are the natural deduction rules for [[copying]] types, with formation and introduction rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{copy}(a):B}$$

elimination rules:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type} \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:B}{\Gamma \vdash \mathrm{ind}_{B}^C(c, e):C[e/z]}$$

computation rules:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type} \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_B:\mathrm{ind}_{B}^C(c, \mathrm{copy}(a)) =_{C[\mathrm{copy}(a)/z]} c[a/x]}$$

and uniqueness rules:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type} \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:B \quad \Gamma, y:B \vdash u:C \quad \Gamma, a:A \vdash i_\mathrm{copy}(u):u[\mathrm{copy}(a)/y] =_{C[\mathrm{copy}(a)/y]} c[a/x]}{\Gamma \vdash \eta_{B}:u[e/z] =_{C[e/z]} \mathrm{ind}_{B}^C(c, e)}$$

### Dependent identity types

The rules for dependent identity types are as follows:

Formation rule for dependent identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, y:B(a), z:B(b) \vdash y =_B^{p} z \; \mathrm{type}}$$ 

Introduction rule for dependent identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, w:B(x) \vdash \mathrm{apd}_B^{p}(w):w(a) =_B^{p} w(b)}$$ 

Elimination rule for dependent identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, y:B(a), z:B(b), q:y =_B^p z \vdash C(y, z, q) \; \mathrm{type} \quad \Gamma, x:A, w:B(x) \vdash t:C(w(a), w(b), \mathrm{apd}_B^{p}(w))}{\Gamma, y:B(a), z:B(b), q:y =_B^p z \vdash J_B^p(t, y, z, q):C(y, z, q)}$$

Computation rules for dependent identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, y:B(a), z:B(b), q:y =_B^p z \vdash C(y, z, q) \; \mathrm{type} \quad \Gamma, x:A, w:B(x) \vdash t:C(w(a), w(b), \mathrm{apd}_B^{p}(w))}{\Gamma, x:A, w:B(x) \vdash \beta_{=_B^p}(w):J(t, w(a), w(b), \mathrm{apd}_B^{p}(w)) =_{C(w(a), w(b), \mathrm{apd}_B^{p}(w))} t}$$

Optional uniqueness rules for dependent identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, w:B(x), q:w(a) =_B^{p} w(b) \vdash K_B^p(x, w, q):q =_{w(a) =_B^{p} w(b)} \mathrm{apd}_B^{p}(w)}$$

### isEquiv types and equivalences

The rules for isEquiv types are as follows:

Formation rules for isEquiv:
$$\frac{\Gamma A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B}{\Gamma \vdash \mathrm{isEquiv}(f) \; \mathrm{type}}$$

Introduction rules for isEquiv:
$$\frac{\Gamma A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B \quad \Gamma \vdash a:A \quad \Gamma, y:B \vdash b(y):f(a) =_B y \quad \Gamma, x:A, y:B, z:f(x) =_B y \vdash \tau_A(x, y, z):a =_A x \quad \Gamma, x:A, y:B, z:f(x) =_B y \vdash \tau_B(x, y, z):b(y) =_B^{\tau_A(x, y, z)} z}{\Gamma \vdash w(a, b, \tau_A, \tau_B):\mathrm{isEquiv}(f)}$$

Elimination rules for isEquiv:
$$\frac{\Gamma A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B \quad \Gamma \vdash p:\mathrm{isEquiv}(f) \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[f(x)/z] \quad \Gamma \vdash e:B}{\Gamma \vdash \mathrm{ind}_{\mathrm{isEquiv}(f)}^C(c, e):C[e/z]}$$

Computation rules for isEquiv:
$$\frac{\Gamma A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B \quad \Gamma \vdash p:\mathrm{isEquiv}(f) \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[f(x)/z] \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_B:\mathrm{ind}_{\mathrm{isEquiv}(f)}^C(c, f(a)) =_{C[f(a)/z]} c[a/x]}$$

Uniqueness rules for isEquiv:
$$\frac{\Gamma A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B \quad \Gamma \vdash p:\mathrm{isEquiv}(f) \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[f(x)/z] \quad \Gamma \vdash e:\mathrm{isEquiv}(f) \quad \Gamma, y:B \vdash u:C \quad \Gamma, a:A \vdash i_f(u):u[f(a)/y] =_{C[f(a)/y]} c[a/x]}{\Gamma \vdash \eta_{\mathrm{isEquiv}(f)}:u[e/z] =_{C[e/z]} \mathrm{ind}_{\mathrm{isEquiv}(f)}^C(c, e)}$$

A family of elements $x:A \vdash f(x):B$ is an equivalence if it comes with a family of elements
$$y:B \vdash \epsilon(f)(y):\mathrm{isEquiv}(f)$$

### Judgmentally univalent universes

Universes are internal models of [[dependent type theory]] inside of the type theory itself. An universe consists of a type of encodings for types $\mathcal{U}$ and a universal type family $\mathcal{T}$ which takes the encodings and returns an actual type, resulting in the formation and type reflection rules for universes:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathcal{U} \; \mathrm{type}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma, A:\mathcal{U} \vdash \mathcal{T}(A) \; \mathrm{type}}$$

Given an encoding $A:\mathcal{U}$, an internal type family indexed by $A$ is a function $B:\mathcal{T}(A) \to \mathcal{U}$. 

A universe is judgmentally univalent if identities $f:A =_\mathcal{U} B$ and equivalences $x:\mathcal{T}(A) \vdash f(x):\mathcal{T}(B)$ are interderivable in the type theory. This is given by the following rules:

Introduction rules:
$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma, x:T[A/X] \vdash f:T[B/X] \quad \Gamma \vdash y:\mathrm{isEquiv}(f)}{\Gamma \vdash \mathrm{equiv}(f, y):A =_U B}$$

Elimination rules:
$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma, x:T[A/X] \vdash f:T[B/X] \quad \Gamma, z:A =_U B \vdash C \; \mathrm{type} \quad \Gamma, x:T[A/X], f:T[B/X], y:\mathrm{isEquiv}(f) \vdash c:C[\mathrm{equiv}(f, y)/z]}{\Gamma, z:A =_U B \vdash \mathrm{ind}_{A =_U B}^C(c):C}$$

Computation rules:
$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma, x:T[A/X] \vdash f:T[B/X] \quad \Gamma, z:A =_U B \vdash C \; \mathrm{type} \quad \Gamma, x:T[A/X], f:T[B/X], y:\mathrm{isEquiv}(f) \vdash c:C[\mathrm{equiv}(f, y)/z]}{\Gamma, x:T[A/X], f:T[B/X], y:\mathrm{isEquiv}(f) \vdash \beta_{A =_U B}^C(c):\mathrm{ind}_{A =_U B}^C(c)[\mathrm{equiv}(f, y)/z] =_{C[\mathrm{equiv}(f, y)/z]} c}$$

Uniqueness rules:
$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma, x:T[A/X] \vdash f:T[B/X] \quad \Gamma, z:A =_U B \vdash C \; \mathrm{type} \quad \Gamma, x:T[A/X], f:T[B/X], y:\mathrm{isEquiv}(f) \vdash c:C[\mathrm{equiv}(f, y)/z] \quad \Gamma, z:A =_U B \vdash u:C \quad \Gamma, x:T[A/X], f:T[B/X], y:\mathrm{isEquiv}(f) \vdash i_\mathrm{in}(u):u[\mathrm{equiv}(f, y)/z] =_{C[\mathrm{in}(x, y)/z]} c}{\Gamma, e:A =_U B \vdash \eta_{A =_U B}^C(c):u[e/z] =_{C[e/z]} \mathrm{ind}_{A =_U B}^C(c)[e/z]}$$

### Internal identity types

A universe $\mathcal{U}$ is closed under identity types if for each element $A:\mathcal{U}$, $a:\mathcal{T}(A)$, and $b:\mathcal{T}(A)$, there is an element $\mathrm{Id}^\mathcal{U}(A, a, b):\mathcal{U}$ which behaves as the internal encoding of the identity type $a =_A b$ in the universe


Formation rule for identity types:
$$\frac{\Gamma \vdash A:\mathcal{U}}{\Gamma, a:\mathcal{T}(A), b:\mathcal{T}(A) \vdash \mathrm{Id}^\mathcal{U}(A, a, b):\mathcal{U}}$$

Introduction rule for identity types:
$$\frac{\Gamma \vdash A:\mathcal{U}}{\Gamma, a:\mathcal{T}(A) \vdash \mathrm{refl}_A^\mathcal{U}(a) : \mathcal{T}(\mathrm{Id}^\mathcal{U}(A, a, a))}$$

Elimination rule for identity types:
$$\frac{\Gamma, x:\mathcal{T}(A), y:\mathcal{T}(A), p:\mathcal{T}(\mathrm{Id}^\mathcal{U}(A, x, y)) \vdash C:\mathcal{U} \quad \Gamma, a:\mathcal{T}(A) \vdash t:\mathcal{T}(C[a, a, \mathrm{refl}_A^\mathcal{U}(a)/x, y, p])}{\Gamma, x:\mathcal{T}(A), y:\mathcal{T}(A), p:\mathcal{T}(\mathrm{Id}^\mathcal{U}(A, x, y)) \vdash J(t, x, y, p):\mathcal{T}(C)}$$

Computation rules for identity types:
$$\frac{\Gamma, x:\mathcal{T}(A), y:\mathcal{T}(A), p:\mathcal{T}(\mathrm{Id}^\mathcal{U}(A, x, y)) \vdash C:\mathcal{U} \quad \Gamma, a:\mathcal{T}(A) \vdash t:\mathcal{T}(C[a, a, \mathrm{refl}_A^\mathcal{U}(a)/x, y, p])}{\Gamma, a:\mathcal{T}(A) \vdash \beta_{\mathrm{Id}^\mathcal{U}(A)}(a) : J(t, a, a, \mathrm{refl}_A^\mathcal{U}(a)) =_{\mathcal{T}(C[a, a, \mathrm{refl}_A^\mathcal{U}(a)/x, y, p])} t}$$

Optional uniqueness rules for identity types:
$$\frac{\Gamma \vdash A:\mathcal{U}}{\Gamma, x:\mathcal{T}(A), p:\mathcal{T}(\mathrm{Id}^\mathcal{U}(A, x, x)), \vdash \eta_{\mathrm{Id}^\mathcal{U}(A)}(x, p):p =_{\mathcal{T}(\mathrm{Id}^\mathcal{U}(A, x, x))} \mathrm{refl}_A^\mathcal{U}(x)}$$

### Function types

Formation rules for function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \to B \; \mathrm{type}}$$

Introduction rules for function types:
$$\frac{\Gamma, x:A \vdash b(x):B}{\Gamma \vdash (x \mapsto b(x)):A \to B}$$

Elimination rules for function types:
$$\frac{\Gamma \vdash f:A \to B \quad \Gamma \vdash a:A}{\Gamma \vdash f(a):B}$$

Computation rules for function types:
$$\frac{\Gamma, x:A \vdash b(x):B \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_{A \to B}:(x \mapsto b(x))(a) =_{B} b}$$

Uniqueness rules for function types:
$$\frac{\Gamma \vdash f:A \to B}{\Gamma \vdash \eta_{A \to B}:f =_{A \to B} (x \to f(x))}$$

A universe $\mathcal{U}$ is closed under function types if for each element $A:\mathcal{U}$ and $B:\mathcal{U}$ there is an element $A \to_\mathcal{U} B:\mathcal{U}$ which behaves as the internal encoding of the function type $A \to B$ in the universe

Formation rules for internal function types:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, A:\mathcal{U}, B:\mathcal{U} \vdash A \to_\mathcal{U} B:\mathcal{U}}$$

Introduction rules for internal function types:
$$\frac{\Gamma, x:\mathcal{T}(A) \vdash b(x):\mathcal{T}(B)}{\Gamma \vdash (x \mapsto b(x)):\mathcal{T}(A \to_\mathcal{U} B)}$$

Elimination rules for internal function types:
$$\frac{\Gamma \vdash f:\mathcal{T}(A \to_\mathcal{U} B) \quad \Gamma \vdash a:\mathcal{T}(A)}{\Gamma \vdash f(a):\mathcal{T}(B)}$$

Computation rules for internal function types:
$$\frac{\Gamma, x:\mathcal{T}(A) \vdash b(x):\mathcal{T}(B) \quad \Gamma \vdash a:\mathcal{T}(A)}{\Gamma \vdash \beta_{A \to_\mathcal{U} B}:(x \mapsto b(x))(a) =_{\mathcal{T}(B)} b}$$

Uniqueness rules for internal function types:
$$\frac{\Gamma \vdash f:\mathcal{T}(A \to_\mathcal{U} B)}{\Gamma \vdash \eta_{A \to_\mathcal{U} B}:f =_{\mathcal{T}(A \to_\mathcal{U} B)} (x \to f(x))}$$

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

A universe $\mathcal{U}$ is closed under pi types if for each element $A:\mathcal{U}$ and family of elements $x:A \vdash B(x):\mathcal{U}$ there is an element $\Pi_\mathcal{U}(x:A).B(x):\mathcal{U}$ which behaves as the internal encoding of the pi type $\prod_{x:A} B(x)$ in the universe

Formation rules for internal Pi types:
$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma, x:\mathcal{T}(A) \vdash B(x):\mathcal{U}}{\Gamma \vdash \Pi_\mathcal{U}(x:A).B(x):\mathcal{U}}$$

Introduction rules for internal Pi types:
$$\frac{\Gamma, x:\mathcal{T}(A) \vdash b(x):\mathcal{T}(B(x))}{\Gamma \vdash \lambda(x:A).b(x):\mathcal{T}(\Pi_\mathcal{U}(x:A).B(x))}$$

Elimination rules for internal Pi types:
$$\frac{\Gamma \vdash f:\mathcal{T}(\Pi_\mathcal{U}(x:A).B(x)) \quad \Gamma \vdash a:\mathcal{T}(A)}{\Gamma \vdash f(a):\mathcal{T}(B[a/x])}$$

Computation rules for internal Pi types:
$$\frac{\Gamma, x:\mathcal{T}(A) \vdash b(x):\mathcal{T}(B(x)) \quad \Gamma \vdash a:\mathcal{T}(A)}{\Gamma \vdash \beta_{\Pi_\mathcal{U}(x:A).B(x)}:\lambda(x:A).b(x)(a) =_{\mathcal{T}(B[a/x])} b[a/x]}$$

Uniqueness rules for internal Pi types:
$$\frac{\Gamma \vdash f:\mathcal{T}(\Pi_\mathcal{U}(x:A).B(x))}{\Gamma \vdash \eta_{\Pi_\mathcal{U}(x:A).B(x)}:f =_{\mathcal{T}(\Pi_\mathcal{U}(x:A).B(x))} \lambda(x).f(x)}$$

### Product types

We use the positive presentation for product types. 

Formation rules for product types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \times B \; \mathrm{type}}$$

Introduction rules for product types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma\vdash B \; \mathrm{type}}{\Gamma, x:A, y:B \vdash \mathrm{in}(x, y):A \times B}$$

Elimination rules for product types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, z:A \times B \vdash C(z) \; \mathrm{type} \quad \Gamma \vdash c:\prod_{x:A} \prod_{y:B} C(\mathrm{in}(x, y))}{\Gamma, z:A \times B \vdash \mathrm{ind}_{A \times B}^C(c, z):C(z)}$$

Computation rules for product types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, z:A \times B \vdash C(z) \; \mathrm{type} \quad \Gamma \vdash c:\prod_{x:A} \prod_{y:B} C(\mathrm{in}(x, y))}{\Gamma, x:A, y:B \vdash \beta_{A \times B}^C(c, \mathrm{in}(x, y)):\mathrm{ind}_{A \times B}^C(c, \mathrm{in}(x, y) =_{C(\mathrm{in}(x, y))} c(\mathrm{in}(x, y))}$$

Uniqueness rules for product types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma\vdash B \; \mathrm{type} \quad \Gamma, z:A \times B \vdash C \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash c:C[(x, y)/z] \quad \Gamma, z:A \times B \vdash u:C \quad \Gamma, x:A, y:B \vdash i_{(-,-)}(u):u[(x, y)/z] =_{C[(x, y)/z]} c}{\Gamma, z:A \times B \vdash \eta_{A \times B}^C(c):u =_{C} \mathrm{ind}_{A \times B}^C(c)}$$

A universe $\mathcal{U}$ is closed under product types if it for each element $A:\mathcal{U}$ and $B:\mathcal{U}$, there is an element $A \times_\mathcal{U} B:\mathcal{U}$ which behaves as the internal encoding of the product type $A \times B$ in the universe

Formation rules for internal product types:
$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash B:\mathcal{U}}{\Gamma \vdash A \times_\mathcal{U} B:\mathcal{U}}$$

Introduction rules for internal product types:
$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash B:\mathcal{U}}{\Gamma, x:\mathcal{T}(A), y:\mathcal{T}(B) \vdash (x, y):\mathcal{T}(A \times_\mathcal{U} B)}$$

Elimination rules for internal product types:
$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash B:\mathcal{U} \quad \Gamma, z:\mathcal{T}(A \times_\mathcal{U} B) \vdash C:\mathcal{U} \quad \Gamma, x:\mathcal{T}(A), y:\mathcal{T}(B) \vdash c:\mathcal{T}(C[(x, y)/z)]}{\Gamma, z:\mathcal{T}(A \times_\mathcal{U} B) \vdash \mathrm{ind}_{A \times_\mathcal{U} B}^C(c):\mathcal{T}(C)}$$

Computation rules for internal product types:
$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash B:\mathcal{U} \quad \Gamma, z:\mathcal{T}(A \times_\mathcal{U} B) \vdash C:\mathcal{U} \quad \Gamma, x:\mathcal{T}(A), y:\mathcal{T}(B) \vdash c:\mathcal{T}(C[(x, y)/z])}{\Gamma, x:\mathcal{T}(A), y:\mathcal{T}(B) \vdash \beta_{A \times_\mathcal{U} B}^C(c):\mathrm{ind}_{A \times_\mathcal{U} B}^C(c)[(x, y)/z] =_{\mathcal{T}(C[(x, y)/z])} c}$$

Uniqueness rules for internal product types:
$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash B:\mathcal{U} \quad \Gamma, z:\mathcal{T}(A \times_\mathcal{U} B) \vdash C:\mathcal{U} \quad \Gamma, x:\mathcal{T}(A), y:\mathcal{T}(B) \vdash c:\mathcal{T}(C[(x, y)/z]) \quad \Gamma, z:\mathcal{T}(A \times_\mathcal{U} B) \vdash u:\mathcal{T}(C) \quad \Gamma, x:\mathcal{T}(A), y:\mathcal{T}(B) \vdash i_{(-,-)}(u):u[(x, y)/z] =_{\mathcal{T}(C[(x, y)/z])} c}{\Gamma, z:\mathcal{T}(A \times_\mathcal{U} B) \vdash \eta_{A \times_\mathcal{U} B}^C(c):u =_{\mathcal{T}(C)} \mathrm{ind}_{A \times_\mathcal{U} B}^C(c)}$$

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

A universe $\mathcal{U}$ is closed under sigma types if for each element $A:\mathcal{U}$ and family of elements $x:A \vdash B(x):\mathcal{U}$ there is an element $\Sigma_\mathcal{U}(x:A).B(x):\mathcal{U}$ which behaves as the internal encoding of the sigma type $\Sigma(x:A).B(x)$ in the universe

Formation rules for internal sigma types:
$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma, x:\mathcal{T}(A) \vdash B:\mathcal{U}}{\Gamma \vdash \Sigma_\mathcal{U} (x:A).B(x):\mathcal{U}}$$

Introduction rules for internal sigma types:
$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma, x:\mathcal{T}(A) \vdash B:\mathcal{U}}{\Gamma, x:A, y:B \vdash \mathrm{in}(x, y):\mathcal{T}(\Sigma_\mathcal{U} (x:A).B(x))}$$

Elimination rules for internal sigma types:
$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma, x:\mathcal{T}(A) \vdash B:\mathcal{U} \quad \Gamma, z:\mathcal{T}(\Sigma (x:A).B(x)) \vdash C:\mathcal{U} \quad \Gamma, x:\mathcal{T}(A), y:\mathcal{T}(B(x)) \vdash c:\mathcal{T}(C[\mathrm{in}(x, y)/z])}{\Gamma, z:\mathcal{T}(\Sigma_\mathcal{U} (x:A).B(x)) \vdash \mathrm{ind}_{\Sigma_\mathcal{U} (x:A).B(x)}^C(c):\mathcal{T}(C)}$$

Computation rules for internal sigma types:
$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma, x:A \vdash B:\mathcal{U} \quad \Gamma, z:\mathcal{T}(\Sigma_\mathcal{U} (x:A).B(x)) \vdash C:\mathcal{U} \quad \Gamma, x:\mathcal{T}(A), y:\mathcal{T}(B(x)) \vdash c:\mathcal{T}(C[\mathrm{in}(x, y)/z])}{\Gamma, x:\mathcal{T}(A), y:\mathcal{T}(B(x)) \vdash \beta_{\Sigma_\mathcal{U} (x:A).B(x)}^C(c):\mathrm{ind}_{\Sigma_\mathcal{U} (x:A).B(x)}^C(c)[\mathrm{in}(x, y)/z] =_{\mathcal{T}(C[\mathrm{in}(x, y)/z])} c}$$

Uniqueness rules for internal sigma types:
$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma, x:\mathcal{T}(A) \vdash B:\mathcal{U} \quad \Gamma, z:\mathcal{T}(\Sigma_\mathcal{U} (x:A).B(x)) \vdash C:\mathcal{U} \quad \Gamma, x:\mathcal{T}(A), y:\mathcal{T}(B(x)) \vdash c:\mathcal{T}(C[\mathrm{in}(x, y)/z]) \quad \Gamma, z:\mathcal{T}(\Sigma_\mathcal{U} (x:A).B(x)) \vdash u:\mathcal{T}(C) \quad \Gamma, x:\mathcal{T}(A), y:\mathcal{T}(B(x)) \vdash i_\mathrm{in}(u):u[\mathrm{in}(x, y)/z] =_{\mathcal{T}(C[\mathrm{in}(x, y)/z])} c}{\Gamma, e:\mathcal{T}(\Sigma_\mathcal{U} (x:A).B(x)) \vdash \eta_{\Sigma_\mathcal{U} (x:A).B(x)}^C(c):u[e/z] =_{\mathcal{T}(C[e/z])} \mathrm{ind}_{\Sigma_\mathcal{U} (x:A).B(x)}^C(c)[e/z]}$$

### Empty type

Formation rules for the empty type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{0} \; \mathrm{type}}$$

Elimination rules for the empty type:
$$\frac{\Gamma, x:\mathbb{0} \vdash C \; \mathrm{type}}{\Gamma, x:\mathbb{0} \vdash \mathrm{ind}_\mathbb{0}^C:C}$$

Uniqueness rules for the empty type:
$$\frac{\Gamma, x:\mathbb{0} \vdash C \; \mathrm{type} \quad \Gamma, x:\mathbb{0} \vdash c:C}{\Gamma, x:\mathbb{0} \vdash \eta_\mathbb{0}(c):c =_{C} \mathrm{ind}_\mathbb{0}^{C}}$$

A universe $\mathcal{U}$ is closed under the empty type if it has an element which behaves as an internal encoding of the empty type in the universe: 

Formation rules for the internal empty type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{0}_\mathcal{U}:\mathcal{U}}$$

Elimination rules for the internal empty type:
$$\frac{\Gamma, x:\mathcal{T}(\mathbb{0}_\mathcal{U}) \vdash C:\mathcal{U}}{\Gamma, x:\mathcal{T}(\mathbb{0}_\mathcal{U}) \vdash \mathrm{ind}_{\mathbb{0}_\mathcal{U}}^C:\mathcal{T}(C)}$$

Uniqueness rules for the internal empty type:
$$\frac{\Gamma, x:\mathcal{T}(\mathbb{0}_\mathcal{U}) \vdash C:\mathcal{U} \quad \Gamma, x:\mathcal{T}(\mathbb{0}_\mathcal{U}) \vdash c:\mathcal{T}(C)}{\Gamma, x:\mathcal{T}(\mathbb{0}_\mathcal{U}) \vdash \eta_{\mathbb{0}_\mathcal{U}}(c):c =_{\mathcal{T}(C)} \mathrm{ind}_{\mathbb{0}_\mathcal{U}}^{C}}$$

### Other types

#### Unit type

Formation rules for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{1} \; \mathrm{type}}$$

Introduction rules for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{pt}:\mathbb{1}}$$

[[singleton induction]]:
$$\frac{\Gamma, x:\mathbb{1} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{pt}:C(\mathrm{pt})}{\Gamma \vdash \mathrm{up}_\mathbb{1}^C(c_\mathrm{pt}):\mathrm{isContr}\left(\sum_{c:\prod_{x:\mathbb{1}} C(x)} (c(\mathrm{pt}) =_{C(\mathrm{pt})} c_\mathrm{pt})\right)}$$

#### Copy types

Formation rules for copy types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{Copy}(A) \; \mathrm{type}}$$

Introduction rules for sum types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{copy}_A:A \to \mathrm{Copy}(A)}$$

Dependent universal property rule for sum types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:\mathrm{Copy}(A) \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_{\mathrm{copy}_A}:\prod_{x:A} C(\mathrm{copy}_A(x))}{\Gamma \vdash \mathrm{up}_{\mathrm{Copy}(A)}^C(c_{\mathrm{copy}_A}):\mathrm{isContr}\left(\sum_{c:\prod_{x:\mathrm{Copy}(A)} C(x)} \prod_{a:A} c(\mathrm{copy}_A(a)) =_{C(\mathrm{copy}_A(a))} c_{\mathrm{copy}_A}(a)\right)}$$

#### Booleans type

Formation rules for the booleans type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{2} \; \mathrm{type}}$$

Introduction rules for the booleans type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{2}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 1:\mathbb{2}}$$

Dependent universal property rule for the booleans type:
$$\frac{\Gamma, x:\mathbb{2} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_1:C(1)}{\Gamma \vdash \mathrm{up}_\mathbb{2}^C(c_0, c_1):\mathrm{isContr}\left(\sum_{c:\prod_{x:\mathbb{2}} C(x)} (c(0) =_{C(0)} c_0) \times (c(1) =_{C(1)} c_1)\right)}$$

#### Sum types

Formation rules for sum types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A + B \; \mathrm{type}}$$

Introduction rules for sum types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{in}_A:A \to A + B} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{in}_B:B \to A + B}$$

Dependent universal property rule for sum types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A + B \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_{\mathrm{in}_A}:\prod_{x:A} C(\mathrm{in}_A(x)) \quad \Gamma \vdash c_{\mathrm{in}_B}:\prod_{y:B} C(\mathrm{in}_B(y))}{\Gamma \vdash \mathrm{up}_{A + B}^C(c_{\mathrm{in}_A}, c_{\mathrm{in}_B}):\mathrm{isContr}\left(\sum_{c:\prod_{x:A + B} C(x)} \left(\prod_{a:A} (c(\mathrm{in}_A(a)) =_{C(\mathrm{in}_A(a))} c_{\mathrm{in}_A}(a))\right) \times \left(\prod_{b:B} (c(\mathrm{in}_B(b)) =_{C(\mathrm{in}_B(b))} c_{\mathrm{in}_B}(b))\right)\right)}$$

#### Natural numbers type

Formation rules for the natural numbers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{N} \; \mathrm{type}}$$

Introduction rules for the natural numbers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{N}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash s:\mathbb{N} \to \mathbb{N}}$$

Dependent universal property rule for the natural numbers type:
$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x))}{\Gamma \vdash \mathrm{up}_\mathbb{N}^C(c_0, c_s):\mathrm{isContr}\left(\sum_{c:\prod_{x:\mathbb{N}} C(x)} (c(0) =_{C(0)} c_0) \times \prod_{x:\mathbb{N}} c(s(x)) =_{C(s(x))} c_s(c(x))\right)}$$

#### Integers type

Formation rules for the integers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{Z} \; \mathrm{type}}$$

Introduction rules for the integers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{Z}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash s:\mathbb{Z} \simeq \mathbb{Z}}$$

Dependent universal property rule for the integers type:
$$\frac{\Gamma, x:\mathbb{Z} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_s:\prod_{x:\mathbb{Z}} C(x) \simeq C(s(x))}{\Gamma \vdash \mathrm{up}_\mathbb{Z}^C(c_0, c_s):\mathrm{isContr}\left(\sum_{c:\prod_{x:\mathbb{Z}} C(x)} (c(0) =_{C(0)} c_0) \times \prod_{x:\mathbb{Z}} c(s(x)) =_{C(s(x))} c_s(c(x))\right)}$$

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

* [[Mike Shulman]], Towards a Third-Generation HOTT Part 1 ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA))

* *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]], *[[Symmetry]]* (2021) $[$[pdf](https://unimath.github.io/SymmetryBook/book.pdf)$]$ 

[[!redirects objective type theory]]
[[!redirects objective type theories]]