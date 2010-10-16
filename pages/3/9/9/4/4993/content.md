This page is dedicated to proving the equivalence of two notions of compactness, one being the classical open-cover formulation, and the other a "stable closure" condition (the property that "$X \to 1$ is a closed map" is stable under pullback). 

## Compactness implies stable closure

One direction is a very classical and straightforward fact, proved in every textbook on general topology. 

+-- {: .un_prop}
######Proposition 
If $X$ is compact, then for any space $Y$ the projection $\pi: X \times Y \to Y$ is a closed map. 
=-- 

+-- {: .proof}
######Proof
Let $C \subseteq X \times Y$ be a closed subset, and suppose that $y$ does not belong to $\pi(C)$. We want to find an open neighborhood of $y$ that does not intersect $\pi(C)$, or so that $X \times V$ does not intersect $C$. Consider the collection $\mathcal{C}$ of all open $U \subseteq X$ for which there exists an open $V \subseteq Y$ containing $y$, such that $U \times V$ does not intersect $C$. Since $y \notin \pi(C)$, for any $x \in X$ we have $(x,y) \notin C$, and since $C$ is closed in the product topology, there exist $V$ containing $y$ and $U$ containing $x$ such that $U \times V$ does not intersect $C$. Therefore, $\mathcal{C}$ covers $X$, so it has a finite subcover $U_i$. For each of the finitely many $i$ there is a corresponding $V_i$ such that $U_i \times V_i$ does not intersect $C$, and the intersection of the $V_i$ is a neighborhood of $y$ which does not intersect $\pi(C)$.
=--

## Stable closure implies compactness

The converse statement requires more ingenuity to prove. A preliminary observation is that the proof above was a bit convoluted because it was phrased throughout in terms of complements of closed sets; this suggests it would be convenient to reformulate the condition of being a closed map directly in terms of _open_ sets: 

+-- {: .un_prop} 
######Proposition 
A map $f: X \to Y$ is closed iff $\forall_f U$ is open in $Y$ for every open $U$ in $X$. Here $\forall_f U$ is defined by the adjunction condition 
$$f^{-1}(B) \subseteq U \qquad iff \qquad B \subseteq \forall_f U$$
for every $B \subseteq Y$. 
=-- 

+-- {: .proof}
######Proof
The traditional formulation is that $\exists_f C$ is closed in $Y$ whenever $C$ is closed in $X$, which is the same as that $\exists_f \neg U = \neg \forall_f U$ is closed in $Y$ whenever $U$ is open in $X$, i.e., $\forall_f U$ is open in $Y$ whenever $U$ is open in $X$. 
=-- 

In the case of a projection map $f = \pi: X \times Y \to Y$, this says 

$$\{y \in Y: X \times \{y\} \subseteq U\}$$ 

is open in $Y$ whenever $U$ is open in $X \times Y$. 

Next, a slight reformulation of the concept of compactness. Recall that a collection of subsets of $X$ is _directed_ if every finite subcollection has an upper bound. Then, a space $X$ is compact if every directed open cover $\Sigma$ of $X$ contains $X$. 

+-- {: .un_thm} 
######Theorem 
If $\pi: X \times Y \to Y$ is a closed map for every space $Y$, then $X$ is compact. 
=-- 

+-- {: .proof}
######Proof 
Let $\Sigma$ be a directed open cover of $X$. Define a space $Y$ as follows: the points of $Y$ are open sets of $X$ (so the underlying set of $Y$ is the topology $\mathcal{O}(X)$), and the open sets of $Y$ are upward-closed subsets $W$ of $\mathcal{O}(X)$ such that $\Sigma \cap W$ is nonempty whenever $W$ is nonempty. 

**Claim:** this is a topology. **Proof:** Clearly such $W$ are closed under arbitrary unions. If $W$ and $W'$ are open and $U \in \Sigma \cap W$ and $U' \in \Sigma \cap W'$, then any upper bound of $U$ and $U'$ in $\Sigma$ belongs to both $W$ and $W'$ since these are upward-closed. 

Moreover, whenever $U$ belongs to $\Sigma$, the principal up-set $prin(U) = \{V \in \mathcal{O}(X): U \subseteq V$ is open in $Y$. 

Now consider the set $E = \{(x, U) \in X \times Y: x \in U\}$. Claim: this is open in $X \times Y$. Proof: for every $(x, U) \in E$, there exists $U' \in \Sigma$ such that $x \in U'$ (because $\Sigma$ is a cover), and then for $U'' = U \cap U'$, the set $U'' \times prin(U'')$ is an open set which contains $(x, U)$, and $U \times prin(U) \subseteq E$ because for every $(y, V) \in U'' \times prin(U'')$, we have $y \in V$. 

By the open-set reformulation of the closed map condition, the set 
$$\{V \in Y: X \times \{V\} \subseteq E\}$$ 
is open in $Y$, so this set is upward-closed and intersects $\Sigma$, so that $X \times \{V\} \subseteq E$ for some $V \in \Sigma$. But then $V$ is all of $X$! So $X \in \Sigma$ for any directed open cover $\Sigma$; therefore $X$ is compact. 
=--

## Reference

The proof of the theorem above was extracted from 

* Martin Escardo, Intersections of compactly many open sets are open, 2009 [(pdf)](http://www.cs.bham.ac.uk/~mhe/papers/compactness-submitted.pdf)

See also [this exchange](http://mathoverflow.net/questions/42186/does-compact-iff-projections-are-closed-require-some-form-of-choice) at Math Overflow, where the question was raised as to whether the axiom of choice (or possibly a weaker choice principle like the [[ultrafilter theorem]]) is required to prove the equivalence of these two notions of compactness (examination of the proofs above show it is not). 
