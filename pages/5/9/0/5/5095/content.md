
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Supercompact cardinals are among the [[large cardinal]]s.

## Definition

For $S$ a [[set]] and $\kappa$ a [[cardinal]], let $P_\kappa(S)$ be the set of [[subset]]s of $S$ of cardinality less than $\kappa$.

For $\lambda$ an [[ordinal]] a cardinal $\kappa$ is called **$\lambda$-supercompact** if $P_\kappa(\lambda)$ admits a [[normal measure]]. It is **supercompact** if it is $\lambda$-supercompact for every $\lambda$.

$\kappa$ being $\lambda$-supercompact is equivalent to there being an [[elementary embedding]]  $j : V \to M$ such that $j(\alpha) = \alpha$ for all $\alpha \lt \kappa$ and $j(\kappa) \gt \lambda$, where $M$ is an [[inner model]] such that $\{f | f : \lambda \to M\} \subset M$, i.e. every $\lambda$-sequence of elements of $M$ is an element of $M$.  

## Properties

By invoking [[Vop?nka's principle]] one can make strong statements about the existence of [[reflective subcategories]]. The assumption of supercompact cardinals is much weaker and accordingly they similarly imply existence of reflective subcategories only under some more additional assumptions.

+-- {: .un_defn}
###### Theorem

The existence of arbitrarily large supercompact cardinals implies the statement:

Every absolute epireflective class of objects in a balanced accessible category is a small-orthogonality class. 

In other words, if $L$ is a [[reflective subcategory|reflective]] [[localization]] functor on a [[balanced category|balanced]] [[accessible category]] such that the unit morphism $X \to L X$ is an [[epimorphism]] for all $X$ and the [[class]] of $L$-[[local object]]s is defined by an [[absolute formula]], then the existence of a suficciently large supercompact cardinal implies that $L is a localization with respect to some [[set]] of morphisms.

=--

This is in ([BagariaCasacubertaMathias](#BagariaCasacubertaMathias))

> [[Urs Schreiber]]: I am being told in prvivate communication that the assumption of epis can actually be dropped. A refined result is due out soon.


## References

Supercompact cardinals are discussed for instance in

* T. Jech _Set Theory_ The Third Millenium Edition, Revised and Expanded.
Springer Monographs in Mathematics. Springer-Verlag, Berlin, Heidelberg (2003)

* A. Kanamori, _The Higher Innite: Large Cardinals in Set Theory from Their
Beginnings_ Perspectives in Mathematical Logic. Springer-Verlag, Berlin, Heidelberg (1994)

The relation to refelctive subcategories is discusssed in

* Joan Bagaria, [[Carles Casacuberta]], Adrian Mathias, _Epireflections and supercompact cardinals_  Journal of Pure and Applied Algebra 213 (2009), 1208-1215 ([pdf](http://atlas.mat.ub.es/personals/casac/articles/bcm.pdf))
{#BagariaCasacubertaMathias}

[[!redirects supercompact cardinals]]