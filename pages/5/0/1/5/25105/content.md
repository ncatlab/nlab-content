
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

In [[dependent type theory]], the equivalence type between two types $A$ and $B$ is the type $A \simeq B$ whose terms are [[equivalence of types|equivalences]] between $A$ and $B$. There are two ways that equivalence types are defined in dependent type theory: analytically from other type formers in the type theory, and synthetically using rules in the type theory. 

### As a dependent sum type of the isEquiv type family

Given a notion of the [[isEquiv]] type family on the function type $A \to B$, the equivalence type is defined by 

$$A \simeq B \coloneqq \sum_{f:A \to B} \mathrm{isEquiv}(f)$$ 

### As a type whose elements are encodings for one-to-one correspondence

Given types $A$ and $B$, we form the type $A \simeq B$ such that given element $R:A \simeq B$, there is a type family $x =_{A, B}^R y$ indexed by $x:A$ and $y:B$, with rules stating that $(-) =_{A, B}^R (-)$ is a [[one-to-one correspondence]], and that given a type $A$, elements $a:A$ and $b:A$, identity $p:a =_A b$, a type family $B$ indexed by $A$ and a family of elements $w:B$ indexed by $A$, one could form the [[transport]] equivalence across $p$ for $B$, $\mathrm{tr}_B(p):B(a) \simeq B(b)$, and the dependent action on $p$ for $w$, $\mathrm{apd}_B(p, w):w(a) =_{B(a), B(b)}^{\mathrm{tr}_B(p)} w(b)$. 

Rules for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \simeq B \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, x:A, y:B \vdash x =_{A, B}^R y \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{tr}_B(p):B(a) \simeq B(b) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B \; \mathrm{type}}{\Gamma, x:A, w:B \vdash \mathrm{apd}_B(p, w):w(a) =_{B(a), B(b)}^{\mathrm{tr}_B(p)} w(b)}$$ 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, y:B \vdash \lambda(R, y):A} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, x:A \vdash \rho(R, x):B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, y:B, x:A, u:x =_{A, B}^R y \vdash \lambda_\kappa(R, x, y, u):\lambda(R, y) =_A x}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, y:B, x:A, u:x =_{A, B}^R y \vdash \rho_\kappa(R, x, y, u):\rho(R, x) =_B y}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, y:B \vdash \lambda_\tau(R, y):\lambda(R, y) =_{A, B}^R y}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, x:A \vdash \rho_\tau(R, x):x =_{A, B}^R \rho(R, x)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, y:B, x:A, u:x =_{A, B}^R y \vdash \lambda_\eta(R, y, x, u):\lambda_\tau(R, y) =_{(\lambda(R, y) =_{A, B}^R y), (x =_{A, B}^R y)}^{\mathrm{tr}_{(-) =_{A, B}^R y}(\lambda_\kappa(R, x, y, u))} u}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, x:A, y:B, u:x =_{A, B}^R y \vdash \rho_\eta(R, x, y, u):\rho_\tau(R, x) =_{(x =_{A, B}^R \rho(R, x)), (x =_{A, B}^R y)}^{\mathrm{tr}_{x =_{A, B}^R (-)}(\rho_\kappa(R, x, y, u))} u}$$

## Properties

### One-to-one correspondences

By the rules for [[dependent sum types]] and [[dependent product types]], one could show that the above rules result in each type family $(-) =_{A, B}^R (-)$ being a [[one-to-one correspondence]] for equivalence $R:A \simeq B$. By the [[introduction rule]] for [[dependent sum types]], one could form the judgments

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, y:B, x:A, u:x =_{A, B}^R y \vdash \eta_\lambda(R, y, x, u):\sum_{p:\lambda(R, y) =_A x} \lambda_\tau(R, y) =_{(\lambda(R, y) =_{A, B}^R y), (x =_{A, B}^R y)}^{\mathrm{tr}_{(-) =_{A, B}^R y}(p)} u}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, x:A, y:B, u:x =_{A, B}^R y \vdash \eta_\rho(R, x, y, u):\sum_{p:\rho(R, x) =_B y} \rho_\tau(R, x) =_{(x =_{A, B}^R \rho(R, x)), (x =_{A, B}^R y)}^{\mathrm{tr}_{x =_{A, B}^R (-)}(p)} u}$$

and by the extensionality principle for dependent sum types, one could form the judgments 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, y:B, x:A, u:x =_{A, B}^R y \vdash \eta_\lambda(R, y, x, u):(\lambda(R, y), \lambda_\tau(R, y)) =_{\sum_{x:A} x =_{A, B}^R y} (x, u)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, x:A, y:B, u:x =_{A, B}^R y \vdash \eta_\rho(R, x, y, u):(\rho(R, x), \rho_\tau(R, x)) =_{\sum_{y:B} x =_{A, B}^R y} (y, u)}$$

By the introduction rule for dependent sum types, the above is the same as 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, y:B, v:\sum_{x:A} x =_{A, B}^R y \vdash \eta_\lambda(R, y, v):(\lambda(R, y), \lambda_\tau(R, y)) =_{\sum_{x:A} x =_{A, B}^R y} v}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, x:A, v:\sum_{y:B} x =_{A, B}^R y \vdash \eta_\rho(R, x, v):(\rho(R, x), \rho_\tau(R, x)) =_{\sum_{y:B} x =_{A, B}^R y} v}$$

and by the introduction rule for [[dependent product types]], the above is the same as

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, y:B \vdash \eta_\lambda(R, y):\prod_{v:\sum_{x:A} x =_{A, B}^R y} (\lambda(R, y), \lambda_\tau(R, y)) =_{\sum_{x:A} x =_{A, B}^R y} v}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, x:A \vdash \eta_\rho(R, x):\prod_{v:\sum_{y:B} x =_{A, B}^R y} (\rho(R, x), \rho_\tau(R, x)) =_{\sum_{y:B} x =_{A, B}^R y} v}$$

Additionally, by the introduction rule for dependent sum types, there are rules

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, y:B \vdash \lambda_\tau'(R, y):\sum_{x:A} x =_{A, B}^R y}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, x:A \vdash \rho_\tau'(R, x):\sum_{x:A} x =_{A, B}^R y}$$

and thus rules 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, y:B \vdash \eta_\lambda(R, y):\prod_{v:\sum_{x:A} x =_{A, B}^R y} \lambda_\tau'(R, y) =_{\sum_{x:A} x =_{A, B}^R y} v}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, x:A \vdash \eta_\rho(R, x):\prod_{v:\sum_{y:B} x =_{A, B}^R y} \rho_\tau'(R, x) =_{\sum_{y:B} x =_{A, B}^R y} v}$$

Then by the introduction rule for dependent sum types, there is a rule

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, y:B \vdash \eta_\lambda(R, y):\sum_{u:\sum_{x:A} x =_{A, B}^R y} \prod_{v:\sum_{x:A} x =_{A, B}^R y} u =_{\sum_{x:A} x =_{A, B}^R y} v}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, x:A \vdash \eta_\rho(R, x):\sum_{u:\sum_{y:B} x =_{A, B}^R y} \prod_{v:\sum_{y:B} x =_{A, B}^R y} u =_{\sum_{y:B} x =_{A, B}^R y} v}$$

which could be simplified down to

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, y:B \vdash \eta_\lambda(R, y):\mathrm{isContr}\left(\sum_{x:A} x =_{A, B}^R y\right)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, x:A \vdash \eta_\rho(R, x):\mathrm{isContr}\left(\sum_{y:B} x =_{A, B}^R y\right)}$$

By the introduction rules for dependent product types, there are rules 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B \vdash \eta_\lambda(R):\prod_{y:B} \mathrm{isContr}\left(\sum_{x:A} x =_{A, B}^R y\right)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B \vdash \eta_\rho(R):\prod_{x:A} \mathrm{isContr}\left(\sum_{y:B} x =_{A, B}^R y\right)}$$

and by the introduction rules for product types, there is a rule

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B \vdash \eta(R):\left(\prod_{y:B} \mathrm{isContr}\left(\sum_{x:A} x =_{A, B}^R y\right)\right) \times \left(\prod_{x:A} \mathrm{isContr}\left(\sum_{y:B} x =_{A, B}^R y\right)\right)}$$

which is precisely the condition that $(-) =_{A, B}^R (-)$ is a [[one-to-one correspondence]] for all equivalences $R:A \simeq B$. 

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

## See also

* [[equivalence in type theory]]

* [[identity type]], [[heterogeneous identity type]]

## References

For the definition of the equivalence type as a dependent sum type, see:

* {#UFP13} [[Univalent Foundations Project]], §2.4 and §4 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

[[!redirects equivalence type]]
[[!redirects equivalence types]]

[[!redirects type of equivalences]]
[[!redirects types of equivalences]]