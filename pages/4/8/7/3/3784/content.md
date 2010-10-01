
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
=--
=--




#Contents#
* automatic table of contents goes here
{:toc}


##Idea
A **spacetime** is a [[smooth Lorentzian space]] $(X,\mu)$ equipped with a time orientation (see there).

In the context of classical [[general relativity]] a **spacetime** is usually in addition assumed to be connected and four-dimensional.

In [[classical physics]], notably in [[special relativity]] and [[general relativity]] points in $X$ model coordinates where _events_ can take place from the viewpoint of an observer ("points in space and time") while the metric $\mu$ models the field of [[gravity]] in [[general relativity]].

###Remark on the physical meaning of points in General Relativity, Einstein's "hole argument"

####Idea
The hole argument elaborates on the meaning of covariance in the _physical_ interpretation of the theory of [[general relativity]], it was of crucial importance for Einstein when he considered the question if the field equations should be covariant with respect to the full diffeomorphism group of a spacetime.

#### The argument

In [[general relativity]], every chart of the [[atlas]] of the given spacetime represents the viewpoint of a physical observer.

Let $(X,\mu)$ be a [[spacetime]]. Let $\phi: V \subset X \to \mathbb{R}^4$ be a chart of $X$ such that there is an open, simply connected subset $U \subset \V$ with vanishing [[stress-energy tensor]] $T$ in $U$.

Assume that there are two points $a, b \in U$ such that the curvature vanishes in a neighborhood of $a$ and does not vanish near $b$. This means in terms of the [[differential geometry]] describing the situation that the [[pseudo-Riemannian metric]] $\mu$ on $X$ is [[Ricci-flat metric|Ricci flat]] when restricted to $U$ and flat when restricted to a neighborhood of $a$. 

Given these assumptions, there is a [[diffeomorphism]] $\psi: X \stackrel{\simeq}{\to} X$ (an [[isomorphism]] in [[Diff]]) reducing to the identity outside of $U$, with $\psi(a) = b$. Let $\mu' = \psi^*(\mu)$ be the pullback of $\mu$ along $\psi$. Since the field equations of [[general relativity]] are covariant (respect [[isomorphism]]s in the category of [[pseudo-Riemannian manifold]]s), both $\mu$ and $\mu'$ are solutions to the field equations. So one observer will say that there is no gravitation at the spacetime point $a$, while another will say there is.

In fact, strictly speaking no observer will say anything like this, because it is impossible to characterize a single point $a$ in a [[spacetime]] in particular and in any [[manifold]] in general in an intrinsic way, without referring to extra structure: given a bare [[manifold]] $X$, a point $a$ in it is a [[morphism]] $x : {*} \to X$ in [[Diff]], a [[generalized element]] of $X$. But under an [[automorphism]] $X \stackrel{\simeq}{\to} X$ of $X$ in [[Diff]], this point is taken to any other point $b : * \stackrel{a}{\to} X \stackrel{\simeq}{\to} X$. So when regarded just by its probes by $*$, a manifold appears just as a bare [[set]] of points, with no interrelation. It is [[evil]] to try to distinguish these points, because in the [[slice category]] $(*,X)$ of elements, they are all isomorphic.

Rather, what really does characterize the [[manifold]] underlying a [[spacetime]] is its collection of all probes by the test spaces $\mathbb{R}^n$, i.e. by all morphisms $\mathbb{R}^n \to X$ in [[Diff]] and their relation among each other. The collection of information encoded by these probes yields the [[sheaf]] $\bar X := Hom_{Diff}(-,X) :$ [[CartSp]]${}^{op} \to Set$, and this does characterize the full structure of the manifold. For more on this see [[diffeological space]].

On the other hand, if there is extra structure available on the manifold $X$, such that for instance a "scalar field", i.e. a smooth function $\phi : X \to \mathbb{R}$, and if we take morphisms of such manifolds to respect this extra structure, then it is possible to intrinsically in an non-[[evil]] way characterize for instance the sub-set of points on which $f$ takes a fixed value. The scalar curvature invariants of a pseudo-Riemannian metric on $X$ do play such a role, and thus induce intrinsic observable structure. So what matters in the above example is not that one point is called $a$ and one is called $b$, but that at one point the Ricci curvature function vanishes, and at the other not. As a [[diffeomorphism]] is applied to the manifold, the points may be re-identitfied, but if the Ricci curvature vanished at one point before it will vanish at the re-identified point after the re-identitfication, and hence still characterizes that as one of the points where the Ricci curvature vanishes. So the apparent paradox in the above arises from insisting that $a$ is $a$ and $b$ is $b$ even after applying a diffeomorphism. This is [[evil]]. The diffeomorphism identifies $a$ with $b$ and $b$ with $a$ instead.

Notice that this argument has really nothing specifically to do with physics or general relativity. The analogue of what is said here about pseudo-Riemannian manifolds could be said about, say, [[symplectic manifold]]s or whatever.

So from the [[nPOV]] there is no mystery here, but the above argument originally troubled Einstein, because at his time it was felt that it violates the demand that the statement "at a certain region in time and space, there is (or isn't) gravitation" should have an objective, observer independent meaning, wether or not there is matter present that "feels" the influence of gravitation. This assumption is based on the Newtonian notions of the absolute, objective existence of space and time. For Newton's physics, space and time exist independently of any observers and of any objects that are present in time and space. If one adds a structure that models gravitation to space and time in this sense, the statement "at a certain region in time and space, there is (or isn't) gravitation" is independent of observers and of the presence of further content (or structures) like matter. 

The conclusion of Einstein and therefore of [[general relativity]] was however that the statement "at a certain region in time and space that contains no matter, there is (or isn't) gravitation" is _not_ independent of the observer. This means that the _physical_ notions of space and time do not have the same objective meaning as in Newton's physics.

On the other hand, the conclusion that one draws from the [[nPOV]] is a simpler and much more general one: it is [[evil]] to try to identify objects in a category in a way that does not respect their [[isomorphism]]s. 

+-- {: .query}
[[Tim van Beek]]: This paragraph could of course be taken to the [[general relativity]] page...
=--

####References

* see Wikipedia on the [hole argument] (http://en.wikipedia.org/wiki/Hole_argument)

### Intermingling of space and time
The noun "spacetime" is used in both [[special relativity]] and [[general relativity]], but is best motivated from the viewpoint of [[general relativity]]. [[special relativity|Special relativity]] deals with the [[Minkowski spacetime]] only. The [[Minkowski spacetime]] allows a _canonical_ choice of _global_ coordinates such that the metric tensor has in every point the form diag(-1, 1, 1, 1), which identifies the first coordinate as representing the time coordinate and the others as representing space coordinates.

Given a general spacetime, there is not necessarily a globally defined coordinate system, and therefore not necessarily a globally defined _canonical_ time coordinate. More specifically, there are spacetimes that admit coordinates defined on subsets where the _physical_ interpretation of the coordinates as modelling time and space coordinates _changes_ over the domain of definition.

(TODO: references and explanations).

## Examples

* [[Minkowski spacetime]]

* [[black hole spacetime]]

  * [[Schwarzschild spacetime]]

  * [[Kerr spacetime]] 

...

[[!redirects space-time]]
[[!redirects space time]]
[[!redirects spacetimes]]
