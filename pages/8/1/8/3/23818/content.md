+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition 

Given [[abelian groups]] $G$ and $H$, a [[quadratic function]] on $G$ with values in $H$ is a map $q: G \to H$ such that the following properties hold:

* (cube relation) For any $x,y,z \in G$,  
$$q(x+y+z) - q(x+y) - q(x+z) - q(y+z) + q(x) + q(y) + q(z) = 0$$
* (homogeneous of degree 2) For any $x \in G$ and any $r \in \mathbb{Z}$, 
$$q(r x) = \sum_{i=0}^{r^2} q(x)$$

A **quadratic abelian group** is an abelian group $G$ equipped with a quadratic function with values in $\mathbb{Z}$. 

## Examples

* Every [[ring]] is a quadratic abelian group. 

## See also

* [[quadratic function]]

* [[abelian group]]

* [[ring]]

* [[Clifford ring]]

[[!redirects quadratic abelian groups]]