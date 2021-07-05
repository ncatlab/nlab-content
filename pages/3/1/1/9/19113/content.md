

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

By a _finite rotation group_ one means a [[finite]] [[subgroup]] of a [[group]] of [[rotations]], hence of a [[special orthogonal group]] $SO(n)$ or [[spin group]] $Spin(n)$ or similar. 

The finite subgroups of [[SO(3)]] and [[SU(2)]] follow an [[ADE classification]] (theorem \ref{ClassificationOfFiniteSubgroupsOfSO3} below).



## Classifcations

### Finite subgroups of $O(3)$, $SO(3)$ and $Spin(3)$

+-- {: .num_theorem #ClassificationOfFiniteSubgroupsOfSO3}
###### Theorem
**([[ADE classification]] of [[finite group|finite]] [[subgroups]] of [[SO(3)]] and [[spin group|Spin(3)]]$\simeq$ [[SU(2)]])**

The [[finite group|finite]] [[subgroups]] of the [[special orthogonal group]] $SO(3)$ as well as the [[finite group|finite]] [[subgroups]] of the [[special unitary group]] [[SU(2)]] are, up to [[conjugation]], given by the following classification:

[[!include ADE -- table]]


Here under the [[double cover]] projection (using the [exceptional isomorphism](spin+group#ExceptionalIsomorphisms) $SU(2) \simeq Spin(3)$)

$$
  SU(2) \simeq Spin(3) \overset{\pi}{\longrightarrow} SO(3)
$$

all the finite subgroups of $SU(2)$ except the [[odd number|odd]]-[[order of a group|order]] [[cyclic groups]] are the [[preimages]] of the corresponding finite subgroups of $SO(3)$, in that we have [[pullback]] [[diagrams]]

$$
  \array{
    \left\langle
     \exp
     \left(
       \pi \mathrm{i} \tfrac{1}{n} 
     \right)
    \right\rangle
    &
    =
    &
    \mathbb{Z}/(2n)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Spin(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Spin(3)
    \\
    &&
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow^{ \mathrlap{\pi} }
    \\
    \left\langle
     Ad_{
     \exp
     \left(
       \pi \mathrm{i} \tfrac{1}{n} 
     \right)
     }
    \right\rangle
    &
    =
    &
    \mathbb{Z}/n
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(3)    
  }
$$

exhibiting the [[even number|even]] [[order of a group|order]] [[cyclic groups]] as subgroups of [[Spin(2)]], including the minimal case of the [[group of order 2]]

$$
  \array{
    \left\langle
     \exp
     \left(
       \pi \mathrm{i}
     \right)
     =
     -1
    \right\rangle
    &
    =
    &
    \mathbb{Z}/2
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Spin(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Spin(3)
    \\
    &&
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow^{ \mathrlap{\pi} }
    \\
    \left\langle
     Ad_{
     \exp
     \left(
       \pi \mathrm{i} 
     \right)
     }
     =
     e
    \right\rangle
    &
    =
    &
    1
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(3)    
  }
$$


as well as

$$
  \array{
    \left\langle
      \exp\left( \pi \mathrm{i} \tfrac{1}{n} \right), \, \mathrm{j} 
    \right\rangle
    &=&
    2 D_{2n}
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Pin_-(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Spin(3)
    \\
    &&
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow^{ \mathrlap{\pi} }
    \\
    \left\langle
      Ad_{\exp\left( \pi \mathrm{i} \tfrac{1}{n}  \right) }, 
      \, 
      Ad_{\mathrm{j}} 
    \right\rangle
    &&
    D_{2n}
    &\overset{\phantom{AA}}{\hookrightarrow}&
    O(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(3)    
  }
$$

exhibiting the [[binary dihedral groups]] as sitting inside the [[Pin(2)]]-[[subgroup]] of [[Spin(3)]],

but only [[commuting diagrams]]

$$
  \array{
    \left\langle
     \exp
     \left(
       2 \pi \mathrm{i} \tfrac{1}{{2n+1}} 
     \right)
    \right\rangle
    &
    =
    &
    \mathbb{Z}/(2n+1)
    &&\overset{\phantom{AA}}{\hookrightarrow}&&
    Spin(3)
    \\
    &&
    \big\downarrow
      &&
      &&
    \big\downarrow^{ \mathrlap{\pi} }
    \\
    \left\langle
     Ad_{
     \exp
     \left(
       2 \pi \mathrm{i} \tfrac{1}{2n+1} 
     \right)
     }
    \right\rangle
    &
    =
    &
    \mathbb{Z}/(2n+1)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(3)    
  }
$$

for the [[odd number|odd]] [[order of a group|order]] [[cyclic group|cyclic]] [[subgroups]].

=--

This goes back to ([Klein 1884, chapter I](#Klein1884)). 
Full proof for $SO(3)$ is spelled out for instance in ([Rees 05, theorem 11](#Rees05), [De Visscher 11](#DeVisscher11)). The proof for the case of $SL(2,\mathbb{C})$ is spelled out in ([Miller-Blichfeldt-Dickson 16](#MillerBlichfeldtDickson16)) reviewed in ([Serrano 14, section 2](#Serrano14)). The proof of the case for $SU(2)$ given the result for $SO(3)$ is spelled out in [Keenan 03, theorem 4](#Keenan03).




### Finite subgroups of $O(4)$, [[SO(4)]] and [[Spin(4)]]
  {#FiniteSubgroupsOfO4}

For classification of the finite subgroups of $O(4)$ see ([duVal 65](#DuVal65), [Conway-Smith 03](#ConwaySmith03))

For finite subgroups of [[Spin(4)]]: [MFF 12, appendix B](#MFF12).

In this classification, the [[symmetry group]] of the [[120-cell]] and hence that of the [[600-cell]] is the [[quotient group]] $(2 I \times 2 I)/\mathbb{Z}_2$  by the [[cyclic group of order 2]] of the [[direct product group]] of two copies of the [[binary icosahedral group]] ([SadocMosseri 89, p. 172](#SadocMosseri89), see [MFF 12, table 16](#MFF12)).






### Finite subgroups of $O(5)$

For classification of the finite subgroups of $O(5)$ see [Mecchia-Zimmermann 10](#MecchiaZimmermann10)


## Properties

### Subgroup lattice
 {#SubgroupLattice}

The [[subgroup]] [[lattice]] of [[SU(2)]] under the three exceptional [[finite group|finite]] subgroups [[2T]], [[2O]], [[2I]] (from Theorem \ref{ClassificationOfFiniteSubgroupsOfSO3}) looks as follows:

<center>
<img src="https://ncatlab.org/nlab/files/ADESubgroupLatticeUnderExceptional.jpg" width="490"/>
</center>

This is obtained from the subgroup lattice as shown on [GroupNames](https://people.maths.bris.ac.uk/~matyd/GroupNames/) for 
$2I \simeq$ <a href="https://people.maths.bris.ac.uk/~matyd/GroupNames/97/SL(2,5).html">SL(2,5)</a> and  $2O \simeq $ <a href="https://people.maths.bris.ac.uk/~matyd/GroupNames/1/CSU(2,3).html">CSU(2,3)</a>

See also [Goncalves-Guaschi 11, appendix](#GoncalvesGuaschi11).


### Group cohomology
 {#GroupCohomology}

+-- {: .num_prop #GroupCohomologyOfFiniteSubgroupsOfSU2}
###### Proposition
**([[group cohomology]] of [[finite subgroups of SU(2)]])

Let $G_{ADE}$ be a [[finite subgroup of SU(2)]]. Then its [[group cohomology]] with [[integer]] [[coefficients]] is as follows:

$$
  H^n_{grp}(G_{ADE}, \mathbb{Z})
  \;\simeq\;
  \left\{
  \array{
    \mathbb{Z} &\vert& n = 0
    \\
    G_{ADE}^{ab} &\vert&  n = 2 \, mod \, 4
    \\
    \mathbb{Z}/{\vert G_{ADE}\vert} &\vert& n \, \text{positive multiple of} \, 4
    \\
    0 &\vert& \text{otherwise} 
  }
  \right.
$$

Here $G_{ADE}^{ab}$ denotes the [[abelianization]]  of $G_{ADE}$ and $\vert G_{ADE}\vert$ its [[cardinality]], hence $\mathbb{Z}/{\vert G_{ADE}\vert}$ the [[cyclic group]] whose [[order of a group|order]] is the cardinality of $G_{ADE}$.

The [[group homology]] with [[integer]] [[coefficients]] is

$$
  H_n^{grp}(G_{ADE}, \mathbb{Z})
  \;\simeq\;
  \left\{
  \array{
    \mathbb{Z} &\vert& n = 0
    \\
    G^{ab}_{ADE} &\vert&  n = 1 \, mod \, 4
    \\
    \mathbb{Z}/{\vert G_{ADE}\vert} &\vert& n= 3 \,mod\, 4
    \\
    0 &\vert& \text{otherwise} 
  }
  \right.
$$


=--


([Tomoda & Zvengrowski 08](#TomodaZvengrowski08), [Epa & Ganter 16, p. 12](#EpaGanter16), see also [FHHP 01, Cor. 3.1](#FHHP01))

+-- {: .num_remark #DiscreteTorsion} 
###### Remark
**([[C-field]] [[discrete torsion]])**

In discussion of [[11-dimensional supergravity]] on [[spacetimes]] with [[ADE-singularities]], the special case 

$$
  \underset{
    \simeq H^3( \mathbb{C}^4 \sslash G_{ADE}, U(1))
  }{
  \underbrace{
    H^4_{grp}(G_{ADE}, \mathbb{Z}) 
  }}
   \;\simeq\;
  \mathbb{Z}/{\vert G_{ADE} \vert }
$$

of Prop. \ref{GroupCohomologyOfFiniteSubgroupsOfSU2}, regarded as expressing [[orbifold cohomology]] of an [[ADE singularity]], as shown under the brace, witnesses the possible [[torsion subgroup|torsion]] [[supergravity C-field]] [[flux]] of [[M5-branes]] [[wrapped brane|wrapped]] on torsion homology 3-cycles ("[[discrete torsion]]", see [Aharony-Bergman-Jafferis 08, p. 8](discrete+torsion#AharonyBergmanJafferis08) and [BDHKMMS 01, section 4.6.2](discrete+torsion#BDHKMMS01)).

See also at _[[Platonic 2-group]] -- [Relation to String 2-group](Platonic+2-group#RelationToTheString2Group)_.


=--


## Related concepts

* [[regular polytope]], [[regular polyhedron]]

* [[ADE singularity]]

* [[McKay correspondence]]

* [[Platonic 2-group]]

* [[wallpaper group]]

## References
  {#References}

### Finite subgroups of $SO(3)$ and $Spin(3)$

The classification in Theorem \ref{ClassificationOfFiniteSubgroupsOfSO3} goes back to

* {#Klein1884} [[Felix Klein]], chapter I of _Vorlesungen über das Ikosaeder und die Auflösung der Gleichungen vom fünften Grade_, 1884, translated as _Lectures on the Icosahedron and the Resolution of Equations of Degree Five_ by George Morrice 1888, [online version](https://archive.org/details/cu31924059413439)

Textbook accounts:

* {#MillerBlichfeldtDickson16} G. A. Miller, H. F. Blichfeldt, L. E. Dickson, _Theory and applications of finite groups_, Dover, New York, 1916

* {#Lamotke86} [[Klaus Lamotke]], _Regular Solids and Isolated Singularities_, Vieweg 1986

* {#Rees05} [[Elmer Rees]], _Notes on Geometry_, Springer 2005

see also 

* {#Serrano14} Javier Carrasco Serrano, _Finite subgroups of $SL(2,\mathbb{C})$ and $SL(3,\mathbb{C})$_, Warwick 2014 ([pdf](https://homepages.warwick.ac.uk/~masda/McKay/Carrasco_Project.pdf))


Complete proof of the classification of the finite subgroups of $SO(3)$ is also spelled out in 

* {#DeVisscher11} Maud De Visscher, _[Groups and Symmetry](http://www.staff.city.ac.uk/maud.devisscher.1/GS/)_ lecture notes handout: _Classification of finite rotation groups_  ([pdf](http://www.staff.city.ac.uk/maud.devisscher.1/GS/classif_rotation.pdf))

Based on the classification of the finite subgroups of $SO(3)$, full proof of that of the finite subgroups of $SU(2)$ is spelled out in

* {#Keenan03} [[Adam Keenan]], _Which finite groups act freely on spheres?_, 2003 ([pdf](http://www.math.utah.edu/~keenan/actions.pdf))

See also

* GroupProps _<a href="https://groupprops.subwiki.org/wiki/Classification_of_finite_subgroups_of_SO(3,R)">Classification of finite subgroups of SO(3,R)</a>

Discussion of the [[lattice]] of [[subgroups]] of the three exceptional subgroups is in 

* {#GoncalvesGuaschi11} Daciberg Lima Gonçalves, John Guaschi, _The Subgroups of the Binary Polyhedral Groups_, Appendix of _The classification of the virtually cyclic subgroups of the sphere braid groups_, Springer (Ed.) (2013) 112 ([arXiv:1110.6628](https://arxiv.org/abs/1110.6628), [pdf](https://link.springer.com/content/pdf/bbm%3A978-3-319-00257-6%2F1.pdf))

Discussion of the [[group cohomology]]:

* {#TomodaZvengrowski08} [[Satoshi Tomoda]], [[Peter Zvengrowski]], *Remarks on the cohomology of finite fundamental groups of 3-manifolds*, Geom. Topol. Monogr. 14 (2008) 519-556 ([arXiv:0904.1876](https://arxiv.org/abs/0904.1876))

see also

* {#FHHP01} [[Bo Feng]], [[Amihay Hanany]], [[Yang-Hui He]], Nikolaos Prezas, Cor. 3.1 in: *Discrete Torsion, Non-Abelian Orbifolds and the Schur Multiplier*, JHEP 0101:033, 2001 ([arXiv:hep-th/0010023](https://arxiv.org/abs/hep-th/0010023))


The [[universal higher central extension]] of finite subgroups of $SU(2)$ ("[[Platonic 2-groups]]") are discussed in

* {#EpaGanter16} [[Narthana Epa]], [[Nora Ganter]], _Platonic and alternating 2-groups_, Higher Structures 1(1):122-146, 2017 ([arXiv:1605.09192](http://arxiv.org/abs/1605.09192))

### Finite subgroups of $O(4)$

* {#DuVal65} [[Patrick du Val]], _Homographies, Quaternions and Rotations_, Oxford Mathematical Monographs, Clarendon Press (1964)

  also(?): Journal of the London Mathematical Society, Volume s1-40, Issue 1 (1965) ([doi:10.1112/jlms/s1-40.1.569b](https://doi.org/10.1112/jlms/s1-40.1.569b))

* {#ConwaySmith03} [[John Conway]], D. A. Smith, _On quaternions and octonions: their geometry, arithmetic and 
symmetry_ A K Peters Ltd., Natick, MA, 2003

* {#MFF12} [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], appendix B of _Half-BPS M2-brane orbifolds_, Adv. Theor. Math. Phys. Volume 16, Number 5 (2012), 1349-1408. ([arXiv:1007.4761](http://arxiv.org/abs/1007.4761), [Euclid](https://projecteuclid.org/euclid.atmp/1408561553))


* {#SadocMosseri89} J. F. Sadoc, R. Mosseri, _Icosahedral order, curved space and quasicrystals_, in Jaric, Gratias (eds.) _Extended icosahedral structures_, 1989 ([GoogleBooks](https://books.google.co.uk/books?id=HWyIUglWeXsC&pg=PA172&lpg=PA172#v=onepage&q&f=false))

### Finite subgroups of $O(5)$

* {#MecchiaZimmermann10} Mattia Mecchia, Bruno Zimmermann, _On finite groups acting on homology 4-spheres and finite subgroups of $SO(5)$_, Topology and its Applications 158.6 (2011): 741-747 ([arXiv:1001.3976](https://arxiv.org/abs/1001.3976))

[[!redirects finite rotation groups]]

[[!redirects classification of the finite rotation groups]]

[[!redirects finite subgroup of SO(3)]]
[[!redirects finite subgroups of SO(3)]]

[[!redirects finite subgroup of SU(2)]]
[[!redirects finite subgroups of SU(2)]]

[[!redirects finite subgroup of Spin(3)]]
[[!redirects finite subgroups of Spin(3)]]


[[!redirects finite subgroup of O(4)]]
[[!redirects finite subgroups of O(4)]]

[[!redirects finite subgroup of SO(4)]]
[[!redirects finite subgroups of SO(4)]]


[[!redirects finite subgroup of O(5)]]
[[!redirects finite subgroups of O(5)]]

[[!redirects finite subgroup of SO(5)]]
[[!redirects finite subgroups of SO(5)]]


[[!redirects classification of finite rotation groups]]
[[!redirects classifications of finite rotation groups]]

