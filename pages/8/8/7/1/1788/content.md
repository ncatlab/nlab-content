
### Super Fiber functors and their automorphism supergroups
 {#FiberFunctors}

The first step in exhibiting a given [[tensor category]] $\mathcal{A}$ as being a [[category of representations]] is to exhibit its objects as having an [[forgetful functor|underlying]] representation space of sorts, and then an [[action]] represented on that space. Hence a necessary condition on $\mathcal{A}$ is that there exists a [[forgetful functor]]

$$
   \omega \;\colon\; \mathcal{A} \longrightarrow \mathcal{V}
$$

to some other [[tensor category]], such that $\omega$ satisfies a list of properties, in particular it should be a [[symmetric monoidal functor|symmetric]] [[strong monoidal functor]].

Such functors are called _[[fiber functors]]_. The idea is that we think of $\mathcal{A}$ as a [[bundle]] over $\mathcal{V}$, and over each $V \in \mathcal{V}$ we find the [[fiber]] $\omega^{-1}(V)$ of that "bundle", consisting of all those objects in $\mathcal{A}$ whose underlying object in the given $V$.

The main point of [[Tannaka duality]] of tensor categories is the observation that if $\mathcal{A}$ is a [[category of representations]] of some [[group]] $G$, then $G$ also [[action|acts]] by [[automorphisms]] on that [[fiber functor]] (i.e. via [[natural isomorphisms]] of functors). In good cases then this may be turned around, and the full [[automorphism group]] of a fiber functor is identified with the group $G$ for which the objects in its fibers are [[representations]], this is the process of [[Tannaka reconstruction]].

There are slight variants on what one requires of a fiber functor. For the present purpose we fix the following definition

+-- {: .num_defn #FiberFunctor} 
###### Definition

Let $\mathcal{A}$ and $\mathcal{T}$ be two $k$-[[tensor categories]] (def. \ref{TensorCategory}) such that 

1. all [[object of finite length|objects have finite length]];

1. all [[hom spaces]] are of [[finite number|finite]] [[dimension]] over $k$.

Let $R \in CMon(Ind(\mathcal{T}))$ be a [[commutative monoid in a symmetric monoidal category|commutative monoid]] (def. \ref{MonoidsInMonoidalCategory}) in the category of [[ind-objects]] in $\mathcal{T}$ (prop. \ref{IndObjectsInATensorCategory}).  

Then a **[[fiber functor]] on $\mathcal{A}$ over $R$** is a [[functor]]

$$
  \omega \;\colon\; \mathcal{A} \longrightarrow R Mod(Ind(\mathcal{T}))
$$ 

from $\mathcal{A}$ to the [[category of modules|category of]] [[module objects]] over $R$ (def. \ref{ModulesInMonoidalCategory}) in the [[category of ind-objects]] $Ind(\mathcal{T})$ (def. \ref{IndObjectsInATensorCategory}), which is

1. a [[braided monoidal functor|braided]] [[strong monoidal functor]];

1. an [[exact functor]] in both variables.

If here $\mathcal{T} = $ [[sVect]] (def. \ref{CategoryOfSuperVectorSpaces}), then this is called a **super fiber functor**.

=--

([Deligne 02, 3.1](#Deligne02))

Given a super fiber functor $\omega \colon \mathcal{A} \to sVect_k$ (def. \ref{FiberFunctor}) there is an evident notion of its [[automorphism group]]: a [[homomorphism]] between [[functors]] is a [[natural transformation]], and that between [[monoidal functors]] is a [[monoidal natural transformation]], according to def. \ref{LaxMonoidalFunctor}, and this is an [[automorphism]] of functors if it is a [[natural automorphism]]. We write

$$
  Aut(\omega) \in Grp
$$

for this automorphism group.

So far this is a group without geometric structure (a [[discrete group]]). But it is naturally equipped with [[supergeometry]] (super-[[algebraic geometry]]) exhibited by a rule for what the "geometrically parameterized families" of its elements are. (For exposition of this perspective see at _[[motivation for sheaves, cohomology and higher stacks]]_).

Concretely, this means that for each [[supercommutative superalgebra]] $A$ with corresponding affine [[super scheme]] $Spec(A)$ (def. \ref{Affines}, def. \ref{SupercommutativeSuperalgebra}) we are to say what the set

$$
  \underline{Aut}(\omega)(Spec(A))
   \in
  Set
$$

of $Spec(A)$-parameterized elements of $Aut(\omega)$ is. In fact, under parameter-wise multiplication in the group, any such set must inherit group structure, so that we should have not one discrete group, but a system of them, labeled by supercommutative superalgebras:

$$
  \underline{Aut}(\omega)(Spec(A))
   \in
  Grp
  \,.
$$

Moreover, if $A_1 \longrightarrow A_2$ is an algebra homomorphism, hence 

$$
  Spec(A_2) \longrightarrow Spec(A_1)
$$ 

a map of affine super schemes according to def. \ref{SupercommutativeSuperalgebra}, then there should be a group homomorphism 

$$
  \underline{Aut}(\omega)(Spec(A_2))
    \longleftarrow
  \underline{Aut}(\omega)(Spec(A_1))
$$

that expresses how a $Spec(A_1)$-parameterized family of elements of $Aut(\omega)$ becomes a $Spec(A_1)$-parameterized family, under this map.

For a minimum of consistency, this assignment must be such that the identity map on $Spec(A)$ induces the identity on $\underline{Aut}(\omega)(Spec(A))$, and that the composite of two maps of affine superschemes goes to the correspondng composite group homomorphisms.

In conclusion, this says that an algebraic supergeometric structure on $Aut(\omega)$ is the datum of a [[presheaf]] of groups, hence of a [[functor]]

$$
  \underline{Aut}(\omega)
   \;\colon\;
  Aff(sVect)^{op} \simeq CMon(sVect)
   \longrightarrow
  Grp
$$

such that the underlying points are those of $Aut(\omega)$:

$$
  \underline{Aut}(\omega)(Spec(k))
  \simeq
  Aut(\omega)
  \,.
$$

We say this is [[representable functor|representable]] if there exists a [[supercommutative Hopf algebra]] $H$ and a [[natural isomorphism]]


$$
  \underline{Aut}(\omega)
  \simeq
  Hom_{CMon(sVect)}(H,-)
  \,.
$$

+-- {: .num_defn #AutomorphismGroupOfFiberFunctor} 
###### Definition

Let $\omega \colon \mathcal{A} \to \mathcal{B}$ be a  [[fiber functor]]  (def \ref{FiberFunctor}).

For $A \in CMon(\mathcal{B})$ a [[commutative monoid]] (def. \ref{MonoidsInMonoidalCategory}), write

$$
  \omega_A 
   \;\colon\;
  \mathcal{A}
    \stackrel{\omega}{\longrightarrow}
  \mathcal{B}
   \stackrel{A \otimes(-)}{\longrightarrow}
  A Mod(\mathcal{B})
$$

for its image under [[extension of scalars]] to $A$ (prop. \ref{MonoidModuleOverItself}).

With this, the **automorphism group** of $\omega$

$$
  \underline{Aut}(\omega)
  \in 
  PSh(Aff(\mathcal{B}))
$$

is defined by

$$
  \underline{Aut}(\omega)(Spec(A))
   \coloneqq
  Aut(\omega_{A})
  \,.
$$


=--

Specializing def. \ref{AutomorphismGroupOfFiberFunctor} to $\mathcal{B} = $ [[sVect]] (def. \ref{CategoryOfSuperVectorSpaces}), where a commutative monoid is a [[supercommutative superalgebra]] (def. \ref{SupercommutativeSuperalgebra}) it reads as follows:

+-- {: .num_example #AutomorphismSuperGroupOfSuperFiberFunctor} 
###### Example

Let $\omega \colon \mathcal{A} \to sVect$ be a  [[fiber functor|super fiber functor]]  (def \ref{FiberFunctor}).

For $A \in CMon(sVect)$ a [[commutative monoid]] (def. \ref{MonoidsInMonoidalCategory}), write

$$
  \omega_A 
   \;\colon\;
  \mathcal{A}
    \stackrel{\omega}{\longrightarrow}
  sVect
   \stackrel{A \otimes(-)}{\longrightarrow}
  A Mod(sVect)
$$


For $A \in CMon(sVect)$ a [[supercommutative algebra]], write

$$
  \omega_A 
   \;\colon\;
  \mathcal{A}
    \stackrel{\omega}{\longrightarrow}
  sVect
   \stackrel{A \otimes(-)}{\longrightarrow}
  A Mod(sVect)
$$

for its image under [[extension of scalars]] to $A$ (prop. \ref{MonoidModuleOverItself}).

With this, the **automorphism super-group** of $\omega$

$$
  \underline{Aut}(\omega)
  \in 
  PSh(Aff(sVect))
$$

is defined by

$$
  \underline{Aut}(\omega)(Spec(A))
   \coloneqq
  Aut(\omega_{A})
  \,.
$$

=--



+-- {: .num_prop #AutomorphismSupergroupOfFiberFunctorIsRepresentable} 
###### Proposition

For $k$ an [[algebraically closed field]] of [[characteristic zero]], and for $\mathcal{A}$ a $k$-[[tensor category]] equipped with a [[fiber functor|super fiber functor]] $\omega$, then its automorphism supergroup (def. \ref{AutomorphismSuperGroupOfSuperFiberFunctor}) is [[representable functor|representable]]: there exists a [[supercommutative Hopf algebra]] $H_\omega$ and a [[natural isomorphism]]

$$
  \underline{Aut}(\omega)
    \simeq
  Hom_{CMon(sVect)}(H_\omega,-)
  \,.
$$

=--

([Deligne 90, prop. 8.11](#Deligne90))

+-- {: .num_lemma #MonoidalTransformationBetweenFiberFunctorIsIso} 
###### Lemma

every [[monoidal natural transformation]] (def. \ref{LaxMonoidalFunctor}) between two [[fiber functors]] (def. \ref{FiberFunctor}) is an [[isomorphism]] (i.e. a [[natural isomorphism]]).

=--

([Deligne 02, lemma 3.2](#Deligne02))


+-- {: .num_defn #FundamentalSupergroup} 
###### Definition

Let $\mathcal{A}$ be a [[tensor category]] and regard the [[identity]] functor on it as a fiber functor (def. \ref{FiberFunctor}). Then the automorphism group of $id_{\mathcal{A}}$ according to def. \ref{AutomorphismSuperGroupOfSuperFiberFunctor} is called the **fundamental group** of $\mathcal{A}$, denoted:

$$
  \pi(\mathcal{A})
   \coloneqq
  \underline{Aut}(id_{\matchcal{A}})
$$


=--

([Deligne 90, 8.12, 8.13](#Deligne90))

+-- {: .num_example #FundamentalGroupOfCategoryOfSuperVectorSpaces} 
###### Example

The fundamental group (def. \ref{FundamentalSupergroup}) of the [[category of super vector spaces]] [[sVect]] (def. \ref{CategoryOfSuperVectorSpaces}) is $\mathbb{Z}/2$:

$$
  \pi(sVect)
    \simeq
  \mathbb{Z}/2
  \,.
$$

The non-trivial element in $\pi(sVect)$ acts on any super-vector space as the [[endomorphism]] which is the identity on even graded elements, and multiplication by $(-1)$ on odd graded elements.

=--

([Deligne 90, 8.14 iv)](#Deligne90))
