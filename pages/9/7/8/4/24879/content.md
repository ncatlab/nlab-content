+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Idea

In this article we introduce a [[structural set theory]] consisting of three basic primitives, [[sets]], [[elements]], and [[functions]], as well as function evaluation, and structural versions of the 10 axioms of [[ZFC]] presented in the nLab article of [[ZFC]], making the set theory equivalent in strength to ZFC. 

## Presentation

### As a simply sorted first-order theory

We work in a [[first-order logic]] with [[equality]]. In structural ZFC, there are three basic primitives, **[[sets]]** $A$, **[[elements]]** $a$, and **[[functions]]** $f$. In addition, there is

* A **[[membership relation]]** $a \in A$ between elements $a$ and sets $A$ which says that element $a$ is in the set $A$

* A ternary relation $f:A \to B$ between functions $f$ and sets $A$ and $B$ which says that function $f$ has **[[domain]]** $A$ and **[[codomain]]** $B$. 

* An quinary relation $\mathrm{ev}(A, B, a, b, f)$ which states that for every set $A$ and $B$, element $a$ and $b$, and $f$, if $a \in A$, $b \in B$ and $f:A \to B$, then $f$ can be evaluated at $a$, and its result is $b$. $b$ is usually written as $f(a)$. 

The axioms of structural ZFC are as follows:

**Axiom 0 (axiom of equality preservation):** _For all sets $A$ and $B$, functions $f:A \to B$, and elements $a \in A$ and $b \in A$, if $a = b$, then $f(a) = f(b)$. 

A function $f:A \to B$ is an **[[injection]]** if for all elements $a \in A$ and $b \in A$, $a = b$ if and only if $f(a) = f(b)$. We define the ternary relation $f:A \hookrightarrow B$ which states that $f$ is an injection with domain $A$ and codomain $B$:
$$f:A \hookrightarrow B \coloneqq f:A \to B \wedge \forall a \in A.\forall b \in A.(a = b) \iff (f(a) = f(b))$$

**Axiom 1 ([[axiom of strong extensionality|Axiom of strong extensionality]]):** _Given sets $A$ and $B$ and an [[injection]] $i:A \hookrightarrow B$, the following statements are logically equivalent to each other:_ 

* _there exists a function $i^{-1}:B \to A$ such that for all elements $a \in A$ and $b \in B$, $i^{-1}(i(a)) = a$ and $i(i^{-1}(b)) = b$_
* _for every element $x \in B$ there exists an element $y \in A$ such that $i(y) = x$_ 

One uses the axiom of strong extensionality as the definition of a [[bijection]] between sets. 

**Axiom 2 (Axiom of [[empty set]]):** _There exists a set $\emptyset$ such that for every other set $A$, there is a unique function $u_A^\emptyset:\emptyset \to A$._

**Axiom 3 (Axiom of [[Cartesian products]]):** _For every set $A$ and $B$, there exists a set $A \times B$ with a function $\pi_A:A \times B \to A$ and a function $\pi_B:A \times B \to B$ such that for every element $a \in A$ and $b \in B$ there is a unique element $(a, b) \in A \times B$, such that $\pi_A((a, b)) = a$ and $\pi_B((a, b)) = b$._

**Axiom 4 (Axiom of [[fibers]]):** _For every set $A$ and $B$, function $f:A \to B$, and element $b \in B$, there exists a set $f^{*}(b)$ and a function $i:f^{*}(b) \to A$, such that for every element $a \in f^{*}(b)$, $f(i(a)) = b$, and for every other set $C$ and function $g:C \to A$ such that for every element $c \in C$, $f(g(c)) = b$, there is a unique function $u_C^{f^{*}(b)}:C \to f^{*}(b)$ such that for every element $c \in C$, $g(c) = i(u_C^{f^{*}(b)}(c))$._

**Axiom 5 ([[axiom schema of separation|Axiom schema of separation]]):** _For any formula $\phi(x)$ with element free variable $x$ and for any set $B$ such that $x \in B$, there exists a set $\{B \vert \phi\}$ with an injection $m:\{B \vert \phi\} \hookrightarrow B$ such that for every element $x \in B$, $\phi(x)$ holds if and only if there exists an element $y \in \{B \vert \phi\}$ such that $m(y) = x$._

**Axiom 6 ([[axiom schema of collection|Axiom schema of collection]]):** _For any formula $\phi(x, X)$ with element free variable $x$ and set free variable $X$ and for any set $A$ such that $x \in A$, there exists a set $B$, function $p:B \to A$, set $C$ and function $M:C \to B$ such that for every $b \in B$, $\phi(p(b), M^{*}(b))$, and for every $a \in A$, if there exists a set $X$ with $\phi(a, X)$, then $a \in \mathrm{im}(p)$._

**Axiom 7 (Axiom of [[power sets]]):** _For every set $A$ there exists a set $\mathcal{P}(A)$ with a set $\in_A$ and an injection $i_{\in_A}:\in_A \hookrightarrow A \times \mathcal{P}(A)$ such that for every set $B$ and $R$ with an injection $i:R \hookrightarrow A \times B$, there exists a unique function $\chi_R:B \to \mathcal{P}(A)$ and a unique function $u_R^{\in_A}:R \to \in_A$ such that for all elements $r \in R$, $\pi_A(i(r)) = \pi_A(i_{\in_A}(u_R^{\in_A}(r)))$ and $\chi_R(\pi_B(i(r))) = \pi_{\mathcal{P}(A)}(i_{\in_A}(u_R^{\in_A}(r))$._

**Axiom 8 (Axiom of [[natural numbers]]):** _There exists a set $\mathbb{N}$ with an element $0 \in \mathbb{N}$ and a function $s:\mathbb{N} \to \mathbb{N}$, such that for all sets $A$ with an element $0_A:A$ and function $s_A:A \to A$, there is a unique function $u_A^\mathbb{N}:\mathbb{N} \to A$ such that $u_A^\mathbb{N}(0) = 0_A$ and for all elements $n \in \mathbb{N}$, $u_A^\mathbb{N}(s(n)) = s_A(u_A^\mathbb{N}(n))$._ 

**Axiom 9 ([[axiom of choice|Axiom of choice]]):** _If $f:A \to B$ is a function such that for every element $x \in B$ there exists an element $y \in A$ such that $f(y) = x$, then there is a function $g:B \to A$ such that for all elements $x \in B$, $f(g(x)) = x$._ 

**Axiom 10 ([[axiom of well-founded materialization|Axiom of well-founded materialization]]):** _Every set can be embedded in some well-founded extensional graph._ 

### As a dependently sorted first-order theory

We work in a [[first-order logic]] with [[equality]]. In structural ZFC, there are three basic primitives:

* **[[sets]]** $A$

* for every set $A$, **[[elements]]** $a \in A$ (the membership $\in$ here is a typing [[judgment]], rather than a relation)

* for every set $A$ and $B$, **[[functions]]** $f:A \to B$ with **[[domain]]** $A$ and **[[codomain]]** $B$ (the function notation $f:A \to B$ here is a [[judgment]], rather than a relation)

In addition, for every function $f:A \to B$ and element $a \in A$, one could form the element $f(a) \in B$; this operation is called **function evaluation**. 

The axioms of structural ZFC are as follows:

**Axiom 0 (axiom of equality preservation):** _For all sets $A$ and $B$, functions $f:A \to B$, and elements $a \in A$ and $b \in A$, if $a = b$, then $f(a) = f(b)$. 

A function $f:A \to B$ is an **[[injection]]** if for all elements $a \in A$ and $b \in A$, $a = b$ if and only if $f(a) = f(b)$. Injections are written as $f:A \hookrightarrow B$. 

**Axiom 1 ([[axiom of strong extensionality|Axiom of strong extensionality]]):** _Given sets $A$ and $B$ and an [[injection]] $i:A \hookrightarrow B$, the following statements are logically equivalent to each other:_ 

* _there exists a function $i^{-1}:B \to A$ such that for all elements $a \in A$ and $b \in B$, $i^{-1}(i(a)) = a$ and $i(i^{-1}(b)) = b$_
* _for every element $x \in B$ there exists an element $y \in A$ such that $i(y) = x$_ 

One uses the axiom of strong extensionality as the definition of a [[bijection]] between sets. 

**Axiom 2 (Axiom of [[empty set]]):** _There exists a set $\emptyset$ such that for every other set $A$, there is a unique function $u_A^\emptyset:\emptyset \to A$._

**Axiom 3 (Axiom of [[Cartesian products]]):** _For every set $A$ and $B$, there exists a set $A \times B$ with a function $\pi_A:A \times B \to A$ and a function $\pi_B:A \times B \to B$ such that for every element $a \in A$ and $b \in B$ there is a unique element $(a, b) \in A \times B$, such that $\pi_A((a, b)) = a$ and $\pi_B((a, b)) = b$._

**Axiom 4 (Axiom of [[fibers]]):** _For every set $A$ and $B$, function $f:A \to B$, and element $b \in B$, there exists a set $f^{*}(b)$ and a function $i:f^{*}(b) \to A$, such that for every element $a \in f^{*}(b)$, $f(i(a)) = b$, and for every other set $C$ and function $g:C \to A$ such that for every element $c \in C$, $f(g(c)) = b$, there is a unique function $u_C^{f^{*}(b)}:C \to f^{*}(b)$ such that for every element $c \in C$, $g(c) = i(u_C^{f^{*}(b)}(c))$._

**Axiom 5 ([[axiom schema of separation|Axiom schema of separation]]):** _For any set $B$ and any formula $\phi(x)$ with free variable $x \in B$, there exists a set $\{B \vert \phi\}$ with an injection $m:\{B \vert \phi\} \hookrightarrow B$ such that for every element $x \in B$, $\phi(x)$ holds if and only if there exists an element $y \in \{B \vert \phi\}$ such that $m(y) = x$._

**Axiom 6 ([[axiom schema of collection|Axiom schema of collection]]):** _For any set $A$ and formula $\phi(x, X)$ with free variables $x \in A$ and $X$, there exists a set $B$, function $p:B \to A$, set $C$ and function $M:C \to B$ such that for every $b \in B$, $\phi(p(b), M^{*}(b))$, and for every $a \in A$, if there exists a set $X$ with $\phi(a, X)$, then $a \in \mathrm{im}(p)$._

**Axiom 7 (Axiom of [[power sets]]):** _For every set $A$ there exists a set $\mathcal{P}(A)$ with a set $\in_A$ and an injection $i_{\in_A}:\in_A \hookrightarrow A \times \mathcal{P}(A)$ such that for every set $B$ and $R$ with an injection $i:R \hookrightarrow A \times B$, there exists a unique function $\chi_R:B \to \mathcal{P}(A)$ and a unique function $u_R^{\in_A}:R \to \in_A$ such that for all elements $r \in R$, $\pi_A(i(r)) = \pi_A(i_{\in_A}(u_R^{\in_A}(r)))$ and $\chi_R(\pi_B(i(r))) = \pi_{\mathcal{P}(A)}(i_{\in_A}(u_R^{\in_A}(r))$._

**Axiom 8 (Axiom of [[natural numbers]]):** _There exists a set $\mathbb{N}$ with an element $0 \in \mathbb{N}$ and a function $s:\mathbb{N} \to \mathbb{N}$, such that for all sets $A$ with an element $0_A:A$ and function $s_A:A \to A$, there is a unique function $u_A^\mathbb{N}:\mathbb{N} \to A$ such that $u_A^\mathbb{N}(0) = 0_A$ and for all elements $n \in \mathbb{N}$, $u_A^\mathbb{N}(s(n)) = s_A(u_A^\mathbb{N}(n))$._ 

**Axiom 9 ([[axiom of choice|Axiom of choice]]):** _If $f:A \to B$ is a function such that for every element $x \in B$ there exists an element $y \in A$ such that $f(y) = x$, then there is a function $g:B \to A$ such that for all elements $x \in B$, $f(g(x)) = x$._ 

**Axiom 10 ([[axiom of well-founded materialization|Axiom of well-founded materialization]]):** _Every set can be embedded in some well-founded extensional graph._ 

## See also

* [[ZFC]]

* [[SEAR]]

* [[ETCS with elements]]

## References

The axiom of well-founded materialization, the structural axiom of extensionality (the strong terminal generator condition of well-pointedness), and the structural axiom schemata of separation and collection could be found in:

* [[Michael Shulman]] (2018). Comparing material and structural set theories. [arXiv:1808.05204](https://arxiv.org/abs/1808.05204).

The rest of the axioms are standard axioms from categorical set theory (or the type theoretic equivalent). 