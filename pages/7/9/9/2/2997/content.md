
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $\sim$ be the [[relation]] of being [[homotopy|homotopic]] (for example between [[morphisms]] in the [[category]] [[Top]]). Let $f:X\to Y$ and $g:Y\to X$ be two morphisms. We say that $g$ is a **left homotopy inverse** to $f$ or that $f$ is a **right homotopy inverse** to $g$ if $g\circ f\sim id_X$. A **homotopy inverse** of $f$ is a map which is simultaneously a left and a right homotopy inverse to $f$. 

$f$ is said to be a [[homotopy equivalence]] if it has a left and a right homotopy inverse. In that case we can choose the left and right homotopy inverses of $f$ to be equal. To show this denote by $g_L$ the left and by $g_R$ the right homotopy inverse of $f$. Then

$$ g_L \sim g_L\circ (f\circ g_R) = (g_L\circ f)\circ g_R \sim g_R. $$

Hence

$$ f\circ g_L\sim f\circ g_R\sim id_X, $$

therefore $g_L$ is not only a left, but also a right, homotopy inverse to $f$. 

This makes sense in any category equipped with an [[equivalence relation]] $\sim$, which is compatible with the composition (and with the equality of morphisms).  

## Examples

* A [[functor]] which is an [[equivalence of categories]] is/has a homotopy inverse with respect to the notion of homotopy given by [[natural isomorphisms]].

* A [[weak homotopy equivalence]] of [[topological spaces]] between [[CW-complexes]] is a [[homotopy equivalence]] and hence has a homotopy inverse.

* A [[weak homotopy equivalence]] of [[simplicial sets]] between [[Kan complexes]] is a [[homotopy equivalence]] and hence has a homotopy inverse.

[[!redirects homotopy inverses]]