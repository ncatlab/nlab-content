#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of _Eilenberg--Mac Lane object_ in an [[(∞,1)-topos]] or [[stable (∞,1)-category]] generalizes the notion of [[Eilenberg?Mac Lane space]] from the [[(∞,1)-topos]] [[Top]] of [[topological space]]s or the [[stable (∞,1)-category]] of [[spectrum|spectra]]:

it is an object $\mathbf{B}^n A$ obtained from an abelian [[group object]] $A$ by [[delooping]] that $n$ times.


The standard [[model category|model]] for these Eilenberg--Mac Lane objects are nothing but the familiar Eilenberg--Mac Lane _[[sheaf|sheaves]]_ of fame in [[abelian sheaf cohomology]].

For recall that every $(\infty,1)$-[[(infinity,1)-topos|topos]] is [[presentable (infinity,1)-category|presented]] by a [[model structure on simplicial presheaves|model category of simplicial sheaves]].

Under the [[Dold?Kan correspondence]] 

$$
  N : SimpAb \stackrel{\leftarrow}{\to} Ch_+ : \Gamma
$$

[[chain complex]]es $A[n]$ of abelian groups concentrated in degree $n$ map into [[simplicial set]]s 

$$
  K(A,n) := \Gamma(A[n])
$$

and these to the corresponding constant simplicial sheaves (on whatever [[site]]) that we denote by the same symbol, for convenience.

Regarding the simplicial sheaf $K(A,n)$ as an object of the $(\infty,1)$-[[(infinity,1)-topos|topos]] [[presentable (infinity,1)-category|presented]] by the given [[model structure on simplicial presheaves|model structure on simplicial sheaves]] means regarding them as the $\infty$-[[infinity-stack|stacks]] that they correspond to under $\infty$-[[infinity-stackification|stackification]]. These are then the **Eilenberg--Mac Lane object**s in our [[(∞,1)-topos]].

## Cohomology

From the general nonsense at [[cohomology]] and comparing with the case [[Eilenberg?Mac Lane space]]s, we see that for $\mathbf{H}$ our $(\infty,1)$-[[(infinity,1)-topos|topos]], for $H$ its [[homotopy category of an (infinity,1)-category|homotopy category]] and for $X \in \mathbf{H}$ any object, the "ordinary" degree $n$-[[cohomology]] of $X$ is

$$
  H^n(X, \mathbb{Z}) := H(X, K(\mathbb{Z},n))
  \,.
$$

## References

top of page 4 of

* Jardine, _Fields Lectures: Simplicial Presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))


[[!redirects Eilenberg-MacLane object]]
[[!redirects Eilenberg?MacLane object]]
[[!redirects Eilenberg--MacLane object]]
[[!redirects Eilenberg-Mac Lane object]]
[[!redirects Eilenberg?Mac Lane object]]
[[!redirects Eilenberg--Mac Lane object]]
[[!redirects Eilenberg-MacLane objects]]
[[!redirects Eilenberg?MacLane objects]]
[[!redirects Eilenberg--MacLane objects]]
[[!redirects Eilenberg-Mac Lane objects]]
[[!redirects Eilenberg?Mac Lane objects]]
[[!redirects Eilenberg--Mac Lane objects]]