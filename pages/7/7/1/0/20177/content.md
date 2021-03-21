
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _[[dimension]]_ of a [[cell complex]] $X$ is the largest [[natural number]] $n \in \mathbb{N}$, if such exists, for which there are non-trivial $n$-[[cells]] in $X$. If there is no such largest $n$ the dimension is also said to be _[[infinity|infinite]]_.


## Definition

Specifically, if $X$ is a [[CW-complex]]

$$
  X \;\simeq\; \underset{\longrightarrow_{\mathrlap{n}}}{\lim} X_n
$$

where each $X_n$ is a [[pushout]] of the form

$$
  \array{
    \underset{ i \in I_n }{\sqcup} S^{n-1}
    &\longrightarrow&
    X_{n-1}
    \\
    \big\downarrow &(po)& \big\downarrow
    \\
    \underset{ i \in I_n }{\sqcup} D^{n}    
    &\longrightarrow&
    X_n
  }
$$

the dimension of $X$ is the largest $n$ for which the indexing sets $I_n$ are [[inhabited set|non-empty]].

## Related concepts

[[!include notions of dimension -- contents]]




[[!redirects dimension of cell complexes]]

[[!redirects dimension of a CW-complex]]
[[!redirects dimension of CW-complexes]]

[[!redirects dimension of a CW complex]]
[[!redirects dimension of CW complexes]]






