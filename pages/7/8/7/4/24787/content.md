+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

An **enhanced factorisation system** on a [[2-category]] is a [[factorisation system on a 2-category]] such that, for any invertible 2-cell $\alpha t e \Rightarrow m s$

\begin{tikzcd}
	A & B \\
	C & D
	\arrow["e", from=1-1, to=1-2]
	\arrow["t", from=1-2, to=2-2]
	\arrow["s"', from=1-1, to=2-1]
	\arrow["m"', from=2-1, to=2-2]
	\arrow["\alpha"{description}, draw=none, from=1-2, to=2-1]
\end{tikzcd}

there is a unique pair of a 1-cell $r : B \to C$ and invertible 2-cell $\beta : t \Rightarrow mr$ such that $r e = s$ and $\beta e = \alpha$.

## References

Enhanced factorisation systems were defined in

* [[Stephen Lack]]. _Codescent objects and coherence_. Journal of Pure and Applied Algebra **175** 1-3 (2002) 223-241 &lbrack;<a href="https://doi.org/10.1016/S0022-4049(02)00136-6">doi:10.1016/S0022-4049(02)00136-6</a>&rbrack;

attributed to [[Max Kelly]].

[[!redirects enhanced factorisation systems]]
[[!redirects enhanced factorization system]]
[[!redirects enhanced factorization systems]]
