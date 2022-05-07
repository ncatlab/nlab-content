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

The idea of a symmetric midpoint algebra comes from [[Peter Freyd]]. 

## Definition

A __symmetric midpoint algebra__ is a [[midpoint algebra]] $(M,\vert)$ with an element $\odot:M$ and a function $(-)^{\bullet}: M \to M$ such that

* for all $a$ in $M$, $(a^{\bullet})^{\bullet} = a$

* for all $a$ and $b$ in $M$, $a^{\bullet} \vert a = \odot$

* for all $a$ and $b$ in $M$, $(a \vert b)^{\bullet} = a^{\bullet} \vert b^{\bullet}$

## Properties

$\odot$ is the only element in $M$ such that $\odot^\bullet = \odot$. 

## Examples

The [[rational numbers]], [[real numbers]], and the [[complex numbers]] with $a \vert b \coloneqq \frac{a + b}{2}$, $\odot = 0$, and $a^{\bullet} = -a$ are examples of symmetric midpoint algebras. 

The [[trivial group]] with $a \vert b = a \cdot b$, $\odot = 1$ and $a^{\bullet} = a^{-1}$ is a symmetric midpoint algebra.

## Related concepts

* [[midpoint algebra]]

* [[cancellative midpoint algebra]]

* [[symmetric cancellative midpoint algebra]]

* [[symmetric midpoint group]]

## References

* [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))


