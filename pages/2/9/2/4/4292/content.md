
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents

## Definition

A power series in a [[variable]] $X$ and with [[coefficients]] in a [[ring]] $R$ is a [[series]] of the form

$$
  \sum_{n = 0}^\infty a_n X^n
$$

where $a_n$ is in $R$ for each $n\ge 0$. Given that there are no additional convergence conditions, a power series is also termed emphatically as a __formal power series__. If $R$ is commutative, then the collection of formal power series in a variable $X$ with coefficients in $R$ forms a commutative ring denoted by $R [ [ X ] ]$. 

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

### As adic completions

Let $R$ be a [[commutative ring]], and let $R[X]$ be the [[polynomial ring]] on one indeterminant $X$. Then $(X)$ is a [[maximal ideal]] in $R[X]$, and results in an [[adic topology]] on $R[X]$. The ring of formal power series in $R$ is the [[adic completion]] of the [[limit]] of the quotient of $R[X]$ by powers of $(X)$:

$$R[[X]] \coloneqq \underset{\leftarrow}\lim R/(X)^n$$

The ring of formal power series for multiple indeterminants $X_i$ is constructed iteratively: because $R[[X_1, X_2, \ldots X_n]]$ is a commutative ring, one could construct the [[polynomial ring]] $R[[X_1, X_2, \ldots X_n]][X_{n+1}]$ on the indeterminant $X_{n+1}$. As above, $(X_{n+1})$ is a [[maximal ideal]] in $R[[X_1, X_2, \ldots X_n]][X_{n+1}]$ with a corresponding [[adic topology]], and one can then take the [[adic completion]]
$$R[[X_1, X_2, \ldots X_n]][[X_{n+1}]] \coloneqq \underset{\leftarrow}\lim R[[X_1, X_2, \ldots X_n]]/(X_{n+1})^m$$
The resulting commutative ring is usually just written as $R[[X_1, X_2, \ldots X_n, X_{n+1}]]$. 

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

### Formal differentiation

One way to define the formal differentiation operator, as a function $\frac{\partial}{\partial X}:R[[X]] \to R[[X]]$, is via the usual formula 

$$
  \frac{\partial}{\partial X}\left(\sum_{n = 0}^\infty a_n X^n\right) \coloneqq \sum_{n = 0}^\infty a_{n + 1} (n + 1) X^n. 
$$

Then $\frac{\partial}{\partial X}$ is an $R$-[[linear function]] on $R[[X]]$ which satisfies the [[Leibniz rule]], meaning that it is a [[derivation]] and $R[[X]]$ is a [[differential algebra]]. 

Here is a conceptual story underlying the formalism. Let $D = R[\varepsilon]/(\varepsilon^2)$ be the [[representing object]] for [[derivations]] (the "[[ring of dual numbers]]"). Let $\delta: R[ [X] ] \to R[ [X] ] \otimes_R D \cong R[ [X] ][\varepsilon]/(\varepsilon^2)$  be the unique topological $R$-algebra map (under the $(X)$-[[adic topologies]] described above) that sends $X$ to $X + \varepsilon$.  (If it helps, think $\delta(q) = q(X + \varepsilon)$.)  

\begin{definition} 
For $p \in R[ [X] ]$, the *derivative* $p'$ is the unique element of $R[ [X] ]$ satisfying 

$$\delta(p) = p(X) + p'(X)\varepsilon.$$ 
\end{definition} 

We leave as an exercise the proof that the two definitions of derivative match: 

$$p'(X) = \frac{\partial}{\partial X} p(X).$$ 

(Hint: the restriction of $p \mapsto p'$ to $R[X]$ is by construction a derivation such that $X' = 1$, and $(X^k)' = k X^{k-1}$ by [[induction]]. This induces derivations on quotient algebras $R[X]/(X^n)$, satisfying the same formula. Then pass to the inverse limit.) 

\begin{proposition} 
**(Chain rule)** For $p \in R[ [X] ]$ and $q \in x R[ [X ] ]$, 

$$(p \circ q)' = (p' \circ q) \cdot q'.$$ 
\end{proposition} 

See [[chain rule#FormalAlgebra|here]] for a conceptual proof, using the universal property of adic completion. 

Relatedly but in a slightly different direction, we can consider differentiation in coalgebraic terms. Suppose the commutative ring $R$ is a [[commutative algebra]] over $\mathbb{Q}$ (thus permitting division by nonzero [[integers]]). Then the set $R[ [X]]$ may be identified with the [[terminal coalgebra of an endofunctor|terminal coalgebra]] $R^\mathbb{N}$ of the [[endofunctor]] $R \times - \colon Set \to Set$ via the map  

$$R[ [X]] \to R^\mathbb{N}\; : \; \sum_{n \geq 0} \frac{a_n X^n}{n!} \mapsto (a_0, a_1, a_2, \ldots)$$ 

whereby the coalgebra structure on $R^\mathbb{N}$, 

$$R^\mathbb{N} \to R \times R^\mathbb{N}\; \colon \; (a_n)_{n \geq 0} \mapsto \langle a_0, (a_{n+1})_{n \geq 0} \rangle,$$ 

corresponds to 

$$R[ [X]] \to R \times R[ [X]]\; \colon\; f(X) \mapsto \langle f(0), f'(X) \rangle.$$ 

One may then apply [[coinduction|coinductive]] techniques to prove various facts. One illustration is given [[coinduction#Examples|here]], where coinduction on power series is used to prove the general binomial theorem 

$$(1 + x)^r \coloneqq \exp(r \log(1 + x)) = \sum_{k \geq 0} \frac{r^\underline{k} x^k}{k!}$$ 

where, remarkably, $r$ is an arbitrary element of $R$. 



## Ring of power series as rings with infinitesimals

| [[ring]] with [[infinitesimals]] | [[function]] | 
---------------------|-----------------|
| [[dual numbers]] | [[differentiable function]] |
| [[Weil ring]] | [[smooth function]] |
| [[power series ring]] | [[analytic function]] |

### Purely real and purely infinitesimal elements

Suppose that $K$ is a [[Archimedean ordered field]] and $K[[\epsilon]]$ is the ring of power series in $K$. Since $K[[\epsilon]]$ is a [[local ring]], the quotient of $K[[\epsilon]]$ by its ideal of non-invertible elements $\epsilon K[[\epsilon]]$ is the [[residue field]] $K$ itself, and the canonical function used in defining the quotient is the function $\Re:K[[\epsilon]] \to K$ which takes a number $a \in K[[\epsilon]]$ to its purely real component $\Re(a) \in K$ and takes $\Re(\epsilon) = 0$. Since $K[[\epsilon]]$ is an ordered $K$-algebra, there is a [[strictly monotone]] [[ring homomorphism]] $h:K \to K[[\epsilon]]$. An element $a \in K[[\epsilon]]$ is **purely real** if $h(\Re(a)) = a$, and an element $a \in K[[\epsilon]]$ is **purely [[infinitesimal]]** if it is in the [[fiber]] of $\Re$ at $0 \in K$. Zero is the only element in $K[[\epsilon]]$ which is both purely real and purely infinitesimal. 

### Analytic functions

Suppose that $K$ is a [[sequentially Cauchy complete]] [[Archimedean ordered field]] with lattice structure, and $K[[\epsilon]]$ is the ring of power series of $K$. Then [[analytic functions]] are each definable on $K$ using the algebraic, order, metric, and convergence structure on $K$. 

The ring homomorphism $h:K \to K[[\epsilon]]$ preserves [[analytic functions]]: given a natural number $n \in \mathbb{N}$ and a purely infinitesimal element $\eta \in \epsilon K[[\epsilon]]$, then for every [[analytic function]] $f \in C^\infty(K)$, there is a function $f_{K[[\epsilon]]}:K[[\epsilon]] \to K[[\epsilon]]$ such that for all elements $x \in K$, $f_{K[[\epsilon]]}(h(x)) = h(f(x))$ and 
$$f_{K[[\epsilon]]}(h(x) + \eta) = \sum_{i = 0}^{\infty} \frac{1}{i!} h\left(\frac{d^i f}{d x^i}(x)\right) \eta^i$$ 

## Related concepts

* [[convergence radius]]

* [[asymptotic series]], [[transseries]]

* [[Tate algebra]]

* [[characteristic series]]

* [power series and their formal spectra](formal+scheme#FormalPowerSeries)

## References

* Wikipedia, _[Formal power series](https://en.wikipedia.org/wiki/Formal_power_series)_

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

[[!redirects power series algebra]]
[[!redirects power series algebras]]

