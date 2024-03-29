
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #Charts}
###### Definition
**([[local chart]] and [[atlas]] and gluing function)

Given an $n$-dimensional [[topological manifold]] $X$ (def. \ref{TopologicalManifold}), then 

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/ChartsOfAManifold.png" width="400"> 
</div>


1. an [[open subset]] $U \subset X$ and a [[homeomorphism]] $\phi \colon \mathbb{R}^n \overset{\phantom{A}\simeq\phantom{A}}{\to} U$ is also called a _[[local coordinate chart]]_ of $X$.

1. an [[open cover]] of $X$ by local charts $\left\{ \mathbb{R}^n \overset{\phi_i}{\to} U \subset X \right\}_{i \in I}$ is called an _[[atlas]]_ of the topological manifold.

1. denoting for each $i,j \in I$ the [[intersection]] of the $i$th chart with the $j$th chart in such an atlas by

   $$
     U_{i j} \coloneqq U_i \cap U_j
   $$ 

   then the induced homeomorphism

   $$
     \mathbb{R}^n
       \supset
        \phantom{AA}
     \phi_i^{-1}(U_{i j})
       \overset{\phantom{A}\phi_i\phantom{A}}{\longrightarrow}
     U_{i j}
       \overset{\phantom{A}\phi_j^{-1}\phantom{A}}{\longrightarrow}
     \phi_j^{-1}(U_{i j})
       \phantom{AA}
       \subset
     \mathbb{R}^n
   $$

   is called the _gluing function_ or _coordinate transformation_ from chart $i$ to chart $j$.

> graphics grabbed from [[The Geometry of Physics - An Introduction|Frankel]]


=--

## Related concepts

* [[transition function]]

[[!redirects gluing functions]]


[[!redirects coordinate transformation]]
[[!redirects coordinate transformations]]
