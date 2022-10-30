The **basis theorem** for [[vector space]]s states that every vector space $V$ admits a basis, or in other words is a free module over its ground field of scalars. It is a famous classical consequence of the axiom of choice (and is equivalent to it by a result of Andreas Blass, proved in 1984). 

## Statement and proofs

+-- {: .un_theorem}
###### Basis theorem

If $V$ is a [[vector space]] over any [[field]] $K$, then $V$ has a basis.
=--

+-- {: .proof}
###### Proof

We apply [[Zorn's lemma]] as follows: consider the poset consisting of the linearly independent subsets of $V$, ordered by inclusion (so $S \leq S'$ if and only if $S \subseteq S'$). If $(S_\alpha)$ is a chain in the poset, then 

$$S = \bigcup_\alpha S_\alpha$$ 

is an upper bound, for each $v$ in the span of $S$ belongs to some $S_\alpha$ and is uniquely expressible as a finite linear combination of elements in $S_\alpha$ and in any $S_\beta$ containing $S_\alpha$, hence uniquely expressible as a finite linear combination of elements in $S$. Thus the hypothesis of Zorn's lemma obtains for this poset; therefore this poset has a maximal element, say $B$. 

Let $W$ be the span of $B$.  If $W$ were a proper subspace of $V$, then for any $v$ in the set-theoretic complement of $W$, $B \cup \{v\}$ is a linearly independent set (for if 

$$a_0 v + a_1 w_1 + \ldots + a_n w_n = 0 \qquad (w_1, \ldots, w_n \in B)$$ 

we must have $a_0 = 0$ -- else we can multiply by $1/a_0$ and express $v$ as a linear combination of the $w_i$, contradicting $\neg(v \in W)$ -- and then the remaining $a_i$ are 0 since the $w_i$ are linearly independent). This contradicts the maximality of $B$. We therefore conclude that $W = V$, and $B$ is a basis for $V$. 
=--

I'll write out a proof of the converse, that the axiom of choice follows from the basis theorem, as soon as I've digested it -- Todd. 

## Generalisations

Given any linearly independent set $A$ and spanning set $C$, if $A \subseteq C$, then there is a basis $B$ with $A \subseteq B \subseteq C$; the theorem above is the special case where $A = \empty$ and $C = V$.  The proof of this more general theorem is a straightforward generalisation of the proof above.