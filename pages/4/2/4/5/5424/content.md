# Contents
* table of contents
{:toc}

## Definition

### In set theory

Let $S$ be a set equipped with a binary relation $\prec$. Then a **bisimulation** is a binary relation $\sim$ such that for all $x \in S$ and $y \in S$ such that $x \sim y$, the following conditions hold:

* for all $a \in S$ such that $a \prec x$, there exists a $b \in S$ such that $b \prec y$ and $a \sim b$
* for all $b \in S$ such that $b \prec y$, there exists a $a \in S$ such that $a \prec x$ and $a \sim b$

For [[labelled transition systems]], [Walker 1994](#Walker94) gives a definition equivalent to the following:

\begin{definition}
On a system with points $P,Q,\ldots$ and transition relations $\{\overset{\alpha}{\rightarrow}:\alpha\in L\}$, a *bisimulation* is a symmetric relation $\sim$ such that whenever $P\sim Q$, $\alpha\in L$ and $P\overset{\alpha}{\rightarrow}P'$, then $Q\overset{\alpha}{\rightarrow}Q'$ with $P'\sim Q'$.
\end{definition}

\begin{definition}
Bisimilarity is the greatest bisimulation.
\end{definition}

Let $\mathrm{traces}(s)$ be the set of all possible (finite or infinite) transition sequences starting as $s$.
Trace equivalence, defined as $s\sim t$ if and only if $\mathrm{traces}(s)=\mathrm{traces}(t)$, is a bisimulation.

### In category theory

In Joyal-Nielsen-Winskel (p.13) is given the following definition. For what a "path category in a category of models" is, see there.

\begin{definition}
Let $P$ be a path category in a category of models $M$. Two objects $X_1,X_2$ are called to be *$P$-bisimilar* if there is a span of $P$-open maps $X_1\leftarrow X\to X_2$.
\end{definition}

The relation of $P$-open maps and [[open map]]s is given by Proposition 11, p.32:

\begin{proposition}
If $P$ is a dense full subcategory of $M$, then $f$-is $P$-open iff $M(-,f)$ is an [[open map]].
\end{proposition}

## See also

* [[simulation]]

* [[extensional relation]]

* [[transition system]]

* [[cotopos]]

* [[coinduction]]

## References

* Wikipedia (English), _[Bisimulation](http://en.wikipedia.org/wiki/Bisimulation)_
*  Peter Aczel; [Non-Well-Founded Sets](https://web.archive.org/web/20161020002632/https://standish.stanford.edu/pdf/00000056.pdf), especially Chapter 4.
* Sam Staton, _[Relating coalgebraic notions of bisimulation](http://arxiv.org/abs/1101.4223)_
* Davide Sangiorgi, _[On the Origins of Bisimulation and Coinduction](http://www.cs.unibo.it/~sangio/DOC_public/history_bis_coind.pdf)_
* [[André Joyal]], Mogens Nielsen, [[Glynn Winskel]], Bisimulation from [[open map|open maps]], [pdf](http://www.brics.dk/RS/94/7/BRICS-RS-94-7.pdf)
* Bard Bloom, Sorin Istrail, Albert Meyer, Bisimulation can't be traced, [pdf](http://www.cse.psu.edu/~catuscia/DEA/General/BloomIstrailMeyer.pdf)
* Yde Venema, Algebras and Coalgebras, &#167;6 (p.332-426).11(p.398-403) in Blackburn, van Benthem, Wolter, Handbook of modal logic, Elsevier, 2007.
* [[Pedro Resende]], _Quantales, finite observations and strong bisimulation_, Theor. Comp. Sci. __254__:1&#8211;2 (2001) 95&#8211;149, <a href="http://dx.doi.org/10.1016/S0304-3975(99)00123-1">doi</a>
* David Walker, _On Bisimulation in the [[pi-calculus|$\pi$-calculus]]_, CONCUR '94: Concurrency Theory (1994).

[[!redirects bisimulations]]
[[!redirects bisimilarity]]
[[!redirects bisimilarities]]