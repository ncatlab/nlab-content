
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
#### Super-Algebra and Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

<center>
<img src="https://ncatlab.org/nlab/files/GrassmannGradedCommutativityI.jpg" width="460">
</center>
<center>
<img src="https://ncatlab.org/nlab/files/GrassmannGradedCommutativityII.jpg" width="460">
</center>


> from [Grassmann 1844, p. 61 and 84](Ausdehnungslehre#Grassmann44)


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

### Basic idea

In the general sense, _superalgebra_ is the study of ([[higher algebra|higher]]) [[algebra]] 

* [[internalization|internal]] to the [[symmetric monoidal category]] of $\mathbb{Z}_2$-[[graded vector spaces]] ([[super vector spaces]]);

equivalently 

* over the [[base topos]] on [[superpoints]].

More specifically, a _[[supercommutative superalgebra]]_ is an [[commutative algebra]] in the context of superalgebra. 

See at _[[geometry of physics -- superalgebra]]_ for more on this.

In the following we first discuss

* _[Associative superalgebras](#AssociativeSuperalgebras)_

as [[monoids]] in the [[symmetric monoidal category]] of [[super vector spaces]]. Then we pass to the perspective of

* _[Algebra in the topos over superpoints](#AlgebraOverSuperpoints)_

and consider systematically [[algebra]] in the [[sheaf topos]] over the [[site]] of [[superpoints]] and show how this reproduces and generalizes the previous notions.

See ([Sachse](#Sachse)) and the references at _[[super ∞-groupoid]]_ for some history of the topos-theoretic perspective on superalgebra.


### Abstract idea
 {#AbstractIdea}

We discuss the general abstract _raison d' &#234;tre_ of super algebra. Readers looking for just the plain definition should probably [skip to below](#AssociativeSuperalgebras) on first reading.

One way to understand the relevance of [[supercommutative superalgebra]] is [[Deligne's theorem on tensor categories]], which states that well-behaved [[tensor categories]] over the [[complex numbers]] are [[equivalence of categories|equivalent]] to [[categories of representations]] of [[supergroups]]. From this perspective the crucial sign rule is related to the [[symmetric monoidal category|symmetric]] [[braided monoidal category|braiding]] in [[tensor categories]]. This in turn may itself be understood from a more general perspective as follows.

Superalgebra is [[universal property|universal]] in the following sense. The crucial super-grading rule (the "Koszul sign rule", [Grassmann 1844, &#167;37, &#167;55](#Grassmann1844)) 

$$
  a \otimes b = (-1)^{deg(a) deg(b)} b \otimes a
$$

in the [[symmetric monoidal category]] of $\mathbb{Z}$-[[graded vector spaces]] is induced from the [[subcategory]] which is the [[abelian 2-group]] of metric graded [[lines]]. This in turn is the [[free construction|free]] [[abelian 2-group]] (groupal [[symmetric monoidal category]]) on a single generator.  (This point of view is amplified in the first part of ([Kapranov 13](#Kapranov13)), whose second part is about [[super 2-algebra]], more details in [Kapranov 15](#Kapranov15)). Generally then super-grading and hence super-algebra arises from the [[truncated object|2-truncation]] (3-[[coskeleton]]) of the free [[abelian ∞-group]] on a single generator, which is the [[sphere spectrum]] $\mathbb{S}$. So the $\mathbb{Z}_2$-grading of superalgebra comes from the [[stable homotopy groups of spheres]] $\pi_n(\mathbb{S})$ in degree 1 and 2:

| $n = $ | $0$ | $1$ | $2$ | $3$ | $4$ | $5$ | $6$ | $7$ | $\cdots$ | 
|--------|-----|-----|-----|-----|-----|-----|-----|-----|--|
| $\pi_n(\mathbb{S}) = $ | $\mathbb{Z}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ | $\mathbb{Z}_{24}$ | $ 0 $ | $0$ | $\mathbb{Z}_2$ | $\mathbb{Z}_{240}$ | $\cdots$ |
| meaning: | degree | [[boson]]/[[fermion]] super-degree | [[spin geometry|spin]] | [[string geometry|string]] | $-$ | $-$ | ? | ? | $\cdots$ |
| [[free construction|free object]] on single [[generators and relations|generator]]: | [[abelian group]] | [[abelian 2-group]] | [[abelian 3-group]] | [[abelian 4-group]] |  |  | [[abelian 7-group]] | [[abelian ∞-group|abelian 8-group]] | [[abelian ∞-group]] | 



This suggests (as indicated in ([Kapranov 13](#Kapranov13), [Kapranov 15](#Kapranov15))) that in full generality [[higher geometry|higher]] [[supergeometry]] is to be thought of as $\mathbb{S}$-[[graded object|graded]] geometry, hence [[Isbell duality|dually]] as [[higher algebra]] with [[∞-group of units]] [[augmented ∞-group|augmented]] over the [[sphere spectrum]]. 

But notice that this is canonically so for every [[E-∞ ring]], see at _[∞-group of units -- Augmented definition](infinity-group+of+units#AugmentedDefinition)_. This would mean: In [[higher geometry]]/[[higher algebra]] supergeometry/superalgebra is intrinsic, canonically given. 


Using this together with [[Hisham Sati|Sati]]'s _[[Geometric and topological structures related to M-branes]]_ and the [[image of the J-homomorphism]]

[[!include image of J -- table]]


we can derive the terminology in the above table as indicated now. 

> The following uses the notions of _[[motivic quantization]]_ as indicated there, to be expanded.

* **$d = 1$ [[sigma-model]]** 

  The [[local coefficients]] for [[quantization|quantizing]] the ([[spinning particle|spinning]]) [[particle]] on the [[boundary]] of the [[string]] ending on a [[D-brane]] (by K-theoretic [[geometric quantization by push-forward]]/[[D-brane charge]]) are

  $$
    \array{   
      B BU(1)
      &\simeq&
      B K(\mathbb{Z},2)
      &\to& 
      B gl_1(KU) 
      &\to&
      KU \text{-}Mod
    }
  $$

  for $KU$ the [[complex K-theory spectrum]] [[E-∞ ring]], and
  hence the characteristic twists are in degree 2 of the group of units, hence of the [graded ∞-group of units](infinity-group%20of%20units#AugmentedDefinition)

  $$
    gl^{gr}_1(KU) \to \mathbb{S}
  $$

  hence are graded by the second [[homotopy group]] 

  $$  
    \pi_2(\mathbb{S}) \simeq \mathbb{Z}_2
  $$

  of the sphere spectrum.

* **$d = 2$ [[sigma-model]]** 

  The [[local coefficients]] for [[quantization|quantizing]] the [[string]] (on the [[boundary]] of the [[M2-brane]] ending on an [[M9-brane]]) are

  $$
    \array{   
      B B^2 U(1)
      &\simeq&
      B K(\mathbb{Z},3)
      &\to& 
      B gl_1(tmf) 
      &\to&
      tmf \text{-}Mod
    }
  $$

  for the [[tmf]] [[E-∞ ring]], and
  hence the characteristic twists are in degree 3 of the group of units, hence of the graded group of units

  $$
    gl^{gr}_1(tmf) \to \mathbb{S}
  $$

  hence are graded by the third [[homotopy group]] 

  $$  
    \pi_3(\mathbb{S}) \simeq \mathbb{Z}_{24}
  $$

  of the sphere spectrum.

* **$d = 5$ [[sigma-model]]** 

  The [[local coefficients]] for [[quantization|quantizing]] the [[Yang monopole]] (on the [[boundary]] of the [[M5-brane]] ending on an [[M9-brane]]) are

  $$
    \array{   
      B B^5 U(1)
      &\simeq&
      B K(\mathbb{Z},6)
      &\to& 
      B gl_1(K(5)) 
      &\to&
      K(5) \text{-}Mod
    }
    \,,
  $$

  and
  hence the characteristic twists are in degree 6 of the group of units, hence of the graded group of units

  $$
    gl^{gr}_1(K(5)) \to \mathbb{S}
  $$

  hence are graded by the sixth [[homotopy group]] 

  $$  
    \pi_6(\mathbb{S}) \simeq \mathbb{Z}_{2}
  $$

  of the sphere spectrum.


## Associative superalgebras
 {#AssociativeSuperalgebras}

### Definition

#### Superalgebras

An ordinary [[associative algebra]] (a [[vector space]] with a linear and associative and unital product operation) is a [[monoid]] in the [[monoidal category]] [[Vect]] of [[vector spaces]].

Throughout, fix a [[field]] $k$ of [[characteristic]] 0.

+-- {: .num_defn #SuperVectorSpaces}
###### Definition

Write [[SVect]] for the [[symmetric monoidal category]] of [[super vector space]]s over $k$. This is the [[category]] of $\mathbb{Z}_2$-[[graded vector space]]s equipped with the unique non-trivial symmetric [[braided monoidal category|braided monoidal structure]].

Objects are vector spaces with a [[direct sum]] decomposition

$$
  V = V_{even} \oplus V_{odd}
$$

and the [[tensor product]] is given in terms of that on vector spaces by

$$
  V \otimes W = 
  (V_{even} \otimes W_{even} \oplus V_{odd}\otimes W_{odd})
  \oplus
  (V_{even} \otimes W_{odd} \oplus V_{odd} \otimes W_{even})
$$

but equipped with the non-trivial braiding morphism

$$
  b_{V, W} : V \otimes W \to W \otimes V
$$

that is the usual braiding isomorphism of [[Vect]] on $V_{even} \otimes W_{even}$ and on $V_{even} \otimes W_{odd} \oplus V_{odd} \otimes W_{even}$ but is $(-1)$ times this on $V_{odd}\otimes W_{odd}$.

=--

+-- {: .num_defn #SuperAlgebras}
###### Definition

A **super (associative) algebra** over $K$ is a [[monoid]] in the [[symmetric monoidal category]] [[SVect]] of [[super vector space]]s.

A **[[graded commutative algebra|(graded)-commutative (associative) algebra]]** over $K$ is a [[commutative monoid in a symmetric monoidal category | commutative monoid]] in the [[symmetric monoidal category]] [[SVect]] of [[super vector space]]s.

=--

This means that a commutative superalgebra is a [[super vector space]]

$$
  A = A_{even} \oplus A_{odd}
$$

equipped with a morphism of super vector spaces

$$
  (-)\cdot (-) : A \otimes A \to A
$$

that is associative and commutative in the usual sense. Specifically for the commutativity this means that with $a,b  \in A_{odd}$ we have

$$
  a \cdot b = - b \cdot a
  \,.
$$

Whereas if either of $a$ or $b$ is in $A_{even}$ we have

$$
  a \cdot b = b \cdot a
  \,.
$$

#### Related notions
 {#RelatedNotions}

+-- {: .num_defn #Center}
###### Definition

The **[[center]]** of a superalgebra $A$ is the sub-superalgebra $Z(A) \hookrightarrow A$ spanned by all those elements $z \in A$ of homogeneous degree which graded-commute with all other homogeneois elements $a$. 

=--

+-- {: .num_defn #Opposite}
###### Definition

For $A$ a superalgebra, its **opposite** $A^{op}$ is the superalgebra with the same underlying [[super vector space]] as $A$, and with multiplication defined on homogeneous elements by

$$
  a_1 \cdot_{A^{op}} a_2 \coloneqq (-1)^{{\vert a_1\vert}{\vert a_2\vert}} a_2 \cdot_{A} a_1
  \,.
$$

=--

+-- {: .num_defn #CentralSimple}
###### Definition

A superalgebra $A$ is called **central simple** if 

1. its [[center]], def. \ref{Center} is the ground field;

1. its only 2-sided graded [[ideals]] are $0$ and $A$ itself.

=--

+-- {: .num_defn #AlgWithBimodules}
###### Definition

Write $2sVect \simeq sAlg$ for the [[2-category]] equivalent to the one whose [[objects]] are superalgebra, [[1-morphisms]] are [[bimodules]] and [[2-morphisms]] are intertwiners. This is naturally a [[monoidal 2-category]].

=--

+-- {: .num_defn #2sVect}
###### Remark

By the discussion at _[[2-vector space]]_ this is equivalently the 2-category of **super 2-vector spaces**. [[equivalence|Equivalence]] in $2sVect \simeq sAlg$ is also called _[[Morita equivalence]]_ of super-algebras.

=--
+-- {: .num_defn #Azumaya}
###### Definition

A superalgebra is an [[Azumaya algebra]] if it is an invertible object in the [[monoidal 2-category]] $s2Vect \simeq sAlg$, def. \ref{AlgWithBimodules}.

=--

+-- {: .num_remark }
###### Remark

The group of [[equivalence classes]] of Azumaya super algebras is called the super _[[Brauer group]]_, see there for more details.

=--


### Examples


#### Endomorphisms algebras, matrix algebras

+-- {: .num_defn #EndomorphismSuperalgebra}
###### Definition

For $V \in SVect$ a [[super vector space]], its [[endomorphism ring]] is canonically a super-algebra. Superalgebras isomorphic to ones of this form, are also called **matrix super algebras**.

=--

+-- {: .num_prop #EndomorphismSuperalgebrasAreCentralSimple}
###### Proposition

A matrix superalgebra, def. \ref{EndomorphismSuperalgebra} is central simple, def. \ref{CentralSimple}.

=--


#### Grassmann algebra 
 
* For $V$ a [[vector space]] or [[graded vector space]] the [[Grassmann algebra]] $\wedge^\bullet V$ is a super algebra. This are the _free_ superalgebras.

#### Clifford algebra 

An class of examples of non-(graded)-commutative superalgebra 
are [[Clifford algebra]].

In fact, let $V$ be a [[vector space]] equipped with symmetric [[inner product]]
$\langle -,- \rangle$. Write $\wedge^\bullet V$ be the [[Grassmann algebra]] on $V$. The inner product makes this a super [[Poisson algebra]]. The [[Clifford algebra]] $Cl(V, \langle -,- \rangle)$ is the [[deformation quantization]] of this.

+-- {: .num_example #ComplexCl1}
###### Example

There is a superalgebra over the [[complex numbers]] of the form

$$
  A = \mathbb{C} \oplus \mathbb{C}\langle u\rangle
  \,,
$$

where the single odd generator satisfies $u \cdot u = 1$.

=--


### Properties
 {#Properties}

#### Relation to ordinary commutative algebras
 {#RelationToOrdinaryCommutativeAlgebra}

+-- {: .num_defn #InclusionOfCommutativeSuperalgebras}
###### Definition

Given some [[ground field]] $k$, write

$$
  \iota \colon CAlg_k \hookrightarrow SCAlg_k
$$

for the [[full subcategory]] of ordinary [[commutative algebras]]
over $k$ into [[supercommutative superalgebras]] (as those having trivial odd part).

=--

+-- {: .num_prop #AdjointsToInclusionOfPlainAlgebra}
###### Proposition

The inclusion $\iota$ of def. \ref{InclusionOfCommutativeSuperalgebras}
has 

1. a [[right adjoint]] $(-)_{even}$ given by restricting a superalgebra
to its even part;

1. a [[left adjoint]] $(-)/((-)_{odd})$ given by forming the "[[body]]", the [[quotient]] by the ideal generated by the odd part (by the "[[soul]]").


=--

This is immediate, but conceptually important, it is made explicit for instance in ([Carchedi-Roytenberg 12, example 3.18](#CarchediRoytenberg12)).

+-- {: .num_remark #AdjointTripleBetweenPlainAndSuperalgebra}
###### Remark

Prop. \ref{AdjointsToInclusionOfPlainAlgebra} 
gives an [[adjoint triple]] of the form

$$
  CAlg_k \stackrel{\overset{(-)/((-)_{odd})}{\longleftarrow}}{\stackrel{\hookrightarrow}{\underset{(-)_{even}}{\longleftarrow}}}
  SCAlg_k
$$

and hence an [[adjoint cylinder]], which induces a pair of [[adjoint modalities]] ([[fermionic modality]] $\dashv$ [[bosonic modality]]).
See at _[[super smooth infinity-groupoid]]_ for more on this.

=--


#### Relation to matrix algebras

+-- {: .num_prop }
###### Proposition

A superalgebra is isomorphic to a matrix algebra, def. \ref{EndomorphismSuperalgebra}, precisely if it is [[equivalence|equivalent]]  in  $2 sVect \simeq Alg$, def. \ref{AlgWithBimodules}, ([[Morita equivalence|Morita equivalent]]) to the ground field super algebra.

=--

#### Picard 3-group, Brauer group
 {#Picard2Groupoid}

We discuss the [[Picard 3-group]] of $2sVect \simeq sAlg$, def. \ref{AlgWithBimodules}, hence the corresponding [[Brauer group]]. See also at _[[super line 2-bundle]]_.

+-- {: .num_theorem #AzumayaAreCentralSimple}
###### Theorem

A superalgebra is invertible/Azumaya, def. \ref{Azumaya}, precisely if it is finite dimensional and central simple, def. \ref{CentralSimple}.

=--

This is due to ([Wall](#Wall)).

+-- {: .num_theorem }
###### Theorem

The [[Brauer group]] of superalgebras over the [[complex numbers]] is the [[cyclic group of order 2]]. That over the [[real numbers]] is cyclic of order 8:

$$
  sBr(\mathbb{C}) \simeq \mathbb{Z}_2
$$
$$
  sBr(\mathbb{R}) \simeq \mathbb{Z}_8
  \,.
$$

The non-trivial element in $sBr(\mathbb{R})$ is that presented by the superalgebra $\mathbb{C} \oplus \mathbb{C} u$ of example \ref{ComplexCl1}, with $u \cdot u = 1$.

=--

This is due to ([Wall](#Wall)).

The following generalizes this to the higher [[homotopy groups]].

+-- {: .num_prop }
###### Proposition

The [[homotopy groups]] of the [[braided 3-group]] $sAlg^\times$ of Azumaya superalgebra are

| | $sAlg^\times_{\mathbb{C}}$ | $sAlg^\times_{\mathbb{R}}$ |
|--|--|--|
| $\pi_2$ | $\mathbb{C}^\times$ | $\mathbb{R}^\times$
| $\pi_1$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$
| $\pi_0$ | $\mathbb{Z}_2$ | $\mathbb{Z}_8$

where the [[groups of units]] $\mathbb{C}^\times$ and $\mathbb{R}^\times$ are regarded as [[discrete groups]].

=--

This appears in ([Freed, (1.38)](#Freed)).


## Algebra in the topos over superpoints
 {#AlgebraOverSuperpoints}

We now consider [[higher algebra]] in the [[(∞,1)-topos]] over [[super points]]: the [[cohesive (∞,1)-topos]] $\mathbf{H} = $ [[Super∞Grpd]].

### The topos

+-- {: .num_defn}

###### Definition

Write $SuperPoint$ for the [[site]] of [[superpoint]]s. Write 

$$
  SuperSet := Sh(SuperPoint)
$$

for the [[sheaf topos]] (a [[presheaf topos]]) over this site.
Write 

$$
  Super \infty Grpd := Sh_{(\infty,1)}(SuperPoint)
$$

for the [[(∞,1)-sheaf (∞,1)-topos]] over this site: the [[(∞,1)-topos]] of [[super ∞-groupoid]]s.

=--

### The line object $\mathbb{R}$
 {#AlgebraInToposOverSuperPoints-TheLineObject}

+-- {: .num_defn #EmbeddingOfSupermanifoldsIntoSheavesOnSuperpoints}
###### Definition

Write

$$
  j \colon SuperSmthMfd \hookrightarrow Sh(SuperPoint)
$$

for the restricted [[Yoneda embedding]] of [[supermanifolds]] given by the canonical inclusion $SuperPoint \hookrightarrow SuperSmoothManifold$.

=--




+-- {: .num_defn #TheRealLine}
###### Definition

Write

$$
  \mathbb{R} := j(\mathbb{R}) \in Sh(SuperPoint)
$$

for the presheaf represented by the [[real line]], regarded as a [[supermanifold]]. Equipped with its canonical [[internalization|internal]] [[ring]] structure this is 

$$
  \mathbb{R} \in Ring(Sh(SuperPoint))
  \,.
$$

=--

+-- {: .num_remark}
###### Remark


By the discussion at [[supermanifold]] (in the section [As locally ringed spaces - Properties](http://ncatlab.org/nlab/show/supermanifold#AsLocallyRingedSpacesProperties)) $\mathbb{R}$ sends the formal dual of a [[Grassmann algebra]] to its even subalgebra

$$
  \mathbb{R}  : Spec \wedge^\bullet V \mapsto (\wedge^\bullet V)_{even}
  \,.
$$

This is canonically equipped with the structure of a (unital) [[commutative ring]] in $SuperSet$.


=--

In ([Sachse](#Sachse)) this appears around (21).


### $\mathbb{R}$-Modules
 {#SuperModulesAsbbKModules}

+-- {: .num_defn}
###### Definition

Write $Mod_{\mathbb{R}}(SuperSet)$ for the [[Mod|category of modules]] over $\mathbb{R}$ of def. \ref{TheRealLine} in $SuperSet$.

=--

+-- {: .num_prop #EmbeddingOfSVectIntoKMod}
###### Proposition

The restriction of the embedding of def. \ref{EmbeddingOfSupermanifoldsIntoSheavesOnSuperpoints} to supermanifolds which are [[super vector spaces]] is a [[functor]]

$$
  j : SVect_{\mathbb{R}} = Mod_{\mathbb{R}}(Set) \hookrightarrow Mod_{\mathbb{K}}(SuperSet)
$$

from real [[super vector spaces]]  to internal modules over $\mathbb{R}$ that sends $V \in SVect_{\mathbb{R}}$ to

$$
  j(V) : Spec \Lambda \mapsto (\Lambda \otimes_\mathbb{R} V)_{even}
  = 
  (\Lambda_{even} \otimes_\mathbb{R} V_{even})
    \oplus
  (\Lambda_{odd} \otimes_\mathbb{R} V_{odd})
  \,.
$$

This is a [[full and faithful functor]].

=--

This appears as ([Sachse, corollary 3.2](#Sachse)).

+-- {: .proof}
###### Proof

The proof is a variation on the [[Yoneda lemma]].

=--

This means that ordinary [[super vector spaces]] are embedded as a [[full subcategory]] in $\mathbb{K}$-modules in the topos over [[super points]].

### Associative and Lie Superalgebras

+-- {: .num_prop}
###### Proposition

The functor $j$ from prop \ref{EmbeddingOfSVectIntoKMod} induces a [[full and faithful functor]]

$$
  SAlg_{\mathbb{R}}(Set) \hookrightarrow Alg_{\mathbb{R}}(SuperSet)
$$

of superalgebras over $\mathbb{R}$ as in def. \ref{SuperAlgebras} and internal [[associative algebra]]s over $\mathbb{R}$ in $SuperSet$.

Similarly we have a faithful embedding

$$
  SLieAlg_{\mathbb{R}}(Set) \hookrightarrow LieAlg_{\mathbb{R}}(SuperSet)
$$

of ordinary [[super Lie algebras]] over $\mathbb{R}$ into the internal [[Lie algebras]] over $\mathbb{R}$ in $SuperSet$.

=--

This appears as ([Sachse, corollary 3.3](#Sachse)).

## Properties

(...)

## Related concepts

* [[super module]], [[super vector space]]

* [[supercommutative algebra]], [[differential graded-commutative superalgebra]]

  [[model structure on differential graded-commutative superalgebras]]

* [[smooth superalgebra]]

* [[supermanifold]]

* [[super 2-algebra]]


## References

### General

The concept of [[Grassmann algebra]] and the [[signs in supergeometry|super-sign rule]] is due to

* {#Grassmann1844} [[Hermann Grassmann]], _[[Ausdehnungslehre]]_ (1844):

Early modern account:

* [[Felix A. Berezin]] (edited by [[Alexandre A. Kirillov]]): *Introduction to Superanalysis*, Mathematical Physics and Applied Mathematics **9**, Springer (1987) &lbrack;[doi:10.1007/978-94-017-1963-6](https://link.springer.com/book/10.1007/978-94-017-1963-6)&rbrack; 


Review of basic superalgebra:

* [[Yuri Manin]], Chapter 3 in: *[[Gauge Field Theory and Complex Geometry]]*, Grundlehren der Mathematischen Wissenschaften **289**, Springer (1988) &lbrack;[doi:10.1007/978-3-662-07386-5](https://doi.org/10.1007/978-3-662-07386-5)&rbrack;

* [[Dennis Westra]], _Superrings and supergroups_, 2009 ([pdf](http://www.mat.univie.ac.at/~michor/westra_diss.pdf))

* {#DeligneMorgan99} [[Pierre Deligne]], [[John Morgan]], Ch 1 in: _Notes on Supersymmetry (following [[Joseph Bernstein]])_, in: *[[Quantum Fields and Strings]], A course for mathematicians*, **1**, Amer. Math. Soc. Providence (1999) 41-97 &lbrack;[ISBN:978-0-8218-2014-8](https://bookstore.ams.org/qft-1-2-s), [web version](http://www.math.ias.edu/qft), [[DeligneMorgan-NotesOnSusy.pdf:file]]&rbrack;

* {#Mirković04} [[Ivan Mirković]], Sec 1 in: *Notes on Super Math*, in *[Quantum Field Theory Seminar](https://people.math.umass.edu/~mirkovic/0.SEMINARS/1.QFT/Fall.04.html)*, lecture notes (2004)  &lbrack;[pdf](https://people.math.umass.edu/~mirkovic/0.SEMINARS/1.QFT/1.SuperMath/8.pdf), [[Mirkovic-NotesOnSupermathematics.pdf:file]]&rbrack;


Discussion of superalgebra as algebra in certain [[symmetric monoidal category|symmetric monoidal]] [[tensor categories]] is in 

* [[Pierre Deligne]], _Cat&#233;gorie Tensorielle_ ([pdf](https://www.math.ias.edu/files/deligne/Tensorielles.pdf))

(see also at [[Deligne's theorem on tensor categories]]).

Lecture notes include

* [[Daniel Freed]], _[[Five lectures on supersymmetry]]_

The observation that the study of super-structures in mathematics is usefully regarded as taking place over the [[base topos]] on the [[site]] of [[super points]] has been made around 1984 in

* [[Albert Schwarz]], _On the definition of superspace_, Teoret. Mat. Fiz. (1984)  Volume 60,  Number 1, Pages 37&#8211;42, ([russian original pdf](http://www.mathnet.ru/links/b12306f831b8c37d32d5ba8511d60c93/tmf5111.pdf))

* [[Alexander Voronov]], _Maps of supermanifolds_ , Teoret. Mat. Fiz. (1984)  Volume 60,  Number 1, Pages 43&#8211;48

and in 

* V. Molotkov., _Infinite-dimensional $\mathbb{Z}_2^k$-supermanifolds_ , ICTP
preprints, IC/84/183, 1984.


A summary/review is in the appendix of

* {#KonechnySchwarz} Anatoly Konechny and [[Albert Schwarz]], 

  _On $(k \oplus l|q)$-dimensional supermanifolds_ in _Supersymmetry and Quantum Field Theory_ ([[Dmitry Volkov]] memorial volume) Springer-Verlag, 1998, Lecture Notes in Physics, 509 , J. Wess and V. Akulov (editors)([arXiv:hep-th/9706003](http://arxiv.org/abs/hep-th/9706003))

  _Theory of $(k \oplus l|q)$-dimensional supermanifolds_ Sel. math., New ser. 6 (2000) 471 - 486
  

* [[Albert Schwarz]], I. Shapiro, _Supergeometry and Arithmetic Geometry_ ([arXiv:hep-th/0605119](http://arxiv.org/abs/hep-th/0605119))

For more along these lines see also the references at _[[supermanifold]]_ and at _[[super infinity-groupoid]]_.

Discussion in terms of [[smooth algebras]] ([[synthetic differential supergeometry]]) is in 

* {#CarchediRoytenberg12} [[David Carchedi]], [[Dmitry Roytenberg]], _On theories of superalgebras of differentiable functions_, Theory and Applications of Categories, Vol. 28, 2013, No. 30, pp 1022-1098. ([arxiv:1211.6134](http://arxiv.org/abs/1211.6134), [TAC](http://www.tac.mta.ca/tac/volumes/28/30/28-30abs.html))


### Brauer groups and Picard 2-groupoid

[[Brauer groups]] of superalgebras are discussed in 

* [[Daniel Freed]], Lectures on twisted K-theory and orientifolds ([pdf](http://www.ma.utexas.edu/users/dafr/ESI.pdf))
 {#Freed}

* [[C. T. C. Wall]], _Graded Brauer groups_, J. Reine Angew. Math. 213 (1963/1964), 187-199. 
 {#Wall}

* [[Pierre Deligne]], _Notes on spinors_ in _[[Quantum Fields and Strings]]_

* [[Peter Donovan]], [[Max Karoubi]], _Graded Brauer groups and K-theory with local coefficients_, Publications Math. IHES 38 (1970), 5-25 ([pdf](http://www.math.jussieu.fr/~karoubi/Donavan.K.pdf))

See also at _[[super line 2-bundle]]_ for more on this.

Discussion of superalgebra as induced from free groupal symmetric monoidal categories ([[abelian 2-groups]]) and hence ultimately from the [[sphere spectrum]] is in 

* {#Kapranov13} [[Mikhail Kapranov]], _Categorification of supersymmetry and stable homotopy groups of spheres_, talk at _[Algebra, Combinatorics and Representation Theory: in memory of Andrei Zelevinsky (1953-2013)](https://web.archive.org/web/20130617191515/http://mathserver.neu.edu/~bwebster/ACRT/)_ (April 2013) &lbrack;[[Webster-ACRTAbstracts2013.pdf:file]],  video:[YT](https://www.youtube.com/watch?v=WBsZrcYOrxI)&rbrack;

  > **Abstract:**. The "minimal sign skeleton" necessary to formulate the [[signs in supergeometry|Koszul sign rule]] is a certain [[Picard category]], a [[symmetric monoidal category]] with all [[invertible object|objects]] and [[invertible morphism|morphisms invertible]]. It can be seen as the free Picard category generated by one object and corresponds, by [[Grothendieck]]'s dictionary, to the [[n-truncation|truncation]] of the [[sphere spectrum|spherical spectrum]] $S$ in degrees 0 and 1, so that $\{\pm 1\}$ appears as the [[first stable homotopy group of spheres]] $\pi_{n+1}(S^n)$. This suggest a "[[higher structures|higher]]" or [[categorification|categorified]] versions of [[super-algebra|super-mathematics]] which utilize deeper structure of [[sphere spectrum|$S$]]. The first concept on this path is that of a supersymmetric monoidal category which is [[categorification|categorified]] version of the concept of a [[supercommutative algebra]].

  > (cf. *[[super 2-algebra]]* and *[[spectral super-scheme]]*)

* {#Kapranov15} [[Mikhail Kapranov]], _Supergeometry in mathematics and physics_, in [[Gabriel Catren]], [[Mathieu Anel]], (eds.) _[[New Spaces for Mathematics and Physics]]_ ([arXiv:1512.07042](http://arxiv.org/abs/1512.07042))

* {#Kapranov15b} [[Mikhail Kapranov]], _Super-geometry_, talk at _[New Spaces for Mathematics & Physics](http://ercpqg-espace.sciencesconf.org/program)_, IHP Paris (Oct-Sept 2015) &lbrack;[video recording](https://www.youtube.com/watch?v=bjsNwKYT8JE)&rbrack;


[[!redirects super algebras]]

[[!redirects superalgebra]]
[[!redirects super-algebra]]



[[!redirects superalgebras]]

[[!redirects even rules]]

[[!redirects commutative superalgebra]]
[[!redirects commutative superalgebras]]
[[!redirects commutative super-algebra]]
[[!redirects commutative super-algebras]]
[[!redirects super-commutative superalgebra]]
[[!redirects super-commutative superalgebras]]
[[!redirects super-commutative super-algebra]]
[[!redirects super-commutative super-algebras]]