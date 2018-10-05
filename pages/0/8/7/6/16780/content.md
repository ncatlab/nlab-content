
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

The _tetrahedral group_ is the [[finite group|finite]] [[symmetry group]] of a [[tetrahedron]]. 

As a symmetry group of one of the [[Platonic solids]], the tetrahedral group participates in the _ADE pattern_:

[[!include ADE -- table]]


More in detail, there are variants of the tetrahedral group corresponding to the stages of the [Whitehead tower of O(3)](Whitehead+tower#OfTheOrthogonalGroup):

* the full tetrahedral group is the [[subgroup]] of [[orthogonal group|O(3)]] 

  $$
    T_d \hookrightarrow O(3)
  $$

  which is the [[stabilizer subgroup|stabilizer]] of the standard embedding of the [[tetrahedron]] into [[Cartesian space]] $\mathbb{R}^3$;

* the _rotational tetrahedral group_ $T \hookrightarrow SO(3)$ is the restriction to [[orientation]]-preserving symmetries, hence to [[special orthogonal group|SO(3)]]; this is [[isomorphism|isomorphic]] to the [[alternating group]] $A_4$;

* next the _binary tetrahedral group_ $2T$ is the [[double cover]], hence the lift of $T$ to [[spin group|Spin(3)]]$\simeq$ [[special unitary group|SU(2)]];

* then there is a [[string 2-group]] lift $String_{2T} \hookrightarrow String_{SU(2)}$ of the tetrahedral group to a _[[Platonic 2-group]]_ ([Epa 10](#Epa10), [Epa-Ganter 16](#EpaGanter16))

$$
  \array{
     String_{2T} &\hookrightarrow& String_{SU(2)}
     \\
     \downarrow && \downarrow
     \\
     2 T &\hookrightarrow & Spin(3) \simeq SU(2)
     \\
     \downarrow && \downarrow
     \\
     T \simeq A_4 &\hookrightarrow&  SO(3)
     \\
     \downarrow && \downarrow
     \\
     T_d \simeq S_5 &\hookrightarrow & O(3)
  }
$$


## Properties

### Basic properties

The full tetrahedral group is [[isomorphism|isomorphic]] to the [[symmetric group]] $S_4$ of [[permutations]] of four elements (see _[Full tetrahedral group is isomorphic to S4](http://groupprops.subwiki.org/wiki/Full_tetrahedral_group_is_isomorphic_to_S4)_).

The [[subgroup]] of [[orientation]]-preserving symmetries is isomorphic to the [[alternating group]] $A_4$.



The [[order of a group|group order]] is:

$\vert T_d\vert = 24$

$\vert T\vert = 12$

$\vert 2T\vert = 24$


+-- {: .num_prop #QuaternionSubgroup}
###### Proposition
**([[quaternion group]] inside [[binary tetrahedral group]])**

The binary tetrahedral group contains the [[quaternion group]] of [[order]] 8, hence the [[binary dihedral group]] of [[order of a group|order]] 8, as a [[subgroup]], in fact as a [[normal subgroup]]:

$$
  2 D_4 =Q_8 \subset 2 T
  \,.
$$

In fact the only [[finite subgroups of SU(2)]] which contain $2 D_4 =Q_8$ as a proper subgroup are the exceptional ones, hence the [[binary tetrahedral group]], the [[binary octahedral group]] and the [[binary icosahedral group]].

=--

See [this Prop](quaternion+group#InclusionInLargerFininteSubgroupsOfSU2) at _[[quaternion group]]_.


### As part of the ADE pattern

[[!include ADE -- table]]


### Character table

[[!include character table of 2T]]


### Group cohomology

The [[group cohomology]] of the tetrahedral group is discussed in [Groupprops](#Groupprops), [Kirdar 13](#Kirdar13).


## References

Discussion in the context of [[classification of finite rotation groups]] goes back to:

* {#Klein1884} [[Felix Klein]], chapter I.4 of _Vorlesungen über das Ikosaeder und die Auflösung der Gleichungen vom fünften Grade_, 1884, translated as _Lectures on the Icosahedron and the Resolution of Equations of Degree Five_ by George Morrice 1888, [online version](https://archive.org/details/cu31924059413439)

Exposition is in 

* Tony Phillips, _[The Geometry of the Binary Tetrahedral Group in SU(2)](http://www.math.stonybrook.edu/~tony/bintet/)_


Discussion of [[higher central extension]] to [[Platonic 2-groups]] is in

* {#Epa10} [[Narthana Epa]], _Platonic 2-groups_, 2010 ([pdf](http://www.ms.unimelb.edu.au/documents/thesis/Epa-Platonic2-Groups.pdf))

* {#EpaGanter16} [[Narthana Epa]], [[Nora Ganter]], _Platonic and alternating 2-groups_, ([arXiv:1605.09192](http://arxiv.org/abs/1605.09192))

See also

* {#Kirdar13} Mehmet Kirdar, _On The K-Ring of the Classifying Space of the Symmetric Group on Four Letters_ ([arXiv:1309.4238](http://arxiv.org/abs/1309.4238))

* Wikipedia, _[Tetrahedral symmetry](https://en.wikipedia.org/wiki/Tetrahedral_symmetry)_

* {#Groupprops} Groupprops, _[Group cohomology of symmetric group:S4](http://groupprops.subwiki.org/wiki/Group_cohomology_of_symmetric_group:S4)_


[[!redirects tetrahedral groups]]

[[!redirects binary tetrahedral group]]
[[!redirects binary tetrahedral groups]]
