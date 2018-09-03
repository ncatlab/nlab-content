+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
=--
=--

Catalan numbers are a specific sequence of nonnegative integers, here denoted $C_n$, with a ubiquitous combinatorial interpretations. In terms of [[binomial coefficient]]s,

$$C_n = \frac{1}{n+1}\binom{2 n}{n}$$

The Catalan numbers $C_n$ count a myriad of different families of objects, including:

* matching pairs of $n$ parentheses properly matched (also known as "Dyck words")

* nonisomorphic ordered (planar) binary trees with $n$ internal vertices

* monotonic lattice paths in an $n\times n$ grid which do not cross below the diagonal, or equivalently, [[monotone functions]] $f : [n] \to [n]$ such that $x \le f(x)$ for all $0 \le x \le n$ (or in other words, [[pointed endomorphisms]] $[n] \to [n]$ in the [[simplex category|simplex 2-category]] $\Delta$)

and many, many more besides (see [Stanley](#Stanley2015) for 214 such interpretations).

## Related concepts

* [[associahedron]]

## References

* Wikipedia, _[Catalan number](https://en.wikipedia.org/wiki/Catalan_number)_
* Richard P. Stanley, _Catalan addendum_, (to problems in Chapter
6 of _Enumerative Combinatorics_, vol. 2) 96 pp. [pdf](http://www-math.mit.edu/~rstan/ec/catadd.pdf)
* {#Stanley2015} Richard P. Stanley, _Catalan numbers_, 215 pp., Cambridge University Press 2015

[[!redirects Catalan numbers]]