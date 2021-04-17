
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[group theory]] a  *transposition* is a [[permutation]] that exchanges two elements and leaves all others fixed.


## Definition

For $n \in \mathbb{N}$ and $1 \leq i \neq j \leq n$, the *transposition* of $i$ with $j$ among $\{1,\cdots, n\}$ is the [[permutation]]

$$
  \array{
    \{1, \cdots, n\}
    &
    \underoverset{\simeq}{\;\;\; \sigma_{i,j} \;\;\; }{\longrightarrow}
    &
    \{1, \cdots, n\}
    \\
    k 
    &\mapsto&
    \left\{
    \array{
       k &\vert& k \notin \{i,j\}
       \\
       j &\vert& k = i
       \\
       i &\vert& k = j
    }
    \right.
  }
$$


## Properties

* Transpositions are [[generators]] for the [[symmetric group]], exhibiting it as a [[finitely generated group]].

* In fact already just the *adjacent transpositions* $t_{i , i+1}$ for $1 \leq i \leq n$ generate the symmetric group, see at *[[Kendall tau distance]]*.

## Related concepts

* [[permutation representation]], [[permutation matrix]]

* [[cyclic permutation]], [[rotation permutation]]


[[!redirects transposition permutations]]

[[!redirects transposition]]
[[!redirects transpositions]]



