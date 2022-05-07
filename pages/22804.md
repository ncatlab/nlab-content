+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
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

A pseudolattice ordered ring is an [[ordered ring]] whose order forms a [[pseudolattice]]. 

## Definition

The following [[essentially algebraic]] definition is adapted from the algebraic definition of [[pseudolattice ordered abelian group]] by [[Peter Freyd]]:

A __pseudolattice ordered ring__ is an [[ring]] $R$ with a function $ramp:R \to R
r$ such that for all $a$ and $b$ in $G$,

$$
  a = ramp(a) - ramp(-a)
$$

$$
  ramp(a - ramp(b)) = ramp(ramp(a) - ramp(b))
$$

and the following [[Horn clause]]: if $ramp(a) = a$ and $ramp(b) = b$, then $ramp(a b) = a b$ (multiplication of non-negative elements is non-negative)

The [[join]] $(-)\vee(-):R \times R \to R$ is defined as

$$
  a \vee b \coloneqq a + ramp(b - a)
$$

and the [[meet]] $(-)\wedge(-):R \times R \to R$ is defined as

$$
  a \wedge b \coloneqq a - ramp(a - b)
$$

The order relation is defined as in all pseudolattices: $a \leq b$ if $a = a \wedge b$. 

## Examples

All [[total order|totally ordered]] rings, such as the [[integers]], the [[rational numbers]], and the [[real numbers]], are pseudolattice ordered rings. 

## Related concepts

* [[ring]]

* [[ordered ring]]

* [[pseudolattice]]

* [[totally ordered ring]]

* [[pseudolattice ordered abelian group]]

## References

* [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))
