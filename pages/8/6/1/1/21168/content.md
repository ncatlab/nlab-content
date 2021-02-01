
> This entry may need to be merged with _[[cochain on a simplicial set]]_.

\tableofcontents

## Idea

Given a [[simplicial set]] $X$, the simplicial cochains on $X$ form a [[cochain complex]].
The [[cohomology]] of this [[cochain complex]] computes the [[cohomology]]
of the [[simplicial set]] $X$.

As a special case, if $X$ is the [[singular simplicial set]]
of a [[topological space]] $S$, then
the simplicial cochains of $X=Sing(S)$
are precisely the [[singular cochains]] of $S$.

## Definition

Given an [[abelian group]] $A$,
the __simplicial cochains__ functor is a functor
$$C^*(-,A)\colon sSet \to coCh.$$
It is defined as the composition
of the [[simplicial chains]] functor (with integer coefficients)
$$C\colon sSet \to sAb \to Ch$$
with the dualization functor
$$Hom(-, A[0])\colon Ch \to coCh.$$

## Additional structures

The simplicial cochains of a [[simplicial set]] $X$
with coefficients in a [[commutative ring]] $A$
admit an action of the [[sequence operad]],
which turns $C^*(X,A)$ into an [[E-infinity algebra]].

In particular, this structure incorporates simplicial [[cup products]]
of cochains, as well as Steenrod's [[generalized cup products]].

## Related concepts

* [[simplicial chains]]

* [[singular cochains]]

* [[singular cohomology]]

[[!redirects simplicial cochains]]
