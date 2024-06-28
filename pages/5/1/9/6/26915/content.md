
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

## References

The original reference:

* [[Alexander A. Migdal]], *Recursion equations in gauge field theories*, Zh. Eksp. Teor. Fiz. **69** (1975) 810–822 (Sov. Phys. JETP 42, 413–418) &lbrack;[pdf](http://jetp.ras.ru/cgi-bin/dn/e_042_03_0413.pdf), [[Migdal-RecursionInGauge.pdf:file]] [spire:100330](https://inspirehep.net/literature/100330)&rbrack;

Further developments:

* Ninoslav E. Bralić, _Exact computation of loop averages in two-dimensional Yang-Mills theory_, Phys. Rev. D 22:12 (1980), 3090–3103.  [doi:10.1103/PhysRevD.22.3090](https://doi.org/10.1103/PhysRevD.22.3090).

* V. A. Kazakov, I. K. Kostov, _Non-linear strings in two-dimensional U(∞) gauge theory_, Nuclear Physics B 176:1 (1980), 199–215.  [doi][1]

[1]: https://doi.org/10.1016/0550-3213(80)90072-3

* Leonard Gross, Christopher King, Ambar Sengupta, _Two dimensional Yang-Mills theory via stochastic differential equations_, Annals of Physics 194:1 (1989), 65–112.  [doi][1]

[1]: https://doi.org/10.1016/0003-4916(89)90032-8

* B. Ye. Rusakov, _LOOP AVERAGES AND PARTITION FUNCTIONS IN U(N) GAUGE THEORY ON TWO-DIMENSIONAL MANIFOLDS_, Modern Physics Letters A 5:9 (1990), 693–703.  [doi](https://doi.org/10.1142/S0217732390000780).

* Dana S. Fine, _Quantum Yang-Mills on the two-sphere_, Communications in Mathematical Physics 134 (1990), 273–292.  [doi](https://doi.org/10.1007/BF02097703).

* Dana S. Fine, _Quantum Yang-Mills on a Riemann surface_, Communications in Mathematical Physics 140 (1991), 321–338.  [doi](https://doi.org/10.1007/BF02099502).

* Ambar Sengupta, _The Yang-Mills measure for $S^2$_, Journal of Functional Analysis **108**  2 (1992) 231–273 &lbrack;<a href="https://doi.org/10.1016/0022-1236(92)90025-E">doi;10.1016/0022-1236(92)90025-E</a>&rbrack;

* Ambar Sengupta, _Quantum Gauge Theory on Compact Surfaces_, Annals of Physics 221:1 (1993), 17–52.  [doi](https://doi.org/10.1006/aphy.1993.1002)

* [[Matthias Blau]], [[George Thompson]], *Quantum Yang-Mills theory on arbitrary surfaces*, International Journal of Modern Physics A **7** 16 (1992) 3781–3806 &lbrack;[doi:10.1142/S0217751X9200168X](https://doi.org/10.1142/S0217751X9200168X)&rbrack;

* [[Edward Witten]], _Two-dimensional gauge theories revisited_, Journal of Geometry and Physics 9:4 (1992), 303–368.  [arXiv:hep-th/9204083](https://arxiv.org/abs/hep-th/9204083). [doi:10.1016/0393-0440(92)90034-X](https://doi.org/10.1016/0393-0440(92)90034-X).

[[!redirects Two-dimensional Yang--Mills theory]]
[[!redirects Yang--Mills theory in two dimensions]]