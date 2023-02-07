
> This entry is meant to be about the general notion of localization of a possible noncommutative ring. For the more restrictive but traditional notion for commutative rings see at *[[localization of a commutative ring]]*. 


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

## Idea

### General

Given a (possibly noncommutative) unital [[ring]] $R$ there are many situations when certain elements or matrices can be inverted in a universal way obtaining a new "localized" ring $S^{-1}R$ equipped with a localization [[homomorphism]] $R\to S^{-1}R$ under which all elements in $S$ are mapped to multiplicatively invertible elements ([[units]]). The latter property must be modified for Cohn localization at multiplicative set of matrices. 

We can typically invert elements in a left or right Ore subset $S\subset R$ or much more generally some multiplicative set or matrices ([[Cohn localization]]) etc. There are also some specific localizations like Martindale localizations in ring theory. 


## Definition

### For general rings

Let $R$ be a [[ring]] and $(S, 1, \cdot)$ be a multiplicative [[submonoid]] of $(R, 1, \cdot)$ with [[monoid]] [[monomorphism]] $i:S \hookrightarrow R$. The **localization** of $R$ at $S$ is defined as the [[initial object|initial]] ring $S^{-1} R$ with a ring homomorphism $h:R \to S^{-1} R$ and monoid homomorphism $j:S \to S^{-1} R$ such that for all $s \in S$, $j(s) \cdot h(i(s)) = 1$ and $h(i(s)) \cdot j(s) = 1$: for every other ring $A$ with a ring homomorphism $k:R \to A$ and monoid homomorphism $l:S \to A$ such that for all $s \in S$, $l(s) \cdot k(i(s)) = 1$ and $k(i(s)) \cdot l(s) = 1$, there is a unique ring homomorphism $g:S^{-1} R \to A$. 

This needs conditions in order to exist, see at *[[Ore localization]]* or *[[noncommutative localization]]*.

The localization of a ring at a multiplicative submonoid $S$ which contains $0$ is the [[trivial ring]]. 



## References

For references on the [[localization of commutative rings]] see [there](localization+of+a+commutative+ring#References).

Discussion of the general concept in [[noncommutative geometry]]:

See references at *[[noncommutative localization]]*

and:

* [[Zoran Škoda]], _Noncommutative localization in noncommutative geometry_,  London Math. Society Lecture Note Series 330 ([pdf](http://www.maths.ed.ac.uk/~aar/books/nlat.pdf)), ed.  A. Ranicki; pp. 220--313, [math.QA/0403276](http://arxiv.org/abs/math.QA/0403276).

[[!redirects localizations of a ring]]

[[!redirects localization of rings]]
[[!redirects localizations of rings]]

[[!redirects localisation of a ring]]
[[!redirects localisations of a ring]]
[[!redirects localisation of rings]]
[[!redirects localisations of rings]]

[[!redirects left localization of a ring]]
[[!redirects left localizations of a ring]]
[[!redirects left localization of rings]]
[[!redirects left localizations of rings]]

[[!redirects left localisation of a ring]]
[[!redirects left localisations of a ring]]
[[!redirects left localisation of rings]]
[[!redirects left localisations of rings]]

[[!redirects right localization of a ring]]
[[!redirects right localizations of a ring]]
[[!redirects right localization of rings]]
[[!redirects right localizations of rings]]

[[!redirects right localisation of a ring]]
[[!redirects right localisations of a ring]]
[[!redirects right localisation of rings]]
[[!redirects right localisations of rings]]