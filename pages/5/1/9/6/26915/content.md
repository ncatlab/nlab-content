
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

*D=2 [[Yang-Mills theory]]* (D=2 YM theory) studies the [[Yang-Mills equations]] over a base [[manifold]] with [[dimension]] $D=2$. This special case allows the definition of the _Yang-Mills measure_.

As with ordinary 4d [[Yang-Mills theory]] being the basis of [[quantum chromodynamics]] (QCD), so coupling suitable [[fermion]] [[field (physics)|physics]] ("[[quarks]]") to $D=2$ Yang-Mills theory leads to the "'t Hooft model" also called *[[D=2 QCD]]*.


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

> See also the references at *[[D=2 QCD]]*.

The original reference:

* [[Alexander A. Migdal]], *Recursion equations in gauge field theories*, Zh. Eksp. Teor. Fiz. **69** (1975) 810–822 (Sov. Phys. JETP 42, 413–418) &lbrack;[pdf](http://jetp.ras.ru/cgi-bin/dn/e_042_03_0413.pdf), [[Migdal-RecursionInGauge.pdf:file]] [spire:100330](https://inspirehep.net/literature/100330)&rbrack;

Further developments:

* Ninoslav E. Bralić, _Exact computation of loop averages in two-dimensional Yang-Mills theory_, Phys. Rev. D **22** 12 (1980) 3090–3103 &lbrack;[doi:10.1103/PhysRevD.22.3090](https://doi.org/10.1103/PhysRevD.22.3090)&rbrack;

* V. A. Kazakov, I. K. Kostov, _Non-linear strings in two-dimensional U(∞) gauge theory_, Nuclear Physics B **176** 1 (1980) 199–215 &lbrack;<a href="https://doi.org/10.1016/0550-3213(80)90072-3">doi:10.1016/0550-3213(80)90072-3</a>&rbrack;

* Leonard Gross, Christopher King, Ambar Sengupta, _Two dimensional Yang-Mills theory via stochastic differential equations_, Annals of Physics 194:1 (1989) 65–112 &lbrack;<a href="https://doi.org/10.1016/0003-4916(89)90032-8">doi:10.1016/0003-4916(89)90032-8</a>&rbrack;

* B. Ye. Rusakov, _Loop averages and partition functions in $U(N)$ gauge theory on two-dimensional manifolds_, Modern Physics Letters A **5** 9 (1990) 693–703 &lbrack;[doi:10.1142/S0217732390000780](https://doi.org/10.1142/S0217732390000780)&rbrack;

* Dana S. Fine, _Quantum Yang-Mills on the two-sphere_, Communications in Mathematical Physics **134** (1990) 273–292  &lbrack;[doi:10.1007/BF02097703](https://doi.org/10.1007/BF02097703)&rbrack;

* Dana S. Fine, _Quantum Yang-Mills on a Riemann surface_, Communications in Mathematical Physics **140** (1991) 321–338.  &lbrack;[doi:10.1007/BF02099502](https://doi.org/10.1007/BF02099502)&rbrack;

* Ambar Sengupta, _The Yang-Mills measure for $S^2$_, Journal of Functional Analysis **108**  2 (1992) 231–273 &lbrack;<a href="https://doi.org/10.1016/0022-1236(92)90025-E">doi;10.1016/0022-1236(92)90025-E</a>&rbrack;

* Ambar Sengupta, _Quantum Gauge Theory on Compact Surfaces_, Annals of Physics **221** 1 (1993) 17–52 &lbrack;[doi:10.1006/aphy.1993.1002](https://doi.org/10.1006/aphy.1993.1002)&rbrack;

* [[Matthias Blau]], [[George Thompson]], *Quantum Yang-Mills theory on arbitrary surfaces*, International Journal of Modern Physics A **7** 16 (1992) 3781–3806 &lbrack;[doi:10.1142/S0217751X9200168X](https://doi.org/10.1142/S0217751X9200168X)&rbrack;

* [[Edward Witten]]. On quantum gauge theories in two dimensions, *Commun.Math. Phys*. **141** (1991) 153–209 &lbrack;[doi:10.1007/BF02100009](https://doi.org/10.1007/BF02100009)&rbrack;

* [[Edward Witten]], _Two-dimensional gauge theories revisited_, Journal of Geometry and Physics **9** 4 (1992) 303–368 &lbrack;[arXiv:hep-th/9204083](https://arxiv.org/abs/hep-th/9204083), [doi:10.1016/0393-0440(92)90034-X](https://doi.org/10.1016/0393-0440(92)90034-X)&rbrack;

* Stefan Cordes, [[Gregory Moore]], [[Sanjaye Ramgoolam]]. *Lectures on 2D Yang-Mills Theory, Equivariant Cohomology and Topological Field Theories* (1994) &lbrack;[hep-th/9411210](https://arxiv.org/abs/hep-th/9411210)&rbrack;

On [[D=2 QCD]] 

* {#tHooft74} [[Gerard ’t Hooft]], *A Two-Dimensional Model For Mesons*, Nucl. Phys. B **75** (1974) 461-470 &lbrack;<a href="https://doi.org/10.1016/0550-3213(74)90088-1">doi:10.1016/0550-3213(74)90088-1</a>&rbrack;

* [[Michael Douglas]], Keke Li, [[Matthias Staudacher]], *Generalized Two-Dimensional QCD*, Nucl.Phys. B **420** (1994) 118-140 &lbrack;[arXiv:hep-th/9401062](https://arxiv.org/abs/hep-th/9401062), <a href="https://doi.org/10.1016/0550-3213(94)90377-8">doi:10.1016/0550-3213(94)90377-8</a>&rbrack;

* [[Emanuel Katz]], Gustavo Marques Tavares, Yiming Xu, _A solution of 2D QCD at Finite $N$ using a conformal basis_ &lbrack;[arxiv:1405.6727](https://arxiv.org/abs/1405.6727)&rbrack;


and its relation to [[string theory]], the "Gross-Taylor model":

* [[David Gross]]. *Two Dimensional QCD as a String Theory*, Nuclear Physics B **400** 1–3 (1993) 161-180 &lbrack;[hep-th/9212149](https://arxiv.org/abs/hep-th/9212149), <a href="https://doi.org/10.1016/0550-3213(93)90402-B">doi:10.1016/0550-3213(93)90402-B</a>&rbrack;

* [[David Gross]], [[Washington Taylor]], *Two Dimensional QCD is a String Theory*, Nucl. Phys. B **400** (1993) 181-210 &lbrack;[arxiv:hep-th/9301068](https://arxiv.org/abs/hep-th/9301068), <a href="https://doi.org/10.1016/0550-3213(93)90403-C">doi:10.1016/0550-3213(93)90403-C</a>&rbrack;

* [[David Gross]], [[Washington Taylor]], *Twists and Wilson loops in the string theory of two-dimensional QCD*, Nucl. Phys. B **403** (1993) 395-452 &lbrack;[hep-th/9303046](https://arxiv.org/abs/hep-th/9303046), <a href="https://doi.org/10.1016/0550-3213(93)90042-N">doi:10.1016/0550-3213(93)90042-N</a>&rbrack;

and the [[Petr Hořava|Hořava model]]:

* [[Petr Hořava]], *Topological Strings and QCD in Two Dimensions* (1993) &lbrack;[hep-th/9311156](https://arxiv.org/abs/hep-th/9311156), [spire](https://inspirehep.net/literature/360453)&rbrack;

* [[Petr Hořava]]. *Topological Rigid String Theory and Two Dimensional QCD*, Nucl.Phys. B **463** (1996) 238-286 &lbrack;[hep-th/9507060](https://arxiv.org/abs/hep-th/9507060), <a href="https://doi.org/10.1016/0550-3213(96)00036-3">doi:10.1016/0550-3213(96)00036-3</a> &rbrack;

In the context of [[generalized global symmetry|generalized global symmetries]]:

* Mendel Nguyen, Yuya Tanizaki, Mithat Ünsal. *Non-invertible 1-form symmetry and Casimir scaling in 2d Yang-Mills theory* (2021) &lbrack;[arXiv:2104.01824](https://arxiv.org/abs/2104.01824)&rbrack;

* [[Tony Pantev]], [[Eric Sharpe]]. *Decomposition and the Gross-Taylor string theory* (2023) &lbrack;[arXiv:2307.08729](https://arxiv.org/abs/2307.08729)&rbrack;

In the more general context of volume-dependent theories:

* Richard Wedeen. *Volume-Dependent Field Theories* (2024). &lbrack;[arXiv:2402.06691](https://arxiv.org/abs/2402.06691)&rbrack;

Discussion of [[lattice gauge theory|lattice]] 2d Yang-Mills theory via [[derived algebraic geometry]] and [[factorization algebra|prefactorization algebras]]:

* [[Marco Benini]], Tomás Fernández, [[Alexander Schenkel]]: *Derived algebraic geometry of 2d lattice Yang-Mills theory* &lbrack;[arXiv:2409.06873](https://arxiv.org/abs/2409.06873)&rbrack;

[[!redirects 2d Yang-Mills theory]]
[[!redirects 2d Yang-Mills theories]]

[[!redirects Two-dimensional Yang--Mills theory]]
[[!redirects Yang--Mills theory in two dimensions]]