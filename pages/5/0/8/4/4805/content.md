
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

For an [[object]] $X$ in a [[category]] with [[coproduct]]s, the **codiagonal** of $X$ is the canonical [[morphism]]

$$
  \nabla : X \coprod X \stackrel{(Id,Id)}{\to} X
  \,.
$$

The dual concept is _[[diagonal]]_ . 

In a [[cartesian bicategory]] $\mathbf{B}$, the pair of terms _diagonal_, _codiagonal_ refer to the canonical comultiplication $\Delta: X \to X \otimes X$ and the dual multiplication $\nabla = \Delta_*: X \otimes X \to X$ on any object. While the comultiplication is not a true diagonal (because $\otimes$ is not a cartesian product in $\mathbf{B}$), it is the diagonal when seen as belonging to the subcategory of _maps_ ([[left adjoints]]), where the restriction of $\otimes$ to $Map(\mathbf{B})$ becomes a [[2-limit|2-product]]. Similarly, $\nabla$ is not a true codiagonal on $\mathbf{B}$, but it becomes a codiagonal in the sense above when seen as belonging to $Map(\mathbf{B})^{op}$, the [[opposite 2-category|opposite]] obtained by reversing $1$-cells but not $2$-cells. 


[[!redirects codiagonal]]
[[!redirects codiagonals]]
[[!redirects codiagonal morphism]]
[[!redirects codiagonal morphisms]]
