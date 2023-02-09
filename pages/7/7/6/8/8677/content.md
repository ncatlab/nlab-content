
> This entry is meant to be about the general notion of localization of a possible noncommutative ring (a special case of *[[Cohn localization]]*). For the more restrictive but traditional notion for commutative rings see at *[[localization of a commutative ring]]*. 


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

Given a (possibly noncommutative) unital [[ring]] $R$ there are many situations when certain elements or matrices can be inverted in a universal way obtaining a new "localized" ring $S^{-1}R$ equipped with a [[localization]] [[homomorphism]] $R\to S^{-1}R$ under which all elements in $S$ are mapped to multiplicatively [[invertible elements]] ([[units]], hence elements of the [[group of units]]). 

This is a special case of and generalizes to the notion of *[[Cohn localization]]* where one may also force certain [[matrices]] with [[coefficients]] in the ring to become invertible.

Often one inverts elements in a left or right [[Ore subset]] $S\subset R$ in which case the localized ring is expressed by fractions as naively expected, called *[[Ore localization]]*. 

The Ore-condition is automatic for [[commutative rings]] which leads to the notion of *[[localization of a commutative ring]]*.

Another special case is known as *[[Martindale localization]]*.



## Definition

### For general rings

Let $S$ be any [[subset]] of a [[ring]] $R$.  

Say that a ring [[homomorphism]] $f \colon R \to A$ is _$S$-inverting_ if the [[image]] of $S$ under $f$ is contained in the [[units]] $A^\times \subset A$, i.e. if for every $s \in S$ there is a $t \in A$ so that $t \cdot f(s) = 1 = f(s) \cdot t$ in $A$. 

Then the _localization of $R$ with respect to $S$_ is a ring homomorphism $h \colon R \to R_S$ which is [[initial object|initial]] with respect to such $S$-inverting ring homomorphisms.  

By this defining [[universal property]] the localization is unique up to [[isomorphism]], when it exists.  Its existence is a special case of [[universal localization]]/[[Cohn localization]], a general abstract construction. 

If $S$ is an [[Ore set]], then the localization of $R$ with respect to $S$ has an explicit description in terms of fractions, see at *[[Ore localization]]*. 

## Examples

* The localization of a ring at a multiplicative submonoid $S$ which contains $0$ is the [[trivial ring]]. 



## References

See the references at *[[Cohn localization]]*, also at *[[noncommutative localization]]*.

For references on the [[localization of commutative rings]] see [there](localization+of+a+commutative+ring#References).


See also:

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