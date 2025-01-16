
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The concept of $W^\ast$-categories is the special case of that of [[C-star category|$C^\ast$-categories]] like [[von Neumann algebras]] (aka $W^\ast$-algebras) are a special case of [[C-star algebra|$C^\ast$-algebras]]. Hence a more systematic name for $W^\ast$-categories would be *$W^\ast$-algebroids* or *von Neumann algebroids*.


## Definition

A __W\*-category__ is a [[C*-category]] $C$
such that for any objects $A,B\in C$, the [[hom-object]] $Hom(A,B)$
admits a [[predual]] as a [[Banach space]].
That is, there is a [[Banach space]]
$Hom(A,B)_*$ such that $(Hom(A,B)_*)^*$ is isomorphic to $Hom(A,B)$
in the category of [[Banach spaces]] and [[contractive maps]] (alias _short maps_).

## W\*-functors

A __W\*-functor__ is a [[functor]] $F\colon C\to D$
such that $F(f^*)=F(f)^*$ for any [[morphism]] $f$ in $C$
and the map of [[Banach spaces]] $Hom(A,B)\to Hom(F(A),F(B))$
admits a [[predual]] for any objects $A$ and $B$ in $C$.

## Bounded natural transformation

The good notion of natural transformations between W\*-categories
is given by __bounded natural transformations__:
a [[natural transformation]] $t\colon F\to G$ between W\*-functors
is bounded if the norm of $t_X\colon F(X)\to G(X)$
is bounded with respect to the object $X$ of $C$.

## The bicategory of W\*-categories

W\*-categories, W\*-functors, and bounded natural transformations
form a [[bicategory]].

This [[bicategory]] is a good setting to work with objects
like [[Hilbert spaces]], [[Hilbert W*-modules]] over [[von Neumann algebras]], [[W*-representations]] of [[von Neumann algebras]], etc.

In particular, in this [[bicategory]],
the [[category of Hilbert spaces]] has infinite [[direct sums]] (generalizing the definition of a [[biproduct]] to infinite families of objects),
unlike in the usual [[bicategory]]
of [[categories]], [[functors]], and [[natural transformations]],
where it only has [[finite limits]] and [[finite colimits]].

The same is true for [[Hilbert W*-modules]] over [[von Neumann algebras]], [[W*-representations]] of [[von Neumann algebras]].

## Related concepts

* [[von Neumann algebra]]

* [[C-star category|$C^\ast$-category]]

## References

* [[P. Ghez]], [[Ricardo Lima]], [[John E. Roberts]], _W\*-categories_, Pacific Journal of Mathematics 120:1 (1985), 79–109 &lbrack;[doi:10.2140/pjm.1985.120.79](https://doi.org/10.2140/pjm.1985.120.79)&rbrack;

Understanding complete [[W*-category|$W^\ast$-categories]] as [[2-Hilbert spaces]]:

* [[André Henriques]], [[Nivedita]], [[David Penneys]]: *Complete $W^\ast$-categories* &lbrack;[arXiv2411.01678](https://arxiv.org/abs/2411.01678)&rbrack;

Exposition:

* [[Nivedita]]: *Towards Models for 2-Hilb and 3-Hilb as targets for functorial field theories*, talk notes (2024) &lbrack;[[Nivedita-ModelFor2HilbForFQFT.pdf:file]]&rbrack;




[[!redirects W*-categories]]

[[!redirects W-star category]]
[[!redirects W-star+categories]]


