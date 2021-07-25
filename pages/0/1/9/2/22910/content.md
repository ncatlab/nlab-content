
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The "Mercator series" (so named after its appearance in [Mercator 1667](#Mercator1667)) is the [[Taylor series]] of the [[natural logarithm]] around 1.

## Statement

\begin{proposition}\label{MercatorSeries}
The [[Taylor series]] of the [[natural logarithm]] around $1 \in \mathbb{R}$ is the following [[series]]:
\[
  \label{MercatorTaylorSeriesForNaturalLogarithm}
  \begin{aligned}
  \underoverset{n = 0}{\infty}{\sum}
  \tfrac{1}{n!}
  \left(
    \frac{d^n}{ d x^n} ln(1 + x)
  \right)_{\vert x = 0}
  x^n
  & 
  \;\;
  =
  \;\;
  \underoverset{n = 1}{\infty}{\sum}
  \frac
    {(-1)^{n+1}}
    {n} 
  x^n
  \\
  &
  \;\;
  =
  \;\;
  x
  - \tfrac{1}{2} x^2
  + \tfrac{1}{3} x^3
  - \tfrac{1}{4} x^4
  + \cdots
  \,.
  \end{aligned}
\]
\end{proposition}
\begin{proof}
For the first two terms notice that
$$
  ln(1 + x) 
  \;\xrightarrow{x \to 0}\;
  ln(1)
  \,=\,
  0
$$
and that the [[derivative]] of the natural logarithm is:
$$
  \frac{d}{d x} \ln(1 + x)
  \;=\;
  \tfrac{1}{1+x}
  \;\xrightarrow{ x \to 0 }\; 
  1
  \,.
$$
From here on, noticing for $k \in \mathbb{N}_+$ that:
$$
  \frac{d}{d x} 
  \left(
  \frac{1}{(1 + x)^k}
  \right)
  \;=\;
  - k
  \frac{1}{(1 + x)^{k+1}}
  \;\xrightarrow{x \to 0}\; 
  - k
$$
we obtain for $n \in \mathbb{N}_+$, by [[induction]]:
$$
  \begin{aligned}
  \frac{d^n}{d x^n} 
  ln(1 + x)
  &
  \;=\;
  \frac{d^{n-1}}{d x^{n-1}}
  \left(
    \frac{1}{1 + x}
  \right)
  \\
  &
  \;=\;
  (n-1)! \cdot (-1)^{n-1}
  \frac{1}{(1 + x)^{n-1}}
  \\
  &
  \;\xrightarrow{ x \to 0 }\; 
  (n-1)! \cdot (-1)^{n+1}
  \end{aligned}
  \,.
$$
Plugging this into the defining equation on the left of (eq:MercatorTaylorSeriesForNaturalLogarithm) and using 
$$
  \frac{(n-1)!}{n!} = \frac{1}{n}
$$
yields the claim.
\end{proof}

## Related concepts

* [[Chern form]]

* [[geometric series]]

## References

Apparently first published in:

* {#Mercator1667} [[Nicholas Mercator]], *Logarithmotechnia: Sive Methodus constuendi Logrithmos*, London 1667  ([GoogleBooks](https://books.google.de/books?hl=en&lr=&id=HFl1JqyXpSoC&oi=fnd&pg=PP6&dq=Logarithmotechnia.&ots=2xDsxWNWwO&sig=PfSwMZjoMnW7EAtH79uxX3ATsqc&redir_esc=y#v=onepage&q=Logarithmotechnia.&f=false))

but will have been known before that.

See also:

* Wikipedia, *[Mercator series](https://en.wikipedia.org/wiki/Mercator_series)*
