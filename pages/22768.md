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

The idea of a minor scale comes from [[Peter Freyd]]. Certain minor scales are models of [[multiplicative linear logic]]. 

Minor scales are an example of [[centipede mathematics]]; a lot of this page will be determining which of Freyd's results in _Algebraic Real Analysis_ still applies in minor scales and possible weakenings of the scale identity axiom. 

+-- {: .standout}
Note: The terms _multiplicative conjunction_, _multiplicative disjunction_, _linear implication_, _reverse linear implication_, _additive conjunction_, and _additive disjunction_ used in this page come from [[scales]], which are algebraic models of multiplicative-additive [[linear logics]]. While the same operations may be defined in the same way in minor scales as in scales, the operations may no longer correspond to any linear logic at all, and are simply defined to reduce syntactical complexity in equational sentences and axioms. 
=--

## Definition

### In terms of multiplicative conjunction and disjunction

A __minor scale__ is a [[symmetric closed midpoint algebra]] $(M,\vert, \odot, (-)^\bullet, \bot, \top)$ with two binary operations $(-)\otimes(-):M\times M\to M$ called __[[multiplicative conjunction]]__ and $(-)\oplus(-):M\times M\to M$ called __[[multiplicative disjunction]]__ such that for all $a$ in $M$, 

$$a \otimes b = b \otimes a$$

$$\bot \otimes a = \bot$$

$$a \otimes \top = a$$

$$a \oplus b = b \oplus a$$

$$\bot \oplus a = a$$

$$a \oplus \top = \top$$

__Linear implication__ can be defined as

$$a \multimap b \coloneqq a^\bullet \oplus b$$

__$\bot$-zooming can be defined as 

$$a^\vee \coloneqq a \oplus a$$

and __$\top$-zooming__ can be defined as 

$$a^\wedge \coloneqq (a^\bullet \oplus a^\bullet)^\bullet$$

__Central dilatations__ can be defined as 

$$b^\dagger \coloneqq ((\odot \vert \bot)\oplus b)^\wedge$$

or as 

$$b^\dagger \coloneqq ((\odot \vert \top)\otimes b)^\vee$$

### In terms of linear implication

From $\multimap$ one could define the zoom operators. 

__$\bot$-zooming__ can be defined as 

$a^\vee \coloneqq a^\bullet \multimap a$

__$\top$-zooming__ can be defined as 

$a^\wedge \coloneqq (a \multimap a^\bullet)^\bullet$

### In terms of zoom operations

A __minor scale__ is a [[symmetric closed midpoint algebra]] $(M,\vert, \odot, (-)^\bullet, \bot, \top)$ with two functions $(-)^\wedge:M\to M$ called __$\top$-zooming__ and $(-)^\vee:M\to M$ called __$\bot$-zooming__ such that for all $a$ in $M$, 

$$(\bot \vert a)^\wedge = \bot$$

$$(\bot \vert a)^\vee = a$$

$$(a \vert \top)^\wedge = a$$

$$(a \vert \top)^\vee = \top$$

__Multiplicative conjunction__ can be defined as

$$a \otimes b \coloneqq (a \vert b)^\wedge$$

__Multiplicative disjunction__ can be defined as 

$$a \oplus b \coloneqq (a \vert b)^\vee$$

__Linear implication__ can be defined as

$$a \multimap b \coloneqq a^\bullet \oplus b$$

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

__$\top$-zooming__ can be defined as 

$$a^\wedge \coloneqq (((\bot \vert \odot) \vert a)^\dagger)^\dagger$$

__Multiplicative conjunction__ can be defined as 

$$a \otimes b \coloneqq (a \vert b)^\wedge$$

__Multiplicative disjunction__ can be defined as 

$$a \oplus b \coloneqq (a \vert b)^\vee$$

__Linear implication__ can be defined as

$$a \multimap b \coloneqq a^\bullet \oplus b$$

### Other operations

The binary operation __additive [[conjunction]]__ is defined as 

$$a \wedge b \coloneqq a \otimes (a^\bullet \oplus b)$$

and __additive [[disjunction]]__ is defined as 

$$a \vee b \coloneqq a \oplus (a^\bullet \otimes b)$$

The binary operation __dilatation__ is defined as 

$$a\vartriangleleft b \coloneqq ((a^\bullet \vert \bot)\oplus b)^\wedge$$

or as 

$$a\vartriangleleft b \coloneqq ((a^\bullet \vert \bot)\otimes b)^\vee$$

## Additional possible equational axioms

Here is a list of other possible equational axioms that a minor scale might satisfy: 

* the __scale identities__: for all $a$ and $b$ in $M$, 

$$a \otimes b = (a^\vee \otimes b^\wedge) \vert (a^\wedge \otimes b^\vee)$$

$$a \oplus b = (a^\wedge \oplus b^\vee) \vert (a^\vee \oplus b^\wedge)$$

The rest of the axioms follow from the scale identities if the minor scale is an [[inequality space]]:

* $\top$ is a [[fixed point]] of $(-)^\vee$:

$$\top^\vee = \top$$

* $\bot$ is a fixed point of $(-)^\wedge$:

$$\bot^\wedge = \bot$$  

* the __axiom of compensation__: for all $a$ in $M$,

$$a = a^\vee \vert a^\wedge$$

* the __axioms of central distributivity__: for all $a$ in $M$,

$$a \otimes \odot = a^\wedge \vert \bot$$ 

$$a \oplus \odot = a^\vee \vert \top$$

* the __axiom of balance__: for all $a$ and $b$ in $M$,

$$a \vert (a \multimap b) = b \vert (b \multimap a)$$

* the __disjunction property__: for all $a$ and $b$ in $M$,

$$(a \multimap b) \vee (b \multimap a) = \top$$

* the __coalgebra equation__: for all $a$ in $M$,

$$a^\vee \vee (a^\wedge)^\bullet = \top$$

* __associativity of multiplicative conjunction__: for all $a$, $b$, and $c$ in $M$

$$a \otimes (b \otimes c) = (a \otimes b) \otimes c$$

* __associativity of multiplicative disjunction__: for all $a$, $b$, and $c$ in $M$

$$a \oplus (b \oplus c) = (a \oplus b) \oplus c$$

* the various __[[lattice]] axioms__ for $(M,\top,\bot,\wedge,\vee)$

* for all $a$ and $b$ in $M$, 

$$(a \otimes b) \multimap (a^\wedge \vert b^\wedge) = \top$$

* for all $a$ and $b$ in $M$, 

$$(a^\vee \vert b^\vee) \multimap (a \oplus b) = \top$$

## Properties

Every minor scale with $\bot = \top$ is [[trivial object|trivial]]. 

$\bot$ is a [[fixed point]] of $(-)^\vee$ and $\top$ is a fixed point of $(-)^\wedge$. 

As a minor scale is a [[closed midpoint algebra]], a minor scale has a [[partial order]] $\leq$. If $a \leq b$, then $a \multimap b = \top$. 

The [[currying]] of $\vartriangleleft$ results in a __dilatation at an element__ $(-)\vartriangleleft:M\to (M\to M)$. For every element $a$ in $M$, dilatation at $a$ is a [[retraction]] of contraction at $a$: $(a\vartriangleleft) \circ (a\vert) = id_M$, where $id_M$ is the [[identity function]] on $M$. 

## Examples

The [[unit interval]] with $a \vert b \coloneqq \frac{a + b}{2}$, $\odot = \frac{1}{2}$, $a^\bullet = 1 - a$, $\bot = 0$, $\top = 1$, $a \otimes b = max(a + b - 1,0)$, $a \oplus b = min(a + b,1)$, $a^\wedge = max(2a - 1,0)$ and $a^\vee = min(2a,1)$ is an example of a minor scale. 

The set of truth values in Girard's [[linear logic]] is a minor scale. 

## Related concepts

* [[symmetric closed midpoint algebra]]

* [[scale]]

* [[linear logic]]

* [[centipede mathematics]]

## References

* [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))


