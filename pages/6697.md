
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Riemannian geometry
+-- {: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Gravity
+-- {: .hide}
[[!include gravity contents]]
=--
=--
=--


#Contents#
* table of contents
{: toc}

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/AdSSlicingByHyperbolic.jpg" width="400">
</div>


## Definition

Up to [[isometry]], the **anti de Sitter spacetime** of [[dimension]] $d$, $AdS_d$, is the [[pseudo-Riemannian manifold]] whose underlying [[manifold]] is the [[submanifold]] of the [[Minkowski spacetime]] $\mathbb{R}^{d-1,2}$ that solves the equation

$$
  \sum_{i = 1}^{d-1} (x_i)^2 - (x_d)^ 2 - (x_0)^2 = -R^2
$$

for some $R \neq 0$ (the "radius" of the spacetime) and equipped with the metric induced from the ambient metric, where $\{x^0, x^1, x^2, \cdots, x^d\}$ denote the canonical [[coordinates]]. $AdS_d$ is [[homeomorphic]] to $\mathbb{R}^{d-1} \times S^1$, and its isometry group is $O(d-1, 2)$.

More generally, one may define the anti de Sitter space of signature $(p,q)$ as isometrically embedded in the space $\mathbb{R}^{p,q+1}$ with coordinates $(x_1, ..., x_p, t_1, \ldots, t_{q+1})$ as the sphere $\sum_{i=1}^p x_i^2 - \sum_{j=1}^{q+1} t_j^2 = -R^2$.

> graphics grabbed from [Yan 19](holographic+entanglement+entropy#Yan19)

## Properties

### Coordinate charts

(...)

in _horospheric coordinates_ the AdS [[metric tensor]] is

$$
  g_{AdS}
  \;=\;
  \frac{1}{z^2}
  \left(
    g_{(\mathbb{R}^{p,1})} + (d z)^2 
  \right)
$$

In terms of

$$
  y \coloneqq 1/z 
$$

this becomes

$$
  g_{AdS}
  \;=\;
  y^2 \, g_{(\mathbb{R}^{p,1})} + \frac{1}{y^2}(d y)^2 
$$

and with 

$$
  y \coloneqq \tfrac{1}{n} r^n
$$

for $n \neq 0$

we get

$$
  g_{AdS}
  \;=\;
  \tfrac{1}{n^2}r^{2n} \, g_{(\mathbb{R}^{p,1})} + \frac{1}{r^2}(d r)^2 
$$



### Conformal boundary

(...)

### Holography

Asymptotically anti-de Sitter spaces play a central role in the realization of the [[holographic principle]] by [[AdS/CFT correspondence]].

### In $p$-adic geometry

A [[p-adic geometry|2-adic]] [[arithmetic geometry]]-version of [[AdS spacetime]] is identified with the [[Bruhat-Tits tree]] for the [[projective general linear group]] $PGL(2,\mathbb{Q}_p)$:

<center>
  <img src="https://ncatlab.org/nlab/files/BruhatTitsTreeOfSL2.jpg" width="600">
</center>

> graphics from [Casselman 14](Bruhat-Tits+tree#Casselman14)

In the [[p-adic AdS/CFT correspondence]] this may be regarded (at some finite depth truncation) as a [[tensor network state]]: 

<center>
<img src="https://ncatlab.org/nlab/files/BruhatTitsTreeTensorNetworkStateFromMetricLie.jpg" width="300">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

and as such validates the [[Ryu-Takayanagi formula]] for [[holographic entanglement entropy]].

## Related concepts

* [[thermal AdS3]]

* [[anti de Sitter group]]

* [[de Sitter spacetime]]

* [[super anti de Sitter spacetime]]

* [[near-horizon geometry]]

* [[singleton representation]]

* [[AdS/CFT correspondence]], [[AdS/QCD correspondence]]

## References

### General

Reviews:

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], volume 1, chapter I.3.8 of: _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

* [[Ingemar Bengtsson]], _Anti-de Sitter space_, lecture notes 1998 ([[Bengtsson98.pdf:file]])

* [[Matthias Blau]], chapter 38 of: _Lecture notes on general relativity_ ([web](http://www.blau.itp.unibe.ch/GRLecturenotes.html))

* [[Gary Gibbons]], _Anti-de-Sitter spacetime and its uses_ ([arXiv:1110.1206](http://arxiv.org/abs/1110.1206))

* {#Natsuume15} [[Makoto Natsuume]], section 6 of: _AdS/CFT Duality User Guide_, Lecture Notes in Physics 903, Springer 2015 ([arXiv:1409.3575](https://arxiv.org/abs/1409.3575))

* Leszek M. Sokolowski, _The bizarre anti-de Sitter spacetime_, International Journal of Geometric Methods in Modern Physics 13 no.9 (2016) 1630016 ([arXiv:1611.01118](https://arxiv.org/abs/1611.01118))


See also:

* Wikipedia, _[anti de Sitter space](http://en.wikipedia.org/wiki/Anti_de_Sitter_space)_

Further discussion:

* Abdelghani Zeghib, _On closed anti de Sitter spacetimes_, Math. Ann. 310, 695&#8211;716 (1998) ([pdf](http://www.umpa.ens-lyon.fr/~zeghib/Anti.de.Sitter.pdf))


* C. Frances, _The conformal boundary of anti-de Sitter space-times_, in  _AdS/CFT correspondence: Einstein metrics and their conformal boundaries_ , 205--216, IRMA Lect. Math. Theor. Phys., 8, Eur. Math. Soc., Z&#252;rich, 2005 ([pdf](http://mahery.math.u-psud.fr/~frances/ads-cft2.pdf))

* Jiri Podolsky, Ondrej Hruska, _Yet another family of diagonal metrics for de Sitter and anti-de Sitter spacetimes_, Phys. Rev. D 95, 124052 (2017) ([arXiv:1703.01367](https://arxiv.org/abs/1703.01367))

Discussion of thermal [[Wick rotation]] on global [[anti-de Sitter spacetime]]  (which is already periodic in _real_ time) to [[Euclidean field theory]] with periodic _imaginary_ time is in

* {#AllenFolacciGibbons87} B. Allen, A. Folacci, [[Gary Gibbons]], _Anti-de Sitter space at finite temperature_, Physics Letters B Volume 189, Issue 3, 7 May 1987, Pages 304-310 (<a href="https://doi.org/10.1016/0370-2693(87)91437-7">doi:10.1016/0370-2693(87)91437-7</a>)

Discussion of [[black holes in anti de Sitter spacetime]]:

* Hawking, Stephen W., and Don N. Page. "Thermodynamics of black holes in anti-de Sitter space." Communications in Mathematical Physics 87.4 (1983): 577-588.

* {#Socolovsky17} M. Socolovsky, _Schwarzschild Black Hole in Anti-De Sitter Space_ ([arXiv:1711.02744](https://arxiv.org/abs/1711.02744))

* Peng Zhao, _Black Holes in Anti-de Sitter Spacetime_ ([pdf](https://pdfs.semanticscholar.org/9939/335e0d282e70201d6087988bf4f5aedfc8f6.pdf))

* Jakob Gath, _The role of black holes in the AdS/CFT correspondence_ ([pdf](https://www.imperial.ac.uk/media/imperial-college/research-centres-and-groups/theoretical-physics/msc/dissertations/2009/Jakob-Gath-Dissertation-2009.pdf))

Relation to [[Teichmüller theory]]:

* Francesco Bonsante, Andrea Seppi, _Anti-de Sitter geometry and Teichmüller theory_ ([arXiv:2004.14414](https://arxiv.org/abs/2004.14414))


### As string vacua

On (in-)stability of non-[[supersymmetry|supersymmetric]] [[AdS spacetime|AdS]] [[string theory vacua|vacua in string theory]]:

* [[Iosif Bena]], [[Krzysztof Pilch]], [[Nicholas Warner]], _Brane-Jet Instabilities_,  J. High Energ. Phys. 2020, 91 (2020) ([arXiv:2003.02851](https://arxiv.org/abs/2003.02851))



[[!include pp-waves as Penrose limits of AdS spacetimes -- references]]

[[!redirects anti de Sitter space]]
[[!redirects anti de Sitter spaces]]
[[!redirects anti-de Sitter space]]
[[!redirects anti-de Sitter spaces]]
[[!redirects anti de Sitter spacetime]]
[[!redirects anti de Sitter spacetimes]]
[[!redirects anti-de Sitter spacetime]]
[[!redirects anti-de Sitter spacetimes]]

[[!redirects anti de-Sitter spacetime]]

[[!redirects AdS-spacetime]]
[[!redirects AdS-spacetimes]]

[[!redirects horospheric coordinates]]
[[!redirects horospheric coordinate chart]]
[[!redirects horospheric coordinate charts]]

[[!redirects AdS spacetime]]
[[!redirects AdS spacetimes]]

[[!redirects AdS]]
