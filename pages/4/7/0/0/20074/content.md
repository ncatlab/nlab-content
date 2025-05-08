
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[probability theory]] the _central limit theorem_ is a [[theorem]] which asserts that the [[sum]] of independent [[random variables]] [[limit of a sequence|tends]] to a [[normal distribution]].

+-- {: .query}
Perhaps a diagram like could be used to express the central limit theorem:

\begin{tikzcd}
	\Omega & {\mathcal{N}} \\
	{X_n} & {Y_n}
	\arrow["f", from=1-1, to=1-2]
	\arrow["{\mathrm{sample}}"', from=1-1, to=2-1]
	\arrow["{\mathrm{sample}}", from=1-2, to=2-2]
	\arrow["g"', from=2-1, to=2-2]
\end{tikzcd}

where

- \[f(\Omega) = \mathcal{N}\left(\mu_\Omega, \sigma^2_\Omega\right)\]
  maps a distribution with finite mean and variance to the normal distribution with the same mean and variance.

- \[g(X) = n \mapsto \mu + \frac {\sum_{m = 0}^n X_m - \mu} {\sqrt{n}}\]
  maps one (random) sequence to another

However, it needs some fixing up. A major issue is the transformed sequence merely converges like a random sequence sampled from the normal distribution. Random sequences are hard to formalize for good reason.
=--


## Related concepts

* [[statistical significance]]

## References

See also

* Wikipedia, _[Central limit theorem](https://en.wikipedia.org/wiki/Central_limit_theorem)_

[[!redirects central limit theorems]]