+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context###
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Definition ##

A **compact connected space** is a space $S$, such as a [[topological space]] or a [[0-truncated]] [[cohesive infinity-groupoid]], such that for [[subspaces]] $A \subseteq S$ and $B \subseteq S$ of $S$ with [[embeddings]] $i_{A,S}:A \hookrightarrow S$ and $i_{B,S}:B \hookrightarrow S$ such that the embedding $i_{A \cup B,S}:A \cup B \hookrightarrow S$ is an [[equivalence in homotopy type theory|equivalence]] $(i_{A \cup B,S}:A \cup B \simeq S)$ and the embedding $i_{\emptyset,A \cap B}:\emptyset \hookrightarrow A \cap B$ is an equivalence $(i_{\emptyset,A \cap B}:\emptyset \simeq A \cap B)$, either $i_{A,S}$ is an equivalence ($i_{A,S}:A \simeq S$) or $i_{B,S}$ is an equivalence ($i_{B,S}:B \simeq S$). 

## Examples ##

* In [[constructive mathematics]], the [[Dedekind real numbers]] are a compact connected space. 

## See also ##

* [[compact space]]

* [[connected space]]

## References ##

* [[Paul Taylor]], (2010). “A lambda calculus for real analysis”. In: Journal of Logic &
Analysis 2.5, pp. 1–115 (cit. on pp. 4, 71–72).
* [[Mike Shulman]], Brouwer’s fixed-point theorem in real-cohesive homotopy type theory, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

[[!redirects compact connected spaces]]