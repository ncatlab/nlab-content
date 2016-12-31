## Statements and proofs 

The **tube lemma** may refer to one of several fundamental lemmas in topology ([[general topology|point-set topology]] to be more exact[^1]) that underlie many arguments involving [[compact spaces]]. That is to say: much like the [[Yoneda lemma]] of pure [[category theory]], there are various closely related statements that can be said to fall under the rubric "tube lemma"; we consider several examples here. 

[^1]: The use of the phrase "point-set topology" signals that the tube lemma proper does refer to *points*, as opposed to the "point-free" or "pointless" topology as developed in the theory of [[locales]]. Point-free analogues of the main consequences of the tube lemma, such as the fact that the product of two compact topological spaces is again compact, are quite nontrivial and require a significantly different approach. 

* If $X$ is any [[topological space|space]] and $Y$ is compact, then the [[projection map]] $p: X \times Y \to X$ is a [[closed map]], i.e., under [[direct image]] (the [[left adjoint]] $\exists_p: P (X \times Y) \to P(X)$ to the [[inverse image]] map $p^\ast: P(X) \to P(X \times Y)$), [[closed sets]] in $X \times Y$ are mapped to closed sets in $X$. 

Assuming the [[principle of excluded middle]], this statement is equivalent to an alternative formulation: let $\forall_p: P(X \times Y) \to P(X)$ be the [[right adjoint]] to $p^\ast: P(X) \to P(X \times Y)$. (In classical logic, $\forall_p = \neg \exists_p \neg$.) Then 

* If $Y$ is compact, then $\forall_p: P(X \times Y) \to P(X)$ takes [[open sets]] in $X \times Y$ to open sets in $X$. (Compare [[overt space]].) 

This alternative may be proven directly as follows. Let $W \subseteq X \times Y$ be an open set, and suppose $\{x\} \subseteq \forall_p(W)$. This means precisely that $p^\ast\{x\} = \{x\} \times Y \subseteq W$. We are required to show that there is a neighborhood $O$ of $x$ such that $O \subseteq \forall_p(W)$, which is to say $O \times Y \subseteq W$. This $O \times Y$ may be pictured as a little open "tube" around $\{x\} \times Y$ which fits inside $W$, thus explaining the name of the eponymous lemma. 

+-- {: .num_lemma #tube} 
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

For another application, see [[compact-open topology]]. 

## Converse of tube lemma 

As explained above, the three statements 

1. Tube lemma, Lemma \ref{tube}

1. $\forall_p: P(X \times Y) \to P(X)$ preserves openness if $X$ is compact 

1. $\exists_p: P(X \times Y) \to P(X)$ preserves closedness if $X$ is compact 

are virtually tautologically equivalent, and in this sense any one of these forms may be referred to as the tube lemma. In this section, we indicate that the converse of the tube lemma holds, stated as follows. 

+-- {: .num_theorem #converse} 
###### Theorem 
If for all spaces $X$ the projection $p: X \times Y \to X$ is closed (form 3), then $Y$ is compact. 
=-- 

Various proofs may be given. If one likes the characterization of compactness that says every [[ultrafilter]] converges, then a neat conceptual proof runs as follows: given a space $Y$ satisfying the hypothesis, take $X$ to be the [[Stone-Cech compactification]] $\beta Y$ of the discrete space $Y_d$ on the underlying set of $Y$, and let $C \subseteq \beta Y \times Y$ be the convergence relation (i.e., $(U, y)$ belongs to $C$ iff the ultrafilter $U$ converges to $y$). One checks that $C$ is closed. Then the direct image $p(C)$ is closed by hypothesis. Notice also that $p(C)$ contains the set of principal ultrafilters $prin(y)$ ($prin(y)$ converges to $y$ after all), and this set may be identified with the dense set $Y_d \subset \beta Y$. Being closed and dense, $p(C)$ is all of $\beta Y$, but this simply says that every ultrafilter on $Y$ converges, so that $Y$ is compact. 

The characterization of compactness via ultrafilter convergence has a slight drawback of relying on the [[ultrafilter theorem]], a kind of choice principle. If one doesn't like this, there are various workarounds that avoid it, but let it be said that all proofs (some of which are collected [here](#Trim)) have basically the same intuitive character. Given $Y$, one forms a space $X$ by adjoining one or more ideal points to the discrete space $Y_d$, where the open sets around an ideal point correspond to elements of some filter $F$ that we want to show clusters around, or converges to, some point of $y$ (in order to show compactness of $Y$). Just as for the convergence relation in the proof sketched above, one passes to the closure $C$ of the diagonal $Y \to Y_d \times Y \hookrightarrow X \times Y$. The image $p(C)$ is closed and contains the dense subset $Y_d$, and so contains any ideal point $p$, and thus $(p, y) \in C$ for some $y$. This turns out to mean $F$ converges or clusters to $y$, as desired. 

Here is a more precise enactment of one such proof. 

+-- {: .proof} 
###### Proof 
Let $Y$ satisfy the hypothesis of Theorem \ref{converse}; to prove $Y$ is compact, suppose $\mathcal{C}$ is some collection of closed sets such that every finite intersection of elements of $C$ is [[inhabited set|inhabited]]. Let $X = Y_d \sqcup \{\infty\}$, formed by adjoining an ideal point $\infty$ to the discrete space $Y_d$ on the underlying set of $Y$, and stipulating that whenever $C \in \mathcal{C}$, the set $C \sqcup \{\infty\}$ is an open neighborhood of $\infty$. The topology thus generated consists of arbitrary subsets $U \subseteq Y$ together with sets $F \sqcup \{\infty\}$ where $F$ belongs to the filter generated by $\mathcal{C}$. Note that the finite intersection property of $\mathcal{C}$ guarantees that the filter is *proper*, meaning in particular $\infty$ is not an open point, equivalently that the closure of $Y_d$ in $X$ is all of $X$. 

We have a diagonal embedding $Y \stackrel{\Delta}{\to} Y_d \times Y \hookrightarrow X \times Y$; let $C$ be the closure of $Y$ in $X \times Y$. Of course $p(C) \subseteq X$ contains $Y_d$, and is closed by hypothesis, so as we just observed $p(C) = X$. So $\infty \in p(C)$; this means that $(\infty, y) \in C$ for some $y \in Y$. By closure, every neighborhood $(C \sqcup \{\infty\}) \times U$ of $(\infty, y)$ meets $\Delta(Y)$. This just says every open $U \in \mathcal{O}_y$ intersects $C$; since $C$ is closed, this means $y \in C$. Thus 

$$y \in \bigcap_{C \in \mathcal{C}} C$$ 

and the non-emptiness of this intersection proves that $Y$ is compact. 
=-- 

## References

* Wikipedia, _[Tube lemma](https://en.wikipedia.org/wiki/Tube_lemma)_ 

* [[Todd Trimble]], *Characterizations of compactness*, [nLab link](https://ncatlab.org/toddtrimble/published/Characterizations+of+compactness). 