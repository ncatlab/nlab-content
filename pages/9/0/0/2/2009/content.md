
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A __skewfield__ (also spelled skew-field), or __division ring__ is a [[unitality|unital]] [[ring]] where each non-[[zero]] [[element]] has a two-sided [[inverse]] and the multiplicative identity element $1$ is not zero. Of course, one can require left and right inverse separately, as for an associative binary operation, if an element has both a left and a right inverse the two inverses are the same.

Equivalently, skewfield is an [[associative unital algebra|associative unital]] $\mathbb{Z}$-[[reciprocal algebra]] where the multiplicative identity element $1$ is not zero. 

Terminology "division ring" points to the fact that this is a unital ring in which any element can be divided by any nonzero element from the left and right, more precisely, the equations $a x = b$ and $y a = b$ have unique solutions iff $a\neq 0$.

A [[commutative ring|commutative]] skewfield is called a _[[field]]_, but sometimes in specialized works on skewfields one often says simply _field_ for _skewfield_. In particular, a specific class of skewfields are called the free fields and the hypercorrection "free skewfield" is extremely rarely used in that context. 

In [[constructive mathematics]] and [[internalization|internally]], the same issues appear for skewfields as for [[fields]], and may be dealt with in the same way.

[[linear algebra|Linear algebra]] is often understood in the generality of division rings, namely the usual notions of _[[linear basis]]_, _[[dimension]]_, _[[linear map]]_, [[matrix]] of a linear map with respect to two bases and so on, and [[Gauss elimination]] procedure, hold without changes for left or right [[vector spaces]] over a division rings.

## Properties

Every finite skewfield is a field (Wedderburn's little theorem).

## Sources of examples

### Quotients of domains

For every commutative domain $R$ there is an [[epimorphism#epiring|epimorphism of rings]] $R\to Q$ which is an injection and $Q$ is a [[field]]. This epimorphism is unique up to isomorphism in the overcategory $R/Rings$ and the field $Q$ is called the quotient field of $R$.

For a noncommutative domain $R$ such an injective epimorphism of rings may not exist, or if it exists it is in general nonunique. For this reason many constructions of quotient skewfields are studied in the literature. 

If $R$ is a left or right [[Ore domain]] then one can define the Ore quotient skewfield as the field of all left or right fractions with all nonzero denominators. 

### Wedderburn-Artin theorem

An important appearance of division rings is via the [[Wedderburn-Artin theorem]]: every simple Artinian ring is isomorphic to a matrix ring of a division ring. (Consequently, every semisimple Artinian ring is a finite direct sum of such).

### Finite dimensional division algebras

Any finite-dimensional algebra without zero divisors is a skew-field. Any division ring is a division algebra over its [[center]], but it may not be finite dimensional over its center.

The most famous noncommutative example of a skewfield is the skewfield of [[quaternions]]. 

The [[Frobenius theorem]] states that apart from the fields of [[real number|real]] and [[complex numbers]] and quaternions, there are no associative finite-dimensional [[division algebras]] over the real numbers; and even if one includes nonassociative finite-dimensional division algebras one obtains only one more example (the [[octonions]]). See at _[[normed division algebra]]_ for more on this.


## Related concepts

* [[division algebra]]

* [[reciprocal algebra]]

* [[Dieudonné determinant]]

* [[division rig]]

* [[noncommutative rational function]]

## References

* Encyclopaedia of Mathematics, [skew-field](https://encyclopediaofmath.org/wiki/Skew-field)
* [[Peter Draxl]], _Skew fields_, London Math. Soc. Lecture notes __81__, Cambridge University Press 1983 ([doi:10.1017/CBO9780511661907](https://doi.org/10.1017/CBO9780511661907), ISBN:9780511661907)
* [[Paul M. Cohn]], _Free rings and their relations_, Academic Press (1971) &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/cohnfree.pdf)&rbrack;

category: algebra

[[!redirects division ring]]
[[!redirects division rings]]
[[!redirects reciprocal ring]]
[[!redirects reciprocal rings]]
[[!redirects skew field]]
[[!redirects skew fields]]
[[!redirects skew-field]]
[[!redirects skew-fields]]
[[!redirects skewfield]]
[[!redirects skewfields]]
