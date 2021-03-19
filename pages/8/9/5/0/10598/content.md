
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The concept of _$G$-CW  complex_ is to that of [[CW-complexes]] as [[topological G-spaces]] are to [[topological spaces]]: for $G$ a [[compact topological group]], the notion of _$G$-CW-complex_ is much like that of [[CW-complex]], only that where in the latter case one builds a [[topological space]] from gluing of [[disks]] $D^n$ ("[[cell complex|cells]]") for a $G$-CW-complex one glues [[products]] of [[disks]] with $G$-[[orbits]] $G/H$ ([[coset spaces]]) for [[compact Lie group|compact]] [[subgroups]] $H$.

These are cofibrant spaces used in $G$-[[equivariant homotopy theory]].

## Examples

### $G$-Manifolds
  {#GManifolds}

The _[[equivariant triangulation theorem]] says that
if a [[compact Lie group]] $G$ acts on a [[compact topological space|compact]] [[smooth manifold]] $X$, then the manifold admits an [[equivariant triangulation]]. In particular it thus has the structure of a G-CW complex. 

([Illman 83, theorem 7.1, corollary 7.2](#Illman83)) Recalled as ([ALR 07, theorem 3.2](#ALR07)). See also [Waner 80, p. 6](#Waner80) who attributes this to [Matumoto 71](#Matumoto71)

Moreover, if the manifold does have a [[manifold with boundary|boundary]], then its G-CW complex may be chosen such that the boundary is a G-subcomplex. ([Illman 83, last sentence above theorem 7.1](#Illman83))

In particular:

+-- {: .num_prop #RepresentationSpheresAreGCWComplexes}
###### Proposition
**([[G-representation spheres are G-CW-complexes]])**

For $G$ a [[compact Lie group]] (e.g. a [[finite group]]) and $V \in RO(G)$ a [[finite dimensional vector space|finite-dimensional]] [[orthogonal group|orthogonal]] $G$-[[linear representation]], the [[representation sphere]] $S^V$ admits the structure of a [[G-CW-complex]].

=--


## Properties

### Equivariant cellular approximation

See at _[[equivariant cellular approximation theorem]]_.

### Equivariant CW-approximation

See at _[[G-CW approximation]]_.

### Equivariant Whitehead theorem

See at _[[equivariant Whitehead theorem]]_.

### Elmendorf's theorem

See at _[[Elmendorf's theorem]]_.


## References

The notion of G-CW complexes is, for the case of [[finite groups]] $G$, due to

* {#Bredon67b} [[Glen Bredon]], Section I.1. of _[[Equivariant cohomology theories]]_, Springer Lecture Notes in Mathematics Vol. 34. 1967 ([doi:10.1007/BFb0082690](https://link.springer.com/book/10.1007/BFb0082690))

announced in

* {#Bredon67a} [[Glen Bredon]], _Equivariant cohomology theories_, Bull. Amer. Math. Soc. Volume 73, Number 2 (1967), 266-268. ([educlid:1183528794](https://projecteuclid.org/euclid.bams/1183528794))

In the broader generality of general [[topological groups]] and specifically of [[compact Lie groups]], the nition of G-CW-complexes and their [[equivariant Whitehead theorem]] is due to:

* {#Matumoto71} [[Takao Matumoto]], _On $G$-CW complexes and a theorem of JHC Whitehead_, J. Fac. Sci. Univ. Tokyo Sect. IA 18, 363-374, 1971 ([[matumoto.pdf:file]])

*  [[Takao Matumoto]], _Equivariant K-theory and Fredholm operators_, J. Fac. Sci. Tokyo 18 (1971/72), 109-112 ([pdf](https://repository.dl.itc.u-tokyo.ac.jp/?action=repository_action_common_download&item_id=39826&item_no=1&attribute_id=19&file_no=1), [[MatumotoEquivariantKTheory.pdf:file]])

(Which, in hindsight and with [[Elmendorf's theorem]], gives a deeper justification for the parametrization over the [[orbit category]] already proposed in [Bredon 67a](#Bredon67a), [Bredon 67b](#Bredon67b).)

* {#Waner80} [[Stefan Waner]], _Equivariant Homotopy Theory and Milnor's Theorem_, Transactions of the American Mathematical Society Vol. 258, No. 2 (Apr., 1980), pp. 351-368 ([JSTOR](http://www.jstor.org/stable/1998061))

Proof that $G$-[[absolute neighbourhood retract|ANRs]] have the [[equivariant homotopy type]] of [[G-CW-complexes]] (for $G$ a [[compact Lie group]]):

* {#Kwasik81} [[Slawomir Kwasik]], _On the Equivariant Homotopy Type of $G$-ANR's_, Proceedings of the American Mathematical Society Vol. 83, No. 1 (Sep., 1981), pp. 193-194 (2 pages) ([jstor:2043921](https://www.jstor.org/stable/2043921))

Textbook accounts:

* {#tomDieck87} [[Tammo tom Dieck]], Sections I.1, I.2 of: _[[Transformation Groups]]_, de Gruyter 1987  ([doi:10.1515/9783110858372]( https://doi.org/10.1515/9783110858372))

* {#Lueck89} [[Wolfgang Lück]], Sections I.1, I.2 of: _Transformation Groups and Algebraic K-Theory_, Lecture Notes in Mathematics **1408** (Springer 1989) ([doi:10.1007/BFb0083681](https://doi.org/10.1007/BFb0083681))

* {#May96} [[Peter May]] et al., Section I.3 of:  _Equivariant homotopy and cohomology theory_, CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996 ([ISBN: 978-0-8218-0319-6](https://bookstore.ams.org/cbms-91/?startBookmarkIdx=200)  [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/alaska1.pdf), [[MayEtAlEquivariant96.pdf:file]])


Lecture notes:

* [[Jay Shah]], _Equivariant algebraic topology_, 2010 ([pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2010/REUPapers/Shah.pdf), [[ShahEquivariantAlgebraicTopology.pdf:file]])

* {#Blumberg17} [[Andrew Blumberg]], _Equivariant homotopy theory_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))






[[!redirects G-CW complexes]]

[[!redirects G-CW-complex]]
[[!redirects G-CW-complexes]]

[[!redirects G-cell complex]]
[[!redirects G-cell complexes]]
