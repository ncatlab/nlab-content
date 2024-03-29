
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--



Several numbers are named after [[Euler]].

# Contents
* table of contents
{: toc}

## Euler's number 

**Euler's number** is the [[irrational number]] typically denoted "[[e]]" and defined by the [[series]]

$$
  e \coloneqq \sum_{n \in \mathbb{N}} \frac{1}{n!}
  \,.
$$

This happens to also be the [[groupoid cardinality]] of the [[groupoid]] $core(FinSet)$, the [[core]] of [[FinSet]].


## Euler numbers

The **Euler numbers** (also called _secant numbers_) $E_n$, $n\geq 0$ are a sequence of [[integer|integers]] defined via the generating function

$$
\frac{1}{ch t}= \frac{2}{e^t+e^{-t}} = \sum_{n\geq 0} E_n \frac{t^n}{n!}
$$

All odd-numbered members of the sequence vanish: $E_{2k-1}=0$ for $k\in\mathbb{N}$. $E_0=1$, $E_2 = -1$, $E_4 = 5$, see [Euler number at wikipedia](http://en.wikipedia.org/wiki/Euler_number) for more and the [Abramowitz--Stegun handbook](http://en.wikipedia.org/wiki/Abramowitz_and_Stegunfor) for many Euler numbers. 
 
+-- {: .num_remark} 
###### Remark 
Sometimes Euler numbers are defined as a different sequence that includes tangent numbers (and is non-alternating in sign): 

$$\sec(x) + \tan(x) = \sum_{n \geq 0} E_n \frac{x^n}{n!}$$ 

where one has $1, 1, 1, 2, 5, 16, \ldots$ as the first few such Euler numbers. These $E_n$ satisfy the recurrence 

$$2 E_{n+1} = \sum_i \binom{n}{i} E_i E_{n-i}$$ 

and count the number of alternating [[permutations]] $\pi$ on $\{1, 2, \ldots, n\}$, i.e. permutations such that $\pi(1) \gt \pi(2) \lt \pi(3) \gt \ldots$. See for example this $n$-Category Caf&#233; [post](https://golem.ph.utexas.edu/category/2008/02/metric_spaces.html#c014963). 
=-- 

Euler numbers generalize to __Euler polynomials__ $E_n(x)$ defined via the generating function

$$
\frac{2e^{tx}}{e^t+1}=\sum_{n\geq 0} E_n(x) \frac{t^n}{n!},
$$ 

so that $E_n = 2^n E_n(\frac{1}{2})$. The Euler polynomials satisfy the recursion $E_n(x+1)+E_n(x)=2x^n$ and may be conversely expressed via Euler numbers as

$$
E_n(x) = \sum_k \left(\array{n\\ k}\right) \frac{E_k}{2^k}\left(x-\frac{1}{2}\right)^{n-k}
$$

There is also a complementarity formula $E_n(1-x)=(-1)^n E_n(x)$. 
See e.g. Louis Comtet, __Advanced combinatorics__, D. Reifel Publ. Co., Dordrecht-Holland, Boston 1974 [djvu](http://ftp.filekeeper.org/download/acm/books/Comtet%20Louis%20-%20Advanced%20Combinatorics.djvu)


## Eulerian numbers

There are also **Eulerian numbers** (forming a different, double sequence $A(n,k)$). Combinatorially, $A(n, k)$ counts the number of permutations $\pi$ of the set $\{1, 2, \ldots, n\}$ with $k$ _ascents_ (an ascent of $\pi$ is an element $j$ such that $\pi(j) \lt \pi(j+1)$). Alternatively, the double sequence can be defined recursively through the formula 

$$x^n = \sum_k A(n, k) \binom{x+k}{n}.$$ 

For applications in algebraic geometry, see "Eulerian polynomials-[Hirzebruch]".

## Euler-Mascheroni constant 

There is also a number, usually denoted as $\gamma$, called the _Euler-Mascheroni constant_. It is defined as a limit 

$$\gamma \coloneqq \lim_{n \to \infty} \sum_{k=1}^n \frac1{k} - \log n$$ 

where $\log$ is the natural [[logarithm]]. It arises for example in discussions of the [[Gamma function]]. 

## Related concepts

* [[exponential map]]

* [[e]]

* [[pi]]

* [[golden ratio]]


[[!redirects Euler number]]
[[!redirects Euler numbers]]
[[!redirects Euler's number]]
[[!redirects Euler's numbers]]

[[!redirects Euler's constant]]

[[!redirects Eulerian number]]
[[!redirects Eulerian numbers]]

[[!redirects Euler polynomial]]
[[!redirects Euler polynomials]]
