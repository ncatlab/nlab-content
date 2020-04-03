## Statement

Recall that a [[topological space]] is [[weakly Lindelöf]] if every [[open cover]] has a [[countable set|countable]] subcollection the union of which is dense.

\begin{theorem}
Every [[weakly Lindelöf topological space|weakly Lindelöf]] space with [[countably locally finite set of subsets|$\sigma$-locally finite]] [[topological base|base]] is [[second countable space|second countable]].
\end{theorem}

\begin{proof}
Let $\mathcal{V}$ be a countably locally finite base. For each $x \in X$, there is a neighborhood $N_x$ meeting countably many members of $\mathcal{V}$. If $X$ is weakly Lindelöf, there is a countable $\{N_n\}_n$ which covers a dense subset of $X$. Then $ \mathcal{U} = \{V\in \mathcal{V} \mid N_n \cap V \neq \emptyset\}$ is a countable basis for X.
\end{proof}

## Related statements and properties

[[!include topology - global countability axioms]]