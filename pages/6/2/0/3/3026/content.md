
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

The _one-point compactification_ of a [[topological space]] is a new [[compact space]] obtained by adding a single new point to the original space.

This is also known as the _Alexandroff compactification_ after a 1924 paper by [[Pavel Aleksandrov|Павел Сергеевич Александров]] (then transliterated 'P.S. Aleksandroff').

The one-point compactification is usually applied to a non-[[compact space|compact]] [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]] space.  In the more general situation, it may not really be a [[compactification]] and hence is called the _one-point extension_ or _Alexandroff extension_.


## Definition

Let $X$ be any [[topological space]]. Its **one-point extension** $X^*$ is the topological space 

* whose underlying [[set]] is the [[disjoint union]] $X \cup \{\infty\}$ 

* and whose [[open set]]s are 

  1. the open subsets of $X$ (thought of as subsets of $X^*$);

  1. the [[complements]] (in $X^*$) of the [[closed subspace|closed]] [[compact space|compact]] subsets of $X$.

(If $X$ is [[Hausdorff space|Hausdorff]], then its compact subsets must always be closed, so (2) is often given in a simpler form.)


## Properties

$X^*$ is [[compact space|compact]].

The evident inclusion $X \to X^*$ is an [[open map|open]] [[embedding]].

The one-point compactification is [[universal property|universal]] among all compact spaces into which $X$ has an open embedding, so it is [[essentially unique]].

$X$ is [[dense subspace|dense]] in $X^*$ iff $X$ is not already compact.  Note that $X^*$ is technically a [[compactification]] of $X$ only in this case.

$X^*$ is [[Hausdorff space|Hausdorff]] (hence a [[compactum]]) if and only if $X$ is already both Hausdorff and [[locally compact space|locally compact]].


## References

* John Kelly, _General Topology_ (1975)


[[!redirects one-point compactification]]
[[!redirects one-point compactifications]]
[[!redirects Alexandroff compactification]]
[[!redirects Alexandroff compactifications]]
[[!redirects Alexandrov compactification]]
[[!redirects Alexandrov compactifications]]
[[!redirects Aleksandrov compactification]]
[[!redirects Aleksandrov compactifications]]
[[!redirects Александров compactification]]
[[!redirects Александров compactifications]]

[[!redirects one-point extension]]
[[!redirects one-point extensions]]
[[!redirects Alexandroff extension]]
[[!redirects Alexandroff extensions]]
[[!redirects Alexandrov extension]]
[[!redirects Alexandrov extensions]]
[[!redirects Aleksandrov extension]]
[[!redirects Aleksandrov extensions]]
[[!redirects Александров extension]]
[[!redirects Александров extensions]]
