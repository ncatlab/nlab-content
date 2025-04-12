
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

In [[dependent type theory]], the equivalence type between two types $A$ and $B$ is the type $A \simeq B$ whose terms are [[equivalence of types|equivalences]] between $A$ and $B$. Like any other notion of type in dependent type theory, there are two different notions of equivalence types in type theory: strict and weak equivalence types. Strict equivalence types use [[judgmental equality]] in the [[conversion rules]], while weak equivalence types use [[identity types]] in the conversion rules. 

### As a dependent sum type of the isEquiv type family

Given a notion of the [[isEquiv]] type family on the function type $A \to B$, the equivalence type is defined by 

$$A \simeq B \coloneqq \sum_{f:A \to B} \mathrm{isEquiv}(f)$$ 

### Locally small equivalence types

Given a [[type universe]] $U$ and a notion of a $U$-small [[isEquiv]] type family for some type $F_U(A, B)$, the locally $U$-small equivalence type is defined by 

$$A \simeq_U B \coloneqq \sum_{f:F_U(A, B)} \mathrm{isEquiv}_U(f)$$ 

$F_U(A, B)$ could be the type of $U$-small [[spans]], the type of $U$-small [[multivalued partial functions]], or the type of $U$-small [[correspondences]]. 

### Rules for equivalence types

There are various different rules one can use for equivalence types, depending upon what notion of equivalence one wishes to use:

* One-To-One correspondences
* Half-adjoint equivalences
* Biinvertible functions
* Functions with contractible fibers

#### One-To-One correspondence types

Let $\mathrm{isContr}(A)$ denote the [[isContr]] [[modality]] which says whether the type $A$ is a [[contractible type]], and let 
$$\exists!x:A.B(x) \coloneqq \mathrm{isContr}\left(\sum_{x:A} B(x)\right)$$ 
be the [[uniqueness quantifier]] over the type family $x:A \vdash B(x)$. A binary correspondence between types $A$ and $B$ is simply a binary type family $x:A, y:B \vdash R(x, y)$. A binary correspondence $x:A, y:B \vdash R(x, y)$ is **one-to-one** if 

* for all $x:A$ there is a unique $y:B$ such that $R(x, y)$, and

* for all $y:B$ there is a unique $x:A$ such that $R(x, y)$. 

Written out in the language of dependent type theory, one has 

$$\mathrm{isOneToOne}(\chi.\gamma.R) \coloneqq \left(\prod_{x:A} \exists!y:B.R(x, y)\right) \times \left(\prod_{y:B} \exists!x:A.R(x, y)\right)$$

In the presence of some form of [[function extensionality]], the type $\mathrm{isOneToOne}(\chi.\gamma.R)$ is guaranteed to be a [[mere proposition]]. 

The rules for equivalence types then state that equivalences, the elements of equivalence types, are (codes for) [[one-to-one correspondences]] (in the same way that functions, the elements of function types, are (codes for) families of elements):

Formation rules for equivalence types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \simeq B \; \mathrm{type}}$$

Introduction rules for equivalence types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A, y:A \vdash R(x, y) \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isOneToOne}(\chi.\gamma.R)}{\Gamma \vdash \mathrm{toEquiv}_{\chi.\gamma.R}(p):A \simeq B}$$

Elimination rules for equivalence types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma, x:A, y:B \vdash \mathrm{toCorr}(e, x, y) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash 121\mathrm{witn}(e):\mathrm{isOneToOne}(\chi.\gamma.\mathrm{toCorr}(e))}$$

Computation rules for equivalence types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A, y:A \vdash R(x, y) \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isOneToOne}(\chi.\gamma.R)}{\Gamma, x:A, y:B \vdash \mathrm{toCorr}(\mathrm{toEquiv}_{\chi.\gamma.R}(p), x, y) \equiv R(x, y) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A, y:A \vdash R(x, y) \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isOneToOne}(\chi.\gamma.R)}{\Gamma \vdash 121\mathrm{witn}(\mathrm{toEquiv}_{\chi.\gamma.R}(p)) \equiv p:\mathrm{isOneToOne}(\chi.\gamma.R)}$$

Uniqueness rules for equivalence types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma, x:A, y:B \vdash \mathrm{toEquiv}_{\chi.\gamma.\mathrm{toCorr}(e)}(121\mathrm{witn}(e)) \equiv e:A \simeq B}$$

#### Half-adjoint equivalence types

A half-adjoint equivalence between types $A$ and $B$ is a record consisting of the following fields:

* a [[function]] $f:A \to B$

* a function $g:B \to A$

* a [[homotopy]] $G:\prod_{x:A} g(f(x)) =_{A} x$

* a homotopy $H:\prod_{y:B} f(g(y)) =_{B} y$

* a homotopy $K:\prod_{x:A} H(f(x)) =_{f(g(f(x)) =_{B} f(x)} \mathrm{ap}_f(f(g(x)), x, G(x))$ expressing the [[coherence law]] for equivalences, where $\mathrm{ap}_f(f(g(x)), x, G(x))$ is the [[function application to identifications|function application of $f$]] to the [[identification]] $G(x)$. 

Thus, the rules for half-adjoint equivalence types state that half-adjoint equivalence types are [[record types]] with the above fields:

Formation rules for half-adjoint equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \simeq B \; \mathrm{type}}$$

Introduction rules for half-adjoint equivalence types:
$$\frac{
\begin{array}{c}
\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash g:B \to A \\ 
\Gamma \vdash G:\prod_{x:A} g(f(x)) =_{A} x \quad \Gamma \vdash H:\prod_{y:B} f(g(y)) =_{B} y \\ 
\Gamma \vdash K:\prod_{x:A} H(f(x)) =_{f(g(f(x)) =_{B} f(x)} \mathrm{ap}_f(f(g(x)), x, G(x))
\end{array}
}{\Gamma \vdash \mathrm{toEquiv}(f, g, G, H, K):A \simeq B}$$

Elimination rules for half-adjoint equivalence types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{func}(e):A \to B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{finv}(e):B \to A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{sec}(e):\prod_{x:A} \mathrm{finv}(e)(\mathrm{func}(e)(x)) =_A x}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{ret}(e):\prod_{y:B} \mathrm{func}(e)(\mathrm{finv}(e)(y) =_{B} y}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{coh}(e):\prod_{x:A} H(f(x)) =_{f(g(f(x)) =_{B} f(x)} \mathrm{ap}_f(f(g(x)), x, G(x))}$$

Computation rules for half-adjoint equivalence types:

$$\frac{
\begin{array}{c}
\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash g:B \to A \\ 
\Gamma \vdash G:\prod_{x:A} g(f(x)) =_{A} x \quad \Gamma \vdash H:\prod_{y:B} f(g(y)) =_{B} y \\ 
\Gamma \vdash K:\prod_{x:A} H(f(x)) =_{f(g(f(x)) =_{B} f(x)} \mathrm{ap}_f(f(g(x)), x, G(x))
\end{array}
}{\Gamma \vdash \mathrm{func}(\mathrm{toEquiv}(f, g, G, H, K)) \equiv f:A \to B}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash g:B \to A \\ 
\Gamma \vdash G:\prod_{x:A} g(f(x)) =_{A} x \quad \Gamma \vdash H:\prod_{y:B} f(g(y)) =_{B} y \\ 
\Gamma \vdash K:\prod_{x:A} H(f(x)) =_{f(g(f(x)) =_{B} f(x)} \mathrm{ap}_f(f(g(x)), x, G(x))
\end{array}
}{\Gamma \vdash \mathrm{finv}(\mathrm{toEquiv}(f, g, G, H, K)) \equiv g:B \to A}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash g:B \to A \\ 
\Gamma \vdash G:\prod_{x:A} g(f(x)) =_{A} x \quad \Gamma \vdash H:\prod_{y:B} f(g(y)) =_{B} y \\ 
\Gamma \vdash K:\prod_{x:A} H(f(x)) =_{f(g(f(x)) =_{B} f(x)} \mathrm{ap}_f(f(g(x)), x, G(x))
\end{array}
}{\Gamma \vdash \mathrm{sec}(\mathrm{toEquiv}(f, g, G, H, K)) \equiv G:\prod_{x:A} g(f(x)) =_{A} x}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash g:B \to A \\ 
\Gamma \vdash G:\prod_{x:A} g(f(x)) =_{A} x \quad \Gamma \vdash H:\prod_{y:B} f(g(y)) =_{B} y \\ 
\Gamma \vdash K:\prod_{x:A} H(f(x)) =_{f(g(f(x)) =_{B} f(x)} \mathrm{ap}_f(f(g(x)), x, G(x))
\end{array}
}{\Gamma \vdash \mathrm{ret}(\mathrm{toEquiv}(f, g, G, H, K)) \equiv H:\prod_{y:B} f(g(y)) =_{B} y}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash g:B \to A \\ 
\Gamma \vdash G:\prod_{x:A} g(f(x)) =_{A} x \quad \Gamma \vdash H:\prod_{y:B} f(g(y)) =_{B} y \\ 
\Gamma \vdash K:\prod_{x:A} H(f(x)) =_{f(g(f(x)) =_{B} f(x)} \mathrm{ap}_f(f(g(x)), x, G(x))
\end{array}
}{\Gamma \vdash \mathrm{coh}(\mathrm{toEquiv}(f, g, G, H, K)) \equiv K:\prod_{x:A} H(f(x)) =_{f(g(f(x)) =_{B} f(x)} \mathrm{ap}_f(f(g(x)), x, G(x))}$$

Uniqueness rules for half-adjoint equivalence types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{toEquiv}(\mathrm{func}(e), \mathrm{finv}(e), \mathrm{sec}(e), \mathrm{ret}(e), \mathrm{coh}(e)) \equiv e:A \simeq B}$$

#### Bi-invertible function types

A bi-invertible function between types $A$ and $B$ is a record consisting of the following fields:

* a [[function]] $f:A \to B$

* a function $g:B \to A$

* a function $h:B \to A$

* a [[homotopy]] $G:\prod_{x:A} g(f(x)) =_{A} x$

* a homotopy $H:\prod_{y:B} f(h(y)) =_{B} y$

Thus, the rules for bi-invertible function types state that bi-invertible function types are [[record types]] with the above fields:

Formation rules for bi-invertible function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \simeq B \; \mathrm{type}}$$

Introduction rules for bi-invertible function types:
$$\frac{
\begin{array}{c}
\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash g:B \to A \quad \Gamma \vdash h:B \to A \\ 
\Gamma \vdash G:\prod_{x:A} g(f(x)) =_{A} x \quad \Gamma \vdash H:\prod_{y:B} f(h(y)) =_{B} y \\ 
\end{array}
}{\Gamma \vdash \mathrm{toEquiv}(f, g, h, G, H):A \simeq B}$$

Elimination rules for bi-invertible function types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{func}(e):A \to B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{fsec}(e):B \to A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{fret}(e):B \to A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{sec}(e):\prod_{x:A} \mathrm{finv}(e)(\mathrm{func}(e)(x)) =_A x}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{ret}(e):\prod_{y:B} \mathrm{func}(e)(\mathrm{finv}(e)(y) =_{B} y}$$

Computation rules for bi-invertible function types:

$$\frac{
\begin{array}{c}
\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash g:B \to A \quad \Gamma \vdash h:B \to A \\ 
\Gamma \vdash G:\prod_{x:A} g(f(x)) =_{A} x \quad \Gamma \vdash H:\prod_{y:B} f(h(y)) =_{B} y \\ 
\end{array}
}{\Gamma \vdash \mathrm{func}(\mathrm{toEquiv}(f, g, G, H, K)) \equiv f:A \to B}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash g:B \to A \quad \Gamma \vdash h:B \to A \\ 
\Gamma \vdash G:\prod_{x:A} g(f(x)) =_{A} x \quad \Gamma \vdash H:\prod_{y:B} f(h(y)) =_{B} y \\ 
\end{array}
}{\Gamma \vdash \mathrm{fsec}(\mathrm{toEquiv}(f, g, G, H, K)) \equiv g:B \to A}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash g:B \to A \quad \Gamma \vdash h:B \to A \\ 
\Gamma \vdash G:\prod_{x:A} g(f(x)) =_{A} x \quad \Gamma \vdash H:\prod_{y:B} f(h(y)) =_{B} y \\ 
\end{array}
}{\Gamma \vdash \mathrm{frec}(\mathrm{toEquiv}(f, g, G, H, K)) \equiv h:B \to A}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash g:B \to A \quad \Gamma \vdash h:B \to A \\ 
\Gamma \vdash G:\prod_{x:A} g(f(x)) =_{A} x \quad \Gamma \vdash H:\prod_{y:B} f(h(y)) =_{B} y \\ 
\end{array}
}{\Gamma \vdash \mathrm{sec}(\mathrm{toEquiv}(f, g, G, H, K)) \equiv G:\prod_{x:A} g(f(x)) =_{A} x}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash g:B \to A \quad \Gamma \vdash h:B \to A \\ 
\Gamma \vdash G:\prod_{x:A} g(f(x)) =_{A} x \quad \Gamma \vdash H:\prod_{y:B} f(h(y)) =_{B} y \\ 
\end{array}
}{\Gamma \vdash \mathrm{ret}(\mathrm{toEquiv}(f, g, G, H, K)) \equiv H:\prod_{y:B} f(h(y)) =_{B} y}$$

Uniqueness rules for bi-invertible function types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{toEquiv}(\mathrm{func}(e), \mathrm{fsec}(e), \mathrm{fret}(e), \mathrm{sec}(e), \mathrm{ret}(e)) \equiv e:A \simeq B}$$

## Properties

### Relation to interval types

Given types $A$ and $B$ and an equivalence $f:A \simeq B$, one could define the dependent type $x:\mathbb{I} \vdash C(x)$ indexed by the [[interval type]] $\mathbb{I}$ as $C(0) \equiv A$, $C(1) \equiv B$, and $\mathrm{tr}_C(0, 1, p) \equiv f$. 

### One-To-One correspondences

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

### Indexed heterogeneous identity types

Given the definition of the equivalence type as the type of encodings for one-to-one correspondences, the [[indexed heterogeneous identity type]] is defined by the rule 

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
