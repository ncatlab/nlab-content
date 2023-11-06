
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

_Laurent series_ generalize [[power series]] by allowing both positive and negative powers. In particular, _Laurent series_ with complex coefficients generalize [[Taylor series]] of analytic functions to [[meromorphic functions]]. A Laurent series for a meromorphic function $f(z)$ at finite $z\in\mathbb{C}$ has the form
$$ f(z) = \sum_{n=k}^{\infty}f_n z^n, $$
where $k$ is merely constrained to be finite and is often negative. 

Or, in some contexts one wants to take $k = -\infty$. Here such a formal sum (with powers extending infinitely in both directions) is suggestive notation for an element belonging to the dual $\prod_{n \in \mathbb{Z}} R \cdot z^n$ 
of a ring $\oplus_{n \in \mathbb{Z}} R \cdot z^n$ (see Laurent polynomials below). In such contexts, Laurent series can be likened to distributions, i.e., functionals on the algebra of functions $\mathbb{Z} \to R$ with compact support. 

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

+-- {: .num_defn #ring} 
###### Definition 
The _ring of formal Laurent series_ over a [[commutative ring]] $A$ in an indeterminate $x$ consists of Laurent series $\sum_{n \in \mathbb{Z}} f_n z^n$, with $f_n \in A$ but where all but finitely many $f_n$ for $n \lt 0$ vanish. 
=-- 

Multiplication defined as above clearly makes sense. If $A$ is a field $k$, then this ring is usually denoted $k((x))$ and is in fact a [[field]]; indeed it is the [[field of fractions]] of the ring $k[ [x] ]$ of [[formal power series]], where $k[ [x] ]$ is often viewed as a discrete [[valuation ring]]. 

+-- {: .num_remark #restrict} 
###### Remark 
It would perhaps be clearer if we used the term "restricted Laurent series" to cover the Laurent series considered in Definition \ref{ring}, and let "Laurent series" be the term that covers doubly infinite series. 
=-- 

## Properties

### Laurent series as distributions 

Another point of view on Laurent series is given in the following alternative definition. 

+-- {: .num_defn} 
###### Definition 
A Laurent series over $k$ is a $k$-linear functional 

$$\phi: k[z, z^{-1}] \to k$$ 

on the algebra of Laurent polynomials. 
=-- 

The associated series is $\sum_{n \in \mathbb{Z}} \phi(z^n)z^n$. But here we emphasize the point of view that Laurent series have a distribution-like character, with Laurent polynomials being considered a space of functions $\mathbb{Z} \to k$ with compact (finite) support, via the evident inclusion 

$$k[z, z^{-1}] \cong \oplus_{n \in \mathbb{Z}} k \cdot z^n \hookrightarrow \prod_{n \in \mathbb{Z}} k \cdot z^n = k^{\mathbb{Z}}.$$ 

Of particular interest as a Laurent series is the formal Dirac distribution, 

$$\delta(z) = \sum_{n \in \mathbb{Z}} z^n,$$ 

which intuitively is like the Fourier transform $\sum_{n = -\infty}^\infty e^{i n x}$ of the pointwise multiplicative identity $\mathbf{1}$ given by $\mathbf{1}(n) = 1$ for all $n$. It has the following property: 

* For $f(z)$ a Laurent polynomial, $f(z)\delta(z) = f(1)\delta(z)$. 

Indeed, notice that $\delta(z)$ is the distribution $p \mapsto p(1)$ which evaluates a Laurent polynomial at the multiplicative identity $z=1$. 

More generally, for $a \in k^\ast$ an invertible unit, the series $\delta(a z) = \sum_{n \in \mathbb{Z}} a^n z^z$ satisfies 

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
If $K$ is [[algebraically closed field|algebraically closed]] and has [[characteristic]] 0, then the [[algebraic closure]] of the field of (restricted) Laurent series $K((x))$ over $K$ is the field of [[Puiseux series]] over $K$.

=-- 

Here "restricted" refers to Remark \ref{restrict}. See _[[Puiseux series]]_ for more details on this result.

### Function field analogy

[[!include function field analogy -- table]]


## References 

* Igor Frenkel, James Lepowsky, and Arne Meurman, _Vertex Operator Algebras and the Monster_, Volume 134 in Pure and Applied Mathematics, Academic Press 1988. 
{#FLM} 
* [Doubly Infinite Laurent Series](http://math.rutgers.edu/~sdurst/DILS.html), lectures for formal Laurent series in [[vertex operator algebra]] context 
* Alexander Zheglov, _Wild division algebras over Laurent series fields_, [math.NT/0503637](http://arxiv.org/abs/math/0503637)

For discussion of products of distributions, see 

* J.F. Colombeau, _Multiplication of distributions_, Bull. Amer. Math. Soc. (N.S.) Volume 23, Number 2 (1990), 251-268. ([web](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.bams/1183555881)) 
{#Col} 