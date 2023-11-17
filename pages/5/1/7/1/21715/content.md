
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Definition

Let $G$ be a [[finite group]]. We write

\[
  \label{OrbitCategory}
  G Orbits \;\subset\; Categories
\]

for the [[orbit category]] of $G$.

+-- {: .num_defn #FiniteDimensionalRationalVectorGSpaces} 
###### Definition
**([[rational vector space|rational]] [[vector G-spaces]])**

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

(using in the first line that forming [[dual linear maps]] is an [[equivalence of categories]] from [[finite dimensional vector spaces]] to their [[opposite category]].)

In generalization of (eq:FunctorCategoryFromOrbitCategoryToOppositeRationalVectorSpaces), dropping the finiteness condition, we write

\[
  \label{DualVectorGSpaces}
  DualVector G Spaces
  \;\coloneqq\;
  Functors
  \Big(
    G Orbits
    \,,\,
    VectorSpaces_{\mathbb{Q}}
  \Big)  
\]

=--

The category (eq:DualVectorGSpaces) is denoted $Vec_G^\ast$ in ([Triantafillou 82](#Triantafillou82)).


## Properties

### Projective objects
 {#ProjectiveObjects}

> Beware that this section uses different notational conventions than the rest of the entry. None of the rest of the entry is necessary for reading this section here.

Notation:

* $G$ a [[finite group]],

* $N(H)/H$ the "[Weyl group](Weyl+group#InEquivariantHomotopyTheory)" of a [[subgroup]] $H \subset G$,

* $Orb_G$ the [[orbit category]] of $G$, equivalently thought of as the [[full subcategory]] of [[G-sets]] $G/H$ of [[cosets]] for [[subgroups]] $H \subset G$,

* $\mathbb{Q}$ the [[ground field]] of [[rational numbers]],

* $Mod_{\mathbb{Q}}^{Orb_G^{op}}$ the [[presheaf category]] on $Orb_G$ with [[coefficients]] in [[rational vector spaces]],

* $\mathbb{Q}[K]$ the [[group algebra]] over the [[rational numbers]], of a [[finite group]] $K$.

\linebreak

\begin{definition}
\label{TheProjectiveGenerators}
([T82, Def. 3.1](#Triantafillou82))
\linebreak

  For 

  * $H \subset G$,

  * $V_H \,\in\, Mod_{ \mathbb{Q}[N(H)/H] }$

define

$$
  \begin{array}{l}
    \underline{V}_H 
    \;\in\;
    Mod_{\mathbb{Q}}^{Orb_G^{op}}
    \\
    \underline{V}_H 
    \;\equiv\;
    \mathbb{Q}\big[
      Orb_G(-,G/H)
    \big]
    \underset{
      \mathbb{Q}[N(H)/H]
    }{\otimes}
    V_H
    \mathrlap{\,.}
  \end{array}
$$
\end{definition}


\begin{proposition}
  \label{ProjectiveGeneratorsAreIndeedProjective}
  ([T82, Prop. 3.2](#Triantafillou82))
  \linebreak
  The objects $\underline{V}_H$ from Def. \ref{TheProjectiveGenerators} are [[projective object|projective]] in $Mod_{\mathbb{Q}}^{Orb_G^{op}}$.
\end{proposition}


\begin{proposition}\label{CharacterizationOfProjectives}
([T82, Prop. 3.4](#Triantafillou82))
\linebreak
 Every [[projective object]] $P \,\in\, Mod_{\mathbb{Q}}^{Orb_G^{op}}$ is a [[direct sum]] of projective generators as in Prop. \ref{TheProjectiveGenerators}.
\end{proposition}

\begin{proof}
We make a bunch of choices:

First, in each [[conjugacy class]] $[H]$ of [[subgroups]] $G$ choose one representative $H \subset G$.

For that $H \hookrightarrow G$, consider the joint [[span]] of the [[images]] of 

$$
  P(G/H \twoheadrightarrow G/H')
  \;\colon\;
  P(G/H') \to P(G/H)
$$

for all intermediate [[subgroup]]-inclusions $H \hookrightarrow H' \hookrightarrow G$:

$$
  0
  \to
  \underset{ H' \supset H }{
    \textstyle{\sum}
  } 
  im\big(
    P(G/H \twoheadrightarrow G/H')
  \big)
  \hookrightarrow
  P(G/H)
  \twoheadrightarrow
  P(G/H)
    \big/
  \underset{ H' \supset H }{
    \textstyle{\sum}
  } 
  im\big(
    P(G/H \twoheadrightarrow G/H')
  \big)
  \to 
  0
  \,.
$$

On the right we have exhibited the [[quotient vector space]] of the inclusion of the joint images on the left (hence the joint [[cokernel]]) making a [[short exact sequence]] of [[rational vector spaces]].

Since [every short exact sequence of vector spaces splits](split+exact+sequence#OfVectorSpaces), we may next *choose* a [[split exact sequence|splitting]]:

\[
  \label{TheSplitting}
  \sigma_H 
    \;\;\colon\;\;
  P(G/H)
    \big/
  \underset{ H' \supset H }{
    \textstyle{\sum}
  } 
  im\big(
    P(G/H \twoheadrightarrow G/H')
  \big)
    \xhookrightarrow{\phantom{---}}
  P(G/H)
  \,,
\]

whose [[image]] we denote by

\[
  \label{VHInProjectiveCover}
  V_H
  \;\;\;\coloneqq\;\;\;
  \sigma
  \Big(
    P(G/H)
      \big/
    \underset{ H' \supset H }{
      \textstyle{\sum}
    } 
    im\big(
      P(G/H \twoheadrightarrow G/H')
    \big)
  \Big)
  \xhookrightarrow{\phantom{---}}
  P(G/H)
  \,.
\]

(In fact, we need this splitting $N(H)/H$-equivariantly: Since we are in [[characteristic zero]] this follows by the fact that every $N(H)/H$-[[linear representation|representation]] splits as a [[direct sum]] of [[irreducible representations]], and by the first part of [[Schur's lemma]], which says that there are no non-zero maps between distinct such direct summands.)

Via these (images of) chosen splittings (eq:VHInProjectiveCover), we may define a morphism in $Mod_{\mathbb{Q}}^{Orb_G^{op}}$ as follows, out of the direct sum of their underlined versions from \ref{TheProjectiveGenerators}:

\[  
  \label{ComparisonMorphismForProjectiveDecomposition}
  \array{
    p 
    &\colon&
    \underset{
      [H] 
    }{\oplus}
    \underline{V}_H
    &\longrightarrow&
    P
    \\
    p_{G/K}
    &\colon&
    \underset{
      [H]
    }{\oplus}
    \mathbb{Q}
    \big[
      Orb_G(G/K, G/H)
      \underset{
        \mathbb{Q}[N(H)/H]
      }{\otimes}
      V_H
    \big]
    &\longrightarrow&
    P(G/K)
    \\
    &&
    \big(
      G/K \xrightarrow{ f } G/H
    \big)
    \,\otimes\,
    v_H
    &\mapsto&
    P(f)(v_H)
    \,,
  }
\]

which is manifestly functorial in $G/K$ (via functoriality of $P$) and hence well-defined.

Since all the direct summands on the left are projective by Prop. \ref{ProjectiveGeneratorsAreIndeedProjective}, it is now sufficient to prove that (eq:ComparisonMorphismForProjectiveDecomposition) is an [[isomorphism]]. Since isomorphisms in [[functor categories]] are detected objectwise and  since [[rational vector spaces]] form a [[balanced category]] (see [there](balanced+category#AbelianCategoriesAreBalanced)) for this it is sufficient to show that for all $K \subset G$ the morphism $p_{G/K}$ (eq:ComparisonMorphismForProjectiveDecomposition) is both an [[epimorphism]] and a [[monomorphism]].

First to see that that $p_{G/K}$ is an epimorphism: To start with, it is clearly surjective onto the summand $V_K$. Hence it is next sufficient to show that given $v_K \in P(G/K)$ which is in the image under $P(G/K \twoheadrightarrow G/H)$ of some $\widehat{v}_H \in P(G/H)$ then it is also in the image of $p_{G/K}$. As before, this is clear for those $\widehat{v}_H \in V_H$. Hence next, as before, it is sufficient to show this for those $\widehat{v}_H$ which are in the image under some $P(G/H \twoheadrightarrow G/H')$ of some $v_{H'} \in P(G/H')$... And so on. Since $G$ is a [[finite group]], this recursive argument eventually terminates with $V_G = P(G/G)$.

Finally, to see that $p_{G/K}$ (eq:ComparisonMorphismForProjectiveDecomposition) is a monomorphism. It is here (only) that we use the assumption that $P$ is [[projective object|projective]]. With the previous point, this implies a [[lift]] $p'$ in the following diagram in $Mod_{\mathbb{Q}}^{Orb_G^{op}}$:

\begin{tikzcd}[sep=25pt]
  & 
  \underset{[H]}{\oplus} \underline{V}_H
  \ar[
    d,
    ->>,
    "{ p }"
  ]
  \\
  P
  \ar[r, equals]
  \ar[ur, dashed, "{ p' }"]
  &
  P
\end{tikzcd}

Hence if $v,w \,\in\, P(G/K)$ such that $p'_{G/K}(v) = p'_{G/K}(w)$ then $p_{G/K} \circ  p'_{G/K}(v) = p_{G/k} \circ p'_{G/K}(w)$ hence $v = w$, whence each $p'_{G/K}$ is injective.
\end{proof}

\begin{corollary}([T82, Prop. 3.6](#Triantafillou82))
 Every object $N \,\in\, Mod_{\mathbb{Q}}^{Orb_G}$ admits a [[projective cover]] in the sense of a [[projective object]] $\underset{[H]}{\osum} \underline{V}_H$ and an [[epimorphism]] $p \,\colon\,\underset{[H]}{\osum} \underline{V}_H \twoheadrightarrow N$. 
\end{corollary}
\begin{proof}
  The construction and verification is verbatim as in Prop. \ref{CharacterizationOfProjectives}, omitting only the proof of injectivity in the last step.
\end{proof}

\linebreak

### Injective objects

> The following is [[formally dual|formal dual]] to the [above](#ProjectiveObjects) discussion of projectivity. But beware that, for the time being the notational conventions are differ, as these discussions come from two different edits.

+-- {: .num_example #RestrictionOfVectorGSpacesToWeyGroupRepresentations} 
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

This gives a [[full subcategory]]-inclusion

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
  W_G(H) Representations^{fin}_{l,\mathbb{Q}}
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
\]

or more generally

\[
  \label{NonFiniteRestrictionFromOrbitCategoryRepresentations}
  W_G(H) Representations^{fin}_{r,\mathbb{Q}}
  \overset{
     \;\;\;
     i_H^\ast
     \;\;\;
  }{\longleftarrow}
  DualVector G Spaces
\]


=--

By the general [[end]]-formula for [[right Kan extension]] ([here](Kan+extension#eq:RightKanExtensionViaEndFormula)), this restriction functor has a [[right adjoint]], given as follows:


+-- {: .num_defn #InjectiveAtomsOfGEquivariantDualVectorSpaces} 
###### Definition
**(injective atoms of dual vector $G$-spaces)**

For $H \subset G$ a [[subgroup]] and 

$$
  V \;\in\; W_G(H) Representations^{fin}_{l,\mathbb{Q}} 
$$

a [[rational vector space|rational]] [[finite number|finite]] [[dimension|dimensional]] left [[representation]] of the [[Weyl group]] of $H$ in $G$, write

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

More generally, for 

$$
  V^\ast \;\in\; W_G(H) Representations_{r,\mathbb{Q}} 
$$

set

$$
  \array{
    G Orbits
    &
      \overset{
        I_H(V^\ast)
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


This construction extends to a [[functor]] [[right adjoint]] to the restriction (eq:RestrictionFromOrbitCategoryRepresentations):

$$
  W_G(H) Representations_{\mathbb{Q}}
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
  DualVector G Spaces
$$

=--

([Triantafillou 82, (4.1)](#Triantafillou82), [Golasinski 97a, Lemma 1.1](#Golasinski97a), [Scull 08, Def. 2.2, Lemma 2.3](#Scull08))

+-- {: .num_prop #InjectiveAtomsOfGEquivariantDualVectorSpacesAreIndeedInjectiveAtoms} 
###### Proposition

$\,$

**(i)**
The objects of the form $I_H(V^\ast)$ (Def. \ref{InjectiveAtomsOfGEquivariantDualVectorSpaces}) are [[injective objects]] in dual [[vector G-spaces]] (Def. \ref{FiniteDimensionalRationalVectorGSpaces}).

**(ii)** Every [[injective]] dual vector $G$-space is a [[direct sum]] of objects of this form, specifically (see Def. \ref{InjectiveEnvelope} below):

$$
  \underline{V}
  \;\in\;
  DualVector G Spaces
  \;\;\;
  \text{is injective}
  \;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;
  \underline{V}
  \;\simeq\;
  \underset{
   \big[   
     H \subsetneqq G
   \big]_{conj}
  }{\bigoplus}
  \,
  I_H
  \left(
    \underset{
      K \supset H
    }{\bigcap}
    ker
    \big(
      \underline{V}(G/H)
        \overset{
          \underline{V}(G/H \to G/K)
        }{\longrightarrow}
      \underline{V}(G/K)
    \big)
  \right)
$$

=--

([Triantafillou 82, Section 3 and p. 10](#Triantafillou82), [Scull 08, Lemma 2.4, Prop. 2.5](#Scull08))


+-- {: .num_example #EquivariantPLDeRhamComplex} 
###### Example
**(equivariant PL de Rham complex  in injective dual vector $G$-space)**

Let $S \in G SimplicialSets$ a [[simplicial set]] equipped with $G$-[[action]], say that the _[[equivariant PL de Rham complex]]_ is the [[functor]] on the [[orbit category]]

$$
  \array{
   G Orbits  
    &
    \overset{
      \Omega^\bullet_{PLdR}
      \big(
        Maps(-,X)^G
      \big)
    }{\longrightarrow}
    &
    dgcAlgebras
    \\
    G/H
    &\mapsto&
    \Omega^\bullet_{PLdR}
    \big(
      X^H
    \big)
  }
$$

which to a [[coset space]] $G/H$ assigns the [[PL de Rham complex]] of the $H$-[[fixed locus]] $X^H \subset X$.

Then the underlying dual [[vector G-space]]

$$
  \array{
   G Orbits  
    &
    \overset{
      \Omega^\bullet_{PLdR}
      \big(
        Maps(-,X)^G
      \big)
    }{\longrightarrow}
    &
    dgcAlgebras
    &\overset{}{\longrightarrow}&
    VectorSpaces_{\mathbb{Q}}
  }
$$

is an [[injective object]] (degreewise, in fact).

=--

([Triantafillou 82, Prop. 4.3](#Triantafillou82))

+-- {: .num_cor } 
###### Corollary

Any [[equivariant PL de Rham complex]] (Def. \ref{EquivariantPLDeRhamComplex}) is a [[fibrant object]] in the [[model structure on equivariant connective dgc-algebras]].

=--

(also [Scull 08, Lemma 5.2](#Scull08))


+-- {: .num_defn #InjectiveEnvelope} 
###### Definition
**([[injective envelope]] of [[dual vector G-spaces]])**

For $\underline{V} \in DualVector G Spaces$ (eq:DualVectorGSpaces),
its _[[injective envelope]]_ is

$$
  \underset{
   \big[   
     H \subset G
   \big]_{conj}
  }{\bigoplus}
  \,
  I_H
  \left(
    \underset{
      K \supsetneqq H
    }{\bigcap}
    ker
    \big(
      \underline{V}(G/H)
        \overset{
          \underline{V}(G/H \to G/K)
        }{\longrightarrow}
      \underline{V}(G/K)
    \big)
  \right)
  \,,
$$

where 

1. the [[direct sum]] is over [[conjugacy classes]] of [[subgroups]], with $H \subset G$ on the right any one representative of its conjugacy class,

1. for $H = G$ the argument of $I_H$ is taken to be all of $\underline{V}(G/G)$,

1. $I_H(-)$ is the injective atom construction from Def. \ref{InjectiveAtomsOfGEquivariantDualVectorSpaces}.

=--

([Triantafillou 82, p. 10](#Triantafillou82), [Scull 01, Prop. 7.34](#Scull01),  [Scull 08, Def. 2.6](#Scull08))

+-- {: .num_defn #TensorProductOfInjectiveDualVectorSpaces} 
###### Lemma
**(tensor product of injective dual vector $G$-spaces)**

The object-wise [[tensor product]] of two finite-dimensional [[injective object|injective]] [[dual vector G-spaces]] (Def. \ref{FiniteDimensionalRationalVectorGSpaces}) is again injective.

=--

This is proven as [Golasinski 97b, Lemma 3.6](#Golasinski97b) (use [Golasinski 97b, Remark 1.2](#Golasinski97b) to see that the Lemma does apply to the ordinary tensor product of finite-dimensional vector spaces).

Beware that incorrect versions of this statement had been circulating; for discussion of the literature see [Golasinski 97b, p. 3](#Golasinski97b) and [Scull 01, Prop. 7.36](#Scull01)


## Examples

### Over $G = \mathbb{Z}_2$
  {#ExamplesOverCyclicGroupOfOrder2}

+-- {: .num_example #OrbitCategoryOfCyclicGroupOfOrder2} 
###### Example
**([[orbit category]] of [[cyclic group of order 2|Z/2Z]])**

For equivariance group the [[cyclic group of order 2]]:

$$
  G \;\coloneqq\;  \mathbb{Z}_2 \;\coloneqq\; \mathbb{Z}/2\mathbb{Z}
  \,.
$$

the [[orbit category]] looks like this:

\[
  \label{OrbitCategoryOfZMod2}
  \mathbb{Z}_2
  Orbits
  \;=\;
  \left\{
  \array{
    \mathbb{Z}_2/1
    &
      \overset{
        \phantom{AAAAA}
      }{ 
        \longrightarrow
      }
    &
    \mathbb{Z}_2/\mathbb{Z}_2
    \\
    Aut = \mathbb{Z}_2
    &&
    Aut = 1
  }
  \right\}
\]

i.e.:

$$
  \begin{aligned}
    \mathbb{Z}_2 Orbits
    \big(
      \mathbb{Z}_2/\mathbb{Z}_2
      \,,\,
      \mathbb{Z}_2/\mathbb{Z}_2
    \big)
    \;\simeq\;
    1
    \\
    \mathbb{Z}_2 Orbits
    \big(
      \mathbb{Z}_2/1
      \,,\,
      \mathbb{Z}_2/\mathbb{Z}_2
    \big)
    \;\simeq\;
    \ast
    \\
    \mathbb{Z}_2 Orbits
    \big(
      \mathbb{Z}_2/\mathbb{Z}_2
      \,,\,
      \mathbb{Z}_2/1
    \big)
    \;\simeq\;
    \varnothing
    \\
    \mathbb{Z}_2 Orbits
    \big(
      \mathbb{Z}_2/1
      \,,\,
      \mathbb{Z}_2/1
    \big)
    \;\simeq\;
    \mathbb{Z}_2
  \end{aligned}
$$

=--

Write

$$
  \mathbf{1}, \mathbf{1}_{sgn}
  \;\in\;
  \mathbb{Z}_2 Representations
$$

for the two [[irreducible representations]] (the [[trivial representation]] and the [[sign representation]], respectively) of the [[Weyl group]] $W_{\mathbb{Z}_2}(1) = \mathbb{Z}_2$.

Their induced injective dual vector $\mathbb{Z}_2$-spaces, according to Def. \ref{InjectiveAtomsOfGEquivariantDualVectorSpaces}, are:

$$
  I_1(\mathbf{1})
  \;\;
  \colon
  \;\;
  \;\;\;\;\;
  \array{
    \mathbb{Z}_2/1  
    &\mapsto&
    \mathbb{Z}_2 Reps
    \Big(
      \underset{
        \simeq \, \mathbf{1} \oplus \mathbf{1}_{sgn}
      }{
      \underbrace{
        \mathbb{Q}
        \big[
          \mathbb{Z}_2 Orbits( \mathbb{Z}_2/1, \mathbb{Z}_2/1 )
        \big]   
      }
      }
      \,,\,
      \mathbf{1}
    \Big)
    &
    \simeq 
    &
    \mathbf{1}
    \\
    \big\downarrow 
    &&
    \\
    \mathbb{Z}_2/\mathbb{Z}_2
    &\mapsto&
    \mathbb{Z}_2 Reps
    \Big(
      \underset{
        \simeq \, 0
      }{
      \underbrace{
        \mathbb{Q}
        \big[
          \mathbb{Z}_2 Orbits( \mathbb{Z}_2/\mathbb{Z}_2, \mathbb{Z}_2/1 )
        \big]   
      }
      }
      \,,\,
      \mathbf{1}
    \Big)
    & \simeq
    &
    0
  }
$$

and

$$
  I_1(\mathbf{1}_{sgn})
  \;\;
  \colon
  \;\;
  \;\;\;\;\;
  \array{
    \mathbb{Z}_2/1  
    &\mapsto&
    \mathbb{Z}_2 Reps
    \Big(
      \underset{
        \simeq \, \mathbf{1} \oplus \mathbf{1}_{sgn}
      }{
      \underbrace{
        \mathbb{Q}
        \big[
          \mathbb{Z}_2 Orbits( \mathbb{Z}_2/1, \mathbb{Z}_2/1 )
        \big]   
      }
      }
      \,,\,
      \mathbf{1}_{sgn}
    \Big)
    &
    \simeq 
    &
    \mathbf{1}_{sgn}
    \\
    \big\downarrow 
    &&
    \\
    \mathbb{Z}_2/\mathbb{Z}_2
    &\mapsto&
    \mathbb{Z}_2 Reps
    \Big(
      \underset{
        \simeq \, 0
      }{
      \underbrace{
        \mathbb{Q}
        \big[
          \mathbb{Z}_2 Orbits( \mathbb{Z}_2/\mathbb{Z}_2, \mathbb{Z}_2/1 )
        \big]   
      }
      }
      \,,\,
      \mathbf{1}_{sgn}
    \Big)
    & \simeq
    &
    0
  }
$$

Similarly, write

$$
  \mathbf{1} \;\in\; 1 Representations
$$

for the unique [[irrep]] of the [[Weyl group]] $W_{\mathbb{Z}_2}(\mathbb{Z}_2) = 1$.

Its induced injective dual vector $\mathbb{Z}_2$-spaces, according to Def. \ref{InjectiveAtomsOfGEquivariantDualVectorSpaces}, is:

$$
  I_{\mathbb{Z}_2}(\mathbf{1})
  \;\;
  \colon
  \;\;
  \;\;\;\;\;
  \array{
    \mathbb{Z}_2/1  
    &\mapsto&
    1 Reps
    \Big(
      \underset{
        \simeq \, \mathbf{1}
      }{
      \underbrace{
        \mathbb{Q}
        \big[
          \mathbb{Z}_2 Orbits( \mathbb{Z}_2/1, \mathbb{Z}_2/\mathbb{Z}_2 )
        \big]   
      }
      }
      \,,\,
      \mathbf{1}
    \Big)
    &
    \simeq 
    &
    \mathbf{1}
    \\
    \big\downarrow 
    &&
    &&
    \big\downarrow{}^{\mathrlap{\mathrm{id}}}
    \\
    \mathbb{Z}_2/\mathbb{Z}_2
    &\mapsto&
    1 Reps
    \Big(
      \underset{
        \simeq \, \mathbf{1}
      }{
      \underbrace{
        \mathbb{Q}
        \big[
          \mathbb{Z}_2 Orbits( \mathbb{Z}_2/\mathbb{Z}_2, \mathbb{Z}_2/\mathbb{Z}_2 )
        \big]   
      }
      }
      \,,\,
      \mathbf{1}
    \Big)
    & \simeq
    &
    \mathbf{1}
  }
$$



## Related concepts

* [[equivariant chain complex]]

* [[equivariant dgc-algebra]], [[model structure on equivariant dgc-algebras]]

* [[equivariant rational homotopy theory]]



## References


* {#Triantafillou82} [[Georgia Triantafillou]], _Equivariant minimal models_, Trans. Amer. Math. Soc. **274** (1982) 509-532  &lbrack;[jstor:1999119](http://www.jstor.org/stable/1999119)&rbrack;


* {#Golasinski97a} [[Marek Golasiński]], _Componentwise injective models of functors to DGAs_, Colloquium Mathematicum, Vol. 73, No. 1 (1997)  ([dml:21048](https://eudml.org/doc/210480), [[GolasinskiInjectiveModels.pdf:file]])

* {#Golasinski97b} [[Marek Golasiński]], _Injective models of $G$-disconnected simplicial sets_,  Annales de l'Institut Fourier, Volume 47 (1997) no. 5, p. 1491-1522 ([numdam:AIF_1997__47_5_1491_0](http://www.numdam.org/item/?id=AIF_1997__47_5_1491_0))

* {#Scull01} [[Laura Scull]], _Rational $S^1$-equivariant homotopy theory_, Transactions of the AMS, Volume 354, Number 1, Pages 1-45 2001 ([pdf](http://www.ams.org/journals/tran/2002-354-01/S0002-9947-01-02790-8/S0002-9947-01-02790-8.pdf), [doi:10.1090/S0002-9947-01-02790-8](https://doi.org/10.1090/S0002-9947-01-02790-8))

* {#Scull08} [[Laura Scull]], _A model category structure for equivariant algebraic models_, Transactions of the American Mathematical Society 360 (5), 2505-2525, 2008 ([doi:10.1090/S0002-9947-07-04421-2](https://doi.org/10.1090/S0002-9947-07-04421-2))

[[!redirects vector G-spaces]]

[[!redirects dual vector G-space]]
[[!redirects dual vector G-spaces]]

[[!redirects equivariant vector space]]
[[!redirects equivariant vector spaces]]


