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

With [[local prequantum field theory]] in [[dimension]] $d$ formulated as [[de Donder-Weyl field theory]], every [[local Lagrangian]] is incarnated as a  [[circle n-bundle with connection|principal d-form connection]] $\mathbf{L}$ on some [[space]] $X$, such that its [[curvature]] form $\omega$ determines by its [[kernel]] the tangents to the solutions of the [[equations of motion]]. (see [cftcht, sections 3.1, 3.2,  3.4](#cftcht)).

What is traditionally considered in the literature is the special case of this where $X$ is the (dualized, first) [[jet bundle]] of a [[field bundle]] over a [[smooth manifold]] (see at _[[multisymplectic geometry]]_) and the underlying [[principal infinity-bundle]] of $\mathbf{L}$ is trivial, so that $\mathbf{L}$ is incarnated as a globally defined [[differential n-form|differential d-form]]. Moreover, this is traditionally expressed as the product $L \, vol$ of a [[smooth function]] times a prescribed [[volume form]]. This function $L$ then is what in much of the traditional literure is referred to as the Lagrangian of the [[theory (physics)|theory]].


A [[symmetry]] of the theory which preserves the Lagrangian up to a [[divergence]] is then precisely a [[quantomorphism n-group|quantomorphism]] of $\mathbf{L}$, namely a pair consisting of the symmetry

$$
  \phi \colon X \stackrel{\simeq}{\longrightarrow} X
$$

together with an [[equivalence]]

$$
  \eta \colon \phi^\ast \mathbf{L} \stackrel{\simeq}{\longrightarrow} \mathbf{L}
  \,.
$$

When expressing $\mathbf{L}$ as a [[modulating morphism]] $\mathbf{L} \colon X \longrightarrow \mathbf{B}^d U(1)_{conn}$ into the [[smooth infinity-stack|smooth]] [[moduli infinity-stack]] of [[circle n-bundle with connection|circle d-bundles with connection]] then this is an equivalence in the [[slice (infinity,1)-topos]] over $\mathbf{B}^d U(1)_{conn}$:

$$
  \mathbf{QuantMorph}(\mathbf{L})
  =
  \left\{
  \array{
    X && \stackrel{\phi}{\longrightarrow} && X
    \\
    & \searrow &\swArrow_{\eta}& \swarrow
    \\
    && \mathbf{B}^d U(1)_{conn}
  }
  \right\}
  \,.
$$

(The detailed definition of this [[quantomorphism n-group|quantomorphism d-group]] involved [[differential concretification]] of the naive [[automorphism infinity-group]] in the slice.)

Under [[Lie differentiation]] this gives [^Lie] the [[Poisson bracket Lie n-algebra]] $\mathfrak{Pois}(\mathbf{L})$. In its [[dg-Lie algebra]] version spelled out [here](Poisson+bracket+Lie+n-algebra#PoissondgAlgebra) and restricted to the special case of globally defined Lagrangian form,  this has, in degree 0,  precisely the Lie bracket of conserved currents as known from traditional literature, for instance ([AGIT89, equations (13), (14)](#AGIT89)). Details are in [cftcht, 3.3](#cftcht).

But the $\mathfrak{Pois}(\mathbf{L})$ contains in addition the equivalence between two central terms, coming from [[higher gauge transformations]]. Taking this into account, the [extension theorem](Poisson+bracket+Lie+n-algebra#ExtensionTheorem) for $\mathfrak{Pois}(X,\omega)$ says that its truncation to a Lie algebra is an extension by $H^{d-1}_{dR}(X)$.  This has been informally argued for instance in [AGIT 89, p. 8](#AGIT89).

[^Lie This has strictly been proven only for low $n$, but is sort of obvious generally ]



## References

* Sam Treiman,  [[Roman Jackiw]], [[David Gross]],  _Lectures on current algebra and its applications_ , Princeton University Press. (1972)  ([publisher](http://press.princeton.edu/titles/2071.html))

* [[Steven Weinberg]], _Current Algebra and Gauge Theories. I_ Phys. Rev. D 8, 605&#8211;625 (1973) 

* Herbert Pietschmann, _On the Early History of Current Algebra_ ([arXiv:1101.2748](http://arxiv.org/abs/1101.2748))

General discussion and application to the [[Green-Schwarz super p-brane sigma models]] is in


* {#AGIT89} [[José de Azcárraga]], [[Jerome Gauntlett]], J.M. Izquierdo, [[Paul Townsend]], _Topological Extensions of the Supersymmetry Algebra for Extended Objects_, Phys. Rev. Lett. 63 (1989) 2443 ([spire](http://inspirehep.net/record/26393?ln=en))


Discussion from an [[nPOV]] is in

* {#cftcht} _[[schreiber:Classical field theory via Cohesive homotopy types]]_

[[!redirects current algebras]]