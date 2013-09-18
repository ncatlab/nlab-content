
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Laurent series_ generalize [[power series]] by allowing both positive and negative powers. In particular, _Laurent series_ with complex coefficients generalize [[Taylor series]] of analytic functions to meromorphic functions. A Laurent series for a meromorphic function $f(z)$ at finite $z\in\mathbb{C}$ has the form
$$ f(z) = \sum_{n=k}^{\infty}f_n z^n, $$
where $k$ is merely constrained to be finite and is often negative.

## Definition

+-- {: .num_defn} 
###### Definition 
A _Laurent series_ in one variable $z$ over a commutative unital ring $k$ is a [[doubly infinite series]] 
$$ f(z) = \sum_{n=-\infty}^{\infty} f_n z^n ,$$
where $f_n\in k$. Equivalently: a Laurent series is a function $\mathbb{Z} \to k: n \mapsto f_n$. The $k$-module of Laurent series is denoted $k[ [z, z^{-1}] ]$. 
=-- 

A _Laurent polynomial_ is a Laurent series for which all but finitely many $f_n$ are zero. Laurent polynomials form a ring which may be described as $k[z, z^{-1}]$ or abstractly as $k[x, y]/(x y - 1)$. Observe that Laurent series in the generality discussed here do not analogously form a ring: the obvious definition of the coefficients of the product $h(z) = f(z)g(z)$ of two Laurent series $f(z), g(z)$, 

$$h_n = \sum_{k \in \mathbb{Z}} f_k g_{n-k},$$ 

doesn't make sense in general (although it could sometimes make sense in topological contexts where some such infinite sums can converge, as in the case $k = \mathbb{C}$). 

+-- {: .num_remark} 
###### Remark 
The $k$-vector space of Laurent series does however form a module over the ring of Laurent polynomials, i.e., if $f(z) \in k[z, z^{-1}]$ and $g(z)$ is a Laurent series, then the product $h(z) = f(z)g(z)$ as defined above always makes sense. 
=-- 

In general, questions of convergence are treated as separate issues. In complex analysis, the Laurent series $\sum_{n \in \mathbb{Z}} a_n z^n$ describes a meromorphic function in a neighborhood around the point $z = 0$ (possibly with a pole there) if all but finitely many negatively indexed terms are zero. Similarly, series of the form $\sum_{n = -N}^{\infty} a_n (z-a)^n$ describe meromorphic functions in a neighborhood of $z=a$ with poles of order at most $N$. 

On the other hand, in algebra one often hears of the ring of _formal Laurent series_. Here, the presence of the word "ring" signifies that we are restricting the coefficients so that multiplication makes sense. Thus, 

+-- {: .num_defn} 
###### Definition 
The _ring of formal Laurent series_ over a [[commutative ring]] $A$ in an indeterminate $x$ consists of Laurent series $\sum_{n \in \mathbb{Z}} f_n z^n$, with $f_n \in A$ but where all but finitely many $f_n$ for $n \lt 0$ vanish. 
=-- 

Multiplication defined as above clearly makes sense. If $A$ is a field $k$, then this ring is usually denoted $k((x))$ and is in fact a [[field]]; indeed it is the [[field of fractions]] of the ring $k[ [x] ]$ of [[formal power series]], where $k[ [x] ]$ is often viewed as a discrete [[valuation ring]]. 


## Properties

### Dirac distribution 

Of particular interest as a Laurent series is the formal Dirac distribution, 

$$\delta(z) = \sum_{n \in \mathbb{Z}} z^n,$$ 

which intuitively is like the Fourier transform $\sum_{n = -\infty}^\infty e^{i n x}$ of the pointwise multiplicative identity $\mathbf{1}$ given by $\mathbf{1}(n) = 1$ for all $n$. It has the following property: 

* For $f(z)$ a Laurent polynomial, $f(z)\delta(z) = f(1)\delta(z)$. 

Thus, $\delta(z)$ behaves something like the distribution which evaluates at the multiplicative identity $z=1$. More generally, for $a \in k^\ast$ an invertible unit, the series $\delta(a z) = \sum_{n \in \mathbb{Z}} a^n z^z$ satisfies 

* $f(z)\delta(a z) = f(a^{-1})\delta(a z)$. 

Just as it doesn't make sense in general to multiply distributions (at least not without heavy qualifications, as in the theory of [Colombeau](#Col)), we cannot make sense of expressions like $\delta(z)^2$. However, one can meaningfully work with derivatives of distributions, so we have for example 

$$\delta'(z) = \sum_{n \in \mathbb{Z}} n z^n$$ 

which has the property 

* $f(z)\delta'(z) = f(1)\delta'(z) - f'(1)\delta(z)$. 

Indeed, there is a formal calculus of the Dirac distribution that plays an important role in the theory of vertex operator algebras. See for example the treatment in [Frenkel, Lepowsky, Meurman](#FLM). 

One can also work with _convolution products_ $h(z) = (f \ast g)(z)$, defined by multiplying coefficients degree-wise: 

$$h(z) = \sum_{n \in \mathbb{Z}} f_n g_n z^n.$$ 

### Algebraic closure

+-- {: .num_theorem #Puiseux} 
###### Theorem 
If $K$ is [[algebraically closed field|algebraically closed]] and has [[characteristic]] 0, then the [[algebraic closure]] of the field of formal Laurent series $K((x))$ over $K$ is the field of [[Puiseux series]] over $K$.

=-- 

See at _[[Puiseux series]]_ for more details.


## References 

* Igor Frenkel, James Lepowsky, and Arne Meurman, _Vertex Operator Algebras and the Monster_, Volume 134 in Pure and Applied Mathematics, Academic Press 1988. 
{#FLM} 

See also 

* [Doubly Infinite Laurent Series](http://math.rutgers.edu/~sdurst/DILS.html), lectures for formal Laurent series in [[vertex operator algebra]] context 

For discussion of products of distributions, see 

* J.F. Colombeau, _Multiplication of distributions_, Bull. Amer. Math. Soc. (N.S.) Volume 23, Number 2 (1990), 251-268. ([web](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.bams/1183555881)) 
{#Col} 