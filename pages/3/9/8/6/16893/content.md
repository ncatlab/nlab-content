[[!redirects spectral analytic geometry]]
[[!redirects spectral analytic spaces]]
[[!redirects spectral analytic space]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

If one thinks of [[global analytic geometry]] as a theory based on the study of monoids in the monoidal category of Banach modules over a base Banach ring (e.g., $(\mathbb{Z},|\cdot|_\infty)$), it is quite tempting to look for a geometric theory of the associated cohomology theories, that one may call spectral global analytic geometry.

A first step in this direction of a good homotopy theory for global analytic spaces (that would be useful for the study of their cohomological invariants) would be to work with spectral rings in the symmetric monoidal category of Banach modules (over a given fixed Banach ring).

However, one would like the theory not to depend on the choice of a particular Banach ring, because it is also desirable to be invariant by the natural power action of $\mathbb{R}_+^*$ on [[proxi-Banach ring|Banach proxi-norms]], that are multiplicative maps that fulfill the weak triangular inequality
$$
|a+b|\leq \max(|2|,|1|)\cdot \max(|a|,|b|).
$$

A possible research direction is to look at Gromov's ideas about metric homotopy theory: one may try to define a category of geometric objects whose homotopy groups are naturally equipped with Banach pseudo-norms. If one looks for non-linear versions of Banach spaces, it is natural to look at metric spaces with Lipschitz maps between them (because their sets of maps are equipped with a natural "norm"). So one may try to develop global analytic homotopy theory (a way to look for interesting cohomological invariants for global analytic spaces, such as [[topological cyclic homology]] or [[topological derived de Rham cohomology]]) by developing the stable homotopy theory of metric spaces.

## Constraints

A natural very small set of constraints for a relaxed approach to the homotopy theory of metric spaces is the following:

* A metrized ring spectrum should be "something like" a commutative ring spectrum $A$ together with norms on its homotopy groups such that $\pi_0(A)$
is a seminormed ring and $\pi_i(A)$ is a seminormed module over $\pi_0(A)$ for all $i$.

* Having a metric ring sphere spectrum $\mathbb{S}$ such that $\pi_0(\mathbb{S})=(\mathbb{Z},|\cdot|_\infty)$.

* Having a natural action of $\mathbb{R}_+^*$ on the homotopy category (this is not contradictory with the previous constraint: one actually needs a family of sphere ring spectra, or its limit, that would have $\pi_0(\mathbb{S})=(\mathbb{Z},|\cdot|_\infty^\infty)$, in the sense of pro-objects).

* Getting back the homotopy theory of spectral Banach modules when one works over a fixed base Banach ring.

* To each spectrum, one associated a cohomology theory with values in complete ind-Banach modules over a given Banach ring.

## Objectives

One would like to be able to define "de Rham-like coefficients" over arbitrary global analytic spaces, even in mixed characteristic. One may hope (following Hesselholt, Connes and Bhatt/Scholze/Morrow) that topological coefficients (such as topological cyclic homology and topological derived de Rham/Andr&#233;-Quillen cohomology) may be a first step in this very optimistic direction.
Indeed, they seem to take care of something like Buium's differential calculus along the integers, and thus also of Witt vector constructions, in a completely canonical way.

## Constructions

To develop a homotopy theory for metric spaces, we first need a category of "metric spaces" that has all limits and colimits (usual metric spaces don't even have finite coproducts). One may then develop the associated stable homotopy theory by the usual methods, once fixed a metric on the interval $[0,1]$. To get a theory that is $\mathbb{R}_+^*$-invariant, one actually needs to equip $[0,1]$ with the limit of the family of [[proxi-metric space|proxi-metrics]]
$$d_\infty^t(x,y):=|x-y|_\infty^t$$
as $t$ goes to $\infty$.
This formal limit makes sense in a convenient category of metric spaces, where one keeps some track of the finite level $t$ information.

## References

This nlab page.