
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Contextreynolds
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[proof theory]] and the theory of [[programming languages]], the term "logical relations" refers to a certain style of argument used in proving results such as [[strong normalization]] or [[observational equivalence]].  Although there is no precise definition, typically a logical relation (or _logical predicate_) corresponds to a _family_ of (sometimes unary) [[relations]] defined by induction on [[types]], and such that the definition of the relation at a particular type mirrors the logical structure of that type in an appropriate sense.

## Example

As originally described by ([Tait 1967](#Tait67)) (and presented in ([Girard 1990](#Girard90))), logical predicates can be used to prove strong normalization for the [[simply-typed lambda calculus]].  The idea is to define a family of predicates $RED_T$ over terms, indexed by types $T$, such that:

* ($T = X$ an atomic type): $t \in RED_X$ iff $t$ is strongly normalizing

* ($T = U \to V$ a function type): $t \in RED_{U \to V}$ iff $\forall u$, $u \in RED_U$ implies $t(u) \in RED_V$.

By induction on $T$, one establishes the following three conditions:

1. if $t \in RED_T$, then $t$ is strongly normalizing

1. if $t \in RED_T$ and $t \to t'$, then $t' \in RED_T$

1. if $t$ is _neutral_ (i.e., either a variable or application) and for all $t \to t'$ we have $t' \in RED_T$, then $t \in RED_T$

Finally, one proves the "fundamental lemma"

* if $t:T$ then $t \in RED_T$

which by condition (1) implies that every simply-typed term is strongly normalizing.

## Related concepts

* [[programming language]], [[computer science]]

## References

* {#Tait67} W. W. Tait. _Intensional Interpretations of Functionals of Finite Type I_, JSL 32:2, June 1967. ([JSTOR](http://www.jstor.org/stable/2271658))

* {#Plotkin73} [[Gordon Plotkin]]. _Lambda-definability and logical relations_, unpublished manuscript, Edinburgh 1973. ([pdf](http://homepages.inf.ed.ac.uk/gdp/publications/logical_relations_1973.pdf))

* {#Reynolds83} [[John C. Reynolds]], _Types, Abstraction and Parametric Polymorphism_ Information Processing 83(1) (1983), pp. 513-523.

* {#Girard90} [[Jean-Yves Girard]], [[Yves Lafont]], and [[Paul Taylor]], _Proofs and Types_, 1990. ([web](http://www.paultaylor.eu/stable/Proofs+Types))

For a recent perspective:

* {#Hermida13} [[Claudio Hermida]], [[Uday Reddy]], E. Robinson, section 2 of _Logical Relations and Parametricity - A Reynolds Programme for Category Theory and Programming Languages_, Electronic Notes in Theoretical Computer Science (2013) ([pdf](http://www.cs.bham.ac.uk/~udr/papers/logical-relations-and-parametricity.pdf))

See also 

* Patricia Johann, [[Neil Ghani]], _Logical Relations for Program Verification_, research proposal ([pdf](https://personal.cis.strath.ac.uk/neil.ghani/lrpv.pdf))
  {#JohannGhani}

* [[Thierry Coquand]], from slide 63 on in _Equality and dependent type theory_ ([pdf](http://www.cse.chalmers.se/~coquand/equality.pdf))

* Florian Rabe, Kristina Sojakova, _Logical Relations for a Logical Framework_ ([pdf](http://kwarc.info/frabe/Research/RS_logrels_12.pdf))

* Carsten Sch&#252;rmann, Jeffrey Sarnat, _Structural logical relations_ ([pdf](http://www.twelf.org/slr/slr.pdf))

Further discussion:

* StackExchange discussion, _[What are differences between logical relations and simulations?](http://cstheory.stackexchange.com/questions/5427/what-are-the-differences-between-logical-relations-and-simulations)_

* TYPES mailing list thread on the [origin of the term "logical relation"](http://lists.seas.upenn.edu/pipermail/types-list/2006/001042.html)

[[!redirects logical relations]]