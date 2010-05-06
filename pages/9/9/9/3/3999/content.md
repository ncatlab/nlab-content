# Idea #

[[compact space|Compactness]] is an extremely useful concept in [[topology]].  The basic idea is that a topological space is compact if it isn't "fuzzy around the edges".

Whilst one can study a topological space by itself, it is often useful to probe it with known spaces.  A common choice for topological spaces, and in particular metric spaces, is to use the natural numbers, and the 1-point compactification of the natural numbers.  This is more traditionally known as studying the topology using sequences and convergent sequences.

Thus one can ask, "Can I detect compactness using probes from $\mathbb{N}$, and $\mathbb{N} \cup \{*\}$?".  The short answer to this is "No", but that just reveals that the question was too restrictive.  Rather, one should ask "What does compactness look like if all I'm allowed to use are probes from $\mathbb{N}$ and $\mathbb{N} \cup \{*\}$?".  The answer to that question is "sequential compactness".

Thus **sequential compactness** is what [[compact space|compactness]] looks like if all one has to test it are sequences.

# Definition #

+-- {: .num_defn #seqcpt}
###### Definition ######
A topological space is **sequentially compact** if every [[sequence]] in it has a [[convergence|convergent]] [[subsequence]].
=--

# Properties #

The following is a list of properties of and pertaining to sequentially compact spaces.

1. Every [[compact space]] is sequentially compact.  The converse is true if the space has a countable base at each point.
2. In particular, for a metric space, the notions of sequential compactness and compactness coincide.
3. A topological space $X$ is sequentially compact if and only if $\mathbb{R} \times X$ has the _tube property_.  That is, that a neighbourhood of $\{0\} \times X$ necessarily contains a subset of the form $(-\epsilon, \epsilon) \times X$.