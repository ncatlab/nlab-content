
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

* An element $a = a_0 + a_1 x + a_2 x^2 + \ldots$ in $R[ [x] ]$ is (multiplicatively) invertible iff $a_0$ is invertible. 

This follows easily from the observation that we can invert $1 + x b$ for any power series $b$ by forming $1 - x b + x^2 b^2 - \ldots$ and collecting only finitely many terms in each degree. As a simple corollary, 

* If $R$ is a [[local ring]], then the power series ring $R[ [X] ]$ is also a local ring. 

### Functional substitution and inversion 

+-- {: .num_prop} 
###### Proposition 
$R[ [x_1, \ldots, x_n] ]$ equipped with the ideal $(x_1, \ldots, x_n)$ is the free [[formal group law|adic]] $R$-algebra on $n$ generators, in the sense that it is the value of the left adjoint $Pow$ to the forgetful functor 

$$Ideal: AdicRAlg \to Set: (A, I) \mapsto I$$ 

as applied to the set $\{x_1, \ldots, x_n\}$. 
=-- 

+-- {: .proof} 
###### Proof 
The idea is that for each adic $R$-algebra $(S, I)$ and element $(s_1, \ldots s_n) \in I^n$, there is a unique adic algebra map $R[ [x_1, \ldots, x_n] ] \to S$ that sends $x_i$ to $s_i$; this adic algebra map sends a power series $\sum a_{k_1, \ldots, k_n} x_1^{k_1} x_n^{k_n}$ to the sequence of truncations 

$$\left(\sum_{k_1 + \ldots + k_n \lt k} a_{k_1, \ldots, k_n} s_1^{k_1} \ldots s_n^{k_n} \mod I^k\right)_k$$ 

belonging to $\underset{\longleftarrow}{\lim}_k S/I^k \cong S$. 
=-- 

It follows that we may define a clone or cartesian operad as follows: the $n^{th}$ component is the set $I_n = (x_1, \ldots, x_n) \subset R[ [x_1, \ldots, x_n] ]$ which is the monad value $Ideal Pow(\{x_1, \ldots, x_n\})$. Letting $M$ denote the monad $Ideal \circ Pow$, with monad multiplication $\mu$, and $[n]$ the set $\{x_1, \ldots, x_n\}$, the clone multiplication 

$$I_n \times I_k^n \to I_k$$ 

is the composition of the maps 

$$M(n) \times M(k)^n \cong M(n) \times \hom([n], M(k)) \stackrel{1 \times func}{\to} M(n) \times \hom(M(n), M M(k)) \stackrel{eval}{\to} M M(k) \stackrel{\mu(k)}{\to} M(k)$$ 

The clone multiplication thus defined is called *substitution of power series*; it takes a tuple consisting of $p(x_1, \ldots, x_n) \in I_n, q_1(x_1, \ldots x_k) \in I_k, \ldots q_n(x_1, \ldots, x_k) \in I_k)$ to a power series denoted as 

$$p(q_1(x_1, \ldots, x_k), \ldots q_n(x_1, \ldots, x_k)).$$ 

The resulting clone or operad yields, in the particular case $k = n = 1$, an associative substitution operation 

$$x R[ [x] ] \times x R[ [x] ] \stackrel{sub}{\to} x R[ [x] ]$$ 

with $sub(p, q) = p \circ q$ the power series $p(q(x))$. 

+-- {: .num_prop #InvertibleElements} 
###### Proposition 
The group of invertible elements in the substitution monoid $x R[ [x] ]$ consists of power series of the form $a_1 x + a_2 x^2 + \ldots$ where $a_1$ is multiplicatively invertible in the ring $R$. 
=-- 

In other words, we can functionally invert a power series provided that the linear coefficient $a_1$ is invertible in $R$. 

+-- {: .proof} 
###### Proof 
Given power series $a = a_1 x + a_2 x^2 + \ldots$ and $b = b_1 x + b_2 x^2 + \ldots$, we may read off coefficients of the composite $a \circ b$ as 

$$(a \circ b)_k = \sum_{n \geq 1} a_n \sum_{k = k_1 + \ldots + k_n} b_{k_1} b_{k_2} \ldots b_{k_n}$$ 

where in particular $(a \circ b)_1 = a_1 b_1$. Now $a$ is the left functional inverse of $b$, or $b$ is the right inverse of $a$, if $(a \circ b)(x) = x$, i.e., if $(a \circ b)_k = 1$ if $k = 1$ and $0$ otherwise. The first equation says simply $(a \circ b)_1 = a_1 b_1 = 1$ which implies $a_1$ is invertible. Conversely, if $a_1$ is multiplicatively invertible and $b_1 = a_1^{-1}$, then the equations 

$$\array{
\sum_{n \geq 1} a_n \sum_{k = k_1 + \ldots + k_n} b_{k_1} b_{k_2} \ldots b_{k_n} & = 1\; if\; k = 1 \\ 
 & = 0\; if\; k \neq 1
}$$ 

may be uniquely solved for the remaining $a_i$\'s given the $b_j$\'s, and uniquely solved for the remaining $b_j$\'s given the $a_i$\'s, by an inductive procedure: for $k \neq 1$ we have 

$$a_1 b_k + a_k b_1^k + \; terms\; a_n b_{k_1} \ldots b_{k_n} = 0$$ 

and this allows us to solve for $b_k$, 

$$b_k = -a_1^{-1}(a_k b_1^k + \; terms\; a_n b_{k_1} \ldots b_{k_n})$$ 

given the values $a_1, \ldots, a_k$ and earlier $b$-values $b_{k_j}$ for $k_j \lt k$ given by inductive hypothesis. Similarly we can solve for $a_k$ in terms of given coefficients $b_1, \ldots, b_k$ and earlier $a$-values $a_n$, $n \lt k$. Thus every power series $a$ has a right inverse if $a_1^{-1}$ exists, and $b$ has a left inverse if $b_1^{-1}$ exists, and this completes the proof. 
=-- 


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

* Tim Gowers's blog: [differentiating-power-series](https://gowers.wordpress.com/2014/02/22/differentiating-power-series)


category: analysis, algebra

[[!redirects power series]]
[[!redirects formal power series]]


[[!redirects power series ring]]
[[!redirects power series rings]]

[[!redirects formal power series ring]]
[[!redirects formal power series rings]]

[[!redirects formal power series algebra]]
[[!redirects formal power series algebras]]

