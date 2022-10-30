
# The Henstock integral
* table of contents
{: toc}

## Idea

The *Henstock integral* (also attributed to *Kurzweil*, *Denjoy*, *Luzin*, and *Perron*, and sometimes called, neutrally but perhaps ambiguously, the *gauge integral*) is a way to define the [[integral]] of a (partial) function $f:\mathbb{R}\to \mathbb{R}$ which applies to more functions than either the [[Riemann integral]] or the [[Lebesgue integral]] and is in some ways better behaved as well.

For instance, the (even) function
$$
t\mapsto \frac{\sin(1/t^3)}{t},\quad t \in \mathbb{R}\setminus\{0\}
$$
is not Lebesgue integrable on any interval containing 0, but it has ([[David Roberts|DR]]: according to WolframAlpha) Henstock integral
$$
\int_{0}^x \frac{\sin (1/t^3)}{t} = \frac{1}{3}\left( \pi - 2 Si(1/x^3)\right)
$$
where $Si(x)$ is the [[sine integral]] $\int_0^x \frac{\sin(t)}{t}dt $ (note that $Si$ extends to an [[entire function]] on $\mathbb{C}$).


However, the Lebesgue integral is more commonly used by working mathematicians because it fits more naturally into the general theory of [[measure]], while the Riemann/Darboux integral is more commonly used in introductory calculus courses because its definition is simpler.


## Definition

Let $[a,b]$ be a closed [[interval]] in $\mathbb{R}$ and let $f:[a,b]\to \mathbb{R}$.  A *tagged partition* $P$ of $[a,b]$ is a finite sequence of points $a = u_0 \lt u_1 \lt \dots \lt u_{n+1} = b$ together with points $t_i \in [u_i, u_{i+1}]$ for all $i$.  The *Riemann sum* of $f$ over such a tagged partition is 

$$ \sum_P f = \sum_{i=0}^{n} f(t_i) \cdot (u_{i+1} - u_{i}). $$

Define a *gauge* on $[a,b]$ to be any function $\delta: [a,b] \to (0,\infty)$.  We say that a tagged partition is *$\delta$-fine* if $[u_i, u_{i+1}] \subset (t_i - \delta(t_i), t_i + \delta(t_i))$.

Finally, we say that $I$ is the **integral** of $f$ on $[a,b]$, written $I = \int_{a}^b f(x) d x$, if for any $\epsilon\gt 0$ there exists a gauge $\delta$ such that

$$ {| \sum_P f - I |} \lt \epsilon $$

for any $\delta$-fine partition $P$.  If such an $I$ exists, we say that $f$ is (Henstock) **integrable** on $[a,b]$.

If we require a gauge to be a [[constant function]], then we recover the definition of the [[Riemann integral]].


## Properties

### The fundamental theorem of calculus

The Henstock integral satisfies a very nice form of the [[fundamental theorem of calculus]]:

+-- {: .un_theorem}
###### Theorem
If $f$ is differentiable on $[a,b]$, then $f'$ is Henstock integrable on $[a,b]$, and $\int_a^b f'(x) d x = f(b) - f(a)$.
=--

+-- {: .un_theorem}
###### Theorem
If $f$ is Henstock integrable on $[a,b]$, then $F(x) = \int_a^x f(t) d t$ is differentiable [[almost everywhere]] on $[a,b]$ and $F' = f$.
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
