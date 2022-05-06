
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
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

Let $G$ be a [[finite group]].

+-- {: .num_defn #EquivariantPLDeRhamComplex} 
###### Definition
**(equivariant PL de Rham complex )**

Let $S \in G SimplicialSets$ be a [[simplicial set]] equipped with $G$-[[action]], for instance the [[singular simplicial set]] of a [[topological G-space]].

The _equivariant PL de Rham complex_ of $S$ is the [[equivariant dgc-algebra]] given as the [[functor]] from the [[orbit category]] of $G$ to the category of [[dgc-algebras]]

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

=--

## Properties

+-- {: .num_prop #EquivariantPLDeRhamComplexIsInjectiveInDualVectorGSpaces} 
###### Proposition
**([[equivariant PL de Rham complex]] is degreewise [[injective object|injective]] in [[dual vector G-spaces]])**

The [[dual vector G-space]] underlying the equivariant PL de Rham complex (Def. \ref{EquivariantPLDeRhamComplex})

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

is degreewise an [[injective object]].

=--

([Triantafillou 82, Prop. 4.3](#Triantafillou82))

+-- {: .num_cor } 
###### Corollary

Any equivariant PL de Rham complex (Def. \ref{EquivariantPLDeRhamComplex}) is a [[fibrant object]] in the [[model structure on equivariant connective dgc-algebras]].

=--

(also [Scull 08, Lemma 5.2](#Scull08))

In fact:

+-- {: .num_prop} 
###### Proposition
**([[Quillen adjunction between equivariant simplicial sets and equivariant connective dgc-algebras]])**

Let $G$ be a [[finite group]].

The $G$-[[equivariant PL de Rham complex]]-construction is the [[left adjoint]] in a [[Quillen adjunction]] between

* the [[opposite model structure|opposite]] of the [[projective model structure on equivariant connective dgc-algebras]]

* the [[model structure on equivariant simplicial sets]] 

  (i.e.: the global projective [[model structure on functors]] from the [[opposite category|opposite]] of the [[orbit category]] to the [[classical model structure on simplicial sets]])

$$
  \big(
    G dgcAlgebras^{\geq 0}_{k}
  \big)^{op}_{proj}
  \underoverset
    {
      \underset
        {\;\;\; exp \;\;\;}
        {\longrightarrow}
    }
    {
      \overset
        {\;\;\;\Omega^\bullet_{PLdR}\;\;\;}
        {\longleftarrow}
    }
    {\bot_{\mathrlap{Qu}}}
  G SimplicialSets_{Qu}
$$

=--

([Scull 08, Prop. 5.1](#Scull08))


## Related concepts

* [[equivariant rational homotopy theory]]

## References

* {#Triantafillou82} [[Georgia Triantafillou]], _Equivariant minimal models_, Trans. Amer. Math. Soc. vol 274 pp 509-532 (1982) ([jstor:1999119](http://www.jstor.org/stable/1999119))


* {#Scull08} [[Laura Scull]], _A model category structure for equivariant algebraic models_, Transactions of the American Mathematical Society 360 (5), 2505-2525, 2008 ([doi:10.1090/S0002-9947-07-04421-2](https://doi.org/10.1090/S0002-9947-07-04421-2))
