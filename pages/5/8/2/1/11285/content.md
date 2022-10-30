
# Taylor\'s Theorem
* table of contents
{: toc}

## Idea

The [[Taylor polynomial]]s of a [[differentiable function]] approximate it by [[polynomial]] functions; the various versions of Taylor's Theorem describe how good this approximation is.  The limiting case of this is the [[Taylor series]].


## Preliminary definitions

Let $f$ be a [[partial function]] on a [[cartesian space]] $\mathbb{R}^d$ (or $\mathbb{C}^d$), let $c$ be a [[concrete point|point]] in the cartesian space, and let $k$ be a [[natural number]] (actually we can allow $k \geq -1$ also, using [[negative thinking]]).

+-- {: .num_defn}
###### Definition

If  $f$ is [[differentiable function|differentiable]] $k$ times at $c$, then the __[[Taylor polynomial]]__ of $f$ at $c$ with order $k$ is the unique [[polynomial]] in $d$ variables of degree at most $k$ whose derivatives at $c$ match those of $f$ up to order $k$.
=--

It is straightforward (by differentiating a polynomial [[ansatz]]) to find an explicit formula (in the variable $x$):
$$ T^k_{f@c}(x) = \sum_{n = 0}^k \frac{f^{(n)}(c) (x-c)^n}{n!} .$$
We have written this as if $f$ is a function of one variable; but interpret $n$ as a [[multi-index]] whose length $\ell$ satisfies $0 \leq \ell \leq k$, with $f^{(n)}$ the mixed [[partial derivative]] given by that multi-index, $n!$ the [[factorial]] of $\ell$, and $(x-c)^n$ a product of $\ell$ factors of the form $x_i - c_i$ (where $i$ is an index appearing in the multi-index $n$).  Then this works in any cartesian space.  (Note that we include all possible orderings of a multi-index as separate terms; this leads to repeated terms that, when combined, will cancel some of the factors in the factorial.)

In the case of a function of several variables, we can also manage the maximum degrees in the various variables separately, although nobody seems to bother with this.


## Statements

There are several different versions of Taylor\'s Theorem, all stating an extent to which a Taylor polynomial of $f$ at $c$, when evaluated at $x$, approximates $f(x)$.

Here is the simplest statement, which requires only continuity of $f$ (which we really only need for $k = 0$, since it\'s automatic for $k \geq 1$ and not actually necessary for $k = -1$):
+-- {: .num_theorem #limit}
###### Theorem

If $f$ is [[continuous function|continuous]] at $c$, then
$$ \lim_{x \to c} \frac{{f(x) - T^k_{f@c}(x)}}{{\|x - c\|}^k} = 0 .$$
=--
(The norm ${\|\cdot\|}$ can be left out in one variable, or placed in the numerator to handle all components of a vector-valued function at once.)

If $f^{(k)}$ has some continuity, then we get a version of Taylor\'s Theorem with an integral:
+-- {: .num_theorem #integral}
###### Theorem

If $f^{(k)}$ is [[absolutely continuous function|absolutely continuous]], then
$$ f(x) = T^k_{f@c}(x) + \int_{t=a}^x \frac{f^{(k+1)}(t) (x-t)^{k+1} \,\mathrm{d}t}{(k + 1)!} .$$
=--
(Note that $f^{(k+1)}$ is [[almost function|defined almost everywhere]] and [[Lebesgue integrable function|Lebesgue integrable]], because $f^{(k)}$ is absolutely continuous.)


[[!redirects Taylor's theorem]]
[[!redirects Taylor's theorems]]
[[!redirects Taylor's theorem]]
[[!redirects Taylor's theorems]]
[[!redirects Taylor\'s theorem]]
[[!redirects Taylor\'s theorems]]

[[!redirects Taylor polynomial]]
[[!redirects Taylor polynomials]]
