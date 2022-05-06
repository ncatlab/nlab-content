
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea and definition

Condensed sets aim to provide a convenient setting
in the framework of [[homotopical algebra]] for working with algebraic objects that have some sort of a [[topological space|topology]] on them.

\begin{definition}
A _condensed set_ is a [[sheaf]] of sets on the [[pro-étale site]] of a point.
That is, a condensed set is a functor
$$ProfiniteSet^op \to Set$$
such that the natural map
$$T(S\sqcup S')\to T(S)\times T(S')$$
is a bijection for any [[profinite sets]] $S$ and $S'$,
whereas the natural map
$$T(S)\to T(S')\rightrightarrows T(S'\times_S S')$$
is a bijection for any surjection of [[profinite sets]] $S'\to S$.
\end{definition}

## Related concepts

* [[pyknotic set]]

* [[pro-étale site]]

* [[profinite set]]

## References

* [[Peter Scholze]], _Lectures on condensed mathematics_, [PDF](https://www.math.uni-bonn.de/people/scholze/Condensed.pdf)

[[!redirects condensed sets]]
[[!redirects condensed object]]
[[!redirects condensed objects]]
