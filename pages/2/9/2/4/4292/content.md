
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

A power series in a [[variable]] $X$ and with [[coefficients]] in a [[ring]] $R$ is a [[series]] 
of the form

$$
  \sum_{n = 0}^\infty a_n X^n
$$

with coefficients $(a_n \in R)_{n = 0}^\infty$. If there are
no additional convergence conditions on a power series 
we call it for emphasis also __formal power series__. 

If there is $k \in \mathbb{N}$ such that $a_n = 0 $ for all $n \gt k$ then this is a [[polynomial]] of degree $k$.

The collection of formal power series in variable $X$ with coefficients in a commutative ring $R$ is denoted $R [ [ X ] ]$. 

More generally, one considers power series $\sum_{n_1=0,n_2=0,\ldots, n_k = 0}^\infty a_{n_1\ldots n_k} X_1^{n_1} X_2^{n_2}\cdots X_k^{n_k}$ in $k$ variables $X_1,\ldots, X_k$ which are declared commutative with $a_{n_1\ldots n_k}\in R$, where $R$ is commutative;
they form a formal power series ring $R [ [ X_1,\ldots, X_k
] ]$. More generally, we can consider noncommutative (associative unital) ring $R$ and words in noncommutative 
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

## Related concepts

* [[convergence radius]]

* [[asymptotic series]]

## References

A formalization in [[homotopy type theory]] and there in [[Coq]] is discussed in section 4 of

* &#193;lvaro Pelayo, [[Vladimir Voevodsky]], [[Michael Warren]], _A preliminary univalent formalization of the p-adic numbers_ ([arXiv:1302.1207](http://arxiv.org/abs/1302.1207))



[[!redirects power series]]
[[!redirects formal power series]]
