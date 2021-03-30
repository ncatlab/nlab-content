
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum field theory
+-- {: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

Originally, the _Ginzburg--Landau model_ is a [[model (physics)|model]] in [[solid state physics]] for [[superconductivity]].

Roughly this type of model has then been used as models for 2d [[quantum field theory]] in [[string theory]].
There, a _Landau--Ginzburg model_ (LG-model) is a 2-[[dimension|dimensional]] [[supersymmetry|supersymmetric]] [[sigma model]] [[QFT]] characterized by the fact that its [[Lagrangian]] contains a [[potential]] term: given a [[complex manifold|complex]] [[Riemannian manifold|Riemannian]] [[target space]] $(X,g)$, the [[action functional]] of the LG-model is schematically of the form

$$
  S_{LB} : (\phi : \Sigma \to X) \mapsto
  \int_\Sigma \left( \vert \nabla \Phi \vert^2 + \vert (\nabla W)(\phi) \vert^2 
  + fermionic\;terms \right) d \mu
  \,,
$$

where $\Sigma$ is the 2-[[dimension]]al [[worldsheet]] and $W : X \to \mathbb{C}$ -- called the model's _superpotential_ -- is a [[holomorphic function]]. (Usually $X$ is actually taken to be a [[Cartesian space]] and all the nontrivial structure is in $W$.)

Landau--Ginzburg models have gained importance as constituting one type of QFTs that are related under [[homological mirror symmetry]]:

If the [[target space]] $X$ is a [[Fano variety]], the usual [[B-model]] does not quite exist on it, since the corresponding supersymmetric [[string]] [[sigma model]] is not conformally invariant as a quantum theory, and the axial $U(1)$ [[R-current]] used to define the B-twist is [[quantum anomaly|anomalous]]. Still, there exists an analogous [[derived category]] of B-branes. A Landau--Ginzburg model is something that provides the dual A-branes to this under [[homological mirror symmetry]]. Conversely, Landau--Ginzburg B-branes are homological mirror duals to the [[A-model]] on a Fano variety.
(...)

As suggested by [[Maxim Kontsevich]] (see [Kapustin-Li, section 7](#KapustinLi)), the B-branes in the LG-model (at least in a certain class of cases) are not given by [[chain complexes]] of [[coherent sheaves]] as in the [[B-model]], but by _[[twisted complexes]]_ : for these the square of the [[differential]] is in general non-vanishing and identified with the _superpotential_ of the LG-model. 


(...)

## Properties

### The $\infty$-categories of branes


A [[brane]] for a LG model is given by a [[matrix factorization]] of its superpotential.


(...) [[curved dg-algebra]]

(...) [CaldararuTu](#CaldararuTu)


## Related concepts

* [[2d TQFT]], [[TCFT]]

* [[holographic superconductor]]

## References

### In superconductivity

Discussion as a model for [[superconductors]]:

The original article:

* [[В. Л. Гинзбург]], [[Л. Д. Ландау]], _К теории сверхпроводимости_, ЖЭТФ 20 (1950), 1064.

English translation:

* [[Vitaly Ginzburg]], [[Lev Landau]], _On the Theory of Superconductivity_,  In: _On Superconductivity and Superfluidity_ Springer (2009) ([doi:1007/978-3-540-68008-6_4](https://doi.org/10.1007/978-3-540-68008-6_4))


Review:

* {#Chapman00} S. J. Chapman, Section 2 of: _A Hierarchy of Models for Type-II Superconductors_, IAM Review Vol. 42, No. 4 (2000), pp. 555-598 ([jstor:2653134](https://www.jstor.org/stable/2653134))

* {#Timm20} Carsten Timm, Section 6 of: _Theory of Superconductivity_, 2020 ([pdf](https://tu-dresden.de/mn/physik/itp/cmt/ressourcen/dateien/skripte/Skript_Supra.pdf?lang=en))

### In string theory

Discussion as a [[supersymmetry|supersymmetric]] [[sigma model]] in [[string theory]] [[KK-compactification|on]] [[Calabi-Yau manifolds]]:

* {#VafaWarner89} [[Cumrun Vafa]], [[Nicholas Warner]], _Catastrophes and the Classification of Conformal Theories_, Phys.Lett. B218 (1989) 51 ([doi:10.1016/0370-2693(89)90473-5](https://doi.org/10.1016/0370-2693%2889%2990473-5))

* [[Brian Greene]], [[Cumrun Vafa]], _Calabi--Yau Manifolds and Renormalization Group Flows_, Nucl.Phys. B324 (1989) 371 (<a href="https://doi.org/10.1016/0550-3213(89)90471-9">doi:10.1016/0550-3213(89)90471-9</a>)

* [[Edward Witten]], _Phases of $N=2$ Theories In Two Dimensions_, Nucl.Phys.B 403:159--222, 1993 ([arXiv:hep-th/9301042](http://arxiv.org/abs/hep-th/9301042))

Lecture notes:

* [[Edward Witten]], _Dynamical aspects of QFT_, Lecture 15: _The Landau--Ginzburg description of $N=2$ minimal models; Quantum cohomology and K&#228;hler manifolds_,  in Part IV of _[[Quantum Fields and Strings]]_.



#### Branes

The [[branes]] of the LG-model are discussed for instance in

* [[Anton Kapustin]], Yi Li, _D-Branes in Landau--Ginzburg models and algebraic geometry_, [arXiv:hep-th/0210296](http://arxiv.org/abs/hep-th/0210296)
 {#KapustinLi}

The [[derived category]] of [[D-brane]]s in type B LG-models is discussed in

* {#Orlov} [[Dmitri Orlov]], _Triangulated categories of singularities and D-branes in Landau--Ginzburg models_, Proc. Steklov Inst. Math. 2004, no. 3 (246), 227--248 ([arXiv:math/0302304](http://arxiv.org/abs/math/0302304))

* [[Dmitri Orlov]]_Derived categories of coherent sheaves and triangulated categories of singularities_, Algebra, arithmetic, and geometry: in honor of Yu. I. Manin. Vol. II, 503&#8211;531, Progr. Math., 270, Birkh&#228;user Boston,
Inc., Boston, MA, 2009 ([arXiv:math.ag/0503632](http://arxiv.org/abs/math.ag/0503632))
 

* Andrei Caldararu, Junwu Tu, _Curved $A_\infty$-algebras and Landau--Ginzburg models_ ([pdf](http://www.math.wisc.edu/~andreic/publications/AinfinityLG.pdf))
 {#CaldararuTu}

#### Defects

General defects of B-twisted affine LG models were first discussed in

* [[Ilka Brunner]], [[Daniel Roggenkamp]], _B-type defects in Landau--Ginzburg models_, JHEP 0708 (2007) 093, ([arXiv:0707.0922](http://arxiv.org/abs/0707.0922))

The graded pivotal bicategory of B-twisted affine LG models is studied in detail in 

* Nils Carqueville, [[Daniel Murfet]], _Adjunctions and defects in Landau--Ginzburg models_, Advances in Mathematics, Volume 289 (2016), 480--566, ([arXiv:1208.1481](http://arxiv.org/abs/1208.1481))

Orbifolds of defects are studied in

* [[Ilka Brunner]], [[Daniel Roggenkamp]], _Defects and Bulk Perturbations of Boundary Landau--Ginzburg Orbifolds_, JHEP 0804 (2008) 001, ([arXiv:0712.0188](http://arxiv.org/abs/0712.0188))

* Nils Carqueville, Ingo Runkel, _Orbifold completion of defect bicategories_, ([arXiv:1210.6363](http://arxiv.org/abs/1210.6363))

* [[Ilka Brunner]], Nils Carqueville, Daniel Plencner, _Orbifolds and topological defects_, Comm. Math. Phys. 332 (2014), 669--712, ([arXiv:1307.3141](http://arxiv.org/abs/1307.3141))

* [[Ilka Brunner]], Nils Carqueville, Daniel Plencner, _Discrete torsion defects_, Comm. Math. Phys. 337 (2015), 429--453, ([arXiv:1404.7497](http://arxiv.org/abs/1404.7497))

A relation to [[linear logic]] and the [[geometry of interaction]] is in 

* {#Murfet14} [[Daniel Murfet]], _Computing with cut systems_ ([arXiv:1402.4541](http://arxiv.org/abs/1402.4541))

#### TCFT formulation

Discussions of topological Landau--Ginzburg [[B-models]] explicitly as open [[TCFT]]s (aka open topological string theories) are in

* Nils Carqueville, _Matrix factorisations and open topological string theory_, JHEP 07 (2009) 005, ([arXiv:0904.0862](http://arxiv.org/abs/0904.0862))

* [[Ed Segal]], _The closed state space of affine Landau--Ginzburg B-models_ ([arXiv:0904.1339](http://arxiv.org/abs/0904.1339))

* Nils Carqueville, Michael Kay, _Bulk deformations of open topological string theory_, Comm. Math. Phys. 315, Number 3 (2012), 739--769, ([arXiv:1104.5438](http://arxiv.org/abs/1104.5438))



[[!include elliptic genera as partition functions -- references]]




[[!redirects LG model]]
[[!redirects LG models]]
[[!redirects LG-model]]
[[!redirects LG-models]]

[[!redirects Landau Ginzburg model]]
[[!redirects Landau Ginzburg models]]
[[!redirects Landau-Ginzburg model]]
[[!redirects Landau-Ginzburg models]]
[[!redirects Landau–Ginzburg model]]
[[!redirects Landau–Ginzburg models]]
[[!redirects Landau--Ginzburg model]]
[[!redirects Landau--Ginzburg models]]
