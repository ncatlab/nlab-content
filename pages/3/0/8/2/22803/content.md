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

A pseudolattice ordered abelian group is an [[ordered abelian group]] whose order forms a [[pseudolattice]]. 

## Definition

The following [[algebraic theory|algebraic]] definition is from [[Peter Freyd]]:

A __pseudolattice ordered abelian group__ is an [[abelian group]] $G$ with a function $ramp:G \to G$ such that for all $a$ and $b$ in $G$,

$$
  a = ramp(a) - ramp(-a)
$$

and

$$
  ramp(a - ramp(b)) = ramp(ramp(a) - ramp(b))
$$

The [[join]] $(-)\vee(-):G \times G \to G$ is defined as

$$
  a \vee b \coloneqq a + ramp(b - a)
$$

and the [[meet]] $(-)\wedge(-):G \times G \to G$ is defined as

$$
  a \wedge b \coloneqq a - ramp(a - b)
$$

The order relation is defined as in all pseudolattices: $a \leq b$ if $a = a \wedge b$. 

## Examples

All [[total order|totally ordered]] abelian groups, such as the [[integers]], the [[rational numbers]], and the [[real numbers]], are pseudolattice ordered abelian groups. 

An example of a pseudolattice ordered abelian group that is not totally ordered is the abelian group of [[Gaussian integers]] with $ramp(1) \coloneqq 1$ and $ramp(i) \coloneqq i$. 

## Related concepts

* [[abelian group]]

* [[ordered abelian group]]

* [[pseudolattice]]

* [[totally ordered abelian group]]

* [[pseudolattice ordered ring]]

## References

* [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))
