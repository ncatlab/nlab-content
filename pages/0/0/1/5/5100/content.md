
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### $(\infty,2)$-Topos theory
+--{: .hide}
[[!include (infinity,2)-topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _[[indexed category]]_ is a [[2-presheaf]]. An _indexed functor_ is a [[morphism]] of 2-presheaves, the "indexed"-terminology here is traditional in 1-[[topos theory]] and hence indexed functors are usually considered only between [[pseudofunctors]] (as opposed to more general [[2-functors]]).

## Definition

Let $S$ be a category. Let  $\mathbb{C}$ and $\mathbb{D}$ be $S$-[[indexed categories]], that is, [[pseudofunctors]] $S^\mathrm{op} \to Cat$, then an **$S$-indexed functor** $F:{\mathbb{C}}\to{\mathbb{D}}$ is a [[pseudonatural transformation]] $F \colon \mathbb{C} \Rightarrow \mathbb{D}$: it assigns to each [[object]] $A$ of $S$ a [[functor]] $F^A:{\mathbb{C}}^A\to{\mathbb{D}}^A$ and to each [[morphism]] $f:A\to B$ of $S$ a [[natural isomorphism]] $\mathbb{D}(f) \circ F^B \cong F^A \circ \mathbb{C}(f)$ that is coherent with respect to the structural isomorphisms of $\mathbb{C}$ and $\mathbb{D}$ (see [[pseudonatural transformation]] for details).

## Related concepts

* [[indexed adjoint functor theorem]]

* [[indexed monoidal category]]

## References

Section B1 of 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

[[!redirects indexed functors]]