
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

## References

An [[E-infinity algebra]] on simplicial cochains is constructed in

* [[Albrecht Dold]], _Über die Steenrodschen Kohomologieoperationen_, Annals of Math. (2) 73 (1961), 258–294.

* [[Vladimir Hinich]], [[Vadim Schechtman]], _On homotopy limit of homotopy algebras_. K-theory, arithmetic and
geometry (Moscow, 1984–1986), 240–264, Lecture Notes in Mathematics 1289, Springer, 1987.

* [[James McClure]], [[Jeffrey Smith]], _Multivariable cochain operations and little $n$-cubes_, Journal of the American Mathematical Society 16:3 (2003), 681-704.
[doi](https://doi.org/10.1090/s0894-0347-03-00419-3), [arXiv](https://arxiv.org/abs/math/0106024).


[[!redirects simplicial cochains]]