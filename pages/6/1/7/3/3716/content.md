
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A **Poisson Lie group** (often written Poisson-Lie group) or Lie Poisson group $G$ is a [[ Lie group]] and a [[Poisson manifolds]], the two structures being compatible such that the group product is a smooth map of Poisson manifolds where $G\times G$ has the product Poisson structure. 

**Warning**: the inverse map is NOT a Poisson map unless G has the trivial Poisson structure, in fact it is an anti-Poisson map.


[[deformation quantization|Deformation quantizations]] of Poisson Lie groups are [[Hopf algebras]]. The usual [[quantum groups]] have smaller number of quantum subgroups (i.e. Hopf quotient algebras) than the corresponding Lie group has, namely only only those whose classical limits are not only Lie subgroups but Poisson Lie subgroups. 

## Properties

### Relation to quantum groups

One can regard Poisson groups as the [[classical limit]] of [[quantum groups]]: a theorem by Drinfeld established a [[bijection]] between connected, simply connected Poisson Lie groups and [[Lie bialgebras]]. 

## Examples

### Additive Poisson Lie groups
 {#AdditivePoissonLieGroups}

A [[Lie-Poisson structure]] is an additive Poisson Lie group (e.g. [Kosmann-Schwarzbach 04, p. 46](#KosmannSchwarzbach04)).

If $H$ is any (finite dimensional) Lie group then the dual $(T_e H)^*$ of its [[tangent Lie algebra]] has a canonical bracket introduced by Kirillov which makes it into a Poisson Lie group. To this aim one identifies $(T_e H)^*$ with its own tangent space $T_u (T_e H)^*$ and interprets the differential $df$ of a function $f:(T_e H)^*\to \mathbb{R}$ as a function $(T_e H)^*\to ((T_e H)^*)^*\cong T_e H$ where the finite dimensionality is used. Then Kirillov defines

$$
\lbrace f_1, f_2\rbrace (u) = \langle [(df_1)_u, (df_2)_u, u\rangle
$$

Given two Lie groups $H,K$, the Lie algebra homomorphisms $T_e H \to T_e K$ are in 1-1 correspondence with the Poisson Lie maps $(T_e K)^* \to (T_e H)^*$. 


## Related concepts

* [[dressing action]]
* [[Poisson Lie 2-group]]

* _Unrelated_ is the concept of the Lie group that [[Lie integration|integrates]] the [[Lie algebra]] inside a [[Poisson algebra]]. This is instead called a _[[quantomorphism group]]_.

## References

* V. Chari, A. Pressley, _A guide to quantum groups_, Camb. Univ. Press 1994
* [[S. Majid]], _Foundations of quantum group theory_, Cambridge University Press 1995, 2000. 
* Gloria Mar&#237; Beffa, _A transverse structure for the Lie-Poisson bracket on the dual of the Virasoro algebra_,  Pacific J. Math. __163__ (1994),  no. 1, 43--72, [euclid](http://projecteuclid.org/getRecord?id=euclid.pjm/1102622628)
* M. A. Semenov-Tian-Shansky, _&#1043;&#1088;&#1091;&#1087;&#1087;&#1099; &#1055;&#1091;&#1072;&#1089;&#1089;&#1086;&#1085;&#1072;&#8211;&#1051;&#1080;. &#1050;&#1074;&#1072;&#1085;&#1090;&#1086;&#1074;&#1099;&#1081; &#1087;&#1088;&#1080;&#1085;&#1094;&#1080;&#1087; &#1076;&#1074;&#1086;&#1081;&#1089;&#1090;&#1074;&#1077;&#1085;&#1085;&#1086;&#1089;&#1090;&#1080; &#1080; &#1089;&#1082;&#1088;&#1091;&#1095;&#1077;&#1085;&#1085;&#1099;&#1081; &#1082;&#1074;&#1072;&#1085;&#1090;&#1086;&#1074;&#1099;&#1081; &#1076;&#1091;&#1073;&#1083;&#1100;_, Teoret. Mat. Fiz., 1992, 93:2,  302&#8211;329 (in Russian) [pdf](http://83.149.209.141/php/getFT.phtml?jrnid=tmf&paperid=1530&volume=93&year=1992&issue=2&fpage=302&what=fullt&option_lang=eng); in English: _Poisson&#8211;Lie groups. The quantum duality principle and the twisted quantum double_, Theoret. and Math. Physics 1992, 93:2, 1292&#8211;1307 [doi](http://dx.doi.org/10.1007/BF01083527); _Poisson groups and dressing transformations_, Zap. Nauchn. Sem. LOMI, 150 (1986),  119–142 [mathnet.ru](http://mi.mathnet.ru/znsl4975); _Poisson Lie groups, quantum duality principle, and the quantum double_, in: Math. aspects of conformal and topological field theories and quantum groups (South Hadley, MA, 1992),  219--248, Contemp. Math. __175__, AMS 1994.
* M. A. Semenov-Tian-Shansky, _Classical $r$-matrices, Lax equations, Poisson Lie groups and dressing transformations_, in:  Field theory, quantum gravity and strings, II (Meudon/Paris, 1985/1986), 174--214, Lec. Notes in Phys. __280__, Springer 1987, [MR89g:58098](http://www.ams.org/mathscinet-getitem?mr=89g:58098)
* A. P. Fordy, A. G. Reyman, M. A. Semenov-Tian-Shansky, _Classical $r$-matrices and compatible Poisson brackets for coupled KdV systems_,  Lett. Math. Phys. __17__ (1989), no. 1, 25--29, [doi](http://dx.doi.org/10.1007/BF00420010), [MR90e:58061](http://www.ams.org/mathscinet-getitem?mr=90e:58061)
* A. Yu. Alekseev, A. Z. Malkin, _Symplectic structures associated to Lie-Poisson groups_,  Comm. Math. Phys. __162__  (1994),  no. 1, 147--173.
* T. Tao's blog: [The Euler-Arnold equation](http://terrytao.wordpress.com/2010/06/07/the-euler-arnold-equation) 
* [[Peter Olver]], _Applications of Lie groups to differential equations_, Springer
* A. Cannas da Silva, [[Alan Weinstein]], _Geometric models for noncommutative algebras_, Berkeley Math. Lec. Notes Series, AMS 1999, [pdf](http://math.berkeley.edu/%7Ealanw/Models.pdf)

* [[Yvette Kosmann-Schwarzbach]], _Groupes de Lie-Poisson quasitriangulaires_, in:  G&#233;om&#233;trie symplectique et m&#233;canique (La Grande Motte, 1988),  161--177, Springer LNM __1416__, 1990.

* {#KosmannSchwarzbach04} [[Yvette Kosmann-Schwarzbach]], _Lie bialgebras, Poisson Lie groups and dressing transformations_, in _Integrability of Nonlinear Systems_, Second edition, Lecture Notes in Physics 638, Springer-Verlag, 2004, pp. 107-173. ([pdf](http://www.math.polytechnique.fr/cmat/kosmann/lnp2.pdf))

* A. G. Reyman, _Poisson structures related to quantum groups_, in: Quantum groups and their applications in physics (Varenna, 1994), 407--443,
Proc. Internat. School Phys. Enrico Fermi, 127, IOS, Amsterdam, 1996, [MR97j:58052](http://www.ams.org/mathscinet-getitem?mr=97j:58052)
* Nicola Ciccoli, _Quantization of co-isotropic subgroups_, Lett. Math. Phys. __42__:2 (1997) 123--138, [doi](http://www.ams.org/leavingmsn?url=http://dx.doi.org/10.1023/A:1007352218739), [MR98k:58252](http://www.ams.org/mathscinet-getitem?mr=98k:58252)
* Renaud Brahami, _Cluster X-varieties for dual Poisson-Lie groups I, II_, [arxiv/1005.5289](http://arxiv.org/abs/1005.5289), [arxiv/1006.4583](http://arxiv.org/abs/1006.4583)

* L&#225;szl&#243; Feh&#233;r, [[Ctirad Klimčík]], _Poisson-Lie generalization of the Kazhdan-Kostant-Sternberg reduction_,  Lett. Math. Phys. __87__ (2009), no. 1-2, 125--138, [doi](http://dx.doi.org/10.1007), [MR2010c:53122](http://www.ams.org/mathscinet-getitem?mr=2010c:53122))

* V. Fock, A. B. Goncharov, _Cluster X-varieties, amalgamation and Poisson-Lie groups_, [math.RT/0508408](https://arxiv.org/abs/math/0508408).

* Ivan Calvo, Fernando Falceto, David Garcia-Alvarez, _Topological [[Poisson sigma model]]s on Poisson-Lie groups_, JHEP 0310 (2003) 033, [arXiv](https://arxiv.org/abs/hep-th/0307178).

* Philip Boalch, _[[Stokes phenomenon|Stokes matrices]] and Poisson Lie groups_, Invent. math. 146, 479-506 (2001), [math.DG/0011062](https://arxiv.org/abs/math/0011062).

* [[Ctirad Klimčík]], [[Pavol Ševera]], _[[T-duality]] and the moment map_, IHES/P/96/70, [hep-th/9610198](http://arxiv.org/abs/hep-th/9610198); _Poisson-Lie T-duality: open strings and D-branes_, CERN-TH/95-339. Phys.Lett. B376 (1996) 82-89, [hep-th/9512124](http://arxiv.org/abs/hep-th/9512124)

* [[Anton Alekseev]], [[Ctirad Klimčík]], [[Arkady Tseytlin]], _Quantum Poisson-Lie T-duality and WZNW model_, Nucl. Phys. B458:430-444 (1996) [hep-th/9509123](http://arxiv.org/abs/hep-th/9509.3123)
* David Li-Bland, [[Pavol Ševera]], _On deformation quantization of Poisson-Lie groups and moduli spaces of flat connections_, [arXiv/1307.2047](http://arxiv.org/abs/1307.2047)


Generalization of [[Noether's theorem]] to Poisson-Lie group [[symmetries]], not necessarily acting by [[symplectomorphisms]], for which the [[conserved charges]] may be nonabelian:

* [[Florian Girelli]], Christopher Pollack, Aldo Riello: *Beyond Noether: A Covariant Study of Poisson-Lie Symmetries in Low Dimensional Field Theory* &lbrack;[arXiv:2505.14942](https://arxiv.org/abs/2505.14942)&rbrack;




[[!redirects Poisson-Lie group]]
[[!redirects Lie Poisson group]]
[[!redirects Lie-Poisson group]]

[[!redirects Poisson Lie groups]]
[[!redirects Poisson-Lie groups]]
[[!redirects Lie Poisson groups]]
[[!redirects Lie-Poisson groups]]

[[!redirects Poisson group]]
[[!redirects Poisson groups]]