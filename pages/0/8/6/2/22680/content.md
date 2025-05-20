+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Absorption monoids are the [[monoid objects]] in [[pointed sets]], in the same way that [[rings]] are the [[monoid objects]] in [[abelian groups]]. Thus, the theory of absorption monoids and the theory of rings are very similar to each other, except that rings have additive structure whereas absorption monoids do not have additive structure. 

## Definition

An __absorption monoid__ or __annihilation monoid__ is a [[monoid]] $(M,1,\cdot)$ that is also an [[absorption magma]] $(M,0)$. 

Equivalently, it is a [[monoid object]] in the [[category]] of [[pointed sets]], since left and right multiplication $\cdot$ by any element $x$ preserves the point $0$. 

## Properties

### Initial and terminal absorption monoids

The [[initial object|initial]] absorption monoid is the [[boolean domain]] $\mathbb{2}$ with elements $0 \in \mathbb{2}$ representing [[false]], $1 \in \mathbb{2}$ representing [[true]], and $(-)\cdot(-):\mathbb{2} \times \mathbb{2} \to \mathbb{2}$ representing [[conjunction]]. 

The [[terminal object|terminal]] absorption monoid is the [[trivial monoid]] $\mathbb{1}$, the monoid whose underlying [[set]] is a [[singleton]]. The trivial monoid is also [[strictly terminal]]. 

### Absorption monoid homomorphisms

Given absorption monoids $M$ and $N$, an absorption monoid homomorphism is a function $h:M \to N$ such that 

* $h(0) = 0$
* $h(1) = 1$
* for all $a \in M$ and $b \in M$, $h(a \cdot b) = h(a) \cdot h(b)$.

### Ideals and anti-ideals

A two-sided [[ideal]] of an absorption monoid $M$ is a subset $I$ of $M$ such that 

* $0 \in I$
* for all elements $a \in M$ and $b \in M$, if $a \cdot b \in I$, then either $a \in I$ or $b \in I$. 

A two-sided anti-ideal of an absorption monoid $M$ is a subset $A$ of $M$ such that 

* $0 \notin I$ 
* for all elements $a \in M$ and $b \in M$, if $a \in I$ and $b \in I$, then $a \cdot b \in I$. 

### Quotient absorption monoids

Given an absorption monoid $M$ and a two-sided ideal $I$, the quotient of $M$ by $I$ is the [[initial object|initial]] absorption monoid $M/I$ with absorption monoid homomorphism $i:M \to M/I$ such that for all elements $a \in I$, $i(a) = 0$. 

### Invertible elements

An element $a \in M$ is an **invertible element** or a **unit** if there exists an element $b \in M$ such that $a \cdot b = 1$ and $b \cdot a = 1$. 

The set of invertible elements $M^\times$ in an absorption monoid $M$ is always closed under multiplication; i.e. $M^\times$ is a [[submonoid]] of $M$. In fact, since every element is invertible, $M^\times$ forms a [[subgroup]] of $M$, called the [[group of units]]. 

### Division monoids

An absorption monoid $M$ is a [[division monoid]] if every non-invertible element in $M$ is equal to zero. $M$ is Heyting if there is a [[tight apartness relation]] on $M$ such that every invertible element is apart from zero, and $M$ is discrete if every element in $M$ is either zero or invertible. 

### Regular elements

An element $a \in M$ is a **regular element**, **cancellative element**, or **cancellable element** if for all elements $b \in M$ and $c \in M$, $b = c$ if and only if $a \cdot b = a \cdot c$ and $c \cdot a = c \cdot b$. 

The set of regular elements $\mathrm{Reg}(M)$ in an absorption monoid $M$ is always closed under multiplication; i.e. $\mathrm{Reg}(M)$ is a [[submonoid]] of $M$. 

### Integral monoids

An absorption monoid $M$ is an [[integral monoid]] if every non-regular element in $M$ is equal to zero. $M$ is Heyting if there is a [[tight apartness relation]] on $M$ such that every regular element is apart from zero, and $M$ is discrete if every element in $M$ is either zero or regular. 

### Ore sets and Ore absorption monoids

Given an absorption monoid $M$, an [[Ore set]] is a [[submonoid]] $S$ of $\mathrm{Reg}(M)$ such that every element of $S$ satisfies the left and right Ore conditions:

* for all $a \in S$ and $b \in M$, there exists $c \in S$ and $d \in M$ such that $a \cdot d = b \cdot c$
* for all $a \in S$ and $b \in M$, there exists $c \in S$ and $d \in M$ such that $d \cdot a = c \cdot b$

A absorption monoid is an Ore absorption monoid if $\mathrm{Reg}(M)$ is an Ore set. 

### Localization and group completion

The localization of an Ore integral monoid $M$ at $\mathrm{Reg}(M)$ is a [[division monoid]]. The [[localization of a monoid|localization]] of an absorption monoid at $0$ is the [[trivial group]]; thus, the [[group completion]] of any absorption monoid is the [[trivial group]]. 

### Actions and modules

Given an absorption monoid $M$, an left $M$-action on a pointed set $(P, 0)$ is an ternary function $\alpha_L:M \times P \to P$ such that: 

* for all elements $p \in P$, $\alpha_L(1, p) = p$
* for all elements $a \in M$, $b \in M$, and $c \in P$, $\alpha_L(a, \alpha_L(b, c)) = \alpha_L(a \cdot b, c)$
* for all elements $p \in P$, $\alpha_L(0, p) = 0$
* for all elements $a \in M$, $\alpha_L(a, 0) = 0$

A right $M$-action on a pointed set $(P, 0)$ is a binary function $\alpha_R:P \times M \to P$ such that: 

* for all elements $p \in P$, $\alpha_R(p, 1) = p$
* for all elements $a \in M$, $b \in M$, and $c \in P$, $\alpha_R(\alpha_R(c, a), b) = \alpha_R(c, a \cdot b)$
* for all elements $p \in P$, $\alpha_R(p, 0) = 0$
* for all elements $a \in M$, $\alpha_R(0, a) = 0$

Given absorption monoids $M$ and $N$, an $M$-$N$-[[biaction]] on a pointed set $(P, 0)$ is a ternary function $\alpha:M \times P \times N \to P$ such that: 

* for all elements $p \in P$, $\alpha(1, p, 1) = p$
* for all elements $a \in M$, $b \in M$, $c \in P$, $d \in N$, $e \in N$, $\alpha(a, \alpha(b, c, d), e) = \alpha_L(a \cdot b, c, d \cdot e)$
* for all elements $p \in P$ and $d \in N$, $\alpha_L(0, p, d) = 0$
* for all elements $a \in M$ and $d \in N$, $\alpha_L(a, 0, d) = 0$
* for all elements $a \in M$ and $p \in P$, $\alpha_L(a, p, 0) = 0$

Pointed sets equipped with left or right $M$-actions are called left or right $M$-[[module object|modules]], and pointed sets equipped with $M$-$N$-biactions are called $M$-$N$-[[bimodule object|bimodules]]. 

## Examples

### The multiplicative monoid of the natural numbers

The multiplicative monoid of the natural numbers $\mathbb{N}^\times$ is the [[free object|free]] commutative absorption monoid on the natural numbers, the [[initial object|initial]] commutative absorption monoid $\mathbb{N}^\times$ with a function $\mathrm{prime}:\mathbb{N} \to \mathbb{N}^\times$. $\mathbb{N}^\times$ has [[decidable equality]]. The localization of $\mathbb{N}^\times$ at the image of $\mathrm{prime}$, or equivalently at the non-zero elements of $\mathbb{N}^\times$, is the multiplicative monoid of the non-negative rational numbers, $\mathbb{Q}_{\geq 0}^\times$. 

### Other examples

* The [[extended natural numbers]] $(\bar{\mathbb{N}}, 0, +, \infty)$ are an absorption monoid. 

* Every [[integral monoid]] is an absorption monoid.

* The multiplicative monoid of every [[rig]] is an absorption monoid. 

* Every [[01-bounded semilattice]] is an abosrption [[semilattice]]. 

## Related concepts

* [[monoid]]

* [[integral monoid]]

* [[zero divisor]]

* [[rig]], [[ring]], [[lattice]], [[field]]

[[!include oidification - table]]

[[!redirects absorption monoids]]
[[!redirects annihilation monoid]]
[[!redirects annihilation monoids]]

[[!redirects absorbing element]]
[[!redirects absorbing elements]]
[[!redirects annihilating element]]
[[!redirects annihilating elements]]

[[!redirects absorption law]]
[[!redirects absorption laws]]