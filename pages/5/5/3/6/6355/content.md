
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}


## Idea
 {#Idea}

In the context of [[mechanics]] (broadly construed), one distinguishes between *kinematics* and *dynamics*:

1. __Kinematics__ concerns (only) the [[physical fields]], [[space of states|space of]] [[states]] and [[algebra of observables|algebras of]] [[observables]].

2. __Dynamics__ additionally treats the evolution of the system in [[time]] or generally [[spacetime]], via, a [[Hamiltonian flow]] or similar.

   > (In the [[Schrödinger picture]], one think of the [[states]] as evolving, while the [[observables]] evolve in the [[Heisenberg picture]]. In the [[interaction picture]] we think of the states as evolving with respect to a given time evolution and the observables to evolve, too, with respect to a [[perturbation theory|perturbation]] of this time evolution.)

In the common framework of [[Lagrangian field theory]] both of these aspects are in principle encoded by a [[Lagrangian density]] (cf. at *[[covariant phase space]]*).


## Formalization

The notions of kinematics and dynamics may be formally defined in the two formalizations of [[quantum field theory]]: [[FQFT]] and [[AQFT]].


### In FQFT

Consider a [[quantum field theory]] as given by a [[strong monoidal functor]]

$$
  Z : Bord_n^S \to \mathcal{C}
$$

from a [[category of cobordisms]] with $S$-[[structure]] (for instance [[conformal structure]] or [[Riemannian structure]]) to some [[symmetric monoidal category]] $\mathcal{C}$.

Then:

* the _kinematics_ of $Z$ is $Z_0 : Ob(Bord_n^S) \to Ob(\mathcal{C})$, the action of the [[functor]] $Z$ on [[objects]].

* with that given, the _dynamics_ of $Z$ is $Z_1 : Mor(Bord_n^S) \to Mor(\mathcal{C})$, the action of the functor $Z$ on [[morphisms]].

This means that as we regard an $n$-dimensional [[QFT]] as an [[FQFT|extended QFT]] given by an [[n-functor]]

$$
  Z \colon Bord_n^S \to \mathcal{C}
$$

from an [[(infinity,n)-category of cobordisms]] with $S$-structure to some [[symmetric monoidal (infinity,n)-category]] $\mathcal{C}$ the dichotomy between kinematics and dynamics may be regarded as being blurred a bit: we can regard the action $Z_0$ on [[object]]s as the genuine kinematics and the action $Z_n$ on [[n-morphism]]s as the genuine dynamics, and then the actions $Z_{1 \leq k \leq n-1}$ as interpolating between these two notions.


### In AQFT

(...)


## Examples

### In $\sigma$-models

We discuss the notions of kinematics and dynamics for [[sigma-model]] [[QFT]]s.


#### Charged particle

Given a  [[Riemannian manifold|Riemannian]] [[target space]] $(X,g)$ and a  [[background gauge field]]s given by a [[circle n-bundle with connection|circle bundle with connection]] $(P \to X, \nabla)$, the corresponding [[sigma-model]] quantum field theory is, as an [[FQFT]], a [[functor]]

$$
  Z : Bord_1^{Riemn} \to Hilb
  \,.
$$

It sends 

* each [[object]]  -- a [[point]] -- to the space $\Gamma(P \times_{U(1)} \mathbb{C})$ of square integrable [[section]]s of the [[line bundle]] [[associated bundle|associated]] with the background gauge field;

* each [[morphism]] $(\bullet \stackrel{t}{\to} \bullet)$ to the [[operator]] $\exp(i t \nabla^* \nabla)$, where $\nabla^* \nabla$ is the [[Laplace-Beltrami operator]] of the [[covariant derivative]] $\nabla$.

So in terms of the background field data we have: 

* the kinematics is encoded in a smooth [[principal bundle]] -- hence a [[cocycle]] in [[smooth infinity-groupoid -- structures|smooth cohomology]];

* the dynamics is encoded in a [[connection on a bundle|connection]] on this bundle -- hence a refinement of the above cocycle to [[ordinary differential cohomology]].



[[!redirects kinematics and dynamics]]
[[!redirects dynamics and kinematics]]

[[!redirects kinematics]]
[[!redirects dynamics]]
