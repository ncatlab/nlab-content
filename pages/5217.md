# Ordered fields
* table of contents
{: toc}

## Idea

An ordered field is a [[field]] equipped with a compatible [[linear order]].

Note that while the adjective 'ordered' usually refers to a [[partial order]], it is traditionally used more strictly when placed before 'field'.


## Definition

### With linear order
An __ordered field__ is a [[field]] $K$ equipped with a [[linear order]] $\lt$ such that:

*  $1 \gt 0$,
*  If $a, b \gt 0$, then so are $a + b$ and $a b$.

One often sees the definition using a [[total order]] $\leq$ instead of the linear order $\lt$.  This makes no difference in [[classical mathematics]], but we need to use linear orders in [[constructive mathematics]] if we wish to have the usual examples. 

### With a positivity predicate

An ordered field is a [[field]] with a [[predicate]] $\mathrm{isPositive}$ such that 

* zero is not positive: 

$$\not \mathrm{isPositive}(0)$$

* one is positive: 

$$\mathrm{isPositive}(1)$$

* for every element $a:A$, if $a$ is not positive and $-a$ is not positive, then $a = 0$

$$\forall a:A.\neg\mathrm{isPositive}(a) \wedge \neg\mathrm{isPositive}(-a) \Rightarrow (a = 0)$$

* for every term $a:A$, if $a$ is positive, then $-a$ is not positive. 

$$\forall a:A. \forall b:A. \mathrm{isPositive}(a) \Rightarrow \neg\mathrm{isPositive}(-a)$$

* for every term $a:A$, $b:A$, if $a$ is positive, then either $b$ is positive or $a - b$ is positive. 

$$\forall a:A. \forall b:A. \mathrm{isPositive}(a) \Rightarrow \left(\mathrm{isPositive}(b) \vee \mathrm{isPositive}(a - b)\right)$$

* for every term $a:A$, $b:A$, if $a$ is positive and $b$ is positive, then $a + b$ is positive

$$\forall a:A. \forall b:A. \mathrm{isPositive}(a) \wedge \mathrm{isPositive}(b) \Rightarrow \mathrm{isPositive}(a + b)$$

* for every term $a:A$, $b:A$, if $a$ is positive and $b$ is positive, then $a \cdot b$ is positive

$$\forall a:A. \forall b:A. \mathrm{isPositive}(a) \wedge \mathrm{isPositive}(b) \implies \mathrm{isPositive}(a \cdot b)$$

We define the linear order as
$$a \lt b \coloneqq \mathrm{isPositive}(b - a)$$

## Examples

The field $\mathbb{R}$ of [[real numbers]] is [[the]] [[Dedekind completion|Dedekind-complete]] ordered field.

The field $\mathbb{Q}$ of [[rational numbers]] is a [[subfield]] of $\mathbb{R}$ that is too small to be complete.

The field of [[surreal number]]s is a [[field extension]] of $\mathbb{R}$ that is too large to be complete.


## Properties

Every ordered field must have [[characteristic]] $0$, since we can prove by [[induction]] that $n \gt 0$ for every positive [[natural number]] $n$. 

As a result, the [[rational numbers]] are the [[initial]] ordered field, and every ordered field is a [[Q-algebra|$\mathbb{Q}$-algebra]]. 

The [[archimedean field|archimedean]] ordered fields are precisely the [[subfield]]s of [[real number|the field of real numbers]]. 

+-- {: .un_prop}
######Proposition 
Every Dedekind complete ordered field is archimedean. 
=-- 

+-- {: .proof}
######Proof
Suppose otherwise: let $a, b \gt 0$ be given, and suppose $b$ is an upper bound of $a, 2a, 3a, \ldots$. Then $b - a$ is an upper bound of $0, a, 2a, \ldots$ and consequently there can be no least upper bound of the sequence, contradicting Dedekind completeness. 
=-- 

The following is a result in classical mathematics. 

+-- {: .un_prop}
###### Proposition 
A field admits an order ("is orderable") if and only if it is a **real field**, i.e., if the element $-1$ is not a sum of squares. 
=-- 

+-- {: .proof}
###### Proof 
Given an ordered field, any non-zero square is positive since either $-\alpha$ or $\alpha$ is positive, and so $(-\alpha)^2 = \alpha^2$ is positive. Hence a sum of non-zero squares cannot be negative, and in particular cannot be equal to $-1$. 

In the other direction, every real field $F$ may be embedded in a [[real closed field]] (this requires [[Zorn's lemma]]), and a real closed field admits a unique ordering. The restriction of this ordering to the embedded field $F$ gives an ordering on $F$. 
=-- 

## See also

* [[interval arithmetic]]

[[!redirects ordered field]]
[[!redirects ordered fields]]
[[!redirects linearly ordered field]]
[[!redirects linearly ordered fields]]
[[!redirects totally ordered field]]
[[!redirects totally ordered fields]]
[[!redirects strictly ordered field]]
[[!redirects strictly ordered fields]]
