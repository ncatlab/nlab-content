> **Under Construction**

#Contents#
* automatic table of contents goes here
{:toc}


##Idea
A **spacetime** is a [[smooth Lorentzian space]] $(X,\mu)$ equipped with a time orientation (see there).

In [[classical physics]], notably in [[Special Relativity]] and [[General Relativity]] points in $X$ model coordinates where _events_ can take place from the viewpoint of an observer ("points in space and time") while the metric $\mu$ models the field of [[gravity]] in [[General Relativity]].

+--{: .query}
Ian: Let me rephrase what I had originally put here.  The way it is written above, it implies that the metric _only_ models the field of gravity.  But the Reissner-Nordstroem metric, for example, includes both mass and charge terms.  If you take the limit as $M \to 0$ you're left with a metric that is only dependent on charge.  In other words, you end up with a massless charged field that contains a naked singularity.  Either this implies that charge is related to gravity or this implies that the metric models more than just the field of gravity.  This is why I prefer to say it describes the curvature of spacetime.
=--

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

[[!redirects space-time]]
[[!redirects space time]]