
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A weak inverse or quasi-inverse is like an inverse, but weakened to work in situations where being an inverse on the nose would be [[evil]].


## Definitions

Given a [[functor]] $F: C \to D$, a __weak inverse__ of $F$ is a functor $G: D \to C$ with [[natural isomorphism]]s
$$ \iota: id_C \to G \circ F,\; \epsilon: F \circ G \to id_D .$$

If it exists, a weak inverse is unique up to natural isomorphism, and furthermore can be improved to form an [[adjoint equivalence]], where $\iota$ and $\epsilon$ sastisfy the [[triangle identities]].

More generally, given a $2$-[[2-category|category]] $\mathcal{B}$ and a morphisms $F: C \to D$ in $\mathcal{B}$, a __weak inverse__ of $F$ is a morphism $G: D \to C$ with $2$-isomorphisms
$$ \iota: id_C \to G \circ F,\; \epsilon: F \circ G \to id_D .$$

Weak inverses give the proper notion of [[equivalence of categories]] and [[equivalence]] in a $2$-category.  Note that you must use [[anafunctor]]s to get the weak notion of equivalence of categories here without using the [[axiom of choice]].


## Links with homotopy theory

Given the [[geometric realization of categories]] functor $ \vert -\vert: Cat \to Top$, weak inverses are sent to [[homotopy]] inverses. This is because the product with the [[interval groupoid]] is sent to the product with the topological interval $[0,1]$. In fact, less is needed for this to be true, because the classifying space of the [[interval category]] is also the topological interval. If we define a _lax inverse_ to be given by the same data as a weak inverse, but with $\iota$ and $\epsilon$ replaced by [[natural transformation|natural transformations]], then the classifying space functor sends lax inverses to homotopy inverses.  An example of a lax inverse is an [[adjunction]], but not all lax inverses arise this way, as we do not require the triangle identities to hold.

([[David Roberts]]: I'm just throwing this up here quickly, it probably needs better layout or even its own page.) 

## Related concepts

* [[inverse]]

[[!redirects weak inverses]]
