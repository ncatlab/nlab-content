
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A [[monoidal category]] is **strict** if its [[associator]] and left/right [[unitors]] are [[identity natural transformations]].


Very explicitely, it means that:
\begin{definition} A strict monoidal category is a category $\mathcal{C}$ equipped with an object $1 \in \mathcal{C}$ and a bifunctor $\otimes:\mathcal{C} \times \mathcal{C} \rightarrow \mathcal{C}$ such that for every objects $A,B,C$ and morphisms $f,g,h$, we have:

* $(A \otimes B) \otimes C = A \otimes (B \otimes C)$
* $1 \otimes A = A$
* $A \otimes 1 = A$
* $(f \otimes g) \otimes h = f \otimes (g \otimes h)$
* $Id_{1} \otimes f = f$
* $f \otimes Id_{1} = f$

\end{definition}

## Related concepts

* [[coherence theorem for monoidal categories]]

* [[permutative category]]

* [[commutative monoidal category]]

[[!redirects strict monoidal categories]]