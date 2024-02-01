
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### (0,1)-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

A notion of [[ordered ring]] for [[strict weak orders]]. 

## Definition

### With an order relation

A strictly weakly ordered ring is an [[ring]] $R$ with a [[strict weak order]] $\lt$ such that 

* $0 \lt 1$

* for all $a \in R$ and $b \in R$, $0 \lt a$ and $0 \lt b$ implies that $0 \lt a + b$; alternatively, $0 \lt a + b$ implies that $0 \lt a$ or $0 \lt b$. 

* for all $a \in R$ and $b \in R$, if $0 \lt a$ and $0 \lt b$, then $0 \lt a \cdot b$

We define the predicate $\mathrm{isPositive}$ as 

$$\mathrm{isPositive}(a) \coloneqq 0 \lt a$$

### With a positivity predicate

Let $R$ be a [[commutative ring]]. $R$ is an **pseudo-ordered ring** if there is a [[predicate]] $\mathrm{isPositive}$ stating an element $a$ is positive, such that 

* 0 is not positive
* given element $a \in R$, if $a$ is positive, then $-a$ is not positive
* given elements $a \in R$ and $b \in R$; if $a$ is positive, then either $b$ is positive or $a - b$ is positive
* 1 is positive
* given elements $a \in R$ and $b \in R$, if $a$ is positive and $b$ is positive, $a + b$ is positive; alternatively, $a + b$ being positive implies that $a$ is positive or $b$ is positive. 
* given elements $a \in R$ and $b \in R$, if $a$ is positive and $b$ is positive, $a \cdot b$ is positive

We define the order relation $\lt$ as 

$$a \lt b \coloneqq \mathrm{isPositive}(b - a)$$

## Properties

Every strictly weakly ordered ring is a [[preordered ring]] given by the [[negation]] of the strict weak order. In the presence of [[excluded middle]], every strictly weakly ordered ring is a [[total order|totally preordered]] ring. 

## Examples

* Every [[pseudo-ordered ring]] is a strictly weakly ordered ring. 

* Every [[ordered local ring]] is a strictly weakly ordered ring where every element greater than zero or less than zero is invertible.

* In particular, the set of [[Cauchy sequences]] of [[rational numbers]] is a strictly weakly ordered ring. 

* Every [[ordered Kock field]] is a example of a strictly weakly ordered ring which in the presence of [[excluded middle]] is a [[linearly ordered ring]]. 

## See also

* [[ordered local ring]]

* [[ordered Kock field]]

[[!redirects strictly weakly ordered ring]]
[[!redirects strictly weakly ordered rings]]