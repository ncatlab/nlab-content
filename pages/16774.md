
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

The _icosahedral group_ is the [[group]] of [[symmetries]] of an [[icosahedron]].

As a symmetry group of one of the [[Platonic solids]], the icosahedral group participates in the _ADE pattern_:

[[!include ADE -- table]]


More in detail, there are variants of the icosahedral group corresponding to the stages of the [Whitehead tower of O(3)](Whitehead+tower#OfTheOrthogonalGroup):

* the full icosahedral group is the [[subgroup]] of [[orthogonal group|O(3)]] 

  $$
    I_h \hookrightarrow O(3)
  $$

  which is the [[stabilizer subgroup|stabilizer]] of the standard embedding of the [[icosahedron]] into [[Cartesian space]] $\mathbb{R}^3$;

* the _rotational icosahedral group_ $I \hookrightarrow SO(3)$ is the restriction to orientation-preserving symmetries, hence to [[special orthogonal group|SO(3)]]; this is [[isomorphism|isomorphic]] to the [[alternating group]] $A_5$

* finally the _binary icosahedral group_ is the [[double cover]] (see at _[[covering of alternating group]]_), hence the lift of $I$ to [[spin group|Spin(3)]]$\simeq$ [[special unitary group|SU(2)]];

* next there is a [[string 2-group]] lift $\mathcal{I} \hookrightarrow String_{SU(2)}$ of the icosahedral group ([Epa 10](#Epa10), [Epa-Ganter 16](#EpaGanter16))

$$
  \array{
     String_{2I} &\hookrightarrow& String_{SU(2)}
     \\
     \downarrow && \downarrow
     \\
     2 I &\hookrightarrow & Spin(3) \simeq SU(2)
     \\
     \downarrow && \downarrow
     \\
     I \simeq A_5 &\hookrightarrow&  SO(3)
     \\
     \downarrow && \downarrow
     \\
     I_h \simeq A_5\times \mathbb{Z}/2 &\hookrightarrow & O(3)
  }
$$

## Definition 
 {#Definition}

Regard the [[icosahedron]], determined uniquely up to [[isometry]] on $\mathbb{R}^3$ as a regular convex [[polyhedron]] with $20$ faces, as a [[metric space|metric]] subspace $S$ of $\mathbb{R}^3$. Then the *icosahedral group* may be defined as the group of [[isometries]] of $S$. 

More to be added. 

## Properties

### Group order

The [[subgroup]] of [[orientation]]-preserving symmetries of the [[icosahedron]] is the [[alternating group]] $A_5$ whose [[order of a group|order]] is 60. The full icosahedral group is [[isomorphism|isomorphic]] to the [[Cartesian product]] $A_5 \times \mathbb{Z}_2$ (with the [[group of order 2]]). 

Hence the [[order of a group|order]] of the icosahedral group is $ 60 \times 2 = 120 $.

### Exceptional isomorphisms

There is an exceptional [[isomorphism]] $I \simeq PSL_2(\mathbb{F}_5)$, with $2I \simeq SL_2(\mathbb{F}_5)$ covering this isomorphism.

($PSL_2$ the [[projective special linear group]], $SL_2$ the [[special linear group]], $\mathbb{F}_5$ the [[prime field]] for $p = 5$)


### Subgroups

+-- {: .num_prop #QuaternionSubgroup}
###### Proposition
**([[quaternion group]] inside [[binary icosahedral group]])**

The [[binary icosahedral group]] contains the [[quaternion group]] of [[order]] 8, hence the [[binary dihedral group]] of [[order of a group|order]] 8, as a [[subgroup]] (not [[normal subgroup|normal]]):

$$
  2 D_4 =Q_8 \subset 2 I
  \,.
$$

In fact the only [[finite subgroups of SU(2)]] which contain $2 D_4 =Q_8$ as a proper subgroup are the exceptional ones, hence the [[binary tetrahedral group]], the [[binary octahedral group]] and the [[binary icosahedral group]].

=--

See [this Prop](quaternion+group#InclusionInLargerFininteSubgroupsOfSU2) at _[[quaternion group]]_.

+-- {: .num_prop #NormalSubgroupsOf2I}
###### Proposition
**([[normal subgroups]] of [[binary icosahedral group]]

The only proper [[normal subgroup]] of the [[binary icosahedral group]] is its [[center]] $Z(2I) \simeq \mathbb{Z}/2$.


=--




### Quotient spaces

The [[coset space]] $SU(2)/2I$ is the [[Poincaré homology sphere]].

### Group cohomology

For a little bit about the [[group cohomology]] (or at least the homology) of the binary icosahedral group $SL_2(\mathbb{F}_5)$, see _[Groupprops](#Groupprops)_


## Related concepts

* [[Platonic 2-group]]

## References

* {#Klein1884} [[Felix Klein]], chapter I.8 of _Vorlesungen über das Ikosaeder und die Auflösung der Gleichungen vom fünften Grade_, 1884, translated as _Lectures on the Icosahedron and the Resolution of Equations of Degree Five_ by George Morrice 1888, [online version](https://archive.org/details/cu31924059413439)


* Wikipedia, _[Icosahedral symmetry](https://en.wikipedia.org/wiki/Icosahedral_symmetry)_

* {#Groupprops} Groupprops, _[Alternating group:A5](http://groupprops.subwiki.org/wiki/Alternating_group:A5)_ _[Group cohomology of algebrating group:A5](http://groupprops.subwiki.org/wiki/Group_cohomology_of_alternating_group:A5)_

* [[Philip Boalch]], _The fifty-two icosahedral solutions to Painlev&#233; VI_, J. Reine Angew. Math. 596 (2006) 183--214 ([arXiv:0406281](http://arxiv.org/abs/math/0406281))

* {#Epa10} [[Narthana Epa]], _Platonic 2-groups_, 2010 ([pdf](http://www.ms.unimelb.edu.au/documents/thesis/Epa-Platonic2-Groups.pdf))


* {#EpaGanter16} [[Narthana Epa]], [[Nora Ganter]], _Platonic and alternating 2-groups_, ([arXiv:1605.09192](http://arxiv.org/abs/1605.09192))


[[!redirects rotational icosahedral group]]
[[!redirects binary icosahedral group]]
[[!redirects stringy icosahedral group]]

