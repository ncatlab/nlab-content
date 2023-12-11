
#Contents#
* table of contents
{:toc}

## Idea

The classical **hypergeometric series** (introduced by [[Gauss]]) are [[complex number|complex]] solutions of certain [[ordinary differential equations]] of second order, the hypergeometric differential equation. 

Special cases appear in classical problems of [[mathematical physics]], as solutions to the [[wave equation]], Laplace equation or similar when attacked by Fourier method of separation of variables (cf. [[Legendre polynomial]], [[Hermite polynomial]]). 

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

is the shifted [[factorial]]. In fact, let $\sum_{n = 0}^\infty c_n$ be any series of complex numbers such that $c_{n+1}/c_n$ is a rational function of $n$. Then we can find $x,p,q,a_1,\ldots,a_p,b_1,\ldots, b_q$ to write
$$
\frac{c_{n+1}}{c_n} = \frac{(n+a_1)(n+a_2)\cdots (n+a_p) x}{(n+b_1)(n+b_2)\cdots (n+b_q)(n+1)}
$$
and $\sum c_n = c_0\cdot {}_p F_q(a_1,\ldots,a_p; b_1,\ldots, b_q; x)$.

### Classical case, ${}_2 F_1$

Hypergeometric function $F = {}_2 F_1(a,b;c;x)$ satisfies the ordinary differential equation
$$
x(1-x)\frac{d^2 F}{d x^2} + [c-(a+b-1)x]\frac{d F}{d x}
- a b F = 0.
$$
For $Re(c)\gt 0$, $Re(b)\gt 0$ function ${}_2 F_1$ can be represented as the [[Euler integral]]
$$
{}_2 F_1(a,b;c;x) = \frac{\Gamma(c)}{\Gamma(b)\Gamma(c-b)}\int_0^1 t^b (1-t)^{c-b-1}(1-t x)^{-a} d t,\,\,\,\,x\notin [1,+\infty).
$$
The value of this function at origin is $1$. The second solution of the differential equation around $0$ is 
 $x^{1-c} {}_2 F_1(a-c+1,b-c+1;2-c;x)$. 
A basis of solutions around $\infty$ is given by $x^{-a}F(a,1-c+1;1-b+a;x^{-1})$ and $x^{-b}F(b,1-c+b;1-a+b;x^{-1})$.

### Confluent hypergeometric functions

If some singular points of the differential equation coalesce, in the limiting case we obtain confluent hypergeometric function (special case of which are e.g. [[Bessel functions]]).  

## Examples

The classical orthogonal polynomials appear as special cases for particular choices of parameters, for example Jacobi polynomials and, as their special case, [[Legendre polynomial]]s. 

## Generalizations and related equations

There are other variants like  $q$-hypergeometric functions and the basic hypergeometric series.

[[Heun equation]] is the second order [[Fuchsian differential equation|Fuchsian ODE]] with 4 regular singular points at $0,1,a$ and $\infty$; hypergeometric equation can be transformed into Heun equation by a change of variables. 

There is a recent elliptic version of hypergeometric functions due Spiridonov, [Spiridonov2013](#Spiridonov2013). 

There are now modern generalizations to many variables due Aomoto and another variant due [[Mikhail Kapranov]], [[Israel Gelfand]] and [[Andrei Zelevinsky]]. These multidimensional generalizations express pairings between representations of quantum groups at root of unity and representations of affine Lie algebras, which can be interpreted as "hypergeometric" pairings between certain kind of local homology and cohomology on configuration spaces, see [[hypergeometric construction of KZ solutions]]. This has been extensively studied by [[Alexander Varchenko]], [[Hiroaki Terao]], [[Peter Orlik]], [[Daniel Cohen]] and others; often in connection to the study of (complements of) [[arrangements of hyperplanes]] in $\mathbb{C}^n$. [[Selberg integral|Selberg-type integrals]] are involved. 

## References

* G. E. Andrews, R. Askey, R. Roy, _Special functions_, Enc. of Math. and its Appl. __71__, Cambridge Univ. Press 1999

* G. Gasper, M. Rahman, _Basic hypergeometric series_ (1990) 

* [[Israel Gelfand|I. M. Gelfand]], M. M. [[Kapranov]], [[Andrei Zelevinsky|A. Zelevinsky]], _Discriminants, resultants and multidimensional determinants_, Birkh&#228;user 1994, 523 pp.

*  [[Israel Gelfand|I. M. Gel’fand]], M. I. Graev, [[Vladimir Retakh|V. S. Retakh]], _General hypergeometric systems of equations and series of hypergeometric type_, Russian Math. Surveys __47__(4) (1992) 1--88 [doi](https://doi.org/10.1070/RM1992v047n04ABEH000915), transl. from _Общие гипергеометрические системы уравнений и ряды гипергеометрического типа_, УМН __47__:4(286) (1992) 3--82 [mathnet.ru](http://mi.mathnet.ru/umn4540); _General gamma functions, exponentials, and hypergeometric functions_, Russian Math. Surveys __53__:1 (1998) 1--55 [doi](https://doi.org/10.1070/RM1998v053n01ABEH000008), transl. from _Общие гамма-функции, экспоненты и гипергеометрические функции_, УМН, 1998, __53__:1 (319) 3--60 [doi](https://doi.org/10.4213/rm8)

* [[Ian G. Macdonald]], _Hypergeometric functions I_, 1987 ([arxiv/1309.4568](http://arxiv.org/abs/1309.4568))

* (dedicated chapter 2 of) Katsunori Iwasaki, Hironobu Kimura, Shun Shimomura, Masaaki Yoshida, _From Gauss to Painlevé, A modern theory of special functions_, 184 pp.

Lecture notes motivated by [[partial differential equations]] appearing in [[mathematical physics]]:

* [[Cliff P. Burgess]], §10 in: *Primer on Partial Differential Equations for Physicists*, lecture notes (1990) &lbrack;[pdf](https://physics.mcmaster.ca/~cburgess/Notes/mathphys.pdf), [[Burgess-PDEs.pdf:file]]&rbrack;


In relation to the [[Knizhnik-Zamolodchikov equation]] and [[quantum groups]]:

* [[Alexander Varchenko]], _Multidimensional hypergeometric functions and representation theory of Lie algebras and quantum groups_, Adv. Ser. in Math. Phys. __21__, World Sci. Publ. 1995. x+371 pp. ([doi:10.1142/2467](https://doi.org/10.1142/2467))

* V. Tarasov, [[Alexander Varchenko]], _Geometry of $q$-hypergeometric functions, quantum affine algebras and elliptic quantum groups_, Ast&#233;risque __246__ (1997), vi+135 pp. ([arXiv:q-alg/9703044](https://arxiv.org/abs/q-alg/9703044), [numdam:AST_1997__246__R1_0](http://www.numdam.org/item/AST_1997__246__R1_0))



Online entries/resources on hypergeometric function:

* at Wolframworld: [hypergeometric function](http://mathworld.wolfram.com/HypergeometricFunction.html), [confluent hypergeometric functon of the first kind](http://mathworld.wolfram.com/ConfluentHypergeometricFunctionoftheFirstKind.html), [confluent hypergeometric functon of the second kind](http://mathworld.wolfram.com/ConfluentHypergeometricFunctionoftheSecondKind.html), [generalized hypergeometric function](http://mathworld.wolfram.com/GeneralizedHypergeometricFunction.html), [$q$-hypergeometric function](http://mathworld.wolfram.com/q-HypergeometricFunction.html), [regularized hypergeometric function](http://mathworld.wolfram.com/RegularizedHypergeometricFunction.html)

* wikipedia: [hypergeometric series](http://en.wikipedia.org/wiki/Hypergeometric_series), [confluent hypergeometric function](http://en.wikipedia.org/wiki/Confluent_hypergeometric_function)

* [[Alexander Varchenko]]: [list](http://www.math.unc.edu/Faculty/av/complete.htm) of publications

There is also a far reaching elliptic generalization

* {#Spiridonov2013} V. P. Spiridonov, _Classical elliptic hypergeometric functions and their applications_, [pdf](http://www.math.kobe-u.ac.jp/publications/rlm18/17); _Aspects of elliptic hypergeometric functions_, [arxiv/1307.2876](http://arxiv.org/abs/1307.2876)

[[!redirects hypergeometric functions]]