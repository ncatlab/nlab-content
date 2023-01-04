
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

\tableofcontents

## Idea

The set $\Sigma_\mathbb{N} \coloneqq \mathbb{N} \cong \mathbb{N}$ is the [[symmetric group]] of the [[natural numbers]], whose elements $p \in \Sigma_\mathbb{N}$ are the [[permutations]] of the set of natural numbers.

The **Riemann series theorem** or the **Riemann rearrangement theorem** states that given a [[sequence]] of [[real numbers]] $a:\mathbb{N} \to \mathbb{R}$, if the [[series]] $\sum_{n=0}^{\infty} a_n$ is [[conditionally convergent]], then 

* for all real numbers $M \in \mathbb{R}$, there exists a [[permutation]] $p \in \Sigma_\mathbb{N}$ such that the series $\sum_{n=0}^{\infty} a_{p(n)}$ converges to $M$. 

* there exists a [[permutation]] $p \in \Sigma_\mathbb{N}$ such that the series $\sum_{n=0}^{\infty} a_{p(n)}$ diverges. 

## Construction of the real numbers

The Riemann series theorem could be used to construct the [[real numbers]]. Since the Riemann series theorem holds for any conditionally convergent series, it suffices to use the conditionally convergent series defined by the sequence of [[rational numbers]] $a:\mathbb{N} \to \mathbb{Q}$ where $a_{2 n} = \frac{1}{n}$ and $a_{2 n + 1} = -\frac{1}{n}$. Then we define the real numbers as a quotient set $\mathbb{R} \coloneqq C(\Sigma_\mathbb{N})/\sim$ of the subset of the symmetric group of the natural numbers $C(\Sigma_\mathbb{N}) \subseteq \Sigma_\mathbb{N}$ for which the series $\sum_{n=0}^{\infty} a_{p(n)}$ converges for $p \in \Sigma_\mathbb{N}$; i.e. for which the sequence of partial sums is a [[Cauchy sequence]]. We say that permutations $p \in C(\Sigma_\mathbb{N})$ and $q \in C(\Sigma_\mathbb{N})$ are similar $p \sim q$ if their corresponding series have the same limit. This is similar to the construction of the [[real numbers]] as the quotient set of all Cauchy sequences of rational numbers. 

## In constructive mathematics

The Riemann series theorem cannot be proved in [[constructive mathematics]]. In general, given a sequence of rational numbers $a:\mathbb{N} \to \mathbb{Q}$ such that the series $\sum_{n=0}^{\infty} a_n$ is [[conditionally convergent]], any permutation of the indices $p \in \Sigma_\mathbb{N}$ such that the series $\sum_{n=0}^{\infty} a_{p(n)}$ converges would only converges to the [[Cantor real numbers]], since the sequence of partial sums of a series of rational numbers is a sequence of rational numbers, and the limit of any Cauchy sequence of rational numbers is only a [[Cantor real number]]. In the absence of [[excluded middle]] or [[countable choice]], one cannot prove that any [[sequentially Cauchy complete]] [[Archimedean ordered field]], such as the [[Dedekind real numbers]], is equivalent to the [[Cantor real numbers]]. 

## See also

* [[conditional convergence]]

## References

* Wikipedia, *[Riemann series theorem](https://en.wikipedia.org/wiki/Riemann_series_theorem)*