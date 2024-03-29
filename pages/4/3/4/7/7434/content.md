
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

An ordinary $Set$-enriched [[category]] $C$ is called **atomic** if it has a [[small set|small]] [[dense subcategory|dense]] [[full subcategory]] of [[atomic objects]], $Atom(C)$, so that every object $c$ of $C$ is a small colimit of the functor 

$$Atom(C) \downarrow c \stackrel{proj}{\to} Atom(C) \stackrel{i}{\hookrightarrow} C.$$

More generally, for $V$ a [[cosmos]], a $V$-[[enriched category]] $C$ is _atomic_ if it admits a small $V$-dense full subcategory of atomic objects $Atom(C)$, such that every object $c$ is an enriched coend 

$$\int^{a \in Atom(C)} C(i a, c) \cdot i a.$$ 

## Properties

### Relation to presheaf toposes

+-- {: .num_thm}
###### Theorem 

A category $E$ is equivalent to a [[presheaf topos]] (functors with values in the 1-category [[Set]] of [[0-groupoids]]) if and only if it is cocomplete and atomic. 

=-- 

This is due to [[Marta Bunge]], who showed it is enough to have a regular cocomplete category with a [[generating set]] of atomic objects.

## Related concepts

* [[atom]] 

* [[compact object]]

* [[Cauchy completion]] 

[[!redirects atomic categories]]
