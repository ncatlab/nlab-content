
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

In [[dependent type theory]], the equivalence type is to types what the [[identity type]] is to [[terms]]: it represents the collection of "[[equalities]]" between types (equality of types being given by the notion of [[equivalence in type theory]]), in the same way that the identity type represents the collection of equalities between terms (equality of terms being given by the notion of [[identity]]/[[identification]]/[[path]]). 

## Definition

In [[dependent type theory]], the equivalence type between two types $A$ and $B$ is the type $A \simeq B$ whose terms are [[equivalence of types|equivalences]] between $A$ and $B$. Like any other notion of type in dependent type theory, there are two different notions of equivalence types in type theory: strict and weak equivalence types. Strict equivalence types use [[judgmental equality]] in the [[conversion rules]], while weak equivalence types use [[identity types]] in the conversion rules. Weak equivalence types could also be defined analytically from other type formers in the type theory. 

### Strict equivalence types

Given types $A$ and $B$, one could define the type of [[strict equivalences]] betwen $A$ and $B$. These are given by the following rules:

Formation rule for strict equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \simeq B \; \mathrm{type}}$$

Introduction rule for strict equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B \quad \Gamma, y:B \vdash g(y):A \quad \Gamma, x:A \vdash g(f(x)) \equiv x:A \quad \Gamma, y:B \vdash f(g(y)) \equiv y:B}{\Gamma \vdash \mathrm{toequiv}(x:A.f(x), y:B.g(y)):A \simeq B}$$

Elimination rules for strict equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, e:A \simeq B, x:A \vdash \overrightarrow{e}(x):B} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, e:A \simeq B, y:B \vdash \overleftarrow{e}(x):A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, e:A \simeq B, x:A \vdash \overleftarrow{e}(\overrightarrow{e}(x)) \equiv x:A} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, e:A \simeq B, y:B \vdash \overrightarrow{e}(\overleftarrow{e}(y)) \equiv y:B}$$

Computation rules for strict equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B \quad \Gamma, y:B \vdash g(y):A \quad \Gamma, x:A \vdash g(f(x)) \equiv x:A \quad \Gamma, y:B \vdash f(g(y)) \equiv y:B}{\Gamma, x:A \vdash \overrightarrow{\mathrm{toequiv}(x:A.f(x), y:B.g(y))}(x) \equiv f(x):B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B \quad \Gamma, y:B \vdash g(y):A \quad \Gamma, x:A \vdash g(f(x)) \equiv x:A \quad \Gamma, y:B \vdash f(g(y)) \equiv y:B}{\Gamma, y:B \vdash \overleftarrow{\mathrm{toequiv}(x:A.f(x), y:B.g(y))}(y) \equiv g(y):A}$$

Uniqueness rules for strict equivalence types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, e:A \simeq B \vdash \mathrm{toequiv}(x:A.\overrightarrow{e}(x), y:B.\overleftarrow{e}(y)) \equiv e:A \simeq B}$$

### Weak equivalence types

#### As a dependent sum type of the isEquiv type family

Given a notion of the [[isEquiv]] type family on the function type $A \to B$, the equivalence type is defined by 

$$A \simeq B \coloneqq \sum_{f:A \to B} \mathrm{isEquiv}(f)$$ 

#### Locally small equivalence types

Given a [[type universe]] $U$ and a notion of a $U$-small [[isEquiv]] type family for some type $F_U(A, B)$, the locally $U$-small equivalence type is defined by 

$$A \simeq_U B \coloneqq \sum_{f:F_U(A, B)} \mathrm{isEquiv}_U(f)$$ 

$F_U(A, B)$ could be the type of $U$-small [[spans]], the type of $U$-small [[multivalued partial functions]], or the type of $U$-small [[correspondences]]. 

#### Rules for weak equivalence types

In the same way that [[isEquiv]] could be defined in a way such that given the function $f:A \to B$ and a witness $p:\mathrm{isEquiv}(f)$, $(B, f, p)$ satisfies the universal property of a [[wrapped copy]] of $A$, one could define weak equivalence types such that given an equivalence $e:A \simeq B$, $(B, e)$ satsifes the universal property of a [[wrapped copy]] of $A$:

Formation rules for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \simeq B \; \mathrm{type}}$$

Introduction rules for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash g:B \to A \quad \Gamma \vdash G:\prod_{y:B} \mathrm{Id}_B(f(g(y)), y) \quad \Gamma \vdash H:\prod_{x:A} \mathrm{Id}_A(g(f(x)), x)}{\Gamma \vdash \mathrm{toequiv}(f, g, G, H):A \simeq B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, e:A \simeq B, x:A \vdash \mathrm{eval}_{A, B}(e, x):B}$$

Elimination rules for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:B \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_{\mathrm{eval}_{A, B}}:\prod_{e:A \simeq B} \prod_{x:A} C(\mathrm{eval}_{A, B}(e, x))}{\Gamma, e:A \simeq B, y:B \vdash \mathrm{ind}_{A \simeq B}^C(c_{\mathrm{eval}_{A, B}}, e, y):C(y)}$$

Computation rules for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:B \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_{\mathrm{eval}_{A, B}}:\prod_{e:A \simeq B} \prod_{x:A} C(\mathrm{eval}_{A, B}(e, x))}{\Gamma, e:A \simeq B, x:A \vdash \beta_{A \simeq B}^{C}(c_{\mathrm{eval}_{A, B}}, e, x):\mathrm{ind}_{A \simeq B}^C(c_{\mathrm{eval}_{A, B}}, e, \mathrm{eval}_{A, B}(e, x)) =_{C(\mathrm{eval}_{A, B}(e, x))} c_{\mathrm{eval}_{A, B}}(e, x)}$$

Uniqueness rules for equivalence types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:A \simeq B \\
      \Gamma, y:B \vdash C(y) \; \mathrm{type} \quad \Gamma \vdash c:A \simeq B \to \prod_{y:B} C(y) \quad \Gamma \vdash b:B
    \end{array}
  }{\Gamma, e:A \simeq B, y:B \vdash \eta_{A \simeq B}(c, e, y):c(y) =_{C(y)} \mathrm{ind}_{A \simeq B}^C(c, e, y)}$$

If we have [[uniqueness quantifiers]], we could combine the elimination, computation, and uniqueness rules for equivalence types into recursion and induction rules for equivalence types:

Recursion rule for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash c_{\mathrm{eval}_{A, B}}:A \simeq B \to (A \to C)}{\Gamma \vdash \mathrm{up}_{A \simeq B}^C(c_{\mathrm{eval}_{A, B}}):\exists!c:(A \simeq B) \to (B \to C).\prod_{e:A \simeq B} \prod_{x:A} c(e, \mathrm{eval}_{A, B}(e, x)) =_{C} c_{\mathrm{eval}_{A, B}}(e, x)}$$

Induction rule for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, y:B \vdash C(y) \; \mathrm{type} \quad \Gamma \vdash c_{\mathrm{eval}_{A, B}}:\prod_{e:A \simeq B} \prod_{x:A} C(\mathrm{eval}_{A, B}(e, x))}{\Gamma \vdash \mathrm{dup}_{A \simeq B}^C(c_{\mathrm{eval}_{A, B}}):\exists!c:(A \simeq B) \to \prod_{y:B} C(y).\prod_{e:A \simeq B} \prod_{x:A} c(e, \mathrm{eval}_{A, B}(e, x)) =_{C(\mathrm{eval}_{A, B}(e, x))} c_{\mathrm{eval}_{A, B}}(e, x)}$$

#### Coinductive definition

Given two types $A$ and $B$ and two functions $f:A \to B$ and $g:B \to A$, $f$ and $g$ are inverses of each other if for every element $a:A$ and $b:A$, there is an equivalence of types between $f(a) =_B b$ and $a =_A g(b)$:

$$\mathrm{isInv}(f, g) \coloneqq \prod_{a:A} \prod_{b:B} (f(a) =_B b) \simeq (a =_A g(b))$$

This leads to a coinductive definition of the type of equivalences

$$A \simeq B \coloneqq \sum_{f:A \to B} \sum_{g:B \to A} \prod_{a:A} \prod_{b:B} (f(a) =_B b) \simeq (a =_A g(b))$$

Formation rule for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \simeq B \; \mathrm{type}}$$

Introduction rule for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{tr}_B(a, b, p):B(a) \simeq B(b) \; \mathrm{type}}$$

Elimination rules for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \simeq B \quad \Gamma \vdash x:A}{\Gamma \vdash f(x):B} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \simeq B \quad \Gamma \vdash y:B}{\Gamma \vdash f^{-1}(y):A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \simeq B \quad \Gamma \vdash x:A \quad \Gamma \vdash y:B}{\Gamma\vdash \mathrm{coh}(f, x, y):(f(x) =_B y) \simeq (x =_A f^{-1}(y))}$$

Computation rules for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash w:B(x)}{\Gamma \vdash \mathrm{apdl}_B(a, b, p, w):w(a) =_{B(a)} \mathrm{tr}_B(a, b, p)^{-1}(w(b))}$$ 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash w:B(x)}{\Gamma \vdash \mathrm{apdr}_B(a, b, p, w):\mathrm{tr}_B(a, b, p)(w(a)) =_{B(b)} w(b)}$$ 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash w:B(x)}{\Gamma \vdash \mathrm{cohapd}_B(a, b, p, w):\left(\mathrm{coh}(\mathrm{tr}_B(a, b, p), w(a), w(b))(\mathrm{apdr}_B(a, b, p, w)) =_{w(a) =_{B(a)} \mathrm{tr}_B(a, b, p)^{-1}(w(b))} \mathrm{apdl}_B(a, b, p, w)\right) \simeq \left(\mathrm{apdr}_B(a, b, p, w) =_{\mathrm{tr}_B(a, b, p)(w(a)) =_{B(b)} w(b)} \mathrm{coh}(\mathrm{tr}_B(a, b, p), w(a), w(b))^{-1}(\mathrm{apdl}_B(a, b, p, w))\right)}$$ 

## Properties

### Relation to interval types

Given types $A$ and $B$ and an equivalence $f:A \simeq B$, one could define the dependent type $x:\mathbb{I} \vdash C(x)$ indexed by the [[interval type]] $\mathbb{I}$ as $C(0) \equiv A$, $C(1) \equiv B$, and $\mathrm{tr}_C(0, 1, p) \equiv f$. 

### One-to-one correspondences

Given types $A$ and $B$ and an equivalence $f:A \simeq B$, one could define a [[correspondence]] $x:A, y:B \vdash R(x, y)$ as the [[dependent identity type]] 
$$R(x, y) \coloneqq x =_C^p y$$
where $x:\mathbb{I} \vdash C(x)$ is defined as in the previous section. By the properties of [[dependent identity types]], the correspondence is always a [[one-to-one correspondence]]. 

### Quasi-inverse functions with contractible fibers

By the rules for [[function types]], given an equivalence $R:A \simeq B$, one could derive functions $\rho(R):A \to B$ and $\lambda(R):B \to A$. One could show that these functions are [[quasi-inverse functions]] of each other: for all $x:A$ and $y:B$ and equivalences $R:A \simeq B$, there are identities 
$$\rho_\kappa(R, \lambda(R, y), y, \lambda_\tau(R, y)):\rho(R)(\lambda(R)(y)) =_B y$$
$$\lambda_\kappa(R, x, \rho(R)(x), \rho_\tau(R, x)^{-1}):\lambda(R)(\rho(R)(x)) =_A x$$
where $p^{-1}:b =_A a$ is the inverse identity of $p:a =_A b$. By the introduction rule for dependent product types, there are [[homotopies]]
$$\lambda y.\rho_\kappa(R, \lambda(R, y), y, \lambda_\tau(R, y)):\prod_{y:B} \rho(R)(\lambda(R)(y)) =_B y$$
$$\lambda x.\lambda_\kappa(R, x, \rho(R)(x), \rho_\tau(R, x)^{-1}):\prod_{x:A} \lambda(R)(\rho(R)(x)) =_A x$$
which indicate that $\rho(R)$ and $\lambda(R)$ are quasi-inverse functions of each other. 

By the rules for [[dependent sum types]] and [[dependent product types]], one could show that the above functions each have [[contractible]] [[fibers]], making both of them [[coherent inverse functions]] of each other. 

### Heterogeneous identity types

Given the definition of the equivalence type as the type of encodings for one-to-one correspondences, the [[heterogeneous identity type]] is defined by the rule 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B \; \mathrm{type}}{\Gamma \vdash (x =_B^p y) \equiv (x =_{B(a), B(b)}^{\mathrm{tr}_B(p)} y) \; \mathrm{type}}$$

### Identity equivalences, inverse equivalences, and composition of equivalences

The identity equivalence on a type $A$ is defined as an equivalence $\mathrm{id}_A:A \simeq A$ such that for all elements $a:A$,

$$\lambda(\mathrm{id}_A, a) \coloneqq a$$
$$\rho(\mathrm{id}_A, a) \coloneqq a$$
$$(a =_{A, A}^{\mathrm{id}_A} b) \coloneqq (a =_A b)$$

Given an equivalence $R:A \simeq B$, the inverse equivalence of $R$ is an equivalence $R^{-1}:B \simeq A$ such that for all elements $a:A$ and $b:B$,

$$\rho(R^{-1}, a) \coloneqq \lambda(R, a)$$
$$\lambda(R^{-1}, b) \coloneqq \rho(R, b)$$
$$b =_{B, A}^{R^{-1}} a \coloneqq a =_{A, B}^R b$$

Given equivalences $R:A \simeq B$ and $S:B \simeq C$, the composite of $R$ and $S$ is an equivalence $S \circ R:A \simeq C$ such that for all elements $a:A$ and $c:C$,

$$\lambda(S \circ R, a) \coloneqq \lambda(R, \lambda(S, a))$$
$$\rho(S \circ R, c) \coloneqq \rho(S, \rho(R, c))$$
$$a =_{A, C}^{S \circ R} c \coloneqq \sum_{b:B} (a =_{A, B}^R b) \times (b =_{B, C}^R c)$$

### Relation to universes and univalence

Given a [[Russell universe]] $U$, there are two ways to say that types $A:U$ and $B:U$ are equal: by the [[identity type]] $A =_U B$, and the equivalence type $A \simeq B$. The [[univalence axiom]] says that these two types $A =_U B$ and $A \simeq B$ are the same, which is represented by an equivalence between the two types

$$\mathrm{ua}(A, B):(A =_U B) \simeq (A \simeq B)$$

For [[Tarski universes]] $(U, \mathrm{El})$, one instead says that $A =_U B$ is the same as $\mathrm{El}(A) \simeq \mathrm{El}(B)$, represented as 

$$\mathrm{ua}(A, B):(A =_U B) \simeq (\mathrm{El}(A) \simeq \mathrm{El}(B))$$

### Action on equivalences

We introduce a [[modal operator]] $L$ to the type theory, which we assume in general not to be [[idempotent]] or [[monadic]]; this is given by the formation rule 
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash L(A) \; \mathrm{type}}$$
$L$ preserves equivalences: given types $A$ and $B$, there is a function $\mathrm{ae}_L:(A \simeq B) \to L(A) \simeq L(B)$, called the action on equivalences for $L$. 

### Categorical semantics

The [[categorical semantics]] of an equivalence type is an [[object of isomorphisms]]. 

## See also

* [[bijection set]], [[object of isomorphisms]]

* [[equivalence in type theory]]

* [[identity type]], [[heterogeneous identity type]]

* [[autoequivalence type]]

* [[function type]], [[embedding type]]

* [[equivalence extensionality]]

## References

For the definition of the equivalence type as a dependent sum type, see:

* {#UFP13} [[Univalent Foundations Project]], §2.4 and §4 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

[[!redirects equivalence type]]
[[!redirects equivalence types]]

[[!redirects type of equivalences]]
[[!redirects types of equivalences]]

[[!redirects locally small equivalence type]]
[[!redirects locally small equivalence types]]

[[!redirects type of locally small equivalences]]
[[!redirects types of locally small equivalences]]

[[!redirects weak equivalence type]]
[[!redirects weak equivalence types]]

[[!redirects type of weak equivalences]]
[[!redirects types of weak equivalences]]

[[!redirects strict equivalence type]]
[[!redirects strict equivalence types]]

[[!redirects type of strict equivalences]]
[[!redirects types of strict equivalences]]

[[!redirects judgmentally strict equivalence type]]
[[!redirects judgmentally strict equivalence types]]

[[!redirects type of judgmentally strict equivalences]]
[[!redirects types of judgmentally strict equivalences]]

[[!redirects propositionally strict equivalence type]]
[[!redirects propositionally strict equivalence types]]

[[!redirects type of propositionally strict equivalences]]
[[!redirects types of propositionally strict equivalences]]