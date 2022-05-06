## Statement

Recall that a [[topological space]] $X$ is [[paracompact space|paracompact]] if every [[open cover]] has a [[refinement]] by a [[locally finite open cover]]. Further a space is called [[Lindelöf topological space|Lindelöf]] if every [[open cover]] has a [[countable cover|countable]] sub-cover. 

\begin{theorem}
Assuming the [[axiom of choice]]:

Every paracompact space $X$ satisfying the countable chain condition is Lindelöf.
\end{theorem}

\begin{proof}
The proof goes by contradiction: Assume there is an open cover $\{U_i\}_{i\in I}$ with no countable subcover. Let $\{U_j\}_{j\in J}$ be a locally finite refinement, which again must not be countable. This is to say that each point possesses an open neighborhood so small that it is only an element of finitely many $U_j$'s. Inductively (using [[Zorn's lemma]]) construct a maximal system $\{V_\lambda\}_{\lambda \in \Lambda}$ of pairwise disjoint opens being contained in at most finitely many $U_j$'s. Due to maximality $\bigcup_{\lambda\in\Lambda} V_\lambda$ is dense. This fact implies by the countable chain condition that $\Lambda$ is countable. Moreover it implies that each $U_j$ intersects at least one $V_\lambda$. But this is to say that there are at most countably many $U_j$'s. This is a contradiction.
\end{proof}
  
## Related statements and properties

[[!include topology - global countability axioms]]