
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

The _octahedral group_, a [[finite group]], is the group ofn [[symmetries]] of an [[octahedron]].

As a symmetry group of one of the [[Platonic solids]], the octahedral group participates in one of the three exceptional entries cases of the _ADE pattern_:

[[!include ADE -- table]]


More in detail, there are variants of the octahedral group corresponding to the stages of the [Whitehead tower of O(3)](Whitehead+tower#OfTheOrthogonalGroup):

* the full octahedral group is the [[subgroup]] of [[orthogonal group|O(3)]] 

  $$
    O_h \hookrightarrow O(3)
  $$

  which is the [[stabilizer subgroup|stabilizer]] of the standard embedding of the [[octahedron]] into [[Cartesian space]] $\mathbb{R}^3$;

* the _rotational octahedral group_ $O \hookrightarrow SO(3)$ is the restriction to [[orientation]]-preserving symmetries, hence to [[special orthogonal group|SO(3)]]; this is [[isomorphism|isomorphic]] to the [[symmetric group]] $S_4$;

* finally the _binary octahedral group_ is the [[double cover]], hence the lift of $I$ to [[spin group|Spin(3)]]$\simeq$ [[special unitary group|SU(2)]];

* next there is a [[string 2-group]] lift $String_{2O} \hookrightarrow String_{SU(2)}$ of the octahedral group ([Epa 10](#Epa10), [Epa-Ganter 16](#EpaGanter16))

$$
  \array{
     String_{2O} &\hookrightarrow& String_{SU(2)}
     \\
     \downarrow && \downarrow
     \\
     2 O &\hookrightarrow & Spin(3) \simeq SU(2)
     \\
     \downarrow && \downarrow
     \\
     O \simeq S_4 &\hookrightarrow&  SO(3)
     \\
     \downarrow && \downarrow
     \\
     O_h \simeq S_4 \times \mathbb{Z}/2 &\hookrightarrow & O(3)
  }
$$

## Properties

### Basic properties



The [[order of a group|group order]] is:


$\vert O_h\vert = 48$

$\vert O \vert = 24$

$\vert 2O \vert = 48$


The [[subgroup]] of the octahedral group on the [[orientation]]-preserving symmetries is [[isomorphism|isomorphic]] to the [[symmetric group]] $S_4$. This also happens to be the full [[tetrahedral group]].


+-- {: .num_prop #QuaternionSubgroup}
###### Proposition
**([[quaternion group]] inside [[binary tetrahedral group]])**

The [[binary octahedral group]] contains the [[quaternion group]] of [[order]] 8, hence the [[binary dihedral group]] of [[order of a group|order]] 8, as a [[subgroup]] (not [[normal subgroup|normal]]):

$$
  2 D_4 = Q_8 \subset 2 O
  \,.
$$

In fact the only [[finite subgroups of SU(2)]] which contain $2 D_4 =Q_8$ as a proper subgroup are the exceptional ones, hence the [[binary tetrahedral group]], the [[binary octahedral group]] and the [[binary icosahedral group]].

=--

See [this Prop](quaternion+group#InclusionInLargerFininteSubgroupsOfSU2) at _[[quaternion group]]_.


### Character table

[[character table of 2O]]

**[[linear representation theory]] of [[binary octahedral group]] $2 O$**


$\,$

| [[conjugacy classes]]: |  1 |  -1  |  $i$ | a | c | e | f | g | 
|------------------------|----|------|------|---|---|---|---|--|
| their [[cardinality]]: | 1 |  1 | 6  | 8 | 8 | 6 | 6 | 12 |

**[[character table]] over the [[complex numbers]] $\mathbb{C}$**

| [[irrep]]  |  1 |  -1  |  $i$ | a | c | e | f | g | 
|-----------|----|------|------|---|---|---|---|--|
| $\rho_1$ | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 
| $\rho_2$ | 1 | 1 | 1 | 1 | 1 | -1 | -1 | -1 | 
| $\rho_3$ | 2 | 2 | 2 | -1 | -1 | 0 | 0 | 0 | 
| $\rho_4$ | 3 | 3 | -1 | 0 | 0 | 1 | 1 | -1 | 
| $\rho_5$ | 3 | 3 | -1 | 0 | 0 | -1 | -1 | 1 | 
| $\rho_6$ | 2 | -2 | 0 | 1 | -1 | $\sqrt{2}$ | $-\sqrt{2}$ | 0 | 
| $\rho_7$ | 2 | -2 | 0 | 1 | -1 | $-\sqrt{2}$ | $\sqrt{2}$ | 0 | 
| $\rho_8$ | 4 | -4 | 0 | -1 | 1 | 0 | 0 | 0 | 

 
**[[character table]] over the [[real numbers]] $\mathbb{R}$**

| [[irrep]]  |  1 |  -1  |  $i$ | a | c | e | f | g | 
|-----------|----|------|------|---|---|---|---|--|
| $\rho_1$ | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 
| $\rho_2$ | 1 | 1 | 1 | 1 | 1 | -1 | -1 | -1 | 
| $\rho_3$ | 2 | 2 | 2 | -1 | -1 | 0 | 0 | 0 | 
| $\rho_4$ | 3 | 3 | -1 | 0 | 0 | 1 | 1 | -1 | 
| $\rho_5$ | 3 | 3 | -1 | 0 | 0 | -1 | -1 | 1 | 
| $\rho_6 \oplus \rho_6$ | 4 | -4 | 0 | 2 | -2 | $2 \sqrt{2}$ | $-2 \sqrt{2}$ | 0 | 
| $\rho_7 \oplus \rho_7$ | 4 | -4 | 0 | 2 | -2 | $-2 \sqrt{2}$ | $2 \sqrt{2}$ | 0 | 
| $\rho_8 \oplus \rho_8$ | 8 | -8 | 0 | -2 | 2 | 0 | 0 | 0 | 



**References**

* [[James Montaldi]], _[Real representations -- Binary cubic -- 2O](http://www.maths.manchester.ac.uk/~jm/wiki/Representations/BinaryCubic#BinOct)_


### Group cohomology

The [[group cohomology]] of the orientation-preserving octahedral group is discussed in [Groupprops](#Groupprops), [Kirdar 13](#Kirdar13).


## References

* {#Klein1884} [[Felix Klein]], chapter I.7 of _Vorlesungen über das Ikosaeder und die Auflösung der Gleichungen vom fünften Grade_, 1884, translated as _Lectures on the Icosahedron and the Resolution of Equations of Degree Five_ by George Morrice 1888, [online version](https://archive.org/details/cu31924059413439)

Aspects of the linear [[representation theory]] of the binary octahedral group ([[irreducible representations]], [[character table]]) is spelled out at 

* Groupprops, _[Linear representation theory of binary octahedral group](https://groupprops.subwiki.org/wiki/Linear_representation_theory_of_binary_octahedral_group)_

See also

* Wikipedia, _[Octahedral symmetry](https://en.wikipedia.org/wiki/Octahedral_symmetry)_

* {#Groupprops} Groupprops, _[Group cohomology of symmetric group:S4](http://groupprops.subwiki.org/wiki/Group_cohomology_of_symmetric_group:S4)_

* {#Kirdar13} Mehmet Kirdar, _On The K-Ring of the Classifying Space of the Symmetric Group on Four Letters_ ([arXiv:1309.4238](http://arxiv.org/abs/1309.4238))

* {#Epa10} [[Narthana Epa]], _Platonic 2-groups_, 2010 ([pdf](http://www.ms.unimelb.edu.au/documents/thesis/Epa-Platonic2-Groups.pdf))

* {#EpaGanter16} [[Narthana Epa]], [[Nora Ganter]], _Platonic and alternating 2-groups_, ([arXiv:1605.09192](http://arxiv.org/abs/1605.09192))



[[!redirects octahedral groups]]

[[!redirects binary octahedral group]]
[[!redirects binary octahedral groups]]


[[!redirects octahedral symmetry]]
[[!redirects octahedral symmetry group]]

