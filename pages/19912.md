[[!redirects Feynman amplitude on compactified configuration spaces of points]]
[[!redirects Feynman amplitudes on compactified configuration spaces of points]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[perturbative quantum field theory]] an alternative to regarding [[propagators]]/[[Feynman amplitudes]] as [[distributions of several variables]] with [[singularities]] at (in particular) coincident points, one may [[pullback of distributions|pull-back]] these distributions to [[smooth functions]]/[[differential forms]] on [[Fulton-MacPherson compactifications]] of [[configuration spaces]] of points and study their [[renormalization]] from this perspective. Vaguely analogous to the perspective of [[wavefront sets]], this perspective amounts to recording around each potentially singular point an [[n-sphere]] worth of extra [[direction of a vector|directional]] information carried by the [[Feynman amplitude]] in the vicinity of the point.

A general and systematic discussion of [[perturbative quantum field theory]] and its [[renormalization]] from this perspective is offered in [Berghoff 14a](#Berghoff14a), [Berghoff 14b](#Berghoff14b) (albeit presently only for [[Euclidean quantum field theory]], not for [[relativistic quantum field theory]]).

## Examples

### Higher Chern-Simons theory


This approach to [[pQFT]] was originally considered specifically for the [[Chern-Simons propagator]] in  [[quantization of 3d Chern-Simons theory]] in [Axelrod-Singer 93](#AxelrodSinger93), see also [Bott-Cattaneo 97, Remark 3.6](#BottCattaneo97) and [Cattaneo-Mnev 10, Remark 11](#CattaneoMnev10). The analysis applies verbatim to [[higher Chern-Simons theory]] such as notably the [[AKSZ sigma-models]], too, since the [[Feynman propagator]]  depends only on the [[free field theory]]-[[equations of motion]], which is $d A = 0$ in all these cases. 

Here the [[Chern-Simons propagator]] regarded as a non-singular [[differential form]] on the [[Fulton-MacPherson compactification|compactification]] of the [[configuration space of points]] serves to exhibit its [[Feynman amplitudes]] as providing [[graph complex]]-models for the [[de Rham cohomology]] of these [[Fulton-MacPherson compactification|compactified]] [[configuration spaces of points]], a point originally due to [Kontsevich 94](#Kontsevich94) and re-amplified for instance [Campos-Idrissi-Lambrechts-Willwacher 18, p. 66](#CamposIdrissiLambrechtsWillwacher18).


## References

The approach was originally considered specifically for [[Chern-Simons theory]] in 

* {#AxelrodSinger93} [[Scott Axelrod]], [[Isadore Singer]],  _Chern--Simons Perturbation Theory II_, J. Diff. Geom. 39 (1994) 173-213 ([arXiv:hep-th/9304087](http://arxiv.org/abs/hep-th/9304087)) 

which was re-amplified  in 

* {#BottCattaneo97} [[Raoul Bott]], [[Alberto Cattaneo]], Remark 3.6 in _Integral invariants of 3-manifolds_, J. Diff. Geom., 48 (1998) 91-133 ([arXiv:dg-ga/9710001](https://arxiv.org/abs/dg-ga/9710001))

* {#CattaneoMnev10} [[Alberto Cattaneo]], [[Pavel Mnev]], Remark 11 in _Remarks on Chern-Simons invariants_, Commun.Math.Phys.293:803-836,2010 ([arXiv:0811.2045](https://arxiv.org/abs/0811.2045))

and highlighted as a means to obtain [[graph complex]]-models for the [[de Rham cohomology]] of [[configuration spaces of points]] in 

* {#Kontsevich94} [[Maxim Kontsevich]], pages 11-12 of _Feynman diagrams and low-dimensional topology_, First European Congress of Mathematics, 1992, Paris, vol. II, Progress in Mathematics __120__, Birkh&#228;user (1994), 97&#8211;121 ([pdf](http://www.ihes.fr/~maxim/TEXTS/Feynman%20%20diagrams%20and%20low-dimensional%20topology.pdf))

* {#CamposIdrissiLambrechtsWillwacher18} [[Ricardo Campos]], Najib Idrissi, [[Pascal Lambrechts]], [[Thomas Willwacher]], _Configuration Spaces of Manifolds with Boundary_ ([arXiv:1802.00716](https://arxiv.org/abs/1802.00716))


A systematic development of [[perturbative quantum field theory]] with [[Feynman amplitudes]] considered as [[smooth functions]] on [[Fulton-MacPherson compactifications]]/[[wonderful compactifications]] of [[configuration spaces of points]] and more generally of subspace arrangements is due to 

* {#BergbauerBrunettiKreimer09} [[Christoph Bergbauer]], [[Romeo Brunetti]], [[Dirk Kreimer]], _Renormalization and resolution of singularities_ ([arXiv:0908.0633](https://arxiv.org/abs/0908.0633))

* {#Berghoff14a} [[Marko Berghoff]], _Wonderful renormalization_, 2014 ([pdf](http://www2.mathematik.hu-berlin.de/%7Ekreimer/wp-content/uploads/Berghoff-Marko.pdf), [doi:10.18452/17160](https://doi.org/10.18452/17160))

* {#Berghoff14b} [[Marko Berghoff]], _Wonderful compactifications in quantum field theory_,  Communications in Number Theory and Physics Volume 9 (2015) Number 3 ([arXiv:1411.5583](https://arxiv.org/abs/1411.5583))

