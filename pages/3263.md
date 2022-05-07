
#Contents#
* table of contents
{:toc}

## Idea

The classical **hypergeometric series** (introduced by [[Gauss]]) are solutions of certain [[ordinary differential equations]] of second order.

Special cases appear in classical problems of [[mathematical physics]], solutions to the [[wave equation]], Laplace equation or similar are attacked by Fourier method of separation of variables (cf. [[Legendre polynomial]], [[Hermite polynomial]]). 

## Definition

The hypergeometric series is defined by the formula,

$$
{}_p F_q (a_1,\ldots,a_p; b_1,\ldots, b_q; x) = \sum_{n=0}^\infty 
\frac{(a_1)_n (a_2)_n\cdots (a_p)_n}{(b_1)_n (b_2)_n\cdots (b_q)_n}\frac{x^n}{n!}
$$

where $(a)_0 = 1$ and, for $k = 1,2,3,\ldots$

$$
(a)_k := a (a+1) (a+2) \cdots (a+k-1)
$$

is the shifted [[factorial]]. In fact let $\sum_{n = 0}^\infty c_n$ be any series of complex numbers such that $c_{n+1}/c_n$ is a rational function of $n$. Then we can find $x,p,q,a_1,\ldots,a_p,b_1,\ldots, b_q$ to write
$$
\frac{c_{n+1}}{c_n} = \frac{(n+a_1)(n+a_2)\cdots (n+a_p) x}{(n+b_1)(n+b_2)\cdots (n+b_q)(n+1)}
$$
and $\sum c_n = c_0 {}_p F_q(a_1,\ldots,a_p; b_1,\ldots, b_q; x)$.

There are variants like the confluent hypergeometric function (e.g. [[Bessel functions]]), $q$-hypergeometric functions and the basic hypergeometric series. The classical orthogonal polynomials appear as special cases for choices of parameters. There is a recent elliptic version due Spiridonov. 

There are now modern generalizations to many variables due Aomoto and another variant due [[Mikhail Kapranov]], [[Israel Gelfand]] and [[Andrei Zelevinsky]]. These multidimensional generalizations express pairings between representations of quantum groups at root of unity and representations of affine Lie algebras, which can be interpreted as pairings between certain kind of homlogy and cohomology on configuration spaces. This has been extensively studied by Varchenko, Terao and others; often in connection to the study of (complements of) [[arrangements of hyperplanes]] in $\mathbb{C}^n$. [[Selberg integral|Selberg-type integrals]] are involved. 

## References

* G. E. Andrews, R. Askey, R. Roy, _Special functions_, Enc. of Math. and its Appl. __71__, Cambridge Univ. Press 1999

* G. Gasper, M. Rahman, _Basic hypergeometric series_ (1990) 

* [[Israel Gelfand|I. M. Gelfand]], M. M. [[Kapranov]], [[Andrei Zelevinsky|A. Zelevinsky]], _Discriminants, resultants and multidimensional determinants_, Birkh&#228;user 1994, 523 pp.


* [[Ian G. Macdonald]], _Hypergeometric functions I_, 1987 ([arxiv/1309.4568](http://arxiv.org/abs/1309.4568))

In relation to the [[Knizhnik-Zamolodchikov equation]] and [[quantum groups]]:

* [[Alexander Varchenko]], _Multidimensional hypergeometric functions and representation theory of Lie algebras and quantum groups_, Adv. Ser. in Math. Phys. __21__, World Sci. Publ. 1995. x+371 pp. ([doi:10.1142/2467](https://doi.org/10.1142/2467))

* V. Tarasov, [[Alexander Varchenko]], _Geometry of $q$-hypergeometric functions, quantum affine algebras and elliptic quantum groups_, Ast&#233;risque __246__ (1997), vi+135 pp. ([arXiv:q-alg/9703044](https://arxiv.org/abs/q-alg/9703044), [numdam:AST_1997__246__R1_0](http://www.numdam.org/item/AST_1997__246__R1_0))



Online entries/resources on hypergeometric function:

* at Wolframworld: [hypergeometric function](http://mathworld.wolfram.com/HypergeometricFunction.html), [confluent hypergeometric functon of the first kind](http://mathworld.wolfram.com/ConfluentHypergeometricFunctionoftheFirstKind.html), [confluent hypergeometric functon of the second kind](http://mathworld.wolfram.com/ConfluentHypergeometricFunctionoftheSecondKind.html), [generalized hypergeometric function](http://mathworld.wolfram.com/GeneralizedHypergeometricFunction.html), [$q$-hypergeometric function](http://mathworld.wolfram.com/q-HypergeometricFunction.html), [regularized hypergeometric function](http://mathworld.wolfram.com/RegularizedHypergeometricFunction.html)

* wikipedia: [hypergeometric series](http://en.wikipedia.org/wiki/Hypergeometric_series), [confluent hypergeometric function](http://en.wikipedia.org/wiki/Confluent_hypergeometric_function)

* [[Alexander Varchenko]]: [list](http://www.math.unc.edu/Faculty/av/complete.htm) of publications

There is also a far reaching elliptic generalization

* V. P. Spiridonov, _Classical elliptic hypergeometric functions and their applications_, [pdf](http://www.math.kobe-u.ac.jp/publications/rlm18/17); _Aspects of elliptic hypergeometric functions_, [arxiv/1307.2876](http://arxiv.org/abs/1307.2876)

[[!redirects hypergeometric functions]]