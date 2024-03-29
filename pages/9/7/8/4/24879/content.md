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

In this article we introduce a [[structural set theory]] consisting of four basic primitives, [[sets]], [[elements]], [[functions]], and [[relations]], as well as function evaluation, and relation holding, and structural versions of 9 of the 10 axioms of [[ZFC]] presented in the nLab article of [[ZFC]], making the set theory equivalent in strength to ZFC. We propose that [[structural ZFC]] is a suitable theory for [[practical foundations]], as the primitives and axioms are in alignment with the usage of such objects in mathematical practice, rather than coming with its own additional baggage. 

## Presentation

We work in a [[first-order logic]] with [[equality]]. In structural ZFC, there are four basic primitives:

* **[[sets]]** $A$

* for every set $A$, **[[elements]]** $a \in A$ (the membership $\in$ here is a typing [[judgment]], rather than a relation)

* for every set $A$ and $B$, **[[functions]]** $f:A \to B$ with **[[domain]]** $A$ and **[[codomain]]** $B$ (the function notation $f:A \to B$ here is a [[judgment]], rather than a relation)

* for every set $A$ and $B$, **[[relations]]** $\varphi:A \looparrowright B$ with **[[domain]]** $A$ and **[[codomain]]** $B$ (the relation notation $\varphi:A \looparrowright B$ here is a [[judgment]], rather than a relation)

In addition, 

* for every function $f:A \to B$ and element $a \in A$, one could form the element $f(a) \in B$; this operation is called **function evaluation**, 
* for every relation $\varphi:A \looparrowright B$ and element $a \in A$ and $b \in B$, one could form that $\varphi(a, b)$ **holds** of $a$ and $b$. 

The axioms of structural ZFC are as follows:

**Axiom 0A (Axiom of equality preservation):** _For all sets $A$ and $B$, functions $f:A \to B$, and elements $a \in A$ and $b \in A$, if $a = b$, then $f(a) = f(b)$. 

**Axiom 0B ([[axiom of unique choice|Axiom of unique choice]]):** _For all functions $f:A \to B$, there is a unique relation $\varphi:A \looparrowright B$ such that for all $a \in A$ and $b \in B$, $\varphi(a, b)$ iff $b = f(a)$, and for all relations $\varphi:A \looparrowright B$ such that for all $a \in A$, there is a unique $b \in B$ such that $\varphi(a, b)$ holds of $a$ and $b$, there is a function $f:A \to B$ such that $f(a) = b$._ 

A function $f:A \to B$ is an **[[injection]]** if for all elements $a \in A$ and $b \in A$, $a = b$ if and only if $f(a) = f(b)$. Injections are written as $f:A \hookrightarrow B$. 

**Axiom 1 ([[axiom of strong extensionality|Axiom of strong extensionality]]):** _Given sets $A$ and $B$ and an [[injection]] $i:A \hookrightarrow B$, the following statements are logically equivalent to each other:_ 

* _there exists a function $i^{-1}:B \to A$ such that for all elements $a \in A$ and $b \in B$, $i^{-1}(i(a)) = a$ and $i(i^{-1}(b)) = b$_
* _for every element $x \in B$ there exists an element $y \in A$ such that $i(y) = x$_ 

One uses the axiom of strong extensionality as the definition of a [[bijection]] between sets. 

**Axiom 2 (Axiom of [[empty set]]):** _There exists a set $\emptyset$ such that for every other set $A$, there is a unique relation $u_A^\emptyset:\emptyset \looparrowright A$._

**Axiom 3 (Axiom of [[Cartesian products]]):** _For every set $A$ and $B$, there exists a set $A \times B$ with a function $\pi_A:A \times B \to A$ and a function $\pi_B:A \times B \to B$ such that for every element $a \in A$ and $b \in B$ there is a unique element $(a, b) \in A \times B$, such that $\pi_A((a, b)) = a$ and $\pi_B((a, b)) = b$._

Given a set $I$, an $I$-indexed [[family of subsets]] is a relation $M:I \looparrowright A$ to a set $A$ called the **[[union]]** of $M$. 

**Axiom 4 (Axiom of [[indexed subsets]]):** _For every set $I$ and $I$-indexed family of subsets $M:I \looparrowright A$ with union $A$, and for every element $i \in I$, there exists a set $M_i$ and an injection $m:M_i \hookrightarrow A$, such that for every element $a \in M_i$, $M(i, m(a))$ holds for $i$ and $m(a)$, and for every other set $B$ with injection $f:B \hookrightarrow A$ such that for every element $b \in B$, $M(i, f(b))$ holds for $i$ and $f(b)$, there is a unique function $u_B^{M_i}:B \to M_i$ such that for every element $b \in B$, $f(b) = m(u_B^{M_i}(b))$._

**Axiom 5 ([[axiom schema of separation|Axiom schema of separation]]):** _For any set $B$ and any formula $\phi(x)$ with free variable $x \in B$, there exists a set $\{B \vert \phi\}$ with an injection $m:\{B \vert \phi\} \hookrightarrow B$ such that for every element $x \in B$, $\phi(x)$ holds if and only if there exists an element $y \in \{B \vert \phi\}$ such that $m(y) = x$._

**Axiom 6 ([[axiom schema of collection|Axiom schema of collection]]):** _For any set $A$ and formula $\phi(x, X)$ with free variables $x \in A$ and $X$, there exists a set $B$, function $p:B \to A$, and a $B$-indexed family of sets $M:B \looparrowright C$ with union $C$, such that for every $b \in B$, $\phi(p(b), M_b)$, and for every $a \in A$, if there exists a set $X$ with $\phi(a, X)$, then $a \in \mathrm{im}(p)$._

**Axiom 7 (Axiom of [[power sets]]):** _For any set $A$, there exists a set $\mathcal{P}(A)$ and a relation $(-)\in_A(-):A\looparrowright \mathcal{P}(A)$ such that for any set $B$ with injection $i:B \hookrightarrow A$, there exists a unique $b \in \mathcal{P}(A)$ such that for any $x \in A$, $x \in_A b$ holds of $x$ and $b$ if and only if there exists an element $y \in B$ such that $i(y) = x$._

**Axiom 8 (Axiom of [[natural numbers]]):** _There exists a set $\mathbb{N}$ with an element $0 \in \mathbb{N}$ and a function $s:\mathbb{N} \to \mathbb{N}$, such that for all sets $A$ with an element $0_A:A$ and function $s_A:A \to A$, there is a unique function $u_A^\mathbb{N}:\mathbb{N} \to A$ such that $u_A^\mathbb{N}(0) = 0_A$ and for all elements $n \in \mathbb{N}$, $u_A^\mathbb{N}(s(n)) = s_A(u_A^\mathbb{N}(n))$._ 

**Axiom 9 ([[axiom of choice|Axiom of choice]]):** _If $f:A \to B$ is a function such that for every element $x \in B$ there exists an element $y \in A$ such that $f(y) = x$, then there is a function $g:B \to A$ such that for all elements $x \in B$, $f(g(x)) = x$._ 

The structural version of the [[axiom of foundation]], the [[axiom of well-founded materialization]], states that every set can be embedded in some [[well-founded relation|well-founded]] [[extensional relation|extensional]] [[graph]]. This axiom follows from the [[axiom of choice]], and well-founded extensional graphs are not a fundamental concept in structural set theory, so it is not listed here as a separate axiom. 

## Making alternate primitive choices

One could choose to make either the relations or the functions a derived object of the other, leading to **categorical ZFC** and **allegorical ZFC** respectively. 

### Dependently-sorted categorical ZFC

Categorical ZFC follows [[ETCS with elements]] in taking [[functions]] to be fundamental and [[relations]] as defined. 

We work in a [[first-order logic]] with [[equality]]. In structural ZFC, there are three basic primitives:

* **[[sets]]** $A$

* for every set $A$, **[[elements]]** $a \in A$ (the membership $\in$ here is a typing [[judgment]], rather than a relation)

* for every set $A$ and $B$, **[[functions]]** $f:A \to B$ with **[[domain]]** $A$ and **[[codomain]]** $B$ (the function notation $f:A \to B$ here is a [[judgment]], rather than a relation)

In addition, for every function $f:A \to B$ and element $a \in A$, one could form the element $f(a) \in B$; this operation is called **function evaluation**. A relation between sets $A$ and $B$ is a set $R$ with an injection $(s, t):R \hookrightarrow A \times B$. 

### Three-sorted categorical ZFC

An alternate formulation of categorical ZFC three [[sorts]], one for [[sets]], [[elements]], and [[functions]], making structural ZFC into a [[three-sorted set theory]]. The membership $a \in A$ becomes a [[relation]] between the sort of elements and the sort of [[sets]], while the functional domain and codomain notation $f:A \to B$ also becomes a ternary relation between the sort of functions, and two copies of the sort of sets. There is a quinary relation $\mathrm{eval}(A, B, f, a, b)$ between all three sorts, which says that given sets $A$ and $B$, the function $f$ can be evaluated at element $a$ and the result of the evaluation is the element $b$, in the [[context]] of $\varphi:A \looparrowright B$, $a \in A$, and $b \in B$. 

### Dependently sorted allegorical ZFC

Allegorical ZFC follows [[SEAR]] in taking [[relations]] to be fundamental and [[functions]] as defined. 

We work in a [[first-order logic]] with [[equality]]. In structural ZFC, there are three basic primitives:

* **[[sets]]** $A$

* for every set $A$, **[[elements]]** $a \in A$ (the membership $\in$ here is a typing [[judgment]], rather than a relation)

* for every set $A$ and $B$, **[[relations]]** $\varphi:A \looparrowright B$ with **[[domain]]** $A$ and **[[codomain]]** $B$ (the relation notation $\varphi:A \looparrowright B$ here is a [[judgment]], rather than a relation)

In addition, for every relation $\varphi:A \looparrowright B$ and element $a \in A$, one could form the judgment that $\varphi(a, b)$ **holds**. A function is a relation $\varphi:A \looparrowright B$ such that for all $a \in A$, there is a unique element $b \in B$ such that $\varphi(a, b)$ holds, and $b$ is said to be the evaluation of $a$ at $\varphi$. 

### Three-sorted allegorical ZFC

An alternate formulation of allegorical ZFC uses three [[sorts]], one for [[sets]], [[elements]], and [[relations]], making SEAR into a [[three-sorted set theory]]. The membership $a \in A$ becomes a [[relation]] between the sort of elements and the sort of [[sets]], while the relational domain and codomain notation $\varphi:A \looparrowright B$ also becomes a ternary relation between the sort of relations, and two copies of the sort of sets. There is a quinary relation $\mathrm{holds}(A, B, \varphi, a, b)$ between all three sorts, which says that given sets $A$ and $B$, the relation $\varphi$ holds for element $a$ and $b$ in the [[context]] of $\varphi:A \looparrowright B$, $a \in A$, and $b \in B$. 

## See also

* [[ZFC]]

* [[SEAR]]

* [[ETCS with elements]]

## References

The axiom of well-founded materialization, the structural axiom of extensionality (the strong terminal generator condition of well-pointedness), and the structural axiom schemata of separation and collection could be found in:

* [[Michael Shulman]] (2018). Comparing material and structural set theories. [arXiv:1808.05204](https://arxiv.org/abs/1808.05204).

The rest of the axioms are standard axioms from categorical set theory (or the type theoretic equivalent). 

[[!redirects structural ZFC]]

[[!redirects dependently sorted structural ZFC]]
[[!redirects dependently-sorted structural ZFC]]
[[!redirects four sorted structural ZFC]]
[[!redirects four-sorted structural ZFC]]
[[!redirects three sorted structural ZFC]]
[[!redirects three-sorted structural ZFC]]

[[!redirects categorical ZFC]]
[[!redirects dependently sorted categorical ZFC]]
[[!redirects dependently-sorted categorical ZFC]]
[[!redirects three sorted categorical ZFC]]
[[!redirects three-sorted categorical ZFC]]

[[!redirects allegorical ZFC]]
[[!redirects dependently sorted allegorical ZFC]]
[[!redirects dependently-sorted allegorical ZFC]]
[[!redirects three sorted allegorical ZFC]]
[[!redirects three-sorted allegorical ZFC]]