# Ordered fields
* table of contents
{: toc}

## Idea

An ordered field is a [[field]] equipped with a compatible [[strict total order]].

Note that while the adjective 'ordered' usually refers to a [[partial order]], it is traditionally used more strictly when placed before 'field'.


## Definition

Classically: 

\begin{definition}
An __ordered field__ is a [[field]] $K$ equipped with a [[strict total order]] $\lt$ such that $1 \gt 0$ and if $a, b \gt 0$, then so are $a + b$ and $a b$.
\end{definition}

One often sees the definition using a weak [[total order]] $\leq$ instead of the strict total order $\lt$. This makes no difference in [[classical mathematics]], but the definition of the strict total order is the one that generalizes to [[constructive mathematics]]. 

An ordered field could also be defined as a [[field]] with a [[predicate]] $\mathrm{isPositive}$ such that 

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

The strict total order is defined as
$$a \lt b \coloneqq \mathrm{isPositive}(b - a)$$

### In constructive mathematics. 

Due to the fact that in constructive mathematics, a set having a strict total order no longer implies that the set has a weak total order, and a set having a weak total order no longer implies that the set has a strict total order, the notion of ordered field bifurcates into multiple inequivalent notions. 

In particular, the traditional definition of an ordered field as defined above no longer implies that
 
1. that the ordered field is a [[lattice]], that it has binary [[joins]] and [[meets]]

2. that the ordered field, depending on how field is defined (see [[field#Constructive notions]]), is no longer Heyting. 

Thus, some authors in constructive mathematics, such as [Booij 2020](#Booij20) and [Univalent Foundatiins Project 2013](#UFP13), have defined an ordered field to additionally have a lattice structure on $\leq$ and be a Heyting field, with the [[tight apartness relation]] defined as $a \# b$ if and only if $a \lt b$ or $b \lt a$. 

However, other fields with a strict total order, such as the [[MacNeille real numbers]] and the [[surreal numbers]], do not necessarily have a lattice structure, nor are Heyting, so other authors prefer the more traditional definition given above. 

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

## References

* {#Booij20} Auke B. Booij, Analysis in univalent type theory ([pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf))
* {#UFP13} Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

[[!redirects ordered field]]
[[!redirects ordered fields]]
[[!redirects linearly ordered field]]
[[!redirects linearly ordered fields]]
[[!redirects totally ordered field]]
[[!redirects totally ordered fields]]
[[!redirects strictly ordered field]]
[[!redirects strictly ordered fields]]
