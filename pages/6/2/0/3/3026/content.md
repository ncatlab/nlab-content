
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _one-point compactification_ of a [[topological space]] is a new [[compact space]] obtained by adding a single new point to the original space.

This is also known as the _Alexandroff compactification_ or _Alexandroff extension_ after a 1924 paper by [[Pavel Aleksandrov|Павел Сергеевич Александров]] (then transliterated 'P.S. Aleksandroff').

## Definition

Let $X$ be a [[compact space|non-compact]] but [[locally compact space|locally compact]] [[Hausdorff space]]. Its **one-point compactification** $X^*$ is the topological space 

* whose underlying [[set]] is $X \cup \{\infty\}$ 

* and whose [[open set]]s are 

  1. the open subsets of $U$;

  1. subsets $V$ that contain $\infty$ such that $X \setminus V$ is closed and [[compact space|compact]].


## Properties

$X^*$ is [[compact space|compact]].


The evident inclusion $X \to X^*$ is an open [[embedding]].


The one-point compactification is [[universal property|universal]] among all compact spaces into which $X$ has an open embedding, so it is [[essentially unique]].

$X^*$ is technically a [[compactification]] of $X$ (meaning that $X$ is [[dense subspace|dense]] in $X^*$) only if $X$ was not already compact.  $X^*$ is [[Hausdorff space|Hausdorff]] (hence a [[compactum]]) if and only if $X$ was already both Hausdorff and [[locally compact space|locally compact]].


## References

* John Kelly, _General Topology_ (1975)


[[!redirects Alexandroff compactification]]
[[!redirects Alexandrov compactification]]
[[!redirects Aleksandrov compactification]]
[[!redirects Александров compactification]]
[[!redirects one-point extension]]
[[!redirects Alexandroff extension]]
[[!redirects Alexandrov extension]]
[[!redirects Aleksandrov extension]]
[[!redirects Александров extension]]