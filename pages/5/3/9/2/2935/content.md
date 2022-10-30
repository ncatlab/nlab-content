
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


#Contents
* automatic table of contents goes here
{:toc}


## Idea 

The _Poisson $\sigma$-model_ is a 2-dimensional [[sigma-model]] [[quantum field theory]] whose target space is a [[Poisson Lie algebroid]]. It is a [[2-dimensional Chern-Simons theory]]. This may be thought of as encoding the [[quantum mechanics]] of a [[string theory|string]] propagating on the [[phase space]] of a system in [[classical mechanics]]. 

In his solution of the problem of [[deformation quantization]] [[Maxim Kontsevich]] showed that correlators for the 2-string interaction (the correlator on the worldsheet that is a disk with three marked points on its boundary) describe a product operation which is a deformation of the [[Poisson bracket]] on the target space. This solves the formal [[deformation quantization]] problem of the phase space in [[quantum mechanics]] by identifying the quantum algebra with the _open string algebra_ of a [[string theory]] on that target.

The principal variant of the nonlinear Poisson sigma model is sometimes called Cattaneo-Felder model who have shown the graphical expansion used in Kontsevich's approach to the deformation quantization is explained via a Feynman diagram expansion in this model. 

If one considers [[brane]]s in the target space of the Poisson sigma-model, then then algebra of open strings that used to be just the deformation of the Poisson algebra becomes an [[A-infinity algebra|A-infinity algebroid]]. (See the references below).

> Probably something close to a [[Calabi-Yau category]], hence identifying the Poisson sigma-model as a [[TCFT]]. Does anyone know more in this direction?

## Definition

The [[target space]] of a Poisson $\sigma$-model is any [[Poisson manifold]] $(X, \{\})$, or rather the [[Poisson Lie algebroid]] $\mathfrak{P}$ corresponding to that.

A field configuration on a 2-dimensional $\Sigma$ is a [[connection on an infinity-bundle|connection]]

$$
  (\phi,\eta) : \mathfrak{T}\Sigma \to \mathfrak{P}  
 \,.
$$

In components this is

1. a [[smooth function]] $\phi : \Sigma \to X$;

1. a 1-form $\eta \in \Omega^1(\Sigma, \phi^* T X)$
   with values in the pullback of the [[tangent bundle]] of $X$ along $\phi$.

The [[action functional]] on the [[configuration space]] of all such connections for [[compact space|compact]] $\Sigma$ is defined to be

$$
  S : (\phi,\eta) \mapsto 
  \int_\Sigma
  \left(
     \langle \eta \wedge d_{dR}\phi\rangle
     + 
     \frac{1}{2}
     \phi^*\pi(\eta)
  \right)
  \,,
$$

where $\pi \in \wedge^2_{C^\infty(C)}\Gamma(T X)$ is the Poisson tensor of $(X, \{-,-\})$ and where  $\langle -,-\rangle$ is the canonical [[invariant polynomial]] on the [[Poisson Lie algebroid]].


## Properties

### Relation to deformation quantization of Poisson manifolds
 {#RelationToQuantizationOfPoissonManifolds}


In ([Cattaneo-Felder](#CattaneoFelder)) it was shown that the [[n-point function|3-point function]] in the [[path integral quantization]] of the Poisson $\sigma$-model of a [[Poisson Lie algebroid]] associated with a [[Poisson manifold]]  computes the [[star product]] in the [[deformation quantization]] of the Poisson manifold as given by ([Kontsevich](#Kontsevich)).

A [[higher geometric quantization]] that also yields the [[strict deformation quantization]] is discussed at _[[extended geometric quantization of 2d Chern-Simons theory]]_.

One may think of this relation between the 2d Poisson sigma-model and [[quantum mechanics]] = 1d [[quantum field theory]] as an example of the Chern-Simons type [[holographic principle]]. For more along these lines see below at _[holographic dual](#HolographicDual)_.

### Branes
 {#Branes}

The [[branes]] of the Poisson sigma model are related to
[[coisotropic submanifolds]] of the underlying [[Poisson manifold]]. Notice that these are the [[Lagrangian dg-submanifolds]] of the [[Poisson Lie algebroid]]. ([Cattaneo-Felder 03](#CattaneoFelder03)).

### Holographic dual
 {#HolographicDual}

By the Chern-Simons form of the [[holographic principle]] one expects the Poisson sigma-model to be related to a 1-dimensional [[quantum field theory]]. This is [[quantum mechanics]]. The [above](#RelationToQuantizationOfPoissonManifolds) relation to the deformation quantization of Poisson manifolds goes in this direction. More explicit realizations have been attempted, for instance ([Vassilevich](#Vassilevich)). 


## Related concepts

* [[schreiber:∞-Chern-Simons theory]]

* [[sigma-model]]

  * [[AKSZ sigma-model]]

    * **Poisson sigma-model**

      * [[A-model]], [[B-model]]

    * [[Courant sigma-model]]

      * [[Chern-Simons theory]]

* [[schreiber:∞-Chern-Simons theory]]

* [[higher dimensional Chern-Simons theory]]

  * [[1d Chern-Simons theory]]

  * [[2d Chern-Simons theory]]

  * [[3d Chern-Simons theory]]

  * [[4d Chern-Simons theory]]

  * [[5d Chern-Simons theory]]

  * [[6d Chern-Simons theory]]

  * [[7d Chern-Simons theory]]

  * [[infinite-dimensional Chern-Simons theory]]

[[!include infinity-CS theory for binary non-degenerate invariant polynomial - table]]


## References

### General

The Poisson sigma model was first considered in 

* [[Noriaki Ikeda]], _Two-dimensional gravity and nonlinear gauge theory_ , Ann.Phys.235(1994) 435- 464, [hep-th/9312059].

and later independently by P. Schaller, T. Strobl, motivated from an attempt to unify several two-dimensional models of [[gravity]] and to cast them into a common form with [[Yang-Mills theory|Yang-Mills theories]].

* P. Schaller, T. Strobl, _Poisson structure induced (topological) field theories_, Modern Phys. Lett. A 9 (1994), no. 33, 3129--3136, [doi](http://dx.doi.org/10.1142/S0217732394002951); _Introduction to Poisson $\sigma$-models_,  Low-dimensional models in statistical physics and quantum field theory (Schladming, 1995),  321--333, Lecture Notes in Phys. __469__, Springer 1996.

* Thomas Strobl, _Gravity from Lie algebroid morphisms_, Comm. Math. Phys.  __246__  (2004),  no. 3, 475--502, _Algebroid Yang-Mills theories_,   Phys. Rev. Lett.  __93__  (2004),  no. 21, 211601, 4 pp. [doi](http://dx.doi.org/10.1103/PhysRevLett.93.211601)

* M. Bojowald, A. Kotov, T. Strobl, _Lie algebroid morphisms, Poisson sigma models, and off-shell closed gauge symmetries_,  J. Geom. Phys.  54  (2005),  no. 4, 400--426, [doi](http://dx.doi.org/10.1016/j.geomphys.2004.11.002)

* Ctirad Klim&#269;&#237;k, T. Strobl, _WZW-Poisson manifolds_, J. Geom. Phys. __43__ (2002), no. 4, 341--344, <a href="http://dx.doi.org/10.1016/S0393-0440(02)00027-X">doi</a> 


The detailed argument by Cattaneo and Felder on how [[Maxim Kontsevich]]'s formula for the [[deformation quantization]] star product is the 3-point function of the Poisson sigma-model is in

* [[Alberto Cattaneo]], [[Giovanni Felder]], _A path integral approach to the Kontsevich quantization formula_ ,
Commun. Math. Phys. 212, 591--611 (2000) [doi](http://dx.doi.org/10.1007/s002200000229), [math.QA/9902090](http://arxiv.org/abs/math/9902090).
 {#CattaneoFelder}

* [[Alberto Cattaneo]], [[Giovanni Felder]], _Poisson sigma models and deformation quantization_ ,
Mod. Phys. Lett. A 16, 179--190 (2001) [hep-th/0102208](http://arxiv.org/abs/hep-th/0102208).


See also

* [[Alberto Cattaneo]], [[Giovanni Felder]], _Poisson sigma models and symplectic groupoids_ ,
(ed. [[Klaas Landsman]], M. Pflaum, M. Schlichenmeier), Progress in Mathematics 198, 61--93 (Birkh&#228;user, 2001)
[math.SG/0003023](http://arxiv.org/abs/math/0003023).

* [[Alberto Cattaneo]], [[Giovanni Felder]], _On the AKSZ formulation of the Poisson sigma model_ ,
Lett. Math. Phys. 56, 163--179 (2001) [math.QA/0102108](http://arxiv.org/abs/math/0102108).

The interpretation in terms of [[schreiber:infinity-Chern-Simons theory]] is discussed in

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:AKSZ Sigma-Models in Higher Chern-Weil Theory]]_ (2011)

Discussion in terms of [[holography]] is in 

* D. V. Vassilevich, _Holographic duals to Poisson sigma models_ ([arXiv:1301.7029](http://arxiv.org/abs/1301.7029))
 {#Vassilevich}



### With branes 
 {#LitWithBranes}

The study of [[branes]] in the Poisson sigma-model has been started in 

* Damien Calaque, [[Giovanni Felder]], Andrea Ferrario, Carlo A. Rossi, _Bimodules and branes in deformation quantization_ ([arXiv:0908.2299](http://arxiv.org/abs/0908.2299))

* Damien Calaque, [[Giovanni Felder]], Carlo A. Rossi, _Deformation quantization with generators and relations_ ([arXiv:0911.4377](http://arxiv.org/abs/0911.4377))

* [[Alberto Cattaneo]], [[Giovanni Felder]], _Coisotropic submanifolds in Poisson geometry and branes in the Poisson $\sigma$-model_, Lett.Math.Phys. 69 (2004) 157-175 ([arXiv:0309180](http://arxiv.org/abs/math/0309180))
 {#CattaneoFelder03}

* Andrea Ferrario, _Poisson Sigma Model with branes and hyperelliptic Riemann surfaces_ ([arXiv:0709.0635](http://arxiv.org/abs/0709.0635))

A review is in 

* F. Falceto, _Branes in Poisson sigma models_ (2009) ([pdf](http://benasque.org/2009gph/talks_contr/094Falceto.pdf))

### Recent developments

* Francesco Bonechi, [[Alberto Cattaneo]], [[Pavel Mnev]], _The Poisson sigma model on closed surfaces_ ([arXiv:1110.4850](http://arxiv.org/abs/1110.4850))

[[!redirects Poisson sigma model]]