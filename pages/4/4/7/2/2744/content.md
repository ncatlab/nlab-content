#Contents#
* automatic table of contents goes here
{:toc}

#Idea#


Multisymplec geometry is a generalization of [[symplectic geometry]] to cases where the symplectic 2-form is generalized to a higher degree [[differential form]].
It encodes aspects of [[n-symplectic manifold]]s. For the moment, see there for further details and references.

In as far as [[symplectic geometry]] encodes [[Hamiltonian mechanics]], multisymplectic geometry may be regarded as resulving the symplectic geometry of the [[Hamiltonian mechanics]] of [[classical field theory]]: the kinematics of an $n$-dimensional field theory may be encoded in an degree $1+n$ higher symplectic form. Roughly the idea is that undeer a suitable fiber integration this becomes an ordinary symplectic form on the ordinary phase space of the theory.

This is similar to, and in fact a special case of, how for instance a [[line bundle]] on a [[loop space]] with a 2-form [[Chern class]] may arise by [[trasgression]] from a [[bundle gerbe]] down on the original space, with a 3-form class.

By effectively undoing this implicit transgression in the ordinary [[Hamiltonian mechanic]]s of [[classical field theory]], multisymplectic geomtry provides a general framework for a geometric, covariant formulation of [[classical field theory]], where _covariant formulation_ means that spacelike and timelike directions on a given space-time be treated on equal footing. 

# Survey of developments in the field#

There is in this sense a covariant form of the [[Legendre transformation]] which associates to every field variable as many conjugated momenta -- the multimomenta -- as there are space-time dimensions. These, together with the field variables, those of $n$-dimensional space-time, and an extra variable, the energy variable, span the multiphase space [1]. For a recent exposition on the differential geometry of this construction, see [2]. Multiphase space, together with a closed, nondegenerate differential $(n+1)$-form, the multisymplectic form, is an example of a multisymplectic manifold [3]. 

Among the achievements of the multisymplectic approach is a geometric formulation of the relation of infinitesimal symmetries and covariantly conserved quantities ([[Noether's theorem]]), see [4] for a recent review, and [5,6] for a clarification of the improvement techniques ("Belinfante-Rosenfeld formula") of the energy-momentum tensor in classical field theory. 

Multisymplectic geometry also provides convenient sets of variational integrators for the numerical study of partial differential equations [7].

Since in multisymplectic geometry, the symplectic 2-form of classical [[Hamiltonian mechanics]] is replaced by a closed [[differential form]] of higher tensor degree, multivector fields and differential forms have their natural appearance. (See [8] for an interpretation of multivector fields as describing solutions to field equations infinitesimally.) Multivector fields form a [[graded Lie algebra]] with the [[Schouten bracket]] (see [9] for a review and unified viewpoint). Using the multisymplectic $(n+1)$-form, one can construct a new bracket for the differential forms, the Poisson forms [10], generalizing a well-known formula for the Poisson brackets related to a symplectic 2-form. 

A remarkable fact is that in order to establish a Jacobi identity, the multisymplectic form has to have a potential, a condition that is not seen in symplectic geometry. Further, the admissible differential forms, the Poisson forms, are subject to the rather strong restrictions on their dependence on the multimomentum variables [11]. In particular, $(n-1)$-forms in this context can be shown to arise exactly from the covariantly conserved currents of Noether symmetries [11], which allows their pairing with spacelike hypersurfaces to yield conserved charges in a geometric way.

Not much is known about the interpretation of Poisson forms of form degree between zero and n-1. However, as $(n-1)$-forms describe vector fields and hence collections of lines [2, 10], and as (certain) functions describe n-vector fields and hence collections of bundle sections [8], it seems natural to speculate that the intermediate forms may be useful for the [[brane]]s of [[string theory]].

The Hamiltonian, infinite dimensional formulation of [[classical field theory]] requires the choice of a spacelike hypersurface ("Cauchy surface") [12] which manifestly breaks the general covariance of the theory at hand. For $(n-1)$-forms, the above mentioned new bracket reduces to the Peierls-deWitt bracket after integration over the spacelike hypersurface [13]. With the choice of a hypersurface, a constraint analysis [14] _&#224; la_ Dirac [15,16] can be performed [17]. Again, the necessary breaking of general covariance raises the need for an alternative formulation of all this [18]; first attempts have been made to carry out a [[Marsden-Weinstein reduction]] [19] for multisymplectic manifolds with symmetries [20]. However, not very much is known about how to quantize a multisymplectic geometry, see [21] for an approach using a path integral.

This discussion so far concerns field theories of first order, i.e. where the Lagrangian depends on the fields and their first derivatives. Higher order theories can be reduced to first order ones for the price of introducing auxiliary fields. A direct treatment would involve higher order jet bundles [22]. A definition of the covariant Legendre transform and the multiphase space has been given for this case [3].

#References#

Much of the above survey and of the following list of references is reproduced from the web-page

* [[Cornelis Mertzlufft-Paufler]], [Multisymplectic geometry](http://www.mertzlufft-paufler.de/multisymplectic_geometry.html)

References mentioned above are

* [1] J. Kijowski, W. Szczyrba, _A Canonical Structure For Classical Field Theories_ . Commun. Math. Phys. 46 (1976) 183.

* [2] M. J. Gotay, J. Isenberg, J. E. Marsden: _Momentum maps and classical relativistic fields. I: Covariant field theory_ [arXiv:physics/9801019v2].

* [3] M. J. Gotay, _A multisymplectic framework for classical field theory and the calculus of variations. I: Covariant Hamiltonian formalism_ 
In M. Francaviglia (ed.), _Mechanics, analysis and geometry: 200 years after Lagrange_ Amsterdam etc.: North-Holland (1991), 203-235.

* [4] M. de Leon, D. Martin de Diego, A. Santamaria-Merino, _Symmetries in Classical Field Theory_ [arXiv:math-ph/0404013].

* [5] M. J. Gotay, J. E. Marsden: _Stress-energy-momentum tensors and the Belinfante-Rosenfeld formula_ Contemp. Math. vol. 132, AMS, Providence, 1992, 367-392.

* [6] M. Forger, H. R&#246;mer, _Currents and the energy-momentum tensor in classical field theory: a fresh look at an old problem_ Ann. Phys. (N.Y.) 309 (2004) 306-389. [arXiv:hep-th/0307199].

* [7] A. Lew, J. E. Marsden, M. Ortiz, M. West, _An overview of variational integrators_
In L. P. Franca (ed.), Finite Element Methods: 70's and Beyond. Barcelona (2003).

* [8] C. Paufler, H. R&#246;mer, _The Geometry of Hamiltonian n-vector fields in Multisymplectic Field Theory_ J. Geom. Phys. 44, No.1(2002), 52-69. [arXiv: math-ph/0102008].

* [9]Y. Kosmann-Schwarzbach: Derived brackets. Lett. Math. Phys. 69 (2004) 61-87 [arXiv:math.DG/0312524].

[10] M. Forger, C. Paufler, H. R&#246;mer: _The Poisson Bracket for Poisson Forms in Multisymplectic Field Theory_ Rev. Math. Phys. 15 (2003) 705 [arXiv:math-ph/0202043].

* [10] M. Forger, C. Paufler, H. R&#246;mer, _Hamiltonian Multivector Fields and Poisson Forms in Multisymplectic Field Theory_ [arXiv:math-ph/0407057].

* [11] M. J. Gotay, _A multisymplectic framework for classical field theory and the calculus of variations. II: Space + time decomposition_ Differ. Geom. Appl. 1(4) (1991), 375-390.

* [12] M. O. Salles, _Campos Hamiltonianos e Colchete de Poisson na Teoria Geom&#233;trica dos Campos_ , PhD thesis, IME-USP, June 2004.

* M. Forger, S. V. Romero, _Covariant Poisson Brackets in Geometric Field Theory_ Commun. Math. Phys. 256 (2005), 375-410. [arXiv:math-ph/0408008].

* [13] M. J. Gotay, J. M. Nester, _Generalized constraint algorithm and special presymplectic manifolds_
In G. E. Kaiser, J. E. Marsden, Geometric methods in mathematical physics, Proc. NSF-CBMS Conf., Lowell/Mass. 1979, Berlin: Springer-Verlag, Lect. Notes Math. 775 (1980) 78-80.

* [14] P. A. M. Dirac, _Lectures on Quantum Mechanic_ Belfer Graduate School of Science, Yeshiva University, N.Y., 1964.

[15] M. Henneaux, C. Teitelboim, _Quantization of Gauge systems_ Princeton University Press, 1992.

* [16] M. J. Gotay, J. Isenberg, J. E. Marsden, R. Montgomery, _Momentum Maps and Classical Relativistic Fields II: Canonical Analysis of Field Theories_ (2004) [arXiv:math-ph/0411032].

* [17] N. P. Landsman, _Against the Wheeler-DeWitt equation_ Class. Quan. Grav. 12 (1995) L119-L124. [arXiv:gr-qc/9510033].

* [18] J. E. Marsden, A. Weinstein _Reduction of symplectic manifolds with symmetry_ Rept. Math. Phys. 5 (1974) 121-130.

* [19] F. Munteanu, A. M. Rey, M. Salgado, _The G&#252;nther's formalism in classical field theory: momentum map and reduction_ J. Math. Phys. 45, No. 5 (2004) 1730-1750.

* [20] D. Bashkirov, G. Sardanashvily, _Covariant Hamiltonian Field Theory. Path Integral Quantization_
[arXiv:hep-th/0402057].

* [21]D. J. Saunders, _The Geometry of Jet Bundles_ Lond. Math. Soc. Lect. Notes Ser. 142, Cambr. Univ. Pr., Cambridge, 1989.

A [[higher category theory|higher categorial]] interpretation of 2-plectic geometry is given in

* [[John Baez]], [[Chris Rogers]], _Categorified Symplectic Geometry and the String Lie 2-Algebra_ ([arXiv](http://arxiv.org/abs/0901.4721))

This builds a bridge to the notion of [[n-symplectic manifold]]s.