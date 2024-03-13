
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

## Statement

Recall that a [[topological space]] is [[weakly Lindelöf topological space|weakly Lindelöf]] if every [[open cover]] has a [[countable set|countable]] subcollection the union of which is dense.

\begin{theorem}
Every [[weakly Lindelöf topological space|weakly Lindelöf]] space with [[countably locally finite set of subsets|$\sigma$-locally finite]] [[topological base|base]] is [[second countable space|second countable]].
\end{theorem}

\begin{proof}
Let $\mathcal{V}$ be a locally finite collection of nonempty open sets. For each $x \in X$, there is a neighborhood $N_x$ meeting finitely many members of $\mathcal{V}$. As $X$ is weakly Lindelöf, there are $x_n$ such that $\{N_{x_n}\}_n$ covers a dense subset of $X$. Then each member of $ \mathcal{V}$ meets some $N_{x_n}$, showing $ \mathcal{V}$ is countable.

Therefore any countably locally finite base in a weakly Lindelöf space is countable, showing the space is second countable.
\end{proof}

## Related statements and properties

[[!include topology - global countability axioms]]

## References
 {#References}

* Steven Clontz, reply to: "Is a $\sigma$-locally finite collection of open sets locally countable?" &lbrack;[MO:a/4878837](https://math.stackexchange.com/a/4878837/58526)&rbrack;

