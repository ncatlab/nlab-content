
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

\tableofcontents

## Idea

A notion of [[topological space]] which comes with predefined notions of [[neighbourhood]], [[point-set apartness]], and nearness, without having to define any of them in terms of the others. 

## Definition

A **unified topological space** is a [[set]] $A$ with a **unified topology** - three [[relations]] $\ll$, $\bowtie$, and $\approx$ between $A$ and its [[power set]] $\mathcal{P}(A)$, such that for all elements $x$ of $A$ and subsets $U$ and $V$ of $A$, 

* $\ll$ is a [[topological space|topology]] in the usual sense: 

  * if $x \ll U$, then $x \in U$

  * if $x \ll U$ and $U \subseteq V$, then $x \ll V$

  * $x \ll A$

  * if $x \ll U$ and $x \ll V$, then $x \ll U \cap V$

  * if $x \ll U$, then $x \ll \{y \in A \vert y \ll U\}$

* $\bowtie$ is a [[point-set apartness space|point-set apartness]] in the usual sense: 

  * if $x \bowtie U$, then $x \in U$ is false

  * if $x \bowtie U$ and $U \subseteq V$, then $x \bowtie V$

  * $x \bowtie \emptyset$

  * if $x \bowtie U$ and $x \bowtie V$, then $x \bowtie U \cup V$

  * if $x \bowtie U$, then $x \bowtie \{y \in A \vert y \approx U\}$

* $\approx$ satisfies the following closure space axioms:  

  * if $x \in U$, then $x \approx U$

  * if $x \approx U$ and $U \subseteq V$, then $x \approx V$

  * $x \approx \emptyset$ is false

  * if $x \approx U \cup V$ and $x \approx U$, then $x \approx V$

  * if $x \approx \{y \in A \vert y \approx U\}$, then $x \approx U$

* The following compatibility condition holds:

  * if $x \ll U$ and $x \approx V$, then there exists an element $y$ of $A$ such that $y \in U \cap V$. 

## Related concepts

* [[topological space]]

* [[point-set apartness space]]

* [[antithesis interpretation]]

## References

Unified topologies were defined in definition 10.17 of:

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518).

[[!redirects unified topological space]]
[[!redirects unified topological spaces]]

[[!redirects unified topology]]
[[!redirects unified topologies]]