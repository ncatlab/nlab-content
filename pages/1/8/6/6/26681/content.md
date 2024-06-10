
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

A family of subsets of a [[topological space]], for which for every point the intersection of subsets containing it is open, is called an _inner-preserving family_ or _Q family_.

A [[topological space]], for which every (countable) open covering has an inner-preserving open [[refinement]], is called _(countably) orthocompact_.

## Properties

Orthocompactness generalizes other notations of compactness:

* [[compact|Compact]] spaces are orthocompact as finite open refinements are inner-preserving in particular.
* (Countably) [[metacompact]] spaces are (countably) orthocompact as point finite open refinements are inner-preserving in particular.
* (Countably) [[paracompact]] spaces are (countably) orthocompact as locally finite open refinements are inner-preserving in particular.

\begin{prop}
Closed subsets of (countably) orthocompact spaces are (countably) orthocompact.
\end{prop}

\begin{prop}
Orthocompact spaces are countably orthocompact and countably orthocompact [[Lindelöf spaces]] are orthocompact.
\end{prop}
\begin{proof} Follows directly from the fact that every [[open cover]] of a [[Lindelöf space]] has a countable sub-cover.
\end{proof}

\begin{prop}
[[P-spaces]] are countably orthocompact.
\end{prop}
\begin{proof} Follows directly from the fact that _every_ countable [[open cover]] of a [[P-space]] is already inner-preserving.
\end{proof}

([Dontchev 98](#Dontchev98))

\begin{prop}
Spaces with [[Alexandroff topology]] are orthocompact.
\end{prop}
\begin{proof} Follows directly from the fact that _every_ [[open cover]] of a space with [[Alexandroff topology]] is already inner-preserving.
\end{proof}

([Dontchev 98](#Dontchev98))

\begin{theorem}
Given an orthocompact space $X$, the [[product space]] $X\times[0,1]$ is orthocompact iff $X$ is countably [[metacompact]].
\end{theorem}

([Scott 75](#Scott75))

## References

* {#Dontchev98} Julian Dontchev, _Orthocompactness and semi-stratifiability in the density topology_. [arXiv:math/9809069](https://arxiv.org/abs/math/9809069)
* {#Scott75} B. M. Scott, _Towards a product theory for orthocompactness_, "Studies in Topology", N.M. Stavrakas and K.R. Allen, eds (1975), 517–537.

See also:

* Wikipedia, _[Orthocompact space](https://en.wikipedia.org/wiki/Orthocompact_space)_

[[!redirects orthocompact]]
[[!redirects orthocompactness]]
[[!redirects orthocompact spaces]]

[[!redirects countably orthocompact]]
[[!redirects countably orthocompact spaces]]