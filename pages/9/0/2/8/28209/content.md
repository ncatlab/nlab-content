## Idea

An extension of the notion of a [[C*-algebra]] to unbounded operators.

In complete analogy to abstract and concrete definitions of a [[C*-algebra]], there are abstract and concrete definitions of an extended C\*-algebra.

## Definition

An __extended C\*-algebra__  is a complex (or real) 
locally convex [[*-algebra]] $A$ such that

* the poset of subsets $B\subset A$ that are closed, absolutely convex, bounded, $1\in B$, and $B^2\subset B$ has a maximal element $B_0$;

* $A$ is _pseudocomplete_: for every $B$ as above, the [[Minkowski functional]] of $B$ induces a complete norm on $A$;

* $A$ is _symmetric_: for every $x\in A$, the element $(1+x^*x)^{-1}$ exists and belongs to $A_0$, the bounded part of $A$, comprising elements $a\in A$ such that there is a nonzero $\lambda$ for which the set $\{(\lambda x)^n\mid n\ge0\}$ is bounded.

## Concrete definition

An __extended C\*-algebra__  is a complex (or real) [[*-algebra]] $A$ of closed densely defined unbounded operators on a [[Hilbert space]] closed under the operations of strong sum, strong multiplication, passing to adjoints that contains all scalar multiples of the identity operator and for every $x\in A$ we have $(1+x^*x)^{-1}\in A$.

## Related concepts

* [[extended von Neumann algebra]]

## References

* J. B. Cooper, _Extended C\*-algebras and W\*-algebras_, Proceedings of the Symposium on Functional Analysis (Istanbul, 1973), 75–84. Publications of the Mathematical Research Institute Istanbul 1. Mathematical Research Institute, Istanbul, 1974.  [PDF](https://dmitripavlov.org/scans/cooper.pdf).

  * an expository article

* G. R. Allan, _On a class of locally convex algebras_, Proceedings of the London Mathematical Society s3-17:1 (1967), 91-114.  [DOI](https://doi.org/10.1112/plms/s3-17.1.91).

  * defines abstract extended C*-algebras (as GB*-algebras) in Definition 2.5
  * develops Gelfand duality

* P. G. Dixon, _Generalized B\*-algebras_, Proceedings of the London Mathematical Society s3-21:4 (1970), 693-715.  [DOI](https://doi.org/10.1112/plms/s3-21.4.693).

  * establishes functional calculus for commutative extended C\*-algebras and Gelfand-Neumark theorem for noncommutative extended C\*-algebras
  * defines concrete C\*-algebras in Definition 7.1
  * shows that abstract and concrete extended C\*-algebras are equivalent in Theorem 7.13

[[!redirects extended C*-algebras]]