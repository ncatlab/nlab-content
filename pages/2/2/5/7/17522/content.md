
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given two [[vector bundles]] $V_1 \to X$ and $V_2 \to X$ over the same base space $X$, their _tensor product of vector bundles_ $V_1 \otimes V_2 \to X$ is the vector bundle over $X$ whose [[fiber]] over any point is the [[tensor product of vector spaces]] (i.e. the [[tensor product of modules]]) of the respective fibers of $V_1$ and $V_2$ (the [fiber-wise](topological+vector+bundle#FiberwiseOperations) tensor product).

The tensor product of vector bundles makes the category [[Vect(X)]] into a [[symmetric monoidal category|symmetric]] [[monoidal category]], in fact a [[distributive monoidal category]].


## Definition

+-- {: .num_defn }
###### Definition
**(tensor product of [[topological vector bundles]])**

Let $X$ be a [[topological space]], and let $E_1 \to X$ and $E_2 \to X$ be two [[topological vector bundles]] over $X$. 

Let $\{U_i \subset X\}_{i \in I}$ be an [[open cover]] with respect to which both vector bundles locally trivialize (this always exists: pick a [[local trivialization]] of either bundle and form the joint [[refinement]] of the respective [[open covers]] by [[intersection]] of their patches). Let 

$$
  \left\{
    (g_1)_{i j}
    \colon U_i \cap U_j \to GL(n_1)
  \right\}
  \phantom{AAA}
  \text{and}  
  \phantom{AAA}
  \left\{
    (g_2)_{i j}
    \colon
     U_i \cap U_j \longrightarrow GL(n_2)
  \right\}
$$

be the [[transition functions]] of these two bundles with respect to this cover.

For $i, j \in I$ write

$$
  \array{
    (g_1)_{i j} \otimes (g_2)_{i j}
    &\colon&
    U_i \cap U_j
      &\longrightarrow&
    GL(n_1 \cdot n_2)
  }
$$

be the pointwise [[tensor product of vector spaces]] of these transition functions

Then the _tensor product bundle_ $E_1 \otimes E_2$ is the one glued from this tensor product of the transition functions (by [this construction](topological+vector+bundle#TopologicalVectorBundleFromCechCocycle)):

$$
  E_1 \otimes E_2
  \;\coloneqq\;
  \left(
    \left( \underset{i}{\sqcup} U_i \right)
    \times 
    \left(
      \mathbb{R}^{n_1 \cdot n_2}
    \right)
  \right)/ \left( \left\{ (g_1)_{i j} \otimes (g_2)_{i j} \right\}_{i,j \in I} \right)
  \,.
$$
 

=--

## Examples

+-- {: .num_prop #FinitrRankBundleHomomorphismIsSectionOfTensorProductWithDual}
###### Proposition

Let $X$ be a [[topological space]] and let $E_i \overset{p_i}{\to} X$ be a two [[topological vector bundles]] over $X$, of [[finite number|finite]] [[rank of a vector bundle]]. Then a [[homomorphism]] of vector bundles

$$
  f \;\colon\; E_1 \rightarrow E_2
$$

is equivalently a [[section]] of the tensor product of $E_2$ with the [[dual vector bundle]] of $E_1$:


$$
  Hom_{Vect(X)}(E_1, E_2)
   \;\simeq\;
  \Gamma_X( E_1^\ast \otimes_X E_2)
  \,.
$$

Moreover, this section is a trivializing section ([this example](topological+vector+bundle#FiberwiseLinearlyIndependentSectionsTrivialize)) precisely if the corresponding morphism is an [[isomorphism]].

=--


## Related concepts

* [[external tensor product of vector bundles]]

* [[direct sum of vector bundles]]

* [[inner product on vector bundles]]

* [[dual vector bundle]]

* [[tensor product]]

* [[tensor category]]

## References

* [[Max Karoubi]], §4.8 in: _K-Theory -- An introduction_, Grundlehren der mathematischen Wissenschaften **226** Springer (1978) &lbrack;[pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007%2F978-3-540-79890-3](https://link.springer.com/book/10.1007%2F978-3-540-79890-3)&rbrack;



[[!redirects tensor products of vector bundles]]

[[!redirects tensor product of line bundles]]
[[!redirects tensor products of line bundles]]