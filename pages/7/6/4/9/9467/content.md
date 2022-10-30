
# Cauchy\'s mistake
* table of contents
{: toc}

## Overview

In his influential 1821 textbook _[[Cours d'Analyse]]_, [[Augustin Cauchy]] states a theorem that is now widely regarded as false, attributed to a confusion between [[pointwise convergence]] and [[uniform convergence]].  This mistake ---if indeed it is a mistake--- is of both pedagogical and philosophical-historical interest.


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

Analysing this argument, Philipp von Seidel (first, and others afterwards) realised that it could be fixed if $f$ converges to $f_\infty$ _[[uniform convergence|uniformly]]_, so that $n$ is independent of $h$.  Another fix is to make $h$ independent of $n$, by requiring the family $f$ to be [[equicontinuous family|equicontinuous]], although this idea came much later.


### In epsilontics

Writing Cauchy\'s argument in the epsilontic language developed by [[Karl Weierstrass]], we have:

+-- {: .proof}
###### Non-proof
(Non-theorem \ref{mistake})

Let $\epsilon$ be a [[positive number]], and consider $\epsilon/3$.  Because $f$ converges to $f_\infty$ at $x$, there is some [[natural number]] $N$ such that ${|f_n(x) - f_\infty(x)|} \lt \epsilon/3$ whenever $n \geq N$.  Because $f_n$ is continuous at $x$ for each $n$, there is some positive number $\delta$ such that ${|f_n(x + h) - f_n(x)|} \lt \epsilon/3$ whenever $h \lt \delta$.  Because $f$ converges to $f_\infty$ at $x + h$ for each $h$, there is some natural number $N$ such that ${|f_\infty(x + h) - f_n(x + h)|} \lt \epsilon/3$ whenever $n \geq N$.  Therefore, there is some $\delta$ such that
$$    {|f_\infty(x + h) - f_\infty(x)|}
 \leq {|f_\infty(x + h) - f_n(x + h)|} + {|f_n(x + h) - f_n(x)|} + {|f_n(x) - f_\infty(x)|}
  \lt \epsilon/3 + \epsilon/3 + \epsilon/3
    = \epsilon
.$$
In other words, $f_\infty$ is continuous.
=--

...


### In nonstandard analysis

...


## References

The original mistake is in

*  [[Augustin Cauchy]] (1821); _[[Cours d'Analyse]].

The reconstruction in terms of nonstandard analysis is in the historical appendix to

*  [[Abraham Robinson]] (1960); _Nonstandard Analysis_.

An interesting discussion forms Chapter 3 of

*  [[Imre Lakatos]] (1978); _Mathematics, Science, and Epistemology_.

(This partly retracts Lakatos\'s analysis in _[[Proofs and Refutations]]_.)


[[!redirects Cauchy's mistake]]
[[!redirects Cauchy's mistake]]
[[!redirects Cauchy\'s mistake]]
