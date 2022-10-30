

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Operator algebra
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Noncommutative geometry
+--{: .hide}
[[!include noncommutative geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_KK-theory_ is a "bivariant" joint generalization of [[operator K-theory]] and [[K-homology]]: for $A, B$ two [[C*-algebras]], the _KK-group_ $KK(A,B)$ is a natural [[homotopy]] [[equivalence class]] of $(A,B)$-[[Hilbert bimodules]] equipped with an additional left weak [[Fredholm module]] structure. These KK-groups $KK(A,B)$ behave in the first argument as [[K-homology]] of $A$ and in the second as [[K-cohomology]]/[[operator K-theory]] of $B$.

Abstractly, KK-theory is an [[additive category]] of [[C*-algebras]] which is the split-[[exact functor|exact]] and [[homotopy]]-invariant [[localization]] of [[C*Alg]] at the [[compact operators]]. Hence, abstractly KK-theory is a fundamental notion in [[noncommutative topology]], but its standard presentation by [[Fredholm module|Fredolm]]-[[Hilbert bimodules]] as above is rooted in [[functional analysis|functional]] [[analysis]]. A slight variant of this localization process is called _[[E-theory]]_.

Due to this joint root in [[functional analysis]] and ([[noncommutative topology|noncommutative]]) [[cohomology]]/[[homotopy theory]] ("[[noncommutative stable homotopy theory]]"), KK-theory is a natural home of [[index theory]], for [[elliptic operators]] on [[smooth manifolds]] as well as for their generalization to [[equivariant cohomology|equivariant]] situations, to [[foliations]] and generally to [[Lie groupoid]]-theory (via their [[groupoid convolution C*-algebras]]) and [[noncommutative geometry]].

As a special case of this, [[quantization]] in its incarnation as [[geometric quantization by push-forward]] has been argued to naturally proceed by [[index theory]] in KK-theory ([Landsman 03](#Landsman03), [Bos 07](#Bos07)). Also the coupling of [[D-branes]] and their [[Chan-Paton bundles]] in [[twisted K-theory]] with [[RR-charge]] in [[string theory]] is naturally captured by the coupling between [[K-homology]] and [[K-cohomology]] in KK-theory (e.g. [Szabo 08](#Szabo)).

## Definition

We state first the original and standard definition of $KK$-groups in terms of [[equivalence classes]] of [[Fredholm module|Fredholm]]-[[Hilbert C*-module|Hilbert C*]]-[[Hilbert bimodules|bimodules]] in 

* [In terms of Fredholm Hilbert C-star-bimodules](#InTermsOfFredholmHilbertBimodules)

Then we state the abstract [[category theory|category-theoretic]] characterization by [[localization]] in

* _[Universal category-theoretic characterization](#UniversalCharacterization). 

An equivalent and explicity [[homotopy theory|homotopy theoretic]] characterization akin to that of the standard [[homotopy category]] [[Ho(Top)]] is in  

* [In terms of homotopy classes of star-homomorphisms](#RelationToHomotopyClassesOfStarHomomorphisms).


### In terms of Fredholm-Hilbert $C^\ast$-bimodules
 {#InTermsOfFredholmHilbertBimodules}

+-- {: .num_defn }
###### Definition

In all of the following, "$C^\ast$-algebra" means _[[separable topological space|separable]]_ [[C*-algebra]]. We write [[C*Alg]] for 
for the [[category]] whose [[objects]] are separable $C^\ast$-algebras and whose [[morphisms]] are $\ast$-[[homomorphisms]] between these.

=--

+-- {: .num_example }
###### Example

We write

* $\mathcal{B} \coloneqq \mathcal{B}(\mathcal{H})$ for the $C^\ast$-algebra of [[bounded operators]] on a complex, infinite-dimensional separable [[Hilbert space]]; 

* $\mathcal{K} \coloneqq \mathcal{K}(\mathcal{H}) \hookrightarrow \mathcal{B}(\mathcal{H})$ for the [[compact operators]].

=--

+-- {: .num_defn #HilbertCStarModule}
###### Definition

For $B \in $ [[C*Alg]], a [[Hilbert C*-module]] over $B$ is 

1. a [[complex numbers|complex]] [[vector space]] $H$;

1. equipped with a [[C*-representation]] of $B$ from the right;

1. equipped with a [[sesquilinear map]] (linear in the second argument)

   $$
     \langle -,-\rangle \colon H \times H \to B
   $$

   (the $B$-valued [[inner product]])

such that 

1. $\langle -,-\rangle$ behaves indeed like a positive definitine inner product over $B$:

   1. $\langle x,y\rangle^\ast = \langle y,x\rangle$

   1. $\langle x,x\rangle \geq 0$ (in the sense of [[positive elements]] in $B$)

   1. $\langle x,x\rangle = 0$ precisely if $x = 0$;

   1. $\langle x,y \cdot b\rangle = \langle x,y \rangle \cdot b $

1. $H$ is [[complete space|complete]] with respect to the [[norm]]:

   ${\Vert x \Vert_H} \coloneqq {\Vert \langle x,x\rangle\Vert_B}$.

=--

+-- {: .num_defn #HilbertBimodule}
###### Definition

For $A,B \in C^\ast Alg$ an $(A,B)$-[[Hilbert C*-bimodule]] is an $B$-[[Hilbert C*-module]], def. \ref{HilbertCStarModule} $(H, \langle \rangle)$ equipped with a [[C-star representation]] of $A$ from the left such that all $a \in A$ are "adjointable" in the $B$-valued inner product, meaning that

$$
  \langle a^\ast \cdot x,y\rangle = \langle x, a y\rangle
  \,.
$$


=--


+-- {: .num_defn }
###### Definition

For $A, B \in $ [[C*Alg]], **Kasparov $(A,B)$-bimodule**
is n $\mathbb{Z}_2$-[[graded vector space|graded]] $(A,B)$-[[Hilbert bimodules]] $\mathcal{H}, \langle -,-\rangle$, def. \ref{HilbertBimodule}, equipped with an adjointable odd-graded [[bounded operator]] $F \in \mathcal{B}_A(\mathcal{H})$ such that 

1. $\pi(a)(F^2 - 1) \in \mathcal{K}_A(\mathcal{H})$ 

1. $[\pi(a), F] \in \mathcal{K}_A(\mathcal{H})$ for all $a \in A$. 

=--

+-- {: .num_example }
###### Example

For $B = \mathbb{C}$ a Kasparov $(A,B)$-bimodule is equivalently an $A$-[[Fredholm module]].

=--

+-- {: .num_defn #HomotopyOfKasparovBimodules}
###### Definition

A [[homotopy]] between two Kasparov $(A,B)$-bimodules is an $(A, C([0,1],B))$-bimodule which interpolates between the two.

(...)

=--

+-- {: .num_defn }
###### Definition

Writes $KK(A,B)$ for the set of [[equivalence classes]] of Kasparov $(A,B)$-bimodules under homotopy, def. \ref{HomotopyOfKasparovBimodules}.

=--

+-- {: .num_prop }
###### Proposition

$KK(A,B)$ is naturally an [[abelian group]] under [[direct sum]] of bimodules and operators.

=--

+-- {: .num_prop #KasparovProduct}
###### Proposition

There is a composition operation

$$
  KK(A,B) \times KK(B,C) \to KK(A,C)
$$

such that (...). This is called the **Kasparov product**.

=---

A streamlined version of the definition of the Kasparov product is in ([Skandalis 84](#Skandalis84)). 

+-- {: .num_remark}
###### Remark

From the point of view of [[E-theory]] the Kasparov product is equivalently just the composition of homotopy classes of completely poistive [[asymptotic C*-homomorphisms]]. See at _[[E-theory]]_ for more on this.

=--




### Universal category-theoretic characterization
 {#UniversalCharacterization}

+-- {: .num_prop #KasparovProductIsAssociative}
###### Proposition

The Kasparov product, def. \ref{KasparovProduct}, is [[associativity|associtative]]. Thus under the Kasparov product

$$
  KK(-,-) \;\colon\; C^\ast Alg \times C^\ast Alg \to C^\ast Alg
$$

is the [[hom-functor]] of an [[additive category]]. 

=--

([Higson 87, theorem 4.1](#Higson))


The category $KK$ is a kind of [[localization]] of the category of [[C-star-algebras]]:

+-- {: .num_theorem #KKIsAdditiveSplitExactLocalizationAtCompacts}
###### Theorem

The canonical functor

$$
  Q \colon C^\ast Alg \to KK
$$

exhibits $KK$ as the [[universal property|universal category]] receiving a functor from [[C*-algebras]] such that

1. $KK$ is an [[additive category]];

1. $Q$ is homotopy-invariant;

1. $Q$ [[isomorphism|inverts]] the [[tensor product]] with the [[C*-algebra]] of [[compact operators]]

   (for all $C^\ast$-homomorphisms of the form $id \otimes e \langle e,- \rangle \;\colon A\; \to A \otimes \mathcal{K}$ the morphism $Q(id \otimes e \langle e)$ is an [[isomorphism]]).

1. $Q$ preserves [[split short exact sequences]].

=--

This is due to ([Higson 87, theorem 4.5](#Higson)). The generalization to the equivariant case is due to ([Thomsen 98](#Thomsen98)).

+-- {: .num_cor }
###### Corollary

The minimal [[tensor product of C-star-algebras]]

$$
  \otimes \colon C^\ast Alg \times C^\ast Alg \to C^\ast Alg
$$

extends uniquely to a [[tensor product]] $\otimes_{KK}$ on $KK$ such that there is a [[commuting diagram]] of [[functors]]

$$
  \array{
    C^\ast Alg \times C^\ast Alg &\stackrel{Q \times Q}{\to}& KK
    \\
    \downarrow^{\mathrlap{\otimes}} && \downarrow^{\mathrlap{\otimes_{KK}}}
    \\
    C^\ast Alg &\stackrel{Q}{\to}& KK
  }
  \,.
$$

=--

([Higson 87, theorem 4.8](#Higson))

For more discussion of more explicit presentations of this [[localization]] process for obtaining KK-theory see at _[[homotopical structure on C*-algebras]]_ and also at _[[model structure on operator algebras]]_.


### Relation to homotopy-classes of $\ast$-homomorphisms
 {#RelationToHomotopyClassesOfStarHomomorphisms}

Theorem (Cuntz)

If $A,B$ are [[C-star-algebras]] with $A$ separable and $B$ $\sigma$-unital, then 

$$
  KK(A,B) \simeq [q A, B \otimes \mathcal{K}]
  \,,
$$

where

* $q A$ is the [[kernel]] of the [[codiagonal]] $A \star A \to A$,

* $\mathcal{K}$ is the $C^\ast$-algebra of [[compact operators]].

* $[-,-]$ is the set of [[homotopy]] [[equivalence classes]] of $\ast$-[[homomorphisms]].

(reviewed in ([Joachim-Johnson07](#JoachimJohnson07))).

## Properties


### Relation to operator K-cohomology, K-homology, twisted K-theory
 {#RelationToKCohomologyAndTwistedKTheory}

KK-theory is a joint generalization of [[operator K-theory]], hence also of [[topological K-theory]], as well as of [[K-homology]] and of [[twisted K-theory]].

For $A \in $ [[C*Alg]] we have that 

* $KK(\mathbb{C}, A) \simeq K_0(A)$ 

is the [[operator K-theory]] group of $A$ in degree 0 and

* $KK(C(\mathbb{R}^1),A) \simeq K_1(A)$

is the [[operator K-theory]] group of $A$ in degree 1. (e.g. ([Introduction, p. 20](#Introduction)). If here $A = C(X)$ is the [[C*-algebra]] of functions on a suitable [[topological space]] $X$, then this is the [[topological K-theory]] of that space

* $KK(\mathbb{C}, C(X)) \simeq K^0(X)$

* $KK(C(\mathbb{R}), C(X)) \simeq K^1(X)$.

More generally, if $A = C_r(\mathcal{G}_\bullet)$ is the reduced [[groupoid convolution algebra]] of a [[Lie groupoid]], then 

* $KK(\mathbb{C}, C_r(\mathcal{G}_\bullet)) \simeq K^0(\mathcal{G})$

is the K-theory of the corresponding [[differentiable stack]]. If moreover $c \colon \mathcal{G} \to \mathbf{B}^2 U(1)$ is a [[circle 2-group]]-[[principal 2-bundle]] ($U(1)$-[[bundle gerbe]]) over $\mathcal{X}$ and if $A = C(\mathcal{X}_\bullet, c)$ is the  [[twisted groupoid convolution algebra]] of the corresponding [[centrally extended Lie groupoid]], then 

* $KK(\mathbb{C}, C_r(\mathcal{X}_\bullet,x)) = K^0(\mathcal{X}, c)$ 

is the corresponding [[twisted K-theory]] ([Tu, Xu, Laurent-Gengoux 03](#TXLG)).


On the other hand, with $A$ in the first argument and the complex numbers in the second we have that

* $K(A,\mathbb{C}) \simeq K^0(A)$

ar equivalence classes of $A$-[[Fredholm modules]] and hence the [[K-homology]] of $A$.

(...)

### Relation to extensions

There is an [[isomorphism]]

$KK(A,B) \simeq Ext^1(A,B)$

to a suitable group of suitable [[extensions]] of $A$ by $B$. ([Kasparov 80](#Kasparov80), reviewed in [Inassaridze](#Inassaridze)).

### Triangulated (stable) structure

+-- {: .num_prop }
###### Proposition

$KK$ is naturally a stable [[triangulated category]].

=--

([Meyer 07](#Meyer), [Uuye 10, theorem 2.29](#Uuye10)).

### Excision and relation to E-theory

+-- {: .num_defn }
###### Definition

Given a [[short exact sequence]] of [[C*-algebras]] one says that $KK$ satisfies **[[excision]]** or that it is **excisive** for this sequence if it preserves its [[exact sequence|exactness]] in the middle.

=--

+-- {: .num_example }
###### Example

By theorem \ref{KKIsAdditiveSplitExactLocalizationAtCompacts}, $KK$ is excisive over [[split exact sequences]].

=--

+-- {: .num_prop }
###### Proposition

$KK$ is excisive for [[nuclear C*-algebras]] in the first argument.

=--

This is discussed ([Kasparov 80, section 7](#Kasparov80)), ([Cuntz-Skandalis 86](#CuntzSkandalis86)).

More generally:

+-- {: .num_prop }
###### Proposition

$KK$ is excisive for [[K-nuclear C*-algebras]] in the first argument.

=--

([Skandalis 88](#Skandalis88))

+-- {: .num_remark }
###### Remark

It is not expected that excision is satisfied fully generally by $KK$. Instead, the [[universal property|universal]] improvement of $KK$-theory under excision can be constructed. This is called _[[E-theory]]_. See there for more.

=--

### Poincar&#233; duality and Thom isomorphism

+-- {: .num_prop #PoincareDuality}
###### Proposition

Let $X$ be a [[smooth manifold]] which is [[compact topological space|compact]]. Then the [[C*-algebra]] $C(X) \otimes C_0(T^\ast X)$
(the tensor product of the algebra of functions of compact supposer on $X$ and on its [[cotangent bundle]]) is isomorphic, in $KK$, to $\mathbb{C}$:

$$
  d \colon C(X) \otimes C_0(T^\ast X) \stackrel{\simeq}{\to}  
  \mathbb{C}
  \,.
$$

=--

([Kasparov 80](#Kasparov80))

+-- {: .num_cor }
###### Corollary

For $X$ a [[compact topological space|compact]] [[smooth manifold]], there is a [[natural isomorphism]] ([[Thom isomorphism]])

$$
  K_0( C_0(T^\ast X))
    \simeq
  KK(\mathbb{C}, C_0(T^\ast X))
    \stackrel{KK(C,(-)\otimes C(X))}{\to}
  KK(C(X), C(X) \otimes C_0(T^\ast X) )
    \underoverset{\simeq}{KK(C(X), d)}{\to}
  KK(C(X), \mathbb{C} )
  \,.
$$

=--




## Further Theorems

* The [[Baum-Connes conjecture]] is naturally formulated within KK-theory.

* The [[Novikov conjecture]] has been verified in many cases using KK-theory. (see for instance [Roseberg 80](#Rosernberg80)).

* The [[Atiyah-Singer index theorem]] is naturally formutaled in KK-theory/[[E-theory]]. (See ([Higson-Roe](#HigsonRoe))).

## Related concepts

* [[operator K-theory]]

  * [[E-theory]]

* [[homotopical structure on C*-algebras]], [[model structure on operator algebras]]

## References

### General

KK-theory was introduced by [[Gennady Kasparov]] in 

* [[Gennady Kasparov]], _The operator $K$-functor and extensions of $C^{\ast}$-algebras_, Izv. Akad. Nauk SSSR Ser. Mat. __44__  (1980), no. 3, 571&#8211;636, 719, [MR81m:58075](http://www.ams.org/mathscinet-getitem?mr=582160), [Zbl](http://www.zentralblatt-math.org/zmath/search/?an=Zbl%200464.46054%7CZbl%200448.46051), [abstract](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=im&paperid=1739&option_lang=eng), [english doi](http://dx.doi.org/10.1070%2FIM1981v016n03ABEH001320), free Russian original: [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=im&paperid=1739&volume=44&year=1980&issue=3&fpage=571&what=fullt&option_lang=eng)
 {#Kasparov80}

prompted by the advances in [[Brown-Douglas-Fillmore theory]], especially in the last 1977 article.

Some streamlining of the definitions appeared in

* [[Georges Skandalis]], _Some remarks on Kasparov theory_, J. Funct. Anal. 59 (1984) 337-347.
 {#Skandalis84}

A textbook account is in 

* B. Blackadar, _K-theory for Operator Algebras_, 2nd ed. Cambridge University Press, Cambridge (1999)

Introductions and surveys include

* [[Gennady Kasparov]], _Operator K-theory and its applications: elliptic operators, group representations, higher signatures $C^\ast$-extensions_, Proceedings ICM 1983 Warszawa, PWN-Elsevier (1984) 987-1000.

* [[Nigel Higson]], _A primer on KK-theory_. Proc. Sympos. Pure Math. 51, Part 1, 239&#8211;283. (1990) ([pdf](http://www.math.psu.edu/higson/math/Papers_files/Higson%20-%201990%20-%20A%20primer%20on%20KK-theory.pdf))

* [[Georges Skandalis]], _Kasparov's bivariant K-theory and applications_ Exposition. Math. 9, 193&#8211;250 (1991) ([pdf slides](http://www.math.vanderbilt.edu/~bisch/ncgoa08/talks/skandalis2.pdf))

* _Introduction to KK-theory and E-theory_, Lecture  notes (Lisbon 2009) ([pdf slides](http://oaa.ist.utl.pt/files/cursos/courseD_Lecture4_KK_and_E1.pdf))
 {#Introduction}

* Heath Emerson, [[R. Meyer]] (notes taken by S. Hong), _KK-theory and Baum-Connes conjecture_, Lectures at _Summer school on operator algebras and noncommutative geometry_ (June 2010) ([pdf](http://www.pims.math.ca/files/EM_%20KK-theory_BC_Conjecture.pdf))

### Excision

Excision for KK-theory is further studied in 

* [[Joachim Cuntz]], [[Georges Skandalis]], _Mapping cones and exact sequences in KK-theory_, J. Operator Theory 15 (1986) 163-180.
 {#CuntzSkandalis86}

* [[Georges Skandalis]], _Une notion de nuclearit&#233; en K-theorie_, K-Theory 1 (1988) 549-574.
 {#Skandalis88}


### In Category theory and Homotopy theory

KK-theory is naturally understood in terms of [[universal properties]] in [[category theory]] and in [[homotopy theory]].

That $KK(A,B)$ is naturally thought of as a collection of "generalized [[homomorphisms]]" of $C^\ast$-algebras was amplified in 

* [[Joachim Cuntz]], _Generalized Homomorphisms Between C*'-algebras and KK-theory, Springer Lecture Notes in Mathematics, 1031 (1983), 31-45.

* [[Joachim Cuntz]], _K-theory and C*-algebras_, Springer Lecture Notes in Mathematics, 1046 (1984), 55-79.

That under the Kasparov product these are indeed the [[hom-objects]] in a [[category]] was first observed in 

* [[Nigel Higson]], _A characterization of KK-theory_,  Pacific J. Math. Volume 126, Number 2 (1987), 253-276. ([EUCLID](http://projecteuclid.org/euclid.pjm/1102699804))

where moreover this category is realized as the [[universal property|universal]] additive and split exact "[[localization]]" of $C^\ast Alg$ at the $C^\ast$-algebra of [[compact operators]].



The generalization of this statement to [[equivariant cohomology|equivariant]] KK-theory is in 

* Klaus Thomsen, _The universal property of equivariant KK-theory_ ([K-theory preprint](http://www.math.uiuc.edu/K-theory/0249/))
 {#Thomsen98}

Characterization of KK-theory as the [[satellites]] of a functor is in 

* [[Hvedri Inassaridze]], _Universal property of Kasparov bivariant K-theory_ ([[InassaridzeOnKK.pdf:file]], [ps](http://www.math.uni-bielefeld.de/~bak/kasp.ps))
 {#Inassaridze}

A [[triangulated category]] structure for KK-theory is discussed in 

* [[Ralf Meyer]], _Categorical aspects of bivariant K-theory_, ([arXiv:math/0702145](http://arxiv.org/abs/math/0702145))
 {#Meyer}

* [[Ralf Meyer]], [[Ryszard Nest]], _Homological algebra in bivariant K-theory and other triangulated categories_ ([arXiv:math/0702146](http://arxiv.org/abs/math/0702146))

* [[Ralf Meyer]], _KK-theory as a triangulated category_, Lecture notes (2009) ([pdf](http://wwwmath.uni-muenster.de/u/echters/Focused-Semester/lecturenotes/Meyer_--_KK-theory_as_a_triangulated_category.pdf))
 {#Meyer}

A [[model category]] realization of KK-theory is discussed in 

* [[Michael Joachim]], [[Mark Johnson]], _Realizing Kasparov's KK-theory groups as the homotopy classes of maps of a Quillen model category_ ([arXiv:0705.1971](http://arxiv.org/abs/0705.1971))
 {#JoachimJohnson07}

A [[category of fibrant objects]]-structure on [[C*Alg]] which unifies the above homotopical pictures is discussed in

* [[Otgonbayar Uuye]], _Homotopy theory for $C^\ast$-algebras_ ([arXiv:1011.2926](http://arxiv.org/abs/1011.2926))
 {#Uuye10}

More on this is at _[[homotopical structure on C*-algebras]]_.

Further discussion in the context of [[stable homotopy theory]] and [[E-theory]] is in

* Martin Grensing, _Noncommutative stable homotopy theory_ ([arXiv:1302.4751](http://arxiv.org/abs/1302.4751))

* Snigdahayan Mahanta, _Higher nonunital Qullen $K'$-theory, KK-dualities and applications to topological $\mathbb{T}$-duality_  [pdf](http://wwwmath.uni-muenster.de/u/snigdhayan.mahanta/papers/KQ.pdf)
 {#Mahanta}


### In the context of the Novikov conjecture

* [[Jonathan Rosenberg]], _Group C*-algebras and Topological Invariants_ , Proc. Conf. in Neptun, Romania, 1980, Pitman (London, 1985)
 {#Rosernberg80}

### In the context of the Atiyah-Singer index theorem

The classical [[Atiyah-Singer index theorem]] is reviewed in [[operator K-theory]] (with some hints towards KK-theory) in 

* [[Nigel Higson]], [[John Roe]], _Lectures on operator K-theory and the Atiyah-Singer Index Theorem_ (2004) ([pdf](http://folk.uio.no/rognes/higson/Book.pdf))
 {#HigsonRoe}

Generalization to the relative case in [[KK-theory]], hence for indices of fiberwise [[elliptic operators]] on [[Hilbert C*-module]]-[[fiber bundles]] is in

* Jody Trout, _Asymptotic Morphisms and Elliptic Operators over $C^\ast$-algebras_, K-theory, 18 (1999) 277-315 ([arXiv:math/9906098](http://arxiv.org/abs/math/9906098))

### For convolution algebras and In geometric quantization

Discussion of KK-theory with an eye towards [[representation of a C-star algebra|C-star representations]] of [[groupoid convolution 

algebras]] in the context of [[geometric quantization]] [[geometric quantization by push-forward|by push-forward]] is in 

* [[Klaas Landsman]], _Quantization as a functor_ ([arXiv:math-ph/0107023](http://arxiv.org/abs/math-ph/0107023))

* [[Klaas Landsman]], _Functorial quantization and the Guillemin-Sternberg conjecture_ ([arXiv:math-ph/0307059](http://arxiv.org/abs/math-ph/0307059))
 {#Landsman03}

* [[Rogier Bos]], _Groupoids in geometric quantization_ PhD Thesis (2007) ([pdf](http://www.math.ist.utl.pt/~rbos/ProefschriftA4.pdf))
 {#Bos07}

See also the related references at _[[Guillemin-Sternberg geometric quantization conjecture]]_.

The KK-theory of twisted convolution algebras and its relation to [[twisted K-theory]] of [[differentiable stacks]] is discussed in

* [[Jean-Louis Tu]], [[Ping Xu]], [[Camille Laurent-Gengoux]], _Twisted K-theory of differentiable stacks_ ([arXiv:math/0306138](http://arxiv.org/abs/math/0306138))
 {#TXLG}

Discussion of groupoid 1-[[cocycles]] and their effect on the [[groupoid algebra]] KK-theory is discussed in 

* Bram Mesland, _Groupoid cocycles and K-theory_ ([arXiv:1005.3677](http://arxiv.org/abs/1005.3677))


### In D-brane theory

KK-theory also describes [[RR-field]] [[charges]] and sources in [[D-brane]] theory.

A review is in

* [[Richard Szabo]], _D-branes and bivariant K-theory_ ([arXiv:0809.3029](http://arxiv.org/abs/0809.3029))
 {#Szabo}

### Smooth refinement and spectral triple

Discussion of KK-theory for [[spectral triples]] is discussed in

* [[Bram Mesland]], _Spectral triples and KK-theory: A survey_ ([arXiv:1304.3802](http://arxiv.org/abs/1304.3802))

### Algebraic KK-theory

Analogues of Kasparov K-theory in the spirit of [[algebraic K-theory]] are developed in

* [[Grigory Garkusha]], _Algebraic Kasparov K-theory. I_, [pdf](http://maths.swan.ac.uk/staff/gg/papers/AlgKasparov11.pdf), _II_, [pdf](http://front.math.ucdavis.edu/1206.0178);
Universal bivariant algebraic K-theories, J. Homotopy Relat. Struct. 8(1) (2013), 67-116 [pdf](http://maths.swan.ac.uk/staff/gg/papers/homotopyuniv.pdf)

[[!redirects Kasparov K-theory]]
[[!redirects bivariant K-theory]]

[[!redirects KK-group]]
[[!redirects KK-groups]]

[[!redirects Kasparov KK-group]]
[[!redirects Kasparov KK-groups]]

[[!redirects Kasparov KK-groups]]
