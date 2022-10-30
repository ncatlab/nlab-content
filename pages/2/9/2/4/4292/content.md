
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

A power series in a [[variable]] $X$ and with [[coefficients]] in a [[ring]] $R$ is a [[series]] of the form

$$
  \sum_{n = 0}^\infty a_n X^n
$$

where $a_n$ is in $R$ for each $n\ge 0$. Given that there are
no additional convergence conditions, a power series is also termed emphatically as a __formal power series__. If $R$ is commutative, then the collection of formal power series in a variable $X$ with coefficients in $R$ forms a commutative ring denoted by $R [ [ X ] ]$. 

More generally, a power series in $k$ commuting variables $X_1,\ldots, X_k$ with coefficients in a ring $R$ has the form $\sum_{n_1=0,n_2=0,\ldots, n_k = 0}^\infty a_{n_1\ldots n_k} X_1^{n_1} X_2^{n_2}\cdots X_k^{n_k}$. If $R$ is commutative, then the collection of formal power series in $k$ commuting variables $X_1,\ldots, X_k$ form a formal power series ring denoted by $R [ [ X_1,\ldots, X_k
] ]$. 

More generally, we can consider noncommutative (associative unital) ring $R$ and words in noncommutative 
variables $X_1,\ldots, X_k$ of the form
$$
w = X_{i_1}\cdots X_{i_m}
$$
(where $m$ has nothing to do with $k$) and with coefficient $a_w \in R$ (here $w$ is a word of any length, not a multiindex in the previous sense). Thus the power sum is of the form $\sum_w a_w X_w$ and they form a formal power series ring in variables $X_1,\ldots, X_k$ denoted by $R\langle \langle X_1,\ldots, X_k \rangle\rangle$. Furthermore, $R$ can be even a noncommutative [[semiring]] in which case the words belong to the free monoid on the set $S = \{ X_1,\ldots, X_k\}$, the partial sums are then belong to a monoid semiring $R\langle S\rangle$. The formal power series then also form a semiring, by the multiplication rule
$$
\sum_{r} a_r X_r \cdot \sum b_s X_s = \sum_w \sum_{u,v; w = u v} a_u b_v X_w
$$
Of course, this implies that in a specialization, $b$-s commute with variables $X_{i_k}$; what is usually generalized to take some endomorphisms into an account (like at noncommutative polynomial level of partial sums where we get skew-polynomial rings, i.e. iterated Ore extensions).

## Examples

### Polynomials

For a natural number $k$, a power series $\sum_{n=0}^\infty a_n X^n$ such that $a_n = 0$ for all $n \gt k$ is a [[polynomial]] of degree at most $k$.

### Taylor series

* [[Taylor series]]

### MacLaurin series

For $f \in C^\infty(\mathbb{R})$ a [[smooth function]] on the [[real line]], and for $f^{(n)} \in C^\infty(\mathbb{R})$ denoting its $n$th [[derivative]] its [[MacLaurin series]] (its [[Taylor series]] at $0$) is the power series

$$
  \sum_{n = 0}^\infty  
   \frac{1}{n!} f^{(n)}(0) x^n
  \,.
$$

If this power series [[convergence|converges]] to $f$, then we say that $f$ is _[[analytic function|analytic]]_.

### Laurent series

* [[Laurent series]]

### Puiseux series
  
* [[Puiseux series]]

## Properties

* If $R$ is a [[local ring]], then the power series ring $R[ [X] ]$ is also a local ring.

## Related concepts

* [[convergence radius]]

* [[asymptotic series]], [[transseries]]

* [[Tate algebra]]

* [[characteristic series]]

* [power series and their formal spectra](formal+scheme#FormalPowerSeries)

## References

* Wikipedia, _[Formal power series](en.wikipedia.org/wiki/Formal_power_series)_

A formalization in [[homotopy type theory]] and there in [[Coq]] is discussed in section 4 of

* &#193;lvaro Pelayo, [[Vladimir Voevodsky]], [[Michael Warren]], _A preliminary univalent formalization of the p-adic numbers_ ([arXiv:1302.1207](http://arxiv.org/abs/1302.1207))

The discussion of the differentiation of a converging power series term by term is at

* Tom Gower's blog: [differentiating-power-series](https://gowers.wordpress.com/2014/02/22/differentiating-power-series)


category: analysis, algebra

[[!redirects power series]]
[[!redirects formal power series]]


[[!redirects power series ring]]
[[!redirects power series rings]]

[[!redirects formal power series ring]]
[[!redirects formal power series rings]]

[[!redirects formal power series algebra]]
[[!redirects formal power series algebras]]

