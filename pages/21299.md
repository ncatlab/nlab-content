## Definition

A morphism $f$ of [[simplicial sets]] is a __simplicial weak equivalence__ if any of the following equivalent conditions is satisfied:

* $Ex^\infty(f)$ is a [[simplicial homotopy equivalence]].
* $Ex^\infty(f)$ has the [[right homotopy lifting property]] with respect to $\partial\Delta^n\to\Delta^n$.
* $Ex^\infty(f)$ induces [[isomorphisms]] on [[simplicial homotopy groups]],
i.e., $Ex^\infty(f)$ induces an [[isomorphism]] on $\pi_0$ and all [[homotopy groups]] for any choice of basepoints.
* $Hom(f, A)$ is a [[simplicial homotopy equivalence]] for every [[Kan complex]] $A$.
* $f$ has the [[right homotopy lifting property]] with respect to $Sd^i \partial\Delta^n \to Sd^i \Delta^n$ (allowing [[subdivisions]] for homotopies also).
* $f$ belongs to the class of [[weak equivalences]] in the [[model category]] whose [[cofibrations]] are [[monomorphisms]] and [[fibrant objects]] are [[Kan complexes]].
* The morphism $f$ is a composition of a [[trivial cofibration]] and a [[trivial fibration]], both of which are defined using lifting properties.
* Applying the [[category of elements]] functor produces a [[Thomason weak equivalence]] of categories. The class of [[Thomason weak equivalences]] forms the smallest [[basic localizer]], i.e., the smallest class of [[functors]] between [[small categories]] that contains identities, is closed under [[retracts]] and the 2-out-of-3 property, contains all functors A→1 for which the category A has a [[terminal object]], and is locally determined: if $u\colon A\to B$ and $w\colon B\to C$ are functors, with $v=w\circ u\colon A\to C$, and for any $c\in C$ the induced functor of comma categories $v/c\to w/c$ is a [[Thomason weak equivalence]], then so is u.

[[!redirects simplicial weak equivalences]]