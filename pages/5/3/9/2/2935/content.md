
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


\tableofcontents



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
  (\phi,\eta) : \mathfrak{T}^*\Sigma \to \mathfrak{P}  
 \,.
$$

In components this is

1. a [[smooth function]] $\phi : \Sigma \to X$;

1. a 1-form $\eta \in \Omega^1(\Sigma, \phi^* T^* X)$
   with values in the pullback of the [[cotangent bundle]] of $X$ along $\phi$.

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


[Cattaneo & Felder 2000](#CattaneoFelder2000) showed that the [[n-point function|3-point function]] in the [[path integral quantization]] of the Poisson $\sigma$-model of a [[Poisson Lie algebroid]] associated with a [[Poisson manifold]]  computes the [[star product]] in the [[deformation quantization]] of the Poisson manifold as given by [Kontsevich](#Kontsevich).

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

* [[Noriaki Ikeda]], _Two-dimensional gravity and nonlinear gauge theory_ , Ann.Phys. **235** (1994) 435- 464 &lbrack;[hep-th/9312059](https://arxiv.org/abs/hep-th/9312059), [doi:10.1006/aphy.1994.1104](https://doi.org/10.1006/aphy.1994.1104)&rbrack;

and later independently by P. Schaller, T. Strobl, motivated from an attempt to unify several two-dimensional models of [[gravity]] and to cast them into a common form with [[Yang-Mills theory|Yang-Mills theories]].

* P. Schaller, T. Strobl, _Poisson structure induced (topological) field theories_, Modern Phys. Lett. A **9** (1994), no. 33, 3129--3136 &lbrack;[doi:10.1142/S0217732394002951](http://dx.doi.org/10.1142/S0217732394002951)&rbrack;; _Introduction to Poisson $\sigma$-models_,  Low-dimensional models in statistical physics and quantum field theory (Schladming, 1995),  321--333, Lecture Notes in Phys. __469__, Springer 1996.

* Thomas Strobl, _Gravity from Lie algebroid morphisms_, Comm. Math. Phys.  __246__  (2004),  no. 3, 475--502, _Algebroid Yang-Mills theories_,   Phys. Rev. Lett.  __93__  (2004),  no. 21, 211601, 4 pp. &lbrack;[doi:10.1103/PhysRevLett.93.211601](http://dx.doi.org/10.1103/PhysRevLett.93.211601)&rbrack;

* [[Martin Bojowald]], [[Alexei Kotov]], Thomas Strobl, _Lie algebroid morphisms, Poisson sigma models, and off-shell closed gauge symmetries_,  J. Geom. Phys.  __54__:4  (2005) 400--426 &lbrack;[doi:10.1016/j.geomphys.2004.11.002](https://doi.org/10.1016/j.geomphys.2004.11.002)&rbrack;

* Ctirad Klim&#269;&#237;k, T. Strobl, _WZW-Poisson manifolds_, J. Geom. Phys. __43__ (2002), no. 4, 341--344 &lbrack;<a href="http://dx.doi.org/10.1016/S0393-0440(02)00027-X">doi:10.1016/S0393-0440(02)00027-X</a>&rbrack;


The detailed argument by Cattaneo and Felder on how [[Maxim Kontsevich]]'s formula for the [[deformation quantization]] star product is the 3-point function of the Poisson sigma-model is in

* {#CattaneoFelder2000} [[Alberto Cattaneo]], [[Giovanni Felder]], _A path integral approach to the Kontsevich quantization formula_, Commun. Math. Phys. **212** (2000) 591--611 &lbrack;[doi:10.1007/s002200000229](http://dx.doi.org/10.1007/s002200000229), [math.QA/9902090](http://arxiv.org/abs/math/9902090)&rbrack;
 

* [[Alberto Cattaneo]], [[Giovanni Felder]], _Poisson sigma models and deformation quantization_, Mod. Phys. Lett. A **16** (2001) 179--190 &lbrack;[hep-th/0102208](http://arxiv.org/abs/hep-th/0102208), [doi:10.1142/S0217732301003255](https://doi.org/10.1142/S0217732301003255)&rbrack;


See also:

* [[Alberto Cattaneo]], [[Giovanni Felder]], _Poisson sigma models and symplectic groupoids_ , (ed. [[Klaas Landsman]], M. Pflaum, M. Schlichenmeier), Progress in Mathematics 198, 61--93 (Birkh&#228;user, 2001)
&lbrack;[math.SG/0003023](http://arxiv.org/abs/math/0003023)&rbrack;

* [[Alberto Cattaneo]], [[Giovanni Felder]], _On the AKSZ formulation of the Poisson sigma model_, Lett. Math. Phys. **56** (2001) 163--179 &lbrack;[math.QA/0102108](http://arxiv.org/abs/math/0102108), [doi:10.1023/A:1010963926853](https://doi.org/10.1023/A:1010963926853)&rbrack;

Review:

* Nima Moshayedi: *Kontsevich’s Deformation Quantization and Quantum Field Theory*, Springer (2022) &lbrack;[doi:10.1007/978-3-031-05122-7](https://doi.org/10.1007/978-3-031-05122-7)&rbrack;


Interpretation in terms of [[schreiber:infinity-Chern-Simons theory]]:

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]]: _[[schreiber:AKSZ Sigma-Models in Higher Chern-Weil Theory]]_ (2011)

Discussion in terms of [[holography]]:

* {#Vassilevich} D. V. Vassilevich, _Holographic duals to Poisson sigma models_, Phys. Rev .D **87** (2013) 104011 &lbrack;[arXiv:1301.7029](http://arxiv.org/abs/1301.7029), [doi:10.1103/PhysRevD.87.104011](https://doi.org/10.1103/PhysRevD.87.104011)&rbrack;
 



### With branes 
 {#LitWithBranes}

The study of [[branes]] in the Poisson sigma-model has been started in 

* [[Damien Calaque]], [[Giovanni Felder]], Andrea Ferrario, Carlo A. Rossi, _Bimodules and branes in deformation quantization_, Compos.Math. **147** (2011) 105-160 &lbrack;[arXiv:0908.2299](http://arxiv.org/abs/0908.2299), [doi:10.1112/S0010437X10004847](https://doi.org/10.1112/S0010437X10004847)&rbrack;

* [[Damien Calaque]], [[Giovanni Felder]], Carlo A. Rossi, _Deformation quantization with generators and relations_, J. Algebra **337** (2011) 1-12 &lbrack;[arXiv:0911.4377](http://arxiv.org/abs/0911.4377), [doi:10.1016/j.jalgebra.2011.03.037](https://doi.org/10.1016/j.jalgebra.2011.03.037)&rbrack;

* {#CattaneoFelder03} [[Alberto Cattaneo]], [[Giovanni Felder]], _Coisotropic submanifolds in Poisson geometry and branes in the Poisson $\sigma$-model_, Lett.Math.Phys. **69** (2004) 157-175 &lbrack;[arXiv:0309180](http://arxiv.org/abs/math/0309180), [doi:10.1007/s11005-004-0609-7](https://doi.org/10.1007/s11005-004-0609-7)&rbrack;
 

* Andrea Ferrario, _Poisson Sigma Model with branes and hyperelliptic Riemann surfaces_, J.Math.Phys. **49** (2008) 092301 &lbrack;[arXiv:0709.0635](http://arxiv.org/abs/0709.0635), [doi:10.1063/1.2982234](https://doi.org/10.1063/1.2982234)&rbrack;

A review is in 

* F. Falceto, _Branes in Poisson sigma models_ (2009) ([pdf](http://benasque.org/2009gph/talks_contr/094Falceto.pdf))

### Further developments

* Francesco Bonechi, [[Alberto Cattaneo]], [[Pavel Mnev]], _The Poisson sigma model on closed surfaces_, JHEP **01** (2012) 099 &lbrack;[arXiv:1110.4850](http://arxiv.org/abs/1110.4850), <a href="https://doi.org/10.1007/JHEP01(2012)099">doi:10.1007/JHEP01(2012)099</a>&rbrack;

* [[Thomas Basile]], [[Athanasios Chatzistavrakidis]], [[Sylvain Lavau]]: *Supersymmetric Poisson and Poisson-supersymmetric sigma models* &lbrack;[arXiv:2504.13114](https://arxiv.org/abs/2504.13114)&rbrack;



[[!redirects Poisson sigma model]]