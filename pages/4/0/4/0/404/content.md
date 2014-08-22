
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Definition

For $C$ any [[category]], its **arrow category** is the [[functor category]]

$$
  Arr(C) := Funct(I,C) = [I,C] = C^I
$$

for $I$ the [[interval category]] $\{0 \to 1\}$.  $Arr(C)$ is also written $[\mathbf{2},C]$, $C^{\mathbf{2}}$, $[\Delta[1],C]$, or $C^{\Delta[1]}$, since $\mathbf{2}$ and $\Delta[1]$ (for the $1$-[[simplex]]) are common notations for the interval category.


This means that the [[objects]] of $Arr(C)$ are the [[morphisms]] (the "arrows", therefore the name) of $C$, while the [[morphisms]] of $Arr(C)$ are pairs of $C$ morphisms constituting [[commuting diagram|commuting]] square [[diagrams]] in $C$. 


## Properties

* $Arr(C)$ is the equivalently the [[comma category]] $(id/id)$ where $id\colon C \to C$ is the [[identity functor]].

* $Arr(C)$ plays the role of a directed [[homotopy|path object]] for categories in that functors
$$
  X \to Arr(Y)
$$
are the same as [[natural transformations]] between functors between $X$ and $Y$.


## Related concepts

* [[path space object]]

* [[slice category]], [[undercategory]]

* [[arrow (∞,1)-category]]

* [[arrow (∞,1)-topos]]


[[!redirects arrow category]]
[[!redirects arrow categories]]
