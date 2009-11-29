[[!redirects exponential law for based spaces]]
When in a [[convenient category of topological spaces]], e.g. [[compactly generated space]]s, there is an [[adjunction]] between the mapping space and the product in that category.
For general [[topological space]]s there is no globally defined adjunction, instead we need some conditions. Here is the statement containing all the subtleties.

**Teorem (Exponential law).** Let
$X,Y,B$ be topological spaces. For any $f\in B^{X\times Y}$,
formula
$$
[(\theta f)(y)](x) = f(x,y)
$$
defines **continuous** map $(\theta f)(x):Y\to B^X$
which we call the map adjoint to $f$.
The adjunction map
$$
\theta : Map(X\times Y,B)\to Map(Y,B^X), \,\,\,\,\,\,\,\theta:f\mapsto \theta f
$$
is 1-1, and if $X$ is locally compact and Hausdorff then $\theta$ is bijection.
Independently from that assumption on $X$, if $Y$ is
Hausdorff, then $\theta$ is continuous in the [[compact-open topology]]
$$
\theta : B^{X\times Y}\to (B^X)^Y.
$$
If both assumptions (on $X$ and $Y$) are satisfied, then
$\theta$ is not only a continuous bijection, but also open, hence a homeomorphism.

There is also a version for based (=[[pointed object|pointed]]) topological spaces. The cartesian product then needs to be replace by the smash product of the based spaces. Regarding that the maps preserve the based point, the adjunction map $\theta$ induces the adjunction map

 $$\theta':Map_*(X\wedge Y,B)\to Map_*(Y,B^X)$$

where the mapping space $Map_*$ for based spaces is the subspace of the usual mapping space in compact-open topology, which consists only of the mapping preserving the based point. 

It appears, that $\theta'$ is again 1-1 and continuous, and it is bijective if $X$ is locally compact Hausdorff. If $Y$ is also Hausdorff then $\theta'$ is a homeomorphism. 

[[!redirects exponential law for topological spaces]]