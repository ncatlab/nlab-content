
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

+-- {: .num_defn #CharElement}
###### Definition

For $A$ an [[abelian group]] and given a symmetric [[bilinear form]]

$$
  \langle-,-\rangle \;\colon\; A\times A \longrightarrow \mathbb{Z}
$$

then a _characteristic element_ of the bilinear form is an element $\lambda\in A$ such that for all $x\in A$ the [[equation]]

$$
  \langle x,x\rangle = \langle x,\lambda \rangle\; mod\;2
$$

holds, or in other words such that 

$$
  \langle x,x\rangle \pm \langle x,\lambda \rangle \in \mathbb{Z}
$$

is divisible by $2\in \mathbb{Z}$.

=--

+-- {: .num_remark}
###### Remark

Often this is considered for the bilinear form being an [[intersection product]] in which case $A$ is a [[cohomology group]] and so in this case one also often speaks of _characteristic cohomology classes_.

=--


## Properties

### Relation to quadratic refinements
 {#RelationToQuadraticRefinements}

+-- {: .num_prop #QuadRef}
###### Proposition

A characteristic element determines a [[quadratic refinement]] $q_\lambda$ of $\langle-,-\rangle$ by

$$
  q_\lambda 
    \colon 
  x \mapsto 
  \tfrac{1}{2}\left(
     \langle x,x\rangle
     + 
     \langle x,\lambda\rangle
  \right)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This follows by trivial direct computation:

$$
  \begin{aligned}
    q_\lambda(x  + y) - q_\lambda(x)- q_\lambda(y)
    & =
    \tfrac{1}{2}
    \left(
      \left(x^2 + y^2 + 2 x y + \lambda x + \lambda y\right)
      -
      \left(x^2 + \lambda x\right)
      -
      \left(y^2 + \lambda y\right)
    \right)
    \\
    & = 
    x y
  \end{aligned} 
$$

the only point being that the prefactor $\tfrac{1}{2}$ indeed makes sense, by def. \ref{CharElement}.

=--

## Examples

+-- {: .num_example #WuClassForIntersectionPairing}
###### Example

Characteristic elements for the [[intersection pairing]] on integral [[ordinary cohomology]] are integral lifts of the [[Wu classes]], hence [[integral Wu structures]]. 

=--


## References

Discussion of the refinement of [[integral Wu structures]] as the characteristic elements of the [[intersection product]] from [[ordinary cohomology]] to [[ordinary differential cohomology]] is in

* {#HopkinsSinger02} [[Michael Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_, ([arXiv:math.AT/0211216](http://arxiv.org/abs/math.AT/0211216))

Further discussion of the use of characteristic elements in the construction of [[Theta characteristics]] is in

* {#PoonenRains11} Bjorn Poonen, Eric Rains, _Self cup products and the theta characteristic torsor_ ([arXiv:1104.2105](http://arxiv.org/abs/1104.2105))


[[!redirects characteristic element of a bilinear form]]
[[!redirects characteristic elements of a bilinear form]]
[[!redirects characteristic elements of bilinear forms]]
