+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

## Statement

\begin{theorem}
Using [[countable choice]], then:
Every [[second-countable space|second-countable]] [[topological space]] $X$ is [[Lindelöf space|Lindelöf]], i.e. any open cover admits a countable subcover.
\end{theorem}

\begin{proof}
Let $\{U_n\}$ be a countable base of the topology.
Given any open cover $\{V_\lambda\}$ of $X$, we can form the index set $I\subset \mathbb{N}$ of those $U_n$ that are contained in some $V_\lambda$.
By assumption $\bigcup_{i\in I} U_{i} = \bigcup_\lambda V_\lambda = X$.
The axiom of [[countable choice]] provides now a section of $\bigsqcup_{i\in I} \{\lambda \mid U_i \subset V_\lambda\}\to I$.
\end{proof}

## Related properties

[[!include topology - global countability axioms]]
