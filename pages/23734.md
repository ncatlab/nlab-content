[[!redirects prefields]]

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

In the same vein that [[commutative rings]] are to [[integral domains]] and [[GCD rings]] are to [[GCD domains]], [[prefields]] are to [[fields]]. 

## Definition ##

A commutative ring $R$ is a **prefield** if there exists a function $(-)^{-1}: \mathrm{Can}(R) \to R$ from the [[multiplicative submonoid of cancellative elements]] in $R$ to $R$ itself, often called the *multiplicative inverse* or *reciprocal*, such that for all $e \in \mathrm{Can}(R)$, $e \cdot e^{-1} = 1$ and $e^{-1} \cdot e = 1$. 

Thus, in an prefield, $\mathrm{Can}(R)$ and the [[group of units]] $R^\times$ coincide. 

## Examples ##

* The [[rational numbers]] $\mathbb{Q}$ are a prefield. 

* A classical field $F$ is a prefield where $\mathrm{Can}(F)$ is the multiplicative monoid of elements not equal to zero (where inequality is [[denial inequality]])

$$\mathrm{Can}(F) \cong \{x \in F \vert x \neq 0\}$$

* A [[Heyting field]] $F$ is a prefield where $\mathrm{Can}(F)$ is the multiplicative monoid of elements apart from zero

$$\mathrm{Can}(F) \cong \{x \in F \vert x \# 0\}$$

* An [[ordered field]] $F$ is a prefield where $\mathrm{Can}(F)$ is the multiplicative monoid of elements with a positive absolute value

$$\mathrm{Can}(F) \cong \{x \in F \vert 0 \lt \vert x \vert\}$$

* The [[trivial ring]] $0$ is the unique prefield up to unique isomorphism such that $0 \in \mathrm{Can}(0)$. The trivial ring is also the terminal prefield. 

* The [[cyclic ring]] $\mathbb{Z}/4\mathbb{Z}$ is a prefield, because $2 \in \mathbb{Z}/4\mathbb{Z}$ is not cancellative: $2 \cdot 2 = 0$ and $2 \cdot 0 = 0$, but $2 \neq 0$, and thus, $\mathrm{Can}(\mathbb{Z}/4\mathbb{Z})$ is the same as the group of units $\{1, 3\}$. 

* Non-example: the [[integers]] $\mathbb{Z}$ are not a prefield. 

## See also ##

* [[commutative ring]]

* [[GCD ring]]

* [[Bézout ring]]

* [[Euclidean ring]]

* [[prefield of fractions]]

* [[prevector space]]

* [[field]]