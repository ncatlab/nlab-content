
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

For an [[object]] $X$ in a [[category]] with [[coproducts]], the **codiagonal** of $X$ (or _fold morphism_) is the canonical [[morphism]]
$$
  \nabla : X \sqcup X \stackrel{(Id,Id)}{\to} X.
$$
The dual concept is _[[diagonal]]_ . 

In a [[cartesian bicategory]] $\mathbf{B}$, the pair of terms _diagonal_, _codiagonal_ refer to the canonical comultiplication $\Delta: X \to X \otimes X$ and the dual multiplication $\nabla = \Delta_*: X \otimes X \to X$ on any object. While the comultiplication is not a true diagonal (because $\otimes$ is not a cartesian product in $\mathbf{B}$), it is the diagonal when seen as belonging to the subcategory of _maps_ ([[left adjoints]]), where the restriction of $\otimes$ to $Map(\mathbf{B})$ becomes a [[2-limit|2-product]]. Similarly, $\nabla$ is not a true codiagonal on $\mathbf{B}$, but it becomes a codiagonal in the sense above when seen as belonging to $Map(\mathbf{B})^{op}$, the [[opposite 2-category|opposite]] obtained by reversing $1$-cells but not $2$-cells. 

##Possible confusion

The term 'codiagonal' is also sometimes used in the context of the theory of [[bisimplicial sets]]. For this use see [[total simplicial set]], within that entry.

## Related concepts

* [[diagonal]]

* [[cylinder object]]


[[!redirects codiagonal]]
[[!redirects codiagonals]]
[[!redirects codiagonal morphism]]
[[!redirects codiagonal morphisms]]
[[!redirects codiagonal map]]
[[!redirects codiagonal maps]]

[[!redirects fold morphism]]
[[!redirects fold morphisms]]
[[!redirects fold map]]
[[!redirects fold maps]]