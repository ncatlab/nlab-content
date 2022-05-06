

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of _Riemannian orbifolds_ is the joint generalization of the concepts of _[[Riemannian manifolds]]_ and _[[orbifolds]]_:

A Riemannian orbifold is an [[orbifold]] equipped with an orbifold [[atlas]] where each [[chart]] $(\widehat{U}_i, G)$ is equipped with a [[Riemannian metric]] such that the [[action]] of $G$ is by [[isometries]], and such that the transition functions from one chart to the other are isometries.

A key aspect is that the orbifold [[singularities]] behave like carrying singular [[curvature]], notably there are [[flat orbifolds]] (also "Euclidean orbifolds", i.e. Riemannian orbifolds with vanishing [[Riemann curvature]] away from the [[singularities]]) whose underlying [[topological spaces]] are [[n-spheres]] (see [below](#FlatCompact2DimensionalOrbifolds)).


Key examples of flat orbifolds are global [[homotopy quotients]] $\mathbb{T}^n \sslash G$ of the [[n-torus]] $\mathbb{T}^n$ equipped with its canonical flat [[Riemannian metric]]. These flat orbifolds are called _toroidal orbifolds_.

## Properties

> under construction

Every flat orbifold whose underlying [[metric space]] is [[connected topological space|connected]] and [[complete metric space|complete]]) is a global quotient of [[Euclidean space]]/[[Cartesian space]] $\mathbb{R}^n$ 

([Ratcliffe 06, 13.3.10](#Ratcliffe06))




## Examples

### Non-compact orbifolds

Basic examples of non-compact Riemannian orbifolds are [[conical singularities]]. 

In the flat case these are [[homotopy quotients]] of the form $V\sslash G$ for $G$ a [[finite group]] and $V \in RO(G)$ a [[finite-dimensional vector space|finite-dimensional]] [[orthogonal group|orthogonal]] [[linear representation]] of $G$. 


\begin{center}
<img src="https://ncatlab.org/nlab/files/Z2OrbifoldSingularity.jpg" width="600">
\end{center}

> graphics grabbed from [Blumenhagen-Lüst-Theisen 13](#BlumenhagenLustTheisen13)

For $V = \mathbb{H}$ equipped with the canonical action of [[finite subgroups of SU(2)]] these are the [[ADE-singularities]].


### Compact flat orbifolds from crystallographic groups
 {#CompactFlatOrbifoldsFromCrystallographicGroups}



+-- {: .num_example #CompactFlatOrbifoldFromCrystallographicGroup}
###### Example
**([[compact topological space|compact]] [[flat orbifolds]] from [[crystallographic groups]])**

Let $E$ be a [[Euclidean space]] and $S \subset Iso(E)$ a [[crystallographic group]] [[action|acting]] on it, with translational [[normal subgroup]] [[lattice (discrete subgroup)|lattice]] $N \subset S$ and corresponding [[point group]] $G = S/N$. 

$$
  \array{
    & 
    1 && 1
    \\
    & \downarrow && \downarrow
    \\
    {\text{normal subgroup}
    \atop
    \text{lattice of translations}}
    & 
    N &\subset& E
    &
    {\text{translation} \atop \text{group}}
    \\
    &
    \big\downarrow && \big\downarrow 
    \\
    {\text{crystallographic} \atop \text{group}}
    &
    S &\subset& Iso(E)
    &
    {\text{Euclidean}
    \atop
    \text{isometry group}}
    \\
    &
    \big\downarrow && \big\downarrow 
    \\
    {\text{point} \atop \text{group}}
    &
    G &\subset& O(E) 
    &
    {\text{orthogonal} \atop \text{group}}
    \\
    &
    \downarrow && \downarrow
    \\
    &
    1 && 1
  }
$$

Then the [[action]] of $G$ on $E$ descends to the [[quotient space]] [[torus]] $E/N$ ([this Prop.](crystallographic+group#InducedPointGroupActionOnTorus))

$$
  \array{
    E 
      &\overset{g}{\longrightarrow}&
    E
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    E/N 
      &\underset{g}{\longrightarrow}& 
    E/N
  }
$$

The resulting [[homotopy quotient]] $(E/N)\sslash G$ is a compact flat orbifold.


=--



The following is the class of special cases of 
Example \ref{CompactFlatOrbifoldFromCrystallographicGroup} for [[point group]] being the [[involution]]-[[action]] by [[reflection]] at a point:

+-- {: .num_example #CoordinateReflectionOnNTorus}
###### Example
**([[coordinate function|coordinate]] [[reflection]] on [[n-torus]])** 

Let $\mathbb{T}^d \coloneqq \mathbb{R}^d / \mathbb{Z}^d$ be the [[n-torus|d-torus]] and consider the [[action]] of the [[cyclic group]] $\mathbb{Z}_2$ by canonical [[coordinate function|coordinate]] [[reflection]]

$$
  \array{
    \mathbb{Z}_2 \times \mathbb{T}^d
    &\longrightarrow&
    \mathbb{T}^d
    \\
    (\sigma, \vec x)
    &\mapsto&
     - \vec x
  }
  \,.
$$

The resulting [[homotopy quotient]] [[orbifold]] $\mathbb{T}^d\sslash\mathbb{Z}_2$ has $2^d$ [[singularities]]/[[fixed points]], namely the points with all coordinates in $\{0\,,\, 1/2\, \mathrm{mod} \mathbb{Z}\}$.

In applications to [[string theory]] orbifolds of the form $\mathbb{R}^{p,1} \times \mathbb{T}^d\sslash \mathbb{Z}_2$ play the role of [[orientifold]] [[spacetimes]] with $2^d$ [[Op-planes]].

=--

### Flat compact 2-dimensional orbifolds
 {#FlatCompact2DimensionalOrbifolds}

In 2 dimensions the [[crystallographic groups]] are the "[[wallpaper groups]]". Hence, as a special case of Example \ref{CompactFlatOrbifoldFromCrystallographicGroup},
the flat [[compact topological space|compact]]  2-dimensional orbifolds may be classified as [[homotopy quotients]] of the [[2-torus]] by [[wallpaper groups]] (for review see e.g. [Guerreiro 09](#Guerreiro09)):


<center>
<img src="https://ncatlab.org/nlab/files/CompactFlat2dOrbifolds.jpg" width="600">
</center>

> graphics grabbed from [Bettiol-Derdzinski-Piccione 18](#BettiolDerdzinskiPiccione18)


#### 2-sphere
 {#TwoSphereAsFlatOrbifold}
 

The [[2-sphere]] arises, in particular, as the [[quotient space]] of the [[torus]] $\mathbb{C}/\mathbb{Z}^2$ by the [[involution]] $z \mapsto -z$, exhibited by the [[Weierstrass elliptic function]] (e.g. [Mukase 04, end of 1.4](Weierstrass+elliptic+function#Mukase04). This realizes the 2-sphere as the underlying coarse space of a [[flat orbifold]] with four singular points, called the _[[pillowcase orbifold]]_.



### Flat compact 3-dimensional orbifolds

#### 3-Sphere

Many flat compact oriented 3-dimensional orbifolds have coarse underlying topological space the [[3-sphere]] ([Dunbar 88](#Dunbar88))

### Flat compact 4-dimensional orbifolds
 {#FlatCompact4dOrbifolds}

#### Kummer surface

The orbifold quotient of the [[4-torus]] by the sign [[involution]] on all four canonical [[coordinates]] is the flat compact 4-dimensional orbifold known as the _[[Kummer surface]]_ $T^4 \sslash \mathbb{Z}_2$ -- the special case of Example \ref{CoordinateReflectionOnNTorus} for $d = 4$. This is a singular [[K3-surface]] (e.g. [Bettiol-Derdzinski-Piccione 18, 5.5](#BettiolDerdzinskiPiccione18))


\begin{center}
<img src="https://ncatlab.org/nlab/files/KummerSingular.jpg" width="300">
\end{center}

> graphics grabbed from [Snowden 11](orbifold#Snowden11)

Also $\mathbb{T}^4\sslash\mathbb{Z}_4$ gives a toroidal orbifold. As [[orientifolds]] with [[D5-branes]] in [[type IIB string theory]] these are discussed in [Buchel-Shiu-Tye 99, Sec. II](#BuchelShiuTye99).


#### 4-Sphere
 {#4SphereAsFlatOrbifold}

The [[complex projective space]] $\mathbb{C}P^2$ is an orbifold quotient of the [[4-torus]] (see [this MO comment](https://mathoverflow.net/a/213009/381)), in generalization of how the [[Weierstrass elliptic function]] exhibits the [[Riemann sphere]] as $\mathbb{T}^2/\mathbb{Z}_2$ ([above](#TwoSphereAsFlatOrbifold)).

A further $\mathbb{Z}_2$-quotient of $\mathbb{C}P^2$ gives the [[4-sphere]] (see at _[4-sphere as quotient of complex projective plane](4-sphere#AsAQuotientOfTheComplexProjectivePlane)_).

\linebreak

### Flat compact 6-dimensional orbifolds

see [FRTV 12](#FRTV12)

### 7-Dimensional $G_2$-orbifolds

see _[[G2-orbifold]]_


## Related concepts

* [[crystallographic group]]

* [[branched cover]]

* [[complex orbifold]]

* [[symplectic orbifold]]

* [[Lorentzian orbifold]]

## References

### General

On [[Riemannian orbifolds]]:

* Joseph Ernest Borzellino, _Riemannian Geometry of Orbifolds_, Dissertation, University of California - Los Angeles, January 1, 1992, pages 1-57.  1992 ([calpoly.edu/math_fac/111](https://digitalcommons.calpoly.edu/math_fac/111))


* {#Ratcliffe06} [[John Ratcliffe]], _Geometric Orbifolds_, chapter 13 in _Foundations of Hyperbolic Manifolds_, Graduate Texts in Mathematics 149, Springer 2006 ([doi:10.1007/978-0-387-47322-2](https://doi.org/10.1007/978-0-387-47322-2), <a href="http://entsphere.com/pub/pdf/Ratcliffe%20-%20Foundations%20of%20hyperbolic%20manifolds%20(2e)%20-%20GTM%20149.pdf">pdf</a>)

* Christian Lange, _Orbifolds from a metric viewpoint_, Geom Dedicata (2020) ([arXiv:1801.03472](https://arxiv.org/abs/1801.03472), [doi:10.1007/s10711-020-00521-x](https://doi.org/10.1007/s10711-020-00521-x))

* {#BettiolDerdzinskiPiccione18} Renato G. Bettiol, Andrzej Derdzinski, [[Paolo Piccione]], _Teichmüller theory and collapse of flat manifolds_, Annali di Matematica (2018) 197: 1247 ([arXiv:1705.08431](https://arxiv.org/abs/1705.08431), [doi:10.1007/s10231-017-0723-7](https://doi.org/10.1007/s10231-017-0723-7))

The [[isometry group]] of [[Riemannian orbifolds]]:

* A. V. Bagaev & N. I. Zhukova, _The isometry groups of Riemannian orbifolds_,  Sib Math J 48, 579–592 (2007) ([doi:10.1007/s11202-007-0060-y](https://doi.org/10.1007/s11202-007-0060-y))

Real-analytic Riemannian orbifolds:

* Marja Kankaanrinta, _On real analytic orbifolds and Riemannian metrics_, 
Algebraic & Geometric Topology 13 (2013) 2369–2381 ([doi:10.2140/agt.2013.13.2369](http://dx.doi.org/10.2140/agt.2013.13.2369))

The Yamabe invariant:

* Kazuo Akutagawal, _Computations of the orbifold Yamabe invariant_, Mathematische Zeitschrift volume 271, pages 611–625 (2012) ([doi:10.1007/s00209-011-0880-0](https://doi.org/10.1007/s00209-011-0880-0))

    

More generally, [[G-structures]] on orbifolds:

* A. V. Bagaev, N. I. Zhukova , _The Automorphism Groups of Finite Type $G$-Structures on Orbifolds_, Siberian Mathematical Journal 44, 213–224 (2003) ([doi:10.1023/A:1022920417785](https://doi.org/10.1023/A:1022920417785))

* [[Robert Wolak]], _Orbifolds, geometric structures and foliations. Applications to harmonic maps_, Rendiconti del seminario matematico - Universita politecnico di Torino, vol. 73/1 , 3-4 (2016), 173-187 ([arXiv:1605.04190](https://arxiv.org/abs/1605.04190))

Discussion of [[gravity]] and maybe [[quantum gravity]] on orbifolds:

* Helio V. Fagundes, Teofilo Vargas, _Orbifolds, Quantum Cosmology, and Nontrivial Topology_ ([arXiv:gr-qc/0611048](https://arxiv.org/abs/gr-qc/0611048))

Discussion of [[perturbative string theory]] on toroidal orbifolds

* {#BlumenhagenLustTheisen13} [[Ralph Blumenhagen]], [[Dieter Lüst]], [[Stefan Theisen]], Chapter 10.5 _Toroidal orbifolds_,  of _Basic Concepts of String Theory_ Part of the series Theoretical and Mathematical Physics pp 585-639 Springer 2013

For more see the references at _[[orbifold]]_.


### Flat orbifolds

* [[John Ratcliffe]], Steven T. Tschantz, _The Calabi construction for compact flat orbifolds_, Topology and its Applications Volume 178, 1 December 2014, Pages 87-106 ([doi:10.1016/j.topol.2014.09.005](https://doi.org/10.1016/j.topol.2014.09.005))



#### Of dimension 2

In 2 dimensions

* [[John Milnor]], _On Lattès Maps_ ([arXiv:math/0402147](https://arxiv.org/abs/math/0402147))

* {#Guerreiro09} João Guerreiro, _Orbifolds and Wallpaper Patterns_ ([pdf](https://faculty.math.illinois.edu/~ruiloja/Estudantes/TrabalhoJGuerreiro.pdf))

2d toroidal [[orientifolds]]:

* Dongfeng Gao, [[Kentaro Hori]], Section 7.3 of: _On The Structure Of The Chan-Paton Factors For D-Branes In Type II Orientifolds_ ([arXiv:1004.3972](https://arxiv.org/abs/1004.3972))

* {#DMR14} [[Charles Doran]], Stefan Mendez-Diez, [[Jonathan Rosenberg]], _String theory on elliptic curve orientifolds and KR-theory_ ([arXiv:1402.4885](http://arxiv.org/abs/1402.4885))

#### Of dimension 3

* {#Dunbar88} [[William Dunbar]], _Geometric orbifolds_, Rev. Mat. Univ. Complutense Madr. 1, No.1-3, 67-99 (1988)



#### Of dimension 4

Flat (toroidal) orbifolds of dimension 4:

In the the context of [[black holes in string theory]]:


* Justin R. David, Gautam Mandal, Spenta R. Wadia, _Microscopic Formulation of Black Holes in String Theory_, Phys.Rept.369:549-686,2002 ([arXiv:hep-th/0203048](https://arxiv.org/abs/hep-th/0203048))


In the context of [[RR-field tadpole cancellation]] for [[intersecting D-brane models]] on toroidal orientifolds:

Specifically [[K3]] [[orientifolds]] ($\mathbb{T}^4/G_{ADE}$) in [[type IIB string theory]], hence for [[D9-branes]] and [[D5-branes]]:


* [[Eric Gimon]], [[Joseph Polchinski]], Section 3.2 of: _Consistency Conditions for Orientifolds and D-Manifolds_, Phys. Rev. D54: 1667-1676, 1996 ([arXiv:hep-th/9601038](https://arxiv.org/abs/hep-th/9601038))

* {#GimonJohnson96} Eric Gimon, [[Clifford Johnson]], _K3 Orientifolds_, Nucl. Phys. B477: 715-745, 1996 ([arXiv:hep-th/9604129](https://arxiv.org/abs/hep-th/9604129))

* {#BuchelShiuTye99} Alex Buchel, [[Gary Shiu]], S.-H. Henry Tye, _Anomaly Cancelations in Orientifolds with Quantized B Flux_, Nucl.Phys. B569 (2000) 329-361 ([arXiv:hep-th/9907203](https://arxiv.org/abs/hep-th/9907203))

* P. Anastasopoulos, A. B. Hammou, _A Classification of Toroidal Orientifold Models_, Nucl. Phys. B729:49-78, 2005 ([arXiv:hep-th/0503044](https://arxiv.org/abs/hep-th/0503044))

Specifically [[K3]] [[orientifolds]] ($\mathbb{T}^4/G_{ADE}$) in [[type IIA string theory]], hence for [[D8-branes]] and [[D4-branes]]:

* {#ParkUranga98} [[Jaemo Park]], [[Angel Uranga]], _A Note on Superconformal N=2 theories and Orientifolds_, Nucl. Phys. B542:139-156, 1999 ([arXiv:hep-th/9808161](https://arxiv.org/abs/hep-th/9808161))


* {#AFIRU00a} G. Aldazabal, S. Franco, [[Luis Ibanez]], R. Rabadan, [[Angel Uranga]], _D=4 Chiral String Compactifications from Intersecting Branes_, J. Math. Phys. 42:3103-3126, 2001 ([arXiv:hep-th/0011073](https://arxiv.org/abs/hep-th/0011073))

* {#AFIRU00b} G. Aldazabal, S. Franco, [[Luis Ibanez]], R. Rabadan, [[Angel Uranga]], _Intersecting Brane Worlds_, JHEP 0102:047, 2001 ([arXiv:hep-ph/0011132](https://arxiv.org/abs/hep-ph/0011132))

* {#KataokaShimojo01} H. Kataoka, M. Shimojo, _$SU(3) \times SU(2) \times U(1)$ Chiral Models from Intersecting D4-/D5-branes_, Progress of Theoretical Physics, Volume 107, Issue 6, June 2002, Pages 1291–1296 ([arXiv:hep-th/0112247](https://arxiv.org/abs/hep-th/0112247), [doi:10.1143/PTP.107.1291](https://doi.org/10.1143/PTP.107.1291))

Systematic construction of [[Ricci tensor|Ricci flat]] [[Riemannian metrics]] on [[K3]] [[orbifolds]]:

* [[Shamit Kachru]], [[Arnav Tripathy]], [[Max Zimet]], _K3 metrics_ ([arXiv:2006.02435](https://arxiv.org/abs/2006.02435))

* [[Arnav Tripathy]], [[Max Zimet]], _A plethora of K3 metrics_ ([arXiv:2010.12581](https://arxiv.org/abs/2010.12581))







In the context of [[Mathieu moonshine]] from [[string]] [[sigma models]] on [[K3]]s: 

* [[Matthias Gaberdiel]], [[Stefan Hohenegger]], [[Roberto Volpato]], _Symmetries of K3 sigma models_, Commun.Num.Theor.Phys. 6 (2012) 1-50 ([arXiv:1106.4315](https://arxiv.org/abs/1106.4315))

* [[Matthias Gaberdiel]], Roberto Volpato, _Mathieu Moonshine and Orbifold K3s_ ([arXiv:1206.5143](https://arxiv.org/abs/1206.5143))

#### Of dimension 6

In 6 dimensions (mostly motivated as singular [[supersymmetry and Calabi-Yau manifolds|Calabi-Yau compactifications]] of [[heterotic string theory]] to 4d)

* Jens Erler, [[Albrecht Klemm]], _Comment on the Generation Number in Orbifold Compactifications_, Commun. Math. Phys. 153:579-604, 1993 ([arXiv:hep-th/9207111](https://arxiv.org/abs/hep-th/9207111))

* [[Dieter Lüst]], S. Reffert, E. Scheidegger, S. Stieberger, _Resolved Toroidal Orbifolds and their Orientifolds_, Adv. Theor. Math. Phys. 12:67-183, 2008 ([arXiv:hep-th/0609014](https://arxiv.org/abs/hep-th/0609014))

* S. Reffert, _Toroidal Orbifolds: Resolutions, Orientifolds and Applications in String Phenomenology_, Munich 2006 ([arXiv:hep-th/0609040](https://arxiv.org/abs/hep-th/0609040), [spire:725406](https://inspirehep.net/literature/725406))

* [[Ron Donagi]], [[Katrin Wendland]], _On orbifolds and free fermion constructions_, J. Geom. Phys. 59:942-968, 2009 ([arXiv:0809.0330](https://arxiv.org/abs/0809.0330))

* {#FRTV12} Maximilian Fischer, Michael Ratz, Jesus Torrado, Patrick K.S. Vaudrevange, _Classification of symmetric toroidal orbifolds_, JHEP 1301 (2013) 084 ([arXiv:1209.3906](https://arxiv.org/abs/1209.3906))




[[!redirects Riemannian orbifolds]]

[[!redirects flat orbifold]]
[[!redirects flat orbifolds]]

[[!redirects toroidal orbifold]]
[[!redirects toroidal orbifolds]]
