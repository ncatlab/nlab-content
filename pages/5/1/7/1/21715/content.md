
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

### Injective objects

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

By the general [[end]]-formula for [[right Kan extension]], this restriction functor has a [[right adjoint]], given as follows:


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

([Triantafillou 82, (4.1)](#Triantafillou82), [Scull 08, Def. 2.2, Lemma 2.3](#Scull08))

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


+-- {: .num_defn #EquivariantPLDeRhamComplex} 
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

* {#Triantafillou82} [[Georgia Triantafillou]], _Equivariant minimal models_, Trans. Amer. Math. Soc. vol 274 pp 509-532 (1982) ([jstor:1999119](http://www.jstor.org/stable/1999119))

* {#Scull01} [[Laura Scull]], _Rational $S^1$-equivariant homotopy theory_, Transactions of the AMS, Volume 354, Number 1, Pages 1-45 2001 ([pdf](http://www.ams.org/journals/tran/2002-354-01/S0002-9947-01-02790-8/S0002-9947-01-02790-8.pdf), [doi:10.1090/S0002-9947-01-02790-8](https://doi.org/10.1090/S0002-9947-01-02790-8))

* {#Scull08} [[Laura Scull]], _A model category structure for equivariant algebraic models_, Transactions of the American Mathematical Society 360 (5), 2505-2525, 2008 ([doi:10.1090/S0002-9947-07-04421-2](https://doi.org/10.1090/S0002-9947-07-04421-2))

[[!redirects vector G-spaces]]

[[!redirects dual vector G-space]]
[[!redirects dual vector G-spaces]]

[[!redirects equivariant vector space]]
[[!redirects equivariant vector spaces]]


