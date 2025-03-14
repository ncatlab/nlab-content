
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

It is well known that when the [[higher dimensional Chern-Simons theory|higher Chern-Simons term]] in [[11-dimensional supergravity]] is [[KK-compactification|compactified]] on a [[4-sphere]] to yield the [[7-dimensional Chern-Simons theory]] which inside [AdS7/CFT6](AdS-CFT#AdS7CFT6) is [[duality in string theory|dual]] to the [[M5-brane]] [[6d (2,0)-superconformal QFT]], the [[cup product]] square in [[ordinary differential cohomology]] that enters its definition is to receive a [[quadratic refinement]]. This was originally argued in [Witten 97](http://ncatlab.org/nlab/show/7d+Chern-Simons+theory#Witten97) and then formalized and proven in [[Quadratic Functions in Geometry, Topology, and M-Theory|Hopkins-Singer 02]].

What though is the situation up in 11 dimensions before compactifying to 7-dimensions?

In [DFM 03, section 9](supergravity+C-field#DiaconescuFreedMoore03) it is claimed that the full 11-dimensional Chern-Simons term evaluated on the [[supergravity C-field]] (with its [[flux quantization]] correction, see there) indeed carries a _cubic refinement_.

More precisely, and slightly paraphrasing, the [[fiber integration in ordinary differential cohomology|transgression]] $\int_X CS_{11}(\hat C)$ of the [[higher dimensional Chern-Simons theory|11-dimensional Chern-Simons term]] of [[11-dimensional supergravity|11d SuGra]]  to 10d spacetime $X$ is a [[complex line bundle]] on the [[moduli space]] $CField(X)$ of [[supergravity C-field|supergravity C-fields]] $\hat C$ is claimed to be such that its "cubical line" $\Theta(\int_X CS_{11}(\hat C))$ (in the notation at _[[cubical structure on a line bundle]]_) is the  line bundle on the space of triples of C-field configurations which is given by the transgression of the three-fold [[cup product in ordinary differential cohomology]], 

$$
  \Theta\left(\int_X CS_{11}\left(-\right)\right)
  \simeq
  \int_X (-)_1 \cup (-)_2 \cup (-)_3
  \,.
$$


## Relation to F-theory and the topological Witten genus

In the context of "[[F-theory]] compactifications" of [[M-theory]], one considers [[supergravity C-field|C-fields]] on an [[elliptic fibration]] which are "factorizable fluxes", in that their underlying [[cocycle]] $\hat C$ in [[ordinary differential cohomology]] is the [[cup product in ordinary differential cohomology|cup product]] of a cocycle $\hat C_{fib}$ on the fiber with one $\hat C_b$ on the base

$$
  \hat C \coloneqq \hat C_{b} \cup \hat C_{fib}
 \,.
$$

In approaches like [GKP 12 (around p. 19)](F-theory#GKP12) and [KMW 12](F-theory#KMW12) the [[supergravity C-field|C-field]] is factored as a [[cup product in ordinary differential cohomology|cup product]] of a degree-2 cocycle on the elliptic fiber with a degree-2 class in the [[Calabi-Yau space|Calabi-Yau]]-base. This makes the component of the C-field on the elliptic fiber a [[complex line bundle]] (with [[connection on a bundle|connection]]). Notice that the space of complex line bundles on an elliptic curve is dual to the elliptic curve itself.

On the other hand in  e.g. [DFM 03, p. 38](supergravity+C-field#DiaconescuFreedMoore03) the factorization is  taken to be that of two degree-3 cocycles in the base (which are then identified with the combined degree-3 [[RR-field]]/[[B-field]] flux coupled to the [[(p,q)-string]]) with, respectively, the two canonical degree-1 cocycles $\hat t_i$ on the elliptic fiber which are given by the two canonical coordinate functions $t_i$ (speaking of a [[framed elliptic curve]]). In this case the fiber-component of the [[supergravity C-field]] "is" the [[elliptic curve]]-fiber, 

$$
  \hat C \coloneqq \hat B_{NS} \cup \hat t_1 + \hat B_{RR} \cup \hat t_2
$$

or equivalently each point in the moduli space of $H$-flux in 10d induces an identification of the $G$-flux with the elliptic curve this way.



This is maybe noteworthy in that when the [[supergravity C-field|C-field]] is identified with the compactification  [[elliptic curve]] in this way, then the formula for $\Theta\left(\int_X CS_{11}(\hat C)\right)$ as [above](#Idea) is exactly that appearing in the definition of a [[cubical structure on a line bundle]] over an [[elliptic curve]]. But a "cubical" trivialization of $\Theta(\mathcal{O}(-\{0\}))$ over a given elliptic curve is what in ([Hopkins 02](string+orientation+of+tmf#Hopkins02), [AHS01](string+orientation+of+tmf#AndoHopkinsStrickland01)) is used to induce the [[sigma-orientation]] of the corresponding [[elliptic cohomology theory]] and in totality the [[string-orientation of tmf]]. But that is the refinement of the [[Witten genus]], hence of the [[partition function]] of the [[heterotic string]].

Now, by the above fact that $\Theta\left(CS_{11}(-)\right) \simeq \int_X (-)_1 \cup (-)_2 \cup (-)_3$, a cubical trivialization of $\Theta(L)$ is also given by a trivialization of the topological class of the C-field. This is one way (or is at least closely related) to the trivialization of the anomaly line bundle which "sets the quantum integrand" of M-theory.

So there is a curious coincidence of concepts here, which might want to become a precise identification: 

on the one hand there is naturally a [[cubical structure on a line bundle]] on the Chern-Simons line bundle over the moduli space of [[supergravity C-fields]] which for [[F-theory]] compactifications and factorizable flux configurations induces in particular a cubical structure on a line bundle over the compactification elliptic curve. On the other hand, the latter are the structures that enter the refined construction of the [[Witten genus]] via the [[string orientation of tmf]].

## Relation to S-duality and 3-form flux
 {#RelationToSDualityAnd3FormFlux}

The refined perspective on [[perturbative string theory|perturbative]] [[type II string theory]] is that (see also at _[[orientifold]]_) the [[B-field]] is a [[cocycle]] in ([[twisted cohomology|twisted]]) [[ordinary differential cohomology]], while the [[RR-field]] is a [[cocycle]] in [[differential K-theory]] (in fact [[KR-theory]]). This is however not compatible with [[non-perturbative effect|non-perturbative]] [[S-duality]], which mixes the degree- components here. 

In [DFM 03, section 9.3](supergravity+C-field#DiaconescuFreedMoore03) it was argued that the cubical structure on the 11d CS term alleviates this problem, even though at face value it does not really solve it. But see at _[S-duality -- Cohomological nature of type II fields](S-duality#CohomologicalNatureOfTypeIIFieldsUnderSDuality)_ for more on this.


