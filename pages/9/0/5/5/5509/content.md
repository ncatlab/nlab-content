

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

## Definition


+-- {: .un_defn}
###### Definition

A [[paracompact topological space]] $X$ has **covering dimension** $\leq n \in \mathbb{N}$ if for every [[open cover]] $\{U_i \to X\}$ there exists an open refinement $\{V_i \to X\}$, such that each $(n+1)$-fold intersection of pairwise distinct $V_i$ is empty

$$
 V_{i_1} \cap \cdots \cap V_{i_{n+1}} = \emptyset
  \,.
$$


=--

## Properties

\begin{theorem}

If the [[paracompact topological space]] $X$ has covering dimension $\leq n$, then the [[(∞,1)-category of (∞,1)-sheaves]] $Sh_{(\infty,1)}(X) := Sh_{(\infty,11)}(Op(X))$ is an [[(∞,1)-topos]] of [[homotopy dimension]] $\leq n$.

\end{theorem}

This is [[Higher Topos Theory|HTT, theorem 7.2.3.6]].

\begin{remark}
  For [[separable metric spaces]] the notion of covering dimension is particularly well-behaved. See [there](separable+metric+space#PropertiesDimension).
\end{remark}

## Related concepts

[[!include notions of dimension -- contents]]




[[!redirects covering dimensions]]