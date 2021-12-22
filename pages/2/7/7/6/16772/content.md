
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

### Dihedral groups
 {#DihedralGroups}

The dihedral group, $D_{2n}$, is a [[finite group]] of [[order of a group|order]] $2n$. It may be defined as the [[symmetry group]] of a regular $n$-gon. 

For instance $D_6$ is the symmetry group of the equilateral triangle and is [[isomorphism|isomorphic]] to the [[symmetric group]], $S_3$.

For $n \in \mathbb{N}$, $n \geq 1$, the dihedral group $D_{2n}$ is thus the [[subgroup]] of the [[orthogonal group]] [[O(2)|$O(2)$]] which is [[generators and relations|generated]] from the [[finite group|finite]] [[cyclic group|cyclic]] [[subgroup]] $C_n \,\coloneqq\, \mathbb{Z}/n$ of [[SO(2)|$SO(2)$]] and the [[reflection]] at the $x$-axis (say).  It is a [[semidirect product group|semi-direct product]] of $C_n$ and a [[finite group of order 2|$C_2 \,\coloneqq\, \mathbb{Z}/2$]] corresponding to that reflection, hence fitting into a {#ShortExactSequence} [[short exact sequence]] as follows:

\begin{tikzcd}
  \mathbb{Z}/n
  \ar[r, hook]
  \ar[d, hook]
  &
  \mathrm{SO}(2)
  \ar[d, hook]
  \\
  D_{2n}
  \ar[d, ->>]
  \ar[r, hook]
  &
  \mathrm{O}(2)
  \ar[d, ->>]
  \\
  \mathbb{Z}/2
  \ar[r,-,shift left=1pt]
  \ar[r,-,shift right=1pt]
  &
  \mathbb{Z}/2
\end{tikzcd}

Under the further embedding $O(2)\hookrightarrow SO(3)$ the cyclic and dihedral groups are precisely those [[finite subgroups of SO(3)]] that, among their [[ADE classification]], are not in the exceptional series. 


+-- {: .num_remark #NotationConvention}
###### Remark
**Warning on notation**

There are two different conventions for numbering the dihedral groups.  

1. The above is the _algebraic convention_ in which the suffix gives the [[order]] of the group: ${\vert D_{2 n}\vert} = 2 n$.

1. In the _geometric convention_ one writes "$D_n$" instead of "$D_{2n}$", recording rather the geometric nature of the object of which it is the symmetry group.  

   Also beware that there is yet another group denoted $D_n$ mentioned at _[[Coxeter group]]_.

=--


### Binary dihedral/dicyclic groups
  {#BinaryDihedralGroup}

Under the further lift through the [[spin group]]-[[double cover]] map $SU(2) \simeq Spin(3) \to SO(3)$ of the [[special orthogonal group]], the dihedral group $D_{2n}$ is covered by the _binary dihedral group_, also known as the _dicyclic group_ and denoted

$$
  2 D_{2n} = Dic_n
$$

Equivalently, this is the [[lift]] of the dihedral group $D_{2n}$ ([above](#DihedralGroups)) through the [[pin group]] [[double cover]] of the [[orthogonal group]] [[O(2)]] to [[Pin(2)]]

$$
  \array{
    2 D_{2n}
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Pin_-(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Spin(3)
    \\
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow
    \\
    D_{2n}
    &\overset{\phantom{AA}}{\hookrightarrow}&
    O(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(3)    
  }
$$

Explicity, let $\mathbb{H} \simeq \mathbb{C} \oplus \mathrm{j} \mathbb{C}$ be the [[quaternions]] realized as the [[Cayley-Dickson double]] of the [[complex numbers]], and identify the [[circle group]]

$$
  SO(2) \simeq S\big( \mathbb{C}\big) \hookrightarrow \mathbb{H}
$$

with the [[unit circle]] in $\mathbb{C} \hookrightarrow \mathbb{H}$ this way, with group structure given by [[multiplication]] of [[quaternions]]. Then the [[Pin group]] [[Pin(2)]] is [[isomorphism|isomorphic]] to the [[subgroup]] of the [[group of units]] $\mathbb{H}^\times$ of the [[quaternions]] which consists of this copy of [[SO(2)]] together with the multiples of the imaginary quaternion $\mathrm{j}$ with this copy:

$$
  Pin_-(2)
  \;\simeq\;
  S\big( \mathbb{C}\big) 
   \;\cup\; 
  \mathrm{j} \cdot S\big( \mathbb{C}\big) 
  \;\subset\;
  S(\mathbb{H}) 
  \;\simeq\;
  Spin(3)
  \,.
$$

The binary dihedral group $2 D_{2n}$ is the [[subgroup]] of that generated from 

1. $ a \coloneqq \exp\left( \pi \mathrm{i} \tfrac{1}{n} \right) \in S(\mathbb{C}) \subset Pin_-(2) \subset Spin(3)$

1. $x \coloneqq  \mathrm{j} \in Pin_-(2) \subset Spin(3)$.

It is manifest that these two generators satisfy the relations

$$
  a^{2n} = 1
  \,,
  \phantom{AA}
  x^2 = a^n \; (= -1)
  \,,
  \phantom{AA}
  x^{-1} a x = a^{-1}
$$

and in fact these [[generators and relations]] fully determine $2 D_{2n}$, up to [[isomorphism]].





## Properties

### Group cohomology

The [[group cohomology]] of the dihedral group is discussed for instance at [Groupprops](#Groupprops).

### As part of the ADE pattern

[[!include ADE -- table]]

### Group presentation

The dihedral group $D_{2n}$ has a group presentation 

$$\langle x,y : x^n=y^2=(xy)^2=1\rangle.$$

From this it is easy to see that it is a [[semi-direct product]] of the $C_n$ generated by $x$ and the $C_2$ generated by $y$.  The action of $y$ on $x$ is given by $\,^y x= x^{-1}$.

It is a standard example considered in elementary [[combinatorial group theory]].


## Examples

### Quaternion group $Q_8$ and triality

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://upload.wikimedia.org/wikipedia/commons/5/59/Dynkin_diagram_D4.png" width="100"/>
</div>

The first binary dihedral group $2 D_4$ is [[isomorphism|isomorphic]] to the [[quaternion group]] of order 8:

$$
  2 D_4 (= Dic_2) \simeq Q_8
  \,.
$$

In the [[ADE-classification]] this is the entry [[D4]].


[[!include character table of 2D4=Dic2=Q8]]




## Related concepts

* [[anti-cyclotomic extension]]

* [[dihedral homology]]

* [[group presentation]]

* [[Coxeter group]]

## References

Discussion in the context of the [[classification of finite rotation groups]] goes back to 

* {#Klein1884} [[Felix Klein]], chapter I.4 of _Vorlesungen über das Ikosaeder und die Auflösung der Gleichungen vom fünften Grade_, 1884, translated as _Lectures on the Icosahedron and the Resolution of Equations of Degree Five_ by George Morrice 1888, [online version](https://archive.org/details/cu31924059413439)


See also

* Wikipedia, _[Dihedral group](https://en.wikipedia.org/wiki/Dihedral_group)_

* Wikipedia, _[Binary dihedral group](https://en.wikipedia.org/wiki/Dicyclic_group#Binary_dihedral_group)_

* Wikipedia, _[Dicyclic group](https://en.wikipedia.org/wiki/Dicyclic_group)_

* [[Groupprops]], _[Dicyclic group](https://groupprops.subwiki.org/wiki/Dicyclic_group)_

* [[Groupprops]], _[Linear representation theory of dicyclic groups](https://groupprops.subwiki.org/wiki/Linear_representation_theory_of_dicyclic_groups)_

* {#Groupprops} [[Groupprops]], _[Group cohomology of dihedral group:D8](http://groupprops.subwiki.org/wiki/Group_cohomology_of_dihedral_group:D8)_

* [[GroupNames]], _[Dicyclic groups $Dic_n$](https://people.maths.bris.ac.uk/~matyd/GroupNames/dicyclic.html)_



Discussion as the [[equivariance group]] in [[equivariant cohomology theory]]: 

* {#Greenless01} [[John Greenlees]], Section 2 of: _Rational $SO(3)$-Equivariant Cohomology Theories_, in _Homotopy methods in algebraic topology_ (Boulder, CO, 1999), Contemp. Math. **271**,  Amer. Math. Soc. (2001) 99 ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.36.5444), [GBooks](https://books.google.de/books?id=X2YbCAAAQBAJ&lpg=PR7&ots=tdiPe0oWYn&dq=%22Homotopy%20methods%20in%20algebraic%20topology%22&lr&pg=PR7#v=onepage&q=%22Homotopy%20methods%20in%20algebraic%20topology%22&f=false))

and specifically in [[equivariant K-theory]] and [[KR-theory]]:

* {#BrunerGreenlees10} [[Robert Bruner]], [[John Greenlees]], Chapter 8 of: *Connective Real K-Theory of Finite Groups*, Mathematical Surveys and Monographs **169** AMS 2010 ([ISBN:978-0-8218-5189-0](https://bookstore.ams.org/surv-169))

Discussion of [[equivariant ordinary cohomology]] ([[Bredon cohomology]]) over the point but in arbitrary [[RO(G)-degree]], for [[equivariance group]] a [[dihedral group]] of [[order of a group|order]] $2p$:

* [[Igor Kriz]], [[Yunze Lu]], *On the $RO(G)$-graded coefficients of dihedral equivariant cohomology*, Mathematical Research Letters **27** 4 (2020) ([arXiv:2005.01225](https://arxiv.org/abs/2005.01225), [doi:10.4310/MRL.2020.v27.n4.a7](https://dx.doi.org/10.4310/MRL.2020.v27.n4.a7))




[[!redirects dihedral groups]]

[[!redirects binary dihedral group]]
[[!redirects binary dihedral groups]]

[[!redirects dicyclic group]]
[[!redirects dicyclic groups]]

