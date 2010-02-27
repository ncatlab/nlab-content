<div class="rightHandSide toc">
[[!include physicscontents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea {#Idea}


+-- {: .standout}

Multisymplectic geometry is (or should be) to [[symplectic geometry]] as [extended quantum field theory](http://ncatlab.org/nlab/show/FQFT#Extended) is to non-extended [[quantum field theory]]:

in the multisymplectic **extended phase space** of an $n$-dimensional [[classical field theory|field theory]] a state is not just a point, but an $n$-dimensional subspace.

=--


**Multisymplectic geometry** is a generalization of [[symplectic geometry]] to cases where the symplectic 2-form is generalized to a higher degree [[differential form]].

In as far as [[symplectic geometry]] encodes [[Hamiltonian mechanics]], multisymplectic geometry may be regarded as resolving the symplectic geometry of the [[Hamiltonian mechanics]] of [[classical field theory]]: the kinematics of an $n$-dimensional field theory may be encoded in an degree $(n+1)$ symplectic form. 

In this application to physics, multisymplectic geometry is also known as the **covariant symplectic approach** to field theory (e.g. [section 2 here](http://arxiv.org/PS_cache/physics/pdf/9801/9801019v2.pdf#page=18)).


The idea is that under a suitable fiber integration multisymplectic geometry becomes ordinary symplectic form on the ordinary phase space of the theory, similar to, and in fact as a special case of, how for instance a [[line bundle]] on a [[loop space]] with a 2-form [[Chern class]] may arise by [[transgression]] from a [[bundle gerbe]] down on the original space, with a 3-form class.

By effectively undoing this implicit transgression in the ordinary [[Hamiltonian mechanics]] of [[classical field theory]], multisymplectic geomtry provides a general framework for a geometric, covariant formulation of [[classical field theory]], where _covariant formulation_ means that spacelike and timelike directions on a given space-time be treated on equal footing. 




## Extended phase spaces in covariant field theory {#extended phase space}

In this section we describe multisymplectic geometry in its application
as a description of [[classical field theory]].

Recall that that on ordinary [[phase space]] of a physical system is a [[symplectic manifold]] whose points correspond to the _states_ of the system. The **extended phase space** of an $n$-dimensional quantum field theory is a multisymplectic space whose points correspond to pairs consisting of

* a point in the field theorie's parameter space -- an "event";

* a state of the theory "at that event".

So **extended phase spaces _localizes_ the information about states** : a point in here encodes not just the entire state of the system, but remembers explcitly what that state is like over any point in parameter space.

### Covariant configuration bundle

Consider [[classical field theory]] over a **parameter space** $\Sigma$. From the point of view of [[FQFT]] $\Sigma$ will be one fixed [[cobordism]] on which we want to understand the (classical) field theory.

We assume that a **field configuration** on $\Sigma$ is a [[section]] 
$\phi : \Sigma \to E$ of some prescribed [[bundle]] $E \to \Sigma$. 

**Example.** For instance an $n$-dimensional [[sigma-model]] [[quantum field theory]] is one whose field configurations on $\Sigma$ are given by maps 

$$
  \phi : \Sigma \to X
$$ 

into some prescribed **target space** $X$. This is the case where $E = \Sigma \times X$ is a **trivial [[bundle]]**.

**Remark.** Beware of the standard source of confusion here when correlating this formalism with actual physics: the physical spacetime that we inhabit may be given either by $\Sigma$ or by $X$:

* in the description of the [[quantum mechanics]] of objects propagating _in_ our physical spacetime, subject to forces exerted by fixed background [[gauge field]]s (such as electrons propagating in our particle accelerator, subject to the electromagnetic field in the accelerator tube), physical spacetime is identifid with target space $X$, while $\Sigma$ is the **worldvolume** of the object that propagates through $X$. The _field configurations_ on $\Sigma$ are really the maps $\Sigma \to X$ that determine how the object sits in spacetime.

* in quantum mechanics of fields on spacetime, such as the quantized electromagnetic field in a laser, it is $\Sigma$ which represents physical spacetime, and $X$ is some abstract space, for instance a smooth version of the [[classifying space]] $\mathcal{B}U(1)$, so that a field configuration $\Sigma \to X$ encodes a [[line bundle]] [[connection on a bundle|with connection]] that encodes a configuration of the [[electromagnetic field]].


**Definition.** The **configuration space** of the system is the space of all field configurations, hence the space $\Gamma_\Sigma(E)$ of [[section]]s of the [[bundle]] $E$.

In the $\sigma$-model example this is some incarnation of the mapping space $[\Sigma,X]$.

**Remark.** Beware that in low dimensions one often distinguishes between the space of _configurations_ $\Sigma \to X$ and that of _trajectories_ or _histories_ $\Sigma \times \mathbb{R} \to X$. This comes from the case $\Sigma = *$ where for a particle propagating on $X$ the maps $[*,X] \simeq X$ are the possible configurations of the particle at a given parameter times, while maps $[* \times \mathbb{R}, X] = [\mathbb{R}, X]$ are the trajectories. But for the higher dimensional and [[FQFT|extended]] field theories under discussion here, this distinction becomes a bit obsolete and trajectories become just a special case of configurations.

**Definition.** In the **non-covariant** approach one would try to consider the a [[cotangent bundle]] of the configuration space $\Gamma(E)$ as _phase space_ . Contrary to that, in the **covariant approach** one considers the much smaller space $E$ instead. This is then called the **covariant configuration space** or **covariant configuration bundle**.


**Definition** Write $J^1 E \to \Sigma$ for the first order [[jet bundle]] of the configuration space bundle $E \to \Sigma$. Its fiber over $s \in \Sigma$ are equivalence classses of [[germ]]s of [[section]]s at $x$, where two germs are identified if their first derivatives coincide. 


### Covariant phase space


**Definition** The **covariant phase space** is the multisymplectic manifold 

* whose underlying manifold is the **dual jet bundle** 
  $(J^1 E)^* \to E$ -- the [[vector bundle]] 
  over covariant configuration space $E$ whose 
  fiber at $e \in E_s$ is the set of affine maps 

  $$
    J_e^1 E \to \Lambda_s^{n+1} \Sigma
    \,.
  $$


* equipped with the canonical $(n+2)$-form

  $$
    \omega = d \alpha
    \,,
  $$

  where $\alpha$ is the canonical $(n+1)$-form

Given $\pi : E \to \Sigma$, with $\mathrm{dim} \Sigma =n+1$, the dual jet bundle $(J^1 E)^*$ is isomorphic to a particular vector sub-bundle of the $n+1$-form bundle $\Lambda^{n+1}T^{*}E$. 
Given a point $y \in E$, a tangent vector $v \in T_{y} E$ 
is said to be **vertical** if $d \pi(v) = 0$.  
Define $\Lambda^{n+1}_{1}T^{*}E$ to be the subbundle of the $n+1$-form bundle $\Lambda^{n+1} T^{*} E$ whose fiber at $y \in E$ 
consists of all $\beta \in \Lambda^{n+1} T^{*}_{y} E$ such that
\[          \iota_{v_1}\iota_{v_2} \beta =0   \]
for all vertical vectors $v_1,v_2 \in T_{y}E$.
Sections of $\Lambda^{n+1}_{1}T^{*}E$ are called $\mathbf{n}$**-horizontal** $\mathbf{n+1}$**-forms**. 
      

**Example** For the [[sigma-model]] case with $E = X \times \Sigma$ and $\{q^i\}$ coordinates on $X$ and $\{\sigma^s\}$ coordinates on $\Sigma$, the canonical $(n+1)$-form is

$$
  \alpha = \sum_{i,s} p_i^s d q^i \wedge (\iota_{\partial_{\sigma^s}}) d \sigma^1 \wedge \cdots \wedge d \sigma^n
  +
  p d \sigma^1 \wedge \cdots \wedge d \sigma^n
$$


... blah-blah-blah...


### Examples

#### Bosonic particle propagating on a manifold

Ordinary point particle mechanics on $X$ describes trajectories $\mathbb{R} \to X$ in $X$, with parameter space $\Sigma = \mathbb{R}$ the real line, thought of as the abstract **worldline** of the particle.

* parameter space: $\Sigma = \mathbb{R}$, the **worldline**;

* target space: $X$, some [[manifold]] -- **spacetime**;

* configuration bundle: $(E \to \mathbb{E}) = (\mathbb{R}\times X \to \mathbb{R})$;

* jet bundle: $J^1 E = \mathbb{R} \times T X$ .

for $U \subset E = \mathbb{R} \times X$ a local patch with coordinate functions $\{t, q^i\}$, there are canonically induced coordinates on $J^1 E$ written $\{t,q^i, v^i\}$.

Here a collection of vaues $(q^i_0)$ is a **position** of the particle and $(v^i_0)$ is a **velocity** of the particle. Notice that in this covariant approach these are not positions and velocities "at a given time". Rather, a point in $J^1 E$ specified a parameter time and a corresponding position and velocity.

....


Let $U \to X$ be a local patch of $X$ with canonical coordinates $\{x^i\}$.

The canonical 2-form on the extended phase space in this case is traditionally locally written as

$$
  \omega|_U = d \alpha|_U = d( p_i \wedge d q^i + H \wedge d t )
  \,.
$$


... blah-blah-blah...




#### Electromagnetism

* parameter space: $\Sigma$ is spacetime;

A field configuration of the [[electromagnetic field]] is a [[line  bundle]] [[connection on a bundle|with connection]] on $\Sigma$. If we assume the corresponding bundle to be trivial, then this is just a [[differential form|1-form]] on $\Sigma$. So in this simplified case we can take

* configuration bundle: $T^* \Sigma$ is the [[cotangent bundle]] of $\Sigma$.


#### Bosonic string propagating on a manifold

* parameter space: $\Sigma$ some 2-dimensional manifold -- the **worldsheet** -- for instance $\Sigma = S^1 \times \mathbb{R}$ models
a closed string propagating without interaction.

* target space. $X$ spacetime;

* covariant configuration bundle $E = \Sigma \times X$.

(more needs to be said here...)

... blah-blah-blah...


## Relation to $n$-symplectic manifolds

There is also the notion of

* [[n-symplectic manifold]]s. 

Which is different, but related...

....blah-blah....


## Survey of developments in the field {#SurveyDevelopments}

There is in this sense a covariant form of the [[Legendre transformation]] which associates to every field variable as many conjugated momenta -- the multimomenta -- as there are space-time dimensions. These, together with the field variables, those of $n$-dimensional space-time, and an extra variable, the energy variable, span the multiphase space [1]. For a recent exposition on the differential geometry of this construction, see [2]. Multiphase space, together with a closed, nondegenerate differential $(n+1)$-form, the multisymplectic form, is an example of a multisymplectic manifold [3]. 

Among the achievements of the multisymplectic approach is a geometric formulation of the relation of infinitesimal symmetries and covariantly conserved quantities ([[Noether's theorem]]), see [4] for a recent review, and [5,6] for a clarification of the improvement techniques ("Belinfante-Rosenfeld formula") of the energy-momentum tensor in classical field theory. 

Multisymplectic geometry also provides convenient sets of variational integrators for the numerical study of partial differential equations [7].

Since in multisymplectic geometry, the symplectic 2-form of classical [[Hamiltonian mechanics]] is replaced by a closed [[differential form]] of higher tensor degree, multivector fields and differential forms have their natural appearance. (See [8] for an interpretation of multivector fields as describing solutions to field equations infinitesimally.) Multivector fields form a [[graded Lie algebra]] with the [[Schouten bracket]] (see [9] for a review and unified viewpoint). Using the multisymplectic $(n+1)$-form, one can construct a new bracket for the differential forms, the Poisson forms [10], generalizing a well-known formula for the Poisson brackets related to a symplectic 2-form. 

A remarkable fact is that in order to establish a Jacobi identity, the multisymplectic form has to have a potential, a condition that is not seen in symplectic geometry. Further, the admissible differential forms, the Poisson forms, are subject to the rather strong restrictions on their dependence on the multimomentum variables [11]. In particular, $(n-1)$-forms in this context can be shown to arise exactly from the covariantly conserved currents of Noether symmetries [11], which allows their pairing with spacelike hypersurfaces to yield conserved charges in a geometric way.

Not much is known about the interpretation of Poisson forms of form degree between zero and n-1. However, as $(n-1)$-forms describe vector fields and hence collections of lines [2, 10], and as (certain) functions describe n-vector fields and hence collections of bundle sections [8], it seems natural to speculate that the intermediate forms may be useful for the [[brane]]s of [[string theory]].

The Hamiltonian, infinite dimensional formulation of [[classical field theory]] requires the choice of a spacelike hypersurface ("Cauchy surface") [12] which manifestly breaks the general covariance of the theory at hand. For $(n-1)$-forms, the above mentioned new bracket reduces to the Peierls-deWitt bracket after integration over the spacelike hypersurface [13]. With the choice of a hypersurface, a constraint analysis [14] _&agrave; la_ Dirac [15,16] can be performed [17]. Again, the necessary breaking of general covariance raises the need for an alternative formulation of all this [18]; first attempts have been made to carry out a [[Marsden-Weinstein reduction]] [19] for multisymplectic manifolds with symmetries [20]. However, not very much is known about how to quantize a multisymplectic geometry, see [21] for an approach using a path integral.

This discussion so far concerns field theories of first order, i.e. where the Lagrangian depends on the fields and their first derivatives. Higher order theories can be reduced to first order ones for the price of introducing auxiliary fields. A direct treatment would involve higher order jet bundles [22]. A definition of the covariant Legendre transform and the multiphase space has been given for this case [3].

## References

### On classical multisymplectic geometry

A comprehensive source on covariant field theory with plenty of further references is

* Mark J. Gotay, James Isenberg, Jerrold E. Marsden, Richard Montgomery, _Momentum Maps and Classical Relativistic Fields. Part I: Covariant Field Theory_ ([arXiv:physics/9801019](http://arxiv.org/abs/physics/9801019))

Much of the material in the [section on covariant field theory](#extended phase space) is based on this.

Other texts include

* [[Carlo Rovelli]], _Covariant hamiltonian formalism for field theory: Hamilton-Jacobi equation on the space $\mathcal{G}$_ ([arXiv:gr-qc/0207043](http://arxiv.org/abs/gr-qc/0207043))


* xyz...




Much of the above [survey of recent developments](#SurveyDevelopments) and of the following list of references is reproduced from the web-page

* [[Cornelius Mertzlufft-Paufler]], _[Multisymplectic geometry](http://www.mertzlufft-paufler.de/multisymplectic_geometry.html)_

References mentioned above are

* [1] J. Kijowski, W. Szczyrba, _A Canonical Structure For Classical Field Theories_ . Commun. Math. Phys. 46 (1976) 183.

* [2] M. J. Gotay, J. Isenberg, J. E. Marsden: _Momentum maps and classical relativistic fields. I: Covariant field theory_ [arXiv:physics/9801019v2](http://arxiv.org/abs/physics/9801019v2).

* [3] M. J. Gotay, _A multisymplectic framework for classical field theory and the calculus of variations. I: Covariant Hamiltonian formalism_ 
In M. Francaviglia (ed.), _Mechanics, analysis and geometry: 200 years after Lagrange_ Amsterdam etc.: North-Holland (1991), 203--235.

* [4] M. de Leon, D. Martin de Diego, A. Santamaria-Merino, _Symmetries in Classical Field Theory_ [arXiv:math-ph/0404013](http://arxiv.org/abs/math-ph/0404013).

* [5] M. J. Gotay, J. E. Marsden: _Stress-energy-momentum tensors and the Belinfante--Rosenfeld formula_ Contemp. Math. vol. 132, AMS, Providence, 1992, 367--392.

* [6] M. Forger, H. R&#246;mer, _Currents and the energy-momentum tensor in classical field theory: a fresh look at an old problem_ Ann. Phys. (N.Y.) 309 (2004) 306--389. [arXiv:hep-th/0307199](http://arxiv.org/abs/hep-th/0307199).

* [7] A. Lew, J. E. Marsden, M. Ortiz, M. West, _An overview of variational integrators_
In L. P. Franca (ed.), Finite Element Methods: 70's and Beyond. Barcelona (2003).

* [8] C. Paufler, H. R&#246;mer, _The Geometry of Hamiltonian $n$-vector fields in Multisymplectic Field Theory_ J. Geom. Phys. 44, No.1(2002), 52--69. [arXiv:math-ph/0102008](http://arxiv.org/abs/math-ph/0102008).

* [9] Y. Kosmann-Schwarzbach: Derived brackets. Lett. Math. Phys. 69 (2004) 61--87 [arXiv:math.DG/0312524](http://arxiv.org/abs/math.DG/0312524).

* [10] M. Forger, C. Paufler, H. R&#246;mer: _The Poisson Bracket for Poisson Forms in Multisymplectic Field Theory_ Rev. Math. Phys. 15 (2003) 705 [arXiv:math-ph/0202043](http://arxiv.org/abs/math-ph/0202043).

* [10] M. Forger, C. Paufler, H. R&#246;mer, _Hamiltonian Multivector Fields and Poisson Forms in Multisymplectic Field Theory_ [arXiv:math-ph/0407057](http://arxiv.org/abs/math-ph/0407057).

* [11] M. J. Gotay, _A multisymplectic framework for classical field theory and the calculus of variations. II: Space + time decomposition_ Differ. Geom. Appl. 1(4) (1991), 375--390.

* [12] M. O. Salles, _Campos Hamiltonianos e Colchete de Poisson na Teoria Geom&#233;trica dos Campos_ , PhD thesis, IME-USP, June 2004.

* M. Forger, S. V. Romero, _Covariant Poisson Brackets in Geometric Field Theory_ Commun. Math. Phys. 256 (2005), 375--410. [arXiv:math-ph/0408008](http://arxiv.org/abs/math-ph/0408008).

* [13] M. J. Gotay, J. M. Nester, _Generalized constraint algorithm and special presymplectic manifolds_
In G. E. Kaiser, J. E. Marsden, Geometric methods in mathematical physics, Proc. NSF-CBMS Conf., Lowell/Mass. 1979, Berlin: Springer-Verlag, Lect. Notes Math. 775 (1980) 78--80.

* [14] P. A. M. Dirac, _Lectures on Quantum Mechanic_ Belfer Graduate School of Science, Yeshiva University, N.Y., 1964.

* [15] M. Henneaux, C. Teitelboim, _Quantization of Gauge systems_ Princeton University Press, 1992.

* [16] M. J. Gotay, J. Isenberg, J. E. Marsden, R. Montgomery, _Momentum Maps and Classical Relativistic Fields II: Canonical Analysis of Field Theories_ (2004) [arXiv:math-ph/0411032](http://arxiv.org/abs/math-ph/0411032).

* [17] N. P. Landsman, _Against the Wheeler-DeWitt equation_ Class. Quan. Grav. 12 (1995) L119-L124. [arXiv:gr-qc/9510033](http://arxiv.org/abs/gr-qc/9510033).

* [18] J. E. Marsden, A. Weinstein _Reduction of symplectic manifolds with symmetry_ Rept. Math. Phys. 5 (1974) 121--130.

* [19] F. Munteanu, A. M. Rey, M. Salgado, _The G&#252;nther's formalism in classical field theory: momentum map and reduction_ J. Math. Phys. 45, No. 5 (2004) 1730--1750.

* [20] D. Bashkirov, G. Sardanashvily, _Covariant Hamiltonian Field Theory. Path Integral Quantization_
[arXiv:hep-th/0402057](http://arxiv.org/abs/hep-th/0402057).

* [21] D. J. Saunders, _The Geometry of Jet Bundles_ Lond. Math. Soc. Lect. Notes Ser. 142, Cambr. Univ. Pr., Cambridge, 1989.

A [[higher category theory|higher categorial]] interpretation of 2-plectic geometry is given in

* [[John Baez]], [[Chris Rogers]], _Categorified Symplectic Geometry and the String Lie 2-Algebra_. [arXiv:0901.4721](http://arxiv.org/abs/0901.4721).

This builds a bridge to the notion of [[n-symplectic manifold]]s.

### On quantization of multisymplectic geometry {#RefsonQuantization}

The following articles discuss the [[quantization]] procedure for multisymplectic geometry, generalizing [[geometric quantization]] of [[symplectic geometry]].

* I.V. Kanatchikov, _Geometric (pre)quantization in the polysymplectic approach to field theory_ , ([arXiv:hep-th/0112263](http://arxiv.org/abs/hep-th/0112263)).

The author has also written a paper on [[canonical quantization]]:

* I.V. Kanatchikov, _DeDonder-Weyl theory and a hypercomplex extension of quantum mechanics to field theory_ , ([arXiv:hep-th/9810165](http://arxiv.org/abs/hep-th/9810165v1))


Kanatchikov's "algebra of observables" is a [[Gerstenhaber algebra]] . The relationship between it and the [[Lie superalgebra]] of observables constructed by Forger, Paufler, and Roemer is discussed in this paper:


* M. Forger, C. Paufler, and H. Roemer, _The Poisson Bracket for Poisson Forms in Multisymplectic Field Theory_ , ([arXiv:math-ph/0202043](http://arxiv.org/abs/math-ph/0202043v1))

Kanatchikov's formalism was used by S.P. Hrabak to develop a multisymplectic formulation of [[classical BRST]] 

[[!redirects covariant field theory]]