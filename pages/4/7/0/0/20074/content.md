
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
Perhaps a diagram like

\begin{tikzcd}
	{\Omega(\mu, \sigma^2)} && {\mathcal{N}(\mu, \sigma^2) } \\
	\\
	{X_n} && {n \mapsto \mu + \frac {\sum_{m = 0}^n X_m - \mu} {\sqrt{n}}}
	\arrow[from=1-1, to=1-3]
	\arrow["{\mathrm{sample}}"', from=1-1, to=3-1]
	\arrow["{\mathrm{sample}}", from=1-3, to=3-3]
	\arrow[from=3-1, to=3-3]
\end{tikzcd}

could be used to express this, but it needs some fixing up. A major issue is the transformed sequence merely converges like a random sequence sampled from the normal distribution.
=--


## Related concepts

* [[statistical significance]]

## References

See also

* Wikipedia, _[Central limit theorem](https://en.wikipedia.org/wiki/Central_limit_theorem)_

[[!redirects central limit theorems]]