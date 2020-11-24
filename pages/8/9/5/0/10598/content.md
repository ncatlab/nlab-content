
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

### Elmendorf's theorem

The collection of $G$-CW-complexes has a [[full sub-(infinity,1)-category|full embedding]] into the [[(infinity,1)-presheaves]] on the [[orbit category]] $Orb(G)$.  This is given by sending a $G$-CW complex, $Y$, to the presheaf sending $G/H$ to $Y^H$, the subspace of $Y$ fixed by $H$.

See at _[[Elmendorf's theorem]]_.

## References

Good lecture notes are

* {#Blumberg17} [[Andrew Blumberg]], _Equivariant homotopy theory_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))


A standard reference is

* {#May96} [[Peter May]], sections I.3 of _Equivariant homotopy and cohomology theory_ CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996. With contributions by M. Cole, G. Comezana, S. Costenoble, A. D. Elmenddorf, J. P. C. Greenlees, L. G. Lewis, Jr., R. J. Piacenza, G. Triantafillou, and S. Waner. ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/alaska1.pdf))

  Section X.2 there discusses the generalization to [[RO(G)-grading]].

See also


* {#Matumoto71} T. Matumoto, _Equivariant K-theory and Fredholm operators, J. Fac. Sci. Tokyo 18 (1971/72), 109-112 ([jairo](http://jairo.nii.ac.jp/0021/00002586/en))


* {#Waner80} [[Stefan Waner]], _Equivariant Homotopy Theory and Milnor's Theorem_, Transactions of the American Mathematical Society Vol. 258, No. 2 (Apr., 1980), pp. 351-368 ([JSTOR](http://www.jstor.org/stable/1998061))


* Jay Shah, _Equivariant algebraic topology_, [pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2010/REUPapers/Shah.pdf)

* {#Illman83} [[Sören Illman]], _The equivariant triangulation theorem for actions of compact Lie groups_, Math. Ann. 262 (1983), no. 4, 487&#8211;501 ([web](http://gdz.sub.uni-goettingen.de/dms/load/img/?PID=GDZPPN002323249))

* {#ALR07} A. Adem, J. Leida and Y. Ruan, _Orbifolds and Stringy Topology_, Cambridge Tracts in Mathematics **171** (2007) ([pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/Ruan.pdf))

* {#ALR07} A. Adem, J. Leida and Y. Ruan, _Orbifolds and Stringy Topology_, Cambridge Tracts in Mathematics **171** (2007) ([pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/Ruan.pdf))


[[!redirects G-CW complexes]]

[[!redirects G-CW-complex]]
[[!redirects G-CW-complexes]]

[[!redirects G-cell complex]]
[[!redirects G-cell complexes]]
