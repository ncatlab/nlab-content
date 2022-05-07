
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Any [[group]] $G$ has a [[category]] of finite-dimensional [[complex number|complex]]-linear [[representations]], often denoted $Rep(G)$.  This is a [[symmetric monoidal category|symmetric monoidal]] [[abelian category]] (a "[[tensor category]]") and thus has a [[Grothendieck ring]], which is called the **representation ring** of $G$ and denoted $R(G)$. Elements of the representation ring are hence formal differences (with respect to [[direct sum]]) of ordinary representations: [[virtual representations]].

### In components

More concretely, we get $R(G)$ as follows.  It has a [[basis]] $(e_i)_i$ given by the [[isomorphism classes]] of **[[irreducible representations]]** of $G$: that is, $i$ is an index for an irreducible finite-dimensional complex representation of $G$.  It has a product given by 

$$ e_i e_j = \sum_k m_{i j}^k e_k ,$$

where $m_{i j}^k$ is the multiplicity of the $k$th irrep in the 
[[tensor product of representations]] of the $i$th and $j$th irreps.  

In [[physics]] these coefficients are also known as _[[Clebsch-Gordan coefficients]]_ (specifically for $G$ the [[special orthogonal group]] $SO(3)$), and the relations they satisfy are also known as _[[Fierz identities]]_ (specifically for $G$ a [[spin group]]).

Notice that $R(G)$ is commutative thanks to the [[symmetric monoidal category|symmetry]] of the tensor product.


### As equivariant K-theory of the point
 {#AsEquivariantKTheoryOfThePoint}

Equivalently the representation ring of $G$ over the [[complex numbers]] is the $G$-[[equivariant K-theory]] of the point, or equivalently by the [[Green-Julg theorem]], if $G$ is a [[compact Lie group]], the [[operator K-theory]] of the [[group algebra]] (the [[groupoid convolution algebra]] of the [[delooping]] groupoid of $G$):

$$
  R_{\mathbb{C}}(G) \simeq KU^0_G(\ast) \simeq KK(\mathbb{C}, C(\mathbf{B}G))
  \,.
$$

The first [[isomorphism]] here follows immediately from the elementary definition of equivariant [[topological K-theory]], since a $G$-[[equivariant vector bundle]] over the point is manifestly just a [[linear representation]] of $G$ on a [[complex vector space]].

(e.g. [Greenlees 05, section 3](#Greenlees05), [Wilson 16, example 1.6 p. 3](#Wilson16))

Therefore a similar isomorphism identifies the $G$-representation ring over the [[real numbers]] with the equivariant orthogonal $K$-theory of the point in degree 0:

$$
  R_{\mathbb{R}}(G)
  \;\simeq\;
  KO_G^0(\ast)
  \,.
$$

But beware that equivariant [[KO]], even of the point, is much richer in higher degree ([Wilson 16, remark 3.34](#Wilson16))

In fact, [[equivariant KO-theory]] of the point subsumes the [[representation rings]] over the [[real numbers]], the [[complex numbers]] and the [[quaternions]]:

$$
  KO_G^n(\ast)
  \;\simeq\;
  \left\{
  \array{
    0 &\vert& n = 7
    \\
    R_{\mathbb{H}}(G)/ R_{\mathbb{R}}(G) &\vert& n = 6
    \\
    R_{\mathbb{H}}(G)/ R_{\mathbb{C}}(G) &\vert& n = 5
    \\
    R_{\mathbb{H}}(G) \phantom{/ R_{\mathbb{R}}(G) }  &\vert& n = 4
    \\
    0 &\vert& n = 3
    \\
    R_{\mathbb{C}}(G)/ R_{\mathbb{H}}(G) &\vert& n = 2
    \\
    R_{\mathbb{R}}(G)/ R_{\mathbb{C}}(G) &\vert& n = 1
    \\
    R_{\mathbb{R}}(G) \phantom{/ R_{\mathbb{R}}(G)} &\vert& n =0
  }
  \right.
$$

([Greenlees 05, p. 3](#Greenlees05))


[[!include Segal completion -- table]]

## Properties

### Relation to the character ring

If $G$ is a [[finite group]] and we [[tensor product of modules|tensor]] $R(G)$ with the [[complex numbers]], it becomes [[isomorphism|isomorphic]] to the **[[character ring]]** of $G$: that is, the ring of complex-valued functions on $G$ that are constant on each [[conjugacy class]].  Such functions are called **[[class functions]]**.

Similarly for $G$ a [[compact Lie group]], its complex linear [[representations]] $\rho \colon G \to U(n) \to Aut(\mathbb{C}^n)$ (for all $n \in \mathbb{N}$) are uniquely specified by their [[characters]] $\chi_\rho \coloneqq tr(\rho(-)) \colon G \to \mathbb{C}$. Therefore also here the representation ring is often called the _character ring_ of the group.
 
### Relation to Schur's lemma

The ([[isomorphism classes]]) of [[finite-dimensional vector space|finite-dimensional]] [[irreducible representations]] $V_i$ form the canonical $\mathbb{Z}$-[[linear basis]] of the representation ring:

$$
  R(G) \;\simeq\; \mathbb{Z}\big[  \{V_i\}_i \big]
  \,.
$$

Moreover, the [[function]] assigning [[dimensions]] of [[hom-object|hom]]-[[vector spaces]] constitutes a canonical bilinear symmetric [[inner product]]:

$$
  \langle -,-\rangle
  \;\colon\;
  R(G) \times R(G)
    \longrightarrow
  \mathbb{Z}
  \,.
$$

In terms of this, _[[Schur's lemma]]_ states that the [[irreducible representations]] generally constitute an _[[orthogonal basis]]_, and even an _[[orthonormal basis]]_ when the [[ground field]] is [[algebraically closed field|algebraically closed]].

For more discussion of this perspective, see 

* at _[[Schur's lemma]]_ the section _[In terms of categorical algebra](Schur's+lemma#InterpretationInCategoricalAlgebra)_;

* at _[[Gram-Schmidt process]]_ the section _[Categorified Gram-Schmidt  process](Gram-Schmidt+process#CategorifiedGramSchmidtProcess)_.


### Relation to equivariant K-theory

The representation ring of a [[compact Lie group]] is equivalent to the $G$-[[equivariant K-theory]] of the point.

$$
  Rep(G) \simeq K_G(\ast)
  \,.
$$

The construction of representations by [[index]]-constructions of $G$-equivariant [[Dirac operators]] ([[push-forward in generalized cohomology|push-forward]] in $G$-[[equivariant K-theory]] to the point) is called _[[Dirac induction]]_.

[[!include Segal completion -- table]]


### Lambda-ring structure
 {#LambdaRingStructure}

The [[Adams operations]] equip the representation ring with the structure of a [[Lambda ring]],. (e.g. [tomDieck 79, section 3.5](#tomDieck79), [tom Dieck 09, section 6.2](#tomDieck09), [Meir 17](#Meir17)).

### Relation to the Burnside ring

Let $G$ be a [[finite group]]. Consider

1. the [[Burnside ring]] $A(G)$, which is the [[Grothendieck group]] of the [[monoidal category]] $G Set$ of [[finite set|finite]] [[G-sets]];

1. the [[representation ring]] $R(G)$, which is the [[Grothendieck group]] of the monoidal category $G Rep$ of [[finite dimensional vector space|finite dimensional]] $G$-[[linear representations]].

Then then map that sends a G-set to the corresponding linear [[permutation representation]] is a [[strong monoidal functor]]

$$
  G Set \overset{\mathbb{C}[-]}{\longrightarrow} G Rep
$$

and hence induces a [[ring homomorphism]]

$$
  A(G) \overset{ \mathbb{C}[-] }{\longrightarrow} R(G)
$$

Under the identitification

1. of the [[Burnside ring]] with the [[equivariant stable cohomotopy]] of the point 

   $$
     A(G) \;\simeq\; \mathbb{S}_G(\ast)
   $$

   (see [there](Burnside+ring#AsTheEquivariantStableCohomotopyOfThePoint))

1. of the [[representation ring]] with the [[equivariant K-theory]] of the point

   $$
     R(G) \;\simeq\; K_G(\ast)
   $$

   (as [above](#AsEquivariantKTheoryOfThePoint))

this should be image of the initial morphism of [[E-infinity ring spectra]]

$$
  \mathbb{S} \longrightarrow KU
$$

from the [[sphere spectrum]] to [[KU]].


### Splitting principle and Brauer induction theorem

The [[Brauer induction theorem]] says that, over the [[complex numbers]], the representation ring is generated already from the [[induced representations]] of 1-dimensional representations. This may be regarded as the [[splitting principle]] for linear representations and for [[characteristic classes of linear representations]] ([Symonds 91](#Symonds91)).


## Examples


### Spin group

The completion of $Rep(Spin(2k))$ is $\mathbb{Z}[ [ e^{\pm x_j} ] ]$ for $1 \leq j \leq k$ (e.g [Brylinski 90, p. 9](#Brylinski90)).


## Related concepts

* [[Clebsch-Gordan coefficients]], [[Fierz identities]]

* [[Deligne's theorem on tensor categories]]

## References


### General


Lecture notes include

* {#tomDieck09} [[Tammo tom Dieck]], section 4.4. in _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))

Exposition in relation to [[equivariant K-theory]] includes

* [[Akhil Mathew]], _[Equivariant K-theory](https://amathew.wordpress.com/2011/12/03/equivariant-k-theory/)_

* {#Greenlees05} [[John Greenlees]], _Equivariant version of real and complex connective K-theory_, Homology Homotopy Appl. Volume 7, Number 3 (2005), 63-82. ([Euclid:1139839291](http://projecteuclid.org/euclid.hha/1139839291))


* {#Wilson16} [[Dylan Wilson]], _Equivariant K-theory_, 2016 ([pdf](https://www.math.uchicago.edu/~dwilson/notes/equivariant-k-theory-talk.pdf), [[WilsonKTheory16.pdf:file]])

Classical results for [[compact Lie groups]]:

* {#Segal68} [[Graeme Segal]], _The representation ring of a compact Lie group_, Publications Math&#233;matiques de l'Institut des Hautes &#201;tudes Scientifiques, January 1968, Volume 34, Issue 1, pp 113-128 ([numdam:PMIHES_1968__34__113_0](http://www.numdam.org/item/?id=PMIHES_1968__34__113_0))

* Masaru Tackeuchi, _A remark on the character ring of a compact Lie group_, J. Math. Soc. Japan Volume 23, Number 4 (1971), 555-705 ([Euclid](http://projecteuclid.org/euclid.jmsj/1259849785))


In the generality of [[super Lie groups]]:

* [[Gregory Landweber]], _Representation rings of Lie superalgebras_, K-Theory 36 (2005), no. 1-2, 115-168 ([arXiv:math/0403203](http://arxiv.org/abs/math/0403203))

* [[Gregory Landweber]], _Twisted representation rings and Dirac induction_, J. Pure Appl. Algebra 206 (2006), no. 1-2, 21-54 ([arXiv:math/0403524](http://arxiv.org/abs/math/0403524))

With an eye towards [[loop group representations]]:

* {#Brylinski90} [[Jean-Luc Brylinski]], _Representations of loop groups, Dirac operators on loop space, and modular forms_, Topology, 29(4):461&#8211;480, 1990.

Concerning the [[Brauer induction theorem]] and the [[splitting principle]]:

* {#Symonds91} [[Peter Symonds]], _A splitting principle for group representations_, Comment. Math. Helv. (1991) 66: 169 ([dml:140229](https://eudml.org/doc/140229), [doi:10.1007/BF02566643](https://doi.org/10.1007/BF02566643))


### Adams operations

The [[Adams operations]] and [[Lambda-ring]]-structure on representation rings are discussed in

* {#tomDieck79} [[Tammo tom Dieck]], section 3.5 of _[[Transformation Groups and Representation Theory]]_, Lecture Notes in Mathematics 766 Springer 1979

* Robert Boltje, _A characterization of Adams operations on representation rings_, 2001 ([pdf](https://boltje.math.ucsc.edu/publications/p01v.pdf))

* {#tomDieck09} [[Tammo tom Dieck]], section 6.2 of  _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))

* [[Michael Boardman]], _Adams operations on Group representations_, 2007 ([pdf](http://www.math.jhu.edu/~jmb/note/adamrept.pdf))

* {#Meir17} Ehud Meir, [[Markus Szymik]], _Adams operations and symmetries of representation categories_ ([arXiv:1704.03389](https://arxiv.org/abs/1704.03389))

[[!redirects representation rings]]
