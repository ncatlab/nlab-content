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

### In commutative rings

For a [[commutative ring]] $R$, a **quadratic function** is a [[function]]  $f \colon R \to R$ with [[elements]] $a \in R$, $b \in R$, $c \in R$ such that for all $x \in R$,

$$f(x) = a \cdot x^2 + b \cdot x + c$$

where $x^2$ is the canonical [[square function]] of the [[multiplication|multiplicative]] [[monoid]]. 

### Between $R$-modules

Given a [[commutative ring]] $R$ and $R$-[[module]]s $M$ and $N$, an __$R$-quadratic function__ on $M$ with values in $N$ is a map $q: M \to N$ such that the following properties hold:

* (cube relation) For any $x,y,z \in M$,  
$$q(x+y+z) - q(x+y) - q(x+z) - q(y+z) + q(x) + q(y) + q(z) = 0$$
* (homogeneous of degree 2) For any $x \in M$ and any $r \in R$, 
$$q(r x) = r^2 q(x)$$

### Between abelian groups

Given [[abelian groups]] $G$ and $H$, a __quadratic function__ on $G$ with values in $H$ is a map $q: G \to H$ such that the following properties hold:

* (cube relation) For any $x,y,z \in G$,  
$$q(x+y+z) - q(x+y) - q(x+z) - q(y+z) + q(x) + q(y) + q(z) = 0$$
* (homogeneous of degree 2) For any $x \in G$ and any $r \in \mathbb{Z}$, 
$$q(r x) = \sum_{i=0}^{r^2} q(x)$$

## See also 

* [[completing the square]]

* [[quadratic formula]]

* [[quadratic form]], [[quadratic refinement]]

* [[linear function]], [[polynomial function]]

* [[real quadratic function]]

* [[quadratic abelian group]]

* [[cubic function]]

## References

See also:

* Wikipedia, _[Quadratic function](https://en.wikipedia.org/wiki/Quadratic_function)_

Discussion of quadratic functions in the form of [[quadratic refinements]] of [[intersection pairings]] (in [[cohomology]]), as a phenomenon in [[algebraic topology]], [[differential topology]] as well as in [[string theory]]:

* [[Mike Hopkins]], [[Isadore Singer]], *[[Quadratic Functions in Geometry, Topology, and M-Theory]]*, J. Diff. Geom. **70** (2005) 329-452 $[$[arXiv:math/0211216](https://arxiv.org/abs/math/0211216), [euclid.jdg/1143642908](https://projecteuclid.org/euclid.jdg/1143642908)$]$

[[!redirects quadratic functions]]