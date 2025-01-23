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

An **enhanced factorisation system** on a [[2-category]] is an orthogonal [[factorisation system on a 2-category]] such that, for any invertible 2-cell $\alpha : t e \Rightarrow m s$

\begin{tikzcd}
	A & B \\
	C & D
	\arrow["e", from=1-1, to=1-2]
	\arrow["t", from=1-2, to=2-2]
	\arrow["s"', from=1-1, to=2-1]
	\arrow["m"', from=2-1, to=2-2]
	\arrow["\alpha"{description}, draw=none, from=1-2, to=2-1]
\end{tikzcd}

there is a unique pair of a 1-cell $r : B \to C$ and invertible 2-cell $\beta : t \Rightarrow m r$ such that $r e = s$ and $\beta e = \alpha$.

\begin{tikzcd}
	A & B \\
	C & D
	\arrow["e", from=1-1, to=1-2]
	\arrow["s"', from=1-1, to=2-1]
	\arrow[""{name=0, anchor=center, inner sep=0}, "r"{description}, from=1-2, to=2-1]
	\arrow["t", from=1-2, to=2-2]
	\arrow["m"', from=2-1, to=2-2]
	\arrow["\beta"{description, pos=0.6}, draw=none, from=0, to=2-2]
\end{tikzcd}

## References

The condition to be an enhanced factorisation system was observed in the following, though the concept was not isolated:

* [[A. J. Power]],  _A general coherence result_, J. Pure Appl. Algebra 57 (1989), no. 2, 165&#8211;173. [doi:10.1016/0022-4049(89)90113-8](http://dx.doi.org/10.1016/0022-4049%2889%2990113-8) [MR0985657](http://www.ams.org/mathscinet-getitem?mr=985657)

Enhanced factorisation systems were defined in

* [[Stephen Lack]]. _Codescent objects and coherence_. Journal of Pure and Applied Algebra **175** 1-3 (2002) 223-241 &lbrack;<a href="https://doi.org/10.1016/S0022-4049(02)00136-6">doi:10.1016/S0022-4049(02)00136-6</a>&rbrack;

attributed to [[Max Kelly]].

[[!redirects enhanced factorisation systems]]
[[!redirects enhanced factorization system]]
[[!redirects enhanced factorization systems]]
