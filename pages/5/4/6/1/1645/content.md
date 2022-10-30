

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

There are at least two things that are called _quantum anomalies_ in the context of [[quantum field theory]]

* **anomalous action functional**: the [[action functional]] (in [[path integral|path integral quantization]]) is not a globally well defined [[function]], but instead a [[section]] of a [[line bundle]] on [[configuration space]];

* **anomalous symmetry** (gauge anomaly): a symmetry of the [[action functional]] does not extend to a symmetry of the exponentiated action times the path integral measure; or equivalently the [[action]] of a group on classical [[phase space]] is not preserved by [[deformation quantization]].

## Definition

### Anomalous action functional

There are two major kinds of [[action functional]]s that may be anomalous in that they are not actually [[function]]s/[[functional]]s on the configuration space of fields, but just [[section]]s of some [[line bundle]]:

* theories with fermions (see e.g. [[spinors in Yang-Mills theory]])

* [[gauge theory|gauge theories]] with higher degree gauge fields ([[differential cohomology|differential cocycles]] of higher degree.) 

#### Fermionic anomalies

The [[path integral]] for a [[quantum field theory]] with [[fermion]]s can be decomposed into a [[fermionic path integral]] (see there for more details) over the [[fermionic field]]s follows by that over the [[bosonic field]]s. The former, a [[Berezin integral]] is typically well defined for a fixed configuration of the bosonic fields, but does not produce a well defined function on the space of all bosonic fields: but a _twisted function_ , a section of some line bundle called a [[determinant line bundle]] or, in $8k+2$ dimensions, its square root, the [[Pfaffian line bundle]]. 

So to even start making sense of the remaining path integral over the bosonic degree of freedom, this [[determinant line bundle]] or the corresponding [[Pfaffian line bundle]] has to be trivializale. Its non-trivializability is the _fermionic anomaly_ .


#### Higher gauge-theoreric anomalies

For the moment see [[Green-Schwarz mechanism]] for more.


### Anomalous symmetry

> under construction

Let 

$$
  S : C \to \mathbb{R}
$$

be a (well defined) [[nLab:action functional]]. Write $P$ for its resolved [[covariant phase space]] in [[dg-geometry]] and 

$$
  S^{BV} : P \to \mathbb{R}
$$

for the BV-action functional, both as given by [[BRST-BV formalism]].

If the action functional is local (comes from a [[Lagrangian]] on [[jet space]]) the [[covariant phase space]] $P$ a priori only carries a [[presymplectic structure]]. But by BV-theory there exists an equivalent (homotopical) derived action functional $S_\Psi^{BV} : P \to \mathbb{R}$ such that $S_\Psi^{BV}$ does induce a genuine [[symplectic structure]] on the [[derived geometry|derived]] space $P$.

For ordinary [[Poisson manifold]]s and hence [[symplectic manifold]]s [[Maxim Kontsevich]]'s theorem says that their [[deformation quantization]] always exist. But if $S$ is the [[action functional]] of a [[gauge theory]] then $P$ is in general a nontrivial derived [[infinity-Lie algebroid]] (its function algebra has "ghosts" and "ghosts of ghost": the [[Chevalley-Eilenberg algebra]] generators) and the theorem does not apply. Instead, the quantization of the derived symplectic space $P$ exists only if the first and second [[infinity-Lie algebroid cohomology]] of $P$ vanishes:

These two cohomology groups 

$$
 Anom_{gauge} = H^1(CE(P)) \oplus H^2(CE(P))
$$

are called the **gauge anomaly** of the system. Only if they vanish does the [[quantization]] of the [[gauge theory]] encoded by $S$ exist.

More concretely, the function algebra on $P$ is a graded-commutative [[dg-algebra]] equipped with a graded Poisson bracket $\{-,-\}_{BV}$ and an element $Q \in C^\infty(P)$ (the BV-BRST charge) whose [[Hamiltonian vector field]] is the [[derivation]] that is the [[differential]] of the dg-algebra $C^\infty(X)$. If the gauge anomaly does not vanish, then, while the deformation quantization of the graded algebra $C^\infty(P)$ to a non commutative graded algebra with commutator $[-,-]$ will exist, it may happen that the image $\hat Q$ of $Q$ under the quantization no longer satisfies $[\hat Q,\hat Q] = 2 \hat Q^2$. Therefore the [[derivation]] $[\hat Q,-]$ will not define a [[differential]] and therefore the quantization of the graded-commutative [[dg-algebra]] $C^\infty(P)$ will only be a noncommutative algebra, not a non-commutative dg-algebra, hence will not be functions on a non-commutative space in [[derived geometry]].


## Examples

### Anomalous action functional

#### Spinning particles and super-branes 
  {#SpinningParticlesAndSuperBranes}

The [[sigma-model]] for a [[supersymmetry|supersymmetric]] fundamental [[brane]] on a target space $X$ has an anomaly coming from the nontriviality of [[Pfaffian line bundle]]s associated with the [[fermion]]ic fields on the worldvolume. These anomalies disappear (i.e. these bundles are trivializable) when the structure group of the [[tangent bundle]] of $X$ has a sufficiently high lift through the [[Whitehead tower]] of $O(n)$.

* **Spin structure** the worldline anomaly for the spinning particle/superparticle vanishes when $X$ has [[Spin structure]] 

  This is a classical result. A concrete derivation is in 

  * [[Edward Witten]], _Global anomalies in String theory_ in _Symposium on anomalies, geometry, topology_ , World Scientific Publishing, Singapore (1985)

* **String structure** the worldsheet anomaly for the spinning string/superstring in [[heterotic string theory]] vanishes (essentially) when $X$ has [[String structure]] 

  This is originally due to Killingback and Witten. A commented list of literature is [here](http://golem.ph.utexas.edu/string/archives/000572.html). Recently [[Ulrich Bunke]] gave the rigorous proof

  * [[Ulrich Bunke]], _String structures and trivialisations of a Pfaffian line bundle_ ([arXiv](http://arxiv.org/abs/0909.0846))

in terms of [[differential cohomology]] in general and [[differential string structure]]s in particular.

* **Fivebrane structure** the worldvolume anomaly for the super-5-brane in [[dual heterotic string theory]] vanishes (essentially) when $X$ has [[Fivebrane structure]]. See there.


### Anomalous symmetry

#### Conformal anomaly

For the moment see [[Liouville cocycle]].



## References

### Anomalous action functional

The computation of _gravitational anomalies_ in the sense of nontrivialities of [[Pfaffian line bundle]]s of fermions over [[configuration space]]s of [[metric]]s is due to

* L. Alvarez-Gaume and [[Edward Witten]], _Gravitational Anomalies_ Nucl. Phys. B234 (1984) 269.

* [[Edward Witten]], _Global gravitational anomalies_ , Commun. Math. Phys. 100 (1985) 197. ([EUCLID](http://projecteuclid.org/euclid.cmp/1103943444))

The mathematical formulation of this in terms of [[index theory]] is due to

* [[Michael Atiyah]], [[Isadore Singer]], _Dirac operators coupled to vector potentials_, Proc. Nat. Acad. Sci. USA __81__, 2597-2600 (1984)

* J.-M. Bismut and [[Daniel Freed]], _The analysis of elliptic families. I. Metrics and connections on
determinant bundles_ , Comm. Math. Phys. 106 (1986), no. 1, 159&#8211;176.

* J.-M. Bismut and [[Daniel Freed]], _The analysis of elliptic families. II. Dirac operators, eta invariants,
and the holonomy theorem_ , Comm. Math. Phys. 107 (1986), no. 1, 103&#8211;163.

A physicists' monograph is

* Reinhold A. Bertlmann, _Anomalies in quantum field theory_, Oxford Science Publ., 1996, 2000

A clear description of the quantum anomalies for higher gauge theories is in

* [[Dan Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_ ([arXiv](http://arxiv.org/abs/hep-th/0011220))

As an application of this, a detailed discussion of the cancellation of the anomaly of the [[supergravity C-field]] in 11-dimensional [[supergravity]] is in

* [[Dan Freed]], [[Greg Moore]], _Setting the quantum integrand of M-theory_ ([arXiv:hep-th/0409135](http://arxiv.org/abs/hep-th/0409135))

The role of [[spin structure]]s as the anomaly cancellation condition for the spinning particle is discussed in

* [[Edward Witten]], _Global anomalies in String theory_ in _Symposium on anomalies, geometry, topology_ , World Scientific Publishing, Singapore (1985)

The anomaly line bundles for [[self-dual higher gauge theory]] is discussed in 

* Samuel Monnier, _The anomaly line bundle of the self-dual field theory_ ([arXiv:1109.2904](http://arxiv.org/abs/1109.2904))

### Gauge anomaly
 {#ReferencesGaugeAnomaly}

An interpretation of gauge anomalies as failures of [[Hamiltonian]]s to have [[self-adjoint extension]]s is in

* J. G. Esteve, _Origin of the anomalies: the modified Heisenberg equation_ ([arXiv:hep-th/0207164](http://arxiv.org/abs/hep-th/0207164))

Discussion in the context of [[BRST-BV formalism]] is in

* R. Amorim, N.R.F.Braga, R. Thibes, _Axial and gauge anomalies in the field antifield quantization of the generalized Schwinger model_ ([arXiv:hep-th/9712014](http://arxiv.org/abs/hep-th/9712014))

### In finite-dimensional quantum mechanics

* [[A. P. Balachandran]], Amilcar R. de Queiroz, _Mixed states from anomalies_, [arxiv/1108.3898](http://arxiv.org/abs/1108.3898)
* Carlos Alcalde, Daniel Sternheimer, _Analytic vectors, anomalies and star representations_, Lett. Math. Phys. __17__ (1989), no. 2, 117&#8211;127. [MR90h:22012](http://www.ams.org/mathscinet-getitem?mr=993017), [doi](http://dx.doi.org/10.1007/BF00402326) (the last section has also the field theory case)

[[!redirects anomaly]]
[[!redirects anomalies]]
[[!redirects quantum anomalies]]

[[!redirects gauge anomaly]]
[[!redirects gauge anomalies]]