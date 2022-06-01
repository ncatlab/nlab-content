[[!redirects pseudolattice ordered abelian groups]]
[[!redirects l-group]]
[[!redirects l-groups]]

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

A pseudolattice ordered abelian group or l-group is an [[ordered abelian group]] whose order forms a [[pseudolattice]]. 

## Definition

### With the join operation

A __pseudolattice ordered abelian group__ or __l-group__ is an [[abelian group]] $G$ with a binary [[join]] operation $(-)\vee(-):G \times G \to G$ such that $(G, \vee)$ is a [[commutative magma|commutative]] [[idempotent]] [[semigroup]], and 

* for all $a \in G$, $b \in G$, $c \in G$, $a \vee b = b$ implies that $(a + c) \vee (b + c) = b + c$ and $(c + a) \vee (c + b) = c + b$

The meet is defined as 

$$
  a \wedge b \coloneqq -(-a \vee -b),
$$

the ramp function is defined as 

$$
  ramp(a) \coloneqq a \vee 0, 
$$

and the absolute value is defined as 

$$
  \vert a \vert \coloneqq a \vee -a
$$

The order relation is defined as in all pseudolattices: $a \leq b$ if $a = a \wedge b$. 

### With the ramp function 

The following [[algebraic theory|algebraic]] definition is from [[Peter Freyd]]:

A __pseudolattice ordered abelian group__ or __l-group__ is an [[abelian group]] $G$ with a function $ramp:G \to G$ such that for all $a$ and $b$ in $G$,

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

the [[meet]] $(-)\wedge(-):G \times G \to G$ is defined as

$$
  a \wedge b \coloneqq a - ramp(a - b)
$$

and the absolute value is defined as 

$$
  \vert a \vert \coloneqq ramp(a) + ramp(-a)
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

* [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))