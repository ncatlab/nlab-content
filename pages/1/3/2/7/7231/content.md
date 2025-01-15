
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Exceptional structures
+-- {: .hide}
[[!include exceptional structures -- contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[Lie group]] $G_2$ is one (or rather: three) of the [[exceptional Lie groups]]. One way to characterize it is as the [[automorphism group]] of the [[octonions]] as a [[normed algebra]]:

$$
  G_2 = Aut(\mathbb{O})
  \,.
$$

Another way to characterize it is as the [[stabilizer subgroup]] inside the [[general linear group]] $GL(7)$ of the canonical [[differential n-form|differential 3-form]]  $\langle ,(-)\times (-) \rangle$ on the [[Cartesian space]] $\mathbb{R}^7$

$$
  G_2 \simeq Stab_{GL(7)}(\langle -, -\times -\rangle)
  \,.
$$

As such, the group $G_2$ is a higher analog of the [[symplectic group]] (which is the group that preserves a canonical 2-form on any $\mathbb{R}^{2n}$), obtained by passing from [[symplectic geometry]] to [[2-plectic geometry]].


## Definition
 {#Definition}


+-- {: .num_defn #As2PlectomorphismsOnR7}
###### Definition

On the [[Cartesian space]] $\mathbb{R}^7$ consider the _[[associative 3-form]]_, the constant [[differential n-form|differential 3-form]]  $\omega \in \Omega^3(\mathbb{R}^7)$ given on tangent vectors $u,v,w \in \mathbb{R}^7$ by

$$
  \omega(u,v,w) \coloneqq \langle u , v \times w\rangle
  \,,
$$

where

* $\langle -,-\rangle$ is the canonical [[bilinear form]] 

* $(-)\times(-)$ is the [[cross product]] of vectors.

Then the group $G_2 \hookrightarrow GL(7)$ is the [[subgroup]] of the [[general linear group]] acting on $\mathbb{R}^7$ which preserves the canonical [[orientation]] and preserves this 3-form $\omega$. Equivalently, it is the subgroup preserving the orientation and the [[Hodge star operator|Hodge dual]] differential 4-form $\star \omega$.

=--

See for instance the introduction of [Joyce 1996](#Joyce96).

## Properties

### Orientation
 {#Orientation}

The inclusion $G_2 \hookrightarrow GL(7)$ of def. \ref{As2PlectomorphismsOnR7} factors through the [[special orthogonal group]]

$$
  G_2 
    \hookrightarrow 
  SO(7) 
    \hookrightarrow 
  GL(7)
  \,.
$$


### Dimension
 {#Dimension}

The [[dimension]] of (the [[manifold]] [[underlying]]) $G_2$ is 

$$
  dim(G_2) = 14
  \,.
$$

One way to see this is via [octonionic basic triples](octonion#ElementaryTriples) $(e_1, e_2, e_3) \in \mathbb{O}^3$ and the fact ([this proposition](octonion#BasicTriplesFormAutomorphism)) that these form a [[torsor]] over $G_2$, hence that the space of them has the same dimension as $G_2$: 

* the space of choices for $e_1$ is the 6-[[sphere]] of imaginary unit octonions;

* given that, the space of choices for $e_2$ is a 5-sphere of imaginary unit octonions orthogonal to $e_1$;

* given that, then the space of choices for $e_3$ is the [[3-sphere]] of imaginary unit octonions orthogonal to both $e_1$ and $e_2$.

Hence

$$
  dim(G_2) = dim(S^6) + dim(S^5) + dim(S^3) = 14
  \,.
$$

(e.g. [Baez, 4.1](#Baez))


### Cohomology

The _[[Dwyer-Wilkerson space]]_ $G_3$ ([Dwyer-Wilkerson 93](Dwyer-Wilkerson+H-space#DwyerWilkerson93)) is a [[p-adic completion|2-complete]] [[H-space]], in fact a finite [[loop space]]/[[infinity-group]], such that the mod 2 [[cohomology ring]] of its [[classifying space]]/[[delooping]] is the mod 2 [[Dickson invariants]] of rank 4. As such, it is the fourth and last space in a series of [[infinity-groups]] that starts with 3 [[compact Lie groups]]:

| $n=$ | 1 | 2 | 3 | 4 | 
|--|--|--|--|--|
| $DI(n)=$ | [[Z/2]] | [[SO(3)]] | [[G2]] | [[G3]] |
|          | [= Aut(C)](complex+number#AutomorphismsOfComplexNumbersIsZ2)        | [= Aut(H)](quaternion#AutomorphismsOfQUatrnionsAlgebraIsSO3)       |  [= Aut(O)](octonion#AutomorphismsOfOctonionAlgebraIsG2)  |   |




### Subgroups
 {#Subgroups}

We discuss various [[subgroups]] of $G_2$.

+-- {: .num_defn #StabilizerOfQuaternions}
###### Definition

Write 

* $G_2 = Aut(\mathbb{O})$, the [[automorphism group]] of the octonions as a normed alegbra,

* $Stab_{G_2}(\mathbb{H})$, the [[stabilizer subgroup]] of [[generalized the|the]] [[quaternions]] inside the octonions, i.e. of elements $\sigma\in G_2$ such that $\sigma_{|\mathbb{H}}\colon \mathbb{H}\to \mathbb{H} \hookrightarrow\mathbb{O}$;

* $Fix_{G_2}(\mathbb{H})$ for the further subgroup of elements that [[fixed point|fix]] each quaternions (the "elementwise stabilizer group"), i.e. those $\sigma$ with $\sigma_{\vert \mathbb{H}} = id_{\mathbb{H}}$.

=--

+-- {: .num_prop #ElementwiseStabilizerOfHIsSU2}
###### Proposition

The elementwise stabilizer group of the [[quaternions]] is [[SU(2)]]:

$$
  Fix_{G_2}(\mathbb{H}) \simeq SU(2)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Consider [octonionic basic triples](octonion#ElementaryTriples) $(e_1, e_2, e_3) \in \mathbb{O}^3$ and the fact ([this proposition](octonion#BasicTriplesFormAutomorphism)) that these form a [[torsor]] over $G_2$.
The choice of $(e_1,e_2)$ is equivalently a choice of inclusion $\mathbb{H} \hookrightarrow \mathbb{O}$. Then the remaining space of choices for $e_3$ is the [[3-sphere]] (the space of unit imaginary octonions orthogonal to both $e_1$ and $e_2$). This carries a unit group structure, and by the torsor property this is the required subgroup of $SU(2)$.

=--


+-- {: .num_prop #StabilizingAndFixingTheQuaternions}
###### Proposition

The subgroups in def. \ref{StabilizerOfQuaternions} sit in a [[short exact sequence]] of the form

$$
  \array{
    1 &=& 1
    \\
    \downarrow && \downarrow
    \\
    Fix_{G_2}(\mathbb{H}) & \simeq & SU(2)
    \\
    \downarrow && \downarrow
    \\
    Stab_{G_2}(\mathbb{H}) & \simeq & SO(4)
    \\
    \downarrow && \downarrow
    \\
    Aut(\mathbb{H}) &\simeq& SO(3)
    \\
    \downarrow && \downarrow
    \\
    1 &=& 1
  }
$$

exhibiting [[special orthogonal group|SO(4)]] as a [[group extension]] of the [[special orthogonal group]] $SO(3)$ by the [[special unitary group]] $SU(2)$.

=--

(e.g. [Ferolito, section 4](#Ferolito), see also at *[SO(3) -- Irreps](SO%283%29#irreducible_representations)*)



Furthermore there is a [[subgroup]] $SU(3) \hookrightarrow G_2$ whose [[intersection]] with $SO(4)$ is $U(2)$. The [[simple Lie group|simple]] part $SU(2)$ of this intersection is a [[normal subgroup]] of $SO(4)$.

(see e.g. [Miyaoka 93](#Miyaoka93))

The [[coset space]] [[G2/SU(3) is the 6-sphere]]. See there for more.


<img src="https://ncatlab.org/nlab/files/3dSubgroupsOfG2.jpg" width="700">

(from [Kramer 02](#Kramer02))


The [[Weyl group]] of $G_2$ is the [[dihedral group]] of [[order of a group|order]] 12. (see e.g. [Ishiguro, p. 3](#Ishiguro)).


$\,$



### Supgroups

+-- {: .num_prop #QuotientOfSpin7ByG2IsS7}
###### Proposition
**([[coset space]] of [[Spin(7)]] by [[G₂]] is [[7-sphere]])**

Consider the canonical [[action]] of [[Spin(7)]] on the [[unit sphere]] in $\mathbb{R}^8$ (the [[7-sphere]]),

1. This action is is [[transitive action|transitive]];

1. the [[stabilizer group]] of any point on $S^7$ is [[G₂]];

1. all [[G₂]]-subgroups of [[Spin(7)]] arise this way, and are all [[conjugate subgroup|conjugate]] to each other.

Hence the [[coset space]] of [[Spin(7)]] by [[G₂]] is the [[7-sphere]]

$$
  Spin(7)/G_2 \;\simeq\; S^7
  \,.
$$

=--

(e.g [Varadarajan 01, Theorem 3](#Varadarajan01))

### Coset quotients

[[!include coset space structure on n-spheres -- table]]


### $G$-Structure and exceptional geometry

[[!include Spin(8)-subgroups and reductions -- table]]

### Relation to higher prequantum geometry

The 3-form $\omega$ from def. \ref{As2PlectomorphismsOnR7} we may regard as equipping $\mathbb{R}^7$ with [[n-plectic geometry|2-plectic structure]]. From this point of view $G_2$ is the linear subgroup of the [[2-plectomorphism group]], hence (up to the translations) the image of the [[Heisenberg group]] of $(\mathbb{R}^7, \omega)$ in the symplectomorphism group.

Or, dually, we may regard the 4-form $\star \omega$ of def. \ref{As2PlectomorphismsOnR7} as being a [[n-plectic geometry|3-plectic structure]] and $G_2$ correspondingly as the linear part in the [[3-plectomorphism group]] of $\mathbb{R}^7$.

### As zero-divisors of the sedenions

It is shown in Corollary 2.14 of [Moreno (1997)](#Moreno97) that the unit-norm [[zero-divisor|zero-divisors]] of the [[sedenion|sedenions]] is isomorphic to $G_2$. (More precisely, the smooth manifold $\{(p, q) \mid p q = 0, |p| = |q| = 1\}$ is diffeomorphic to $G_2$. This can also be improved to an isomorphism of $G_2$-torsors.)

## Related concepts

* [[G₂ manifold]], [[generalized G₂-manifold]]

* [[M-theory on G₂-manifolds]], [[G₂-MSSM]]

* **G₂**, [[F₄]],

  [[E₆]], [[E₇]], [[E₈]], [[E₉]], [[E₁₀]], [[E₁₁]], $\cdots$


[[!include special holonomy table]]

## References

### General

* {#SpringerVeltkamp00} [[Tonny Springer]], [[Ferdinand Veldkamp]], chapter 2 of _Octonions, Jordan Algebras, and Exceptional Groups_, Springer Monographs in Mathematics, 2000

Surveys are in

* Spiro Karigiannis, _What is... a $G_2$-manifold_ ([pdf](http://www.ams.org/notices/201104/rtx110400580p.pdf))

* [[Simon Salamon]], _A tour of exceptional geometry_, ([pdf](http://calvino.polito.it/~salamon/G/COR/tour.pdf))

* Wikipedia, _[G₂](http://en.wikipedia.org/wiki/G2_%28mathematics%29)_ .

The definitions are reviewed for instance in 

* {#Joyce96} [[Dominic Joyce]], _Compact Riemannian 7-manifolds with holonomy $G_2$_, Journal of Differential Geometry **43** 2 (1996) &lbrack;[doi:10.4310/jdg/1214458109](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-43/issue-2/Compact-Riemannian-7-manifolds-with-holonomy-G_2-I/10.4310/jdg/1214458109.full), [pdf](http://www.intlpress.com/JDG/archive/1996/43-2-291.pdf)&rbrack;
 
* {#Ferolito} Ferolito _The octonions and $G_2$_ ([pdf](https://www2.bc.edu/~reederma/Ferolito.pdf))

* {#Baez} [[John Baez]], section 4.1 _[G2](http://math.ucr.edu/home/baez/octonions/node14.html)_ of: _The Octonions_ ([arXiv:math/0105155](http://arxiv.org/abs/math/0105155))

* Ruben Arenas, _Constructing a Matrix Representation of the Lie Group $G_2$_, 2005 ([pdf](https://www.math.hmc.edu/seniorthesis/archives/2005/rarenas/rarenas-2005-thesis.pdf))

Discussion in terms of the [[Heisenberg group]] in [[2-plectic geometry]] is in 

* {#Ibort} Alberto Ibort, _Multisymplectic geometry: generic and exceptional_, _[Proceedings of the IX Fall workshop on geometry and physics](http://rsme.es/public/publi3.htm)_ ([[IbortMultisymplectic.pdf:file]])
 

A description of the root space decomposition of the [[Lie algebra]] $\mathfrak{g}_2$ is in

* {#Basak17} Tathagata Basak, _Root space decomposition of $\mathfrak{g}_2$ from octonions_, arXiv:[1708.02367](https://arxiv.org/abs/1708.02367)

As the group of [[zero-divisor|zero divisors]] of the [[sedenion|sedenions]]

* {#Moreno97} Guillermo Moreno. *The zero divisors of the Cayley-Dickson algebras over the real numbers*. (1997) ([doi](https://arxiv.org/abs/q-alg/9710013))



Cohomological properties are discussed in 

* Younggi Choi, _Homology of the gauge group of exceptional Lie group $G_2$_, J. Korean Math. Soc. 45 (2008), No. 3, pp. 699&#8211;709 

Discussion of [[subgroups]] includes

* {#Miyaoka93} [[Reiko Miyaoka]], _The linear isotropy group of $G_2/SO(4)$, the Hopf fibering and isoparametric hypersurfaces_, Osaka J. Math. Volume 30, Number 2 (1993), 179-202. ([Euclid](http://projecteuclid.org/euclid.ojm/1200784357))

* {#Ishiguro} Kenshi Ishiguro, _Classifying spaces and a subgroup of the exceptional Lie group $G_2$_ [pdf](http://hopf.math.purdue.edu/Ishiguro/G2.pdf)

* {#Kramer02} Linus Kramer, 4.27 of _Homogeneous Spaces, Tits Buildings, and Isoparametric Hypersurfaces_, AMS 2002

Discussion of $G_2$ as a subgroup of [[Spin(7)]]:

* {#Varadarajan01} [[Veeravalli Varadarajan]], _Spin(7)-subgroups of SO(8) and Spin(8)_, Expositiones Mathematicae, 19 (2001): 163-177 ([pdf](https://core.ac.uk/download/pdf/81114499.pdf))


### Applications in physics

Discussion of [[Yang-Mills theory]] with $G_2$ as [[gauge group]] is in 

* Ernst-Michael Ilgenfritz, Axel Maas, _Topological aspects of $G_2$ Yang-Mills theory_ ([arXiv:1210.5963](http://arxiv.org/abs/1210.5963))

[[!redirects G2]]