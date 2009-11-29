
When in a [[convenient category of topological spaces]], e.g. [[compactly generated space]]s, there is an [[adjunction]] between the mapping space and the product in that category.
For general [[topological space]]s there is no globally defined adjunction, instead we need some conditions. Here is the statement containing all the subtleties.


+-- {: .query}
In what sense is the map $\theta f$ below continuous?  I mean, what is the topology on $B^X$?  You don\'t introduce the compact--open topology until later, but that\'s the topology that I would guess is relevant.  ---Toby
=--

+-- {: .un_theorem}
###### Theorem (Exponential law)
Let
$X,Y,B$ be [[topological spaces]]. For any $f\in B^{X\times Y}$,
the formula
$$
[(\theta f)(y)](x) = f(x,y)
$$
defines a [[continuous map]] $\theta f:Y\to B^X$
which we call the map adjoint to $f$, or the [[adjunct]] of $f$.

The adjunction map
$$
\theta : Map(X\times Y,B)\to Map(Y,B^X), \,\,\,\,\,\,\,\theta:f\mapsto \theta f
$$
is a [[one-to-one function]], and if $X$ is [[locally compact space|locally compact and Hausdorff]] then $\theta$ is a [[bijection]].
Independently from that assumption on $X$, if $Y$ is
[[Hausdorff space|Hausdorff]], then $\theta$ is continuous in the [[compact-open topology]]
$$
\theta : B^{X\times Y}\to (B^X)^Y.
$$

If both assumptions (on $X$ and $Y$) are satisfied, then
$\theta$ is not only a continuous bijection, but also open, hence a [[homeomorphism]].
=--

There is also a version for based (= [[pointed space|pointed]]) topological spaces. The [[cartesian product]] then needs to be replace by the [[smash product]] of the based spaces. Regarding that the maps preserve the base point, the adjunction map $\theta$ induces the adjunction map

 $$\theta_*:Map_*(X\wedge Y,B)\to Map_*(Y,B^X)$$

where the mapping space $Map_*$ for based spaces is the subspace of the usual mapping space, in compact--open topology, which consists of the mappings preserving the base point. 

It appears that $\theta_*$ is again one-to-one and continuous, and it is bijective if $X$ is locally compact Hausdorff. If $Y$ is also Hausdorff then $\theta_*$ is a homeomorphism. 


[[!redirects exponential law for topological spaces]]
[[!redirects exponential law for based spaces]]