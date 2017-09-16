#Idea#

Recall that an [[Eilenberg-MacLane space]] is a special [[object]] in the [[(infinity,1)-topos]] [[Top]] of [[topological space]]s.

This has an analog in arbitrary [[(infinity,1)-topos]]es (if [[infinity-stack]]s). The standard [[model category|model]] for these Eilenberg-MacLane objects are nothing but the familiar Eilenberg-MacLane _[[sheaf|sheaves]]_ of fame in [[abelian sheaf cohomology]].

For recall that every [[(infinity,1)-topos]] is [[presentable (infinity,1)-category|presented]] by a [[model structure on simplicial presheaves|model category of simplicial sheaves]].

Under the [[Dold-Kan correspondence]] 

$$
  N : SimpAb \stackrel{\leftarrow}{\to} Ch_+ : \Gamma
$$

[[chain complex]]es $A[n]$ of abelian groups concentrated in degree $n$ map into [[simplicial set]]s 

$$
  K(A,n) := \Gamma(A[n])
$$

and these to the corresponding constant simplicial sheaves (on whatever [[site]]) that we denote by the same symbol, for convenience.

Regarding the simplicial sheaf $K(A,n)$ as an object of the [[(infinity,1)-topos]] [[presentable (infinity,1)-category|presented]] by the given [[model structure on simplicial presheaves|model structure on simplicial sheaves]] means regarding them as the [[infinity-stack]]s that they correspond to under [[infinity-stackification]]. These are then the **Eilenberg-MacLane object**s in our [[(infinity,1)-topos]].

#Cohomology#

From the general nonsense at [[cohomology]] and comparing with the case [[Eilenberg-MacLane space]]s, we see that for $\mathbf{H}$ our [[(infinity,1)-topos]], for $H$ its [[homotopy category of an (infinity,1)-category|homotopy category]] and for $X \in \mathbf{H}$ any object, the "ordinary" degree $n$-[[cohomology]] of $X$ is

$$
  H^n(X, \mathbb{Z}) := H(X, K(\mathbb{Z},n))
  \,.
$$

#References#

top of page 4 of

* Jardine, _Fields Lectures: Simplicial Presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))