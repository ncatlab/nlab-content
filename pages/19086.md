# Contents 
* table of contents 
{:toc} 

## Introduction 

For $x \gt 0$, let $\pi(x)$ denote the number of primes $p \leq x$ (in these notes, $p$ is always used to denote prime numbers). The celebrated [[prime number theorem|Prime Number Theorem]] is the asymptotic statement 

$$\pi(x) \sim \frac{x}{\log(x)}$$ 

where we recall that $f(x) \sim g(x)$ means $\underset{x \to \infty}{\lim} \frac{f(x)}{g(x)} = 1$. 

This was first proven in 1896 independently by Hadamard and de la Vall&eacute;e-Poussin, first by proving a result on the zeroes of the Riemann zeta function $\zeta(s)$ (that none occur on the line $Re(s) = 1$), which can be proven without too much difficulty. They then deduced the prime number theorem from this result, by a fairly intricate analysis. 

Over the decades this analysis was whittled down more and more until it reached a fairly definitive form, in the form of a succinct "Tauberian theorem" due to [D.J. Newman (1980)](#new). A streamlined account was written up in the American Mathematical Monthly by [Don Zagier (1997)](#zag1), who managed to produce a proof virtually from scratch in a little less than three pages (it requires just a bit of background in complex analysis, not much more than Cauchy's theorem). 

As in his famous [one-sentence proof](#zag2) that primes of the form $4n+1$ are sums of two squares, Zagier seemed to be aiming explicitly for maximal compression while still keeping the argument (arguably) self-contained. It's an impressive performance, alright, but its terseness will probably force most readers to follow up with pen and paper on the side to verify his arguments in detail. In this article we will mostly follow Zagier's line, but with some slight expansions and glosses so that pen and paper is (hopefully) unnecessary. 


## Chebyshev's estimate 

In this section we prove a result essentially due to Chebyshev which puts us already in the neighborhood of the prime number theorem. Introduce a function  

$$\theta(x) = \sum_{p \leq x} \log(p).$$ 
 
By the following result, our job is done once we establish the relation $\theta(x) \sim x$. 

+-- {: .num_lemma #asymp} 
###### Lemma 
The asymptotic statement $\theta(x) \sim x$ implies the prime number theorem. 
=--

+-- {: .proof} 
###### Proof 
In one direction, we have an obvious inequality 

$$\theta(x) = \sum_{p \leq x} \log(p) \leq \sum_{p \leq x} \log(x) = \pi(x)\log(x).$$ 

Assuming that $\theta(x) \sim x$, this implies that given $\epsilon \gt 0$, the inequality 

$$\label{ineq1} 1 - \epsilon \lt \frac{\pi(x) \log(x)}{x}$$ 

holds for all sufficiently large $x$. 

In the other direction, for any $\epsilon \gt 0$ we have 

$$\array{ 
\theta(x) & \geq & \sum_{x^{1-\epsilon} \lt p \leq x} \log(p) \\
 & \geq & \sum_{x^{1-\epsilon} \lt p \leq x} \log(x^{1-\epsilon}) \\ 
 & = & (1 - \epsilon)\log(x) \cdot (\pi(x) - \pi(x^{1 - \epsilon})) \\ 
 & \geq & (1 - \epsilon)\log(x) \cdot (\pi(x) - x^{1 - \epsilon})
}$$ 

From the last line and (eq:ineq1) (which implies $\frac{\pi(x)\log(x)}{x}$ is bounded below by a positive constant), we obtain 

$$\array{
\frac{\theta(x)}{x} & \geq & (1-\epsilon)\frac{\pi(x)\log(x)}{x} - x^{-\epsilon} \\ 
 & \geq & (1 - 2\epsilon)\frac{\pi(x)\log(x)}{x}
}$$ 

for sufficiently large $x$. Thus for any small $\epsilon \gt 0$ (say less than $1/3$) and the assumption $\theta(x) \sim x$ we have 

$$1 - \epsilon \leq \frac{\pi(x)\log(x)}{x} \leq (1 - 2\epsilon)^{-1}\frac{\theta(x)}{x} \leq (1 - 3\epsilon)^{-1}$$ 

or simply 

$$1 - \epsilon \leq \frac{\pi(x)\log(x)}{x} \leq (1 - 3\epsilon)^{-1}$$ 

for all sufficiently large $x$. 
=--

Proving the asymptotic result $\theta(x) \sim x$ will involve complex analysis applied to the Riemann zeta function. An easier preliminary result gives information on the *order* of $\theta(x)$; it will later be used as a technical hypothesis in the Tauberian theorem with which we conclude. The order result is essentially due to Chebyshev, who actually established sharper estimates (which we won't need). In fact, he also showed that if $\frac{\pi(x)\log(x)}{x}$ has a limit, then that limit must be $1$. 

+-- {: .num_lemma #cheb} 
###### Lemma 
$\theta(x) = \mathrm{O}(x)$. 
=-- 

+-- {: .proof} 
###### Proof 
First let us observe that 

$$2^{2n} \geq \binom{2n}{n} \geq \prod_{n \lt p \lt 2n} p = \exp(\theta(2n) - \theta(n))$$ 

so that 

$$2n\log(2) \geq \theta(2n) - \theta(n).$$ 

If $n \leq x \lt n+1$, then $\theta(x) = \theta(n)$ and $\theta(2x) \leq \theta(2n) + \log(2x)$, so that 

$$2x\log(2) \geq 2n\log(2) \geq \theta(2n) - \theta(n) \geq \theta(2x) - \log(2x)  - \theta(x)$$ 

or simply 

$$\theta(x) - \theta(x/2) \leq x\log(2) + \log(x).$$ 

Taking a telescopic sum, we have 

$$\theta(x) = \sum_{k = 0}^{n-1} \theta(x/2^k) - \theta(x/2^{k+1}) \leq \sum_{k=0}^{n-1} (x/2^k)\log(2) + \sum_{k=0}^{n-1} \log(x/2^k)$$ 

where $n$ is chosen so that $1 \leq x/2^n \lt 2$ (so $n = floor(\log_2(x))$). The first term on the right is bounded above by $\log(2) x$. The second term is bounded above by $\log_2(x) \cdot \log(x) = K\log(x)^2$ (where $K = \log_2(e)$), which considered asymptotically is small compared to $x$. Thus, for any $C \gt \log(2)$, we have 

$$\theta(x) \leq C x$$ 
for all sufficiently large $x$, which completes the proof. 
=-- 


## Analytic continuation of the zeta function to $Re(s) \gt 0$ 

Let 

$$\label{prod} \zeta(s) = \sum_{n=1}^\infty \frac1{n^s} = \prod_p \left(1 - \frac1{p^s}\right)^{-1}$$ 

define the usual Riemann zeta function on the region $Re(s) \gt 1$. First we establish a meromorphic continuation of $\zeta(s)$ to the region $Re(s) \gt 0$, or in fact a holomorphic continuation of $\zeta(s) - \frac1{s-1}$ to this region. 

+-- {: .num_prop #cont} 
###### Proposition 
The function $\Psi$ defined by the expression 

$$\Psi(s) = \sum_{n=1}^\infty \int_n^{n+1} \frac1{n^s} - \frac1{x^s}\; d x$$ 

converges absolutely for $Re(s) \gt 0$, giving a holomorphic function in that region, and 

$$\Psi(s) = \zeta(s) - \frac1{s-1}$$ 

over the region $Re(s) \gt 1$. 
=-- 

+-- {: .proof} 
###### Proof 
Let us bound the summands in the definition of $\Psi(s)$: 

$$\array{
\left| \int_n^{n+1} \frac1{n^s} - \frac1{x^s}\; d x \right| & = & \left| \int_n^{n+1} \int_n^x \; \frac{s}{t^{s+1}}\; d t\; d x \right|\\ 
 & \leq & \int_n^{n+1} \int_n^x \; \frac{{|s|}}{{|t^{s+1}|}}\;d t \; d x \\ 
 & = & \int_n^{n+1} \int_n^x \; \frac{{|s|}}{t^{Re(s) + 1}}\; d t\; d x \\ 
 & \leq & \int_n^{n+1} \int_n^x \; \frac{{|s|}}{n^{Re(s) + 1}}\;d t \; d x \\
 & \leq & \frac{{|s|}}{n^{Re(s) + 1}}.
}$$ 

Since $\sum_{n=1}^\infty \frac1{n^{Re(s) + 1}}$ converges over the region $Re(s) \gt 0$, it follows that the series for $\Phi(s)$ converges absolutely, and $\Psi(s)$ is a holomorphic function, in that region. 

Over the region $Re(s) \gt 1$, we have 

$$\array{
\Psi(s) & = & \sum_{n=1}^\infty \frac1{n^s} - \int_n^{n+1} \frac1{x^s}\; d x \\
 & = & \sum_{n=1}^\infty \frac1{n^s} - \sum_{n=1}^\infty \int_n^{n+1} \frac1{x^s}\; d x \\ 
 & = & \zeta(s) - \int_1^\infty \frac1{x^s}\; d x \\ 
 & = & \zeta(s) - \frac1{s-1}
}$$ 

as asserted. 
=-- 



## The zeta function has no zeroes on the line $Re(s) = 1$ 

Now we relate $\theta(x)$ to $\zeta(s)$ by introducing an auxiliary function $\Phi$ that is connected with the logarithmic derivative of $\zeta(s)$. For $Re(s) \gt 1$ put 

$$\Phi(s) = \sum_p \frac{\log(p)}{p^s}.$$ 

Over $Re(s) \gt 1$, we calculate 

$$\log \zeta(s) = -\sum_p \log(1 - p^{-s})$$ 

which upon differentiating yields 

$$\array{
\frac{\zeta^'(s)}{\zeta(s)} & = & -\sum_p \frac{\log(p) p^{-s}}{1 - p^{-s}} \\
 & = & -\sum_p \log(p) p^{-s} -\sum_p \frac{\log(p) p^{-s}p^{-s}}{1 - p^{-s}} \\ 
 & = & -\Phi(s) - \sum_p \frac{\log(p)}{p^s(p^s - 1)}
}$$ 

with the last sum converging over the region $Re(s) \gt \frac1{2}$. From this and the analytic continuation of $\zeta(s)$ (Proposition \ref{cont}), we see that $\Phi(s)$ admits a meromorphic continuation over $Re(s) \gt \frac1{2}$, and holomorphic in that region except possibly where $\zeta(s)$ has zeroes, or at the simple pole $s = 1$. 

+-- {: .num_prop #nozero} 
###### Proposition 
$\Phi(s) - \frac1{s-1}$ is holomorphic over the region $Re(s) \geq 1$, i.e., $\zeta(s)$ has no zeroes over $Re(s) \geq 1$. 
=-- 

+-- {: .proof} 
###### Proof 
The case $Re(s) \gt 1$ is easily handled by the product formula (eq:prod). 

For a fixed $t \gt 0$, let $\mu$ be the order of the zero of $\zeta(1 + i t)$ (if $\zeta(1 + i t) \neq 0$ then of course $\mu = 0$); it is the same as the order of the zero at $s = 1 - i t$. Let $\nu$ be the order of the zero at $1 \pm 2i t$. We then have 

1. $\underset{\epsilon \searrow 0}{\lim} \epsilon \cdot \Phi(1 + \epsilon) = 1$ (since $\zeta(s)$ has a pole of order $1$ at $s = 1$), and similarly 

1. $\underset{\epsilon \searrow 0}{\lim} \epsilon \cdot \Phi(1 + \epsilon \pm i t) = -\mu$, 

1. $\underset{\epsilon \searrow 0}{\lim} \epsilon \cdot \Phi(1 + \epsilon \pm 2i t) = -\nu$. 

Observe that for $\epsilon \gt 0$, 

$$\array{
0 & \leq & \epsilon \cdot \sum_p \frac{\log(p)}{p^{1 + \epsilon}} (p^{i t/2} + p^{-i t/2})^4 \\ 
 & = & \epsilon \cdot \sum_p \frac{\log(p)}{p^{1 + \epsilon}} \sum_{k = -2}^2 \binom{4}{r + 2} p^{-i r t} \\ 
 & = & \epsilon \cdot \sum_{r = -2}^2 \binom{4}{r+2} \Phi(1 + \epsilon + i r t) 
}$$ 

from which, in conjunction with 1., 2., 3. above, we deduce $0 \leq 6 - 8\mu - 2\nu$, so that $\mu = 0$. 
=-- 

The function $\theta(x)$ is related to the function $\Phi(s)$ by way of a Riemann-Stieltjes integral: 

$$\Phi(s) = \sum_p \frac{\log(p)}{p^s} = \int_1^\infty \frac{d \theta(x)}{x^s}$$ 

for $Re(s) \gt 1$. An integration by parts yields 

$$\int_1^M \frac{d \theta(x)}{x^s} = \left[\frac{\theta(M)}{M^s} - \theta(1)\right] + \int_1^M \theta(x) \frac{s}{x^{s+1}}\; d x$$ 

where $\underset{M \to \infty}{\lim} \frac{\theta(M)}{M^s} = 0$ by Lemma \ref{cheb}. Thus 

$$\label{RS} \Phi(s) = s \int_1^\infty \frac{\theta(x)}{x^{s+1}}\; d x = s \int_0^\infty e^{-s t} \theta(e^t)\; d t.$$ 

## Reduction to a Tauberian theorem 

The asymptotic result $\theta(x) \sim x$ will be established by appeal to the following result: 

+-- {: .num_theorem #conv} 
###### Theorem 
Suppose that the integral 

$$\int_1^\infty \; \frac{\theta(x) - x}{x^2}\; d x$$

converges. Then $\theta(x) \sim x$. 
=-- 

+-- {: .proof} 
###### Proof 
Suppose that for some $\lambda \gt 1$ there exist arbitrarily large $x$ such that $\lambda x \leq \theta(x)$. The monotonicity of $\theta$ implies the first inequality that follows: 

$$\int_x^{\lambda x} \; \frac{\theta(t) - t}{t}\; \frac{d t}{t} \geq \int_x^{\lambda x} \; \frac{\lambda x - t}{t}\; \frac{d t}{t} = \int_1^\lambda \; \frac{\lambda x - t x}{t x} \; \frac{d t}{t} = \int_1^\lambda \; \frac{\lambda - t}{t^2}\; d t \gt 0.$$ 

This is a contradiction, because convergence of $\int_1^\infty \; \frac{\theta(t) - t}{t^2}\; d t$ implies that $\int_x^{\lambda x} \; \frac{\theta(t) - t}{t^2}\; d t$ can be made arbitrarily small by taking $x$ large. 

Similarly, if we suppose that for some $\lambda \lt 1$ there exist arbitrarily large $x$ such that $\theta(x) \leq \lambda x$, then 

$$\int_{\lambda x}^x \; \frac{\theta(t) - t}{t}\; \frac{d t}{t} \leq \int_{\lambda x}^x \; \frac{\lambda x - t}{t}\; \frac{d t}{t} = \int_\lambda^1 \; \frac{\lambda x - t x}{t x} \; \frac{d t}{t} = \int_\lambda^1 \; \frac{\lambda - t}{t^2}\; d t \lt 0$$ 

which again leads to a contradiction. 
=--  

Thus we focus on convergence of 

$$\label{rewrite} \int_1^\infty \; \frac{\theta(x) - x}{x}\; \frac{d x}{x} = \int_0^\infty \; \frac{\theta(e^t) - e^t}{e^t}\; d t$$ 

For $Re(s) \gt 1$ we have, from (eq:RS),  

$$\array{
\frac{\Phi(s)}{s} - \frac1{s-1} & = & \int_0^\infty \; e^{-s t}\theta(e^t) - e^{(1-s)t}\; dt \\ 
 & = & \int_0^\infty \; e^{-s t} (\theta(e^t) - e^t)\; d t
}$$ 

or what is the same, for the region $Re(s) \gt 0$, 

$$\label{laplace} \frac{\Phi(s+1)}{s+1} - \frac1{s} = \int_0^\infty \; e^{-(s+1) t} (\theta(e^t) - e^t)\; d t = \int_0^\infty \; e^{-s t}\left( \frac{\theta(e^t) - e^t}{e^t} \right)\; d t
$$ 

where the left side is in fact holomorphic over $Re(s) \geq 0$, hence takes a finite value at $s = 0$, say $L$. 

The Tauberian theorem we will establish permits the conclusion 

$$L = \underset{s \searrow 0}{\lim} \int_0^\infty \; e^{-s t}\left( \frac{\theta(e^t) - e^t}{e^t} \right)\; d t = \int_0^\infty \; \frac{\theta(e^t) - e^t}{e^t} \; d t$$ 

which in turn will yield the Prime Number Theorem: 

+-- {: .num_theorem #pnt} 
###### Theorem 
The integral $\int_0^\infty \; \frac{\theta(e^t) - e^t}{e^t} \; d t$ converges. 
=-- 

(The prime number theorem follows from this by (eq:rewrite), Theorem \ref{conv}, and Lemma \ref{asymp}.) 

## Proof of the Tauberian theorem 

Here is the statement of the particular Tauberian theorem used (recalling that "Tauberian" signifies a family of theorems that roughly speaking give conditions for convergence of series or integral expressions occurring at natural boundaries of regions where series or integral representations are defined). This particular form was given by D.J. Newman, and allows a dramatic shortening of the proof of the prime number theorem, as shown convincingly by Zagier, who as we said compressed it down to under three pages. 

+-- {: .num_theorem #taub} 
###### Theorem 
Let $f(t)$ be a function that is bounded and locally integrable over the domain $t \geq 0$, and suppose that its Laplace transform, defined for $Re(s) \gt 0$ by the equation 

$$g(s) = \int_0^\infty \; e^{-s t} f(t)\; d t,$$ 

extends to a function $g$ that is holomorphic over the region $Re(s) \geq 0$. Then the integral $\int_0^\infty\; f(t)\; d t$ converges and equals $g(0)$. 
=-- 

The proof below involves some fairly refined complex analysis. It may be well to recall that we say a function $g$ is *holomorphic* at a point $z_0$ if $g$ is defined over a small neighborhood $\{z: {|z-z_0|} \lt \delta\}$ of the point and in that neighborhood is expressible as a convergent Taylor series 

$$g(z) = \sum_{n=0} \frac{a_n (z - z_0)^n}{n!}.$$ 

Then we say $g$ is holomorphic over a (not necessarily open) region if it is holomorphic at every point in the region. 

In the case of interest $f(t) = \frac{\theta(e^t) - e^t}{e^t}$, the order estimate Lemma \ref{cheb} guarantees that $f$ is bounded and locally integrable, and we have already observed that its Laplace transform, which is 

$$g(s) = \frac{\Phi(s+1)}{s+1} - \frac1{s}$$ 

by (eq:laplace), is holomorphic in the region $Re(s) \geq 0$ by Proposition \ref{nozero}. Thus all the hypotheses of the theorem are satisfied in this case, and its conclusion in this case is Theorem \ref{pnt}. So all that remains is to prove Theorem \ref{taub}. 

+-- {: .proof} 
###### Proof 
For $T \geq 0$, put 

$$g_T(s) = \int_0^T \; e^{-s t} f(t)\; d t.$$ 

Clearly $g_T$ is an entire (i.e., everywhere holomorphic) function. We are trying to show that $\underset{T \to \infty}{\lim} g_T(0) = g(0)$. 

A straightforward application of Cauchy's theorem yields 

$$g_T(0) - g(0) = \frac1{2\pi i} \int_C \; \left(g_T(z) - g(z)\right) e^{z T}\; \frac{d z}{z}$$ 

for contours $C$ having $0$ as an interior point, such that $g_T - g$ is holomorphic on $C$ and its interior. We will choose $C$ to be the boundary of the closed region $D = \{z: {|z|} \leq R\; and\; Re(z) \geq -\delta\}$ where for a given $R$, we choose $\delta$ small enough that $g_T - g$ is holomorphic in $D$ (this uses compactness of the interval $I = \{i t: -R \leq t \leq R\}$ and holomorphicity of $g_T - g$ along $I$). 

The idea would be to estimate the contribution of the integral over $C_+$, the part of $C$ where the real part is nonnegative, and over $C_-$ where it is nonpositive, hoping to show these contributions are small when $R$ is large. This almost works, except that we don't have good control over the size of the contributions near the area where $Re(z) = 0$. To offset this, a mollifying factor $(1 + \frac{z^2}{R^2})$ is introduced in the integrand ("Carleman's formula"): this is close to zero near $Re(z) = 0$ and has the desired mitigating effect. 

Thus we instead use 

$$g_T(0) - g(0) = \frac1{2\pi i} \int_C \; \left(g_T(z) - g(z)\right) e^{z T}\; \left(1 + \frac{z^2}{R^2}\right)\; \frac{d z}{z}$$ 

Suppose now that ${|f(t)|}$ is globally bounded by $B$. For $Re(z) \gt 0$ we have 

$${|g_T(z) - g(z)|} \leq \int_T^\infty\; {|f(t)e^{-z t}|}\; d t \leq B \int_T^\infty e^{-Re(z)t}\; d t = B \frac{e^{-Re(z)T}}{Re(z)}$$ 

and we also have, over the circle ${|z|} = R$, 

$$\array{
{|e^{z T}(1 + z^2/R^2)(1/z)|} & = & e^{Re(z)T} \cdot {|(R^2 z^{-1} + z)/R^2|} \\ 
 & = & e^{Re(z)T} \cdot {|({|z|}^2 z^{-1} + z)/R^2|} \\ 
 & = & e^{Re(z)T} \cdot {|(\bar{z} + z)/R^2|} \\ 
 & = & e^{Re(z)T} \cdot {|2Re(z)|}/R^2
}$$ 

so that putting the factors together, the integral over $C_+$ is bounded in absolute value by 

$$2B/R^2 \int_{C_+}\; {|d z|} = 2\pi B/R$$ 

(and of course this hasn't taken into account the factor $\frac1{2\pi i}$ outside the integral). In any case, with the Carleman factor, the contribution 
from the $C_+$ part is $B/R$, which is small if $R$ is large. 

Now we bound the contribution from $C_-$ by considering $g_T$ and $g$ separately. First let us bound 

$$\frac1{2\pi i} \int_{C_-} \; g_T(z) e^{z T}\; \left(1 + \frac{z^2}{R^2}\right)\; \frac{d z}{z}.$$ 

For this, we can take advantage of the fact that $g_T$ is entire, and (courtesy of Cauchy's theorem) replace $C_-$ by the semicircle where ${|z|} = R, Re(z) \lt 0$. The estimates are similar in form to those above, starting with

$${|g_T(z)|} \leq \int_0^T {|f(t)|}\cdot {|e^{-z t}|}\; d t \leq B \int_0^T e^{-Re(z)t}\; d t \leq B \int_{-\infty}^T e^{-Re(z)t}\; d t = B \frac{e^{-Re(z)T}}{-Re(z)}.$$ 

Bear in mind here that we are now considering $Re(z) \lt 0$ and $-Re(z) = {|Re(z)|}$; the bound produced tends to be very large. But, large as it may be, it is offset by the bound on the product of the remaining factors in the integrand, which is $e^{Re(z)T} \cdot {|2Re(z)|}/R^2$. We conclude as before that over $C_-$ the overall contribution from $g_T$ has upper bound $B/R$. 

Finally, we bound 

$$\frac1{2\pi i} \int_{C_-} \; g(z) e^{z T}\; \left(1 + \frac{z^2}{R^2}\right)\; \frac{d z}{z}.$$

Holding $R$ fixed, the expression $g(z)\cdot \left(1 + \frac{z^2}{R^2}\right) \cdot \frac1{z}$ taken over $C_-$ is bounded in absolute value by a number $K$. Whereas along $Re(z) = -\delta$, by taking $T$ very large we can make ${|e^{z T}|}$ as small as we like, so that considering $g$ separately, the contribution over $C_-$ can be discarded as vanishingly small (in other words, first pick $R$, then pick $\delta$, and finally pick $T$, to get this contribution to be as small as we like). This completes the proof. 
=-- 

## References 

* {#new} Donald J. Newman, *Simple analytic proof of the prime number theorem*, Amer. Math. Monthly 87 (1980), 693-696. 

* {#zag1} Don Zagier, *Newman's short proof of the prime number theorem*, Amer. Math. Monthly 104 (1997), 705-708. ([pdf](https://www.maa.org/sites/default/files/pdf/upload_library/22/Chauvenet/Zagier.pdf)) 

* {#zag2} Don Zagier, *A one-sentence proof that every prime $p \equiv 1 (\mod 4)$ is a sum of two squares*, Amer. Math. Monthly, Vol. 97 No. 2 (1990), p. 144. ([link](https://people.mpim-bonn.mpg.de/zagier/files/doi/10.2307/2323918/fulltext.pdf)) 
