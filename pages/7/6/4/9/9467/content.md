# The Cauchy sum theorem
* table of contents
{: toc}

## Overview

In his influential 1821 textbook _[[Cours d'Analyse]]_, [[Augustin Cauchy]] states a [[theorem]] that is now widely regarded as [[false]], attributed to a confusion between [[pointwise convergence]] and [[uniform convergence]].  This mistake --- if indeed it was a mistake --- is of both pedagogical and philosophical-historical interest.

[[counterexample|Counterexamples]] (specific [[Fourier series]]) were known already to [[Joseph Fourier]], and [[Niels Abel]] specifically pointed them out as counterexamples to Cauchy\'s claim.  However, Cauchy denied that these were [[counterexamples]], on the grounds that the series did not converge everywhere (which is a hypothesis in the theorem).  [[Imre Lakatos]] has argued that the confusion rests on different conceptions of the [[continuum]], so that Cauchy\'s notion of convergence everywhere is really more like Weierstrass\'s notion of uniform convergence than pointwise convergence, and the theorem as he intended it is true.

Although Cauchy\'s original formulation was about the sum of an [[infinite series]], we will consider it in the slightly more elementary context of the limit of an [[infinite sequence]]; the modern isomorphism between these was already well established and used explicitly by Cauchy.


## Statements

+-- {: .num_theorem #mistake}
###### Non-theorem (attributed to Cauchy, 1821)

Let $f = (f_1, f_2, \ldots)$ be an [[infinite sequence]] of [[continuous functions]] from the [[real line]] to itself.  Suppose that, for every [[real number]] $x$, the sequence $(f_1(x), f_2(x), \ldots)$ converges to some (necessarily unique) real number $f_\infty(x)$, defining a [[function]] $f_\infty$; in other words, the sequence $f$ [[pointwise convergence|converges pointwise]] to $f_\infty$.  Then $f_\infty$ is also continuous.
=--

+-- {: .num_theorem #uniform}
###### Theorem (attributed to Seidel, 1847)

Let $f = (f_1, f_2, \ldots)$ be an [[infinite sequence]] of [[continuous functions]] from the [[real line]] to itself.  Suppose that the sequence $f$ [[uniform convergence|converges uniformly]] to a function $f_\infty$.  Then $f_\infty$ is also continuous.
=--

+-- {: .num_theorem #equicontinuous}
###### Theorem (attributed to ???)

Let $f = (f_1, f_2, \ldots)$ be an [[equicontinuous family|equicontinuous]] [[infinite sequence|sequence]] of (necessarily [[continuous functions|continuous]]) functions from the [[real line]] to itself.  Suppose that, for every [[real number]] $x$, the sequence $(f_1(x), f_2(x), \ldots)$ converges to some (necessarily unique) real number $f_\infty(x)$, defining a [[function]] $f_\infty$; in other words, the sequence $f$ [[pointwise convergence|converges pointwise]] to $f_\infty$.  Then $f_\infty$ is also continuous.
=--


## Counterexamples

The first counterexamples to Non-Theorem \ref{mistake} arose as [[Fourier series]].  The sawtooth wave
$$ \sum_{k = 1}^\infty \frac{\sin(k x)}{k} = \frac{\pi}{2} - \frac{x \mathbin{mod} 2 \pi}{2} $$
may be the simplest.  Each partial sum of this [[infinite series]] is continuous; the sum converges pointwise as indicated for $x$ not a multiple of $2 \pi$ and to $0$ (which is the average of the limits $\pm\pi/2$ on either side) for $x$ a multiple of $2 \pi$.  However, the sequence of partial sums is not equicontinuous, nor does it converge uniformly.  And indeed, the sum is not continuous at multiples of $2 \pi$.

A simple counterexample from outside of this context is
$$ f_n(x) \coloneqq x^n $$
on $[0,1]$.  (We can make this a function on all of $\mathbb{R}$ by letting $f_n(x)$ be $f_n(0) = 0$ for $x \lt 0$ and letting $f_n(x)$ be $f_n(1) = 1$ for $x \gt 1$.)  Each $f_n$ is continuous; the pointwise limit is $f_\infty(x) = 0$ for $x \lt 1$ but $f_\infty(x) = 1$ for $x \geq 1$, which is not continuous.  Again, the sequence is not equicontinuous, and its convergence is not uniform.

Another counterexample is
$$ f_n(x) \coloneqq \exp ({-n {|x|}}) .$$
(The [[absolute value]] is here only to handle negative values of $x$; the example is [[analytic function|analytic]] on $]0,\infty[$.)  Now $f_\infty(0) = 1$, while $f_\infty(x) = 0$ for $x \ne 0$.


## Proofs

Here is Cauchy\'s argument:
+-- {: .proof}
###### Proof?

At any $x$, we have
$$
      {|f_\infty(x + h) - f_\infty(x)|}
    = {|f_\infty(x + h) - f_n(x + h) + f_n(x + h) - f_n(x) + f_n(x) - f_\infty(x)|}
 \leq {|f_\infty(x + h) - f_n(x + h)|} + {|f_n(x + h) - f_n(x)|} + {|f_n(x) - f_\infty(x)|}
.$$
As $n$ becomes infinite and $h$ becomes infinitesimal, all of the terms on the right become infinitesimal (respectively, because $f$ converges to $f_\infty$ at $x + h$, because $f_n$ is continuous at $x$, and because $f$ converges to $f_\infty$ at $x$).  Thus, the expression on the left also becomes infinitesimal, proving that $f_\infty$ is continuous at $x$.
=--

Nowadays, we\'d say that a variable approaches zero rather than that it becomes infinitesimal.  If we interpret this argument in modern analysis, then the proof is flawed, because (the lower bound for) $n$ depends on $h$ in the first term, while (the upper bound for the absolute value of) $h$ depends on $n$ in the second term; they cannot be chosen simultaneously.

Analysing this argument, Philipp von Seidel (first, and others afterwards) realised that it could be fixed if $f$ converges to $f_\infty$ _[[uniform convergence|uniformly]]_, so that $n$ is independent of $h$.  Another fix is to make $h$ independent of $n$, by requiring the family $f$ to be [[equicontinuous family|equicontinuous]], although this idea came later.


### In epsilontics

Writing Cauchy\'s argument in the [[epsilontic analysis|epsilontic]] language developed by [[Karl Weierstrass]], we have:
+-- {: .proof}
###### Non-proof
(Non-theorem \ref{mistake}).

Let $\epsilon$ be a [[positive number]], and consider $\epsilon/3$.  Because $f$ converges to $f_\infty$ at $x$, there is some [[natural number]] $N$ such that ${|f_n(x) - f_\infty(x)|} \lt \epsilon/3$ whenever $n \geq N$.  Because $f_n$ is continuous at $x$ for each $n$, there is some positive number $\delta$ such that ${|f_n(x + h) - f_n(x)|} \lt \epsilon/3$ whenever $h \lt \delta$.  Because $f$ converges to $f_\infty$ at $x + h$ for each $h$, there is some natural number $N$ such that ${|f_\infty(x + h) - f_n(x + h)|} \lt \epsilon/3$ whenever $n \geq N$.  Therefore, there are $N$ and $\delta$ such that
$$    {|f_\infty(x + h) - f_\infty(x)|}
 \leq {|f_\infty(x + h) - f_n(x + h)|} + {|f_n(x + h) - f_n(x)|} + {|f_n(x) - f_\infty(x)|}
  \lt \epsilon/3 + \epsilon/3 + \epsilon/3
    = \epsilon
$$
whenever $n \geq N$ and $h \lt \delta$.  Fixing any such $n$, $f_\infty$ is continuous.
=--

We have used the variable names $n$ and $h$ in two different [[contexts]] each, then pretended that they arose in a single context for the final inequality.  The error can be made more explicit by using different variable names:
+-- {: .proof}
###### Non-proof
(Non-theorem \ref{mistake}).

Let $\epsilon$ be a [[positive number]], and consider $\epsilon/3$.  Because $f$ converges to $f_\infty$ at $x$, there is some [[natural number]] $N$ such that ${|f_n(x) - f_\infty(x)|} \lt \epsilon/3$ whenever $n \geq N$.  Because $f_{n'}$ is continuous at $x$ for each $n'$, there is some positive number $\delta$ such that ${|f_{n'}(x + h) - f_{n'}(x)|} \lt \epsilon/3$ whenever $h \lt \delta$.  Because $f$ converges to $f_\infty$ at $x + h'$ for each $h'$, there is some natural number $N'$ such that ${|f_\infty(x + h') - f_{n''}(x + h')|} \lt \epsilon/3$ whenever $n'' \geq N'$.  Therefore, there are $N, N'$ and $\delta$ such that
$$    {|f_\infty(x + h) - f_\infty(x)|}
 \leq {|f_\infty(x + h') - f_{n''}(x + h')|} + {|f_{n'}(x + h) - f_{n'}(x)|} + {|f_n(x) - f_\infty(x)|}
  \lt \epsilon/3 + \epsilon/3 + \epsilon/3
    = \epsilon
$$
whenever $n, n', n'' \geq max(N, N')$ and $h, h' \lt \delta$.  Fixing any such $n, n', n''$, $f_\infty$ is continuous.
=--
The final inequality is now clearly spurious, since $n, n', n''$ need not be equal, nor $h, h'$.

This can be fixed up to a point.  We may let $n'$ be $n$ and let $h'$ be $h$, but then we have no control over $n''$.  Conversely, we may let $n, n', n''$ all be (anything bounded below by) $max(N,N')$, but then we have no control over $h'$.  Indeed, Non-theorem \ref{mistake} is false, as the counterexamples show.

However, the weaker theorems with strengthened hypotheses are valid, by similar proofs:
+-- {: .proof}
###### Proof
(Theorem \ref{uniform}).

Let $\epsilon$ be a [[positive number]], and consider $\epsilon/3$.  Because $f$ converges uniformly to $f_\infty$, there is some [[natural number]] $N$ such that ${|f_n(x + h) - f_\infty(x + h)|} \lt \epsilon/3$ for every $h$ (including $h \coloneqq 0$) whenever $n \geq N$.  Because $f_n$ is continuous at $x$ for each such $n$, there is some positive number $\delta$ such that ${|f_n(x + h) - f_n(x)|} \lt \epsilon/3$ whenever $h \lt \delta$.  Therefore, there is $N$ such that, whenever $n \geq N$, there is $\delta$ such that
$$    {|f_\infty(x + h) - f_\infty(x)|}
 \leq {|f_\infty(x + h) - f_n(x + h)|} + {|f_n(x + h) - f_n(x)|} + {|f_n(x) - f_\infty(x)|}
  \lt \epsilon/3 + \epsilon/3 + \epsilon/3
    = \epsilon
$$
whenever $h \lt \delta$.  Fixing any such $n$, $f_\infty$ is continuous.
=--
+-- {: .proof}
###### Proof
(Theorem \ref{equicontinuous}).

Let $\epsilon$ be a [[positive number]], and consider $\epsilon/3$.  Because $f$ converges to $f_\infty$ at $x$, there is some [[natural number]] $N$ such that ${|f_n(x) - f_\infty(x)|} \lt \epsilon/3$ whenever $n \geq N$.  Because $f$ is equicontinuous at $x$, there is some positive number $\delta$ such that ${|f_n(x + h) - f_n(x)|} \lt \epsilon/3$ for every $n$ whenever $h \lt \delta$.  Because $f$ converges to $f_\infty$ at $x + h$ for each such $h$, there is some natural number $N'$ such that ${|f_\infty(x + h) - f_n(x + h)|} \lt \epsilon/3$ whenever $n \geq N'$.  Therefore, there are $N$ and $\delta$ such that, whenever $h \lt \delta$, there is $N'$ such that
$$    {|f_\infty(x + h) - f_\infty(x)|}
 \leq {|f_\infty(x + h) - f_n(x + h)|} + {|f_n(x + h) - f_n(x)|} + {|f_n(x) - f_\infty(x)|}
  \lt \epsilon/3 + \epsilon/3 + \epsilon/3
    = \epsilon
$$
whenever $n \geq max(N,N')$.  Fixing any such $n$, $f_\infty$ is continuous.
=--


### In nonstandard analysis

Writing Cauchy\'s argument in the language of [[nonstandard analysis]] developed by [[Abraham Robinson]], we have:
+-- {: .proof}
###### Non-proof
(Non-theorem \ref{mistake}).

Because $f$ converges to $f_\infty$ at $x$, ${|f_n(x) - f_\infty(x)|}$ is [[infinitesimal number|infinitesimal]] whenever $n$ is [[infinite number|infinite]].  Because $f_n$ is continuous at $x$ for each finite $n$, it is continuous at $x$ for each infinite $n$ (by the [[transfer principle]]), so ${|f_n(x + h) - f_n(x)|}$ is infinitesimal whenever $h$ is infinitesimal.  Because $f$ converges to $f_\infty$ at each [[standard point]], $f$ converges to $f_\infty$ at the nonstandard point $x + h$ (by the transfer principle), so ${|f_\infty(x + h) - f_n(x + h)|}$ is infinitesimal whenever $n$ is infinite.  Therefore,
$$    {|f_\infty(x + h) - f_\infty(x)|}
 \leq {|f_\infty(x + h) - f_n(x + h)|} + {|f_n(x + h) - f_n(x)|} + {|f_n(x) - f_\infty(x)|}
$$
is also infinitesimal whenever $n$ is infinite and $h$ is infinitesimal.  Fixing any such $n$, $f_\infty$ is continuous.
=--

Both uses of the transfer principle are illegitimate, since the statements to which they\'re applied are not [[first-order logic|first-order]] in the language of the [[real numbers]].  Indeed, consider the counterexample $f_n(x) = \exp ({-n {|x|}})$ near $x = 1$.  Then ${|f_n(0 + h) - f_n(0)|} = \exp ({-n {|h|}}) - 1$ is infinitesimal as claimed iff $n h$ is infinitesimal, which may fail.  Conversely, ${|f_\infty(0 + h) - f_n(0 + h)|} = \exp ({-n {|h|}})$ (for $h \ne 0$) is infinitesimal iff $n h$ is infinite, which may also fail.  In between, when $n h$ is finite and finitesimal, both fail!

We can rewrite this proof more carefully, putting down what really follows in place of the misuse of the transfer principle:
+-- {: .proof}
###### Non-proof
(Non-theorem \ref{mistake}).

Because $f$ converges to $f_\infty$ at $x$, ${|f_n(x) - f_\infty(x)|}$ is [[infinitesimal number|infinitesimal]] whenever $n$ is [[infinite number|infinite]].  Because $f_n$ is continuous at $x$ for each finite $n$, there is some infinite $N$ such that $f_n$ is continuous at $x$ for all $n \leq N$, so then ${|f_n(x + h) - f_n(x)|}$ is infinitesimal whenever $h$ is infinitesimal.  Because $f$ converges to $f_\infty$ at each [[standard point]] and $x + h$ is [[nearstandard point|nearstandard]], there is an infinite number $N'$ such that ${|f_\infty(x + h) - f_n(x + h)|}$ is infinitesimal whenever $n \geq N'$.  Therefore,
$$    {|f_\infty(x + h) - f_\infty(x)|}
 \leq {|f_\infty(x + h) - f_n(x + h)|} + {|f_n(x + h) - f_n(x)|} + {|f_n(x) - f_\infty(x)|}
$$
is also infinitesimal whenever $n \leq N$, $n \geq N'$, and $h$ is infinitesimal.  Fixing any such $n$, $f_\infty$ is continuous.
=--
This is more clearly wrong, since there may be no such $n$ in the last step (as $N'$ may be larger than $N$).

However, we can modify this to produce correct proofs of the weaker theorems:
+-- {: .proof}
###### Proof
(Theorem \ref{uniform}).

Because $f$ converges to $f_\infty$ at $x$, ${|f_n(x) - f_\infty(x)|}$ is [[infinitesimal number|infinitesimal]] whenever $n$ is [[infinite number|infinite]].  Because $f_n$ is continuous at $x$ for each finite $n$, there is some infinite $N$ such that $f_n$ is continuous at $x$ for all $n \leq N$, so then ${|f_n(x + h) - f_n(x)|}$ is infinitesimal whenever $h$ is infinitesimal.  Because $f$ converges to $f_\infty$ uniformly, $f$ converges to $f_\infty$ at the nonstandard point $x + h$, so ${|f_\infty(x + h) - f_n(x + h)|}$ is infinitesimal whenever $n$ is infinite.  Therefore,
$$    {|f_\infty(x + h) - f_\infty(x)|}
 \leq {|f_\infty(x + h) - f_n(x + h)|} + {|f_n(x + h) - f_n(x)|} + {|f_n(x) - f_\infty(x)|}
$$
is also infinitesimal whenever $n \leq N$ is infinite and $h$ is infinitesimal.  Fixing any such $n$, $f_\infty$ is continuous.
=--
+-- {: .proof}
###### Proof
(Theorem \ref{equicontinuous}).

Because $f$ converges to $f_\infty$ at $x$, ${|f_n(x) - f_\infty(x)|}$ is [[infinitesimal number|infinitesimal]] whenever $n$ is [[infinite number|infinite]].  Because $f$ is equicontinuous at $x$, $f_n$ is continuous at $x$ even for infinite $n$, so ${|f_n(x + h) - f_n(x)|}$ is infinitesimal whenever $h$ is infinitesimal.  Because $f$ converges to $f_\infty$ at each [[standard point]] and $x + h$ is [[nearstandard point|nearstandard]], there is an infinite number $N$ such that ${|f_\infty(x + h) - f_n(x + h)|}$ is infinitesimal whenever $n \geq N$.  Therefore,
$$    {|f_\infty(x + h) - f_\infty(x)|}
 \leq {|f_\infty(x + h) - f_n(x + h)|} + {|f_n(x + h) - f_n(x)|} + {|f_n(x) - f_\infty(x)|}
$$
is also infinitesimal whenever $n \geq N$ and $h$ is infinitesimal.  Fixing any such $n$, $f_\infty$ is continuous.
=--
(To check that these are valid, one must know the nonstandard formulations of uniform convergence and equicontinuity that are used; but they are correct.  Specifically, a sequence $f$ of functions converges uniformly to a function $f_\infty$ iff, for every hyperreal number $x$, the sequence $f(x) = (f_n(x))_n$ of hyperreal numbers converges to the hyperreal number $f_\infty(x)$; and $f$ is equicontinuous at a real number $x$ iff, for every hyperinteger $n$, the hyperfunction $f_n$ is continuous at $x$.)

On the other hand, in the light of nonstandard analysis, we can also reevaluate Cauchy\'s original claim.  Cauchy himself, when confronted with counterexamples such as the Fourier series, denied that the sequence of functions converged everywhere.  One interpretation of this is that it fails to converge at some nonstandard points.  By this analysis, Cauchy\'s notion of convergence everywhere is our modern notion of uniform convergence, not pointwise convergence, and his theorem is true (and his proof correct, even if less detailed than one might like).


## Lakatos\'s view

In his experimental textbook _[[Proofs and Refutations]]_, [[Imre Lakatos]] used Cauchy\'s sum theorem to motivate the concept of uniform convergence.  Two years later, he partially reevaluated his discussion in light of the question of what Cauchy\'s conception of the continuum was.

According to Lakatos, it is ahistorical to interpret Cauchy\'s 1821 result using either Weierstrass\'s epsilontics or Robinson\'s nonstandard analysis.  Cauchy did not mean that $f_n(x)$ converges (in $n$) for each fixed standard real number $x$, nor that it converges for each fixed hyperreal number $x$; rather, he said that it converges for each *variable* real number.  In particular, when discussing the Fourier series
$$ \sum_{k = 1}^\infty \frac{\sin(k x)}{k} ,$$
Cauchy states (in 1853) that the sequence
\[ \sum_{k = 1}^n \frac{\sin(k x)}{k} \label{FourierPS} \]
of partial sums fails to converge when $x = 1/n$; that is, $x$ is a variable whose value depends on the position in the sequence!  Such a claim is hard to interpret in an epsilontic framework; but in a nonstandard framework, it simply means that for some particular infinite values of $n$ and infinitesimal values of $x$ (namely those for which $x = 1/n$), this partial sum is not infinitely close to $0$ (which is the value of the partial sum at $x = \lim_n (1/n) = 0$), demonstrating that the sequence is not equicontinuous.

If we (still arguably ahistorically) interpret convergence to mean to that $f_n(x_n)$ converges (in $n$) for every convergent sequence $(x_n)_n$ of real numbers, then this is equivalent (given that each $f_n$ is continuous) to uniform convergence, and Cauchy\'s result would again be true and his argument would be (when formalised with either epsilontics or nonstandard analysis) valid.

On the other hand (and this goes beyond what Lakatos wrote), one way to interpret Cauchy\'s claim that (eq:FourierPS) fails to converge when $x = 1/n$ is, using nonstandard analysis, simply that for any particular infinite value of $n$ and using the infinitesimal value $x = 1/n$, this partial sum is not infinitely close to $0$ (which is the value of the infinite sum at $x = \lim_n (1/n) = 0$).  This suggests interpreting convergence to mean that $f_n(c+h)$ is infinitely close to $f_\infty(c)$ whenever $n$ is infinite and $h$ is infinitesimal (for $c$ real), which again is equivalent (given continuity of $f_n$) to uniform convergence, again justifying Cauchy\'s proof.  However, proving that uniform convergence is equivalent to this is basically the same concept as the nonstandard proof of Theorem \ref{uniform} anyway.

## Related concepts

* [[Cauchy's theorems]]

## References

The original sum theorem is in

*  [[Augustin Cauchy]] (1821). _[[Cours d'Analyse]]_.

Cauchy\'s most thorough defence of the theorem against critics is in

*  [[Augustin Cauchy]] (1853). Note sur les s&#233;ries convergentes dont les divers termes sont des fonctions continues d\'une variable r&#233;elle ou imaginaire, entre des limites donn&#233;es.

The reconstruction in terms of nonstandard analysis is in the historical appendix to

*  [[Abraham Robinson]] (1966). _Nonstandard Analysis_.

Lakatos\'s discussion forms Chapter 3 of

*  [[Imre Lakatos]] (1978). _Mathematics, Science, and Epistemology_.


[[!redirects Cauchy's mistake]]
[[!redirects Cauchy's mistake]]
[[!redirects Cauchy\'s mistake]]
[[!redirects Cauchy/'s mistake]]

[[!redirects Cauchy sum theorem]]
[[!redirects Cauchy's sum theorem]]
[[!redirects Cauchy\'s sum theorem]]
[[!redirects Cauchy's sum theorem]]
