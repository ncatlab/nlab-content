> This entry is about scales in [[algebra]]. For scales in [[geometry]] and [[physics]], see [[length scale]]. 

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

A __scale__ is a [[minor scale]] $(M,\vert, \odot, (-)^\bullet, \bot, \top,(-)^\wedge,(-)^\vee)$ such that 

* for all $a$ and $b$ in $M$, $(a \vert b)^\wedge = (a^\vee \vert b^\wedge)^\wedge \vert (a^\wedge \vert b^\vee)^\wedge$

* for all $a$ and $b$ in $M$, $(a \vert b)^\vee = (a^\wedge \vert b^\vee)^\vee \vert (a^\vee \vert b^\wedge)^\vee$

## Properties

Every scale with $\bot = \top$ is [[trivial object|trivial]]. 

$\top$ is a [[fixed point]] of $(-)^\vee$ and $\bot$ is a fixed point of $(-)^\wedge$. 

For every $a$ in $M$, $a = a^\vee \vert a^\wedge$. 

For every $a$ in $M$, $(a\vert \odot)^\wedge = a^\wedge \vert \bot$ and $(a\vert \odot)^\vee = a^\vee \vert \top$. 

As a scale is a [[closed midpoint algebra]], a scale has a [[partial order]]. Let the binary operation $(-)\multimap(-):M \times M \to M$ be defined as 

$$a \multimap b \coloneqq (a^\bullet \vert b)^\vee$$ 

If $a \multimap b = \top$, then $a \leq b$. 

### Lattice structure

The [[meet]] of $a$ and $b$ is given by

$$a \wedge b \coloneqq (a \vert (a^\bullet \vert b)^\vee)^\wedge$$

and the [[join]] of $a$ and $b$ is given by 

$$a \wedge b \coloneqq (a \vert (a^\bullet \vert b)^\wedge)^\vee$$

### Ideals and filters

...

### As star-autonomous categories

...

## Examples

The [[unit interval]] with $a \vert b \coloneqq \frac{a + b}{2}$, $\odot = \frac{1}{2}$, $a^\bullet = 1 - a$, $\bot = 0$, $\top = 1$, $a^\wedge = max(2a-1,0)$, and $a^\vee = min(2a,1)$ is an example of a scale.

The set of truth values in [[linear logic]] is a scale. 

## Related concepts

* [[minor scale]]

* [[chromatic scale]]

## References

* [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))

[[!redirects scales]]
