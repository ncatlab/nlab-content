+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Enriched category theory
+-- {: .hide}
[[!include enriched category theory contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A **lax extranatural transformation** is to a [[lax transformation]] as an [[extranatural transformation]] is to a [[natural transformation]].

## Definition

Let $\mathcal{A}$, $\mathcal{B}$, $\mathcal{C}$, and $\mathcal{D}$ be bicategories and $P\colon\mathcal{A}\times\mathcal{B}^\mathsf{op}\times\mathcal{B}\to\mathcal{D}$ and $Q\colon\mathcal{A}\times\mathcal{C}^\mathsf{op}\times\mathcal{C}\to\mathcal{D}$ be pseudofunctors (we are going to use the invertibility of their lax functoriality constraints below). The following is [ [Corner 2017, Definition 2.2] ](#Corner), but laxified:

+-- {: .num_defn}
###### Definition

A **lax extranatural transformation** $P\overset{\bullet}{\Rightarrow}Q$ from $P$ to $Q$ consists of

1. _Components._ For each $A\in\mathrm{Obj}(\mathcal{B}$ and each $C\in\mathrm{Obj}(C)$, a lax transformation
   $$\alpha_{(-),B,C}\colon P^B_{(-),B}\Rightarrow Q^{C}_{(-),C},$$
   called the **component** of $\alpha$ at $(B,C)$.

2. _Lax Extranaturality Constraints I._ For each $1$-morphism $g\colon B\longrightarrow B'$ of $\mathcal{B}$, a $2$-morphism
   $$\alpha_{g}\colon\alpha_{A,B',C}\circ P^{\mathsf{id}_{B'}}_{\mathsf{id}_{A},g}\Rightarrow\alpha_{A,B,C}\circ P^{g}_{\mathsf{id}_{A},\mathsf{id}_{B}}$$
   of $\mathcal{D}$ as in the diagram
   
   \begin{imagefromfile}
       "file_name": "lax_extranaturality_1.svg",
       "width":     "250"
   \end{imagefromfile}

   called the **lax extranaturality constraint of $\alpha$ at $g$**.

3. _Lax Extranaturality Constraints II._ For each $1$-morphism $h\colon C\longrightarrow C'$ of $\mathcal{D}$, a $2$-morphism
   $$\alpha_{h}\colon Q^{\biid_{C}}_{\biid_{A},h}\circ\alpha_{A,B,C}\Rightarrow Q^{h}_{\biid_{A},\biid_{C'}}\circ\alpha_{A,B,C'}$$
   of $\mathcal{D}$ as in the diagram

   \begin{imagefromfile}
       "file_name": "lax_extranaturality_2.svg",
       "width":     "250"
   \end{imagefromfile}

   called the **lax extranaturality constraint of $\alpha$ at $h$**.

【...】

=--

## References

* {#Corner} Alexander Corner, _A Universal Characterisation of Codescent Objects_ ([arXiv](http://arxiv.org/abs/1709.01332)).