
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Internal categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For any [[category]] $\mathcal{E}$ with pullbacks, it is easy to define the notion of [[internal category|category in]] $\mathcal{E}$, and the definition of an internal [[functor]] between such is similarly straightforward.  But it is not so obvious how to define [[presheaf|presheaves]] on internal categories, because they must land in the ambient category $\mathcal{E}$.

The solution lies in thinking of presheaves on an ordinary category $\mathcal{E}$, and more generally [[profunctor]]s $C &#8696; D$, as giving sets equipped with an _action_ of the arrows of $C,D$, i.e. as their [[category of elements|categories of elements]].

## Definition

Let $\mathbf{Span}(\mathcal{E})$ be the the [[bicategory]] of [[span|spans]] in a category $\mathcal{E}$ with [[pullbacks]]. 
The bicategory $\mathbf{Prof}(\mathcal{E})$ of [[internal categories]] and profunctors in $\mathcal{E}$ is defined to be the bicategory $\mathbf{Mod}(\mathbf{Span}(\mathcal{E}))$ of [[monads]] and [[module over a monad|modules]] in $\mathbf{Span}(\mathcal{E})$.

An *internal profunctor* $C \nrightarrow D$ between internal categories $C$ and $D$ is a module from $C$ to $D$.  An *internal presheaf* on $C$, or an *internal discrete fibration*, is a module $C \nrightarrow 1$, where $1$ is the [[discrete category]] on the [[terminal object]] of $\mathcal{E}$. Dually, an *internal discrete opfibration* is a module $1 \nrightarrow D$. 

An internal presheaf in $\mathcal{E}$ is the same thing as an [[internal diagram]] in $\mathcal{E}$.

### Details

Let $C = (s, C_{1}, t) \colon C_{0} \nrightarrow C_{0}$ and $D = (s, D_{1}, t) \colon D_{0} \nrightarrow D_{0}$ be the underlying graphs of monads in the bicategory $\mathbf{Span}(\mathcal{E})$, that is, $C$ and $D$ are internal categories in $\mathcal{E}$. 
Consider a span $(f_{0}, M_{0}, g_{0}) \colon C_{0} \nrightarrow D_{0}$ as a $1$-cell in $\mathbf{Span}(\mathcal{E})$. 

A *left $C$-module* consists of a morphism of spans $\lambda \colon (s, C_{1}, t) ; (f_{0}, M_{0}, g_{0}) \Rightarrow (f_{0}, M_{0}, g_{0})$, as depicted below, that is compatible with the unit and multiplication maps of the monad $C$. 
\begin{tikzcd}[column sep=scriptsize]
	{C_{0}} & {C_{1}} & {C_{0}} & {M_{0}} & {D_{0}} \\
	&& {C_{1}\times_{C_{0}}M_{0}} \\
	{C_{0}} && {M_{0}} && {D_{0}}
	\arrow[Rightarrow, no head, from=1-1, to=3-1]
	\arrow["s"', from=1-2, to=1-1]
	\arrow["t", from=1-2, to=1-3]
	\arrow["{f_{0}}"', from=1-4, to=1-3]
	\arrow["{g_{0}}", from=1-4, to=1-5]
	\arrow[Rightarrow, no head, from=1-5, to=3-5]
	\arrow[from=2-3, to=1-2]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=135}, draw=none, from=2-3, to=1-3]
	\arrow[from=2-3, to=1-4]
	\arrow["\lambda"', from=2-3, to=3-3]
	\arrow["{f_{0}}", from=3-3, to=3-1]
	\arrow["{g_{0}}"', from=3-3, to=3-5]
\end{tikzcd}

\begin{lemma}
A left $C$-module determines an internal category $M_{C}$ and a span of internal functors $C \leftarrow M_{C} \rightarrow \mathsf{disc}(D_{0})$ whose left leg is an internal [[discrete fibration]]. The underlying morphism of internal graphs is depicted below. 
\begin{tikzcd}
	{C_{0}} & {M_{0}} & {D_{0}} \\
	{C_{1}} & {C_{1} \times_{C_{0}} M_{0}} & {D_{0}} \\
	{C_{0}} & {M_{0}} & {D_{0}}
	\arrow["{f_{0}}"', from=1-2, to=1-1]
	\arrow["{g_{0}}", from=1-2, to=1-3]
	\arrow[Rightarrow, no head, from=1-3, to=2-3]
	\arrow["s", from=2-1, to=1-1]
	\arrow["t"', from=2-1, to=3-1]
	\arrow["\lambda"', from=2-2, to=1-2]
	\arrow[from=2-2, to=2-1]
	\arrow[from=2-2, to=2-3]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=-90}, draw=none, from=2-2, to=3-1]
	\arrow[from=2-2, to=3-2]
	\arrow[Rightarrow, no head, from=2-3, to=3-3]
	\arrow["{f_{0}}", from=3-2, to=3-1]
	\arrow["{g_{0}}"', from=3-2, to=3-3]
\end{tikzcd}
\end{lemma}

A *right $D$-module* consists of a morphism of spans $\rho \colon (f_{0}, M_{0}, g_{0}) ; (s, D_{1}, t) \Rightarrow (f_{0}, M_{0}, g_{0})$, as depicted below, that is compatible with the unit and multiplication maps of the monad $D$. 
\begin{tikzcd}[column sep=scriptsize]
	{C_{0}} & {M_{0}} & {D_{0}} & {D_{1}} & {D_{0}} \\
	&& {M_0 \times_{D_0} D_{1}} \\
	{C_{0}} && {M_{0}} && {D_{0}}
	\arrow[Rightarrow, no head, from=1-1, to=3-1]
	\arrow["{f_{0}}"', from=1-2, to=1-1]
	\arrow["{g_{0}}", from=1-2, to=1-3]
	\arrow["s"', from=1-4, to=1-3]
	\arrow["t", from=1-4, to=1-5]
	\arrow[Rightarrow, no head, from=1-5, to=3-5]
	\arrow[from=2-3, to=1-2]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=135}, draw=none, from=2-3, to=1-3]
	\arrow[from=2-3, to=1-4]
	\arrow["\rho"', from=2-3, to=3-3]
	\arrow["{f_{0}}", from=3-3, to=3-1]
	\arrow["{g_{0}}"', from=3-3, to=3-5]
\end{tikzcd}

\begin{lemma}
A right $D$-module determines an internal category $M_{D}$ and a span of internal functors $\mathsf{disc}(C_{0}) \leftarrow M_{D} \rightarrow D$ whose right leg is an internal [[discrete opfibration]]. The underlying morphism of internal graphs is depicted below. 
\begin{tikzcd}
	{C_{0}} & {M_{0}} & {D_{0}} \\
	{C_{0}} & {M_{0} \times_{D_{0}} D_{1}} & {D_{1}} \\
	{C_{0}} & {M_{0}} & {D_{0}}
	\arrow["{f_{0}}"', from=1-2, to=1-1]
	\arrow["{g_{0}}", from=1-2, to=1-3]
	\arrow[Rightarrow, no head, from=2-1, to=1-1]
	\arrow[Rightarrow, no head, from=2-1, to=3-1]
	\arrow[from=2-2, to=1-2]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=90}, draw=none, from=2-2, to=1-3]
	\arrow[from=2-2, to=2-1]
	\arrow[from=2-2, to=2-3]
	\arrow["\rho"', from=2-2, to=3-2]
	\arrow["s"', from=2-3, to=1-3]
	\arrow["t", from=2-3, to=3-3]
	\arrow["{f_{0}}", from=3-2, to=3-1]
	\arrow["{g_{0}}"', from=3-2, to=3-3]
\end{tikzcd}
\end{lemma}

An *internal profunctor* $(\lambda, \rho) \colon C \nrightarrow D$, or [[module over a monad|module]] in $\mathbf{Span}(\mathcal{E})$, between internal categories $C$ and $D$ consists of a span $(f_{0}, M_{0}, g_{0}) \colon C_{0} \nrightarrow D_{0}$ equipped with a left $C$-module $\lambda$ and a right $D$-module $\rho$ which are compatible, in the sense that the following diagram commutes. 
\begin{tikzcd}
	{C_{1} \times_{C_{0}} M_{0} \times_{D_{0}} D_{1}} & {M_{0} \times_{D_{0}} D_{1}} \\
	{C_{1}\times_{C_{0}} M_{0}} & {M_{0}}
	\arrow["{\lambda \times D_{1}}", from=1-1, to=1-2]
	\arrow["{C_{1} \times \rho}"', from=1-1, to=2-1]
	\arrow["\rho", from=1-2, to=2-2]
	\arrow["\lambda"', from=2-1, to=2-2]
\end{tikzcd}