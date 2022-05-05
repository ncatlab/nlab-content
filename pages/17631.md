+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

Catalan numbers are a specific sequence of [[negative number|nonnegative]] [[integers]], here denoted $C_n$, with a ubiquitous [[combinatorics|combinatorial]] interpretations. In terms of [[binomial coefficients]] they are given by

$$ 
  C_n = \frac{1}{n+1}\binom{2 n}{n}
  \,.
$$

The Catalan numbers $C_n$ count a myriad of different families of objects, including:

* matching pairs of $n$ parentheses properly matched (also known as "Dyck words")

* nonisomorphic ordered (planar) binary [[trees]] with $n$ internal [[vertices]]

* monotonic lattice paths in an $n\times n$ grid which do not cross below the diagonal, or equivalently, [[monotone functions]] $f : [n] \to [n]$ such that $x \le f(x)$ for all $0 \le x \le n$ (or in other words, [[pointed endomorphisms]] $[n] \to [n]$ in the [[simplex category|simplex 2-category]] $\Delta$)

and many, many more besides (see [Stanley](#Stanley2015) for 214 such interpretations).

## Related concepts

* [[associahedron]]

## References

* Wikipedia, _[Catalan number](https://en.wikipedia.org/wiki/Catalan_number)_
* Richard P. Stanley, _Catalan addendum_, (to problems in Chapter
6 of _Enumerative Combinatorics_, vol. 2) 96 pp. [pdf](http://www-math.mit.edu/~rstan/ec/catadd.pdf)
* {#Stanley2015} Richard P. Stanley, _Catalan numbers_, 215 pp., Cambridge University Press 2015

For an interpretation in terms of [[species]] (or *structure types*) see

* [[John Baez]], [[James Dolan]], _From Finite Sets to Feynman Diagrams_, ([arXiv:math/0004133](https://arxiv.org/abs/math/0004133), p. 19).

[[!redirects Catalan numbers]]