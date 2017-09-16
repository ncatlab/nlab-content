The **basis theorem** for [[vector space]]s states that every vector space $V$ admits a basis, or in other words is a free module over its ground field of scalars. It is a famous classical consequence of the axiom of choice (and is equivalent to it by a result of Andreas Blass, proved in 1984). 

**Proof**: We apply [[Zorn's lemma]] as follows: consider the poset consisting of pairs $(U, S_U)$ where $U \subseteq V$ is a vector subspace and $S_U \subseteq U$ is a basis for $U$, ordered by inclusion of pairs (so $(U, S_U) \leq (U', S_{U'})$ if and only if $S_U \subseteq S_{U'}$). If $(U_\alpha, S_{U_\alpha})$ is a chain in the poset, then 

$$(U, S_U) = (\bigcup_\alpha U_\alpha, \bigcup_\alpha S_{U_\alpha})$$ 

is an upper bound, for each $v \in U$ belongs to some $U_\alpha$ and is uniquely expressible as a finite linear combination of elements in $S_\alpha$ and in any $S_\beta$ containing $S_\alpha$, hence uniquely expressible as a finite linear combination of elements in $S$. Thus the hypothesis of Zorn's lemma obtains for this poset; therefore this poset has a maximal element, say $(W, S_W)$. 

If $W$ were a proper subspace of $V$, then for any $v$ in the set-theoretic complement of $W$, $S_W \cup \{v\}$ is a linearly independent set (for if 

$$a_1 v + a_2 w_1 + \ldots + a_n w_n = 0 \qquad (w_1, \ldots, w_n \in S_W)$$ 

we must have $a_1 = 0$ -- else we can multiply by $1/a_1$ and express $v$ as a linear combination of the $w_i$, contradicting $\neg(v \in W)$ -- and then the remaining $a_i$ are 0 since the $w_i$ are linearly independent). The span of $S_W \cup \{v\}$ now strictly contains $W$ and has $S_W \cup \{v\}$ as basis; this contradicts the maximality of $(W, S_W)$. We therefore conclude that $W = V$, and $S_W$ is a basis for $V$. 

Anybody know how to prove the converse: that the axiom of choice follows from the basis theorem? 

