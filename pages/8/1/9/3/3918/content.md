#Contents#
* tic
{:toc}

#Idea
Pseudodifferential operators generalize [[differential operator]]s and are of similar importance to the theory of [[partial differential equation]]s as [[Schwartz distributions]], see also [[microlocal analysis]].

#Definition
Let $X \subset \mathbb{R}^n$ be open.
A pseudodifferential operator is a [[Fourier integral operator]] of the form

$$
A: C^{\infty}_0 (X) \to \mathcal{D}'(X)
$$

$$
 A u(x) = \frac{1}{(2 \pi)^n} \int \int e^{i (x-y) \theta} a(x,y, \theta) u(y) dy d\theta
$$

If $\mathcal{F}$ denotes the [[Fourier transform]] a short hand notation for this definition is $A u = \mathcal{F}^{-1} (a \, \mathcal{F}u)$, put in words: Fourier transform $u$, multiply with $a$ and transform back.

If $a$ is a polynomial the definition reduces to the application of a differential operator with constant coefficients. The function $a$ is called the **symbol** of the pseudodifferential operator $A$. If one uses the symbol space defined below, then $a$ is assumed to be an element of $S^m_{\rho, \delta}(X \times X \times \mathbb{R}^n)$ 

##Definition of symbols
If one allows arbitrary functions as symbols there will be no control of the behaviour of the associated pseudodifferential operators, of course. In order to get a theory where these operators are, for example, continuous with respect to the standard topologies on the [[topological vector space]]s that they are defined on, some assumptions have to be made. Different levels of generality of the theory correspond to different assumptions about the symbols. One standard symbol space is defined as follows:

Let $X \subset \mathbb{R}^n$ be open, $0 \le \rho \le 1, 0 \le \delta \le 1, m \in \mathbb{R}, n \in \mathbb{N}, n \neq 0$.

* definition: $S^m_{\rho, \delta}$ is the space of all $a \in C^{\infty}(X \times \mathbb{R}^n)$ such that for all compact $K \subset \subset X$ and all $\alpha, \beta \in \mathbb{N}^n$ there is a constant $C_{K, \alpha, \beta}$ such that
$$
        | \partial^{\alpha}_x \, \partial^{\beta}_{\theta} \, a(x, \theta)| \leq C_{K, \alpha, \beta} (1 + | \theta |)^{m - \rho | \beta | + \delta | \alpha |}
$$
The space $S^m_{\rho, \delta}$ is called the space of **symbols of order $m$ and of type $(\rho, \delta)$**.


#References

* Wikipedia on [pseudodifferential operator] (http://en.wikipedia.org/wiki/Pseudo-differential_operator)

An elementary and short introduction can be found here:

* Xavier Saint Raymond: _Elementary Introduction to the Theory of Pseudodifferential Operators_ ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0847.47035&format=complete))

[[!redirects pseudodifferential operators]]