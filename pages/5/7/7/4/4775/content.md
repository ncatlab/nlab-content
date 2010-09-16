## Idea

The *essential fiber* of a [[functor]] is a non-[[evil]] replacement for the [[fiber]].  It is a category-theoretic version of a [[homotopy fiber]].

## Definition

Let $p:E\to B$ be a functor and $b\in B$ an [[object]].  The **essential fiber** of $p$ over $b$ is the following category:

* its objects are pairs $(e,\phi)$ where $e\in E$ is an object and $\phi\colon p(e)\cong b$ is an [[isomorphism]].
* its morphisms $(e,\phi)\to (e',\phi')$ are morphisms $f\colon e\to e'$ in $E$ such that $\phi' \circ p(f) = \phi$.

The essential fiber can be identified with the [[pseudopullback]] of $p$ along the functor $b\colon 1\to B$ from the [[terminal category]] which picks out the object $b$.  It can also be identified with a [[homotopy fiber]] in the [[canonical model structure]] on [[Cat]].  When [[groupoids]] are identified with [[homotopy 1-types]], the essential fiber actually coincides with the classical homotopy fiber (up to equivalence).

## Relationship to fibrations

If $p$ is an [[isofibration]], then any of its essential fibers is equivalent to the corresponding strict fiber.  This includes the case when $p$ is a [[Grothendieck fibration]].

On the other hand, when $p$ is a [[Street fibration]] (the non-evil version of a Grothendieck fibration), then essential fibers do *not* coincide with strict fibers, and essential fibers are the more useful notion.  In particular, the correspondence between fibrations and [[pseudofunctors]] only goes through for Street fibrations if one defines the pseudofunctor using essential fibers.

[[!redirects essential fibre]]
[[!redirects essential fibers]]
[[!redirects essential fibres]]
