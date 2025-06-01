
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Two [[morphisms]] in a category $C$ (or just [[edges]] in a [[directed graph]]) are __parallel__ if they have the same [[source]] and [[target]]. Equivalently a pair of __parallel morphisms__ in $C$ consists of an [[object]] $x$, and object $y$, and two morphisms $f, g: x \to y$.

$$
  \array{
    x
      &
      \underoverset
        {\underset{g}{\longrightarrow}}
        {\overset{f}{\longrightarrow}}
        {}
      &
    y
  }
$$

This may be extended to a family of any number of morphisms, but the morphisms are always compared pairwise to see if they are parallel. Degenerate cases: a family of one parallel morphism is simply a morphism; a family of zero parallel morphisms is simply a pair of objects.

## The walking parallel pair

The above considerations can be formalized in the following definition.

\begin{definition}
The __walking parallel pair__ category $P$
has two objects, 0 and 1,
and two nonidentity arrows, $f,g\colon 0\to 1$.
\end{definition}

Now functors $P\to C$ are precisely pairs of parallel morphisms.

## Limits and colimits

The [[limit]] of a pair (or family) or morphisms is called their __[[equalizer]]__; the [[colimit]] is their __[[coequalizer]]__. (Of course, these do not always exist.)

## Related concepts

* [[fork]]

[[!include notions of walking structure]]

[[!include free diagrams -- table]]

[[!redirects parallel morphism]]
[[!redirects parallel morphisms]]
[[!redirects parallel pair of morphisms]]
[[!redirects parallel pairs of morphisms]]

[[!redirects parallel arrow]]
[[!redirects parallel arrows]]
[[!redirects parallel pair of arrows]]
[[!redirects parallel pairs of arrows]]

[[!redirects parallel pair]]
[[!redirects parallel pairs]]

[[!redirects walking parallel pair]]
[[!redirects walking parallel pairs]]

[[!redirects pair of parallel morphisms]]
[[!redirects pairs of parallel morphisms]]

[[!redirects parallel edge]]
[[!redirects parallel edges]]

[[!redirects walking equalizer category]]
[[!redirects walking coequalizer category]]
