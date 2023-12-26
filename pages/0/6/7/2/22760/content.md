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

## Properties

The [[currying]] of the midpoint operation $\vert$ results in the __contraction__ $(-)\vert : M \to (M \to M)$. Contractions are midpoint [[homomorphisms]]: for all $a$, $b$, and $c$ in $M$, $(a \vert) (b \vert c) = ((a \vert) b) \vert ((a \vert) c)$. 

## Examples

The [[rational numbers]], [[real numbers]], and the [[complex numbers]] with $a \vert b \coloneqq \frac{a + b}{2}$ are examples of midpoint algebras. 

The [[trivial group]] with $a \vert b = a \cdot b$ is a midpoint algebra.

## Related concepts

* [[commutative magma]]

* [[cancellative midpoint algebra]]

* [[symmetric midpoint algebra]]

## References

* [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))

* [[Martín Escardó]] and [[Alex Simpson]]. *A universal characterization of the closed Euclidean interval.* In 16th Annual IEEE Symposium on Logic in Computer Science, Boston, Massachusetts, USA, June 16-19, 2001, Proceedings, pages 115–125. IEEE Computer Society, 2001. ([doi:10.1109/LICS.2001.932488](https://doi.org/10.1109/LICS.2001.932488), [pdf](http://www.cs.bham.ac.uk/~mhe/papers/interval.pdf))
