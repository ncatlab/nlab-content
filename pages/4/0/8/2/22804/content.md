+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
#### (0,1)-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A lattice-ordered ring is an [[partially ordered ring]] whose partial order forms a [[lattice]]. Lattices here are assumed not to have top or bottom elements, because otherwise the only such lattice-ordered ring is the [[trivial ring]]. 

## Definition

A **lattice-ordered ring** or **l-ring** is a [[preordered ring]] where the partial order $\lt$ is a [[lattice]]: it has binary [[joins]] and [[meets]]. 

If the relation $\leq$ is only a [[preorder]], then the [[preordered ring]] $R$ is said to be a **prelattice-ordered ring**. 

### Essentially algebraic definition

The following [[essentially algebraic]] definition is adapted from the algebraic definition of [[lattice-ordered abelian group]] by [[Peter Freyd]]:

A __lattice-ordered ring__ is an [[ring]] $R$ with a function $ramp:R \to R$ such that for all $a$ and $b$ in $G$,

$$
  a = ramp(a) - ramp(-a)
$$

$$
  ramp(a - ramp(b)) = ramp(ramp(a) - ramp(b))
$$

and the following [[Horn clause]]: 

$$
  ramp(a) = a \wedge ramp(b) = b \vdash ramp(a b) = a b
$$

An element $a$ in $R$ is __non-negative__ if $ramp(a) = a$. The Horn clause can then be stated as multiplication of non-negative elements is non-negative.

The [[join]] $(-)\vee(-):R \times R \to R$ is defined as

$$
  a \vee b \coloneqq a + ramp(b - a)
$$

the [[meet]] $(-)\wedge(-):R \times R \to R$ is defined as

$$
  a \wedge b \coloneqq a - ramp(a - b)
$$

and the absolute value is defined as 

$$
  \vert a \vert \coloneqq ramp(a) + ramp(-a)
$$

The order relation is defined as in all lattices: $a \leq b$ if $a = a \wedge b$. 

## Examples

All [[total order|totally ordered]] rings, such as the [[integers]], the [[rational numbers]], and the [[real numbers]], are lattice-ordered rings. 

## Related concepts

* [[ring]]

* [[ordered ring]]

* [[lattice]]

* [[totally ordered ring]]

* [[lattice-ordered abelian group]]

## References

* Wikipedia, [Lattice-ordered ring](https://en.wikipedia.org/wiki/Lattice-ordered_ring)

* [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))

[[!redirects l-ring]]
[[!redirects l-rings]]

[[!redirects lattice-ordered ring]]
[[!redirects lattice-ordered rings]]

[[!redirects lattice ordered ring]]
[[!redirects lattice ordered rings]]

[[!redirects prelattice-ordered ring]]
[[!redirects prelattice-ordered rings]]

[[!redirects prelattice ordered ring]]
[[!redirects prelattice ordered rings]]

[[!redirects pseudolattice-ordered ring]]
[[!redirects pseudolattice-ordered rings]]

[[!redirects pseudolattice ordered ring]]
[[!redirects pseudolattice ordered rings]]