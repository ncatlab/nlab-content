[[!redirects Hausdorff maximality principle]]


The __Hausdorff maximal principle__ is a version of [[Zorn's lemma]], equivalent to the usual version and thus (given [[excluded middle]]) equivalent to the [[axiom of choice]].

## Statement and proofs

Given a [[partial order|poset]] (or [[preorder|proset]]) $S$, let a _chain_ in $S$ be a [[subset]] $A$ of $S$ which, as a sub-proset, is [[total order|totally ordered]].  A chain $A$ is _maximal_ (as a chain) if the only chain that $A$ is contained in is $A$ itself.

+-- {: .un_theorem}
###### Theorem (Hausdorff maximal principle)

Every chain in a proset is contained in a maximal chain.
=--

+-- {: .proof}
###### Proof

We will use [[Zorn's lemma]]. Let $P$ be a proset and let $C \subseteq P$ be a chain. Consider the collection $\mathcal{C}$ of chains in $P$ that contain $C$, ordered by inclusion. If $\{C_\alpha\}_{\alpha \in A} \subseteq \mathcal{C}$ is a family totally ordered by inclusion, then the union $\bigcup_\alpha C_\alpha$, with the order coming from $P$, is also totally ordered: any two elements $x \in C_\alpha, y \in C_\beta$ are comparable in $max(C_\alpha, C_\beta)$. The hypotheses for Zorn's lemma therefore obtain on $\mathcal{C}$, and we conclude that $\mathcal{C}$ has a maximal element, which is clearly maximal in the collection of all chains. 

=--

+-- {: .proof}
###### Proof of converse

Conversely, suppose that the Hausdorff maximal principle holds; we will prove Zorn's lemma. Suppose given a poset (or preorder) $P$ such that every chain in $P$ has an upper bound. Since $\empty$ is a chain, the Hausdorff maximal principle implies that $P$ contains a maximal chain $C$; let $x$ be an upper bound of $C$. Then $x$ is maximal: if $x \leq y$, then $C = C \cup \{y\}$ by maximality of $C$; therefore $y \in C$ and hence $y \leq x$ since $x$ is an upper bound of $C$. 

=--