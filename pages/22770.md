> This entry is about scales in [[algebra]] and [[linear logic]]. For scales in [[geometry]] and [[physics]], see [[length scale]]. 

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The idea of a scale comes from [[Peter Freyd]]. 

## Definition

A __scale__ is a [[minor scale]] $M$ such that 

* for all $a$ and $b$ in $M$, $a \otimes b = (a^\vee \otimes b^\wedge) \vert (a^\wedge \otimes b^\vee)$

* for all $a$ and $b$ in $M$, $a \oplus b = (a^\wedge \oplus b^\vee) \vert (a^\vee \oplus b^\wedge)$

In a scale, $\oplus$ is __[[multiplicative disjunction]]__ and $\otimes$ is __[[multiplicative conjunction]]__. 

The operator __additive [[conjunction]]__ is defined as 

$$a \wedge b \coloneqq a \otimes (a^\bullet \oplus b)$$

and __additive [[disjunction]]__ is defined as 

$$a \vee b \coloneqq a \oplus (a^\bullet \otimes b)$$

## Properties

Every scale with $\bot = \top$ is [[trivial object|trivial]]. 

$\top$ is a [[fixed point]] of $(-)^\vee$ and $\bot$ is a fixed point of $(-)^\wedge$. 

For every $a$ in $M$, $a = a^\vee \vert a^\wedge$. 

For every $a$ in $M$, $a \otimes \odot = a^\wedge \vert \bot$ and $a \oplus \odot = a^\vee \vert \top$. 

As a scale is a [[closed midpoint algebra]], a scale has a [[partial order]]. Let the binary operation $(-)\multimap(-):M \times M \to M$ be defined as 

$$a \multimap b \coloneqq a^\bullet \oplus b$$ 

If $a \multimap b = \top$, then $a \leq b$. 

$(M,\wedge,\vee,\bot,\top)$ forms a [[lattice]]. 

### Ideals of a scale

A subset $\mathcal{I}$ of a scale $M$ is an __[[ideal]]__ if $\bot \in \mathcal{I}$, and $x \vee y \in \mathcal{I}$ if and only if $x \in \mathcal{I}$ and $y \in \mathcal{I}$. An ideal is a __zoom-invariant ideal__ if it is closed under $\bot$-zooming. 

Given an element $a$ in scale $M$, a __principal zoom-invariant ideal__ $((a))$ is the subset of all $b$ in $M$ such that $(\bot\vert)^n b \leq a$ for all large $n$ in $\mathbb{N}$. 

A __[[Jacobson radical]]__ of a scale $M$ is the set $J(M)$ of all $a$ in $M$ such that for all $n$ in $\mathbb{N}$, $x \leq (\bot\vert)^n \top$. $M$ is __semi-simple__ if $J(M)$ is [[trivial]]. 

### As star-autonomous categories

...

## Examples

The [[unit interval]] with $a \vert b \coloneqq \frac{a + b}{2}$, $\odot = \frac{1}{2}$, $a^\bullet = 1 - a$, $\bot = 0$, $\top = 1$, $a^\wedge = max(2a-1,0)$, and $a^\vee = min(2a,1)$ is an example of a scale.

The set of truth values in Girard's [[linear logic]] is a scale. 

## Related concepts

* [[minor scale]]

* [[Heyting scale]]

* [[linear logic]]

## References

* [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))

[[!redirects scales]]
