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

* nonisomorphic (rooted planar) binary [[trees]] with $n$ internal [[vertices]];

* ways of defining the product of elements $x_0,\dots,x_n$ within a (not necessarily [[associative]]) [[magma]], or equivalently, ways of fully parenthesizing a string of $n+1$ letters;

* nonisomorphic rooted planar [[trees]] with $n$ [[edges]];

* strings consisting of $n$ well-balanced pairs of parentheses (also known as "Dyck words"), or equivalently, [[surjective]] [[monotone functions]] $w : (n) + (n) \to (2n)$ such that $w(\iota_1 j) \le w(\iota_2 j)$ for all $1 \le j \le n$;

* monotonic lattice paths in an $n\times n$ grid which do not cross below the diagonal, or equivalently, [[injective]] [[monotone functions]] $p : [2n] \to [n] \times [n]$ such that $\pi_1 p(i) \le \pi_2 p(i)$ for all $0 \le i \le 2n$;

* [[monotone functions]] $f : [n] \to [n]$ such that $f(0) = 0$ and $x \le f(x)$ for all $0 \le x \le n$, or in other words, [[pointed endomorphisms]] $[n] \to [n]$ in $\Delta_\bot$ (the sub-2-category of the [[simplex category|simplex 2-category]] $\Delta$ spanned by the first-element-preserving functions);

and many, many more besides (see the [Stanley](#Stanley2015) references and OEIS [A000108](#a000108)).

## Related concepts

* [[associahedron]]

## References

* Wikipedia, _[Catalan number](https://en.wikipedia.org/wiki/Catalan_number)_
* [[Richard P. Stanley]], _Catalan addendum_, (to problems in Chapter 6 of _Enumerative Combinatorics_, vol. 2) 96 pp. [pdf](http://www-math.mit.edu/~rstan/ec/catadd.pdf)
* {#Stanley2015} [[Richard P. Stanley]], _Catalan numbers_, 215 pp., Cambridge University Press 2015
* {#a000108} Sequence [A000108](https://oeis.org/A000108) in the [OEIS](https://oeis.org/)

For an interpretation in terms of [[species]] (or *structure types*) see

* [[John Baez]], [[James Dolan]], _From Finite Sets to Feynman Diagrams_, ([arXiv:math/0004133](https://arxiv.org/abs/math/0004133), p. 19).

[[!redirects Catalan numbers]]