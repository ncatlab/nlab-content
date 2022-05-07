
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Exceptional structures
+-- {: .hide}
[[!include exceptional structures -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


Moonshine usually refers to the mysterious connections between the [[Monster simple group]] and the modular function $j$, the [[j-invariant]]. There were a bunch of [[conjectures]] about this connection that were proved by [[Richard Borcherds]], en passant mentioning the existence of the [[Moonshine vertex algebra]] (constructed then later in [FLM 89](#FrenkelLepowskiMeurman89)). Nowadays there is also Moonshine for other simple groups, by the work of J. Duncan. Eventually there should be an entry for the general moonshine phenomenon.

The whole idea of moonshine began with [[John McKay]]'s observation that the [[Monster group]]'s first nontrivial [[irreducible representation]] has [[dimension]] 196883, and the [[j-invariant]] $j(\tau)$ has the [[Fourier series]] expansion
$$
  j(\tau) = q^{-1} + 744 + 196884q + 21493760q^{2} + \dots
$$
where $q=\exp(i2\pi\tau)$, and famously 196883+1=196884. Thompson observed in (1979) that the other coefficients are obtained from the dimensions of Monster's irreducible representations. 

But the monster was merely _conjectured_ to exist until Griess (1982) explicitly constructed it. The construction is horribly complicated (take the sum of three irreducible representations for the [[centralizer]] of an [[involution]] of...). 

[Frenkel-Lepowski-Meurman 89](#FrenkelLepowskiMeurman89) constructed an infinite-dimensional [[module]] for the [[Monster vertex algebra]]. This is by a generalized [[Kac-Moody algebra]] via [[bosonic string theory]] and the [[Goddard-Thorn theorem|Goddard-Thorn "No Ghost" theorem]]. The [[Monster group]] acts naturally on this "Moonshine Module" (denoted by $V\natural$). 

To cut the story short, we end up getting from the Monster group to a module it acts on which is related to "modular stuff" (namely, the modular [[j-invariant]]). The idea [[Terry Gannon]] pitches is that Moonshine is a generalization of this association, it's a sort of "mapping" from "Algebraic gadgets" to "Modular stuff". 

## Automorphism groups of vertex operator algebras
 {#AutomorphismGroupsOfVertexOperatorAlgebras}

Realizations of [[sporadic finite simple groups]] as [[automorphism groups of vertex operator algebras]] in [[heterotic string theory]] and [[type II string theory]] (mostly on [[K3-surfaces]], see [[HET - II duality]]):


* The [[Conway group]] $Co_{0}$ is the [[automorphism group|group of]] [[automorphisms of a super VOA]] of the unique chiral [[number of supersymmetries|N=1]] [[super vertex operator algebra]] of [[central charge]] $c = 12$ without fields of [[conformal weight]] $1/2$

  ([Duncan 05](#Duncan05), see also [Paquette-Persson-Volpato 17, p. 9](#PaquettePerssonVolpato17))

* similarly, there is a super VOA, the _[[Monster vertex operator algebra]]_, whose [[automorphism group|group of]] of [[automorphisms of a VOA]] is the [[monster group]] 

  ([Frenkel-Lepowski-Meurman 89](#FrenkelLepowskiMeurman89), [Griess-Lam 11](#GriessLam11))


## Related concepts

* [[Monster]]

* moonshine

  * [[Mathieu moonshine]]

  * [[umbral moonshine]]

  * [[O'Nan moonshine]]

* [[automorphism of a vertex operator algebra]]




## References

### General

* [[Richard Borcherds]], _What is Moonshine?,
 Proceedings of the International Congress of Mathematicians, Vol. I (Berlin, 1998).
_Doc. Math._ 1998, Extra Vol. I, 607&#8211;615 (electronic). [MR1660657](http://www.ams.org/mathscinet-getitem?mr=1660657) [arXiv:math/9809110v1](http://arxiv.org/abs/math/9809110) [math.QA]

* John F. R. Duncan, Michael J. Griffin, Ken Ono, _Moonshine_ ([arXiv:1411.6571](http://arxiv.org/abs/1411.6571))

* {#GriessLam11} [[Robert Griess]] Jr., Ching Hung Lam, _A new existence proof of the Monster by VOA theory_ ([arXiv:1103.1414](https://arxiv.org/abs/1103.1414))

* {#FrenkelLepowskiMeurman89} [[Igor Frenkel]], [[James Lepowsky]], Arne Meurman, _Vertex operator algebras and the monster_, Pure and Applied Mathematics __134__, Academic Press, New York 1989. liv+508 pp. [MR0996026](http://www.ams.org/mathscinet-getitem?mr=996026)

* [[Terry Gannon]], *Monstrous moonshine: the first twenty-five years*, _Bull. London Math. Soc._ **38** (2006), no. 1, 1&#8211;33.  [MR2201600](http://www.ams.org/mathscinet-getitem?mr=2201600) [arXiv:math/0402345](http://arxiv.org/abs/math/0402345) [math.QA]

* [[Terry Gannon]], _Moonshine beyond the Monster: The Bridge Connecting Algebra, Modular Forms and Physics_, Cambridge Monographs on Mathematical Physics, Cambridge University Press, Cambridge, Massachusetts 2006. [MR2257727](http://www.ams.org/mathscinet-getitem?mr=2257727)

* Koichiro Harada, _"Moonshine" of finite groups_.
EMS Series of Lectures in Mathematics. European Mathematical Society (EMS), Z&#252;rich, 2010. viii+76 pp. [MR2722318](http://www.ams.org/mathscinet-getitem?mr=2722318)

* Griess, Robert L., Jr.; Lam, Ching Hung *A moonshine path from E8 to the Monster*, J. Pure Appl. Algebra_ 215 (2011), no. 5, 927&#8211;948 [MR2747229](http://www.ams.org/mathscinet-getitem?mr=2747229) [arXiv:0910.2057v2](http://arxiv.org/abs/0910.2057v2) [math.GR]

* Jae-Hyun Yang "Kac-Moody algebras, the Monstrous Moonshine, Jacobi forms and infinite products." _Number theory, geometry and related topics_ (Iksan City, 1995), 13&#8211;82, Pyungsan Inst. Math. Sci., Seoul, 1996. [MR1404967](http://www.ams.org/mathscinet-getitem?mr=1404967) [arXiv:math/0612474v2](http://arxiv.org/abs/math/0612474) [math.NT]

* Vassilis Anagiannis, [[Miranda Cheng]], _TASI Lectures on Moonshine_ ([arXiv:1807.00723](https://arxiv.org/abs/1807.00723))

### Historical References 

* [[John Conway]] and Simon Norton, "Monstrous moonshine." _Bull. London Math. Soc._ **11** (1979), no. 3, 308--339; [MR0554399](http://www.ams.org/mathscinet-getitem?mr=554399) (81j:20028)

* {#FrenkelLepowskiMeurman89} [[Igor Frenkel]], [[James Lepowsky]], Arne Meurman, "A natural representation of the Fischer-Griess Monster with the modular function $J$ as character." _Proc. Nat. Acad. Sci. U.S.A._ **81** (1984), no. 10, Phys. Sci., 3256--3260. [MR0747596](http://www.ams.org/mathscinet-getitem?mr=747596) (85e:20018)

* [[Robert Griess]], "The friendly giant." _Invent. Math._ **69** (1982), no. 1, 1--102. [MR671653](http://www.ams.org/mathscinet-getitem?mr=671653) (84m:20024)

* John G. Thompson, "Some numerology between the Fischer-Griess Monster and the elliptic modular function." _Bull. London Math. Soc._ **11** (1979), no. 3, 352--353. [MR0554402](http://www.ams.org/mathscinet-getitem?mr=554402) (81j:20030)

### Further developments
 {#FurtherDevelomentsReferences}

* [[Miranda Cheng]], John F. R. Duncan, Jeffrey A. Harvey, _Umbral Moonshine_ ([arXiv:1204.2779](http://arxiv.org/abs/1204.2779))

* John F. R. Duncan, Michael J. Griffin and Ken Ono, _Proof of the Umbral Moonshine Conjecture_ ([arXiv:1503.01472](http://arxiv.org/abs/1503.01472))

* [[Scott Carnahan]], _Monstrous Moonshine over Z?_ ([arXiv:1804.04161](https://arxiv.org/abs/1804.04161))


### Realization in superstring theory

Discussion of possible realizations in [[superstring theory]] (specifically [[heterotic string theory]] and [[type II string theory]] in [[K3-surfaces]], see [[HET - II]]) via [[automorphisms of super vertex operator algebras]]:

* S. Chaudhuri, D.A. Lowe, _Monstrous String-String Duality_, Nucl. Phys. B469 : 21-36, 1996 ([arXiv:hep-th/9512226](https://arxiv.org/abs/hep-th/9512226))

* {#Duncan05} John F. Duncan, _Super-moonshine for Conway's largest sporadic group_ ([arXiv:math/0502267](https://arxiv.org/abs/math/0502267))


* {#PaquettePerssonVolpato16} [[Natalie Paquette]], Daniel Persson, Roberto Volpato, _Monstrous BPS-Algebras and the Superstring Origin of Moonshine_ ([arXiv:1601.05412](http://arxiv.org/abs/1601.05412))

* {#KachruPaquetteVolpato16} [[Shamit Kachru]], [[Natalie Paquette]], Roberto Volpato, _3D String Theory and Umbral Moonshine_ ([arXiv:1603.07330](http://arxiv.org/abs/1603.07330))


* {#PaquettePerssonVolpato17} [[Natalie Paquette]], Daniel Persson, Roberto Volpato, _BPS Algebras, Genus Zero, and the Heterotic Monster_ ([arXiv:1701.05169](https://arxiv.org/abs/1701.05169))

* [[Shamit Kachru]], Arnav Tripathy, _The hidden symmetry of the heterotic string_ ([arXiv:1702.02572](https://arxiv.org/abs/1702.02572))

Specifically in relation to [[KK-compactifications]] of [[string theory]] on [[K3-surfaces]] ([[duality between heterotic and type II string theory]])

* {#ChengHarrisonVolpatoZimet16} [[Miranda Cheng]], Sarah M. Harrison, Roberto Volpato, Max Zimet, _K3 String Theory, Lattices and Moonshine_ ([arXiv:1612.04404](https://arxiv.org/abs/1612.04404), [doi:10.1007/s40687-018-0150-4](https://doi.org/10.1007/s40687-018-0150-4))

Possible relation to [[bosonic M-theory]]:

* [[Alessio Marrani]], [[Michael Rios]], [[David Chester]], _Monstrous M-theory_ ([arXiv:2008.06742](https://arxiv.org/abs/2008.06742))




[[!redirects moonshine]]
[[!redirects monstrous moonshine]]

[[!redirects Moonshine vertex algebra]]
[[!redirects moonshine vertex algebra]]

[[!redirects Moonshine vertex algebras]]
[[!redirects moonshine vertex algebras]]