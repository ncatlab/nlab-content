

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

In [[Euclidean field theory]], an alternative to regarding [[propagators]]/[[correlators]] as [[distributions of several variables]] with [[singularities]] on the [[fat diagonal]], is to [[pullback of distributions|pull-back]] these distributions to [[smooth functions]]/[[differential forms]] on ([[Fulton-MacPherson compactifications]] of) [[configuration spaces of points]] and regard them in this incarnation, in particular discuss their [[renormalization]] from this perspective.

Analogous to the perspective of [[wavefront sets]] for distributions, this perspective amounts to recording around each potentially singular point an [[n-sphere|(d-1)-sphere]] worth of extra [[direction of a vector|directional]] information carried by the [[correlator]]/[[Feynman amplitude]] in the vicinity of the point.

This approach goes back to [Axelrod-Singer 93](#AxelrodSinger93) in the discussion of [[perturbative quantum field theory|perturbative]] [[quantization of Chern-Simons theory]]. Here the [[graph complex]] of [Kontsevich 94](#Kontsevich94) (full details due to [Lambrechts-Volić 14](#LambrechtsVolic14)) shows that the [[de Rham algebra]] of the [[configuration space of points]] is actually [[quasi-isomorphism|quasi-isomorphic]] to all possible [[Feynman amplitudes]] for free [[Chern-Simons theory|Chern-Simons]]/[[AKSZ theory]].

A general and systematic discussion of [[perturbative quantum field theory]] and its [[renormalization]] from this perspective is offered in [Berghoff 14a](#Berghoff14a), [Berghoff 14b](#Berghoff14b) (albeit presently only for [[Euclidean quantum field theory]], not for [[relativistic quantum field theory]]).

## Examples

### Higher Chern-Simons theory


This approach to [[pQFT]] was originally considered specifically for the [[Chern-Simons propagator]] in  [[quantization of 3d Chern-Simons theory]] in [Axelrod-Singer 93](#AxelrodSinger93), see also [Bott-Cattaneo 97, Remark 3.6](#BottCattaneo97) and [Cattaneo-Mnev 10, Remark 11](#CattaneoMnev10). The analysis applies verbatim to [[higher Chern-Simons theory]] such as notably the [[AKSZ sigma-models]], too, since the [[Feynman propagator]]  depends only on the [[free field theory]]-[[equations of motion]], which is $d A = 0$ in all these cases. 

Here the [[Chern-Simons propagator]] regarded as a non-singular [[differential form]] on the [[Fulton-MacPherson compactification|compactification]] of the [[configuration space of points]] serves to exhibit its [[Feynman amplitudes]] as providing [[graph complex]]-models for the [[de Rham cohomology]] of these [[Fulton-MacPherson compactification|compactified]] [[configuration spaces of points]], a point due to [Kontsevich 94](#Kontsevich94), [Kontsevich 93, 5](#Kontsevich93):

\[
  \label{TheQuasiIsomorphism}
  \underset{
    \color{blue}
    \array{
      \phantom{A}
      \\
      \text{graph complex}
      \\
      \text{of n-point Feynman diagrams}
      \\
      \text{for Chern-Simons theory}
      \\
      \text{on} \; \Sigma 
    }
  }{
    Graphs_n(\Sigma)
  }
  \underoverset{
    \simeq_{\mathrlap{qi}}
  }
  {
    \color{blue}
    \array{
      \text{assign Feynman amplitudes}
      \\
      \text{of Chern-Simons theory}
      \\
      \phantom{A}
    }
  }
  {
    \longrightarrow
  }
  \underset{
    \color{blue}
    \array{
      \phantom{A}
      \\
      \text{de Rham algebra}
      \\
      \text{of semi-algebraic differential forms}
      \\
      \text{on the FM-compactification}
      \\
      \text{of the configuration space of n points}
      \\
      \text{in}\; \Sigma
    }
  }{
  \Omega^\bullet_{PA}
  \big(
    Conf_n\big(  \Sigma \big)
  \big)
  }
  \,.
\]


## Related concepts

* [[quantization of 3d Chern-Simons theory]]


## References

The approach was originally considered specifically for [[Chern-Simons theory]] in 

* {#AxelrodSinger93} [[Scott Axelrod]], [[Isadore Singer]],  _Chern--Simons Perturbation Theory II_, J. Diff. Geom. 39 (1994) 173-213 ([arXiv:hep-th/9304087](http://arxiv.org/abs/hep-th/9304087)) 

which was re-amplified  in 

* Daniel Altschuler, Laurent Freidel, Section 3 of: _Vassiliev knot invariants and Chern-Simons perturbation theory to all orders_, Commun. Math. Phys. 187 (1997) 261-287 ([arxiv:q-alg/9603010](https://arxiv.org/abs/q-alg/9603010))

* {#BottCattaneo97} [[Raoul Bott]], [[Alberto Cattaneo]], Remark 3.6 in _Integral invariants of 3-manifolds_, J. Diff. Geom., 48 (1998) 91-133 ([arXiv:dg-ga/9710001](https://arxiv.org/abs/dg-ga/9710001))

* {#CattaneoMnev10} [[Alberto Cattaneo]], [[Pavel Mnev]], Remark 11 in _Remarks on Chern-Simons invariants_, Commun. Math. Phys. 293: 803-836, 2010 ([arXiv:0811.2045](https://arxiv.org/abs/0811.2045))

* [[Alberto Cattaneo]], [[Pavel Mnev]], [[Nicolai Reshetikhin]], appendix B of _Perturbative quantum gauge theories on manifolds with boundary_, Communications in Mathematical Physics, January 2018, Volume 357, Issue 2, pp 631–730  ([arXiv:1507.01221](https://arxiv.org/abs/1507.01221), [doi:10.1007/s00220-017-3031-6](https://doi.org/10.1007/s00220-017-3031-6))

and highlighted as a means to obtain [[graph complex]]-models for the [[de Rham cohomology]] of [[configuration spaces of points]]/[[knot spaces]] in 


* {#Kontsevich93} [[Maxim Kontsevich]], _Vassiliev's knot invariants_, Advances in Soviet Mathematics, Volume 16, Part 2, 1993 ([pdf](http://pagesperso.ihes.fr/~maxim/TEXTS/VassilievKnot.pdf))

* {#Kontsevich94} [[Maxim Kontsevich]], pages 11-12 of _Feynman diagrams and low-dimensional topology_, First European Congress of Mathematics, 1992, Paris, vol. II, Progress in Mathematics __120__, Birkh&#228;user (1994), 97&#8211;121 ([pdf](http://www.ihes.fr/~maxim/TEXTS/Feynman%20%20diagrams%20and%20low-dimensional%20topology.pdf))

with full details and proofs in

* {#LambrechtsVolic14} [[Pascal Lambrechts]], [[Ismar Volić]], sections 6 and 7 of _Formality of the little N-disks operad_, Memoirs of the American Mathematical Society no. 1079, 2014  ([arxiv:0808.0457](https://arxiv.org/abs/0808.0457), [doi:10.1090/memo/1079](http://dx.doi.org/10.1090/memo/1079))

see also

* {#CamposIdrissiLambrechtsWillwacher18} [[Ricardo Campos]], Najib Idrissi, [[Pascal Lambrechts]], [[Thomas Willwacher]], _Configuration Spaces of Manifolds with Boundary_ ([arXiv:1802.00716](https://arxiv.org/abs/1802.00716))


A systematic development of [[Euclidean field theory|Euclidean]] [[perturbative quantum field theory]] with [[n-point functions]] considered as [[smooth functions]] on [[Fulton-MacPherson compactifications]]/[[wonderful compactifications]] of [[configuration spaces of points]] and more generally of subspace arrangements is due to 

* {#BergbauerBrunettiKreimer09} [[Christoph Bergbauer]], [[Romeo Brunetti]], [[Dirk Kreimer]], _Renormalization and resolution of singularities_, ESI preprint 2010 ([arXiv:0908.0633](https://arxiv.org/abs/0908.0633), [ESI:2244](https://mat.univie.ac.at/~esiprpr/esi2244.pdf))

* {#Bergbauer09} [[Christoph Bergbauer]], _Renormalization and resolution of singularities_, talks as IHES and Boston, 2009 ([pdf](http://www.emg.uni-mainz.de/Dateien/bergbauer.pdf))

* {#Berghoff14a} [[Marko Berghoff]], _Wonderful renormalization_, 2014 ([pdf](http://www2.mathematik.hu-berlin.de/%7Ekreimer/wp-content/uploads/Berghoff-Marko.pdf), [doi:10.18452/17160](https://doi.org/10.18452/17160))

* {#Berghoff14b} [[Marko Berghoff]], _Wonderful compactifications in quantum field theory_,  Communications in Number Theory and Physics Volume 9 (2015) Number 3 ([arXiv:1411.5583](https://arxiv.org/abs/1411.5583))

Analogous discussion for configuration spaces of points regarded as [[Hilbert schemes of points]] and with their [[ordinary cohomology]] replaced by [[K-theory]]:

* Jian Zhou, _K-Theory of Hilbert Schemes as a Formal Quantum Field Theory_ ([arXiv:1803.06080](https://arxiv.org/abs/1803.06080))

Discussion specifically in [[topological quantum field theory]] with an eye towards [[supersymmetry|supersymmetric]] field theory, in terms of the [[ordinary homology]] of [[configuration spaces of points]]:

* [[Christopher Beem]], [[David Ben-Zvi]], [[Mathew Bullimore]], [[Tudor Dimofte]], [[Andrew Neitzke]], _Secondary products in supersymmetric field theory_ ([arXiv:1809.00009](https://arxiv.org/abs/1809.00009))


[[!redirects correlator as differential form on configuration space of points]]
[[!redirects correlators as differential forms on configuration space of points]]

[[!redirects correlator as differential form on a configuration space of points]]
[[!redirects correlator as a differential form on a configuration space of points]]
[[!redirects correlators as differential forms on a configuration space of points]]
[[!redirects correlators as differential forms on configuration spaces of points]]

[[!redirects Feynman amplitudes as differential forms on configuration spaces of points]]


[[!redirects Feynman amplitude on compactified configuration space of points]]
[[!redirects Feynman amplitude on compactified configuration spaces of points]]
[[!redirects Feynman amplitudes on compactified configuration spaces of points]]

[[!redirects propagators regarded as differential forms on configuration spaces]]
