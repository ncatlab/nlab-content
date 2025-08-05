
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

When the [[theory]] of [[gravity]] in the form of _[[general relativity]]_ was developed at the beginning of the 20th century, the abstract notion of a [[smooth manifold]] independently of its [[coordinate charts]] was still unfamiliar. Theories like that of [[electromagnetism]] were traditionally all formulated with respect to what today would be called a choice of [[coordinate patch]]. The development of [[general relativity]] by [[Albert Einstein]] went through a phase in which what is now called the principle of _[[general covariance]]_ was only gradually understood.

The "hole argument" or "hole [[paradox]]", which was put forward in ([Einstein-Grossmann](#EinsteinGrossmann)), is the observation that given a [[pseudo-Riemannian metric|pseudo]]-[[Riemannian metric]] $g$ on some [[spacetime]] $X$ -- hence a field configuration of [[gravity]], and given a point $x : * \to X$ and a [[diffeomorphism]] $\phi : X \stackrel{\simeq}{\to} X$, in general the value of $g$ around $x$ is entirely unrelated to the value of the [[pullback of a cotensor|pullback]] metric $\phi^* g$ at $x$. 

This was regarded as a source of puzzlement for a while -- a "[[paradox]]" -- because if one thinks that the point $x$ in $X$ is absolutely fixed (the locus of an "observer" in spacetime) and that two metrics related by a [[diffeomorphism]] as above are equivalent field configurations, it would seem that the field of gravity "at $x$" is undetermined and undeterminable. For a while this reasoning was regarded as an obstacle to the idea of [[general covariance]] and indeed in ([Einstein-Grossmann](#EinsteinGrossmann)) the notion of general covariance was still rejected in view of this.

But of course the value of the metric $g$ at $x$ _does_ coincide with that of $\phi^* g$... at the transformed point $\phi(x)$. An attempt at more words on this is below in [Discussion](#Discussion).




## The "hole argument"
 {#TheArgument}

The original argument was formulated more in detail along the following lines.

In [[general relativity]], every chart of the [[atlas]] of the given spacetime represents the viewpoint of a physical observer.

Let $(X,\mu)$ be a [[spacetime]]. Let $\phi: V \subset X \to \mathbb{R}^4$ be a chart of $X$ such that there is an open, simply connected subset $U \subset \V$ with vanishing [[stress-energy tensor]] $T$ in $U$.

Assume that there are two points $a, b \in U$ such that the curvature vanishes in a neighborhood of $a$ and does not vanish near $b$. This means in terms of the [[differential geometry]] describing the situation that the [[pseudo-Riemannian metric]] $\mu$ on $X$ is [[Ricci-flat metric|Ricci flat]] when restricted to $U$ and flat when restricted to a neighborhood of $a$. 

Given these assumptions, there is a [[diffeomorphism]] $\psi: X \stackrel{\simeq}{\to} X$ (an [[isomorphism]] in [[Diff]]) reducing to the identity outside of $U$, with $\psi(a) = b$. Let $\mu' = \psi^*(\mu)$ be the pullback of $\mu$ along $\psi$. Since the field equations of [[general relativity]] are covariant (respect [[isomorphism]]s in the category of [[pseudo-Riemannian manifold]]s), both $\mu$ and $\mu'$ are solutions to the field equations. So one observer will say that there is no gravitation at the spacetime point $a$, while another will say there is.

## Discussion
 {#Discussion}

As is often the case when confused about automorphisms, it clarifies the issue to talk about more general *isomorphisms* first.  Thus, consider two different manifolds $X$ and $Y$ and a diffeomorphism $\psi:Y\cong X$, with metric $\mu$ on $X$ and pulled back metric $\mu' = \psi^*(\mu)$ on $Y$.  Then $(X,\mu)$ and $(Y,\mu')$ represent the same physical reality, with $\psi$ as a witness of this fact.  In particular, if $\psi(a)=b$, then the gravitational field at $a$ in $Y$ will coincide with the gravitational field at $b$ in $X$, as it should be since both represent the same point of spacetime.

Now suppose we have another diffeomorphism $\phi:Y\cong X$.  Then in general $\mu'$ will be different from $\phi^*(\mu)$, and therefore there is no reason that the gravitational field at $a$ in $Y$ will coincide with the gravitational field at $\phi(a)$ in $X$.  This should still be obvious.  But the "hole paradox" now arises when we take $X$ and $Y$ to be the same and $\phi$ to be the identity map.

In other words, if we have used some isomorphism $\psi$ to witness that two manifolds represent the same reality, then we can't "switch halfway through" our argument and start identifying them along some different isomorphism $\phi$.  This is true even if the two manifolds are the same and $\phi$ is the identity.

Notice that this argument has really nothing specifically to do with physics or general relativity. The analogue of what is said here about pseudo-Riemannian manifolds could be said about, say, [[symplectic manifold]]s or whatever.

So from the [[nPOV]] there is no mystery here, but the above argument originally troubled Einstein, because at his time it was felt that it violates the demand that the statement "at a certain region in time and space, there is (or isn't) gravitation" should have an objective, observer independent meaning, whether or not there is matter present that "feels" the influence of gravitation. This assumption is based on the Newtonian notions of the absolute, objective existence of space and time. For Newton's physics, space and time exist independently of any observers and of any objects that are present in time and space. If one adds a structure that models gravitation to space and time in this sense, the statement "at a certain region in time and space, there is (or isn't) gravitation" is independent of observers and of the presence of further content (or structures) like matter. 

The conclusion of Einstein and therefore of [[general relativity]] was however that the statement "at a certain region in time and space that contains no matter, there is (or isn't) gravitation" is _not_ independent of the observer. This means that the _physical_ notions of space and time do not have the same objective meaning as in Newton's physics.

On the other hand, the conclusion that one draws from the [[nPOV]] is a simpler and much more general one: when identifing isomorphic objects in a category, we have to remember which isomorphism we used. For a formulation of the situation in terms of [[homotopy type theory]] see the relevant section in [general covariance](general+covariance#InHomotopyTypeTheory).


## Related concepts

* [[general covariance]]

## References

The original discussion:

* {#EinsteinGrossmann} [[Albert Einstein]], M. Grossmann: _Entwurf einer verallgemeinerten Relativit&#228;tstheorie und einer Theorie der Gravitation_ Zeitschrift f&#252;r Math. Phys. 62, 225&#8211;259 (1914)
 
Review:

* [[Sebastian De Haro]], [[Jeremy Butterfield]], section 10.1 in: 
*The Philosophy and Physics of Duality*, Cambridge University Press (2025) &lbrack;[arXiv:2508.01616](https://arxiv.org/abs/2508.01616), [ISBN:9780198846338](https://global.oup.com/academic/product/the-philosophy-and-physics-of-duality-9780198846338)&rbrack;
  > (with an eye towards relating to [[AdS/CFT duality]])

* Wikipedia: _[Hole argument] (http://en.wikipedia.org/wiki/Hole_argument)_

A treatment in terms of [[HoTT]]:

* [[John Dougherty]], _The Hole Argument, take n_, Foundations of Physics (2019), ([doi](https://doi.org/10.1007/s10701-019-00291-x)).



[[!redirects hole paradox]]
