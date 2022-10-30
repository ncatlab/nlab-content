Measure spaces are used in the general theory of measure and integration, somewhat analogous to the role played by [[topological spaces]] in the study of continuity.


## Idea ##

For the general theory of measure spaces, we first need a _[[measurable space]]_ $(X, \Sigma)$, that is a [[set]] equipped with a collection $\Sigma$ of __measurable sets__ complete under certain operations.  Then this becomes a measure space $(X, \Sigma, \mu)$ by throwing in a [[function]] $\mu$ from $\Sigma$ to the a space of values (such as the [[real line]]) that gets along with the set-theoretic operations that $\Sigma$ has.  If $E$ is a measurable set, then $\mu(E)$ is called the __measure__ of $E$ with respect to $\mu$.


## Notation ##

The traditional notation for an integral (ultimately going back to [[Gottfried Leibniz]]) was
\[ \label{Leibniz} \int_a^b f(x) \mathrm{d}x \]
(where $f(x)$ might be replaced by some formula in the variable $x$).  In modern measure theory, we can now understand this as the integral of the [[measurable function]] $f$ on the [[interval]] $[a,b]$ relative to [[Lebesgue measure]].  If we wish to generalise from Lebesgue measure to an arbitrary measure $\mu$ and generalise from $[a,b]$ to an arbitrary measurable set $E$, then we can write
\[ \label{full} \int_E f(x) \mu(\mathrm{d}x) \]
instead.  Now, if $f$ is not given by a formula, then there is no need for the dummy variable $x$, which gives
\[ \label{simple} \int_E f \mu .\]
However, it has been more common to keep the symbol '$\mathrm{d}$' and write
\[ \label{excessive} \int_E f \mathrm{d}\mu .\]
(Note that '$\mathrm{d}$' can be read as 'with respect to' in both (eq:Leibniz) and (eq:excessive), although meaning different things; in the former case, it indicates the dummy variable, while in the latter case, it indicates the measure.)  This notation then leads to replacing (eq:full) with
\[ \label{switched} \int_E f(x) \mathrm{d}\mu(x) .\]
This last notation, however, hides the fact that integrating a function with respect to a measure is a way of multiplying a function by a measure to get a new measure; the integral of $f$ on $E$ with respect to $\mu$ is simply the measure of $E$ with respect to $f \mu$, as can be seen in (eq:simple).

See [Usenet discussion](http://groups.google.com/group/sci.math.research/browse_thread/thread/e28593bfd6b83aac/67a61d19e8f4d57f), and contrast (eq:switched) with the [Stieltjes integral](http://secure.wikimedia.org/wikipedia/en/wiki/Stieltjes_integral).  The notation (eq:simple) has also been used in an introductory graduate-level course by [[John Baez]].

There is also some variation in notation as to whether to use a roman '$\mathrm{d}$' or an italic '$\mathit{d}$'; roman is more common in England and italic in America.  But of course, that variation should not cause any difficulties!

+--{.query}
[[Eric]]: $d$ is also the [[exterior derivative]] and $d\mu$ is a volume form. Is there a nice way to say this that is consistent with the above? Update: The Usenet discussion probably discusses this, but I'm too lazy to read the whole thing right now (past my bedtime!).
=--

## Definitions

A (positive) **measure** on a [[measurable space]] $(X, \Sigma)$ is a function to the partially ordered rig $\mathbb{R}_+$ of extended nonnegative reals (in which $0 \cdot \infty = 0$),

$$\mu: \Sigma \to [0, \infty],$$ 

such that 

$$\mu(\bigcup_{i = 1}^{\infty} S_i) = \sum_{i=1}^{\infty} \mu(S_i); \qquad \mu(\emptyset) = 0$$ 

+--{.query}
[[Eric]]: Is there some nice "arrow theoretic" way to state the above? It seems to be screaming to be a functor or an internalization or something.
=--

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


[[!redirects measure spaces]]