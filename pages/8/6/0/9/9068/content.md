

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--
# Contents
* automatic table of contents goes here
{:toc}

##Idea

The concept of a **codense functor** is the dual of [[dense functor]].


## Definition

Let $F\colon A \to B$ be a [[functor]] between [[categories]]. It is **codense** when for each $b \in B$ the following is true:

  $Lim((b \downarrow F) \to A \to B) = b$

(where $(b \downarrow F)$ is a [[comma category]] (in this case the [[under category]]) from $b$ to the functor $F$.

This notion is dual to the notion of [[dense functor]].

Equivalently, a functor $F$ is **codense** iff $Id_B$, together with identity natural transformation $Id_F\colon F \to F$, is the pointwise right [[Kan extension]], $Ran_F F$, of $F$ along $F$.

Also, $F$ is **codense** iff  its [[codensity monad]] is the identity.

A [[subcategory]] is **codense** if the inclusion functor is codense.  

## Examples

*  Let $I$ denote the unit interval. Then the full subcategory of the category  of compact topological spaces $T$ whose only object is $I^2$ is a codense subcategory of $T$ ([Ulmer 68, p.80](#Ulmer68)).

## Related concepts

* [[dense]]

* [[dense functor]]

* [[codensity monad]]

## References

* {#Ulmer68} [[Friedrich Ulmer]], _Properties of Dense and Relative Adjoint Functors_, Journal of Algebra 8, 77-95 (1968)  

* [[William Lawvere]], _John Isbell's Adequate Subcategories_, TopCom **11** no.1 2006. ([link](http://at.yorku.ca/t/o/p/d/65.htm)) 