
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


# Contents 
* table of contents 
{:toc} 

## Statement and proof 

There are a number of [[category theory|categorically-flavored]] ways of characterizing [[compact spaces]]; for example, as [[relational beta-modules]] $X$ where the beta-module structure $\xi: \beta(X) \nrightarrow X$ is an [[entire relation]] (satisfies $1_{\beta(X)} \leq \xi^\circ \xi$). One of the more useful characterizations, as emphasized by [[Walter Tholen]], is given by the following elementary statement (also one of the definitions listed in [[compact space]]): 

+-- {: .num_theorem #char} 
###### Theorem 
A [[topological space]] $X$ is [[compact topological space|compact]] if and only if for every space $Y$, the [[projection map]] $\pi \colon Y \times X \to Y$ out of the [[product topological space]] is a [[closed map]]. 
=-- 

In this article we will collect a number of proofs and points of view on this result, and show how it makes possible a very direct hands-on proof of the [[Tychonoff theorem]], without the need for infrastructure such as [[ultrafilters]] or [[nets]]. This type of proof may be adapted for use in undergraduate classrooms. 

The "only if" half is covered in essentially every textbook and should be routine for any working mathematician, although it seems proofs often use needlessly many indices and look as though they tacitly invoke the [[axiom of choice]]. Our proof should help circumvent that impression. 

+-- {: .num_prop #onlyif} 
###### Proposition 

If $X, Y$ are [[topological spaces]] with $X$ [[compact topological space|compact]], then the [[projection map]] $\pi \colon Y \times X \to Y$ out of the [[product topological space]] is a [[closed map]]. 

=-- 

+-- {: .proof} 
###### Proof 
Let $C \subseteq Y \times X$ be a [[closed subset]]; we must show the [[direct image]] $\pi(C)$ is closed in $Y$. Suppose $y \notin \pi(C)$; equivalently, suppose that the [[pre-image]] $\pi^{-1}(y) = \{y\} \times X$ does not intersect $C$. By the nature of closed subsets ([this lemma](Introduction+to+Topology+--+1#UnionOfOpensGivesClosure)) it is sufficient that we find an [[open neighborhood]] $V$ of $y$ that does not [[intersection|intersect]] $\pi(C)$, or equivalently such that $(V \times X) \cap C = \emptyset$. Consider the collection of all open $U \subseteq X$ such that $(W \times U) \cap C = \emptyset$ for some [[open neighborhood]] $W$ of $y$. This collection [[open cover|covers]] $X$, since $(y, x) \notin C$ for every $x \in X$ and by closure of $C$ we can therefore find a neighborhood $W \times U$ of $(y, x)$ that doesn't intersect $C$. By compactness of $X$, this [[open cover]] has a [[finite cover|finite]] subcover, say $U_1, \ldots, U_n$. For each of these $U_i$ there is a corresponding $W_i$ such that $(W_i \times U_i) \cap C = \emptyset$ (in fact there is a unique largest such $W_i$: just take the union of all such). Now put $V \coloneqq \bigcap_{i=1}^n W_i$. We have for each $i$ between $1$ and $n$ that $V \times U_i \subseteq W_i \times U_i \subseteq \neg C$ (the [[complement]] of $C$ in $X \times Y$), hence 

$$V \times X \;=\; V \times \bigcup_{i=1}^n U_i \;=\; \bigcup_{i=1}^n V \times U_i \subseteq \neg C$$ 

so that $(V \times X) \cap C = \emptyset$. 
=-- 

The "if" half is not quite so routine. We will first give a very direct proof that doesn't involve any fancy machinery (such as [[ultrafilters]]), although the fancy machinery does help give a better conceptual understanding of what is really going on, as we explain below. 

+-- {: .num_prop #if} 
###### Proposition 

If $X$ is a [[topological space]] with the property that the [[projection]] $\pi \colon Y \times X \to Y$ out of the [[product topological space]] is a [[closed map]] for every space $Y$, then $X$ is [[compact topological space|compact]]. 

=-- 

+-- {: .proof #ifProof} 
###### Proof 

Given a space $X$ satisfying this property, let $(C_i)_{i \in I}$ be any collection of [[closed subsets]] of $X$ having the [[finite intersection property]], that any intersection of finitely many $C_i$ is [[inhabited set|inhabited]]. Compactness of $X$ will follow if we can show $\bigcap_{i \in I} C_i$ is inhabited (by [this prop.](compact+space#fip)). 

Given that collection, construct a space $Y$ whose underlying set ${|Y|}$ is formed by adjoining a point $\infty$ to the underlying set of $X$ (so ${|Y|} = {|X|} \sqcup \{\infty\}$), and topologized by taking [[sub-base of a topology|subbasis]] elements to consist of _any_ subset of $X$ (not necessarily open) and any subset of the form $C_i \cup \{\infty\}$. (Thus we are embedding the "[[discrete topological space|discretification]]" of $X$ in a larger space $Y$.) Let $K \subseteq Y \times X$ be the [[topological closure]] of the set $\Delta = \{(x, x): x \in {|X|}\}$. By hypothesis, $\pi(K)$ is closed in $Y$, and contains $X$. But then it must also contain $\infty$ because the [[finite intersection property]] of the collection $(C_i)$ guarantees that $\infty$ is not an [[open point]] of $Y$. It follows that $K$ contains a point of the form $(\infty, x)$. 

This means that every [[neighborhood]] $(C_i \cup \{\infty\}) \times U$ of $(\infty, x)$ intersects the [[diagonal]] $\Delta$ in an inhabited set. In other words, $C_i \cap U$ is inhabited. But this means that $x \in C_i$ for every $i$, for if $x \notin C_i$ for some $i$, then by closure of $C_i$ we could find an open neighborhood $U$ of $x$ such that $C_i \cap U = \emptyset$. Hence $x \in \bigcap_{i \in I} C_i$, making this intersection inhabited, as required. 
=-- 

+-- {: .num_remark #Acknowledgement} 
###### Remark 
I ([[Todd Trimble]]) learned of this particular arrangement of proof during an email exchange with [[Tom Leinster]], who told me he learned it from [[Ioan James]]. I don't know who first invented it though. Pedagogically it is attractive because it avoids any need to discuss nets or ultrafilters or filters; it's just straight-up topology of the kind taught at typical American undergraduate institutions. 
=-- 

### Variant proofs 

There are actually quite a few proofs of Proposition \ref{if} that appear in the literature. The proof given [above](#ifProof) might have been the result of a gradual whittling down from more abstract, high-powered-looking proofs. 

1. One "canonical" proof that a seasoned mathematician might dream up goes as follows. Consider $Y = \beta({|X|})$, the space of [[ultrafilters]] on the underlying set ${|X|}$ of $X$, or the [[Stone-Cech compactification]] of $X$ (retopologized as a discrete space). Let $K \subseteq Y \times X$ be the convergence relation (i.e., $(U, x) \in K$ iff the ultrafilter $U$ on the set $X$ converges to the point $x$ in the space $X$). One readily checks that $K$ is closed. Thus $\pi(K) \subseteq Y$ is closed by hypothesis. Also observe that the "diagonal" $\Delta = \{(prin(x), x): x \in X\}$, where $prin(x)$ is the principal ultrafilter generated by $x$, sits inside $K$ since $prin(x)$ converges to $x$. So $\pi(K)$ also contains all principal ultrafilters which form a dense subset of $Y$. Being closed and dense, $\pi(K)$ is all of $Y$. But this just means that for every ultrafilter $U$ there is some $(U, x) \in K$, i.e., every ultrafilter converges to some point. This classically implies compactness of $X$. 

1. On reflection, we didn't really have to consider the entire space $\beta({|X|})$; we can just work with one ultrafilter at a time. So if we want to prove that every ultrafilter $U$ converges, we can just look at the subset ${|X|} \cup \{U\} \hookrightarrow \beta({|X|})$ with the [[subspace topology]] coming from $\beta({|X|})$ and run through the same diagonal proof. This gives us the proof found in Bourbaki's General Topology: given an ultrafilter $U$ on the underlying set of $X$, form a new space $Y$ whose underlying set is ${|X|} \sqcup \{\infty\}$ and topologized by saying all subsets of $X$ are open, and $A \sqcup \{\infty\}$ is an open neighborhood of $\infty$ if $A \in U$. This is just a direct description of the subspace topology coming from $\beta({|X|})$, and the rest of the proof runs parallel to the proof given in 1. 

1. On further reflection, the ultrafilter convergence characterization of compact spaces does rely on the [[ultrafilter theorem]] (that every proper filter can be extended to an ultrafilter), which involves the [[axiom of choice]] or some choice-y principle outside ZF. If one doesn't like this, one can always use just [[filters]] instead, and use the characterization of compact spaces that says that every proper filter on ${|X|}$ admits a [[cluster point]]. This characterization doesn't require any form of Choice. So, one would start with $Y = {|X|} \sqcup \{\infty\}$ but use a given proper filter $F$ to describe the neighborhoods of $\infty$; otherwise the description of $Y$ looks just the same as before. 

1. On still further reflection, one doesn't have to mention filters or cluster points at all. Instead one can work directly with a collection of sets $C_i$ satisfying the finite intersection property, and secretly think of that as generating a filter (a proper one by the FIP) and then follow 3. to define the topology of the space $Y$. As it happens, a cluster point of that filter is just a point lying in the intersection of all the $C_i$. This brings us to the proof we gave of Proposition \ref{if}. 

1. {#StillOtherCleverConstructions} Still other clever constructions of $Y$ are available. One has been described by [[Martín Escardó]] ([Escard&#243; 09](Escardo09)), who credits [[Leopoldo Nachbin]]. One nice feature is that Escard&#243; favors a point of view where instead of defining a continuous map $f: X \to Z$ to be closed if the direct image mapping or [[existential quantification]] $\exists_f: P(X) \to P(Z)$ preserves closed subsets, he uses instead the [[universal quantification]] $\forall_f: P(X) \to P(Z)$ and asks that this preserve *open sets*. This strategy circumvents the apparent use of [[excluded middle]] in proving Proposition \ref{onlyif}: he proves it directly and constructively. In any case, he considers a [[directed set|directed]] [[open cover]] $\Sigma$ of the given space $X$, then takes $Y = \mathcal{O}(X)$, the set of open sets of $X$, and topologizes $Y$ by taking its inhabited open sets to be upward-closed subsets $W \subseteq \mathcal{O}(X)$ such that $W \cap \Sigma$ is inhabited. Using the open-set formulation of closed maps, he then argues that $X$ belongs to $\Sigma$, which proves compactness. (This argument was also reprised [here](https://ncatlab.org/toddtrimble/published/Characterizations+of+compactness#escardo).) 

## Consequences

### Tychonoff theorem 
 {#TychonoffTheorem}

It has been observed by [Clementino and Tholen](#CT1996) that the closed-projection formulation of compactness (theorem \ref{char}) allows a fairly efficient proof of the [[Tychonoff theorem]], saying that the [[product topological space]] of any [[set]] of [[compact topological space]] is itself compact. First a very routine lemma. 

+-- {: .num_lemma #LemmaTychonoff} 
###### Lemma 
Let $(X_i)_{i: I}$ be a family of [[topological spaces]]. Then for a point $x$ and subset $A$ of the [[product topological space]] $\prod_{i: I} X_i$, we have $x \in Cl(A)$ (the [[topological closure]] of $x$) if, for every [[finite set|finite]] $F \subseteq I$, we have $\pi_F(x) \in Cl(\pi_F(A))$ under the [[projection]] map $\pi_F \colon \prod_{i: I} X_i \to \prod_{i: F} X_i$. 
=-- 

+-- {: .proof #LemmaTychonoffProof} 
###### Proof 
Suppose $x \notin Cl(A)$, so that there is an [[open neighborhood]] $U$ of $x$ such that $U \cap A = \emptyset$ (by [this lemma](Introduction+to+Topology+--+1#UnionOfOpensGivesClosure)). Sets of the [[pre-image]] of the form $\pi_i^{-1}(U_i)$ for open $U_i \subseteq X_i$ form a [[subbase|subbasis]] of the product topology, so there is a basis element $\pi_F^{-1}(V)$ (for some $V = U_{i_1} \times \ldots \times U_{i_n}$ and $F = \{i_1, \ldots, i_n\}$) that is a neighborhood of $x$ and contained in $U$, so we have $A \cap \pi_F^{-1}(V) = \emptyset$ or $A \subseteq \neg \pi_F^{-1}(V) = \pi_F^{-1}(\neg V)$ ([[pre-image]] of the [[complement]]) or what is the same, $\pi_F(A) \subseteq \neg V$ or $\pi_F(A) \cap V = \emptyset$. Since $V$ is a neighborhood of $\pi_F(x)$ not intersecting $\pi_F(A)$, we conclude $\pi_F(x) \notin Cl(\pi_F(A))$. In summary we have shown that $(x \notin Cl(A)) \Rightarrow \underset{ {F \subset  I} \atop { \text{finite} }}{\exists} \left( \pi_F(x) \notin Cl(\pi_F(A))\right)$. By [[contraposition]], this proves the claim.
=-- 

+-- {: .num_theorem} 
###### Theorem 
**([[Tychonoff theorem]])** 

The [[cartesian product]] of a [[small set|small]] family of [[compact topological spaces]] with the [[product topology]] is itself compact. 

=-- 

+-- {: .proof} 
###### Proof 
Let $(X_\alpha)_{\alpha \lt \kappa}$ be a family of compact spaces indexed by an [[ordinal]] $\kappa$. According to Theorem \ref{char}, it is enough to show that the [[projection]]

$$Y \times \prod_{\alpha \lt \kappa} X_\alpha \to Y$$ 

is a [[closed map]] for any space $Y$. We do this by [[induction]] on $\kappa$. The case $\kappa = 0$ is trivial. 

It will be convenient to introduce some notation. For $\gamma \leq \kappa$, let $X^\gamma$ denote the product $Y \times \prod_{\alpha \lt \gamma} X_\alpha$ (so $X^0 = Y$ in this notation), and for $\beta \leq \gamma$ let $\pi_\beta^\gamma \;\colon\; X^\gamma \to X^\beta$ be the obvious projection map. Let $K \subseteq X^\kappa$ be closed, and put $K_\beta \coloneqq Cl(\pi_{\beta}^\kappa(K))$. In particular $K_\kappa = K$ since $K$ is closed, and we are done if we show $\pi_0^\kappa(K) = K_0$. 

Assume as inductive hypothesis that starting with any $x_0 \in K_0$ there is $x_\beta \in K_\beta$ for all $\beta \lt \kappa$ such that whenever $\beta \lt \gamma \lt \kappa$, the compatibility condition $\pi_\beta^\gamma(x_\gamma) = x_\beta$ holds. In particular, $\pi_0^\beta(x_\beta) = x_0$ for all $\beta \lt \kappa$, and we are now trying to extend this up to $\kappa$. 

If $\kappa = \beta + 1$ is a [[successor ordinal]], then the projection 

$$\pi_\beta^\kappa \;\colon\; X^\beta \times X_\beta \to X^\beta$$ 

is a closed map since $X_\beta$ is compact. Thus $\pi_\beta^\kappa(K) = Cl(\pi_\beta^\kappa(K)) = K_\beta$ since $K$ is closed, so there exists $x_\kappa \in K$ with $\pi_\beta^\kappa(x_\kappa) = x_\beta$, and then 

$$\pi_0^\kappa(x_\kappa) = \pi_0^\beta \pi_\beta^\kappa (x_\kappa) = \pi_0^\beta(x_\beta) = x_0$$ 

as desired. 

If $\kappa$ is a [[limit ordinal]], then we may regard $X^\kappa$ as the [[inverse limit]] of spaces $(X^\beta)_{\beta \lt \kappa}$ with the obvious transition maps $\pi_\beta^\gamma$ between them. Hence the tuple $(x_\beta)_{\beta \lt \kappa}$ defines an element $x_\kappa$ of $X^\kappa$, and all that remains is to check that $x_\kappa \in K$. But since $K$ is closed, lemma \ref{LemmaTychonoff} says that it is sufficient to check that for every finite set $F$ of ordinals below $\kappa$, that $\pi_F(x_\kappa) \in Cl(\pi_F(K))$ (as a subspace of $\prod_{\alpha \in F} X_\alpha$). But for every such $F$ there is some $\beta \lt \kappa$ that dominates all the elements of $F$. One then checks 

$$\pi_F(x_\kappa) = \pi_F^\beta \pi_\beta^\kappa(x_\kappa) = \pi_F^\beta(x_\beta) \in \pi_F^\beta(K_\beta) = \pi_F^\beta(Cl(\pi_\beta^\kappa(K))) \subseteq Cl(\pi_F^\beta \pi_\beta^\kappa(K)) = Cl(\pi_F(K))$$ 

where the inclusion indicated as $\subseteq$ just results from continuity of $\pi_F^\beta$. This completes the proof. 
=-- 
### Tube lemma
 {#TubeLemma}

The following useful lemma was effectively proved already within the proof of prop. \ref{onlyif}, but it is worth making it explicit:


+-- {: .num_lemma #tube} 
###### Lemma 
**([[tube lemma]])** 

Let 

1. $X$ be a [[topological space]],

1. $Y$ a [[compact topological space]],

1. $x \in X$ a point,

1. $W \underset{\text{open}}{\subset} X \times Y$ an open subset in the [[product topology]], 

such that the $Y$-[[fiber]] over $x$ is contained in $W$:

$$
  \{x\} \times Y \;\subseteq\; W
  \,.
$$ 

Then there exists an [[open neighborhood]] $U_x$ of $x$ such that the "tube" $U_x \times Y$ around the fiber $\{x \} \times Y$ is still contained: 

$$
  U_x \times Y \subseteq W
  \,.
$$

=-- 


+-- {: .proof}
###### Proof

Let 

$$
  C \coloneqq (X \times Y) \backslash W
$$ 

be the [[complement]] of $W$. Since this is closed, by prop. \ref{onlyif} also its projection $p_X(C) \subset X$ is closed. 

Now

$$
  \begin{aligned}
    \{x\} \times Y \subset W
      & \;\Leftrightarrow\;
    \{x\} \times Y \; \cap \; C = \emptyset  
    \\
    & \;\Rightarrow\; 
    \{x\} \cap  p_X(C) = \emptyset
  \end{aligned}
$$

and hence by the closure of $p_X(C)$ there is (by [this lemma](Introduction+to+Topology+--+1#UnionOfOpensGivesClosure)) an open neighbourhood $U_x \supset \{x\}$ with 

$$
  U_x \cap p_X(C) = \emptyset
  \,.
$$  

This means equivalently that $U_x \times Y \cap C = \emptyset$, hence that $U_x \times Y \subset W$.

=--

+-- {: .num_remark} 
###### Remark

More [[category theory|category theoretically]], the tube lemma \ref{tube} becomes the statement that for $X$ compact, the map $\forall_\pi: P(Y \times X) \to P(Y)$ takes opens to opens, as mentioned [above](#StillOtherCleverConstructions).

=--



## References 

* {#CT1996} [[Maria Manuel Clementino]] and [[Walter Tholen]], *Tychonoff's theorem in a category*, Proc. Amer. Math. Soc., Vol. 124 No. 11 (Nov. 1996), 3311-3314. ([pdf](http://www.ams.org/journals/proc/1996-124-11/S0002-9939-96-03435-1/S0002-9939-96-03435-1.pdf)) 

* {#Escardo09} [[Martín Escardó]], *Intersections of compactly many open sets are open*, preprint dated May 27, 2009. ([pdf](http://www.cs.bham.ac.uk/~mhe/papers/compactness-submitted.pdf)) 

* {#Milne} [[James Milne]], section 17 of _[[Lectures on Étale Cohomology]]_

       
Much of the material of the present article was earlier collected in 

* [[Todd Trimble]], *Characterizations of compactness*, personal nLab webpage. ([link](https://ncatlab.org/toddtrimble/published/Characterizations+of+compactness)) 
