
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

## Definition

+-- {: .num_prop #StableEquivalenceOfVectorBundles}
###### Definition
**(stable equivalence of [[topological vector bundles]])**

Let $X$ be a [[topological space]]. Define an [[equivalence relation]] $\sim_{stable}$ on [[topological vector bundles]]
over $X$ by declaring two vector bundles $E_1 E_2 \in Vect(X)$ to be equivalent if there exists a
[[trivial vector bundle]] $X \times k^n$ of some [[rank]] $n$ such that after [[tensor product of vector bundles]]
with this trivial bundle, both bundles become [[isomorphism|isomorphic]]

$$
  \left(
    E_1
      \sim_{stable}
    E_2
  \right)
    \;\Leftrightarrow\;
  \underset{n \in \mathbb{N}}{\exists}
  \left(
     E_1 \otimes_X (X \times k^n)
       \;\simeq\;
     E_2 \otimes_X (X \times k^n)
  \right)
  \,.
$$

If $E_1 \sim_{stable} E_2$ we say that $E_1$ and $E_2$ are _stably equivalent vector bundles_.

=--

## Related concepts

* [[topological K-theory]]

[[!redirects stable equivalences of vector bundles]]

[[!redirects stable equivalence class of vector bundles]]
[[!redirects stable equivalence classes of vector bundles]]
