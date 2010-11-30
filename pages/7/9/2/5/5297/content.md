
# Bicategory of maps
* table of contents
{: toc}

## Definition

If $K$ is a [[bicategory]], then a [[morphism]] $f \colon a \to b$ is called a **map** if it has a [[right adjoint]] $f^* \colon b \to a$.  (This is in slight contrast to the common usage of "map" to denote simply a [[morphism]] in any category.)

The bicategory $Map K$ is the [[locally full sub-2-category]] of $K$ determined by the maps.


## Examples

* In the bicategory [[Rel]] of [[sets]] and [[relations]], a relation is a map if and only if it is the [[graph of a function]].  Consequently, $Map Rel$ is equivalent to [[Set]].

* Similarly, if $C$ is a category with finite [[limits]], then there is a bicategory $Span C$ of [[spans]] in $C$.  The bicategory $Map Span C$ is equivalent to $C$.

* In the bicategory [[Prof]] of [[categories]] and [[profunctors]] (perhaps [[enriched category|enriched]]), if $B$ is a [[Cauchy complete category]], then a profunctor $A\to B$ is a map if and only if it is represented by a functor $A\to B$.  If $B$ is not Cauchy complete, then maps $A\to B$ correspond to functors from $A$ to the Cauchy completion of $B$.


## Properties

If every map in $K$ is [[comonadic morphism|comonadic]] and $Map K$ has a terminal object, then $Map K$ is equivalent to a $1$-category.  If in addition $K$ is a [[cartesian bicategory]] and every [[comonad]] in $K$ has an [[Eilenberg--Moore object]], then $K$ is [[biequivalence|biequivalent]] to $Span Map K$, $Map K$ having finite limits.  The converse is true if pullback squares in $Map K$ satisfy the Beck--Chevalley condition in $K$, i.e. if their [[mates]] are invertible (see [\[LWW10\]](#LWW10)).

$Map K$ is a [[regular category]] if and only if $K$ is a unitary tabular [[allegory]], equivalently a [[bicategory of relations]] in which every [[coreflexive morphism]] [[split idempotent|splits]].  In that case $Rel Map K \simeq K$.

Similarly, $Map K$ is a [[topos]] if and only if $K$ is a unitary tabular power allegory.


## Maps and equipments

A [[2-category equipped with proarrows]] is, by definition, a bijective-on-objects [[pseudofunctor]] $K\to M$ such that the image of every arrow in $K$ is a map in $M$.  Equivalently, therefore, it is a bijective-on-objects pseudofunctor $K\to Map M$.

Hence the inclusion $Map M \to M$ is the "universal" proarrow equipment that can be constructed with a given bicategory $M$ as its bicategory of proarrows.  More precisely, there is a forgetful functor from $Equip$ to $Bicat$ which remembers only the bicategory $M$ of proarrows, and the assignment of $M$ to $Map M \to M$ is its right adjoint.

+--{: .query}
[[Mike Shulman]]: This is obviously morally true, but I can't be bothered right now to check which 1-, 2-, or 3-categories of equipments and bicategories one has to use to make it precisely correct.
=--

A lot of work in bicategories that makes use of maps could easily be reformulated in a proarrow equipment, and conversely.  Thus, it is to some extent a question of aesthetics which is preferred.  One advantage of proarrow equipments is they can distinguish between a category and its Cauchy completion (as objects of Prof), while maps in bicategories are perhaps simpler in some ways.


## References

* Carboni, Walters, _Cartesian bicategories I_, JPAA 49, 1987.
{: #CW87 }

* Lack, Walters, Wood, _Bicategories of spans as cartesian bicategories_, TAC 24(1), 2010.
{: #LWW10 }

[[!redirects bicategories of maps]]
[[!redirects map in a bicategory]]
[[!redirects maps in a bicategory]]
