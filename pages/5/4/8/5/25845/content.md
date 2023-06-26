## Definition

Recall that a [[triangulated category]] is given by a 1-category $C$ together with a suspension or translation endofunctor $X\mapsto X[1]$ and a distinguished family of diagrams of the form
$$
X \to Y \to Z\to X[1],
$$
called exact triangles, satisfying some axioms. 

A triangulated category $B$ is a __full triangulated subcategory__ of a triangulated category $C$ if it is

* a [[full subcategory]] $B\subset C$ in 1-categorical sense 

* closed under translation functor

* triangulated with respect to triangles in $C$

## Localization by a full triangulated subcategory

Given a full triangulated subcategory $B\subset C$, the class $\Sigma$ of morphisms $s$ which fit into a triangle in $C$ of the form
$$
X \overset{s}\to Y \to N\to X[1]
$$
where $N\in Ob(B)$
forms a (left and right) [[calculus of fractions]]. 
Hence we can form a localization (quotient) category $C[\Sigma^{-1}]$. This category equipped with induced translation functor and the exact triangles which are the images of the exact triangles in $C$ under the localization functor, is triangulated and usually denoted $C/B$. The localization functor is triangulated, sends all objects in $B$ into the $0$ object,  and is universal among all triangulated functors with this property.  

## Literature

For example

* [[Dmitri Orlov]], _Triangulated categories of singularities and equivalences between Landau-Ginzburg models_, Sbornik: Mathematics __197__:12 (2006) 1827 [doi](https://doi.org/10.1070/SM2006v197n12ABEH003824)
