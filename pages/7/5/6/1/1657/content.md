Measure spaces are used in the general theory of measure and integration, somewhat analogous to the role played by topological spaces in the study of continuity.

## Definitions

A (positive) **measure** on a [[measurable space]] $(X, \Sigma)$ is a function to the partially ordered rig $\mathbb{R}_+$ of extended nonnegative reals (in which $0 \cdot \infty = 0$),

$$\mu: \Sigma \to [0, \infty],$$ 

such that 

$$\mu(\bigcup_{i = 1}^{\infty} S_i) = \sum_{i=1}^{\infty} \mu(S_i); \qquad \mu(\emptyset) = 0$$ 

whenever the $S_i$ are mutually disjoint. A **measure space** consists of a measurable space and a measure on it. A measure space $(X, \Sigma, \mu)$ for which $\mu(X) = 1$ is often called a **probability space** (at least in probabilistic contexts!). 

Each measurable subset $S \subseteq X$ induces a measurable **characteristic function** $\chi_S: X \to \mathbb{R}_+$ where $\chi_S(x) = 1$ if $x \in S$, $\chi_S(x) = 0$ if $x \notin S$. A **simple** measurable function is a finite $\mathbb{R}_+$-linear combination of measurable characteristic functions, and a measure $\mu$ induces an **integral** or **valuation** on simple measurable functions by the rule 

$$\int \sum_{1 \leq i \leq n} a_i \chi_{S_i} d\mu = \sum_{1 \leq i \leq n} a_i \mu(S_i)$$ 

The integral is extended to all measurable functions $f: X \to [0, \infty]$ by the rule 

$$\int f d\mu = \sup \{\int s d\mu: 0 \leq s \leq f, s simple\}$$ 

* Sometimes the notation used is $\int_X f d\mu$. If $S \subseteq X$ is measurable, one may define $\int_S f d\mu$ to be $\int_X \chi_S \cdot f d\mu$. 

A measurable function $f: X \to [0, \infty]$ is **integrable** with respect to $\mu$ if its integral is finite. For measurable functions $f: X \to [-\infty, \infty]$, define $f_+$ and $f_{-}$ by 

$$f_+(x) = \max\{f(x), 0\}, \qquad f_{-}(x) = \max\{-f(x), 0\}$$ 

so that $f = f_+ - f_{-}$, $|f| = f_+ + f_{-}$. We say $f$ is **integrable** if both $f_+$ and $f_{-}$ are integrable, and we put 

$$\int f d\mu = \int f_{+} d\mu - \int f_{-} d\mu$$ 

Finally, a measurable complex-valued function $f: X \to \mathbb{C}$ is integrable if both its real and imaginary parts are; its integral is defined in the obvious way. It is not hard to show that $f$ is integrable if and only if $|f|$ is integrable. Hence a [[pseudonormed vector space|pseudonorm]] is defined on the vector space of complex-valued integrable functions by 

$$\|f\|_1 = \int |f| d\mu$$ 

One has that $\|f\|_1 = 0$ if and only if $f = 0$ **almost everywhere**, meaning that 

$$\mu(\{x: f(x) \neq 0\}) = 0$$ 

The functions which are 0 almost everywhere form a closed linear subspace $Null$ of the pseudonormed space of integrable functions. We say $f = g$ almost everywhere (a.e.) if $f - g \in Null$. The pseudonorm descends to a norm on the quotient space of a.e. equivalence classes of integrable functions, and the resulting normed space is denoted $L^1(X, \Sigma, \mu)$ (sometimes shortened to $L^1(X, \mu)$ or just $L^1(X)$ if the measure is clear). 