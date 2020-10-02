
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
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

## Idea

Where the [[projective model structure on connective dgc-algebras]] models the [[rational homotopy theory]] of rationally [[finite type]] [[nilpotent topological spaces]] (by the [[fundamental theorem of dg-algebraic rational homotopy theory]]), its $G$-[[equivariant cohomology|equivariant]] enhancement ([Scull 08](#Scull08)) models $G$-[[equivariant rational homotopy theory]] of [[topological G-spaces]]:

Using [[Elmendorf's theorem]], the underlying [[category]] is that of [[diagrams]] of connective [[dgc-algebras]] parametrized over the [[orbit category]] of $G$: _$G$-[[equivariant dgc-algebras]]_. A key technical aspect of this generalization is that not all [[objects]] are [[injective object|injective]] anymore, but otherwise the definitions and properties of the model structure proceed in analogy to [Bousfield-Gugenheim](model+structure+on+dg-algebras#BousfieldGugenheim76)'s [[projective model structure on connective dgc-algebras]]. Notably, the [[minimal cofibrations]] coincide with the equivariant [[minimal Sullivan models]] earlier considered by [Triantafillou 82](#Triantafillou82).

## Definition
 {#Definition}

+-- {: .num_prop } 
###### Proposition

There is a [[model category]]-[[mathematical structure|structure]] on the [[category]] 

$$
  Functors
  \big(
    G Orbits
    \,,\,
    dgcAlgebras^{\geq 0}_{\mathbb{Q}}
  \big)
$$

of connective $G$-[[equivariant dgc-algebras]] (i.e. with [[differential]] of degree +1) over the [[rational numbers]], whose [[weak equivalences]] and [[fibrations]] are those of the underlying [[model structure on equivariant connective cochain complexes]], hence:

$\mathrm{W}$ -- [[weak equivalences]] are the [[quasi-isomorphisms]] over each $G/H \in G Orbits$;

$Fib$ -- [[fibrations]] are the morphisms which over each $G/H \in G Orbits$ are degree-wise [[surjections]] whose degreewise [[kernels]] are [[injective objects]] (in the [[category]] of [[vector G-spaces]]).

=--

([Scull 08, Theorem 3.2](#Scull08))


## Properties

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

* [[vector G-space]]

* [[equivariant chain complex]], [[model structure on equivariant chain complexes]]

* [[equivariant dgc-algebra]]

* [[equivariant PL de Rham complex]]

* [[equivariant Sullivan model]]

* [[equivariant cohomology]]

* [[equivariant rational homotopy theory]]

* [[equivariant rational stable homotopy theory]]

* [[model structure on topological G-spaces]]


## References

* {#Triantafillou82} [[Georgia Triantafillou]], _Equivariant minimal models_, Trans. Amer. Math. Soc. vol 274 pp 509-532 (1982) ([jstor:1999119](http://www.jstor.org/stable/1999119))


* [[Marek Golasiński]], _Equivariant rational homotopy theory as a closed model category_, Journal of Pure and Applied Algebra Volume 133, Issue 3, 30 December 1998, Pages 271-287 (<a href="https://doi.org/10.1016/S0022-4049(97)00127-8">https://doi.org/10.1016/S0022-4049(97)00127-8</a>)

  (for Hamiltonian groups)

* {#Scull08} [[Laura Scull]], _A model category structure for equivariant algebraic models_, Transactions of the American Mathematical Society 360 (5), 2505-2525, 2008 ([doi:10.1090/S0002-9947-07-04421-2](https://doi.org/10.1090/S0002-9947-07-04421-2))

[[!redirects model structures on equivariant dgc-algebras]]

[[!redirects model structure on equivariant connective dgc-algebras]]
[[!redirects model structures on equivariant connective dgc-algebras]]

[[!redirects projective model structure on equivariant connective dgc-algebras]]
[[!redirects projective model structures on equivariant connective dgc-algebras]]

