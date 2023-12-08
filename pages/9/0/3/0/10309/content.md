
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

The 2-dimensional [[sphere]] naturally carries the structure of a [[Poisson manifold]], in fact of a [[symplectic manifold]], with its standard [[volume form]] serving as the [[symplectic form]]. As such one may consider the ([[strict deformation quantization|strict]]) [[deformation quantization]] of its [[Poisson algebra]] of functions.

## Details
 {#Details}

There are various notions of deformation quantization which one may consider. By default one often means [[formal deformation quantization]] with values in [[formal power series]] in [[Planck's constant]] $\hbar$. One definition of *strict* deformation quantization takes it to be such a formal deformation quantization which happens to [[convergence of a sequence|converge]] for finite [[real number]] values of $\hbar$. This is not known to exist for the 2-sphere.

However, there are other notions of strict quantization via deformation of the algebra of functions (review in [Hawkins (2007), Section 2](#Hawkins07)).

### Formal deformation quantization

(...)

### Strict deformation quantization

One kind of [[strict deformation quantization]] of the 2-sphere is obtained as follows &lbrack;[Hawkins (2007), section 4](#Hawkins07)&rbrack;. 

Take the [[volume]] of the 2-sphere to be a [[natural number]]. Then there is a [[prequantum line bundle]] $(L,\nabla)$ on $S^2$ whose [[curvature]] 2-form is the [[symplectic form]], hence the [[volume form]], and which is a [[holomorphic line bundle]] with respect to the standard [[complex manifold]] structure of the 2-sphere (the [[Riemann sphere]]). 

For $N \in \mathbb{N}_+$ a positive [[natural number]], the [[geometric quantization]] of the 2-[[sphere]] for [[Planck's constant]] $\hbar = 1/N$ produced the [[space of quantum states]]

$$
  \mathcal{H}_N = \Gamma_{hol}(S^2, L^{\otimes N})
$$

which is the [[space of sections|space of holomorphic sections]] of the $N$th tensor power of the [[prequantum line bundle]]. See at _[[geometric quantization of the 2-sphere]]_.

This is a [[finite dimensional vector space|finite-dimensional]] [[complex vector space|complex]] [[Hilbert space]], hence becomes a [[module]] over the  [[matrix algebra]] $Mat_N(\mathbb{C})$.

One finds that the assignment

$$
  \left\{
    0 , \cdots, \frac{1}{N}, \cdots, \frac{1}{3}, \frac{1}{2}, 1
  \right\}
  \longrightarrow
  C^\ast Alg
$$

which sends $\frac{1}{N}$ to $Mat_N(\mathbb{C})$ is a [[strict deformation quantization]] of the 2-sphere.

## Related concepts

* [[quantization of the 2-sphere]]

  * [[geometric quantization of the 2-sphere]]

  * **deformation quantization of the 2-sphere**

## References

* {#Hawkins07} [[Eli Hawkins]], Section 4 of: *An Obstruction to Quantization of the Sphere*, Communications in Mathematical Physics **283** (2008) 675–699  &lbrack;[arXiv:0706.2946](http://arxiv.org/abs/0706.2946), [doi:10.1007/s00220-008-0517-2](https://doi.org/10.1007/s00220-008-0517-2)&rbrack;
 
following

* {#BordemannMeinrenkenSchlichenmaier93} [[Martin Bordemann]], [[Eckhard Meinrenken]], [[Martin Schlichenmaier]], _Toeplitz Quantization of Kähler Manifolds and $gl(N)$ $N\to\infty$_,  	Commun. Math. Phys. **165** (1994) 281-296 &lbrack;[arXiv:hep-th/9309134](http://arxiv.org/abs/hep-th/9309134), [doi:10.1007/BF02099772](https://doi.org/10.1007/BF02099772)&rbrack;
 

[[!redirects strict deformation quantization of the 2-sphere]]

