
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

Then the corresponding _tautological equivariant line bundle_ $\mathcal{L}_V$ is the $k^\ast$-[[fiber bundle]] which is [[associated bundle|associated]] to the canonical $k^\times$-[[principal bundle]] over [[projective G-space]]:

$$
  \array{
    \mathcal{L}_v
    & \coloneqq & 
    \frac{
      (V \setminus \{0\}) \times k^\ast
    }{
      k^\times
    }
    &
    \overset{
      [v,z]
      \mapsto
      \big(
        [v], v \cdot z
      \big)
    }{\hookrightarrow}
    &
    \frac{
      V \setminus \{0\}
    }{
      k^\times
    }    
    \times
    V
    \\
    \big\downarrow
    &&
    \big\downarrow {}^{\mathrlap{
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

and equipped with the induced $G$-[[action]] through $V$ (which passes to the [[quotient spaces]] since the $k$-multiplication action commutes with it, by linearity).

Here 

* $k^\times \,\coloneqq\, k \setminus \{0\}$ is the [[group of units]] of $k$;

* $\frac{(-) \times (-)}{k^\times}$ denotes the [[quotient space]] of a [[product space]] by the [[diagonal action]];

* and $k^\ast$ is $k$ equipped with the dual $k^\times$-action

  $$
    \array{
      k^\times \times k^\ast 
      &\longrightarrow&
      k^\ast
      \\
      (g,z) &\mapsto& z/g
    }
  $$

* so that, for $z \neq 0$,

  $$
    [v,z] 
      \;=\; 
    [v, z \cdot 1] 
      \;=\; 
    [v \cdot z, 1] 
      \;\;\in\;\;
    \frac{
      (V \setminus \{0\}) \times k^\ast
    }{
      k^\times
    }
  $$

## Related concepts

* [[equivariant complex-oriented cohomology theory]]


[[!redirects tautological equivariant line bundle]]

[[!redirects equivariant tautological line bundle]]
[[!redirects equivariant tautological line bundles]]


