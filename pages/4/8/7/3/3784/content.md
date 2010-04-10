> **Under Construction**

#Contents#
* automatic table of contents goes here
{:toc}


##Idea
A **spacetime** is a [[smooth Lorentzian space]] $(X,\mu)$ equipped with a time orientation (see there).

In the context of classical [[General relativity]] a **spacetime** is usually in addition assumed to be connected and four-dimensional.

In [[classical physics]], notably in [[Special Relativity]] and [[General Relativity]] points in $X$ model coordinates where _events_ can take place from the viewpoint of an observer ("points in space and time") while the metric $\mu$ models the field of [[gravity]] in [[General Relativity]].

+--{: .query}
Ian: Let me rephrase what I had originally put here.  The way it is written above, it implies that the metric _only_ models the field of gravity.  But the Reissner-Nordstroem metric, for example, includes both mass and charge terms.  If you take the limit as $M \to 0$ you're left with a metric that is only dependent on charge.  In other words, you end up with a massless charged field that contains a naked singularity.  Either this implies that charge is related to gravity or this implies that the metric models more than just the field of gravity.  This is why I prefer to say it describes the curvature of spacetime.

=--

###Remark on the physical meaning of points in General Relativity, Einstein's "hole argument"

####Idea
The hole argument elaborates on the meaning of covariance in the _physical_ interpretation of the theory of [[General Relativity]], it was of crucial importance for Einstein when he considered the question if the field equations should be covariant with respect to the full diffeomorphism group of a spacetime.

####the argument
In [[General Relativity]], every chart of the [[atlas]] of the given spacetime represents the viewpoint of a physical observer.

Let $(X,\mu)$ be a spacetime. Let $\phi: V \subset X \to \mathbb{R}^4$ be a chart of $X$ such that there is an open, simply connected subset $U \subset \V$ with vanishing [[stress-energy tensor]] $T$ in $U$.

Assume that there are two points $a, b \in U$ such that the curvature vanishes in a neighborhood of $a$ and does not vanish $b$.

_remark_: In the terms of [[diffenential geometry]] $X$ is [[Ricci flat]] in $U$ and flat in a neighborhood of $a$. 

Given these assumptions, there is a diffeomorphism $\psi: X \to X$ reducing to the identiy outside of $U$, with $\psi(a) = b$. Let $\mu' = \psi^*(\mu)$ be the pullback of $\mu$ along $\psi$. Since the field equations of [[General Relativity]] are covariant, both $\mu$ and $\mu'$ are solutions to the field equations. So one observer will say that there is no gravitation at the spacetime point $a$, while another will say there is.

From the _mathematical_ viewpoint this is a rather trivial observation, namely that in the category of spacetimes it would be [[evil]] to consider field equations that are not covariant, and that the field equations of [[General Relativity]] are not [[evil]] because they are covariant.

The argument troubled Einstein however, because he supposed that the statement "at a certain region in time and space, there is (or isn't) gravitation" should have an objective, observer independent meaning, wether or not there is matter present that "feels" the influence of gravitation. This assumption is based on the Newtonian notions of the absolute, objective existence of space and time. For Newton's physics, space and time exist independently of any observers and of any objects that are present in time and space. If one adds a structure that models gravitation to space and time in this sense, the statement "at a certain region in time and space, there is (or isn't) gravitation" is independent of observers and of the presence of further content (or structures) like matter. 

The conclusion of Einstein and therefore of [[General Relativity]] was however that the statement "at a certain region in time and space that contains no matter, there is (or isn't) gravitation" is _not_ independent of the observer. This means that the _physical_ notions of space and time do not have the same objective meaning as in Newton's physics.


+-- {: .query}
[[Tim van Beek]]: This paragraph could of course be taken to the [[General Relativity]] page...
=--

####References

* see Wikipedia on the [hole argument] (http://en.wikipedia.org/wiki/Hole_argument)

###intermingling of space and time
The noun "spacetime" is used in both [[Special Relativity]] and [[General Relativity]], but is best motivated from the viewpoint of [[General Relativity]]. [[Special Relativity]] deals with the [[Minkowski spacetime]] only. The [[Minkowski spacetime]] allows a _canonical_ choice of _global_ coordinates such that the metric tensor has in every point the form diag(-1, 1, 1, 1), which identifies the first coordinate as representing the time coordinate and the others as representing space coordinates.

Given a general spacetime, there is not necessarily a globally defined coordinate system, and therefore not necessarily a globally defined _canonical_ time coordinate. More specifically, there are spacetimes that admit coordinates defined on subsets where the _physical_ interpretation of the coordinates as modelling time and space coordinates _changes_ over the domain of definition.

(TODO: references and explanations).

[[!redirects space-time]]
[[!redirects space time]]