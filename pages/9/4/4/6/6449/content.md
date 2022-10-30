
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
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

There are two kinds of higher dimensional generalizations of ordinary 3-dimensional [[Chern-Simons theory]] that are often called "higher dimensional Chern-Simons theory" in the literature. Both are special cases of [[schreiber:infinity-Chern-Simons theory]].

Recall that for $\mathfrak{g}$ a [[Lie algebra]] (not necessarily abelian) with non-generate binary [[invariant polynomial]] $\langle -,-\rangle$, the corresponding [[schreiber:infinity-Chern-Simons theory]] [[QFT]] is ordinary [[Chern-Simons theory]] in dimension 3.

But also every other [[invariant polynomial]] $\langle-,-,\cdots,-\rangle$ on $\mathfrak{g}$ induces an [[schreiber:infinity-Chern-Simons theory]], now in higher dimension. 

Moreover, every [[line Lie n-algebra]] $b^n \mathbb{R}$ carries a canonical invariant polynomial. The [[schreiber:infinity-Chern-Simons theory]] associated with that is often called _abelian higher dimensional CS theory_ .

(...)

More general "higher"-generalization of Chern-Simons theory to [[schreiber:infinity-Chern-Simons theory]] allow $\mathfrak{g}$ to be a (nonabelian) [[Lie 2-algebra]] or more generally a (nonabelian) [[L-infinity algebra]] or fully generally a [[L-infinity algebroid]].

## Higher abelian Chern-Simons theory.

### Definition

The definition of higher abelian Chern-Simons theory is simple _locally_ when certain global [[cohomology|cohomological]] effects can be ignored. We first give the simple local definition and then the full global definition.

Let $k \in \mathbb{N}$ be a [[natural number]], let $d = 4 k + 3$ and let $\Sigma$ be a [[compact space|compact]] [[smooth manifold]] of [[dimension]] $d$.

Then the _simple version_ of abelian $d$-dimensional Chern-Simons theory is defined as follows. 

* the [[configuration space]] is the [[space]] of [[differential form]]s on $\Sigma$ of degree $2k+1$

  $$
    Conf_{simpl} = \Omega^{2k+1}(\Sigma)
    \,,
  $$

* the [[Lagrangian]] is 

  $$
    L : B \mapsto B \wedge d_{dR} B
    \,,
  $$

* and the [[action functional]]

  $$
    S : \Omega^{2k+1}(\Sigma) \to \mathbb{R}
  $$

  is therefore

  $$
    S : B \mapsto \int_\sigma B \wedge d_{dR}B
    \,.
  $$

Notice that generally for an $n$-form $B$ on a closed $(2n+1)$-dimensional manifold $\Sigma$ we have

$$
  \int_\Sigma B \wedge d_{dR} B
  =
  (-1)^{1+n + n(1+n)}
  \int_\Sigma B \wedge d_{dR} B
$$

by first using integration by parts and then switching the order of the wedge factors. Therefore this kind of action vanishes identically when $deg B$ is even. This is the reason for the above assumption that $deg B = 2k+1$ for $k \in \mathbb{N}$ and hence that the Chern-Simons theory is in dimension $4k+3$.

In the full theory instead the configuration space is 

$$
  Conf = \mathbf{H}_{diff}^{2k+2}(\Sigma)
  \,,
$$

the space of [[circle n-bundle with connection|circle (2k+1)-bundles with connection]] (given by [[cocycle]]s in degree $2k+2$ [[ordinary differential cohomology]]). This contains the above simplified configuration space as the subspace of $(2k+1)$-connections whose underlying circle $(2k+1)$-bundle is trivial. 

The action functional is given by

$$
  S : \hat B \mapsto \int_\Sigma \hat B \cup \hat B
  \,,
$$

where now the integral is [[fiber integration in ordinary differential cohomology]] and in the integrand we have the [[cup product in ordinary differential cohomology]] of differential cocycles.

(See for instance ([GT, section 4.1](#GT)), ([FMS, (1.28)](#FMS))).

### Formulation in $\infty$-Chern-Simons theory

We discuss how the above definition arises as a special case of the general notion of 
[[schreiber:infinity-Chern-Simons theory]].

These theories are defined by

* an [[L-infinity algebroid]] $\mathfrak{a}$;

* equipped with an [[invariant polynomial]] $\langle \rangle$.

The abelian higher dimensional Chern-Simons theories in dimension $4k+3$ are the special case of this general situation where

* $\mathfrak{a} = b^{2k+1}\mathbb{R}$ is the [[line Lie n-algebra|line Lie (2k+1)-algebra]], the $(2k+1)$-fold [[delooping]] of the abelian [[Lie algebra]] $\mathbb{R}$;

* $\langle - \rangle$ is the canonical quadratic [[invariant polynomial]] on this.

(...)

See ([FRS, 4.1.4](#FRS)).

### Examples

Higher dimensional abelian Chern-Simons theories appear automatically as components of systems of higher [[supergravity]], for instance in [[11-dimensional supergravity]] (they are automatically induced by the requirement of  [[local supersymmetry]] in these higher dimensional supergravity theories).

(...)

### Properties

#### Holographic relation to $4k+2$-dimensional theory

Higher Chern-Simons theory in dimension $4k+3$ is related by a [[holographic principle]] to [[self-dual higher gauge theory]] in dimension $4k+2$ (at least in the abelian case). 

* $(k=0)$: ordinary 3-dimensional [[Chern-Simons theory]] is related to a [[string]] [[sigma-model]] on its boundary;

* $(k=1)$: 7-dimensional Chern-Simons theory is related to a [[fivebrane]] model on its boundary;

* $(k=2)$: 11-dimensional Chern-Simons theory is related to a parts of a [[type II string theory]] on its bounday (or that of the space-filling 9-[[brane]], if one wishes) ([BelovMoore](#BelovMoore))

## Higher-dimensional non-abelian CS theory

Chern-Simons actions for [[Lie algebra]]s $\mathfrak{g}$ but with higher-degree [[invariant polynomial]]s have in particular received attention for $\mathfrak{g} = \mathfrak{siso}$ the [[super Poincare Lie algebra]]. In this case these action functionals can be regarded as defining higher [[Chern-Simons supergravity]].




## Related concepts

* [[schreiber:infinity-Chern-Simons theory]]

  * [[Chern-Simons theory]]

  * **higher dimensional Chern-Simons theory**

    * [[Chern-Simons gravity]]

  * [[AKSZ sigma-model]]

    * [[Poisson sigma model]]

      * [[A-model]], [[B-model]]

    * [[Courant sigma-model]]

      * [[Chern-Simons theory]]

  * [[1-dimensional Chern-Simons theory]]

* [[higher dimensional WZW models]]

## References

### General

For higher dimensional non-abelian Chern-Simons theory see for instance 

* M&#225;ximo Ba&#241;ados, _Higher dimensional Chern-Simons theories and black holes_ ([pdf](http://worldscibooks.com/etextbook/4388/4388_chap01.pdf))

* M&#225;ximo Ba&#241;ados, Luis Garay, [[Marc Henneaux]], _Existence of local degrees of freedom for higher dimensional pure Chern-Simons theories_ Phys. Rev. D 53, R593&#8211;R596 (1996)  ([pdf](http://prd.aps.org/pdf/PRD/v53/i2/pR593_1))

* M&#225;ximo Ba&#241;ados, Luis Garay, [[Marc Henneaux]], _The dynamical structure of higher dimensional Chern-Simons theory_ ([arXiv:hep-th/9605159](http://arxiv.org/abs/hep-th/9605159))

* G Giachetta, L Mangiarotti, G Sardanashvily, _Noether conservation laws in higher-dimensional Chern-Simons theory_ Modern Physics Letters A Volume 18(2003) ([pdf](http://gnsardan.appfarm.ru/a84.pdf))

### Formulation in differential cohomology

For the formulation of abelian Chern-Simons theory by fiber integration over cup products in [[ordinary differential cohomology]] see

* Enore Guadagnini, Frank Thuillier, _Deligne-Beilinson cohomology and abelian links invariants_ SIGMA 4 (2008), 078, 30 ([arXiv:0801.1445](http://arxiv.org/abs/0801.1445))
  {#GT}

* R. Floreanini, R. Percacci, _Higher dimensional abelian Chern-Simons theory_ Physics Letters B Volume 224, Issue 3, 29 (1989)

* [[Daniel Freed]], [[Gregory Moore]], [[Graeme Segal]], _The Uncertainty of Fluxes_ ([arXiv:hep-th/0605198](http://arxiv.org/abs/hep-th/0605198))
  {#FMS}

### Relation to self-dual theories

The idea of describing [[self-dual higher gauge theory]] by abelian Chern-Simons theory in one dimension higher originates in 

* [[Edward Witten]], _Five-Brane Effective Action In M-Theory_ Journal of Geometry and Physics
Volume 22, Issue 2, May 1997, Pages 103-133  ([arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234))

(there for the [[6d (2,0)-susy QFT]] on the [[fivebrane]]) and

* [[Edward Witten]], _Duality Relations Among Topological Effects In String Theory_ ([arXiv:hep-th/9912086](http://arxiv.org/abs/hep-th/9912086))

Motivated by this the [[differential cohomology]] of self-dual fields had been discussed in 

* [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_
 {#HopkinsSinger}

More discussion of the general principle is in 

* Dmitriy Belov, [[Greg Moore]], _Holographic Action for the Self-Dual Field_ ([arXiv:hep-th/0605038](http://arxiv.org/abs/hep-th/0605038))


The application of this to the description of 
[[type II string theory]] in 10-dimensions to [[schreiber:infinity-Chern-Simons theory|11-dimensional Chern-Simons theory]] is in the followup 

* Dmitriy Belov, [[Greg Moore]], _Type II Actions from 11-Dimensional Chern-Simons Theories_ ([arXiv:hep-th/0611020](http://arxiv.org/abs/hep-th/0611020))
 {#BelovMoore}

### Higher Chern-Simons supergravity

Original articles include

M&#225;ximo Ba&#241;ados, Ricardo Troncoso, Jorge Zanelli, _Higher dimensional Chern-Simons supergravity_ Phys. Rev. D 54, 2605&#8211;2611 (1996) ([pdf](http://cdsweb.cern.ch/record/293524/files/9601003.pdf))

An introduction and survey is in 

* Jorge Zanelli, _Lecture notes on Chern-Simons (super-)gravities_ ([arXiv:hep-th/0502193](http://arxiv.org/abs/hep-th/0502193))




### Higher Chern-Simons invariants
 {#ReferencesInvariants}

* F. Thuillier, _Deligne-Beilinson cohomology and abelian link invariants: torsion case_ J. Math. Phys. 50, 122301 (2009)

* B. Broda, _Higher-dimensional Chern-Simons theory and link invariants_ Physics Letters B Volume 280, Issues 3-4, 30 (1992) Pages 213-218 

### Formulation in $\infty$-Chern-Simons theory

Section 4.1.4 of

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher Chern-Weil Derivation of AKSZ Sigma-Models]]_
 {#FRS}

Section 4.4 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

### Boundary theories

Boundary [[higher dimensional WZW models]] for nonabelian [[higher dimensional Chern-Simons theory]] are discussed in

* J. Gegenberg , G. Kunstatter, _Boundary Dynamics of Higher Dimensional Chern-Simons Gravity_ ([arXiv:hep-th/0010020](http://arxiv.org/abs/hep-th/0010020))

* J. Gegenberg , G. Kunstatter, _Boundary Dynamics of Higher Dimensional AdS Spacetime_ ([arXiv:http://arxiv.org/abs/hep-th/9905228](http://arxiv.org/abs/hep-th/9905228))



[[!redirects higher Chern-Simons theory]]
[[!redirects higher Chern-Simons theories]]

[[!redirects higher dimensional Chern-Simons theories]]

