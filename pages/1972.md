
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

Equivalently the representation ring of $G$ is the $G$-[[equivariant K-theory]] of the point, or equivalently by the [[Green-Julg theorem]], if $G$ is a [[compact Lie group]], the [[operator K-theory]] of the [[group algebra]] (the [[groupoid convolution algebra]] of the [[delooping]] groupoid of $G$):

$$
  R(G) \simeq K_G(\ast) \simeq KK(\mathbb{C}, C(\mathbf{B}G))
  \,.
$$

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

The [[Adams operations]] equip the representation ring with the structure of a [[Lambda ring]],. (e.g. [tom Dieck 09, section 6.2](#tomDieck09), [Meir 17](#Meir17)).

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




## Examples


### Spin group

The completion of $Rep(Spin(2k))$ is $\mathbb{Z}[ [ e^{\pm x_j} ] ]$ for $1 \leq j \leq k$ (e.g [Brylinski 90, p. 9](#Brylinski90)).


## Related concepts

* [[Clebsch-Gordan coefficients]], [[Fierz identities]]

* [[Deligne's theorem on tensor categories]]

## References

Lecture notes include

* {#tomDieck09} [[Tammo tom Dieck]], section 4.4. in _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))


Exposition in relation to [[equivariant K-theory]]:

* [[Akhil Mathew]], _[Equivariant K-theory](https://amathew.wordpress.com/2011/12/03/equivariant-k-theory/)_

Classical results for [[compact Lie groups]]:

* [[Graeme Segal]], _The representation ring of a compact Lie group_, Publications Math&#233;matiques de l'Institut des Hautes &#201;tudes Scientifiques, January 1968, Volume 34, Issue 1, pp 113-128 ([NUMDAM](http://archive.numdam.org/numdam-bin/fitem?id=PMIHES_1968__34__113_0))

* Masaru Tackeuchi, _A remark on the character ring of a compact Lie group_, J. Math. Soc. Japan Volume 23, Number 4 (1971), 555-705 ([Euclid](http://projecteuclid.org/euclid.jmsj/1259849785))


In the generality of [[super Lie groups]]:

* [[Gregory Landweber]], _Representation rings of Lie superalgebras_, K-Theory 36 (2005), no. 1-2, 115-168 ([arXiv:math/0403203](http://arxiv.org/abs/math/0403203))

* [[Gregory Landweber]], _Twisted representation rings and Dirac induction_, J. Pure Appl. Algebra 206 (2006), no. 1-2, 21-54 ([arXiv:math/0403524](http://arxiv.org/abs/math/0403524))

With an eye towards [[loop group representations]]:

* {#Brylinski90} [[Jean-Luc Brylinski]], _Representations of loop groups, Dirac operators on loop space, and modular forms_, Topology, 29(4):461&#8211;480, 1990.

The [[Lambda-ring]]-structure via [[Adams operations]] is discussed in

* {#Meir17} Ehud Meir, Markus Szymik, _Adams operations and symmetries of representation categories_ ([arXiv:1704.03389](https://arxiv.org/abs/1704.03389))

[[!redirects representation rings]]
