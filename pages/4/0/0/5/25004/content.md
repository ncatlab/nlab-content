

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

A strict order is a [[strict total order]] which is not a [[linear relation]]. Strict orders are used in models of the real numbers which have [[infinitesimals]], such as in the smooth real numbers in [[synthetic differential geometry]], and thus where not every real number not greater than or less than zero is equal to zero. 

## Definition

A strict order is a binary relation $\lt$ on a set $S$ which is irreflexive, asymmetric, transitive, and a comparison:

1. for all $a \in S$, $\neg(a \lt a)$ 

2. for all $a \in S$ and $b \in S$, if $a \lt b$, then $\neg(b \lt a)$

3. for all $a \in S$, $b \in S$, and $c \in S$, if $a \lt b$ and $b \lt c$, then $a \lt c$

4. for all $a \in S$, $b \in S$, and $c \in S$, if $a \lt c$, then $a \lt b$ or $b \lt c$

## Properties

The negation of a strict order is a [[preorder]] $a \leq b \coloneqq \neg(b \lt a)$, and thus has an [[equivalence relation]] defined as $a \approx b \coloneqq a \leq b \wedge b \leq a$. Every strict order which is also a [[linear relation]] is a [[strict total order]], whose negation is a [[partial order]]. Thus, in any foundations with [[quotient sets]], every strict order can be made into a strict total order by taking the quotient with respect to the equivalence relation $S/\approx$. 

## See also

* [[strict total order]]

* [[strictly ordered ring]]

* [[ordered local ring]]

* [[ordered Kock field]]

## References

Strict orders are used in defining the smooth real numbers in:

* [[David Jaz Myers]], *Orbifolds as microlinear types in synthetic differential cohesive homotopy type theory* ([arXiv:2205.15887](https://arxiv.org/abs/2205.15887))

[[!redirects strict order]]
[[!redirects strict orders]]
[[!redirects strict ordering]]
[[!redirects strict orderings]]
[[!redirects strictly ordered]]
[[!redirects strictly ordered set]]
[[!redirects strictly ordered sets]]