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

The idea of a minor scale comes from [[Peter Freyd]]. 

## Definition

### In terms of zoom operations

A __minor scale__ is a [[symmetric closed midpoint algebra]] $(M,\vert, \odot, (-)^\bullet, \bot, \top)$ with two functions $(-)^\wedge:M\to M$ called __$\top$-zooming__ and $(-)^\vee:M\to M$ called __$\bot$-zooming__ such that for all $a$ in $M$, 

$$(\bot \vert a)^\wedge = \bot$$

$$(\bot \vert a)^\vee = a$$

$$(a \vert \top)^\wedge = a$$

$$(a \vert \top)^\vee = \top$$

Defining binary operators $(-)\otimes(-):M\times M\to M$ as 

$$a \otimes b \coloneqq (a \vert b)^\wedge$$

and $(-)\oplus(-):M\times M\to M$ as 

$$a \oplus b \coloneqq (a \vert b)^\vee$$

the above axioms can be rewritten as 

$$\bot \otimes a = \bot$$

$$\bot \oplus a = a$$

$$a \otimes \top = a$$

$$a \oplus \top = \top$$

__Central dilatations__ can be defined as 

$$b^\dagger \coloneqq ((\odot \vert \bot)\oplus b)^\wedge$$

or as 

$$b^\dagger \coloneqq ((\odot \vert \top)\otimes b)^\vee$$

### In terms of central dilatations

A __minor scale__ is a [[symmetric closed midpoint algebra]] $(M,\vert, \odot, (-)^\bullet, \bot, \top)$ with a function $(-)^\dagger:M\to M$ called __central dilatation__ such that for all $a$ in $M$,

$$(\odot \vert a)^\dagger = a$$

$$(\top \vert (\top \vert a))^\dagger = \top$$

$$(\bot \vert (\bot \vert a))^\dagger = \bot$$

__$\bot$-zooming__ can be defined as 

$$a^\vee \coloneqq ((a \vert (\odot \vert \top))^\dagger)^\dagger$$

and __$\top$-zooming__ can be defined as 

$$a^\wedge \coloneqq (((\bot \vert \odot) \vert a)^\dagger)^\dagger$$

$(-)\otimes(-):M\times M\to M$ can be defined as 

$$a \otimes b \coloneqq (a \vert b)^\wedge$$

and $(-)\oplus(-):M\times M\to M$ can be defined as 

$$a \oplus b \coloneqq (a \vert b)^\vee$$

## Properties

Every minor scale with $\bot = \top$ is [[trivial object|trivial]]. 

Let the binary operation $(-)\vartriangleleft(-):M\times M\to M$ be defined as 

$$a\vartriangleleft b \coloneqq (((a^\bullet \vert \bot)\vert b)^\vee)^\wedge$$

The [[currying]] of $\vartriangleleft$ results in a __dilatation__ $(-)\vartriangleleft:M\to (M\to M)$. For every element $a$ in $M$, dilatation at $a$ is a [[retraction]] of contraction at $a$: $(a\vartriangleleft) \circ (a\vert) = id_M$, where $id_M$ is the [[identity function]] on $M$. 

$\bot$ is a [[fixed point]] of $(-)^\vee$ and $\top$ is a fixed point of $(-)^\wedge$. 

As a minor scale is a [[closed midpoint algebra]], a minor scale has a [[partial order]]. Let the binary operation $(-)\multimap(-):M \times M \to M$ be defined as 

$$a \multimap b \coloneqq a^\bullet \oplus b$$ 

If $a \leq b$, then $a \multimap b = \top$. 

## Examples

The [[unit interval]] with $a \vert b \coloneqq \frac{a + b}{2}$, $\odot = \frac{1}{2}$, $a^\bullet = 1 - a$, $\bot = 0$, $\top = 1$, $a^\wedge = max(2a-1,0)$, and $a^\vee = min(2a,1)$ is an example of a minor scale. 

The set of truth values in Girard's [[linear logic]] is a minor scale. 

## Related concepts

* [[symmetric closed midpoint algebra]]

* [[scale]]

* [[linear logic]]

## References

* [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))


