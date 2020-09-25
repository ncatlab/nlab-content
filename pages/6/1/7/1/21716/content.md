
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
**([[equivariant PL de Rham complex]] is [[injective object|injective]] in [[dual vector G-spaces]])**

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

is an [[injective object]].

=--

([Triantafillou 82, Prop. 4.3](#Triantafillou82))

## Related concepts

* [[equivariant rational homotopy theory]]

## References

* {#Triantafillou82} [[Georgia Triantafillou]], _Equivariant minimal models_, Trans. Amer. Math. Soc. vol 274 pp 509-532 (1982) ([jstor:1999119](http://www.jstor.org/stable/1999119))


* {#Scull08} [[Laura Scull]], _A model category structure for equivariant algebraic models_, Transactions of the American Mathematical Society 360 (5), 2505-2525, 2008 ([doi:10.1090/S0002-9947-07-04421-2](https://doi.org/10.1090/S0002-9947-07-04421-2))
