

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Pseudodifferential operators generalize [[differential operators]] and are of similar importance to the theory of [[partial differential equations]] as [[Schwartz distributions]], see also [[microlocal analysis]].

## Definition

Let $X \subset \mathbb{R}^n$ be open.
A pseudodifferential operator is a [[Fourier integral operator]] of the form

$$
A: C^{\infty}_0 (X) \to \mathcal{D}'(X)
$$

$$
 A u(x) = \frac{1}{(2 \pi)^n} \int \int e^{i (x-y) \theta} a(x, y, \theta) u(y) dy d\theta
$$

where the function $a$, called the **symbol** of the pseudodifferential operator $A$, belongs to the space $S^m_{\rho, \delta}(X \times X \times \mathbb{R}^n)$ defined below.

If $\mathcal{F}$ denotes the [[Fourier transform]] a short hand notation for this definition is $A u = \mathcal{F}^{-1} (a \, \mathcal{F}u)$, put in words: Fourier transform $u$, multiply with $a$ and transform back.

## Definition of symbols

If one allows arbitrary functions as symbols there will be no control of the behaviour of the associated pseudodifferential operators, of course. In order to get a theory where these operators are, for example, continuous with respect to the standard topologies on the [[topological vector space]]s that they are defined on, some assumptions have to be made. Different levels of generality of the theory correspond to different assumptions about the symbols. One standard symbol space is defined as follows:

Let $X \subset \mathbb{R}^n$ be open, $0 \le \rho \le 1, 0 \le \delta \le 1, m \in \mathbb{R}, n \in \mathbb{N}, n \neq 0$.

* definition: $S^m_{\rho, \delta}$ is the space of all $a \in C^{\infty}(X \times \mathbb{R}^n)$ such that for all compact $K \Subset X$ and all $\alpha, \beta \in \mathbb{N}^n$ there is a constant $C_{K, \alpha, \beta}$ such that
$$
        | \partial^{\alpha}_x \, \partial^{\beta}_{\theta} \, a(x, \theta)| \leq C_{K, \alpha, \beta} (1 + | \theta |)^{m - \rho | \beta | + \delta | \alpha |}
$$
The space $S^m_{\rho, \delta}$ is called the space of **symbols of order $m$ and of type $(\rho, \delta)$**.

It is easy to see that every space $S^m_{\rho, \delta}$ is a Fr&#233;chet space: every $X \subset \mathbb{R}^n$ open has a compact exhaustion, that is an increasing sequence $(K_i)$ with each $K_i \Subset X$ compact such that $\bigcup_{i = 1}^{\infty} K_i = X$, and one can define a countable family of seminorms via

$$
P_{K_i, \alpha, \beta} = \operatorname{sup}_{(x, \theta) \in K_i \times \mathbb{R}^n} \frac{ | \partial^{\alpha}_x \, \partial^{\beta}_{\theta} \, a(x, \theta)|}{(1 + | \theta |)^{m - \rho | \beta | + \delta | \alpha |}}
$$

The space of symbols of order $- \infty$ is defined to be
$$
    S^{- \infty} = \bigcap_{m \in \mathbb{R}} S^m_{\rho, \delta}
$$

Conversly the symbols of order $\infty$ are defined by

$$
    S^{\infty} = \bigcup_{m \in \mathbb{R}} S^m_{\rho, \delta}
$$

Symbols of order $- \infty$ are often called **smoothing** and their operators **smoothing operators**. The reason for this is that their pseudodifferential operators map distribution spaces into spaces of smooth functions, for example:

## Examples

### Every differential operator is a pseudodifferential operator

We restrict ourselfes to one dimension for simplicity, let $D := -i \frac{d}{dx}$ and write a differential operator $P$ as
$$
  P(x, D) := \sum_{k = 0}^n f_n(x) D^k
$$ 
with given functions $f_n$. Then $P$ is a pseudodifferential operator with symbol $a(x, y, \theta) = P(x, \theta)$. The symbol of a differential operator therefore is a polynom in $\theta$, which motivates a part of the definition of symbol classes below: We expect that the growth of the symbol in $\theta$ is polynomial at most, and the degree of the bounding polynomial decreases by $1$ if we apply differentiation in $\theta$ to the symbol.


## Properties

### Smoothing theorem

The pseudodifferential operator of a smoothing symbol maps $\mathcal{E}'$, the [[dual vector space|dual space]] of $C^{\infty}$, into $\mathcal{S}$, the Schwartz space of rapidly decreasing smooth functions.


### Propagation of singularities theorem

* [[propagation of singularities theorem]]


## References

* Wikipedia on [pseudodifferential operator] (http://en.wikipedia.org/wiki/Pseudo-differential_operator)

An elementary and short introduction can be found here:

* Xavier Saint Raymond: _Elementary Introduction to the Theory of Pseudodifferential Operators_ ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0847.47035&format=complete))
* Sylvain Carpentier, Alberto De Sole, [[Victor G. Kac]], _Some algebraic properties of differential operators_, [arxiv/1201.1992](http://arxiv.org/abs/1201.1992)
* [[Lars Hörmander]], _The analysis of linear partial differential operators_, in 4 vols.: I. Distribution theory and Fourier analysis, II. Differential operators with constant coefficients, III. Pseudo-differential operators, IV. Fourier integral operators.

[[!redirects pseudodifferential operators]]

[[!redirects pseudo-differential operator]]
[[!redirects pseudo-differential operators]]
