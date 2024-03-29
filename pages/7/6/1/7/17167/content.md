# Contents 
* table of contents 
{:toc}

## Introduction 

The goal of this article is to prove that a [[compactum|compact Hausdorff]] [[ring]] $R$ is a [[profinite space|profinite]] ring, i.e., is canonically isomorphic as a [[topological ring]] to its [[profinite completion]] $\widehat{R}$, topologized as an inverse limit of [[finite set|finite]] rings with their [[discrete topology|discrete topologies]]. 

Further commentary on this result can be found in a Caf&#233; [blog post](#Lein) of Tom Leinster, in connection with some work by his student Barry Devlin. 

## Preliminaries 

All topological rings considered are $T_0$ (see [[separation axiom]]). As is well-known from the study of [[uniform structures]], this implies that all our rings are [[Hausdorff space|Hausdorff]] and even [[Tychonoff spaces]]. In particular, finite rings are Hausdorff and therefore discrete. If $S$ is a finite ring and $f: R \to S$ is a [[continuous map|continuous]] ring homomorphism, this means the [[kernel]] of $f$ must be an [[open set|open]] [[ideal]] of $R$ (for us, "ideal" always means two-sided ideal), since $\{0\}$ is open in $S$. 

In the converse direction, if $R$ is a compact ring and $I$ is an open ideal, then the ring $R/I$ with the [[quotient topology]] coming from $R$ is discrete (every point is open), and compact since $R$ is compact, and so $R/I$ must then be finite. 

Let $\mathcal{O}(R)$ denote the [[poset]] of open ideals of $R$, ordered by [[subset|inclusion]]. This poset is [[directed set|codirected]] by taking finite [[intersections]] of ideals. Each inclusion $I \subseteq J$ induces a [[surjection]] of finite rings $R/I \to R/J$, and so we get a [[functor]] $\mathcal{O}(R) \to Ring$ whose (projective) [[limit]] is the profinite completion $\widehat{R}$ of $R$; the quotient maps $proj_I: R \to R/I$ of course induce a canonical map $\pi: R \to \widehat{R}$. 

+-- {: .num_prop #surj} 
###### Proposition 
The map $\pi: R \to \widehat{R}$ is surjective. 
=-- 

+-- {: .proof} 
###### Proof 
Since $R$ is compact and $\widehat{R}$ is Hausdorff, the image $\pi(R)$ is closed in $\widehat{R}$, so it suffices to show the image is a [[dense subspace]]. 

So, we are to show that if $U \subseteq \widehat{R}$ is open and [[inhabited set|inhabited]], then there exists $x \in R$ with $\pi(x) \in U$. Let $\pi_I: \widehat{R} \to R/I$ denote a typical component map of the limit cone. A [[basis of a topology|basis]] for the topology of $\widehat{R}$ consists of inhabited finite intersections of the form $U = \pi_{I_1}^{-1}(x_1) \cap \ldots \cap \pi_{I_n}^{-1}(x_n)$ where each $x_k$ is a point of $R/I_k$, so WLOG assume $U$ is of this form. 

Let $y = \langle y_I \rangle_{I \in \mathcal{O}(R)} \in \widehat{R}$ be any point belonging to $U$ (so $y_{I_i} = x_i$ for $i = 1, \ldots, n$), and put $J = \bigcap_{i=1}^n I_i$. Then for each $x_i$ the coordinate $y_J$ maps to $x_i$ under the map $R/J \to R/I_i$, precisely because of the compatibility conditions on the coordinates imposed by the limit. Then, letting $y' \in R$ be an element that maps to $y_J$ under $R \to R/J$, the element $\pi(y')$ lies in $U$ and we are done. 
=-- 

## Compact rings are totally disconnected 

A key technical result is the following (see this $n$-Category Caf&#233; [comment](#Trim)): 

+-- {: .num_theorem #totdisc} 
###### Theorem 
Every compact Hausdorff ring $R$ is [[connected space|totally disconnected]]. 
=-- 

+-- {: .proof} 
###### Proof 
Let $R^\ast$ be the [[Pontryagin duality|Pontryagin dual]] of (the additive group of) $R$; as a space $R^\ast$ is discrete. As $R$ and $R^\ast$ are [[locally compact Hausdorff space|locally compact Hausdorff]], they are [[exponentiable space|exponentiable]] as spaces, and it follows quickly that the functorial maps 

$$Hom(R, R) \to Hom(R^\ast, R^\ast), \qquad Hom(R^\ast, R^\ast) \to Hom(R^{\ast\ast}, R^{\ast\ast}) \cong Hom(R, R)$$ 

are continuous homomorphisms of topological groups. Using naturality of the isomorphism $R \cong R^{\ast\ast}$, these maps are mutually inverse, and so they give an [[isomorphism]] of topological groups. 

The multiplication map $R \times R \to R$ [[currying|transforms]] to a continuous injection $i: R \to Hom(R, R) \cong Hom(R^\ast, R^\ast)$. As $R$ is compact and $Hom(R^\ast, R^\ast)$ is Hausdorff, the injection $i$ maps $R$ homeomorphically onto its image in $Hom(R^\ast, R^\ast)$, i.e., is a subspace embedding. But $Hom(R^\ast, R^\ast)$ is manifestly a subspace of a product of discrete spaces and hence totally disconnected, so $R$ is totally disconnected as well. (In more detail: if $C \subseteq R$ is connected, then the image of $C$ under the composite 

$$C \subseteq R \stackrel{i}{\to} Hom(R^\ast, R^\ast) \hookrightarrow \prod_{x \in R^\ast} R^\ast \stackrel{proj_x}{\;\;\to\;\;} R^\ast$$ 

is also connected and hence a one-point space for each $x \in R^\ast$, so that $i(C)$ and therefore $C$ are one-point spaces.) 
=-- 

## Compact rings have enough open ideals 

By Theorem \ref{totdisc}, Pontryagin duality implies compact rings are totally disconnected, which readies us for a next wave of results. 

+-- {: .num_lemma #compopen} 
###### Lemma 
Let $X$ be a compact Hausdorff totally disconnected space. For each $x \in X$ and open neighborhood $V$ of $x$, there exists a compact open set $U$ such that $x \in U \subseteq V$. 
=-- 

+-- {: .proof} 
###### Proof 
In a compact Hausdorff space $X$, the [connected component](/nlab/show/connected+space#connected_components) of a point $x$ equals its quasi-component; an online proof may be found [here](http://math.stackexchange.com/a/11423/43208). So if $X$ is also totally disconnected, then $x$ is also the intersection of all [[clopen set|clopens]] containing it. Now let $V$ be an open [[neighborhood]] of $x$, so $\bigcap_{x \in K\; clopen} K \subseteq V$ and therefore $\neg V \subseteq \bigcup_{x \in K\; clopen} \neg K$. As $\neg V$ is compact, finitely many such clopens $\neg K_1, \ldots, \neg K_n$ cover $\neg V$, and so $U \coloneqq \bigcap_{i=1}^n K_n \subseteq V$. This $U$ is compact and open and contains $x$, which completes the proof. 
=-- 

+-- {: .num_lemma #opengroup} 
###### Lemma 
Let $A$ be a compact Hausdorff totally disconnected abelian group. For each open neighborhood $V$ of $0 \in A$, there exists an open subgroup $O$ such that $O \subseteq V$. 
=-- 

+-- {: .proof} 
###### Proof 
By Lemma \ref{compopen}, there is a compact open $W$ with $0 \in W \subseteq V$. Now let $\alpha: W \times W \to A$ be the restriction of the addition operation $+: A \times A \to A$. Since $\alpha$ is continuous, there is for each $x \in W$ an open neighborhood $V_x \times U_x \subseteq \alpha^{-1}(W)$ of $(x, 0)$ where we may assume $U_x$ is *symmetric* (i.e., $U_x = -U_x$). Finitely many of the $V_x$ cover $W$, say $V_{x_1}, \ldots, V_{x_n}$. Then putting $U = U_{x_1} \cap \ldots \cap U_{x_n}$, we have that $\alpha(W \times U) \subseteq W$, or $W + U \subseteq W$ for short. This $U$ is again symmetric: $U = -U$. 

Hence if $U^n = U + \ldots + U$ denotes the set of all sums of $n$ elements belonging to $U$, then $U^n$ is open and $W + U^n \subseteq W$ by induction, whence $U^n \subseteq W$. Since $U$ is symmetric, the union $O = \bigcup_n U^n$ is the subgroup generated by $U$; it is open and contained in $W$ and therefore also in $V$, which completes the proof. 
=-- 

+-- {: .num_lemma #openideal} 
###### Lemma 
Let $R$ be a compact Hausdorff totally disconnected ring. For each open neighborhood $V$ of $0$, there is an open ideal $I$ such that $I \subseteq V$. 
=-- 

+-- {: .proof} 
###### Proof 
By Lemma \ref{opengroup}, there is an open additive subgroup $O \subseteq V$. Let $I = \{x \in R: R x R \subseteq O\}$. It is evident that $0 \in I$ and $I$ is an ideal of $R$. Now hold $x \in I$ fixed. For each $(a, b) \in R \times R$, continuity of multiplication implies there are open neighborhoods $W_{(a, b)}$ of $a$, $W_{(a, b)}'$ of $b$, and $V_{(a, b)}$ of $x$ such that $W_{(a, b)} V_{(a, b)} W_{(a, b)}' \subseteq O$. By compactness of $R \times R$, finitely many sets of the form $W_{(a, b)} \times W_{(a, b)}'$ cover $R \times R$. The corresponding finite intersection $\bigcap_{i=1}^n V_{(a_i, b_i)}$ is an open neighborhood of $x$ that is contained in $I$, thus completing the proof. 
=-- 

## Compact rings are profinite 

Now for our final result. 

+-- {: .num_theorem} 
###### Theorem 
For $R$ a compact ring, the canonical map $\pi: R \to \widehat{R}$ is [[monomorphism|injective]]. 
=-- 

This and Proposition \ref{surj} taken together imply that $\pi$ is a ring isomorphism. It is also a [[homeomorphism]] because it is a continuous [[bijection|bijective]] map from a compact space to a Hausdorff space. Therefore $\pi$ is an isomorphism of topological rings. 

+-- {: .proof} 
###### Proof 
As we have an inclusion $\widehat{R} \hookrightarrow \prod_{I \in \mathcal{O}(R)} R/I$ of the profinite completion as projective limit, we see the kernel of $\pi$ is the same as the kernel of 

$$\langle proj_I \rangle_{I \in \mathcal{O}(R)}: R \to \prod_{I \in \mathcal{O}(R)} R/I$$ 

which is precisely $\bigcap_{I \in \mathcal{O}(R)} I$. Since by Lemma \ref{openideal} every neighborhood of $0 \in R$ contains an open ideal $I \in \mathcal{O}(R)$, this intersection is contained in the intersection of all open neighborhoods of $0$, which is $\{0\}$ since $R$ is Hausdorff. Thus the kernel of $\pi$ is trivial, as was to be shown. 
=-- 

## Related concepts 

* [[profinite group]] 

## References 

* [[Tom Leinster]], _Holy Crap, Do You Know What A Compact Ring Is?_, blog post, $n$-Category Caf&#233; (August 20, 2014). ([link](https://golem.ph.utexas.edu/category/2014/08/holy_crap_do_you_know_what_a_c.html)) 
 {#Lein} 

* [[Todd Trimble]], comment on _Holy Crap, Do You Know What A Compact Ring Is?_, blog post, $n$-Category Caf&#233; (August 24, 2014). ([link](https://golem.ph.utexas.edu/category/2014/08/holy_crap_do_you_know_what_a_c.html#c047108))
 {#Trim} 

* L. Ribes and P. Zalesskii, _Profinite groups_, volume 40 of Ergebnisse der Mathematik und ihrer Grenzgebiete. 3. Folge (2000), Springer-Verlag, 
Berlin. 
