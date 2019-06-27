
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The 2-dimensional [[sphere]] naturally carries the structure of a [[Poisson manifold]], in fact of a [[symplectic manifold]], with its standard [[volume form]] serving as the [[symplectic form]]. As such one may consider the [[deformation quantization]] of its [[Poisson algebra]] of functions.

## Properties

### Strict deformation quantization

A [[strict deformation quantization]] of the 2-sphere is obained as follows. 

Take the [[volume]] of the 2-sphere to be a [[natural number]]. Then there is a [[prequantum line bundle]] $(L,\nabla)$ on $S^2$ whose [[curvature]] 2-form is the [[symplectic form]], hence the [[volume form]], and which is a [[holomorphic line bundle]] with respect to the standard [[complex manifold]] structure of the 2-sphere (the [[Riemann sphere]]). 

For $N \in \mathbb{N}_+$ a positive [[natural number]], the [[geometric quantization]] of the 2-[[sphere]] for [[Planck's constant]] $\hbar = 1/N$ produced the [[space of quantum states]]

$$
  \mathcal{H}_N = \Gamma_{hol}(S^2, L^{\otimes N})
$$

which is the [[space of sections|space of holomorphic sections]] of the $N$th tensor power of the [[prequantum line bundle]]. See at _[[geometric quantization of the 2-sphere]]_.

This is a finite-dimensional complex [[Hilbert space]], hence the [[matrix algebra]] $Mat_N(\mathbb{C})$ canonically acts on it. 

One finds that the assignment

$$
  \left\{
    0 , \cdots, \frac{1}{N}, \cdots, \frac{1}{3}, \frac{1}{2}, 1
  \right\}
  \longrightarrow
  C* Alg
$$

which sends $\frac{1}{N}$ to $Mat_N(\mathbb{C})$ is a [[strict deformation quantization]] of the 2-sphere ([Hawkins 07, section 4](#Hawkins07)).

## Related concepts

* [[quantization of the 2-sphere]]

  * [[geometric quantization of the 2-sphere]]

  * **deformation quantization of the 2-sphere**

## References

Section 4 of

* [[Eli Hawkins]], _An Obstruction to Quantization of the Sphere_ ([arXiv:0706.2946](http://arxiv.org/abs/0706.2946))
 {#Hawkins07}

following

* {#BordemannMeinrenkenSchlichenmaier93} Martin Bordemann, [[Eckhard Meinrenken]], Martin Schlichenmaier, _Toeplitz Quantization of K&#228;hler Manifolds and $gl(N)$ $N\to\infty$_,  	Commun.Math.Phys. 165 (1994) 281-296 ([arXiv:hep-th/9309134](http://arxiv.org/abs/hep-th/9309134))
 
