
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

+-- {: .num_example #EquivariantPLDeRhamComplex} 
###### Example

A $G$-equivariant dgc-algebra in the sense of [[equivariant rational homotopy theory]] is a [[functor]] 

$$
  G Orbits
  \longrightarrow
  dgcAlgebras
$$

from the [[orbit category]] of $G$ to the [[category]] of [[dgc-algebras]].

=--



## Examples

+-- {: .num_example #EquivariantPLDeRhamComplex} 
###### Example
**([[equivariant PL de Rham complex]])**

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


## Related concepts

* [[equivariant Sullivan models]]

* [[model structure on equivariant dgc-algebras]]

* [[equivariant rational homotopy theory]]

## References

* {#Triantafillou82} [[Georgia Triantafillou]], _Equivariant minimal models_, Trans. Amer. Math. Soc. vol 274 pp 509-532 (1982) ([jstor:1999119](http://www.jstor.org/stable/1999119))

* [[Marek Golasiński]], _Componentwise injective models of functors to DGAs_, Colloquium Mathematicum, Vol. 73, No. 1 (1997)  ([dml:21048](https://eudml.org/doc/210480), [[GolasinskiInjectiveModels.pdf:file]])

* [[Marek Golasiński]], _Injective models of $G$-disconnected simplicial sets_,  Annales de l'Institut Fourier, Volume 47 (1997) no. 5, p. 1491-1522 ([numdam:AIF_1997__47_5_1491_0](http://www.numdam.org/item/?id=AIF_1997__47_5_1491_0))


* {#Scull08} [[Laura Scull]], _A model category structure for equivariant algebraic models_, Transactions of the American Mathematical Society 360 (5), 2505-2525, 2008 ([doi:10.1090/S0002-9947-07-04421-2](https://doi.org/10.1090/S0002-9947-07-04421-2))

[[!redirects equivariant dgc-algebras]]
