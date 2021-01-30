[[!redirects moment map]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

# The momentum map
* table of contents
{: toc}

## Idea

A _momentum map_ is a dual incarnation of a [[Hamiltonian action]] of a [[Lie group]] (or [[Lie algebra]]) on a [[symplectic manifold]].

An [[action]] of a [[Lie group]] $G$ on a [[symplectic manifold]] $X$ by ([[Hamiltonian symplectomorphisms|Hamiltonian]]) [[symplectomorphisms]] corresponds [[infinitesimal space|infinitesimally]] to a Lie algebra [[homomorphism]] from the [[Lie algebra]] $\mathfrak{g}$ to the [[Hamiltonian vector fields]] on $X$. If this lifts to a coherent choice of [[Hamiltonians]], hence to a Lie algebra homomorphism $\mathfrak{g} \to (C^\infty(X), \{-,-\})$ to the [[Poisson bracket]], then, by [[dual vector space|dualization]], this is equivalently a [[Poisson manifold]] homomorphism of the form

$$
  \mu : X \to \mathfrak{g}^*
  \,.
$$

This $\mu$ is called the _momentum map_ (or _moment map_[^name]) of the Hamiltonian action.
[^name]: Moment map is a misnomer and physically incorrect. It is an erroneous translation of the French notion application moment. See [this mathoverflow question](https://mathoverflow.net/q/242468) for the history of the name.

The name derives from the special and historically first case of [[angular momentum]] in the [[rigid body dynamics|dynamics of rigid bodies]], see _[Examples - Angular momentum](#AngularMomentum)_ below.


## Definition

The [Preliminaries](#Preliminaries) below review some basics of [[Hamiltonian vector fields]]. The definition of the momentum map itself is below in _[Hamiltonian action and the momentum map](#HamiltonianActionAndTheMomentumMap)_.

### Preliminaries
 {#Preliminaries}

This section briefly reviews the notion of [[Hamiltonian vector fields]] on a [[symplectic manifold]]

The basic setup is the following: Let $(M,\omega)$ be a [[symplectic manifold]] with a [[Hamiltonian action]] of a [[Lie group]] $G$. In particular that means that there is an [[action]] $\nu\colon G \times M \to M$ via [[symplectomorphism]]s (diffeomorphisms $\nu_g$ such that $\nu_g^*(\omega) = \omega$). A vector field $X$ is [[symplectic vector field|symplectic]] if the corresponding flow preserves (again by pullbacks) $\omega$. The symplectic vector fields form a Lie subalgebra $\chi(M,\omega)$ of the Lie algebra of all smooth vector fields $\chi(M)$ on $M$ with respect to the Lie bracket. 

By the [[Cartan homotopy formula]] and closedness $d \omega = 0$

$$
\mathcal{L}_X \omega = d \iota_X \omega
$$

where $\mathcal{L}_X$ denotes the [[Lie derivative]]. Therefore a vector field $X$ is symplectic iff $\iota(X)\omega = d H$ for some function $H\in C^\infty(M)$, usually called Hamiltonian (function) for $X$. Here $X$ is determined by $H$ up to a locally constant function. Such $X = X_H$ is called the __Hamiltonian vector field__ corresponding to $H$.  The Poisson structure on $M$ is the bracket $\{,\}$ on functions may be given by 

$$
\{ f, g\} := [X_f,X_g]
$$

where there is a Lie bracket of vector fields on the right hand side.

For $(M,\omega)$ a connected symplectic manifold,  there is an exact sequence of [[Lie algebras]]

$$
  0 \to \mathbf{R}\to (C^\infty(M), \{-,-\}) \to \chi(M,\omega) \to 0
  \,.
$$

See at _[Hamiltonian vector field -- Relation to Poisson bracket](Hamiltonian+vector+field#RelationToFunctions)_.



### Hamiltonian action and momentum map
 {#HamiltonianActionAndTheMomentumMap}

Let $(X, \omega)$ be a [[symplectic manifold]] and let $\mathfrak{g}$ be a [[Lie algebra]]. Write $(C^\infty(X), \{-,-\})$ for the [[Poisson bracket]] Lie algebra underlying the corresponding [[Poisson algebra]]. 

+-- {: .num_defn #MomentumMap}
###### Definition

A _[[Hamiltonian action]]_ of $\mathfrak{g}$ on $(X, \omega)$ is a [[Lie algebra]] [[homomorphism]]

$$
  \tilde \mu \;\colon\; \mathfrak{g} \longrightarrow (C^\infty(X), \{-,-\})
  \,.
$$

The corresponding function

$$
  \mu \;\colon\; X \longrightarrow \mathfrak{g}^*
$$

to the [[dual vector space]] of $\mathfrak{g}$, defined by

$$
  \mu \;\colon\; x \mapsto \tilde \mu(-)(x)
$$

is the corresponding **momentum map**.

=--

+-- {: .num_remark #Notation}
###### Remark

If one writes the evaluation pairing as

$$
  \langle -,-\rangle : \mathfrak{g}^* \otimes \mathfrak{g} \to \mathbb{R}
$$

then the equation characterizing $\mu$ in def. \ref{MomentumMap} reads for all $x \in X$ and $v \in \mathfrak{g}$

$$
  \langle \mu(x), v \rangle = \tilde \mu(v)(x)
  \,.
$$

This is the way it is often written in the literature.

Notice that this in turn means that 

$$
  \tilde \mu(v)= \mu^\ast \langle -,v\rangle
  \,.
$$

=--


+-- {: .num_prop #EquivalenceOfLieAndPoissonFormulation}
###### Proposition

The following are equivalent

1. the linear map underlying $\tilde\mu$ in def. \ref{MomentumMap} is [[Lie algebra]] [[homomorphism]];

1. its dual $\mu$ is a [[Poisson manifold]] [[homomorphism]] with respect to the [[Lie-Poisson structure]] on $\mathfrak{g}^\ast$.

=--

+-- {: .proof}
###### Proof

This follows by just unwinding the definitions.

In one direction, suppose that $\tilde \mu$ is a Lie homomorphism. Since the [[Lie-Poisson structure]] is fixed on linear functions on $\mathfrak{g}^\ast$, it is sufficient to check that $\mu^\ast$ preserves the Poisson bracket on these. 
Consider hence two Lie algebra elements $v_1, v_2 \in \mathfrak{g}$ regarded as linear functions $\langle -,v_i\rangle$ on $\mathfrak{g}^\ast$. Noticing that on such linear functions the Lie-Poisson structure is given by the Lie bracket we have, using remark \ref{Notation}

$$
  \begin{aligned}
    \mu^\ast \{\langle -,v_1\rangle, \langle -,v_2\rangle\}
    &=
    \mu^\ast \langle-,[v_1,v_2]\rangle
    \\
    & = \tilde \mu([v_1,v_2])
    \\
    & = \{\tilde\mu(v_1), \tilde\mu(v_2)\}
    \\
    & = 
   \left\{  
      \mu^\ast \langle -,v_1\rangle, \mu^\ast \langle -,v_2\rangle
   \right\}
  \end{aligned}
$$

and hence $\mu^\ast$ preserves the Poisson brackets.

Conversely, suppose that $\mu$ is a Poisson homomorphism. Then

$$
  \begin{aligned}
    \tilde\mu [v_1,v_2]
    &=
    \mu^\ast \langle -, [v_1,v_2]\rangle
    \\
    & =
    \mu^\ast \{\langle -,v_1\rangle, \langle -,v_2\rangle\}
    \\
    & =
    \left\{
      \mu^\ast \langle -, v_1\rangle,
      \mu^\ast \langle -, v_2\rangle
    \right\}
    \\
    & =
    \left\{
      \tilde\mu(v_1), \tilde\mu(v_2)
    \right\}
  \end{aligned}
$$

and so $\tilde \mu$ is a Lie homomorphism.

=--

## Examples

### Angular momentum
 {#AngularMomentum}
Consider the action of SO(3) on $\mathbb{R}^3$, which induces a Hamiltonian action on $T^*\mathbb{R}^3\cong\mathbb{R}^3\times\mathbb{R}^3$ via 
$$(q,p)\xrightarrow{A\in\text{SO(3)}}(Aq,pA^{-1})$$
where $q$ is a column vector and $p$ is a row vector. Then the momentum map for this Hamiltonian action is 
$$\mu\colon T^*(\mathbb{R}^3)\to \mathfrak{so}(3)^*,\quad \left\langle\mu(q,p),\;\vec\theta\cdot\begin{pmatrix}\Omega_1\\\Omega_2\\\Omega_3\end{pmatrix} \right\rangle\to (\vec{q}\times \vec p)\cdot\vec{\theta}$$
where 
$$\Omega_1=\begin{pmatrix}0&0&0\\0&0&-1\\0&1&0\end{pmatrix},\quad\Omega_2=\begin{pmatrix}0&0&1\\0&0&0\\-1&0&0\end{pmatrix},\quad \Omega_3=\begin{pmatrix}0&-1&0\\1&0&0\\0&0&0\end{pmatrix}$$

If we choose $\Omega_1,\Omega_2,\Omega_3$ as an orthonormal basis of $\mathfrak{so}(3)$ and then identify $\mathfrak{so}(3)\cong\mathfrak{so}(3)^*\cong\mathbb{R}^3$, then $\mu(q,p)=\vec q\times\vec p$, which is the angular momentum. 

## Properties

### Relation to conserved quantities

The values of the momentum map for each given Lie algebra generator may be regarded as the [[conserved current|conserved currents]] given by a _Hamiltonian [[Noether theorem]]_.

Specifically if $(X,\omega)$ is a [[symplectic manifold]] equipped with a "time evolution" [[Hamiltonian action]] $\mathbb{R} \to \mathfrak{Poisson}(X,\omega)$ given by a [[Hamiltonian]] $H$ and if $\mathfrak{g} \to \mathfrak{Poisson}(X,\omega)$ is some [[Hamiltonian action]] with momentum $\Phi(\xi)$ for $\xi \in \mathfrak{g}$ which preserves the Hamiltonian in that the [[Poisson bracket]] vanishes

$$
  \{\Phi^\xi, H\} = 0
$$

then of course also the time evolution of the momentum vanishes

$$
  \frac{d}{d t} \Phi^\xi = \{H, \Phi^\xi\} = 0
  \,.
$$

See at _[Noether theorem -- In terms of momentum maps/Hamiltonian Noether theorem ](Noether%27s+theorem#HamiltonianNoetherTheorem)_.

### Relation to constrained mechanics
 {#RelationToConstrainedMechanics}

In the context of [[constrained mechanics]] the components of the momentum map (as the Lie algebra argument varies) are called [[first class constraints]]. See _[[symplectic reduction]]_ for more.

## Related concepts

The momentum map is a crucial ingredient in the construction of Marsden--Weinstein [[symplectic quotients]] and in other variants of symplectic reduction.




## References

The concept is originally due to [[Jean-Marie Souriau]].

### General

* [[Victor Guillemin]], [[Yael Karshon]], [[Viktor Ginzburg]], _Moment Maps, Cobordisms, and Hamiltonian Group Actions_, Mathematical Surveys and Monographs, volume 98

Lecture notes and surveys include

* [[Joel W. Robbin]], _The moment map_, an exposition, [pdf](http://www.math.wisc.edu/~robbin/moment.pdf)

* [[Nicole Berline]], [[Michèle Vergne]], _Hamiltonian manifolds and moment maps_ ([pdf](http://www.math.polytechnique.fr/~berline/cours-Fudan.pdf))

Original articles include

* [[Victor Guillemin]], [[Shlomo Sternberg]], _Geometric asymptotics_, AMS (1977) ([online](http://www.ams.org/online_bks/surv14))

* [[Michael Atiyah]], _Convexity and commuting Hamiltonians_, Bull. London
Math. Soc. __14__ (1982), 1-15.

* [[Michael Atiyah]], [[Raoul Bott]], _The moment map and equivariant cohomology_, Topology, Vol 23, No. 1 (1984) ([pdf](https://www.math.sunysb.edu/~mmovshev/MAT570Spring2008/BOOKS/atiyahbott_moment.pdf))
  {#AtiyahBott84}

Further developments are in

* M. Spera, _On a generalized uncertainty principle, [[coherent state]]s and the moment map_, J. of Geometry and Physics __12__ (1993) 165-182, [MR94m:58097](http://www.ams.org/mathscinet-getitem?mr=1237511), <a href="http://dx.doi.org/10.1016/0393-0440(93)90032-A">doi</a>


* [[Ctirad Klimcik]], [[Pavol Severa]], _[[T-duality]] and the moment map_, IHES/P/96/70, [hep-th/9610198](http://arxiv.org/abs/hep-th/9610198); _Poisson-Lie T-duality: open strings and D-branes_, CERN-TH/95-339. Phys.Lett. B376 (1996) 82-89, [hep-th/9512124](http://arxiv.org/abs/hep-th/9512124)

* A. Cannas da Silva, [[Alan Weinstein]], _Geometric models for noncommutative algebras_, Berkeley Math. Lec. Notes Series, AMS 1999, ([pdf](http://math.berkeley.edu/%7Ealanw/Models.pdf))

* Friedrich Knop, _Automorphisms of multiplicity free Hamiltonian manifolds_, [arxiv/1002.4256](http://arxiv.org/abs/1002.4256)

* W. Crawley-Boevey, _Geometry of the moment map for representations of
quivers_, Compositio Math. __126__ (2001), no. 3, 257-293.

See also

* wikipedia, _[momentum map](http://en.wikipedia.org/wiki/Moment_map)_

Momentum maps in [[higher geometry]], [[schreiber:Higher geometric prequantum theory]], are discussed in 

* [[Yael Fregier]], [[Chris Rogers]], [[Marco Zambon]], _Homotopy moment maps_ ([arXiv:1304.2051](http://arxiv.org/abs/1304.2051))

### Relation to symplectic reduction

Reviews include for instance



* {#FOF} [[José Figueroa-O'Farrill]], p. 26 of  chapter 2+3 of PhD thesis  ([pdf](http://empg.maths.ed.ac.uk/Activities/BRST/Ch2+3PhD.pdf))
 

### Relation to equivariant cohomology

Relation to [[equivariant cohomology]]:

* [[Michael Atiyah]], [[Raoul Bott]], _The moment map and equivariant cohomology_, Topology vol. 23 No. 1 1984  ([pdf](https://www.math.sunysb.edu/~mmovshev/MAT570Spring2008/BOOKS/atiyahbott_moment.pdf))

### Generalization: group-valued momentum maps

* [[Anton Alekseev]], Anton Malkin, [[Eckhard Meinrenken]], _Lie group valued moment maps_, J. Differential Geom. Volume 48, Number 3 (1998), 445-495. [euclid](http://projecteuclid.org/euclid.jdg/1214460860), [MR1638045](http://www.ams.org/mathscinet-getitem?mr=1638045)

* [[Eckhard Meinrenken]], _Lectures on group-valued moment maps and Verlinde formulas_, 35 pages, January 2012, [pdf](http://www.math.toronto.edu/mein/research/NotreLectures.pdf)

The relation between momentum maps and [[conserved currents]]/[[Noether's theorem]] is amplied for instance in
 
* {#Fan} Huijun Fan, _Lecture 8, Moment map and symplectic reduction_ ([pdf](http://www.math.pku.edu.cn/teachers/fanhj/courses/symp-8.pdf))
 

### In thermodynamics
 {#ReferencesInThermodynamics}

Since momentum maps generalize [[energy]]-functionals, they provide a covariant formulation of [[thermodynamics]]:


* [[Jean-Marie Souriau]], _Thermodynamique et g&#233;om&#233;trie_,  Lecture Notes in Math. 676 (1978), 369&#8211;397 ([scan](http://www-lib.kek.jp/cgi-bin/kiss_prepri.v8?KN=197810025))

* {#IglesiasSouriau84} [[Patrick Iglesias-Zemmour]], [[Jean-Marie Souriau]] _Heat, cold and Geometry_, in: M. Cahen et al (eds.) Differential geometry and mathematical physics, 37-68, D. Reidel 1983 ([web](http://www.jmsouriau.com/Heat_Cold_And_Geometry_1983.htm), [pdf](http://www.jmsouriau.com/Publications/JMSouriau-PIglesias-HeatColdAndGeometry1983.pdf), [doi:978-94-009-7022-9_5](https://doi.org/10.1007/978-94-009-7022-9_5))

* [[Jean-Marie Souriau]], chapter IV "Statistical mechanics" of _Structure of dynamical systems. A symplectic view of physics_ . Translated from the French by C. H. Cushman-de Vries. Translation edited and with a preface by R. H. Cushman and G. M. Tuynman. Progress in Mathematics, 149. Birkh&#228;user Boston, Inc., Boston, MA, 1997

* [[Patrick Iglesias-Zemmour]], _Essai de «thermodynamique rationnelle» des milieux continus_, Annales de l'I.H.P. Physique théorique, Volume 34 (1981) no. 1,  p. 1-24 ([numdam:AIHPA_1981__34_1_1_0](http://www.numdam.org/item/AIHPA_1981__34_1_1_0))

* [[Jean-Marie Souriau]],Mécanique statistique, groupes de Lie et cosmologie. In Colloques int. du CNRS; numéro 237; Aix-en-Provence, France, 1974; pp. 24–28, 59–113. English translation by F. Barbaresco, April, 2020. Available online: https://www.academia.edu/42630654/Statistical_Mechanics_Lie_Group_and_Cosmology_
1_st_part_Symplectic_Model_of_Statistical_Mechanics(access on 20 April 2020)

Review includes

* {#Marle16} Charles-Michel Marle, _From tools in symplectic and Poisson geometry to Souriau's theories of statistical mechanics and thermodynamics_, Entropy 2016, 18(10), 370 ([arXiv:1608.00103](https://arxiv.org/abs/1608.00103))

* Charles-Michel Marle, On Gibbs states of mechanical systems with symmetries, arXiv:2012.00582v2 [math.DG], Januray 13th 2021  

* Barbaresco, F.; Gay-Balmaz, F. Lie Group Cohomology and (Multi)Symplectic Integrators: New Geometric Tools for Lie Group Machine Learning Based on Souriau Geometric Statistical Mechanics. Entropy 2020, 22, 498. https://www.mdpi.com/1099-4300/22/5/498

* Koszul, J.-L., Introduction to Symplectic Geometry, SPRINGER, 2019


[[!redirects moment maps]]

[[!redirects momentum map]]
[[!redirects momentum maps]]

[[!redirects ∞-moment map]]
[[!redirects ∞-moment maps]]

[[!redirects infinity-moment map]]
[[!redirects infinity-moment maps]]

