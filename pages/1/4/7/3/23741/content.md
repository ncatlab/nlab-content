[[!redirects Euclidean rings]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

In the same vein that [[commutative rings]] are to [[integral domains]] and [[GCD rings]] are to [[GCD domains]], [[Euclidean rings]] are to [[Euclidean domains]].

## Definition ##

A **Euclidean ring** is a [[commutative ring]] $R$ for which there exists a [[function]] $d \colon \mathrm{Can}(R) \to \mathbb{N}$ from the [[multiplicative submonoid of cancellative elements]] in $R$ to the [[natural numbers]], often called a *degree function*, such that for all $f \in R$ and $g \in \mathrm{Can}(R)$, there exist $q, r \in R$ such that $f = q \cdot g + r$ and either $r = 0$ or $d(r) \lt d(g)$. There is no uniqueness requirement for $q, r$. 

One could posit, instead of the [[property]] that for all $f \in R$ and $g \in \mathrm{Can}(R)$, there exist $q, r \in R$ such that $f = q \cdot g + r$ and either $r = 0$ or $d(r) \lt d(g)$; that the commutative ring has the [[structure]] of a function $(-)\div(-):R \times \mathrm{Can}(R) \to R$ called the *[[division]] function*, and a function $(-)\ \%\ (-):R \times \mathrm{Can}(R) \to R$ called the *remainder function*, such that for all $f \in R$ and $g \in \mathrm{Can}(R)$, $f = (f \div g) \cdot g + (f\ \%\ g)$ and either $f\ \%\ g = 0$ or $d(f\ \%\ g) \lt d(g)$. There might be multiple such division and remainder functions for the commutative ring $R$. 

One could also add the requirement that $d(a) \leq d(a b)$ for all nonzero $a, b$. There is no loss of generality in assuming it; every Euclidean ring admits such a degree function $d'$, defining $d'(a) = \min \{d(a b): b \in \mathrm{Can}(R)\}$. 

### In constructive mathematics ###

The definition of the Euclidean ring bifurcates in [[constructive mathematics]] due to the disjunctive condition, which could be represented as $(r = 0) \vee (d(r) \lt d(g))$ or as the weaker [[double negation]] $\not((r \neq 0) \wedge (d(r) \geq d(g)))$ in constructive mathematics, or equivalently, as either $(f\ \%\ g = 0) \vee (d(f\ \%\ g) \lt d(g))$ or the weaker $(\not(f\ \%\ g \neq 0) \vee (d(f\ \%\ g) \geq d(g))$. 

## Properties ##

Every Euclidean ring is a [[Bézout ring]], and every [[prefield]] is an Euclidean ring.  

## Examples ##

* The [[integers]] $\mathbb{Z}$ are a Euclidean ring. 

* A classical Euclidean domain $A$ is a Euclidean ring where $\mathrm{Can}(A)$ is the multiplicative monoid of elements not equal to zero (where inequality is [[denial inequality]])

$$\mathrm{Can}(A) \cong \{x \in A \vert x \neq 0\}$$

* A Heyting Euclidean domain $A$ is a Euclidean ring where $\mathrm{Can}(A)$ is the multiplicative monoid of elements apart from zero

$$\mathrm{Can}(A) \cong \{x \in A \vert x \# 0\}$$

* An ordered Euclidean domain $A$ is a Euclidean ring where $\mathrm{Can}(A)$ is the multiplicative monoid of elements with a positive absolute value

$$\mathrm{Can}(A) \cong \{x \in A \vert 0 \lt \vert x \vert\}$$

* The [[trivial ring]] $0$ is the unique Euclidean ring up to unique [[isomorphism]] such that $0 \in \mathrm{Can}(0)$. The [[trivial ring]] is also the [[terminal object|terminal]] Euclidean ring. 

## See also ##

* [[commutative ring]]

* [[Bézout ring]]

* [[GCD ring]]

* [[prefield]]

* [[Euclidean domain]]