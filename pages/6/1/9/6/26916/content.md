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

_D=4 [[Yang-Mills theory]]_ (D=4 YM theory) studies the [[Yang-Mills equations]] over a base [[manifold]] of [[dimension]] $D=4$. This special case allows to reduce the [[Yang-Mills equations]] of second order to the _(anti) self-dual Yang-Mills equations_ ((A)SDYM equations) of first order.

## Basics

Consider

* $G$ a [[Lie group]],

* $B$ an [[orientable]] [[Riemannian manifold|Riemannian]] [[4-manifold]],

* $E\twoheadrightarrow B$ a [[principal bundle|principal $G$-bundle]],

* $A\in\Omega_{\operatorname{Ad}}^1(E,\mathfrak{g})\cong\Omega^1(B,\operatorname{Ad}(E))$ a [[principal connection]],

* $F_A \coloneqq \mathrm{d}_A A=\mathrm{d}A+[A\wedge A]\in\Omega_{\operatorname{Ad}}^2(E,\mathfrak{g})\cong\Omega^2(B,\operatorname{Ad}(E))$ its [[curvature]]. 

[[Chern-Weil theory]] implies that the [[second Chern class]] of the gauge bundle is:

\[
  \label{SecondChernClassByIntegration}
  \big\langle c_2(E),[B] \big\rangle
  =
  \Big\langle 
    c_2\big(\operatorname{Ad}(E)\big),
    [B] 
  \Big\rangle
  =
  -\frac{1}{8\pi^2}
  \int_B \operatorname{tr}(F_A \wedge F_A)
  \;\in\;
  \mathbb{Z}
  \,.
\]

## Application on the 4-sphere

The [[quaternionic Hopf fibration]] is a [[principal SU(2)-bundle]] over $S^4$, which encodes the [[charge quantization]] of the magnetic charge of a [[magnetic monopole]] in five dimensions (Wu-Yang monopole) using:
$$
  \operatorname{Prin}_{\operatorname{Sp}(1)}(S^4)
  \;\cong\;
  \big[S^4,\operatorname{BSp}(1)\big]
  \;=\;
  \pi_4\operatorname{BSp}(1)
  \;\cong\;
  \pi_3\operatorname{Sp}(1)
  \;\cong\;
  \pi_3S^3
  \;\cong\;
  \mathbb{Z}
  \,.
$$
Given an $m\in\mathbb{Z}$, the corresponding [[principal bundle]] is given by [[pullback]] of the [[universal principal bundle]] $ESp(1)\twoheadrightarrow BSp(1)$ along the [[composition]] of the canonical inclusion $S^4\cong\mathbb{H}P^1\hookrightarrow\mathbb{H}P^\infty\cong BSp(1)$ and the map $BSp(1)\rightarrow BSp(1)$ induced by $Sp(1)\rightarrow Sp(1),q\mapsto q^m$.

## Related concepts

* [[D=2 Yang-Mills theory]]

* [[D=3 Yang-Mills theory]]

* [[D=5 Yang-Mills theory]]

* [[D=4 N=1 super Yang-Mills theory]]

* [[D=4 N=2 super Yang-Mills theory]]

* [[D=4 N=4 super Yang-Mills theory]]

* [[topologically twisted D=4 super Yang-Mills theory]]

[[!redirects Four-dimensional Yang--Mills theory]]
[[!redirects Yang--Mills theory in four dimesions]]

[[!redirects anti self-dual Yang-Mills equation]]
[[!redirects anti self-dual Yang-Mills equations]]
[[!redirects ASDYM equation]]
[[!redirects ASDYM equations]]