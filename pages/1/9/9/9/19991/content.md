
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Solid state physics
+-- {: .hide}
[[!include solid state physics -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

Crystallographic groups (also: "space groups") are [[symmetry groups]] of [[crystals]].

The use of crystallographic groups for the study of [[crystals]] (e.g. [Hilton 1903](#Hilton03), [Engel 1986](crystal#Engel86)) is much in the spirit of [[Klein geometry]]/the [[Erlanger program]] (see for instance [Weyl 1938](Erlanger+program#Weyl38); [Grünbaum & Shephard 2010](Erlanger+program#GruenbaumShephard10)).

Concretely, the [[quotient space]]/[[quotient orbifold]] of the space of [[wave vectors]]/[[momenta]] in a [[crystal]] lattice by the (dual) [[crystallographic group]] is the [[Brillouin torus]](-[[orbifold]]), in terms of which most of [[condensed matter theory]] is formulated (see for instance the [[electron energy bands]], the [[valence bundle]], and the [[K-theory classification of topological phases]]).



## Definition

A **crystallographic group** or **space group** in [[dimension]] $n$  is a [[subgroup]] of the corresponding [[Euclidean group]], hence of the [[isometry group]] of [[Euclidean space]] $\mathbb{R}^n$, that contains a (maximal) [[lattice in a vector space|lattice]] in $\mathbb{R}^n$ as a [[subgroup]], and is contained within the [[automorphism group]] of that lattice. In other words, it is a subgroup of the automorphism group of the lattice that contains all the [[translations]] by elements of the lattice itself.

Equivalently, a crystallographic group on a [[Euclidean space]] $E$ is a [[discrete group|discrete]] [[subgroup]] $S \subset Iso(E)$ of the [[isometry group]] of $E$ (its [[Euclidean group]]) that contains a [[lattice (discrete subgroup)|lattice]] $N \subset E \subset Iso(E)$ of [[translation group|translations]] as a [[normal subgroup]] $N \subset S$, such that the corresponding [[quotient group]], called the _[[point group]]_ of the crystallographic group, is a subgroup $G \coloneqq S/N \;\subset\; O(E)$ of the [[orthogonal group]]. 

In short, a crystallographic groups is exhibited by an inclusion of [[short exact sequences]] of ([[nonabelian group|non-abelian]]) [[groups]], as follows:

\[
  \label{CrystallographicInclusionOfShortExactSequences}
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
\]

{#BieberbachTheorem} This transparent description of crystallographic groups is essentially the content of *[[Bieberbach's first theorem]]* (following [Bieberbach 1910](#Bieberbach1910), see [Farkas 1981, Thm. 14](#Farkas81), [Charlap 1986, Thm. I 3.1](#Charlap86), [Engel 1986, Thm. 3.1](#Engel86) for modern accounts and find a concise statement in [Tolcachier 19, Thm. 2.3](#Tolcachier19), also implicitly in [Freed-Moore 13, (0.2)](#FreedMoore13)). Historically, the earlier definition of "crystallographic group" (eg. [Farkas 81, Sec. 3](#Farkas81)) just required that it be any [[discrete group|discrete]] [[subgroup]] of $Iso(E)$ such that the resulting [[quotient space|quotient]] [[topological group]] be [[compact topological group|compact]]. Bieberbach's first theorem (or the statement now known under this name) says that this already implies 1. that the translation subgroup is a full lattice, and 2. that the point group is finite. 

If the crystallographic [[short exact sequence]] on the left of (eq:CrystallographicInclusionOfShortExactSequences) [[split exact sequence|splits]], hence if the space group $S \simeq G \ltimes N$ is the [[semidirect product]] of the [[point group]] with the translational lattice, then $S$ is called a **symmorphic space group**.

The [[conjugacy class]] of a crystallographic group (under [[conjugation]] by [[O(n)]]) represents the *[[Bravais lattice]]* of the corresponding crystal lattice.



## Properties

### Classification
 {#Classification}

In 2 [[dimensions]], there are precisely 17 crystallographic groups, which are distinct up to [[isomorphism]]; these are known as the _[[wallpaper groups]]_. 

In 3 dimensions, there are 219 distinct types, or 230 if chiral copies are considered distinct. The classification of space groups has been carried out up to 6 dimensions.

On the classification of symmorphic space groups see also [this MO comment](https://mathoverflow.net/q/77682/381).

From [Chuprunov-Kuntsevich 88](#ChuprunovKuntsevich88):

> Let us make a brief survey of the main achievements in the $n$-dimensional crystallography that have been amply covered in the literature on the subject [15-17]. When Fedorov and Schoenflies had completed the derivation of 230 space group types of crystals it was natural to consider a possibility of derivation of corresponding groups in higher dimensions. In 1911-12 Bieberbach and Frobenius developed a general theory of the group symmetry of the n-dimensional lattices and proved the existence of a finite number of nonisomorphous space groups in the n-dimensional Euclidean space with an arbitrary number of n. Basing on this general theory, in 1948 Zassenhaus suggested an algorithm to derive the n-dimensional space groups as extensions of the translation subgroups of these groups using point groups. About 1950 Hermann gave a complete description of the possible crystallographic symmetry operations in higher dimensions and discussed the lattices of maximal symmetry and their crystal classes. In 1951 Hurley found 222 geometric crystal classes in the four-dimensional Euclidean space making use of the 1889 work by Goursat who had enumerated the classes of finite groups of the real 4 × 4 matrixes. Later this number was corrected to 227. At present classification of crystallographic groups in the four-dimensional Euclidean space is completed in the main. A complete list of 4783 types of four-dimensional space groups was computed in 1973 and given in an excellent monograph ["Crystallographic groups of four- dimensional space" by Brown et al.](#BrownBulowNeubuserWondratschekZassenhaus78) [15]. These groups were derived on the base of the nine maximal arithmetic crystal classes, derived by Dade in 1965, which allowed one to determine all of the 710 four-dimensional arithmetic classes and to calculate the normalizers of finite groups of the unimodular 4 x 4 matrixes needed for the Zassenhaus algorithm. The monograph [15] is of interest not only by having a complete description of all classes of the four-dimensional crystallographic groups but also by taking a deeper approach to the system of classification of the n-dimensional crystallographic groups, as well as by giving characteristic properties of the four-dimensional crystallographic groups in comparison with that in lower dimensions. One of these properties is enantiomorphizm exhibited not only by the space group types but also by Bravais types of lattices, arithmetic classes and geometric classes. For the first time this phenomenon was found by Shtogrin [18]. 

> The n-dimensional mathematical crystallography is still in progess. Ryshkov [19] determined all maximal arithmetic crystal classes of five-dimensional Euclidean space. Some categories of five- and six-dimensional "small" groups isomorphic to the three-dimensional groups of symmetry, anti- symmetry, two-fold antisymmetry, p- and p'-symmetry were derived by Palistrant [20]. Some aspects of the mathematical theory applied to the n-dimensional crystallography were considered [15, 21].

### Compact flat orbifolds
 {#CompactFlatOrbifolds}

+-- {: .num_prop #InducedPointGroupActionOnTorus}
###### Proposition
**(induced point group action on torus)**

The assumption that the crystallographic translation group $N \subset S$ is a [[normal subgroup]]

$$
  1 \to N \longrightarrow S \longrightarrow G \to 1
$$

implies that the [[action]] of the [[point group]] $G = S/N$ descends to the [[torus]] [[quotient space]] $E/N$

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

=--

+-- {: .proof}
###### Proof

By the definition of [[quotient space]], the condition for this to be the case is that for all $x \in E$ we have $g(n(x)) = n'(g(x))$, or equivalently $g(n(g^{-1}(y))) = n'(y)$, which is implied by $N$ being a [[normal subgroup]]: $g N g^{-1} = N$.

=--

+-- {: .num_remark}
###### Remark

The further [[homotopy quotient]] $(E/N)\sslash G$ of the [[torus]] $E/N$ by this induced [[action]] of the [[point group]] $G$ is a [[compact topological space|compact]] [[flat orbifold]], and most compact flat orbifolds arise this way.

=--

## Related concepts

* [[symmetry group]]

* [[Brillouin torus]]

* [[Bravais lattice]]

* [[topological crystalline insulator]]

## References

Review:

* {#Hilton03} [[Harold Hilton]], *Mathematical crystallography and the theory of groups of movements*, Oxford Clarendon Press (1903) $[$[web](https://archive.org/details/mathematicalcry03hiltgoog/page/n6/mode/2up)$]$

* {#Engel86} [[Peter Engel]], *Geometric Crystallography -- An Axiomatic Introduction to Crystallography*, D. Reidel Publishing (1986) $[$[doi:10.1007/978-94-009-4760-3](https://doi.org/10.1007/978-94-009-4760-3)$]$


* [[Willard Miller]], Chapter 2 "The Crystallographic Groups" in : *Symmetry Groups and Their Applications*, Pure and Applied Mathematics **50** (1972) 16-60 $[$<a href="https://doi.org/10.1016/S0079-8169(08)60959-9">doi:10.1016/S0079-8169(08)60959-9</a>$]$

* {#BrownBulowNeubuserWondratschekZassenhaus78} H. Brown, R. Bülow, J. Neubüser, H. Wondratschek, H. Zassenhaus, _Crystallographic Groups of Four-Dimensional Space_, John Wiley, New York, 1978. 

* {#Farkas81} Daniel R. Farkas, _Crystallographic groups and their mathematics_, Rocky Mountain J. Math. Volume 11, Number 4 (1981), 511-552 ([doi:10.1216/RMJ-1981-11-4-511](https://projecteuclid.org/euclid.rmjm/1250128489))

* {#ChuprunovKuntsevich88} E. V. Chuprunov, T. S. Kuntsevich, _$n$-Dimensional space groups and regular point systems_, Comput. Math. Applic. Vol. 16, No. 5-8, pp. 537-543, 1988 (<a href="https://doi.org/10.1016/0898-1221(88)90243-X">doi:10.1016/0898-1221(88)90243-X</a>)

* D. Weigel, T. Phan and R. Veysseyre, _Crystallography, geometry and physics in higher dimensions. III. Geometrical symbols for the 227 crystallographic point groups in four-dimensional space_, Acta Cryst. (1987). A43, 294-304 ([doi:10.1107/S0108767387099367](https://doi.org/10.1107/S0108767387099367))

* {#FreedMoore13} [[Daniel Freed]], [[Gregory Moore]], _Twisted equivariant matter_, Ann. Henri Poincaré (2013) 14: 1927 ([arXiv:1208.5055](https://arxiv.org/abs/1208.5055))

* {#Tolcachier19} Alejandro Tolcachier, *Holonomy groups of compact flat solvmanifolds*, Geometriae Dedicata **209** (2020) 95–117  $[$[arXiv:1907.02021](https://arxiv.org/abs/1907.02021), [doi:10.1007/s10711-020-00524-8](https://doi.org/10.1007/s10711-020-00524-8)$]$

* [[GAP]] package, _The Crystallographic Groups Catalog_ ([web](http://www.math.rwth-aachen.de/~Greg.Gamble/gap4r3/pkg/crystcat/htm/CHAP001.htm))

Bieberbach's original articles:

* {#Bieberbach1910} [[Ludwig Bieberbach]], *Über die Bewegungsgruppen des $n$ dimensionalen Euklidischen Raumes mit einem endlichen Fundamentalbereich*, Nachrichten von der Gesellschaft der Wissenschaften zu Göttingen, Mathematisch-Physikalische Klasse (1910) 75-84 $[$[dml:58754](https://eudml.org/doc/58754)$]$

* {#Bieberbach1911} [[Ludwig Bieberbach]], *Über die Bewegungsgruppen der Euklidischen Räume (Erste Abhandlung)*, Mathematische Annalen **70** (1911) 297–336  $[$[doi:10.1007/BF01564500](https://doi.org/10.1007/BF01564500)$]$

* {#Bieberbach1912} [[Ludwig Bieberbach]], *Über die Bewegungsgruppen der Euklidischen Räume (ZweiteAbhandlung.) Die Gruppen mit einem endlichen Fundamentalbereich*, Mathematische Annalen  **72** (1912) 400-412 $[$[doi:10.1007/BF01456724]( https://doi.org/10.1007/BF01456724)$]$

A monograph on the topic:

* {#Charlap86} [[Leonard S. Charlap]], *Bieberbach Groups and Flat Manifolds*, Springer (1986) $[$[doi:10.1007/978-1-4613-8687-2](https://doi.org/10.1007/978-1-4613-8687-2)$]$

See also

* [[eom]], _[Crystallographic group](https://www.encyclopediaofmath.org/index.php/Crystallographic_group)_

* [[Groupprops]], _[Space group](https://groupprops.subwiki.org/wiki/Space_group)_

* Wikipedia, _[Space group](https://en.wikipedia.org/wiki/Space_group)_

* Wikipedia, _[Point group](https://en.wikipedia.org/wiki/Point_group)_


Further discussion:

* Chunxiao Liu, Weicheng Ye: *Crystallography, Group Cohomology, and Lieb-Schultz-Mattis Constraints* &lbrack;[arXiv:2410.03607](https://arxiv.org/abs/2410.03607)&rbrack;

On the [[quotient orbifold|quotient]] [[orbifolds]] of [[Euclidean spaces]] by crystallographic groups, for the purpose of [[crystallography]]:

* [[Carroll K. Johnson]], Michael N. Burnett, William D. Dunbar: *Crystallographic Topology and Its Applications*, in: *[Crystallographic Computing 7](https://www.iucr.org/resources/commissions/crystallographic-computing/schools/school96)* *Proceedings of the Macromolecular Crystallography Computing School* (1996) &lbrack;[pdf](https://www.iucr.org/__data/assets/pdf_file/0010/9001/cj.pdf), [[JohnsonEtAl-CrystallographicTopology.pdf:file]]&rbrack;

* [[Carroll K. Johnson]]: *Crystallographic Topology 2: Overview and Work in Progress*, in: *Trends in Mathematical Physics*, AMS/International Press (1999) &lbrack;[amsip:13](https://bookstore.ams.org/amsip-13), [[Johnson-CrystalTopology2.pdf:file]]&rbrack;

* [[Carroll K. Johnson]], Michael N. Burnett: *Crystallographic Topology -- The Topology of Crystallographic Groups and Simple Crystal Structures* &lbrack;[webpage](https://ornl-ndav.github.io/ortep/topology.html)&rbrack;

  * 2.2. [Euclidean 2-Orbifolds from Plane Groups](https://ornl-ndav.github.io/ortep/topology/orbfld2.html)

  * [Orbifold atlas](https://ornl-ndav.github.io/ortep/topology/atlas/atlas.html)



[[!redirects crystallographic groups]]

[[!redirects crystallographic point group]]
[[!redirects crystallographic point groups]]

[[!redirects crystallographic symmetry]]
[[!redirects crystallographic symmetries]]

[[!redirects space group]]
[[!redirects space groups]]

[[!redirects point group]]
[[!redirects point groups]]

[[!redirects symmorphic space group]]
[[!redirects symmorphic space groups]]

[[!redirects symmorphic crystallographic group]]
[[!redirects symmorphic crystallographic groups]]


[[!redirects representation torus]]
[[!redirects representation tori]]

[[!redirects Bieberbach's first theorem]]

[[!redirects Bieberbach's theorem]]
[[!redirects Bieberbach's theorems]]
