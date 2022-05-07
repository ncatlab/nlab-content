[[!redirects inverse rings]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

In the same vein that [[commutative rings]] are to [[integral domains]] and [[GCD rings]] are to [[GCD domains]], [[inverse rings]] are to [[fields]]. 

## Definition ##

Let $F:CRing \to CMon$ be the [[forgetful functor]] from [[CRing]] to [[CMon]] that only remember the multiplicative monoid structure of commutative rings. Given a [[commutative ring]] $R$, let us define the [[cancellative monoid]] $\mathrm{Can}(R)$ as the cancellative [[submonoid]] of the multiplicative monoid $F(R)$ such that every other cancellative submonoid $S$ of $F(R)$ is a cancellative submonoid of $\mathrm{Can}(R)$. 

\begin{definition}
A commutative ring $R$ is a **inverse ring** if $\mathrm{Can}(R)$ is the [[group]] of [[units]] $R^\times$. 
\end{definition}

## Examples ##

* The [[rational numbers]] $\mathbb{Q}$ are a inverse ring. 

* A classical field $F$ is a inverse ring where $\mathrm{Can}(F)$ and $F^\times$ are the multiplicative monoid of elements not equal to zero (where inequality is [[denial inequality]])

$$\mathrm{Can}(F) \cong F^\times \cong \{x \in F \vert x \neq 0\}$$

* A [[Heyting field]] $F$ is a inverse ring where $\mathrm{Can}(F)$ and $F^\times$ are the multiplicative monoid of elements apart from zero

$$\mathrm{Can}(F) \cong F^\times \cong \{x \in F \vert x \# 0\}$$

* An [[ordered field]] $F$ is a inverse ring where $\mathrm{Can}(F)$ and $F^\times$ are the multiplicative monoid of elements with a positive absolute value

$$\mathrm{Can}(F) \cong F^\times \cong \{x \in F \vert 0 \lt \vert x \vert\}$$

* The [[trivial ring]] $0$ is the unique inverse ring up to unique isomorphism such that $\mathrm{Can}(0)$ and $0^\times$ are $F(0)$, where $F:CRing \to CMon$ be the [[forgetful functor]] from [[CRing]] to [[CMon]] that only remember the multiplicative monoid structure of commutative rings. The trivial ring is also the terminal inverse ring. 

* Non-example: the [[integers]] $\mathbb{Z}$ are not a inverse ring, because $\mathrm{Can}(\mathbb{Z})$ is not $\mathbb{Z}^\times$. 

## See also ##

* [[commutative ring]]

* [[GCD ring]]

* [[field]]