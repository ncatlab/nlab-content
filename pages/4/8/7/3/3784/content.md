> **Under Construction**

#Contents#
* automatic table of contents goes here
{:toc}


##Idea
A **spacetime** is a [[smooth Lorentzian space]] $(X,\mu)$ equipped with a time orientation (see there).

In [[classical physics]], notably in [[Special Relativity]] and [[General Relativity]] points in $X$ model coordinates where _events_ can take place from the viewpoint of an observer ("points in space and time") while the metric $\mu$ models the field of [[gravity]] in [[General Relativity]] (though see remark below).

###Remark on the physical meaning of points in General Relativity, Einstein's "hole argument"

* see Wikipedia on the [hole argument] (http://en.wikipedia.org/wiki/Hole_argument)

What does it mean to say "let $A$ be a point in spacetime" from the physical viewpoint? How does it relate to reality?

In [[General Relativity]], every chart of the [[atlas]] of the given spacetime represents the viewpoint of a physical observer.

Choose a chart $\phi$ of $(X,\mu)$, let $\phi^{-1}$ contain an _empty_ subset $U$ (containing nothing that could be observed, e.g. no matter), such that $U$ is open and simply connected. Let $e$ be the gravitational field and assume that $U$ contains a point $A$ where $e$ is flat and a point $B$ where $e$ is not flat. Then there is a diffeomorphism $\psi: X \to X$ reducing to the identiy outside of $U$, with $\psi(A) = B$. Let $e' = \psi^*(e)$ be the pullback of $e$ along $\psi$. Since the field equations of [[General Relativity]] are covariant, both $e$ and $e'$ are solutions to the field equations. So one observer will say that there is no gravitation at the spacetime point $A$, while another will say there is. Or, to put it differently, the field equations do not determine the value $e(A)$, and never can if they are covariant.

The conclusion of [[General Relativity]] of this paradox is that there is no meaning to talk about the spacetime point $A$: a point alone, with nothing obsevable attached to it, does not have an objective meaning ("objective" is "independent of the chosen observer resp. coordinate system").

As a tagline this reads:

+-- {: .standout}
Space and time do not exist on their own in General Relativity. If you remove all manifestations of energy from Newton's space and time, then space and time remain. If you remove all manifestations of energy from a spacetime in General Relativity, nothing remains.
=--

+-- {: .query}
[[Tim van Beek]]: This paragraph could of course be taken to the [[General Relativity]] page...
=--

The name spacetime as a composite noun is best motivated from the viewpoint of [[General Relativity]]: In general there is no globally defined coordinate system, and therefore not necessarily a globally defined _canonical_ time coordinate. More specifically, there are spacetimes that admit coordinates defined on subsets where the _physical_ interpretation of the coordinates as modelling time and space coordinates _changes_ over the domain of definition.
(TODO: references or explanations).

### Remark on the nature of the spacetime metric

While it is accepted by many that the metric represents the gravitational field, there is a school of thought that prefers to see the metric as representing the curvature of spacetime.  This curvature is the result of some field source.  The interpretation espoused above _a priori_ assumes the metric encodes the gravitational field only.  (Note that this implies that charge has a gravitational interpretation.)  If we don't assume this and then we take the mass to zero in the Reissner-Nordstr&#246;m metric, it is possible to interpret the metric as simply representing the curvature of spacetime due to _some_ field source that is not necessarily gravitational.  This would resolve some paradoxes inherent with the other interpretation. [I will fill in a citation for this and an example.]

=--

[[!redirects space-time]]
[[!redirects space time]]