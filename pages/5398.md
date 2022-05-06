

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

In an [[associative algebra]] $A$, the **commutant** of a [[set]] $B \subset A$ of elements of $A$ is the set

$$
  B' = \{a \in A | \forall b \in B:  a b = b a \}
$$

of elements in $A$ that commute with all elements in $B$. 

## Properties

The operation of taking a commutant is a [[contravariant functor|contravariant]] map $P(A) \to P(A)$ that is adjoint to itself in the sense of [[Galois connection|Galois connections]]. In other words, we have for any two subsets $B, C \subseteq A$ the equivalence 

$$B \subseteq C' \qquad iff \qquad C \subseteq B'.$$ 

Hence $B \subseteq B''$ and also $B' = B'''$. 

## Related entries

* [[bicommutant theorem]]

* [[centralizer]]

[[!redirects commutants]]