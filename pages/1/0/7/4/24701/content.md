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

### Basic type formers

In this section, we give the rules for the basic type formers of type theory. This includes [[identification types]], [[dependent identification types]], [[function types]], [[dependent function types]], [[pair types]], and [[dependent pair types]]. 

#### Formation rules

Formation rules for identification types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, b:A \vdash a =_A b \; \mathrm{type}}$$

Formation rules for dependent function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \Pi(x:A).B(x) \; \mathrm{type}}$$

Formation rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type}}{\Gamma \vdash \Sigma(x:A).B(x) \; \mathrm{type}}$$

#### Introduction rules

Introduction rules for identification types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A \vdash \mathrm{refl}_A(a) : a =_A a}$$

Introduction rules for dependent function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma \vdash \lambda(x:A).b(x):\Pi(x:A).B(x)}$$

Introduction rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, y:B(x) \vdash \mathrm{in}(x, y):\Sigma(x:A).B(x)}$$

#### Elimination rules

Elimination rule for identification types:
$$\frac{\Gamma, x:A, y:A, p:x =_A y \vdash C(x, y, p) \; \mathrm{type}}{\Gamma, t:\Pi(a:A).C(a, a, \mathrm{refl}_A(a)), x:A, y:A, p:x =_A y \vdash \mathrm{ind}_{=_A}(t, x, y, p):C}$$

Elimination rules for dependent function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:\Pi(x:A).B(x), a:A \vdash \mathrm{ind}_{\Pi(x:A).B(x)}(f, a):B(a)}$$

Elimination rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, z:\Sigma(x:A).B(x) \vdash \mathrm{ind}_{\Sigma(x:A).B(x)}^A(z):A} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, z:\Sigma(x:A).B(x) \vdash \mathrm{ind}_{\Sigma(x:A).B(x)}^B(z):B(\mathrm{ind}_{\Sigma(x:A).B(x)}^A(z))}$$

#### Computation rules

Computation rules for identification types:
$$\frac{\Gamma, x:A, y:A, p:x =_A y \vdash C(x, y, p) \; \mathrm{type}}{\Gamma, t:\Pi(a:A).C(a, a, \mathrm{refl}_A(a)), x:A \vdash \beta_{=_A}(t, x):\mathrm{ind}_{=_A}(t, x, x, \mathrm{refl}_A(x)) =_{C(x, x, \mathrm{refl}_A(x))} t}$$

Computation rules for dependent function types
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma, a:A \vdash \beta_{\Pi(x:A).B(x)}(a):\mathrm{ind}_{\Pi(x:A).B(x)}(\lambda(x:A).b(x), a) =_{B(a)} b(a)}$$

Computation rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, y:B(x) \vdash \beta_{\Sigma(x:A).B(x)}^A(x, y):\mathrm{ind}_{\Sigma(x:A).B(x)}^A(\mathrm{in}(x, y)) =_A x}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, y:B(x) \vdash \beta_{\Sigma(x:A).B(x)}^B(x, y):\mathrm{ind}_{\Sigma(x:A).B(x)}^B(\mathrm{in}(x, y)) =_{B(\mathrm{ind}_{\Sigma(x:A).B(x)}^A(\mathrm{in}(x, y)))} y}$$

#### Uniqueness rules

Uniqueness rules for dependent function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:\Pi(x:A).B(x) \vdash \eta_{\Pi(x:A).B(x)}(f):f =_{\Pi(x:A).B(x)} \lambda(x).f(x)}$$

Uniqueness rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, z:\Sigma(x:A).B(x) \vdash \eta_{\Sigma(x:A).B(x)}(z):z =_{\Sigma(x:A).B(x)} \mathrm{in}(\mathrm{ind}_{\Sigma(x:A).B(x)}^A(z), \mathrm{ind}_{\Sigma(x:A).B(x)}^B(z))}$$

### Dependent identification types

Now that we have identification types, dependent sum types, and dependent product types, we can define dependent identification types, which are important for defining the rules for higher inductive types. 

Formation rule for dependent identification types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, a:A, y:B(a), b:A, z:B(b), p:a =_A b \vdash y =_B^{p} z \; \mathrm{type}}$$ 

Introduction rule for dependent identification types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:\Pi(x:A).B(x), a:A, b:A, p:a =_A b \vdash \mathrm{apd}_B(f, a, b, p):f(a) =_B^{p} f(b)}$$ 

Elimination rule for dependent identification types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, a:A, y:B(a), b:A, z:B(b), p:a =_A b, q:y =_B^p z \vdash C(a, y, b, z, p, q) \; \mathrm{type} \\
      \Gamma \vdash t:\Pi(a:A).\Pi(b:A).\Pi(p:a =_A b).\Pi(f:\Pi(x:A).B(x)).C(a, f(a), b, f(b), p, \mathrm{apd}_B(f, a, b, p))
    \end{array}
  }{\Gamma, a:A, y:B(a), b:A, z:B(b), p:a =_A b, q:y =_B^p z \vdash J_B^p(t, a, y, b, z, p, q):C(a, y, b, z, p, q)}$$

Computation rules for dependent identification types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, a:A, y:B(a), b:A, z:B(b), p:a =_A b, q:y =_B^p z \vdash C(a, y, b, z, p, q) \; \mathrm{type} \\
      \Gamma \vdash t:\Pi(a:A).\Pi(b:A).\Pi(p:a =_A b).\Pi(f:\Pi(x:A).B(x)).C(a, f(a), b, f(b), p, \mathrm{apd}_B(f, a, b, p))
    \end{array}
  }{\Gamma, f:\Pi(x:A).B(x), a:A, b:A, p:a =_A b \vdash \beta_{=_B^p}(t, f, a, b, p):J_B(t, a, f(a), b, f(b), p, \mathrm{apd}_B(f, a, b, p)) =_{C(a, f(a), b, f(b), p, \mathrm{apd}_B(f, a, b, p))} t}$$

### Structural rules for definitions

Now that we have finally defined identification types, we can define the structural rules for term definitions. The structural rules for term definitions say that given a term $a:A$ and a term definition $b \coloneqq a:A$, one could derive that $b$ is a term of $A$, and that there is an identification between $b$ and $a$:

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash a:A \quad \Gamma \vdash b \coloneqq a:A}{\Gamma \vdash \delta_A(a, b):b =_A a}$$

The structural rules for type definitions are the natural deduction rules for [[copying]] types, with formation and introduction rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{copy}(a):B}$$

elimination rules:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type} \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:B}{\Gamma \vdash \mathrm{ind}_{B}^C(c, e):C[e/z]}$$

computation rules:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type} \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_B:\mathrm{ind}_{B}^C(c, \mathrm{copy}(a)) =_{C[\mathrm{copy}(a)/z]} c[a/x]}$$

and uniqueness rules:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type} \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:B \quad \Gamma, y:B \vdash u:C \quad \Gamma, a:A \vdash i_\mathrm{copy}(u):u[\mathrm{copy}(a)/y] =_{C[\mathrm{copy}(a)/y]} c[a/x]}{\Gamma \vdash \eta_{B}:u[e/z] =_{C[e/z]} \mathrm{ind}_{B}^C(c, e)}$$

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

### Other positive types

Now that we have [[identification types]], [[dependent sum types]], and [[dependent product types]], we can combine the [[elimination rule]], the [[computation rule]], and the [[uniqueness rule]] for any [[positive type]] into one rule, the [[universal property]] rule. 

#### Unit type

Formation rules for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{1} \; \mathrm{type}}$$

Introduction rules for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{pt}:\mathbb{1}}$$

Universal property rule for the unit type:
$$\frac{\Gamma, x:\mathbb{1} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{pt}:C(\mathrm{pt})}{\Gamma \vdash \mathrm{up}_\mathbb{1}^C(c_\mathrm{pt}):\mathrm{isContr}\left(\sum_{c:\prod_{x:\mathbb{1}} C(x)} (c(\mathrm{pt}) =_{C(\mathrm{pt})} c_\mathrm{pt})\right)}$$

#### Copy types

Formation rules for copy types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{Copy}(A) \; \mathrm{type}}$$

Introduction rules for copy types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{copy}_A:A \to \mathrm{Copy}(A)}$$

Universal property rule for copy types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:\mathrm{Copy}(A) \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_{\mathrm{copy}_A}:\prod_{x:A} C(\mathrm{copy}_A(x))}{\Gamma \vdash \mathrm{up}_{\mathrm{Copy}(A)}^C(c_{\mathrm{copy}_A}):\mathrm{isContr}\left(\sum_{c:\prod_{x:\mathrm{Copy}(A)} C(x)} \prod_{a:A} c(\mathrm{copy}_A(a)) =_{C(\mathrm{copy}_A(a))} c_{\mathrm{copy}_A}(a)\right)}$$

#### Booleans type

Formation rules for the booleans type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{2} \; \mathrm{type}}$$

Introduction rules for the booleans type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{2}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 1:\mathbb{2}}$$

Universal property rule for the booleans type:
$$\frac{\Gamma, x:\mathbb{2} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_1:C(1)}{\Gamma \vdash \mathrm{up}_\mathbb{2}^C(c_0, c_1):\mathrm{isContr}\left(\sum_{c:\prod_{x:\mathbb{2}} C(x)} (c(0) =_{C(0)} c_0) \times (c(1) =_{C(1)} c_1)\right)}$$

#### Sum types

Formation rules for sum types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A + B \; \mathrm{type}}$$

Introduction rules for sum types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{in}_A:A \to A + B} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{in}_B:B \to A + B}$$

Universal property rule for sum types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A + B \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_{\mathrm{in}_A}:\prod_{x:A} C(\mathrm{in}_A(x)) \quad \Gamma \vdash c_{\mathrm{in}_B}:\prod_{y:B} C(\mathrm{in}_B(y))}{\Gamma \vdash \mathrm{up}_{A + B}^C(c_{\mathrm{in}_A}, c_{\mathrm{in}_B}):\mathrm{isContr}\left(\sum_{c:\prod_{x:A + B} C(x)} \left(\prod_{a:A} (c(\mathrm{in}_A(a)) =_{C(\mathrm{in}_A(a))} c_{\mathrm{in}_A}(a))\right) \times \left(\prod_{b:B} (c(\mathrm{in}_B(b)) =_{C(\mathrm{in}_B(b))} c_{\mathrm{in}_B}(b))\right)\right)}$$

#### Natural numbers type

Formation rules for the natural numbers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{N} \; \mathrm{type}}$$

Introduction rules for the natural numbers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{N}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash s:\mathbb{N} \to \mathbb{N}}$$

Universal property rule for the natural numbers type:
$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x))}{\Gamma \vdash \mathrm{up}_\mathbb{N}^C(c_0, c_s):\mathrm{isContr}\left(\sum_{c:\prod_{x:\mathbb{N}} C(x)} (c(0) =_{C(0)} c_0) \times \prod_{x:\mathbb{N}} c(s(x)) =_{C(s(x))} c_s(c(x))\right)}$$

#### Integers type

Formation rules for the integers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{Z} \; \mathrm{type}}$$

Introduction rules for the integers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{Z}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash s:\mathbb{Z} \simeq \mathbb{Z}}$$

Universal property rule for the integers type:
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