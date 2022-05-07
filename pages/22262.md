
This page lists counterexamples in [[category theory]].


1. Taking the center of a group does not a define a functor from groups to abelian groups. 

1. Sending an object of a category to its automorphism group (or its endomorphism monoid) is not in general functorial.

1. Composing a [[monadic functor]] with another monadic functor need not be monadic. For example, Torsion-free abelian groups are monadic over abelian groups, which are monadic over sets, but torsion-free abelian groups are not monadic over sets. 

1. Taking the skeleton of a [[monoidal category]] does not in general result in a [[strict monoidal category]]. The argument in the case of Set is given in [this MO answer](https://mathoverflow.net/a/128629) In particular, one cannot in general replace a monoidal category with an equivalent category that is simultaneously  strict monoidal and skeletal. 

1. The category of topological spaces and [[local homeomorphism | local homeomorphisms]] is [[locally cartesian closed category | locally cartesian closed]] but not [[cartesian closed category | cartesian closed]] since it does not have a terminal object.

1. There are functors $D:Aff\to Vect$ and $A:Vect \to Aff$ between the categories of [[vector spaces]] and [[affine spaces]], and we have $D(A(V)) \cong V$ for any $V\in Vect$ and $A(D(U)) \cong U$ for any $U\in Aff$, but the categories are not [[equivalence of categories|equivalent]] --- the second isomorphism is not natural.

 
## References

The initial import of counterexamples in this entry was taken from [this Zulip discussion](). See also [[counterexamples in algebra]].
