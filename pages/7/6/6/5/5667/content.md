

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
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
#### Motivic cohomology
+--{: .hide}
[[!include motivic cohomology - contents]]
=--
=--
=--





#Contents#
* table of contents
{:toc}

## Idea

_KK-theory_ is a "[[bivariant cohomology theory|bivariant]]" joint generalization of [[operator K-theory]] and [[K-homology]]: for $A, B$ two [[C*-algebras]], the _KK-group_ $KK(A,B)$ is a natural [[homotopy]] [[equivalence class]] of $(A,B)$-[[Hilbert bimodules]] equipped with an additional left weak [[Fredholm module]] structure. These KK-groups $KK(A,B)$ behave in the first argument as [[K-homology]] of $A$ and in the second as [[K-cohomology]]/[[operator K-theory]] of $B$.

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

* $\mathcal{B} \coloneqq \mathcal{B}(H)$ for the $C^\ast$-algebra of [[bounded operators]] on a complex, infinite-dimensional separable [[Hilbert space]]; 

* $\mathcal{K} \coloneqq \mathcal{K}(H) \hookrightarrow \mathcal{B}(H)$ for the [[compact operators]].

=--

+-- {: .num_defn #HilbertCStarModule}
###### Definition

For $B \in $ [[C*Alg]], a [[Hilbert C*-module]] over $B$ is 

1. a [[complex numbers|complex]] [[vector space]] $\mathcal{H}$;

1. equipped with a [[C*-representation]] of $B$ from the right;

1. equipped with a [[sesquilinear map]] (linear in the second argument)

   $$
     \langle -,-\rangle \colon \mathcal{H} \times \mathcal{H} \to B
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

For $A,B \in C^\ast Alg$ an $(A,B)$-[[Hilbert C*-bimodule]] is an $B$-[[Hilbert C*-module]], def. \ref{HilbertCStarModule} $(\mathcal{H}, \langle \rangle)$ equipped with a [[C-star representation]] of $A$ from the left such that all $a \in A$ are "adjointable" in the $B$-valued inner product, meaning that

$$
  \langle a^\ast \cdot x,y\rangle = \langle x, a y\rangle
  \,.
$$


=--


+-- {: .num_defn }
###### Definition

For $A, B \in $ [[C*Alg]], **Kasparov $(A,B)$-bimodule**
is a $\mathbb{Z}_2$-[[graded vector space|graded]] $(A,B)$-[[Hilbert bimodules]] $\mathcal{H}, \langle -,-\rangle$, def. \ref{HilbertBimodule}, equipped with an adjointable odd-graded [[bounded operator]] $F \in \mathcal{B}_B(\mathcal{H})$ such that 

1. $(F^2 - 1)\pi(a) \in \mathcal{K}_B(\mathcal{H})$ 

1. $[F, \pi(a)] \in \mathcal{K}_B(\mathcal{H})$ 

1. $(F - F^\ast) \pi(a)\in \mathcal{K}_B(\mathcal{H})$

for all $a \in A$,

hence such that $F$ squares to the identity, commutes with multiplication operators and is self-adjoint _up to_ [[compact operators]]. 

=--

For instance ([Blackadar 99, p. 144](#Blackadar99)).

+-- {: .num_example }
###### Example

For $B = \mathbb{C}$ a Kasparov $(A,B)$-bimodule is equivalently an $A$-[[Fredholm module]] for an essentially self-adjoint [[Fredholm operator]]

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

=--

A streamlined version of the definition of the Kasparov product is in ([Skandalis 84](#Skandalis84)). 

+-- {: .num_remark}
###### Remark

From the point of view of [[E-theory]] the Kasparov product is equivalently just the composition of homotopy classes of completely positive [[asymptotic C*-homomorphisms]]. See at _[[E-theory]]_ for more on this.

=--

+-- {: .num_remark}
###### Remark

On the other hand, at least between $C^\ast$-algebras which are [[algebras of functions]] on [[smooth manifolds]]  $A_i = C(X_i)$ , KK-classes are presented by [[correspondences]] $X_1 \leftarrow Z \to X_2$ and the Kasparov product is given just by the [[fiber product]]-composition operation on correspondences ([Connes-Skandalis 84, theorem 3.2](#ConnesSkandalis84), [Block-Weinberger 99, section 3](#BlockWeinberger99)).

=--



### Universal category-theoretic characterization
 {#UniversalCharacterization}

+-- {: .num_prop #KasparovProductIsAssociative}
###### Proposition

The Kasparov product, def. \ref{KasparovProduct}, is [[associativity|associative]]. Thus under the Kasparov product

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

+-- {: .num_remark }
###### Remark

The localization conditions here are analogous to those that define the localization of [[stable (∞,1)-categories]] to [[noncommutative motives]] See there for more and see the references [below](#AsHomotopyOfStableInfinityCategoryReferences).

=--

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


### In terms of homotopy-classes of $\ast$-homomorphisms
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

### In terms of correspondences/spans of groupoids
 {#InTermsOfCorrespondences}


At least to some extent, KK-classes between [[C*-algebras]] of [[continuous functions]] on manifolds/spaces, and maybe more generally between [[groupoid convolution algebras]] can be represented by certain [[equivalence classes]] of [[spans]]/[[correspondences]] 

$$
  X \leftarrow (Z,E) \to Y
$$

of such [[spaces]].

See the corresponding [references below](#ReferencesInTermsOfCorrespondences).

Such a description by abelianizations of [[correspondences]] is reminiscent of similar constructions of [[motivic cohomology]]. See [below](#AsAnAnalogOfMotives). For more on this see also the pointers at at _[[motivic quantization]]_.

(...)

* category of equivariant correspondences equipped with cocycle: $\hat F_{\mathcal{G}}^\ast$ (theorem 2.26);

* specifically for K-theory cocycles: $\widehat {KK}_{\mathcal{G}}^\ast$  (section 4, page 27)

* pull-push from correspondences to KK in proof of theorem 4.2, bottom of p. 27

(...)



### As an analog of motives in noncommutative topology
 {#AsAnAnalogOfMotives}

To some extent [[KK-theory]]/[[E-theory]] look like an analogue in [[noncommutative topology]] of what in [[algebraic geometry]] is the category of [[motives]]. ([Connes-Consani-Marcolli 05](#ConnesConsaniMarcolli05)). ([Meyer 06](#Meyer06)). 

Specifically the characterization in terms of spans/correspondences [above](#InTermsOfCorrespondences) is reminiscent to the definition of [[pure motives]], see the rferences below: _[In terms of correspondences](#ReferencesInTermsOfCorrespondences). A relation between bivariant [[algebraic K-theory]] and [[motivic cohomology]] is discussed in ([Garkusha-Panin 11](#GarkushaPanin11)).

A universal [[functor]] from KK-theory to [[noncommutative motives]]

$$
  KK \longrightarrow NCC_{dg}
$$

was given in ([Mahanta 13](#Mahanta13)). This sends a [[C*-algebra]] to the [[dg-category]] of [[perfect complexes]] over (the [[unitalization]] of) its underlying [[associative algebra]].

### Equivariant KK-theory
 {#EquivariantKKTheory}

Pretty much all of KK-theory has a generalization to [[equivariant cohomology]] where all algebras and modules are equipped with [[actions]] of a given [[topological group]] or more generally [[topological groupoid]] $\mathcal{G}$, and all operators are suitably [[invariant|invariant]]/[[equivariance|equivariant]] under this action. See at _[[equivariant KK-theory]]_ for more.

The [[Baum-Connes conjecture]] and the [[Green-Julg theorem]] assert that under some conditions $\mathcal{G}$-equivariant KK-theory is equivalent to the plain KK-theory of the [[groupoid convolution algebras]] of the corresponding [[action groupoids]]. See at _[[Green-Julg theorem]]_ for details. 
 

## Examples
 {#Examples}

### Basic examples

+-- {: .num_example }
###### Example

For $f \colon A \to B$ a [[homomorphism]] of $\mathbb{Z}_2$ [[graded C*-algebras]], take $B$ as a right [[Hilbert module]] over itself and equip it with the left [[action]] of $A$ induced by $f$. This makes it a [[Hilbert bimodule]]. Together with the 0-[[Fredholm operator]], this represents an element 

$$
  (B, f, 0) \in KK(A,B)
  \,.
$$

=--

For instance ([Blackadar 99, example 17.1.2 a)](#Blackadar99)).

+-- {: .num_example }
###### Example

For 

$$
  (H_i, F_i) \in KK(A,B)
$$ 

a [[Fredholm module|Fredholm]] $(A_i,B)$-[[Hilbert bimodule]] for $i \in \{1,2\}$, the [[direct sum]] is

$$
  (H_1 \oplus H_2, F_1 \oplus F_2) \in KK(A_1\oplus A_2, B)
  \,.
$$

=--

For instance ([Blackadar 99, example 17.1.2 c)](#Blackadar99)).


### The archetypical examples

+-- {: .num_example }
###### Example

Let $(X,g)$ be a [[closed manifold|closed]] [[smooth manifold|smooth]] [[Riemannian manifold]], and let $V_0, V_1$ be two smooth [[vector bundles]] over $X$ with Hermitian strucure ([[associated bundle|associated]] to a chosen [[unitary group]]-[[principal bundle]]). 

Then given an [[elliptic operator|elliptic]] [[pseudodifferential operator]]

$$
  P \colon \Gamma(V_0) \to \Gamma(V_1)
$$

on smooth [[sections]] it extends to an essentially [[unitary operator|unitary]] [[Fredholm operator]] on [[square integrable function|square integrable]] sections $L^2(V_i)$. 

Consider then the $\mathbb{Z}_2$-graded [[Hilbert space]]

$$
  H \coloneqq L^2(V_0) \oplus L^2(V_1)
$$

equipped with the evident action of $C(X)$ (by "[[multiplication operators]]"). Then with $P$ a [[parametrix]] for $Q$, the 
operator

$$
  F \coloneqq 
  \left[
    \array{
       0 & Q
       \\
       P & 0
    }
  \right]
$$

is a [[Fredholm operator]] on $H$, so that

$$
  \left(
    L^2(V_1) \oplus L^2(V_2), 
  \left[
    \array{
       0 & Q
       \\
       P & 0
    }
  \right]
  \right)
  \in 
  KK(C(X),\mathbb{C})
  \,.
$$


=--

+-- {: .num_example }
###### Example

Let $(X,g)$ be an [[almost complex manifold]]
and let $D \colon \overline{\partial} + \overline{\partial}^\ast$ be the [[Dolbeault-Dirac operator]]. This extends to an operator on 

$$
  H \coloneqq L^2(\Omega^{0,\bullet})
$$

and 

$$
  F \coloneqq \frac{D}{\sqrt{1 + D^2}}
$$

(defined by [[functional calculus]]) is then a [[Fredholm operator]] on that.  Then

$$
  \left(
    L^2(\Omega^{0,\bullet}),
    \frac{\overline{\partial} + \overline{\partial}^\ast}{\sqrt{1+ (\overline{\partial} + \overline{\partial}^\ast)^2}}
  \right)
  \in
  KK(C(X), \mathbb{C})
  \,.
$$


=--


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

### Triangulated structure and $KU$-module structure
 {#TriangulatedAndSpectrumEnrichedStructure}

+-- {: .num_prop }
###### Proposition

$KK$ is naturally a stable [[triangulated category]].

=--

([Meyer 07](#Meyer), [Uuye 10, theorem 2.29](#Uuye10)).

+-- {: .num_prop }
###### Proposition

There is a [[functor]]

$$
  \mathbb{K}(-) \;\colon\; C^\ast Alg \to Ho(Spectra)
$$

to the [[stable homotopy category]] such that 

1. $\pi_n(\mathbb{K})(A) \simeq K_n(A)$, for all $A \in C^\ast Alg$, (hence the spectrum is a cohomology spectrum for the [[operator K-theory]] of $A$);

1. $\mathbb{K}(\mathbb{C})$ is naturally a [[ring spectrum]];

1. $\mathbb{K}(A)$ is naturally a [[symmetric spectrum|symmetric]] $\mathbb{K}(\mathbb{C})$-[[module spectrum]]

1. $\mathbb{K}$ lifts to a [[lax monoidal functor]]
  
   $$
     \mathbb{K} \;\colon\; C^\ast Alg \to Ho(\mathbb{K}(\mathbb{C}) Mod)
   $$

   to the [[homotopy category]] of [[module spectra]], and this in turn extends to a [[lax monoidal functor]] on the KK-category

   $$
     \mathbb{K} \;\colon\; KK \to Ho(\mathbb{K}(\mathbb{C}) Mod)
     \,.
   $$

1. $\mathbb{K}$ restricts to a [[fully faithful functor]] on the [[thick subcategory]] of the [[triangulated category]] $KK$ generated by the [[tensor unit]] (the "[[bootstrap category]]").

=--

This is the main result of ([DEKM 11, section 3](#DEKM11)).

+-- {: .num_remark }
###### Remark

Since $\mathbb{K}$ is a [[lax monoidal functor]] in particular it preserves [[dual objects]] and [[dual morphisms]], hence [[Poincaré duality algebras]] and their [[Umkehr maps]]. 

=--



### K&#252;nneth theorem

The [[thick subcategory]] of the [[triangulated category]] $KK$ generated from the [[tensor unit]] is called the _[[bootstrap category]]_ $Boot \hookrightarrow KK$. For $A \in Boot \hookrightarrow KK$ one has that $KK(A,B)$ satisfies a [[Künneth theorem]]. See at _[[bootstrap category]]_ for more.

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
 {#PoincareDualityAndThomIsomorphism}

+-- {: .num_defn #PoincareDualityAlgebra}
###### Definition

A [[C*-algebra]] is a [[Poincaré duality algebra]]
if it is a [[dualizable object]] in the  [[symmetric monoidal category]] $KK$ with dual its [[opposite algebra]]. 

=--

([Brodzki-Mathai-Rosenberg-Szabo 07, def. 2.1](#BrodzkiMathaiRosenbergSzabo07))


+-- {: .num_prop #PoincareDuality}
###### Proposition

Let $X$ be a [[smooth manifold]] which is [[compact topological space|compact]]. Then the [[C*-algebra]] $C(X) \otimes C_0(T^\ast X)$
(the tensor product of the algebra of functions of [[compact support]] on $X$ and on its [[cotangent bundle]]) is isomorphic, in $KK$, to $\mathbb{C}$:

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

For more discussion see at _[[Poincaré duality algebra]]_.

### Push-forward in KK-theory
 {#UmkehrMap}

[[Umkehr map]] in KK-theory ([Brodzki-Mathai-Rosenberg-Szabo 07, section 3.3](#BrodzkiMathaiRosenbergSzabo07))

If $A$, $B$ are [[Poincaré duality algebras]], 
def. \ref{PoincareDualityAlgebra}, then for $f \colon A \to B$ a morphism, the corresponding [[Umkehr map]] is (postcomposition) with the [[dual morphism]] of its [[opposite algebra]] version:

$$
  f! \coloneqq (f^op)^\ast
  \,.
$$

([Brodzki-Mathai-Rosenberg-Szabo 07, p. 14](#BrodzkiMathaiRosenbergSzabo07))

For more and a discussion of [[twisted Umkehr maps]] see at _[[Poincaré duality algebra]]_ and at _[[Freed-Witten-Kapustin anomaly cancellation]]_.


## Further Theorems

* The [[Baum-Connes conjecture]] is naturally formulated within KK-theory.

* The [[Novikov conjecture]] has been verified in many cases using KK-theory. (see for instance [Rosenberg 80](#Rosenberg80)).

* The [[Atiyah-Singer index theorem]] is naturally formutaled in KK-theory/[[E-theory]]. (See ([Higson-Roe](#HigsonRoe))).

## Related concepts

* [[KK-bootstrap category]]

* [[equivariant KK-theory]]

* [[index theory]]

* [[bivariant cohomology theory]]

* [[bivariant algebraic K-theory]], [[K-motive]]

* [[operator K-theory]]

* [[E-theory]]

* [[homotopical structure on C*-algebras]], [[model structure on operator algebras]]

* [[assembly map]], [[Baum-Connes conjecture]]

[[!include noncommutative motives - table]]


## References

### General

KK-theory was introduced by [[Gennady Kasparov]] in 

* {#Kasparov80} [[Gennady Kasparov]], *The operator $K$-functor and extensions of $C^{\ast}$-algebras*, Izv. Akad. Nauk SSSR Ser. Mat. __44__  (1980), no. 3, 571-636, 719, [MR81m:58075](http://www.ams.org/mathscinet-getitem?mr=582160), [Zbl](http://www.zentralblatt-math.org/zmath/search/?an=Zbl%200464.46054%7CZbl%200448.46051), [abstract](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=im&paperid=1739&option_lang=eng), [english doi](http://dx.doi.org/10.1070%2FIM1981v016n03ABEH001320), free Russian original: [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=im&paperid=1739&volume=44&year=1980&issue=3&fpage=571&what=fullt&option_lang=eng)
 

prompted by the advances in [[Brown-Douglas-Fillmore theory]], especially in the last 1977 article.

Some streamlining of the definitions appeared in

* {#Skandalis84} [[Georges Skandalis]], *Some remarks on Kasparov theory*, J. Funct. Anal. 59 (1984) 337-347.
 

A textbook account is in 

* {#Blackadar99} [[Bruce Blackadar]], *[[K-Theory for Operator Algebras]]*, 2nd ed. Cambridge University Press, Cambridge (1999)
 

Introductions and surveys include

* [[Gennady Kasparov]], *Operator K-theory and its applications: elliptic operators, group representations, higher signatures $C^\ast$-extensions*, Proceedings ICM 1983 Warszawa, PWN-Elsevier (1984) 987-1000.

* [[Nigel Higson]], _A primer on KK-theory_. Proc. Sympos. Pure Math. 51, Part 1, 239&#8211;283. (1990) ([pdf](http://www.math.psu.edu/higson/math/Papers_files/Higson%20-%201990%20-%20A%20primer%20on%20KK-theory.pdf))

* [[Georges Skandalis]], _Kasparov's bivariant K-theory and applications_ Exposition. Math. 9, 193&#8211;250 (1991) ([pdf slides](http://www.math.vanderbilt.edu/~bisch/ncgoa08/talks/skandalis2.pdf))

* {#Introduction} *Introduction to KK-theory and E-theory*, Lecture  notes (Lisbon 2009) ([pdf slides](http://oaa.ist.utl.pt/files/cursos/courseD_Lecture4_KK_and_E1.pdf))
 

* [[Heath Emerson]], [[R. Meyer]] (notes taken by S. Hong), *KK-theory and Baum-Connes conjecture*, Lectures at _Summer school on operator algebras and noncommutative geometry_ (June 2010) ([pdf](http://www.pims.math.ca/files/EM_%20KK-theory_BC_Conjecture.pdf))

* {#Meyer06} [[R. Meyer]], *How analysis and topology interact in bivariant K-theory*, 2006 ([pdf](http://mate.dm.uba.ar/~gcorti/article.pdf))
 
On an approach using quasi-homomorphisms:

* [[Joachim Cuntz]], James Gabe. *Generalized homomorphisms and KK with extra structure* (2024). ([arXiv:2404.06840](https://arxiv.org/abs/2404.06840)).

### Excision

Excision for KK-theory is further studied in 

* {#CuntzSkandalis86} [[Joachim Cuntz]], [[Georges Skandalis]], *Mapping cones and exact sequences in KK-theory*, J. Operator Theory 15 (1986) 163-180.
 

* {#Skandalis88} [[Georges Skandalis]], _Une notion de nuclearit&#233; en K-theorie_, K-Theory 1 (1988) 549-574.
 


### In Category theory and Homotopy theory

KK-theory is naturally understood in terms of [[universal properties]] in [[category theory]] and in [[homotopy theory]].

That $KK(A,B)$ is naturally thought of as a collection of "generalized [[homomorphisms]]" of $C^\ast$-algebras was amplified in 

* [[Joachim Cuntz]], *Generalized Homomorphisms Between $C^\ast$-algebras and KK-theory*, Springer Lecture Notes in Mathematics, 1031 (1983), 31-45. doi:[10.1007/BFb0072109](https://doi.org/10.1007/BFb0072109)

* [[Joachim Cuntz]], _K-theory and C*-algebras,_ Springer Lecture Notes in Mathematics, 1046 (1984), 55-79.

That under the Kasparov product these are indeed the [[hom-objects]] in a [[category]] was first observed in 

* [[Nigel Higson]], _A characterization of KK-theory_,  Pacific J. Math. Volume 126, Number 2 (1987), 253-276. ([EUCLID](http://projecteuclid.org/euclid.pjm/1102699804))

where moreover this category is realized as the [[universal property|universal]] additive and split exact "[[localization]]" of $C^\ast Alg$ at the $C^\ast$-algebra of [[compact operators]].



The generalization of this statement to [[equivariant cohomology|equivariant]] KK-theory is in 

* {#Thomsen98} Klaus Thomsen, _The universal property of equivariant KK-theory_ ([K-theory preprint](http://www.math.uiuc.edu/K-theory/0249/))
 

Characterization of KK-theory as the [[satellites]] of a functor is in 

* {#Inassaridze} [[Hvedri Inassaridze]], _Universal property of Kasparov bivariant K-theory_ ([[InassaridzeOnKK.pdf:file]], [ps](http://www.math.uni-bielefeld.de/~bak/kasp.ps))
 

A [[triangulated category]] structure for KK-theory is discussed in 

* {#Meyer} [[Ralf Meyer]], _Categorical aspects of bivariant K-theory_, ([arXiv:math/0702145](http://arxiv.org/abs/math/0702145))
 

* [[Ralf Meyer]], [[Ryszard Nest]], _Homological algebra in bivariant K-theory and other triangulated categories_ ([arXiv:math/0702146](http://arxiv.org/abs/math/0702146))

* {#Meyer} [[Ralf Meyer]], _KK-theory as a triangulated category_, Lecture notes (2009) ([pdf](http://wwwmath.uni-muenster.de/u/echters/Focused-Semester/lecturenotes/Meyer_--_KK-theory_as_a_triangulated_category.pdf))
 
A [[model category]] realization of KK-theory is discussed in 

* {#JoachimJohnson07} [[Michael Joachim]], [[Mark Johnson]], _Realizing Kasparov's KK-theory groups as the homotopy classes of maps of a Quillen model category_ ([arXiv:0705.1971](http://arxiv.org/abs/0705.1971))
 

A [[category of fibrant objects]]-structure on [[C*Alg]] which unifies the above homotopical pictures is discussed in

* {#Uuye10} [[Otgonbayar Uuye]], _Homotopy theory for $C^\ast$-algebras_ ([arXiv:1011.2926](http://arxiv.org/abs/1011.2926))
 

More on this is at _[[homotopical structure on C*-algebras]]_.

Further discussion in the context of [[stable homotopy theory]] and [[E-theory]] is in

* Martin Grensing, _Noncommutative stable homotopy theory_ ([arXiv:1302.4751](http://arxiv.org/abs/1302.4751))

* {#Mahanta11} [[Snigdhayan Mahanta]], _Higher nonunital Quillen $K'$-theory, KK-dualities and applications to topological $\mathbb{T}$-duality_, Journal of Geometry and Physics, Volume 61, Issue 5 2011, p. 875-889.   ([pdf](http://wwwmath.uni-muenster.de/u/snigdhayan.mahanta/papers/KQ.pdf))
 

Refinement of [[operator K-theory]] to cohomology [[spectra]] is discussed in 

* {#BunkeJoachimStolz03} [[Ulrich Bunke]], [[Michael Joachim]], [[Stephan Stolz]], _Classifying spaces and spectra representing the K-theory of a graded $C^\ast$-algebra_, High-dimensional manifold topology, World Sci. Publ., River Edge, NJ, 2003, pp. 80&#8211;102
 
 
This construction is functorial (only) for _essential_ $\ast$-homomorphisms of [[C*-algebras]].

### As the homotopy category of a stable $\infty$-category
 {#AsHomotopyOfStableInfinityCategoryReferences}

A refinement of the KK-category to a [[spectrum]]-[[enriched category]] ($\sim$ [[stable (∞,1)-category]]) is claimed in 

* {#JoachimStolz09} [[Michael Joachim]], [[Stephan Stolz]], _An enrichment of $KK$-theory over the category of symmetric spectra_ M&#252;nster J. of Math. 2 (2009), 143&#8211;182 ([pdf](http://www3.nd.edu/~stolz/KKenrich.pdf))
 

and the generalization of this to [[equivariant K-theory]] over geometrically discrete groupoids is discussed in 

* {#Mitchener07} [[Paul Mitchener]], _$KK$-theory spectra for $C^\ast$-categories and discrete groupoid $C^\ast$-algebras_ ([arXiv:0711.2152](http://arxiv.org/abs/0711.2152))
 

but this construction is stated to be mistaken on p. 3 of 

* {#DEKM11} [[Ivo Dell'Ambrogio]], [[Heath Emerson]], [[Tamaz Kandelaki]], [[Ralf Meyer]], _A functorial equivariant K-theory spectrum and an equivariant Lefschetz formula_ ([arXiv:1104.3441](http://arxiv.org/abs/1104.3441))
 

This article in turn considers a variant of the construction in ([Bunke-Joachim-Stolz 03](#BunkeJoachimStolz03)) which gives operator K-theory spectra that are functorial for general $\ast$-homomorphisms.

Observations relating to a genuine [[stable (∞,1)-category]] structure maybe at least of [[E-theory]] are in 

* {#Mahanta12} [[Snigdhayan Mahanta]], _Noncommutative stable homotopy and semigroup $C^*$-algebras_,  ESI preprint 2394 ([arXiv:1211.6576](http://arxiv.org/abs/1211.6576))

A complete realization of ([[equivariant K-theory|equivariant]], even) KK-theory as the [[homotopy category of an (infinity,1)-category|homotopy category]] of a [[stable (infinity,1)-category|stable $(\infty,1)$-category]]:

* {#BunkeEngelLand21} [[Ulrich Bunke]], [[Alexander Engel]], [[Markus Land]], *A stable $\infty$-category for equivariant KK-theory* $[$[arXiv:2102.13372](https://arxiv.org/abs/2102.13372)$]$
 


### In the context of the Novikov conjecture

* {#Rosenberg80} [[Jonathan Rosenberg]], _Group C*-algebras and Topological Invariants_ , Proc. Conf. in Neptun, Romania, 1980, Pitman (London, 1985)
 

### In the context of the Atiyah-Singer index theorem

The classical [[Atiyah-Singer index theorem]] is reviewed in [[operator K-theory]] (with some hints towards KK-theory) in 

* {#HigsonRoe} [[Nigel Higson]], [[John Roe]], _Lectures on operator K-theory and the Atiyah-Singer Index Theorem_ (2004) ([pdf](http://folk.uio.no/rognes/higson/Book.pdf))
 

Generalization to the relative case in [[KK-theory]], hence for indices of fiberwise [[elliptic operators]] on [[Hilbert C*-module]]-[[fiber bundles]] is in

* Jody Trout, _Asymptotic Morphisms and Elliptic Operators over $C^\ast$-algebras_, K-theory, 18 (1999) 277-315 ([arXiv:math/9906098](http://arxiv.org/abs/math/9906098))

### For convolution algebras and In geometric quantization

Discussion of KK-theory with an eye towards [[representation of a C-star algebra|C-star representations]] of [[groupoid convolution 

algebras]] in the context of [[geometric quantization]] [[geometric quantization by push-forward|by push-forward]] is in 

* [[Klaas Landsman]], _Quantization as a functor_ ([arXiv:math-ph/0107023](http://arxiv.org/abs/math-ph/0107023))

* {#Landsman03} [[Klaas Landsman]], _Functorial quantization and the Guillemin-Sternberg conjecture_ ,  Proc. Bialowieza 2002 ([arXiv:math-ph/0307059](http://arxiv.org/abs/math-ph/0307059))
 

* {#Bos07} [[Rogier Bos]], _Groupoids in geometric quantization_ PhD Thesis (2007) ([pdf](http://www.math.ist.utl.pt/~rbos/ProefschriftA4.pdf))
 

with a summary/exposition in

* {#Landsman10} [[Klaas Landsman]], _Functoriality of quantization: a KK-theoretic approach_, talk at ECOAS, Dartmouth College, October 2010 ([web](http://www.academia.edu/1992202/Functoriality_of_quantization_a_KK-theoretic_approach))
 


See also the related references at _[[Guillemin-Sternberg geometric quantization conjecture]]_.

The KK-theory of twisted convolution algebras and its relation to [[twisted K-theory]] of [[differentiable stacks]] is discussed in

* {#TXLG} [[Jean-Louis Tu]], [[Ping Xu]], [[Camille Laurent-Gengoux]], _Twisted K-theory of differentiable stacks_ ([arXiv:math/0306138](http://arxiv.org/abs/math/0306138))
 

Discussion of groupoid 1-[[cocycles]] and their effect on the [[groupoid algebra]] KK-theory is discussed in 

* Bram Mesland, _Groupoid cocycles and K-theory_ ([arXiv:1005.3677](http://arxiv.org/abs/1005.3677))

### In terms of correspondences/spans
 {#ReferencesInTermsOfCorrespondences}

#### For plain KK-theory

KK-classes between [[algebras of functions]] on [[smooth manifolds]] are described in terms of [[equivalence classes]] of [[correspondence]] manifolds carrying a [[vector bundle]] in section 3 of

* {#ConnesSkandalis84} [[Alain Connes]], [[Georges Skandalis]], *The longitudinal index theorem for foliations*, Publ. Res. Inst. Math. Sci. **20** 6, 1139-1183 (1984) ([pdf](http://www.alainconnes.org/docs/longitudinal.pdf))
 

This generalizes the [[Baum-Douglas geometric cycles]] from [[K-homology]] to KK-theory.

A further generalization of this, where one algebra $C(Y)$ is generalized to 
$C(Y) \otimes A$ for $A$ a unital separable $C^\ast$-algebra, is in section 3 of:


* {#BlockWeinberger99} [[Jonathan Block]], [[Shmuel Weinberger]], *Arithmetic manifolds of positive scalar curvature*, J. Diff. Geom. 52, no. 2, 375-406 (1999). ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.30.297))
 

In section 5 of

* {#BrodzkiMathaiRosenbergSzabo07} [[Jacek Brodzki]], [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]], _Noncommutative correspondences, duality and D-branes in bivariant K-theory_, Adv. Theor. Math. Phys.13:497-552,2009 ([arXiv:0708.2648](http://arxiv.org/abs/0708.2648))
 

this is reviewed and then a characterization in terms of [[co-spans]] of [[C*-algebras]] is given. This version is effectively a restatement of [the characterization by Cuntz](#RelationToHomotopyClassesOfStarHomomorphisms) as reproduced in ([Blackadar 99, corollary 17.8.4](#Blackadar99)).

For similar structures see also at _[[motive]]_ in the section _[Relation to bivariant K-theory](motive#RelationToKKTheory)_.

A 'generators and relations' description of KK-theory in terms of spans is given in

* Bernhard Burgstaller, _The generators and relations picture of KK-theory_, (2016) arXiv:[1602.03034](http://arxiv.org/abs/1602.03034)


#### For equivariant KK-theory
 {#ReferencesCorrespondencesEquivariant}

Generalization of such [[correspondence]]-presentation to [[equivariant KK-theory]] (and hence, by the [[Green-Julg theorem]] essentially to KK-theory of [[groupoid algebras]] of [[action groupoids]] of [[compact topological groups]]) -- was introduced in 

* [[Heath Emerson]], [[Ralf Meyer]], _Bivariant K-theory via correspondences_, Adv. Math. 225 (2010), 2883-2919 ([arXiv:0812.4949](http://arxiv.org/abs/0812.4949))

based on 

* {#EmersonMeyer09} [[Heath Emerson]], [[Ralf Meyer]] _Equivariant embedding theorems and topological index maps_, Adv. Math. 225 (2010), 2840-2882 ([arXiv:0908.1465](http://arxiv.org/abs/0908.1465))
 

* [[Heath Emerson]], [[Ralf Meyer]], _Dualities in equivariant Kasparov theory_ ([arXiv:0711.0025](http://arxiv.org/abs/0711.0025))

based on technical aspects of the construction of pushforward along and comoposition of equivariant correspondences in

* [[Paul Baum]], [[Jonathan Block]], _Equivariant bicycles on singular spaces_. C.R. Acad. Sci. Paris, t. 311 Serie I, 1990 ([pdf](http://www.math.upenn.edu/~blockj/papers/BlockEquivariantbi.pdf))

* [[Heath Emerson]], [[Ralf Meyer]], *Equivariant embedding theorems and topological index maps*, Adv. Math. 225 (2010), 2840-2882 ([arXiv:0908.1465](http://arxiv.org/abs/0908.1465))


Further developments of this are in 

* [[Heath Emerson]], *Duality, correspondences and the Lefschetz map in equivariant KK-theory: a survey* ([arXiv:0904.4744](http://arxiv.org/abs/0904.4744))

* [[Heath Emerson]], Robert Yuncken, _Equivariant correspondences and the Borel-Bott-Weil theorem_ ([arXiv:0905.1153](http://arxiv.org/abs/0905.1153))


### Relation to motives and algebraic KK-theory
 {#RelationToMotives}

The general analogy between KK-cocycles and [[motives]] is noted explicitly in 

* {#ConnesConsaniMarcolli05} [[Alain Connes]], Caterina Consani, [[Matilde Marcolli]], *Noncommutative geometry and motives: the thermodynamics of endomotives* ([arXiv:math/0512138](http://arxiv.org/abs/math/0512138))
 

* [[Alain Connes]], [[Matilde Marcolli]], *[[Noncommutative Geometry, Quantum Fields and Motives]]*

and also very briefly in ([Meyer 06](#Meyer06)).  

A relation between [[motivic cohomology]] and bivariant [[algebraic K-theory]] is discussed in 

* [[Guillermo Cortiñas]], [[Andreas Thom]], *Bivariant algebraic K-theory*, J. Reine Angew. Math. 510 (2007), 71&#8211;124. ([arXiv:math/0603531](http://arxiv.org/abs/math/0603531))

* {#Mahanta09} [[Snigdahayan Mahanta]], *Noncommutative correspondence categories, simplicial sets and pro $C^\ast$-algebras* ([arXiv:0906.5400](http://arxiv.org/abs/0906.5400))
 

* {#Mahanta11} [[Snigdahayan Mahanta]], *Higher nonunital Quillen $K'$-theory, KK-dualities and applications to topological $\mathbb{T}$-duality*, Journal of Geometry and Physics, Volume 61, Issue 5 2011, p. 875-889.   ([pdf](http://wwwmath.uni-muenster.de/u/snigdhayan.mahanta/papers/KQ.pdf))
 

* {#GarkushaPanin11} [[Grigory Garkusha]], Ivan Panin, _K-motives of algebraic varieties_ ([arXiv:1108.0375](http://arxiv.org/abs/1108.0375))
 

* [[Grigory Garkusha]], _Algebraic Kasparov K-theory. II_ ([arXiv:1206.0178](http://arxiv.org/abs/1206.0178))

For a collection of literature see also paragraph 1.5 in 

* [[Andrew Blumberg]], [[David Gepner]], [[Gonçalo Tabuada]], _A universal characterization of higher algebraic K-theory_ ([arXiv:1001.2282](http://arxiv.org/abs/1001.2282))

(in the context of [[noncommutative motives]]).

In

* {#Mahanta13} [[Snigdhayan Mahanta]], _Higher nonunital Quillen $K'$-theory, KK-dualities, and applications to topological T-duality_,  J. Geom. Phys., 61 (5), 875-889, 2011 ([pdf](http://wwwmath.uni-muenster.de/u/snigdhayan.mahanta/papers/KQ.pdf), [talk notes](http://wwwmath.uni-muenster.de/u/snigdhayan.mahanta/papers/KKTD.pdf))
 

it is shown that there is a universal functor $KK \longrightarrow NCC_{dg}$ from [[KK-theory]] to the category of [[noncommutative motives]], which is the category of [[dg-categories]] and dg-[[profunctors]] up to homotopy between them. This is given by sending a [[C*-algebra]] to the [[dg-category]] of [[perfect complexes]] of (the unitalization of) its underlying [[associative algebra]].

See also at _[[motivic quantization]]_ and _[[motives in physics]]_.



### In D-brane theory

KK-theory also describes [[RR-field]] [[charges]] and sources in [[D-brane]] theory.

A review is in

* {#Szabo} [[Richard Szabo]], _D-branes and bivariant K-theory_, Noncommutative Geometry and Physics 3 1 (2013): 131. ([arXiv:0809.3029](http://arxiv.org/abs/0809.3029))
 

based on

* [[Jacek Brodzki]], [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]], 

  *D-Branes, RR-Fields and Duality on Noncommutative Manifolds*, Commun. Math. Phys. **277** (2008) 643-706 &lbrack;[arXiv:hep-th/0607020](http://arxiv.org/abs/hep-th/0607020), [doi:10.1007/s00220-007-0396-y](https://doi.org/10.1007/s00220-007-0396-y)&rbrack;

  _Noncommutative correspondences, duality and D-branes in bivariant K-theory_, Adv. Theor. Math. Phys.13:497-552,2009 ([arXiv:0708.2648](http://arxiv.org/abs/0708.2648))

  _D-branes, KK-theory and duality on noncommutative spaces_, J. Phys. Conf. Ser. 103:012004,2008 ([arXiv:0709.2128](http://arxiv.org/abs/0709.2128))


### Smooth refinement and spectral triples

Discussion of KK-theory for [[spectral triples]] is discussed in

* [[Bram Mesland]], _Spectral triples and KK-theory: A survey_ ([arXiv:1304.3802](http://arxiv.org/abs/1304.3802))



[[!redirects Kasparov K-theory]]
[[!redirects bivariant K-theory]]

[[!redirects KK-group]]
[[!redirects KK-groups]]

[[!redirects Kasparov KK-group]]
[[!redirects Kasparov KK-groups]]

[[!redirects Kasparov KK-groups]]