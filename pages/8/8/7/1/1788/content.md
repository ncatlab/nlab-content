
Let $G$ be a [[finite group]].

We write

\[
  \label{OrbitCategory}
  G Orbits \;\subset\; Categories
\]

for the [[orbit category]] of $G$.

+-- {: .num_defn #FiniteDimensionalRationalVectorGSpaces} 
###### Definition
**([[finite-dimensional vector space|finite dimensional]] [[rational vector space|rational]] [[vector G-spaces]])**

We say that the _category of finite-dimensional vector G-spaces_ is 
the [[functor category|category of functors]] from the [[opposite category|opposite]] of the [[orbit category]] to the [[category]] of [[finite-dimensional vector space|finite-dimensional]] [[rational vector spaces]]:

\[
  \begin{aligned}
  Vector G Spaces^{fin}_{\mathbb{Q}}
  & 
    \coloneqq
  \;
  PSh
  \Big(
    G Orbits
    \,,\,
    VectorSpaces_{\mathbb{Q}}^{\mathrm{fin}}
  \Big)
  \\
  &
  \coloneqq
  \;
  Functors
  \Big(
    G Orbits^{op}
    \,,\,
    VectorSpaces_{\mathbb{Q}}^{\mathrm{fin}}
  \Big)
  \end{aligned}
\]

Its [[opposite category]] we call the 
_category of finite-dimensional dual vector G-spaces_:

\[
  \label{FunctorCategoryFromOrbitCategoryToOppositeRationalVectorSpaces}
  \begin{aligned}
  \big(
    Vector G Spaces^{fin}_{\mathbb{Q}}
  \big)^{op}
  &
    \simeq
  \;
  PSh
  \Big(
    G Orbits^{op}
    \,,\,
    VectorSpaces_{\mathbb{Q}}^{\mathrm{fin}}
  \Big)
  \\
  & 
  =
  \;
  Functors
  \Big(
    G Orbits
    \,,\,
    VectorSpaces_{\mathbb{Q}}^{\mathrm{fin}}
  \Big)
  \end{aligned}
\]

(Using that forming [[dual linear maps]] is an [[equivalence of categories]] from [[finite dimensional vector spaces]] to their [[opposite category]].)

=--

+-- {: .num_defn #RestrictionOfVectorGSpacesToWeyGroupRepresentations} 
###### Example
(restriction of vector $G$-spaces to Weyl group representations)

Let $H \subset G$ any [[subgroup]]. Notice that its [[Weyl group]] is the [[automorphism group]] of its [[coset space]] in the [[orbit category]]:

\[
  \label{WeylGroup}
  G Orbits
  \big(
    G/H
    \,,\,
    G/H
  \big)
  \;\;
  \simeq
  \;\;
  Aut_{G Orbits}
  \big(
    G/H
  \big)
  \;\;
    \simeq
  \;\;
  W_G(H)
  \;\;
    \coloneqq
  \;\;
  N_G(H)/H
\]

This gives an [[full subcategory]]-inclusion

$$
  \mathbf{B}
  W_G(H)
  \;
  \overset{\;\;i_H\;\;}{\hookrightarrow}
  \;
  G Orbits
$$

of the [[delooping]] category of they Weyl group into the [[orbit category]] of $G$ (eq:OrbitCategory), and hence a restriction functor

\[
  \label{RestrictionFromOrbitCategoryRepresentations}
  W_G(H) Representations^{fin}_{\mathbb{Q}}
  \overset{
     \;\;\;
     (-)^\ast
     \,\circ\, 
     i_H^\ast
     \;\;\;
  }{\longleftarrow}
  \big(
    Vector G Spaces_{\mathbb{Q}}^{fin}
  \big)^{op}
  \,.
\]

=--

By the general [[end]]-formula for [[right Kan extension]], this restriction functor has a [[right adjoint]], given as follows:


+-- {: .num_defn #InjectiveAtomsOfGEquivariantDualVectorSpaces} 
###### Definition
**(injective atoms of dual vector $G$-spaces)**

For $H \subset G$ a [[subgroup]] and 

$$
  V \;\in\; H Representations^{fin}_{\mathbb{Q}} 
$$

a [[rational vector space|rational]] [[finite number|finite]] [[dimension|dimensional]] left $H$-[[representation]], write

$$
  \array{
    G Orbits
    &
      \overset{
        I_H(V)
      }{\longrightarrow}
    &
    \mathbb{Q}VectorSpaces
    \\
    G/K
    &\mapsto&
    W_G(H) Representations
    \Big(  
      \mathbb{Q}
      \big[
        G Orbits
        (  
          G/K, G/H
        )  
      \big]
      \,,\,
      V^\ast
    \Big)
  }
$$

for the [[functor]] from the $G$-[[orbit category]] to [[rational vector spaces]] which assigns to a [[coset space]] $G/K$ the vector space of [[homomorphisms]] of right [[actions]] by the [[Weyl group]] (eq:WeylGroup) from the [[hom-set]] $G Orbits\big(G/K, G/H \big)$ to the [[dual vector space]] equipped with its [[dual linear map|dual action]].

This construction extends to a [[functor]] [[right adjoint]] to the restriction (eq:RestrictionFromOrbitCategoryRepresentations):

$$
  W_G(H) Representations^{fin}_{\mathbb{Q}}
  \underoverset{
    \underset{
      \;\;\;
        I_H
      \;\;\;
    }{
      \longrightarrow
    }
  }{
    \overset{
       \;\;\;
       (-)^\ast
       \,\circ\, 
       i_H^\ast
       \;\;\;
    }{\longleftarrow}
  }
  {\bot}
  \big(
    Vector G Spaces_{\mathbb{Q}}^{fin}
  \big)^{op}
$$

=--

([Triantafillou 82, (4.1)](#Triantafillou82), [Scull 08, Def. 2.2, Lemma 2.3](#Scull08))

+-- {: .num_defn #InjectiveAtomsOfGEquivariantDualVectorSpacesAreIndeedInjectiveAtoms} 
###### Proposition

**(i)**
The objects of the form $I_H(V)$ (Def. \ref{InjectiveAtomsOfGEquivariantDualVectorSpaces}) are [[injective objects]] in dual [[vector G-spaces]] (Def. \ref{FiniteDimensionalRationalVectorGSpaces}).

**(ii)** Every [[injective]] dual vector $G$-space is a [[direct sum]] of objects of this form.

=--

([Triantafillou 82, Section 3](#Triantafillou82), [Scull 08, Lemma 2.4, Prop. 2.5](#Scull08))


***

## Reference

* {#Triantafillou82} [[Georgia Triantafillou]], _Equivariant minimal models_, Trans. Amer. Math. Soc. vol 274 pp 509-532 (1982) ([jstor:1999119](http://www.jstor.org/stable/1999119))


* {#Scull08} [[Laura Scull]], _A model category structure for equivariant algebraic models_, Transactions of the American Mathematical Society 360 (5), 2505-2525, 2008 ([doi:10.1090/S0002-9947-07-04421-2](https://doi.org/10.1090/S0002-9947-07-04421-2))

