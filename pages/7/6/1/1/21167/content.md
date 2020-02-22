\tableofcontents

## Idea

The __sequence operad__ is an [[E-infinity operad]],
valued in [[cochain complexes]],
that acts on [[simplicial cochains]]
of any [[simplicial set]].

Furthermore, this operad has an explicit presentation
in terms of a countable collection of generators and relations.

The operations in this operad are [[generalized cup products|generalized Steenrod cup-$i$ products]]
(denoted by $x \cup_i y$).

## Definition

The __sequence operad__ $Seq$ is the [[suboperad]]
of the [[endomorphism operad]]
of the [[simplicial cochains]] functor
$$S^* \colon sSet \to coCh$$
such that $Seq(n)$ is the subobject of $Hom((S^*)^{\otimes n},S^*)$
consisting of Steenrod's [[generalized cup products]].

## Main property

Theorem 2.15 in McClure and Smith \cite{Cochain}
shows that $Seq$ is an [[E-infinity operad]] in [[cochain complexes]].

By definition, the operad $Seq$ acts on [[simplicial cochains]]
of any [[simplicial set]],
in particular, it acts on [[singular cochains]] of a [[topological space]].

This provides a simple and concrete model of the [[E-infinity algebra]]
structure on [[simplicial cochains]].

## Generalizations to $E_n$-algebras

One can easily identify a suboperad $Seq_n$ of the operad $Seq$
by imposing a simple combinatorial condition on the multiindices
of [[generalized cup products]] (Definition 3.2 in \cite{Cochain}).

The resulting operad is an [[E_n-operad]],
i.e., it is weakly equivalent to the singular cochains on the little
$n$-cubes operad (Theorem 3.5 in \cite{Cochain}).

## References

\bibitem{Cochain}
[[James E. McClure]], [[Jeffrey H. Smith]],
_Multivariable cochain operations and little $n$-cubes_,
[arXiv:math/0106024v3](https://arxiv.org/abs/math/0106024v3).
