## Idea

A nominal set is a formalization of the idea of a set whose elements can have "variables" or "atoms" in them. Nominal sets are used in [[computer science]] to formalize notions of bound variables and [[alpha-equivalence]].

## Definition

A nominal set is an object of the [[Schanuel topos]].
One concrete description of this topos is that it is the [[category of G-sets]] for the group of permutations of the natural numbers topologized as a subspace of the [[Baire space of sequences]]. The continuity can be described as the finite support property below.

A nominal set is a set $X$ with an action of the group of permutations of natural numbers such that each element has finite support: for each $x \in X$ there is some subset $supp(x) \subseteq N$ such that if $\pi$ fixes $supp(x)$ then $\pi \cdot x = x$.

## References

Related $n$Lab entries include [[Schanuel topos]], 

A survey:

* Murdoch J. Gabbay, _Foundations of nominal techniques: logic and semantics of variables in abstract syntax_. Bulletin of Symbolic Logic 17:2, June 2011, 161-229

* Wikipedia, [Nominal techniques](http://en.wikipedia.org/wiki/Nominal_techniques)

In computer science, nominal sets were introduced in 

* Murdoch James Gabbay, _A theory of inductive definitions with alpha-equivalence_, PhD thesis, Cambridge 2001, [pdf](http://www.gabbay.org.uk/papers/thesis.pdf)

See also

* [[Andrew Pitts|A. M. Pitts]], _Nominal sets_, Cambridge University Press 2013

* Daniela Petrisan, _Algebra and topology over nominal sets_, PhD thesis, Leicester 2010, [pdf](https://www.irif.fr/~petrisan/thesis.pdf)

* M. J. Gabbay, [[Andrew Pitts|A. M. Pitts]], _A NEW approach to abstract syntax with variable binding_, Formal Aspects of Computing **13** (2002) pp.341-363. ([draft](http://www.cl.cam.ac.uk/~amp12/papers/newaas/newaas-jv.pdf))

[[!redirects nominal sets]]