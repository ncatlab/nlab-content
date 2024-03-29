# Contents # 
* table of contents 
{:toc} 

## Idea 

The countable chain condition, appearing in various guises (for [[topological spaces]], for [[posets]], for [[Boolean algebras]]), frequently recurs in discussions on [[forcing]] in [[set theory]], particularly in discussions about preservation of [[cardinals]] and [[cofinalities]] in forcing extensions. 

It is something of a misnomer because it is really a condition about [[antichains]]. But in the topological context it is equivalent to a condition on chains, and the name has stuck. 

## Definitions 

+-- {: .num_defn} 
###### Definition 
Suppose $P$ is a poset with a [[minimum|bottom]] element $0$. A *(strong) antichain* in $P$ is a subset $A \subseteq P$ such that for all $a, b \in A$, we have either $a = b$ or $0$ is their [[meet]] (we need not assume general meets exist in $P$). If $P$ is a poset *without* a bottom, we define $A \subseteq P$ to be an antichain if it becomes an antichain in $P^+$, the poset obtained by freely adjoining a bottom to $P$; this is equivalent to saying $a, b$ have no lower bound in $P$. 
=-- 

+-- {: .num_defn} 
###### Definition 
A poset $P$ satisfies the *countable chain condition* if every antichain in $P$ is a [[countable set]] (i.e., at most denumerable). 

A topological space $X$ satisfies the countable chain condition if its [[frame]] of open sets $Op(X)$ does (as a poset). 
=-- 

For future reference, we record a result on the countable chain condition in [[Heyting algebras]] $H$. Let $Reg(H)$ denote the Boolean algebra of regular elements ($x \in H$ such that $x = \neg \neg x$). 

+-- {: .num_lemma #reg} 
###### Lemma 
A Heyting algebra $H$ satisfies the countable chain condition iff $Reg(H)$ does. 
=-- 

+-- {: .proof} 
###### Proof 
The inclusion $Reg(H) \hookrightarrow H$ preserves meets and $0$, so if every antichain in $H$ is countable, then the same is true in $Reg(H)$. 

The quotient map $\neg \neg: H \to Reg(H)$ also preserves meets and $0$ (details are at [[Heyting algebra]]), and moreover the restriction of this map to an antichain $A \subseteq H$ is an injection (if $\neg \neg a = \neg \neg b$ for $a, b \in A$, then $a = b$ or $a \wedge b = 0$; in the latter case $a \leq \neg \neg a = \neg \neg a \wedge \neg \neg b = \neg \neg (a \wedge b) = 0$ and similarly $b = 0$, so $a = b$). So if every antichain in $Reg(H)$ is countable, the same is true in $H$. 
=-- 

### Chains, not antichains 

+-- {: .num_prop} 
###### Proposition 
Let $B$ be a complete Boolean algebra. For cardinals $\kappa$, there is a bijective correspondence between 

* maps $g: \kappa \to B \setminus \{0\}$ such that $\{g(\alpha): \alpha \lt \kappa\}$ is an antichain in $B$; 

* injective [[cocontinuous functor|colimit-preserving]] poset maps $f: \kappa \to B$, 

here regarding $\kappa$ as an [[ordinal]]. 
=-- 

+-- {: .proof} 
###### Proof 
Given an antichain $g: \kappa \to B \setminus \{0\}$, define a colimit-preserving chain $f: \kappa \to B$ by $f(\beta) = \sum_{\alpha \lt \beta} g(\alpha)$ (so $f(0) = 0$, as mandated by colimit-preservation). Given an injective colimit-preserving chain $f: \kappa \to B$, define an antichain $g: \kappa \to B \setminus \{0\}$ by $g(\alpha) = f(\alpha + 1) \setminus f(\alpha) \coloneqq f(\alpha + 1) \wedge \neg f(\alpha)$. It is straightforward to verify that these assignments are inverse to one another. 
=-- 

+-- {: .num_cor} 
###### Corollary 
$B$ satisfies the countable chain condition iff every chain $b_0 \lt b_1 \lt \ldots$ in $B$ is countable. 
=-- 

This corollary is stated in terms of ascending chains, but by self-duality of Boolean algebras, it could equally well be stated in terms of descending chains. 

For topological spaces $X$, the frame $H = Op(X)$ satisfies the countable chain condition iff $Reg(H)$, the complete Boolean algebra of regular open sets, satisfies the countable chain condition (Lemma \ref{reg}). Now a regular element is just an element of the form $\neg U$, which for an open set $U$ is the complement of its closure. Thus for the topological case we deduce the following formulation in terms of chains: 

+-- {: .num_prop} 
###### Proposition 
A space $X$ satisfies the countable chain condition if and only if every collection of open sets $\{U_\alpha\}_{\alpha \lt \kappa}$ that satisfies the condition 

* $\widebar{U_\alpha} \subset \widebar{U_\beta}$ (strict inclusion between closures) whenever $\alpha \lt \beta$ 

is countable. 
=-- 

## Products of separable spaces 

We show in this section that arbitrary products of separable spaces satisfy the countable chain condition. 

+-- {: .num_prop #sep} 
###### Proposition 
A [[separable space]] satisfies the countable chain condition. 
=-- 

+-- {: .proof} 
###### Proof 
Let $D$ be a countable dense set, and suppose given a collection of pairwise disjoint inhabited open sets $\{U_\alpha: \alpha \in A\}$. Each $U_\alpha$ contains at least one $d \in D$. Thus the map $D \to A$ sending $d \in D$ to the unique $\alpha \in A$ such that $d \in U_\alpha$ is surjective, and so $A$ is at most countable. 
=-- 

Next we will need a result in combinatorial set theory. A *$\Delta$-system*, also called a *sunflower*, is a collection of finite sets $A_i$ such that any two intersect in the same set: there is some "common core" $S$ such that $A_i \cap A_j = S$ when $i \neq j$. 

+-- {: .num_lemma} 
###### Lemma 
**(Sunflower lemma)** 
Let $\mathcal{A}$ be an *uncountable* collection of finite sets. Then there is some uncountable subset $\mathcal{B} \subseteq \mathcal{A}$ that is a sunflower. 
=-- 

+-- {: .proof} 
###### Proof 
Without loss of generality, we may suppose all $A \in \mathcal{A}$ have the same cardinality $n$. We argue by induction on $n$. The case $n = 0$ is trivial. Assume the result holds for $n$, and suppose ${|A|} = n + 1$ for all $A \in \mathcal{A}$. If some $a \in X = \bigcup \mathcal{A}$ belongs to uncountably many $A \in \mathcal{A}$, then these $A$ form a collection $\mathcal{A}'$, and by inductive hypothesis the collection $\{A \setminus \{a\}: A \in \mathcal{A}'\}$ has a sunflower $\mathcal{B}'$. Then induction goes through by forming the sunflower $\{B + \{a\}: B \in \mathcal{B}'\}$. 

Otherwise, each $a \in X$ belongs to at most countably many $A \in \mathcal{A}$. In this case we may form an uncountable pairwise disjoint sequence $\{A_\alpha \in \mathcal{A}: \alpha \in \omega_1\}$ by transfinite induction: if $A_\alpha$ have been chosen for all $\alpha: \alpha \lt \beta \lt \omega_1$, then only countably many $A$ have an inhabited intersection with $\bigcup_{\alpha \lt \beta} A_\alpha$, and we simply choose an $A_\beta$ belonging to the uncountable collection that remains after removing such $A$. (So here the common core $S$ of the sunflower is the empty set.) 
=-- 

+-- {: .num_prop #prod} 
###### Proposition 
If $\{X_i\}_{i \in I}$ is an arbitrary family of spaces such that any finite product of the $X_i$ satisfies the countable chain condition, then the full product $X = \prod_{i \in I} X_i$ also satisfies the countable chain condition. 
=-- 

+-- {: .proof} 
###### Proof 
Suppose otherwise, that $\{U_\alpha\}_{\alpha \in A}$ is an uncountable collection of pairwise disjoint inhabited open sets of $X$. Shrinking them if necessary, we may suppose each $U_\alpha$ is a basic open of the form $\prod_{i \in F_\alpha} U_{\alpha, i} \times \prod_{i \notin F_\alpha} X_i$, where $F_\alpha \subseteq I$ is a finite set. The collection $\{F_\alpha\}$ has a sunflower by the Sunflower Lemma, say with common core $S$, and without loss of generality we may suppose $\{F_\alpha\}$ *is* that sunflower (i.e., that the $\alpha$\'s used to index the sunflower are just the $\alpha \in A$: throw away any other $\alpha \in A$). Let $\pi_S: X \to \prod_{i \in S} X_i$ be the obvious projection map. We first claim that the sets $\pi_S(U_\alpha)$ are pairwise disjoint, a purely set-theoretic matter. 

Suppose instead $u \in \pi_S(U_\alpha) \cap \pi_S(U_{\alpha'})$. Regard $u \in \prod_{i \in S} X_i$ as a section of the canonical projection $\sum_{i \in S} X_i \to S$. That it belongs to $\pi_S(U_\alpha)$ simply means it extends to some section $\sigma$ of the canonical map $\sum_{i \in A} X_i \to A$ such that the restriction of $\sigma$ to $F_\alpha$ factors through the inclusion $\sum_{i \in F_\alpha} U_{\alpha, i} \hookrightarrow \sum_{i \in A} X_i$, as on the left half of the following diagram: 

$$\array{
\sum_{i \in F_\alpha} U_{\alpha, i} & \hookrightarrow & \sum_{i \in A} X_i & \hookleftarrow & \sum_{i \in F_{\alpha'}} U_{\alpha', i} \\ 
\mathllap{\exists v} \uparrow & & \mathllap{\sigma} \uparrow \uparrow \mathrlap{\sigma'} & & \uparrow \mathrlap{\exists w} \\ 
F_\alpha & \hookrightarrow & A & \hookleftarrow & F_{\alpha'}\\ 
 & \nwarrow & & \nearrow & \\ 
 & & S & & 
}$$ 

Similarly there is a section $\sigma': A \to \sum_{i \in A} X_i$ and a partial section $w$, as shown on the right half. With the partial sections $v$ and $w$ in hand, amalgamate them to a partial section over the union $F_\alpha \cup F_{\alpha'}$ (we can do this, as $v: F_\alpha \to \sum_{i \in A}$ and $w: F_{\alpha'} \to \sum_{i \in A} X_i$ both restrict to the same map $u$ on the intersection $S = F_\alpha \cap F_{\alpha'}$). Then extend the amalgamation $v \cup w$ however you please to a full section $\sigma'': A \to \sum_{i \in A} X_i$. This $\sigma''$ belongs to both $U_\alpha$ and $U_{\alpha'}$, contradicting their disjointness, and proving the claim. 

Thus the $\pi_S(U_\alpha)$ form an uncountable collection of open, inhabited, pairwise disjoint sets, contradicting the countable chain condition hypothesis on the finite product $\prod_{i \in S} X_i$. With this the proof is complete. 
=-- 

+-- {: .num_cor} 
###### Corollary 
An arbitrary product of separable spaces $X_i$ satisfies the countable chain condition. 
=-- 

+-- {: .proof} 
###### Proof 
Any finite product of separable spaces $X_i$ is separable and thus satisfies the countable chain condition by Proposition \ref{sep}, so the full product does as well by Proposition \ref{prod}. 
=-- 

## Related countability properties of topological spaces

[[!include topology - countability axioms]]

[[!redirects countable chain conditions]] 