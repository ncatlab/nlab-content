
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

A _tautological equivariant line bundle_ is an [[equivariant vector bundle|equivariant]] [[tautological line bundle]] over a [[projective G-space]].

## Definition

Let $G$ be a [[finite group]] (or maybe a [[compact Lie group]]) and let $V$ be a $G$-[[linear representation]] over some [[topological field|topological]] [[ground field]] $k$, with $k P(V)$ its [[projective G-space]].

Then the corresponding _tautological equivariant line bundle_ is

$$
  \array{
    \mathcal{L}_v
    & \coloneqq & 
    \frac{
      (V \setminus \{0\}) \times k
    }{
      k^\times
    }
    \\
    \big\downarrow
    &&
    \big\downarrow^{\mathrlap{
       \frac{id \times pt}{ k^\times }
    }}
    \\
    k P(V)
    &=&
    \frac{
      (V \setminus \{0\}) \times \ast
    }{
      k^\times
    }
  }
$$

equipped with the induced $G$-[[action]] through $V$ (which passes to the [[quotient spaces]] since the $k$-multiplication action commutes with it, by linearity).

## Related concepts

* [[equivariant complex-oriented cohomology theory]]


[[!redirects tautological equivariant line bundle]]

[[!redirects equivariant tautological line bundle]]
[[!redirects equivariant tautological line bundles]]


