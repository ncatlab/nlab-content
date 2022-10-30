
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

[[configuration space|Configuration spaces]] in [[physics]] are typically not just plain spaces, but are [[groupoid]]s and generally [[∞-groupoid]]s. This is traditionally most familiar for configuration spaces of [[gauge theory|gauge theories]]:

* the [[object]]s are the (field-)configurations of the physical system;

* the [[morphism]]s between objects are [[gauge transformation]]s between different but equivalent field configurations;

* the [[k-morphism]]s are "gauge-transformations of gauge transformation": 

  (these higher order gauge transformations are in the traditional physics literature mainly known in their infinitesimal approximation where the configuration [[Lie ∞-groupoid]] is approximated by a [[Lie-∞-algebroid]] whose [[schreiber:Chevalley-Eilenberg algebra]] is the [[BRST complex]]: here they correspond to _ghosts of ghosts_ ).

The operation called **gauge fixing** can essentially be understood as the passage to a more [[skeleton|skelatized]] [[∞-groupoid]]: in the simplest case, it amounts to picking one representative configuration from each equivalence class.

Generally, since the configuration [[∞-groupoid]] typically carries extra structure in that it is a [[topological ∞-groupoid]] or a [[Lie ∞-groupoid]] or the like, the choice of **gauge slice** as it is called is similarly required to preserve that structure.

## Examples

Standard textbook examples of gauge fixings include the following:

* in the [[gauge theory]] of the **[[electromagnetic field]]**, a field configuration is, on a given [[pseudo-Riemannian manifold]] a [[line bundle]] [[connection on a bundle|with connection]]. Often the special case is considered where the underlying manifold is just [[Minkowski space]] and the bundle is assumed to be trivial, in which case a configuration of the gauge field configuration is just a [[differential form|1-form]] $A$ on Minkowski space, and a gauge transformation $\lambda: A \to A'$ is a 0-form, i.e. a function, such that $A' = A + d \lambda$.

  * in the **[[Lorenz gauge]]** the gauge field $A$ is taken to be a [[harmonic form|harmonic]] 1-form $d \star d \star A = 0$.

## Category-theoretic description

Here are more details on how one may think of gauge fixing from the [[nPOV]].

In the [[Quantization as a Kan Extension|Freed and Alm-Schreiber approach to quantization]], the [[action functional]] is a [[functor]] 
$$
e^{\mathrm{i}S}:X \to nVect,
$$ 
where $X$ is some $(\infty,n)$-groupoid called the _space of fields_. The space of fields comes equipped with a projection $\pi:X\to M$ to an $(\infty,n)$-groupoid $M$ called the _moduli space_ of the quantum theory. Then the (path integral) quantization is, if it exists, the [[Kan extension]] $Z:M\to nVect$ of $e^{\mathrm{i}S}$ along $\pi$. The functor $Z$ is customary called the _partition function_ of the theory. 

A **gauge fixing** is a choice of a subgroupoid $X_{gf}$ of $X$ such that the inclusion $X_{gf}\hookrightarrow X$ is an equivalence. The basic idea of gauge fixing is that the gauge fixed partition functions $Z_{gf}$, when they exist, are independent of the particular gauge fixing (since gauge fixing are all equivalent each other) and are equivalent to the original partition function $Z$ (since $X_{gf}$ is equivalent to $X$).

A classical instance of gauge fixing is when $X=\tilde{X}//G$ is an action groupoid, for the action of some group $G$ (the gauge group) on a manifold $\tilde{X}$. In this case a classical gauge fixing is the choice of a _slice_ $S$ in $\tilde{X}$ intersecting each orbit of $G$ exactly once. If the action of $G$ on $\tilde{X}$ is not free, there still will be nontrivial automorphisms in the groupoid $S//G$; these residual internal symmetries are sometimes called _ghost symmetries_

### Classical gauge fixings

* [[BRST complex]]
* [[BV theory]]
  
## Examples

* [[temporal gauge]]
* [[Lorenz gauge]]
* [[Coulomb gauge]]
* Feynman gauge
* light cone gauge

## Related concepts

* [[gauge group]], [[gauge transformation]]
* [[spontaneously broken symmetry]]
* [[Gribov ambiguity]]

[[!redirects gauge fixings]]
     