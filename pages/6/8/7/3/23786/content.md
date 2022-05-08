
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

# Contents #
* table of contents 
{: toc}

## Idea

The [[fragment]] of [[first-order theory|first order]] [[Peano arithmetic]] as described in [Edward Nelson's paper](#Nelson).

## Definition 

Nelson arithmetic is done in the fragment of first order [[Peano arithmetic]] consisting of a [[predicate]] $\mathcal{C}$ satisfying the following [[axioms]]:

1. $\forall_x \neg s(x) = 0$; 

1. $\forall_{x, y} s(x) = s(y) \Rightarrow x = y$; 

1. $\forall_x x + 0 = x$, 

1. $\forall_{x, y} x + s(y) = s(x+y)$; 

1. $\forall_x x \cdot 0 = 0$; 

1. $\forall_{x, y} x \cdot s(y) = x \cdot y + x$; 

1. $\mathcal{C}(0)$; 

1. $\forall_{x} \mathcal{C}(x) \Rightarrow \mathcal{C}(s(x))$; 

## See also

* [[Peano arithmetic]]
* [[finite mathematics]]

## References 

* {#Nelson} [[Edward Nelson]], _Warning Signs of a Possible Collapse of Contemporary Mathematics_ ([pdf](https://web.math.princeton.edu/~nelson/papers/warn.pdf))

