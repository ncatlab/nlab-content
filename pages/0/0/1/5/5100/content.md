
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

\begin{definition}
Let $\mathcal{S}$ be a category. Let  $\mathbb{C}$ and $\mathbb{D}$ be $\mathcal{S}$-[[indexed categories]], that is, [[pseudofunctors]] $\mathcal{S}^\mathrm{op} \to \mathbf{Cat}$, then an **$\mathcal{S}$-indexed functor** $F:{\mathbb{C}}\to{\mathbb{D}}$ is a [[pseudonatural transformation]] $F \colon \mathbb{C} \Rightarrow \mathbb{D}$: it assigns to each [[object]] $A$ of $\mathcal{S}$ a [[functor]] $F_A:{\mathbb{C}}(A) \to {\mathbb{D}}(A)$ and to each [[morphism]] $f:A\to B$ of $\mathcal{S}$ a [[natural isomorphism]] $\mathbb{D}(f) \circ F_B \cong F_A \circ \mathbb{C}(f)$ that is coherent with respect to the structural isomorphisms of $\mathbb{C}$ and $\mathbb{D}$ (see [[pseudonatural transformation]] for details).
\end{definition}

One can also consider indexed functors between categories indexed by different bases, i.e. morphisms of indexed categories.

\begin{definition}
Let $\mathbb{C} : \mathcal{S}^{op} \to \mathbf{Cat}$ and $\mathbb{D} : \mathcal{T}^{op} \to \mathbf{Cat}$ be [[indexed categories]]. A morphism between them is a pair of a functor $\Phi : \mathcal{S} \to \mathcal{T}$ and a pseudonatural transformation $\Phi^\flat : \Phi^*\mathbb{C} \Rightarrow \mathbb{D}$, where $\Phi^* \mathbb{C} = \mathbb{C} \circ \Phi^{op}$ is reindexing of $\mathbb{C}$ along $\Phi$.
\end{definition}

In other words, it's a lax commutative triangle over $\mathbf{Cat}$.

**Remark**. These morphisms correspond to morphisms of [[fibrations]] through the [[Grothendieck construction]].

## Related concepts

* [[indexed adjoint functor theorem]]

* [[indexed monoidal category]]

## References

Section B1 of 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

[[!redirects indexed functors]]