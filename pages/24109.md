
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Statement

The **Banach fixed-point theorem** or **contraction mapping theorem** states: 

Let $(X, \rho)$ be a [[sequentially Cauchy complete]] [[metric space]] with a point $x_0:X$ and a [[rational number]] $C : \mathbb{Q}$ such that for all $x:X$ and $y:X$, $\rho(x, y) \leq C$. Let $T : X \to X$ be an [[endomap]] with a [[rational function|rational]] [[Lipschitz constant]] $0 \lt c \lt 1$. Then $X$ has a unique [[fixed point]], a point $x$ with $\rho(T (x), x) = 0$,
such that for any $y : X$ with $\rho(T (y), y) = 0$, $x = y$. 

## Related concepts

* [[inverse function theorem]]

* [[ordinary differential equation]]

## References

* Auke B. Booij, Analysis in univalent type theory ([pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf))

See also:

* Wikipedia, _[Banach fixed-point theorem](https://en.wikipedia.org/wiki/Banach_fixed-point_theorem)_

[[!redirects Banach fixed point theorem]]
[[!redirects contraction mapping theorem]]