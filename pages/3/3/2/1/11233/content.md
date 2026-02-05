
# The Henstock integral
* table of contents
{: toc}

## Idea

The *Henstock integral* (also attributed to *Kurzweil*, *Denjoy*, *Luzin*, and *Perron*, and sometimes called, neutrally but perhaps ambiguously, the *gauge integral*) is a way to define the [[integral]] of a (partial) function $f:\mathbb{R}\to \mathbb{R}$ which applies to more functions than either the [[Riemann integral]] or the [[Lebesgue integral]] and is in some ways better behaved as well.

However, the Lebesgue integral is more commonly used by working mathematicians because it fits more naturally into the general theory of [[measure]], while the Riemann/Darboux integral is more commonly used in introductory calculus courses because its definition is simpler.


## Definition

Let $[a,b]$ be a closed [[interval]] in $\mathbb{R}$ and let $f:[a,b]\to \mathbb{R}$.  A *tagged partition* $P$ of $[a,b]$ is a finite sequence of points $a = u_0 \leq u_1 \leq \dots \leq u_n = b$ together with points $t_i \in [u_i, u_{i+1}]$ for all $i$.  The *Riemann sum* of $f$ over such a tagged partition is 

$$ \sum_P f = \sum_{i=0}^{n-1} f(t_i) \cdot (u_{i+1} - u_{i}). $$

Define a *gauge* on $[a,b]$ to be any function $\delta: [a,b] \to (0,\infty]$.  We say that a tagged partition is *$\delta$-fine* if $[u_i, u_{i+1}] \subset [t_i - \delta(t_i), t_i + \delta(t_i)]$.

Finally, we say that $I$ is the **integral** of $f$ on $[a,b]$, written $I = \int_a^b f = \int_{a}^b f(x) \,d x$, if for any $\epsilon\gt 0$ there exists a gauge $\delta$ such that

$$ {\left| {\sum_P f - I} \right|} \lt \epsilon $$

for any $\delta$-fine partition $P$.  If such an $I$ exists, it must be unique, and we say that $f$ is (Henstock) **integrable** on $[a,b]$.

We can also write $\int_a f(x) \,d x$ for the [[semidefinite integral|semidefinite]] Henstock integral $\int_a^x f(t) \,d t$, and write $\int_a f$ for the function $x \mapsto \int_a f(x) \,d x$.


### Comparison to the Riemann definition

If we require a gauge to be a [[constant function]], then we recover the definition of the [[Riemann integral]].

Thus the Henstock integral may be seen as a non-uniform generalization of the Riemann integral.  Whereas specifying a constant $\delta$ is tantamount to picking an [[entourage]] on $[a,b]$, specifying a gauge $\delta$ is tantamount to assigning a [[neighbourhood]] to each point in $[a,b]$.  (Indeed, with either definition of integral, it would be equivalent to replace $\delta$ in the definition with an entourage or an assignment of neighbourhoods.)  Similarly, the definition of [[uniformly continuous function]] becomes that of [[continuous function]] if you change $\delta$ from a constant to a gauge.


### Constructive version

In [[constructive analysis]], we must allow a gauge to take [[lower real number|lower real]] values.  (This is not necessary with the Riemann integral.)  Otherwise, there may not be enough gauges, since these are rarely continuous.  (The definition could also be made constructive by explicitly referring to an assignment of neighbourhoods to points or by replacing $\delta$ with an [[entire relation]].)


### Cousin\'s Lemma

Conceivably, there might exist an interval $[a,b]$ and a gauge $\delta$ such that no $\delta$-fine partition of $[a,b]$ exists at all; in that case, the integral of any function $f$ on $[a,b]$ would vacuously take every value $I$.  This is ruled out by [[Cousin's Lemma]], which states precisely that such a partition always exists.  This lemma can be leveraged to prove that the integral is not only nontrivial but also (if it exists at all) unique.  (Proof sketch: prove that if $I$ is an integral of $f$ on $[a, b]$ and $J$ is an integral of $g$ on $[a, b]$, then $I - J$ is an integral of $f - g$ on $[a, b]$, which can be done in the usual way without assuming uniqueness; use Cousin\'s Lemma to prove that any integral of $0$ on $[a, b]$ must be $0$; conclude that if $I$ and $J$ are both integrals of $f$ on $[a, b]$, then $I - J = 0$.)


## Examples

The [[characteristic function]] $\chi_{\mathbb{Q}}$ of the [[rational numbers]] (as a subset of the real numbers) is a famous example of a function that's Lebesgue integrable but not even locally Riemann integrable.  It is Henstock integrable (with integral $0$) on any $[a,b]$ as follows:  Enumerate the rationals in $[a,b]$ as $(q_i)_{i=0}^\infty$.  Given $\epsilon \gt 0$, let $\delta(x)$ be $b-a$ if $x$ is irrational but $2^{-i-2}\epsilon(b-a)$ if $x$ is the rational $q_i$.  Then $\sum_{x\in[a,b]} \chi_{\mathbb{Q}}(x) \,2\delta(x) = \epsilon$.  Since a $\delta$-fine Riemann sum consists of just some of these terms, with $2\delta(x)$ replaced by a length that might be smaller, the value of the $\delta$-fine Riemann sum is thus always at most $\epsilon$.

The (even) function
$$
x\mapsto \frac{\sin(1/x^3)}{x},\quad x \in \mathbb{R}\setminus\{0\}
$$
is not Riemann or Lebesgue integrable on any interval containing 0, but it has the Henstock integral
$$
\int_{0} \frac{\sin (1/x^3)}{x}\,d x = \frac{1}{3}\left( \pi/2 - Si(1/x^3)\right)
$$
where $Si(t)$ is the [[sine integral]] $\int_0 \frac{\sin(t)}{t}d t $ (which extends to an [[entire function]] on $\mathbb{C}$).  This integral can also be found as an [[improper integral|improper]] Riemann integral.

For an example that is neither Lebesgue integrable nor improperly Riemann integrable (not even locally Riemann integrable), we can let $f(x)$ be $\sin(1/x^3)/x$ for irrational $x$ and $1$ for rational $x$.  This one can still be done as an improper Lebesgue integral.  (Are there any functions that are Henstock integrable but not locally Lebesgue integrable?)


## Properties

### The fundamental theorem of calculus

The Henstock integral satisfies a very nice form of the [[fundamental theorem of calculus]]:

+-- {: .un_theorem}
###### Theorem
If $f$ is differentiable on $[a,b]$, then $f'$ is Henstock integrable on $[a,b]$, and $\int_a^b f'(x) d x = f(b) - f(a)$.
=--

+-- {: .un_theorem}
###### Theorem
If $f$ is Henstock integrable on $[a,b]$, then $F(x) = \int_a f(x) d x$ is differentiable [[almost everywhere]] on $[a,b]$ and in fact $F' = f$ almost everywhere (although possibly not everywhere $F$ is differentiable).
=--


### Hake's theorem

+-- {: .un_theorem}
###### Theorem
For any $f$ we have
$$ \int_a^b f(x) d x = \lim_{c\to b^-} \int_a^c f(x) d x $$
in the strong sense that if either side exists, then so does the other, and they are equal.
=--

In particular, what is often taken as a *definition* of the [[improper integral|improper]] Riemann integral (of a potentially unbounded function on a finite interval) is actually a *theorem* for Henstock integrals.  (However, we still need improper Henstock integrals to allow $a = -\infty$ or $b = \infty$.)


### Recovery of Riemann and Lebesgue integrals

+-- {: .query}
I need to check some of the claims below, but I\'m out of time right now.  They are definitely correct for the proper integrals.  ---Toby
=--

Recall that $f\colon [a, b] \to \mathbb{R}$ is Riemann integrable iff $f$ is continuous almost everywhere and bounded; in this case, $f$ is also Henstock integrable, and the Riemann integral of $f$ equals its Henstock integral.

More generally, $f$ is improperly Riemann integrable iff $f$ is Henstock integrable and $f$ is locally Riemann integrable at all but finitely many points in $[a, b]$; then the improper Riemann integral of $f$ equals its Henstock integral.

Still more generally, $f\colon \mathbb{R} \to \mathbb{R}$ is improperly Riemann integrable iff $f$ is improperly Henstock integrable (meaning merely that
$$ \lim_{a \to -\infty, b \to \infty} \int_a^b f(x) \,\mathrm{d}x $$
exists using Henstock integrals) and locally Riemann integrable except at a set of [[isolated point]]s; then the improper Riemann integral of $f$ equals its improper Henstock integral.

Finally (and with incomparable generality), $f\colon \mathbb{R} \to \mathbb{R}$ is Lebesgue integrable iff ${|f|}$ is improperly Henstock integrable; then the Lebesgue integral of $f$ equals its improper Henstock integral (which is proper if the [[support]] of $f$ is [[bounded set|bounded]], of course).


[[!redirects Henstock integral]]
[[!redirects Henstock integrals]]
[[!redirects Henstock integrable]]
[[!redirects Henstock-integrable]]
[[!redirects Henstock integrable function]]
[[!redirects Henstock integrable functions]]
[[!redirects Henstock-integrable function]]
[[!redirects Henstock-integrable functions]]

[[!redirects Kurzweil integral]]
[[!redirects Kurzweil integrals]]
[[!redirects Kurzweil integrable]]
[[!redirects Kurzweil-integrable]]
[[!redirects Kurzweil integrable function]]
[[!redirects Kurzweil integrable functions]]
[[!redirects Kurzweil-integrable function]]
[[!redirects Kurzweil-integrable functions]]

[[!redirects Henstock-Kurzweil integral]]
[[!redirects Henstock-Kurzweil integrals]]
[[!redirects Henstock–Kurzweil integral]]
[[!redirects Henstock–Kurzweil integrals]]
[[!redirects Henstock--Kurzweil integral]]
[[!redirects Henstock--Kurzweil integrals]]
[[!redirects Henstock-Kurzweil integrable function]]
[[!redirects Henstock-Kurzweil integrable functions]]
[[!redirects Henstock–Kurzweil integrable function]]
[[!redirects Henstock–Kurzweil integrable functions]]
[[!redirects Henstock--Kurzweil integrable function]]
[[!redirects Henstock--Kurzweil integrable functions]]

[[!redirects Kurzweil-Henstock integral]]
[[!redirects Kurzweil-Henstock integrals]]
[[!redirects Kurzweil–Henstock integral]]
[[!redirects Kurzweil–Henstock integrals]]
[[!redirects Kurzweil--Henstock integral]]
[[!redirects Kurzweil--Henstock integrals]]
[[!redirects Kurzweil-Henstock integrable function]]
[[!redirects Kurzweil-Henstock integrable functions]]
[[!redirects Kurzweil–Henstock integrable function]]
[[!redirects Kurzweil–Henstock integrable functions]]
[[!redirects Kurzweil--Henstock integrable function]]
[[!redirects Kurzweil--Henstock integrable functions]]

[[!redirects Denjoy integral]]
[[!redirects Denjoy integrals]]
[[!redirects Denjoy integrable function]]
[[!redirects Denjoy integrable functions]]

[[!redirects Luzin integral]]
[[!redirects Luzin integrals]]
[[!redirects Luzin integrable function]]
[[!redirects Luzin integrable functions]]

[[!redirects Perron integral]]
[[!redirects Perron integrals]]
[[!redirects Perron integrable function]]
[[!redirects Perron integrable functions]]

[[!redirects gauge integral]]
[[!redirects gauge integrals]]
[[!redirects gauge integrable]]
[[!redirects gauge-integrable]]
[[!redirects gauge integrable function]]
[[!redirects gauge integrable functions]]
[[!redirects gauge-integrable function]]
[[!redirects gauge-integrable functions]]
