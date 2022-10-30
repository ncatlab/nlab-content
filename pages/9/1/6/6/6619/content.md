
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

(...)

([Hawkins, section 4.2](#EH))

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

(??)

(...)

## Properties

### Relation to deformation quantization

There does not seem to be in the literazure a precise relation between the methods of [[geometric quantization]] discussed here and methods of [[deformation quantization]]. But the following similarity might be relevant:

If the task is to quantize a [[Poisson manifold]], then both methods, [[Maxim Kontsevich]]'s construction of [[deformation quantization]] as well as [[Eli Hawkins]]' geometric quantization pass through a [[n-plectic geometry|2-plectic geometry]] on the [[Poisson Lie algebroid]] which is induced by the Poisson manifold; Kontsevich's construction of the [[star product]], as clarified by Cattaneo and Felder, is really that of the 3-point function in the 2-dimension [[sigma-model]] QFT whose [[target space]] is that Poisson Lie algebroid -- the [[Poisson sigma-model]] --, and the symplectic 2-groupoid that Hawkins et al consider is the 
"extended" geometric quantization over the as in [[extended prequantum field theory]] associated with this theory.

For more on this see at [[extended geometric quantization of 2d Chern-Simons theory]]

## Definition

Given a [[symplectic groupoid]] $(X,\omega)$, the symplectic form defines a class in degree-3 [[de Rham cohomology]] $H_{dR}^3(X)$. 

(Notice that, while this $\omega$ is typically expressed as a 2-form on $X_1$, this represents indeed a degree-3 cocycle in the [[simplicial de Rham complex]] of the [[nerve]] of $X$).

We say that $\omega$ is _integral_ if it is in the image of the [[curvature]] map 

$$
  curv : H^2_{diff}(X,U(1)) \to H^3_{dR}(X)
$$

from the [[ordinary differential cohomology]] of $X$. If this is the case, we say that a lift $(\hat X, \nabla)$ of $\omega$ to $\mathbf{H}_{diff}(X, \mathbf{B}^2 U(1))$, hence to the [[2-groupoid]] of [[circle n-bundle with connection|circle 2-bundles with connection]] over $X$, is a **prequantum line bundle** for $(X,\omega)$.

Notice that this traditional terminology is off by one: the underlying $\hat X \to X$ is a [[circle 2-group]]-[[principal 2-bundle]] on $X$.

## Related concepts

* [[symplectic manifold]], [[geometric quantization]]

* [[C-star algebraic deformation quantization]]

* [[Poisson Lie algebroid]] $\stackrel{\exp(-)}{\mapsto}$ [[symplectic groupoid]] $\stackrel{central extension}{\mapsto}$ **geometric quantization of symplectic groupoids**

* [[symplectic Lie n-algebroid]] $\stackrel{\exp(-)}{\mapsto}$ [[symplectic ∞-groupoid]] $\stackrel{central extension}{\mapsto}$ [[geometric quantization of symplectic ∞-groupoids]]


## References

Symplectic groupoids were introduced as intended tools for the quantization of Poisson manifolds in

* [[Alan Weinstein]], [[Ping Xu]], _Extensions of symplectic groupoids and quantization_, Journal f&#252;r die reine und angewandte Mathematik (1991) Volume 417 ([pdf](http://www.digizeitschriften.de/dms/img/?PPN=GDZPPN00220858X))

Their [[prequantization]] are developed in

* [[Camille Laurent-Gengoux]], [[Ping Xu]], _Quantization of pre-quasi-symplectic groupoids and their Hamiltonian spaces_ in _The Breadth of Symplectic and Poisson Geometry_ Progress in Mathematics, 2005, Volume 232, 423-454 ([arXiv:math/0311154](http://arxiv.org/abs/math/0311154)) 
 {#LGX}

* [[Marius Crainic]], _Prequantization and Lie brackets_ ([arXiv:0403269](http://arxiv.org/abs/math/0403269))

* [[Marius Crainic]], [[Chenchang Zhu]], _Integrability of Jacobi structures_ ([arXiv:math/0403268](http://arxiv.org/abs/math/0403268))

The interpretation of symplectic groupoids in [[higher geometry]] is made fairly explicit in ([LGX](#LGX)) above.

A notion of [[polarization]] and of actual [[geometric quantization]] of symplectic groupoids, yielding a [[strict deformation quantization]] of the underlying Poisson manifold, is discussed in

* [[Eli Hawkins]], _A groupoid approach to quantization_,  J. Symplectic Geom. Volume 6, Number 1 (2008), 61-125. ([arXiv:math.SG/0612363](http://arxiv.org/abs/math.SG/0612363))
  {#EH}


An informal review of some aspects of this article is in

* [[Urs Schreiber]], 

  * [A Groupoid approach to quantization](http://golem.ph.utexas.edu/category/2008/06/a_groupoid_approach_to_quantiz.html)

  * [Landsman on Quantization of Poisson Algebras Associated to Lie Algebroids](http://golem.ph.utexas.edu/category/2008/06/landsmanon_quantization_of_poi.html)

  * [Eli Hawkins on Geometric Quantization I](http://golem.ph.utexas.edu/category/2008/06/eli_hawkins_on_geometric_quant.html)

  * [Eli Hawkins on Geometric Quantization II](http://golem.ph.utexas.edu/category/2008/06/eli_hawkins_on_geometric_quant_1.html)

