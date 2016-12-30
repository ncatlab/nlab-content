## Statements and proofs 

The **tube lemma** refers to one of several fundamental lemmas in topology (point-set topology to be more exact[^1]) that underlies many arguments involving [[compact spaces]]. Much like the [[Yoneda lemma]] of pure [[category theory]], there are various closely related statements that can be said to fall under the rubric "tube lemma"; we consider several examples here. 

[^1]: The use of the phrase "point-set topology" signals that the tube lemma proper does refer to *points*, as opposed to the "point-free" or "pointless" topology as developed in the theory of [[locales]]. Point-free analogues of the main consequences of the tube lemma, such as the fact that the product of two compact topological spaces is again compact, are quite nontrivial and require a significantly different approach. 

One such statement is as follows. 

* If $X$ is any [[topological space|space]] and $Y$ is compact, then the [[projection map]] $p: X \times Y \to X$ is a [[closed map]], i.e., the left adjoint $\exists_p: P (X \times Y) \to P(X)$ to the [[inverse image]] map $p^\ast: P(X) \to P(X \times Y)$ takes [[closed sets]] in $X \times Y$ to closed sets in $X$. 

Assuming the [[principle of excluded middle]], this statement is equivalent to an alternative formulation: let $\forall_p: P(X \times Y) \to P(X)$ be the right adjoint to $p^\ast: P(X) \to P(X \times Y)$. (In classical logic, $\forall_p = \neg \exists_p \neg$.) Then 

* If $Y$ is compact, then $\forall_p: P(X \times Y) \to P(X)$ takes [[open sets]] in $X \times Y$ to open sets in $X$. (Compare [[overt space]].) 

This alternative may be proven directly as follows. Let $W \subseteq X \times Y$ be an open set, and suppose $\{x\} \subseteq \forall_p(W)$. This means precisely that $p^\ast\{x\} = \{x\} \times Y \subseteq W$. We are required to show that there is a neighborhood $O$ of $x$ such that $O \subseteq \forall_p(W)$, which is to say $O \times Y \subseteq W$. This $O \times Y$ may be pictured as a little open "tube" around $\{x\} \times Y$ which fits inside $W$, thus explaining the name of the eponymous lemma. 

+-- {: .num_lemma} 
###### Lemma 
**(Tube lemma)** 
Let $X$ be a space and let $Y$ be compact. For a point $x \in X$ and $W$ open in $X \times Y$, if $\{x\} \times Y \subseteq W$, then there is an open neighborhood $O$ of $x$ such that $O \times Y \subseteq W$. 
=-- 

+-- {: .proof} 
###### Proof 
Let $\mathcal{O}_x$ denote the set of open neighborhoods of $x$, and for $U \in \mathcal{O}_x$, let $U\multimap W$ be the largest open $V$ of $Y$ such that $U \times V \subseteq W$. The collection $\{U \multimap W: U \in \mathcal{O}_x\}$ is an open cover of $Y$; since $Y$ is compact, there is a finite subcover $U_1 \multimap W, U_2 \multimap W, \ldots, U_n \multimap W$. Then $O = U_1 \cap \ldots \cap U_n \in \mathcal{O}_x$ is the desired open. For, $O \subseteq U_i$ implies $(U_i \multimap W) \subseteq (O \multimap W)$, so that 

$$Y = \bigcup_{i=1}^n (U_i \multimap W) \subseteq O \multimap W$$ 

and this implies $O \times Y \subseteq O \times (O \multimap W) \subseteq W$. 
=-- 

+-- {: .num_cor} 
###### Corollary 
The topological product $X \times Y$ of two compact spaces $X, Y$ is compact. 
=-- 

+-- {: .proof} 
###### Proof 
Let $\mathcal{U}$ be any open cover of $X \times Y$, and let $\mathcal{B}$ be the collection of opens of $X \times Y$ that are unions of finitely many elements of $\mathcal{U}$. For each $x \in X$, we have that $\{x\} \times Y$ is compact since $Y$ is, so there is $B \in \mathcal{B}$ such that $\{x\} \times Y \subseteq B$, whence there is $U \in \mathcal{O}_x$ with $U \times Y \subseteq B$ by the tube lemma. 

It follows that the collection 

$$\{U\; open\; in\; X: U \times Y \subseteq B \; for\; some\; B \in \mathcal{B}\}$$ 

covers $X$, whence by compactness of $X$ there is a finite subcover $U_1, \ldots, U_n$ for which $U_i \times Y \subseteq B_i$ for some $B_i \in \mathcal{B}$, and then $B = B_1 \cup \ldots \cup B_n$ belongs to $\mathcal{B}$ and is all of $X \times Y$. 
=-- 


## References

* Wikipedia, _[Tube lemma](https://en.wikipedia.org/wiki/Tube_lemma)_