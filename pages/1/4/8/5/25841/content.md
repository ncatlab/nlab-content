## Definition

In a [[double category]] $\mathbb{D}$ with (chosen) [[companions]], a *retrocell* with boundary 
\begin{tikzcd}
	A & C \\
	B & D
	\arrow[""{name=0, anchor=center, inner sep=0}, "f", "\shortmid"{marking}, from=1-1, to=1-2]
	\arrow["h"', from=1-1, to=2-1]
	\arrow["k", from=1-2, to=2-2]
	\arrow[""{name=1, anchor=center, inner sep=0}, "g"', "\shortmid"{marking}, from=2-1, to=2-2]
	\arrow["\varphi", shorten <=15pt, shorten >=15pt, Rightarrow, from=1, to=0, color=red]
\end{tikzcd}
is defined to be a cell in $\mathbb{D}$ as follows, where $f^{\ast}$ and $k^{\ast}$ are the (chosen) companions of $f$ and $k$, respectively. 
\begin{tikzcd}
	A & B & D \\
	A & C & D
	\arrow["{h^{\ast}}", "\shortmid"{marking}, from=1-1, to=1-2]
	\arrow[Rightarrow, no head, from=1-1, to=2-1]
	\arrow["g", "\shortmid"{marking}, from=1-2, to=1-3]
	\arrow["\varphi"{description}, draw=none, from=1-2, to=2-2]
	\arrow[Rightarrow, no head, from=1-3, to=2-3]
	\arrow["f"', "\shortmid"{marking}, from=2-1, to=2-2]
	\arrow["{k^{\ast}}"', "\shortmid"{marking}, from=2-2, to=2-3]
\end{tikzcd}

## Example

* The double category $\mathbb{S}\mathrm{pan}(\mathcal{C})$ of [[spans]] in a category $\mathcal{C}$ has companions.
The companion of a morphism $f \colon A \rightarrow B$ is a span $A \overset{1_{A}}{\leftarrow} A \overset{f}{\rightarrow} B$. 
A retrocell $\varphi$ in $\mathbb{S}\mathrm{pan}(\mathcal{C})$, as denoted above, corresponds to a morphism of spans as follows. 
\begin{tikzcd}
	A & A & B & X & D \\
	&& {A \times_{B}X} \\
	&& Y \\
	A & Y & C & C & D
	\arrow[Rightarrow, no head, from=1-1, to=4-1]
	\arrow[Rightarrow, no head, from=1-2, to=1-1]
	\arrow["h", from=1-2, to=1-3]
	\arrow["{g_{1}}"', from=1-4, to=1-3]
	\arrow["{g_{2}}", from=1-4, to=1-5]
	\arrow[Rightarrow, no head, from=1-5, to=4-5]
	\arrow["{\pi_{A}}", from=2-3, to=1-2]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=135}, draw=none, from=2-3, to=1-3]
	\arrow["{\pi_{X}}"', from=2-3, to=1-4]
	\arrow["\varphi", from=2-3, to=3-3]
	\arrow[Rightarrow, no head, from=3-3, to=4-2]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=-45}, draw=none, from=3-3, to=4-3]
	\arrow["{f_{2}}", from=3-3, to=4-4]
	\arrow["{f_{1}}", from=4-2, to=4-1]
	\arrow["{f_{2}}"', from=4-2, to=4-3]
	\arrow[Rightarrow, no head, from=4-4, to=4-3]
	\arrow["k"', from=4-4, to=4-5]
\end{tikzcd}

## References

* [[Robert Paré]], _Retrocells_, Theory and Applications of Categories, Vol. 40, 2024, No. 5, pp 130-179. &lbrack;[TAC](http://www.tac.mta.ca/tac/volumes/40/5/40-05abs.html), [arXiv:2306.06436](https://arxiv.org/abs/2306.06436)&rbrack;