
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
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

Traditional [[geometric quantization]] applies to [[symplectic manifolds]] but not to [[Poisson manifolds]]. However, every Poisson manifold can be regarded as a [[symplectic Lie n-algebroid]]: a [[Poisson Lie algebroid]]. This is symplectic, in [[higher symplectic geometry]]. Its [[Lie integration]] is a [[symplectic groupoid]].

There is an generalization of the machinery of geometric quantization to [[symplectic groupoids]] which hence provides a geometric quantization of [[Poisson manifolds]].

## Definition

### Geometric prequantization of a symplectic groupoid
 {#GeometricPrequantization}

Formulated in the language of [[higher differential geometry]], what is traditionally called a [[prequantization]] of a [[symplectic groupoid]] $SG(X,\pi) = \exp(\mathfrak{P}(X,\pi))$ (see [Hawkins, section 4.2](#EH)) is a morphism of [[smooth infinity-groupoids|smooth 2-groupoids]]

$$
  SG(X,\pi) \longrightarrow \mathbf{B}^2 U(1)_{conn^1}
$$

to the [[moduli infinity-stack|moduli 2-stack]] of [[circle n-bundle with connection|circle 2-bundles with 1-form connection]], such that this 2-connection is trivial on the underlying [[Poisson manifold]]

$$
  \array{
    && X 
   \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && SG(X,\pi)
    \\
    & \searrow && \swarrow_{\mathrlap{\widehat{\chi}}}
    \\
    && \mathbf{B}^2 U(1)_{conn^1}
  }
$$

([hgp 13](#hgp), [Bongers 13](#Bongers13) [Nuiten 13](#Nuiten13)) and such that the image of $\chi$ in [[infinity-Lie algebra cohomology|Lie algebroid cohomology]] (hence in [[Poisson cohomology]]) is the given Poisson bitensor $\pi \in CE^\bullet(\mathfrak{P}(X,\pi))$.

By ([[schreiber:Higher Chern-Weil Derivation of AKSZ Sigma-Models|FRS 11]], based on [[schreiber:Cech Cocycles for Differential characteristic Classes|FSS 10]]) the Lie algebroid cocycle

$$
  \pi \;\colon\; \mathfrak{P}(X,\pi) \longrightarrow \mathbb{R}[2]
$$

directly [[Lie integration|Lie integrates]] to a morphism of [[smooth infinity-groupoids|smooth 2-groupoids]] of the form

$$
  \exp(\pi)_{conn}
  \;\colon\;
  SG(X,\pi)_{conn} = \tau_1 \exp(\mathfrak{P}(X,\pi))_{conn}
  \longrightarrow
  \mathbf{B}(\mathbb{R}/\Gamma)_{conn}
  \,,
$$

which is a [[cocycle]] in degree-3 [[ordinary differential cohomology]] on the differential refinement $SG(X,\pi)_{conn}$ of the [[symplectic groupoid]] by [[infinity-Lie algebroid-valued differential form|Lie algebroid valued differential forms]] (the [[moduli stack]] of the [[2d Chern-Simons theory]] induced by the cocycle), with [[coefficients]] in the [[quotient]] group $\mathbb{R}/\Gamma$, where $\Gamma \hookrightarrow \mathbb{R}$ is the group of [[periods]] of 

$$
  \left(
  T S^2 \longrightarrow \mathfrak{P}(X,\pi) \stackrel{\pi}{\longrightarrow} \mathbb{R}[2]
  \right)
  \in \Omega^2_{cl}(S^2)
  \,.
$$

For $\Gamma = \mathbb{Z}$ this hence yields 

$$
  SG(X,\pi) = \tau_1 \exp(\mathfrak{P}(X,\pi))_{conn}
  \longrightarrow
  \mathbf{B}U(1)_{conn}
  \,.
$$

This integrality condition is the one that appears in the traditional literature as ([Bonechi-Cattaneo-Zabzine 05, (1.7)-(1.11)](#BonechiCattaneoZabzine05)) based on ([Crainic-Zhu 04, theorem 3](#CrainicZhu04)).

Forgetting the differential refinement and the [[principal 2-connection]] structure we get an underlying [[circle 2-group]]-[[principal 2-bundle]] on the [[symplectic groupoid]], modulated by

$$
  \exp(\pi) \;\colon\; SH(X,\pi) \longrightarrow \mathbf{B}^2 U(1)
  \,.
$$

That this coincides with the one in the traditional literature can be seen fairly explicitly for instance from ([Bonechi-Cattaneo-Zabzine 05, remark 3](#BonechiCattaneoZabzine05)).

(...)

Notice that given a [[symplectic groupoid]] $(X,\omega)$, the symplectic form defines a class in degree-3 [[de Rham cohomology]] $H_{dR}^3(X)$. 

(Notice that, while this $\omega$ is typically expressed as a 2-form on $X_1$, this represents indeed a degree-3 cocycle in the [[simplicial de Rham complex]] of the [[nerve]] of $X$).

We say that $\omega$ is _integral_ if it is in the image of the [[curvature]] map 

$$
  curv : H^2_{diff}(X,U(1)) \to H^3_{dR}(X)
$$

from the [[ordinary differential cohomology]] of $X$. If this is the case, we say that a lift $(\hat X, \nabla)$ of $\omega$ to $\mathbf{H}_{diff}(X, \mathbf{B}^2 U(1))$, hence to the [[2-groupoid]] of [[circle n-bundle with connection|circle 2-bundles with connection]] over $X$, is a **prequantum line bundle** for $(X,\omega)$.

Notice that this traditional terminology is off by one: the underlying $\hat X \to X$ is a [[circle 2-group]]-[[principal 2-bundle]] on $X$.

(...)

### Polarization of a symplectic groupoid

(...)

([Hawkins, section 4.3](#EH))

(...)


### Geometric quantization of a symplectic groupoid

(...)

([Hawkins, section 5](#EH))

(...)

$$
  \sqrt{\Omega}
  \coloneqq
  \sqrt{\wedge^{max} \Gamma (T_{d t = 0}^\ast \mathcal{G}_1) }
  \otimes
  \sqrt{\wedge^{max} \Gamma (T_{d s = 0}^\ast \mathcal{G}_1) }
$$

$$  
  \begin{aligned}
    pr_1^\ast \sqrt{\Omega}
    \otimes
    pr_2^\ast \sqrt{\Omega}
    & 
    \simeq
    pr_1^\ast \sqrt{\wedge^{max} \Gamma (T_{d s = 0}^\ast \mathcal{G}_1) }
    \otimes
    pr_2^\ast \sqrt{\wedge^{max} \Gamma (T_{d t = 0}^\ast \mathcal{G}_1) }
    \otimes
    pr_1^\ast \sqrt{\wedge^{max} \Gamma (T_{d t = 0}^\ast\mathcal{G}_1) }
    \otimes
    pr_2^\ast \sqrt{\wedge^{max} \Gamma (T_{d s = 0}^\ast \mathcal{G}_1) }
    \\
    & \simeq
    \sqrt{\wedge^{max} \Gamma (T_{d \circ = 0}^\ast \mathcal{G}_2) }
    \otimes
    \sqrt{\wedge^{max} \Gamma (T_{d \circ = 0}^\ast \mathcal{G}_2) }
    \otimes
    pr_1^\ast \sqrt{\wedge^{max} \Gamma (T_{d t = 0}^\ast\mathcal{G}_1) }
    \otimes
    pr_2^\ast \sqrt{\wedge^{max} \Gamma (T_{d s = 0}^\ast \mathcal{G}_1) }
    \\
    & \simeq
    \wedge^{max} \Gamma(T_{d \circ = 0}^\ast \mathcal{G}_2)
    \otimes 
    \circ^\ast \sqrt{\Omega}
  \end{aligned}
$$

(...)

## Properties

### Relation to deformation quantization

There does not seem to be in the literazure a precise relation between the methods of [[geometric quantization]] discussed here and methods of [[deformation quantization]]. But the following similarity might be relevant:

If the task is to quantize a [[Poisson manifold]], then both methods, [[Maxim Kontsevich]]'s construction of [[deformation quantization]] as well as [[Eli Hawkins]]' geometric quantization pass through a [[n-plectic geometry|2-plectic geometry]] on the [[Poisson Lie algebroid]] which is induced by the Poisson manifold; Kontsevich's construction of the [[star product]], as clarified by Cattaneo and Felder, is really that of the 3-point function in the 2-dimension [[sigma-model]] QFT whose [[target space]] is that Poisson Lie algebroid -- the [[Poisson sigma-model]] --, and the symplectic 2-groupoid that Hawkins et al consider is the 
"extended" geometric quantization over the as in [[extended prequantum field theory]] associated with this theory.

For more on this see at [[extended geometric quantization of 2d Chern-Simons theory]]


## Examples

### Ordinary geometric quantization of a symplectic manifold

For $(X,\pi = \omega^{-1})$ an ordinary [[symplectic manifold]]
the [[symplectic groupoid]] is just the [[pair groupoid]]
equipped with the multiplicative form $s^* \omega + t^* \bar \omega$.
Any ordinary [[prequantum line bundle]] $P$ and [[polarization]]
$\mathcal{F}$ of $(X,\omega)$ induces a prequantization
$s^* L + t^* \bar L$ and coresponding polarization of the symplectic groupoid. The resulting [[twisted convolution algebra]] is that of [[compact operators]] on $X/\mathcal{F}$. 

([EH, example 6.1](#EH))


### Moyal quantization of Poisson vector space
 {#MoyalQuantizationofPoissonVectorSpace}

For $(X,\pi)$ a Poisson vector space, hence a [[vector space]] $X = V$ equipped with a constant (translating invariant) [[Poisson bivector]], the geometric quantization of the corresponding [[symplectic groupoid]] yields the [[Moyal quantization]] of $(V, \pi)$.

([GBV 94](#GBV), [EH 06, example 6.2](#EH))


## Related concepts

* [[symplectic manifold]], [[geometric quantization]]

* [[C-star algebraic deformation quantization]]

* [[Poisson Lie algebroid]] $\stackrel{\exp(-)}{\mapsto}$ [[symplectic groupoid]] $\stackrel{central extension}{\mapsto}$ **geometric quantization of symplectic groupoids**

* [[symplectic Lie n-algebroid]] $\stackrel{\exp(-)}{\mapsto}$ [[symplectic ∞-groupoid]] $\stackrel{central extension}{\mapsto}$ [[geometric quantization of symplectic ∞-groupoids]]


## References

Symplectic groupoids were introduced as intended tools for the quantization of Poisson manifolds in

* [[Alan Weinstein]], [[Ping Xu]], _Extensions of symplectic groupoids and quantization_, Journal f&#252;r die reine und angewandte Mathematik (1991) Volume 417 ([pdf](http://www.digizeitschriften.de/dms/img/?PPN=GDZPPN00220858X))

Their [[prequantization]] is developed in

* [[Camille Laurent-Gengoux]], [[Ping Xu]], _Quantization of pre-quasi-symplectic groupoids and their Hamiltonian spaces_ in _The Breadth of Symplectic and Poisson Geometry_ Progress in Mathematics, 2005, Volume 232, 423-454 ([arXiv:math/0311154](http://arxiv.org/abs/math/0311154)) 
 {#LGX}

* [[Marius Crainic]], _Prequantization and Lie brackets_ ([arXiv:0403269](http://arxiv.org/abs/math/0403269))

* [[Marius Crainic]], [[Chenchang Zhu]], _Integrability of Jacobi structures_ ([arXiv:math/0403268](http://arxiv.org/abs/math/0403268))
  {#CrainicZhu04}

* Francesco Bonechi, [[Alberto Cattaneo]], [[Maxim Zabzine]], _Geometric quantization and non-perturbative Poisson sigma model_,  	Adv. Theor. Math. Phys. 10:683-712, 2006 ([arXiv:math/0507223](http://arxiv.org/abs/math/0507223))
  {#BonechiCattaneoZabzine05}

The interpretation of symplectic groupoids in [[higher geometry]] is made fairly explicit in ([LGX](#LGX)) above. This is further expanded on in the last section of 

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_ 2013
  {#hgp13}

and in 

* [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local boundary prequantum field theory]]_, thesis, August 2013
  {#Nuiten13}

* [[Stefan Bongers]], _[[schreiber:master thesis Bongers]]_
  {#Bongers13}


A notion of [[polarization]] and of actual [[geometric quantization]] of symplectic groupoids, yielding a [[strict deformation quantization]] of the underlying Poisson manifold, is discussed in

* [[Eli Hawkins]], _A groupoid approach to quantization_,  J. Symplectic Geom. Volume 6, Number 1 (2008), 61-125. ([arXiv:math.SG/0612363](http://arxiv.org/abs/math.SG/0612363))
  {#EH}

The case over Poisson vector spaces leading to [[Moyal quantization]] was considered earlier in 

* Jose M. Gracia-Bondia, Joseph C. Varilly, _From geometric quantization to Moyal quantization_, J. Math. Phys. 36 (1995) 2691-2701 ([arXiv:hep-th/9406170](http://arxiv.org/abs/hep-th/9406170))
 {#GBV}


