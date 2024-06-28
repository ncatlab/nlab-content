
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_D=2 [[Yang-Mills theory]]_ (D=2 YM theory) studies the [[Yang-Mills equations]] over a base [[manifold]] with [[dimension]] $D=2$. This special case allows the definition of the _Yang-Mills measure_.

## Basics

Consider:

* $G$ a [[Lie group]],

* $B$ an [[orientable]] [[Riemannian manifold|Riemannian]] [[2-manifold]],

* $E\twoheadrightarrow B$ a [[principal bundle|principal $G$-bundle]],

* $A\in\Omega_{\operatorname{Ad}}^1(E,\mathfrak{g})\cong\Omega^1(B,\operatorname{Ad}(E))$ a [[connection]],

* $F_A \coloneqq \mathrm{d}_A A=\mathrm{d}A+[A\wedge A]\in\Omega_{\operatorname{Ad}}^2(E,\mathfrak{g})\cong\Omega^2(B,\operatorname{Ad}(E))$ its [[curvature]]. 

[[Chern-Weil theory]] implies that the [[first Chern class]] of  the gauge bundle is 

\[
  \label{FirstChernClassByIntegration}
  \big\langle c_1(E),[B] \big\rangle
  \,=\,
  \big\langle 
    c_1\big(\operatorname{Ad}(E)\big),
    [B] 
  \big\rangle
  \,=\,
  -\frac{\mathrm{i}}{2\pi}
  \int_B \operatorname{tr}(F_A)
  \;\in\;
  \mathbb{Z}
  \,,
\]

## Application on the 2-sphere
 {#ApplicationToThe2Sphere}

The [[complex Hopf fibration]] is a [[circle principal bundle|principal $U(1)$-bundle]] over [[2-sphere|$S^2$]], which encodes the [[charge quantization]] of the [[magnetic charge]] of a [[magnetic monopole]] in three dimensions ([[Dirac monopole]]) using:
$$
  \operatorname{Prin}_{\operatorname{U}(1)}(S^2)
  \;\cong\;
  \big[ S^2,\operatorname{BU}(1) \big]
  \;=\;
  \pi_2\big( \operatorname{BU}(1) \big)
  \;\cong\;
  \pi_1\big( \operatorname{U}(1) \big)
  \;\cong\;
  \pi_1 S^1
  \;\cong\;
  \mathbb{Z}
  \,.
$$
Given an $m\in\mathbb{Z}$, the corresponding [[principal bundle]] is given by [[pullback]] of the [[universal principal bundle]] $EU(1)\twoheadrightarrow BU(1)$ along the [[composition]] of the canonical inclusion $S^2\cong\mathbb{C}P^1\hookrightarrow\mathbb{C}P^\infty\cong BU(1)$ and the map $BU(1)\rightarrow BU(1)$ induced by $\mathrm{U}(1)\rightarrow \mathrm{U}(1),z\mapsto z^m$.

## Related concepts

* [[D=2 QCD]]
* [[D=4 Yang-Mills theory]]
* [[D=5 Yang-Mills theory]]

[[!redirects Two-dimensional Yang--Mills theory]]
[[!redirects Yang--Mills theory in two dimensions]]