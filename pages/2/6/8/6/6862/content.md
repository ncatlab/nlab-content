+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### $\infty$-Wess-Zumino-Witten theory
+--{: .hide}
[[!include infinity-Wess-Zumino-Witten theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

In the broad meaning a _current algebra_ is the [[Poisson bracket]] algebra of [[conserved currents]] of a [[prequantum field theory]], or else its quantized version of the corresponding [[quantum field theory]].

If the [[symmetry]] corresponding to the [[conserved currents]] via [[Noether's theorem]] preserves the given [[Lagrangian]] only up to a [[divergence]] term, then the current algebra is a [[central extension]] of the Lie algebra of the underlying symmetries. This effect makes current algebras tend to be subtle and of particular mathematical interest.

Particularly famous is the case of the [[WZW model|WZW sigma model]] field theory for a [[string]] propagating on a [[Lie group]] $G$. In this case one chiral half of the algebra of currents is the corresponding [[affine Lie algebra]]. In parts of the (mathematical) literature it is this special case which meant by default by the term _current algebra_.

In fact, taking into account that this [[divergence]] term itself in general has [[higher gauge symmetries]], current algebras are secretly [[strong homotopy Lie algebras]]/[[Lie n-algebras]]. This we discuss [below](#AsAHomotopyLieAlgebra).


## As a homotopy Lie algebra
 {#AsAHomotopyLieAlgebra}

With [[local prequantum field theory]] formulated as [[de Donder-Weyl field theory]], every [[local Lagrangian]] is incarnated as a  [[circle n-bundle with connection]] $\mathbf{L}$ on some space $X$ (for instance on the [[jet bundle]] of a [[field bundle]]), such that its [[curvature]] form $\omega$ determines by its [[kernel]] the tangents to the solutions of the [[equations of motion]]. ([cftcht, 3.1, 3.2,  3.4](#cftcht)).

A [[symmetry]] of the theory which preserves the Lagrangian up to a [[divergence]] is then precisely a [[quantomorphism n-group|quantomorphism]] of $\mathbf{L}$, namely a pair consisting of the symmetry

$$
  \phi \colon X \stackrel{\simeq}{\longrightarrow} X
$$

together with an [[equivalence]]

$$
  \eta \colon \phi^\ast \mathbf{L} \stackrel{\simeq}{\longrightarrow} \mathbf{L}
  \,.
$$

Under [[Lie differentiation]] this gives (this has strictly been proven only for low $n$, but is sort of obvious generally) the [[Poisson bracket Lie n-algebra]] $\mathfrak{Pois}(\mathbf{L})$. In its [[dg-Lie algebra]] version spelled out [here](Poisson+bracket+Lie+n-algebra#PoissondgAlgebra) this has, in degree 0,  precisely the Lie bracket of conserved currents as known from traditional literature, for instance ([Azcarraga-Townsend 89](#AzcarragaTownsend89)). Details are in [cftcht, 3.3](#cftcht).


## References

* Sam Treiman,  [[Roman Jackiw]], [[David Gross]],  _Lectures on current algebra and its applications_ , Princeton University Press. (1972) 

* [[Steven Weinberg]], _Current Algebra and Gauge Theories. I_ Phys. Rev. D 8, 605&#8211;625 (1973) 

* Herbert Pietschmann, _On the Early History of Current Algebra_ ([arXiv:1101.2748](http://arxiv.org/abs/1101.2748))

General discussion and application to the [[Green-Schwarz super p-brane sigma models]] is in

* {#AzcarragaTownsend89} [[José de Azcárraga]], [[Paul Townsend]], _Superspace geometry and the classification of supersymmetric extended objects_, Physical Review Letters Volume 62, Number 22 (1989)

Discussion from an [[nPOV]] is in

* {#cftcht} _[[schreiber:Classical field theory via Cohesive homotopy types]]_

[[!redirects current algebras]]