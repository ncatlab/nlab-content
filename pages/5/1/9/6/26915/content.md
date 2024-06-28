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

Let $G$ be a [[Lie group]] and $E\twoheadrightarrow B$ be a [[principal bundle|principal $G$-bundle]] with $B$ an [[orientable]] [[Riemannian manifold|Riemannian]] [[2-manifold]]. Let $A\in\Omega_{\operatorname{Ad}}^1(E,\mathfrak{g})\cong\Omega^1(B,\operatorname{Ad}(E))$ be a [[connection]] and $F_A:=\mathrm{d}_AA=\mathrm{d}A+[A\wedge A]\in\Omega_{\operatorname{Ad}}^2(E,\mathfrak{g})\cong\Omega^2(B,\operatorname{Ad}(E))$ be its [[curvature]]. [[Chern-Weil theory]] implies:
$$
\langle c_1(E),[B]\rangle
=\langle c_1(\operatorname{Ad}(E)),[B]\rangle
=-\frac{i}{2\pi}\int_B\operatorname{tr}(F_A)
\in\mathbb{Z}.
$$

## Application on the 2-sphere

The [[complex Hopf fibration]] is a [[principal bundle|principal $U(1)$-bundle]] over $S^2$, which describes the [[quantization]] of the magnetic charge of a [[magnetic monopole]] in three dimensions (Dirac monopole) using:
$$
\operatorname{Prin}_{\operatorname{U}(1)}(S^2)
\cong[S^2,\operatorname{BU}(1)]
=\pi_2\operatorname{BU}(1)
\cong\pi_1\operatorname{U}(1)
\cong\pi_1S^1
\cong\mathbb{Z}.
$$
Given an $m\in\mathbb{Z}$, the corresponding [[principal bundle]] is given by [[pullback]] of the [[universal principal bundle]] $EU(1)\twoheadrightarrow BU(1)$ along the [[composition]] of the canonical inclusion $S^2\cong\mathbb{C}P^1\hookrightarrow\mathbb{C}P^\infty\cong BU(1)$ and the map $BU(1)\rightarrow BU(1)$ induced by $U(1)\rightarrow U(1),z\mapsto z^m$.

## Related concepts

* [[D=2 QCD]]

[[!redirects Two-dimensional Yang--Mills theory]]
[[!redirects Yang--Mills theory in two dimensions]]