+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Arithmetic
+-- {: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A way of defining a [[dense linear order]] that behaves like the [[closed intervals]] in a dense linear order, which identifies each closed interval $[a,b]$ with the pair of [[open intervals]] $(-\infty, a), (b, \infty)$. 

## Definition

Given a [[DLO]] $D$,  An __interval cut__ is a pair $(L,U)$ of [[subsets]] of elements in $D$ satisfying these conditions:

1.  $L$ is [[inhabited set|inhabited]]; that is, some element of $D$ belongs to $L$.
2.  Similarly, $U$ is inhabited.
3.  $L$ is a [[lower set]]; that is, if $a \lt b$ are elements of $D$ with $b \in L$, then $a \in L$.
4.  Similarly, $U$ is an [[upper set]]: if $a \lt b$ are elements of $D$ with $a \in U$, then $b \in U$.
5.  $L$ is an upwards [[open set]]; that is, if $a \in L$, then $a \lt b$ for some $b \in L$.
6.  Similarly, $U$ is a  downwards [[open set]]: if $b \in U$, then $a \lt b$ for some $a \in U$.
8.  If $a \in L$ and $b \in U$, then $a \lt b$.

The [[DLO]] of __closed intervals__ in $D$ is defined to be the [[set]] of all interval cuts in $D$. 

## Properties

* The set of all [[located real number|located]] interval cuts in $\mathbb{Q}$ is the [[Dedekind real numbers]]

* The set of all interval cuts in $\mathbb{Q}$ with a [[locator]] is the [[modulated Cauchy real numbers]]

## See also 

* [[interval arithmetic]]

* [[Dedekind cut]]

* [[locator]]

## References

* Auke Booij, *Extensional constructive real analysis via locators*, ([abs:1805.06781](https://arxiv.org/abs/1805.06781))

* Mark Bridger, [Real Analysis: A Constructive Approach Through Interval Arithmetic](https://bookstore.ams.org/amstext-38), Pure and Applied Undergraduate Texts 38, American Mathematical Society, 2019.

[[!redirects interval cuts]]