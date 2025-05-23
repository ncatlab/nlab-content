# Projective planes

* table of contents
{: toc}

## Idea

A projective plane is a [[projective space]] of [[dimension]] 2.  However, projective planes over [[fields]] (or more generally [[division rings]] or [[ternary rings]]) can be characterized axiomatically with a small list of "synthetic" axioms.

## Synthetic Definition

A **projective plane** consists of

* a set of "points"
* a set of "lines"
* a relation between points and lines called "incidence"

satisfying the following axioms:

* there exist at least one point and at least one line
* every pair of distinct points lies on exactly one line
* every pair of distinct lines meet in exactly one point
* every line has at least three points
* not all points are on the same line

Some further axioms which may be added are:

* the diagonal points of a [[complete quadrangle]] are not collinear ("Fano's axiom")

* if the lines joining corresponding vertices of two triangles are concurrent, then the intersections of corresponding sides are collinear ([[Desargues' theorem]])

* if the vertices of a hexagon lie alternately on two lines, then the intersections of opposite sides are collinear ([[Pappus' theorem]])

Of these, Pappus' theorem implies Desargues' theorem.

## Analytic projective planes

For any [[field]] $F$, we can construct the projective plane $F P^2$ in several ways:

* As the set of lines through the origin in $F^3$
* As the set of nonzero vectors in $F^3$ modulo scalar multiples (homogeneous coordinates)
* As the set of projections from $F^3$ onto 1-dimensional linear subspaces
* By starting with $F^2$ and adding a "line at infinity"

The resulting plane satisfies Pappus' theorem, hence also Desargues' theorem.  It satisfies Fano's axiom iff the [[characteristic]] of $F$ is $\neq 2$.

These methods also work for any [[division ring]], such as the [[quaternions]].  In this case, Pappus' theorem doesn't hold, but Desargues' theorem still does.

The [[octonions]] are not associative and this breaks the first two methods, but the latter two can be made to work, resulting in the [[Cayley plane]].  In this case Desargues' theorem does not hold in general, but there are special cases of it which do (corresponding to the fact that the octonions are "alternative").

## Equivalence of synthetic and analytic

In any projective plane, we can define a "scalar" to be an ordered set of four collinear points $(A,B,C,D)$ of which no more than two are equal.  Two scalars are considered equal if they are projectively related, i.e. the four lines joining corresponding points are concurrent.  If Desargues' theorem holds, we can define addition and multiplication on the scalars (omitting one of them that acts like $\infty$) making them into a division ring $F$ such that our plane is isomorphic to $F P^2$.  The ring $F$ is commutative (hence a field) iff Pappus' theorem also holds, and has characteristic $\neq 2$ iff Fano's axiom holds.

If Desargues' theorem fails, then we can still construct a sort of algebraic structure on the scalars, called a [[ternary ring]], which suffices to reconstruct our plane.  However, distinct ternary rings can give rise to isomorphic projective planes, in contrast to the situation for fields and division rings.

## Examples

* [[real projective plane]]

* [[complex projective plane]]

* [[quaternionic projective plane]]

* [[octonionic projective plane]]

## Related pages

* [[projective line]]



## References

* A. Kryftis, _A constructive approach to projective and affine planes_ , PhD Cambridge 2015. ([arXiv:1601.04998](http://arxiv.org/abs/1601.04998))
[[!redirects projective planes]]
