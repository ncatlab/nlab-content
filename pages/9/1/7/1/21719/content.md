
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
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


## Definition

Let $G$ be a [[finite group]].

+-- {: .num_prop } 
###### Proposition

There is a [[model category]]-[[mathematical structure|structure]] on the [[category]] 

$$
  Functors
  \big(
    G Orbits
    \,,\,
    CochainComplexes^{\geq 0}_{\mathbb{Q}}
  \big)
$$

of connective $G$-[[equivariant cochain complexes]] (i.e. with [[differential]] of degree +1) over the [[rational numbers]], whose

$\mathrm{W}$ -- [[weak equivalences]] are the [[quasi-isomorphisms]] over each $G/H \in G Orbits$;

$Cof$ -- [[cofibrations]] are the [[positive number|positive]]-degree wise [[injections]] over each $G/H \in G Orbits$;

$Fib$ -- [[fibrations]] are the morphisms which over each $G/H \in G Orbits$ are degree-wise [[surjections]] whose degreewise [[kernels]] are [[injective objects]] (in the [[category]] of [[vector G-spaces]]).

=--

([Scull 08, Theorem 3.1](#Scull08))

+-- {: .num_example } 
###### Example

For $G = 1$ the [[trivial group]], this reduces to the [[injective model structure on connective cochain complexes]].

=--

## Related concepts

* [[model structure on equivariant dgc-algebras]]

## References

* {#Scull08} [[Laura Scull]], _A model category structure for equivariant algebraic models_, Transactions of the American Mathematical Society 360 (5), 2505-2525, 2008 ([doi:10.1090/S0002-9947-07-04421-2](https://doi.org/10.1090/S0002-9947-07-04421-2))

[[!redirects model structures on equivariant chain complexes]]
