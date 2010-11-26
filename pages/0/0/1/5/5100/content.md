
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let  $\mathbb{C}$ and $\mathbb{D}$ be $\mathbb{E}$-[[indexed categories]], that is, [[pseudofunctors]] $\mathbb{E}^\mathrm{op} \to Cat$.

Then an **$\mathbb{E}$-indexed functor** $F:{\mathbb{C}}\to{\mathbb{D}}$ is a [[pseudonatural transformation]] $F \colon \mathbb{C} \Rightarrow \mathbb{D}$: it assigns to each [[object]] $A$ of $\mathbb{E}$ a [[functor]] $F^A:{\mathbb{C}}^A\to{\mathbb{D}}^A$ and to each [[morphism]] $f:A\to B$ of $\mathbb{E}$ a [[natural isomorphism]] $\mathbb{D}(f) \circ F^B \cong F^A \circ \mathbb{C}(f)$ that is coherent with respect to the structural isomorphisms of $\mathbb{C}$ and $\mathbb{D}$ (see [[pseudonatural transformation]] for details).


[[!redirects indexed functors]]