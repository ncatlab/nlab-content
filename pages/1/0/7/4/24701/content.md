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
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \Pi(x:A).B(x) \; \mathrm{type}}$$

Introduction rules for identification types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A \vdash \mathrm{refl}_A(a) : a =_A a}$$

Introduction rules for dependent function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma \vdash \lambda(x:A).b(x):\Pi(x:A).B(x)}$$

Elimination rule for identification types:
$$\frac{\Gamma, x:A, y:A, p:x =_A y \vdash C(x, y, p) \; \mathrm{type}}{\Gamma, t:\Pi(a:A).C(a, a, \mathrm{refl}_A(a)), x:A, y:A, p:x =_A y \vdash \mathrm{ind}_{=_A}(t, x, y, p):C}$$

Elimination rules for dependent function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:\Pi(x:A).B(x), a:A \vdash \mathrm{ind}_{\Pi(x:A).B(x)}(f, a):B(a)}$$

Computation rules for identification types:
$$\frac{\Gamma, x:A, y:A, p:x =_A y \vdash C(x, y, p) \; \mathrm{type}}{\Gamma, t:\Pi(a:A).C(a, a, \mathrm{refl}_A(a)), x:A \vdash \beta_{=_A}(t, x):\mathrm{ind}_{=_A}(t, x, x, \mathrm{refl}_A(x)) =_{C(x, x, \mathrm{refl}_A(x))} t}$$

Computation rules for dependent function types
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma, a:A \vdash \beta_{\Pi(x:A).B(x)}(a):\mathrm{ind}_{\Pi(x:A).B(x)}(\lambda(x:A).b(x), a) =_{B(a)} b(a)}$$

Uniqueness rules for dependent function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:\Pi(x:A).B(x) \vdash \eta_{\Pi(x:A).B(x)}(f):f =_{\Pi(x:A).B(x)} \lambda(x).f(x)}$$

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

### Heterogeneous identification types

Now that we have identification types and dependent product types, we can define heterogeneous identification types, which are important for defining the isEquiv dependent type on a function, used to determine whether a function is an equivalence, and then used to define definitions. 

Formation rule for heterogeneous identification types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma \vdash y:B \quad \Gamma \vdash z:B
    \end{array}
  }{\Gamma \vdash y =_{B}^{p} z \; \mathrm{type}}$$ 

Introduction rule for heterogeneous identification types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma \vdash f:A \to B \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b
    \end{array}
  }{\Gamma \vdash \mathrm{ap}_{B}(f, a, b, p):f(a) =_{B}^{p} f(b)}$$ 

Elimination rule for heterogeneous identification types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:a =_A b, y:B(a), z:B(b), q:y =_{B}^p z \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:A \to B} \prod_{a:A} \prod_{b:A} \prod_{p:a =_A b} C(a, b, p, f(a), f(b), \mathrm{ap}_{B}(f, a, b, p)) \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma \vdash y:B \quad \Gamma \vdash z:B \quad \Gamma \vdash q:y =_{B}^p z
    \end{array}
  }{\Gamma \vdash J_{B}^p(t, a, y, b, z, p, q):C(a, y, b, z, p, q)}$$

Computation rules for heterogeneous identification types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:a =_A b, y:B, z:B, q:y =_{B}^p z \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:A \to B} \prod_{a:A} \prod_{b:A} \prod_{p:a =_A b} C(a, b, p, f(a), f(b), \mathrm{ap}_{B}(f, a, b, p)) \\
      \Gamma \vdash f:A \to B \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b
    \end{array}
  }{\Gamma \vdash \beta_{=_{B}^p}(t, f, a, b, p):J_{B}(t, a, f(a), b, f(b), p, \mathrm{ap}_{B}(f, a, b, p)) =_{C(a, f(a), b, f(b), p, \mathrm{ap}_{B}(f, a, b, p))} t}$$

### isEquiv types

The rules for isEquiv types are as follows:

Formation rules for isEquiv:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B}{\Gamma \vdash \mathrm{isEquiv}(f) \; \mathrm{type}}$$

Introduction rules for isEquiv:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B \quad \Gamma \vdash a:A \quad \Gamma \vdash b:\prod_{y:B} f(a) =_B y \\
      \Gamma \vdash \tau_A:\prod_{x:A} \prod_{y:B} (f(x) =_B y) \to (a =_A x) \quad \Gamma \vdash \tau_B:\prod_{x:A} \prod_{y:B} \prod_{z:f(x) =_B y} b(y) =_B^{\tau_A(x, y, z)} z
    \end{array}
  }{\Gamma \vdash \mathrm{witn}(a, b, \tau_A, \tau_B):\mathrm{isEquiv}(f)}$$

Elimination rules for isEquiv:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B \quad \Gamma \vdash p:\mathrm{isEquiv}(f) \\
      \Gamma, y:B \vdash C(y) \; \mathrm{type} \quad \Gamma \vdash c_f:\prod_{x:A} C(f(x)) \quad \Gamma \vdash b:B
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{isEquiv}(f)}^C(f, p, c_f, b):C(b)}$$

Computation rules for isEquiv:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B \quad \Gamma \vdash p:\mathrm{isEquiv}(f) \\
      \Gamma, y:B \vdash C(y) \; \mathrm{type} \quad \Gamma \vdash c_f:\prod_{x:A} C(f(x)) \quad \Gamma \vdash a:A
    \end{array}
  }{\Gamma \vdash \beta_{\mathrm{isEquiv}(f)}(f, p, c_f, a):\mathrm{ind}_{\mathrm{isEquiv}(f)}^C(f, p, c_f, f(a)) =_{C(f(a))} c_f(a)}$$

Uniqueness rules for isEquiv:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B \quad \Gamma \vdash p:\mathrm{isEquiv}(f) \\
      \Gamma, y:B \vdash C(y) \; \mathrm{type} \quad \Gamma \vdash c:\prod_{y:B} C(y) \quad \Gamma \vdash b:B
    \end{array}
  }{\Gamma \vdash \eta_{\mathrm{isEquiv}(f)}(f, p, c, b):c(b) =_{C(b)} \mathrm{ind}_{\mathrm{isEquiv}(f)}^C(f, p, c, b)}$$

### Structural rules for definitions

Now that we have finally defined identification types, we can define the structural rules for term definitions. The structural rules for term definitions say that given a term $a:A$ and a term definition $b \coloneqq a:A$, one could derive that $b$ is a term of $A$, and that there is an identification between $b$ and $a$:

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash a:A \quad \Gamma \vdash b \coloneqq a:A}{\Gamma \vdash \delta_A(a, b):a =_A b}$$

Similarly, now that we have finally defined function types and isEquiv types, we can define the structural rules for type definitions. The structural rules for type definitions say that given a type $A$ and a type definition $B \coloneqq A \; \mathrm{type}$, one could derive that $B$ is a type, that there is a function between $A$ and $B$, and that function is an equivalence:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash \delta_{A, B}:A \to B} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash \epsilon_{A, B}:\mathrm{isEquiv}(\delta_{A, B})}$$

### Dependent heterogeneous identification types

Now that we have identification types and dependent product types, we can define dependent heterogeneous identification types, which are important for defining the rules for higher inductive types. 

Formation rule for dependent heterogeneous identification types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma \vdash y:B(a) \quad \Gamma \vdash z:B(b)
    \end{array}
  }{\Gamma \vdash y =_{x:A.B(x)}^{p} z \; \mathrm{type}}$$ 

Introduction rule for dependent heterogeneous identification types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b
    \end{array}
  }{\Gamma \vdash \mathrm{apd}_{x:A.B(x)}(f, a, b, p):f(a) =_{x:A.B(x)}^{p} f(b)}$$ 

Elimination rule for dependent heterogeneous identification types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:a =_A b, y:B(a), z:B(b), q:y =_{x:A.B(x)}^p z \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:a =_A b} C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma \vdash y:B(a) \quad \Gamma \vdash z:B(b) \quad \Gamma \vdash q:y =_{x:A.B(x)}^p z
    \end{array}
  }{\Gamma \vdash J_{x:A.B(x)}^p(t, a, y, b, z, p, q):C(a, y, b, z, p, q)}$$

Computation rules for dependent heterogeneous identification types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:a =_A b, y:B(a), z:B(b), q:y =_{x:A.B(x)}^p z \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:a =_A b} C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \\
      \Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b
    \end{array}
  }{\Gamma \vdash \beta_{=_{x:A.B(x)}^p}(t, f, a, b, p):J_{x:A.B(x)}(t, a, f(a), b, f(b), p, \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) =_{C(a, f(a), b, f(b), p, \mathrm{apd}_{x:A.B(x)}(f, a, b, p))} t}$$

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
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \Sigma(x:A).B(x) \; \mathrm{type}}$$

Introduction rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, y:B(x) \vdash \mathrm{in}(x, y):\Sigma(x:A).B(x)}$$

Elimination rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, z:\Sigma(x:A).B(x) \vdash \mathrm{ind}_{\Sigma(x:A).B(x)}^A(z):A} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, z:\Sigma(x:A).B(x) \vdash \mathrm{ind}_{\Sigma(x:A).B(x)}^B(z):B(\mathrm{ind}_{\Sigma(x:A).B(x)}^A(z))}$$

Computation rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, y:B(x) \vdash \beta_{\Sigma(x:A).B(x)}^A(x, y):\mathrm{ind}_{\Sigma(x:A).B(x)}^A(\mathrm{in}(x, y)) =_A x}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, y:B(x) \vdash \beta_{\Sigma(x:A).B(x)}^B(x, y):\mathrm{ind}_{\Sigma(x:A).B(x)}^B(\mathrm{in}(x, y)) =_{B(\mathrm{ind}_{\Sigma(x:A).B(x)}^A(\mathrm{in}(x, y)))} y}$$

Uniqueness rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, z:\Sigma(x:A).B(x) \vdash \eta_{\Sigma(x:A).B(x)}(z):z =_{\Sigma(x:A).B(x)} \mathrm{in}(\mathrm{ind}_{\Sigma(x:A).B(x)}^A(z), \mathrm{ind}_{\Sigma(x:A).B(x)}^B(z))}$$

### Positive types

Now that we have [[identification types]], [[dependent heterogeneous identification types]], [[equivalence types]], [[dependent sum types]], and [[dependent product types]], we can use that to define the [[equivalence type]], the [[isContr]] [[modality]], the [[uniqueness quantifier]]
$$A \simeq B \coloneqq \sum_{f:A \to B} \mathrm{isEquiv}(f)$$

$$\mathrm{isContr}(A) \coloneqq \sum_{y:A} \prod_{z:A} y =_{A} z$$

$$\exists!x:A.B(x) \coloneqq \mathrm{isContr}\left(\sum_{x:A} B(x)\right)$$
and combine the [[elimination rule]], the [[computation rule]], and the [[uniqueness rule]] for any [[positive type]] into one rule, the [[universal property]] rule.   

#### Unit type

Formation rules for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{1} \; \mathrm{type}}$$

Introduction rules for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{pt}:\mathbb{1}}$$

Universal property rule for the unit type:
$$\frac{\Gamma, x:\mathbb{1} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{pt}:C(\mathrm{pt})}{\Gamma \vdash \mathrm{up}_\mathbb{1}^C(c_\mathrm{pt}):\exists!c:\prod_{x:\mathbb{1}} C(x).(c(\mathrm{pt}) =_{C(\mathrm{pt})} c_\mathrm{pt})}$$

#### Empty type

Formation rules for the empty type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{0} \; \mathrm{type}}$$

Universal property rule for the empty type:
$$\frac{\Gamma, x:\mathbb{0} \vdash C(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{up}_\mathbb{0}^C:\exists!c:\prod_{x:\mathbb{0}} C(x).\mathbb{1}}$$

#### Interval type

Formation rules for the interval type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{I} \; \mathrm{type}}$$

Introduction rules for the interval type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{I}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 1:\mathbb{I}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash p:0 =_{\mathbb{I}} 1}$$

Universal property rule for the interval type:
$$\frac{\Gamma, x:\mathbb{2} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_1:C(1) \quad \Gamma \vdash c_p:c_0 =_C^p c_1}{\Gamma \vdash \mathrm{up}_\mathbb{I}^C(c_0, c_1, c_p):\exists!c:\prod_{x:\mathbb{I}} C(x).(c(0) =_{C(0)} c_0) \times (c(1) =_{C(1)} c_1) \times (\mathrm{apd}_{x:\mathbb{I}.C(x)}(c, c_0, c_1, c_p) =_{c_0 =_C^p c_1} c_p)}$$

#### Copy types

Formation rules for copy types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{Copy}(A) \; \mathrm{type}}$$

Introduction rules for copy types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{copy}_A:A \to \mathrm{Copy}(A)}$$

Universal property rule for copy types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:\mathrm{Copy}(A) \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_{\mathrm{copy}_A}:\prod_{x:A} C(\mathrm{copy}_A(x))}{\Gamma \vdash \mathrm{up}_{\mathrm{Copy}(A)}^C(c_{\mathrm{copy}_A}):\exists!c:\prod_{x:\mathrm{Copy}(A)} C(x).\prod_{a:A} c(\mathrm{copy}_A(a)) =_{C(\mathrm{copy}_A(a))} c_{\mathrm{copy}_A}(a)}$$

### Positive types with extensionality rules

The following positive types has an additional extensionality rule characterizing the [[identification type]] of the positive type, defined using [[equivalence types]]. Otherwise, it is possible that the type is a proposition. 

#### Booleans type

Formation rules for the booleans type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{2} \; \mathrm{type}}$$

Introduction rules for the booleans type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{2}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 1:\mathbb{2}}$$

Universal property rule for the booleans type:
$$\frac{\Gamma, x:\mathbb{2} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_1:C(1)}{\Gamma \vdash \mathrm{up}_\mathbb{2}^C(c_0, c_1):\exists!c:\prod_{x:\mathbb{2}} C(x).(c(0) =_{C(0)} c_0) \times (c(1) =_{C(1)} c_1)}$$

Extensionality rules for the booleans type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{ext}_{\mathbb{2}}^{0, 0}:(0 =_{\mathbb{2}} 0) \simeq \mathbb{1}} \quad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{ext}_{\mathbb{2}}^{0, 1}:(0 =_{\mathbb{2}} 1) \simeq \mathbb{0}}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{ext}_{\mathbb{2}}^{1, 0}:(1 =_{\mathbb{2}} 0) \simeq \mathbb{0}} \quad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{ext}_{\mathbb{2}}^{1, 1}:(1 =_{\mathbb{2}} 1) \simeq \mathbb{1}}$$

#### Circle type

Formation rules for the circle type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash S^1 \; \mathrm{type}}$$

Introduction rules for the circle type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{base}:S^1} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{loop}:\mathrm{base} =_{S^1} \mathrm{base}}$$

Universal property rule for the circle type:
$$\frac{\Gamma, x:\mathbb{2} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_C^\mathrm{loop} c_\mathrm{base}}{\Gamma \vdash \mathrm{up}_\mathbb{I}^C(c_\mathrm{base}, c_\mathrm{loop}):\exists!c:\prod_{x:\mathbb{I}} C(x).(c(\mathrm{base}) =_{C(\mathrm{base})} c_\mathrm{base}) \times (\mathrm{apd}_C(c, c_\mathrm{base}, c_\mathrm{base}, c_\mathrm{loop}) =_{c_\mathrm{base} =_{x:S^1.C(x)}^\mathrm{loop} c_\mathrm{base}} c_\mathrm{loop})}$$

Extensionality rules for the circle type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{ext}_{S^1}:(\mathrm{base} =_{S^1} \mathrm{base}) \simeq \mathbb{N} + \mathbb{1} + \mathbb{N}}$$

#### Sum types

Formation rules for sum types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A + B \; \mathrm{type}}$$

Introduction rules for sum types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{in}_A:A \to A + B} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{in}_B:B \to A + B}$$

Universal property rule for sum types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A + B \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_{\mathrm{in}_A}:\prod_{x:A} C(\mathrm{in}_A(x)) \quad \Gamma \vdash c_{\mathrm{in}_B}:\prod_{y:B} C(\mathrm{in}_B(y))}{\Gamma \vdash \mathrm{up}_{A + B}^C(c_{\mathrm{in}_A}, c_{\mathrm{in}_B}):\exists!c:\prod_{x:A + B} C(x).\left(\prod_{a:A} (c(\mathrm{in}_A(a)) =_{C(\mathrm{in}_A(a))} c_{\mathrm{in}_A}(a))\right) \times \left(\prod_{b:B} (c(\mathrm{in}_B(b)) =_{C(\mathrm{in}_B(b))} c_{\mathrm{in}_B}(b))\right)}$$

Extensionality rules for the sum type:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{ext}_{A + B}^{\mathrm{in}_A, \mathrm{in}_A}:\prod_{a:A} \prod_{b:A} (\mathrm{in}_A(a) =_{A + B} \mathrm{in}_A(b)) \simeq (a =_A b)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{ext}_{A + B}^{\mathrm{in}_A, \mathrm{in}_B}:\prod_{a:A} \prod_{b:B} (\mathrm{in}_A(a) =_{A + B} \mathrm{in}_B(b)) \simeq \mathbb{0}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{ext}_{A + B}^{\mathrm{in}_B, \mathrm{in}_A}:\prod_{a:B} \prod_{b:A} (\mathrm{in}_B(a) =_{A + B} \mathrm{in}_A(b)) \simeq \mathbb{0}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{ext}_{A + B}^{\mathrm{in}_B, \mathrm{in}_B}:\prod_{a:B} \prod_{b:B} (\mathrm{in}_B(a) =_{A + B} \mathrm{in}_B(b)) \simeq (a =_B b)}$$

#### Natural numbers type

Formation rules for the natural numbers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{N} \; \mathrm{type}}$$

Introduction rules for the natural numbers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{N}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash s:\mathbb{N} \to \mathbb{N}}$$

Universal property rule for the natural numbers type:
$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x))}{\Gamma \vdash \mathrm{up}_\mathbb{N}^C(c_0, c_s):\exists!c:\prod_{x:\mathbb{N}} C(x).(c(0) =_{C(0)} c_0) \times \prod_{x:\mathbb{N}} c(s(x)) =_{C(s(x))} c_s(c(x))}$$

#### Integers type

Formation rules for the integers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{Z} \; \mathrm{type}}$$

Introduction rules for the integers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{Z}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash s:\mathbb{Z} \simeq \mathbb{Z}}$$

Universal property rule for the integers type:
$$\frac{\Gamma, x:\mathbb{Z} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_s:\prod_{x:\mathbb{Z}} C(x) \simeq C(s(x))}{\Gamma \vdash \mathrm{up}_\mathbb{Z}^C(c_0, c_s):\exists!c:\prod_{x:\mathbb{Z}} C(x).(c(0) =_{C(0)} c_0) \times \prod_{x:\mathbb{Z}} c(s(x)) =_{C(s(x))} c_s(c(x))}$$

#### Localizations

The localization of a type $A$ at a type $B$ is the (higher) inductive type $L_B(A)$ generated by a function $A \to L_B(A)$ and an equivalence $L_B(A) \simeq (B \to L_B(A))$:

Formation rules for localizations:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash L_B(A) \; \mathrm{type}}$$

Introduction rules for localizations:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{tolocal}:A \to L_B(A)} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{const}_B:L_B(A) \simeq (B \to L_B(A))}$$

#### Disjunctions

The disjunction of a type $A$ and a type $B$ is the (higher) inductive type $A \vee B$ generated by functions $A \to A \vee B$ and $B \to A \vee B$ and an equivalence $A \vee B \simeq (\mathbb{2} \to A \vee B)$:

Formation rules for disjunctions:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \vee B \; \mathrm{type}}$$

Introduction rules for disjunctions:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{in}_A:A \to A \vee B} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{in}_B:B \to A \vee B} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{const}_\mathbb{2}:A \vee B \simeq (\mathbb{2} \to A \vee B)}$$

#### Propositional truncations and set truncations

The propositional truncation $[A]$ of a type $A$ is localization of $A$ at the booleans type $\mathbb{2}$, $[A] \coloneqq L_\mathbb{2}(A)$. The set truncation $[A]_0$ of a type $A$ is localization of $A$ at the circle type $S^1$, $[A]_0 \coloneqq L_{S^1}(A)$. 

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

[[!redirects objective type theories]]