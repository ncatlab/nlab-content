[[!redirects space group]]

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

A **space group** in [[dimension]] $n$, also known as a **crystallographic group**, is a [[subgroup]] of the corresponding [[Euclidean group]], hence of the [[isometry group]] of [[Euclidean space]] $\mathbb{R}^n$, that contains some [[lattice in a vector space|lattice]] in $\mathbb{R}^n$ as a [[subgroup]], and is contained within the [[automorphism group]] of that lattice. In other words, it is a subgroup of the automorphism group of the lattice that contains all the [[translations]] by elements of the lattice itself.

Equivalently, a crystallographic group on a [[Euclidean space]] $E$ is a [[discrete group|discrete]] [[subgroup]] $S \subset Iso(E)$ of the [[isometry group]] of $E$ (its [[Euclidean group]]) that contains a [[lattice (discrete subgroup)|lattice]] $N \subset E \subset Iso(E)$ of [[translation group|translations]] as a [[normal subgroup]] $N \subset S$, such that the corresponding [[quotient group]], called the _[[point group]]_ of the crystallographic group, is a subgroup $G \coloneqq S/N \;\subset\; O(E)$ of the [[orthogonal group]]. 

In short, a crystallographic groups is exhibited by an inclusion of [[short exact sequences]] of ([[nonabelian group|non-abelian]]) [[groups]], as follows:

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

(This perspective on crystallographic groups is known as [[Bieberbach's first theorem]], see for instance [Tolcachier 19, Theorem 2.3](#Tolcachier19), also [Freed-Moore 13, (0.2)](#FreedMoore13).)

If the [[short exact sequence]] on the left [[split exact sequence|splits]], hence if the space group $S \simeq G \ltimes N$ is the [[semidirect product]] of the [[point group]] with the translational lattice, $S$ is called a _symmorphic space group_.

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

## References

* _The Crystallographic Groups_, Pure and Applied Mathematics
Volume 50, 1972, Pages 16-60 (<a href="https://doi.org/10.1016/S0079-8169(08)60959-9">doi:10.1016/S0079-8169(08)60959-9</a>)

* {#BrownBulowNeubuserWondratschekZassenhaus78} H. Brown, R. Bülow, J. Neubüser, H. Wondratschek, H. Zassenhaus, _Crystallographic Groups of Four-Dimensional Space_, John Wiley, New York, 1978. 

* {#Farkas81} Daniel R. Farkas, _Crystallographic groups and their mathematics_, Rocky Mountain J. Math. Volume 11, Number 4 (1981), 511-552 ([doi:10.1216/RMJ-1981-11-4-511](https://projecteuclid.org/euclid.rmjm/1250128489))

* {#ChuprunovKuntsevich88} E. V. Chuprunov, T. S. Kuntsevich, _$n$-Dimensional space groups and regular point systems_, Comput. Math. Applic. Vol. 16, No. 5-8, pp. 537-543, 1988 (<a href="https://doi.org/10.1016/0898-1221(88)90243-X">doi:10.1016/0898-1221(88)90243-X</a>)

* D. Weigel, T. Phan and R. Veysseyre, _Crystallography, geometry and physics in higher dimensions. III. Geometrical symbols for the 227 crystallographic point groups in four-dimensional space_, Acta Cryst. (1987). A43, 294-304 ([doi:10.1107/S0108767387099367](https://doi.org/10.1107/S0108767387099367))

* {#FreedMoore13} [[Daniel Freed]], [[Gregory Moore]], _Twisted equivariant matter_, Ann. Henri Poincaré (2013) 14: 1927 ([arXiv:1208.5055](https://arxiv.org/abs/1208.5055))

* {#Tolcachier19} Alejandro Tolcachier, _Holonomy groups of compact flat solvmanifolds_ ([arXiv:1907.02021](https://arxiv.org/abs/1907.02021))

* [[GAP]] package, _The Crystallographic Groups Catalog_ ([web](http://www.math.rwth-aachen.de/~Greg.Gamble/gap4r3/pkg/crystcat/htm/CHAP001.htm))

See also

* [[eom]], _[Crystallographic group](https://www.encyclopediaofmath.org/index.php/Crystallographic_group)_

* [[Groupprops]], _[Space group](https://groupprops.subwiki.org/wiki/Space_group)_

* Wikipedia, _[Space group](https://en.wikipedia.org/wiki/Space_group)_

* Wikipedia, _[Point group](https://en.wikipedia.org/wiki/Point_group)_

[[!redirects space groups]]

[[!redirects point group]]
[[!redirects point groups]]

[[!redirects symmorphic space group]]
[[!redirects symmorphic space groups]]

[[!redirects symmorphic crystallographic group]]
[[!redirects symmorphic crystallographic groups]]


[[!redirects crystallographic group]]
[[!redirects crystallographic groups]]

[[!redirects representation torus]]
[[!redirects representation tori]]

[[!redirects Bieberbach's first theorem]]

