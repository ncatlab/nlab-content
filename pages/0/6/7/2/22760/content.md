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

The idea of a midpoint algebra comes from [[Peter Freyd]]. 

## Definition

A __midpoint algebra__ is a [[magma]] $(M,\vert)$ that is commutative, idempotent, and medial: 

* for all $a$ in $M$, $a \vert a = a$

* for all $a$ and $b$ in $M$, $a \vert b = b \vert a$

* for all $a$, $b$, $c$, and $d$ in $M$, $(a \vert b) \vert (c \vert d) = (a \vert c) \vert (b \vert d)$

## Examples

The [[rational numbers]], [[real numbers]], and the [[complex numbers]] with $a \vert b \coloneqq \frac{a + b}{2}$ are examples of midpoint algebras. 

The [[trivial group]] with $a \vert b = a \cdot b$ is a midpoint algebra.

## Related concepts

* [[commutative magma]]

* [[cancellative midpoint algebra]]

* [[symmetric midpoint algebra]]

## References

* Insert proper reference to _Algebraic Real Analysis_ by [[Peter Freyd]]