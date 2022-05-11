+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Group theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition 

A **quadratic abelian group** is an [[abelian group]] $G$ with a function $q: G \to \mathbb{Z}$ such that the following properties hold:

* (cube relation) For any $x,y,z \in G$,  
$$q(x+y+z) - q(x+y) - q(x+z) - q(y+z) + q(x) + q(y) + q(z) = 0$$
* (homogeneous of degree 2) For any $x \in G$ and any $r \in \mathbb{Z}$, 
$$q(r x) = r^2 q(x)$$

## Examples

* Every [[ring]] is a quadratic abelian group. 

* Every [[inner product abelian group]] is a quadratic abelian group with $q(x) \coloneqq \langle x, x \rangle$. 

## See also

* [[quadratic function]]

* [[abelian group]]

* [[ring]]

* [[Clifford ring]]

* [[inner product abelian group]]

[[!redirects quadratic abelian groups]]