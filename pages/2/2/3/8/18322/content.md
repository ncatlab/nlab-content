
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--





# Contents 
* table of contents 
{:toc} 

## Introduction 

In this article we collect some results on [[colimits]] of [[paracompact Hausdorff spaces]] as computed in the category of [[topological spaces]] [[Top]], and particular conditions under which the colimit is again paracompact and Hausdorff. 

The account is designed to be parallel to that given in [[colimits of normal spaces]], centering particularly on how paracompactness may be reformulated in terms of an extension or selection property. The relevant result, due to Ernest Michael, is particularly well-adapted to the study of colimits. 

In the sequel, a *paracompactum* (pl. *paracompacta*) is a paracompact Hausdorff space, just as [[compactum]] is a compact Hausdorff space. 

## Basic results 

+-- {: .num_prop #coproduct} 
###### Proposition 
The [[coproduct]] in $Top$ of a small family of paracompacta is a paracompactum. 
=-- 

The proof is very easy. See [here](https://ncatlab.org/nlab/show/paracompact+topological+space#ParacompactnessPreservedByDisjointUnion). 

+-- {: .num_prop} 
###### Proposition 
A [[closed subspace]] $A$ of a paracompactum $X$ is also a paracompactum. 
=-- 

+-- {: .proof} 
###### Proof 
Let $U_\alpha$ be an [[open cover]] of $A$; note $\neg A \cup U_\alpha$ is the maximal open $V_\alpha$ in $X$ such that $U_\alpha = V_\alpha \cap A$. The $V_\alpha$ cover $X$. If $\mathcal{V}$ is a locally finite open refinement of this cover (via paracompactness of $X$), then the family $\{V \cap A: V \in \mathcal{V}\}$ is a locally finite open refinement of the family of sets $U_\alpha$. Finally, $A$ is Hausdorff because Hausdorffness is a [[hereditary property]]. 
=-- 

+-- {: .num_lemma #poclosed} 
###### Lemma 
In $Top$, the pushout $j$ of a (closed/open) embedding $i$ along any continuous map $f$, 

$$\array{
A & \stackrel{i}{\hookrightarrow} & B \\ 
\mathllap{f} \downarrow & po & \downarrow \mathrlap{g} \\ 
C & \underset{j}{\hookrightarrow} & D,
}$$ 

is again a (closed/open) embedding. 
=-- 

+-- {: .proof} 
###### Proof 
For the sake of convenience, we reproduce the proof given [here](/nlab/show/subspace+topology#pushout). 

Since $U = \hom(1, -): Top \to Set$ is [[faithful functor|faithful]], we have that monos are reflected by $U$; also monos and pushouts are preserved by $U$ since $U$ has both a [[left adjoint]] and a [[right adjoint]]. In $Set$, the pushout of a mono along any map is a mono, so we conclude $j$ is monic in $Top$. Furthermore, such a pushout diagram in $Set$ is also a pullback, so that we have the [[Beck-Chevalley condition|Beck-Chevalley equality]] $\exists_i \circ f^\ast = g^\ast \exists_j \colon P(C) \to P(B)$ (where $\exists_i \colon P(A) \to P(B)$ is the [[direct image]] map between [[power sets]], and $f^\ast: P(C) \to P(A)$ is the [[inverse image]] map). 

To prove that $j$ is a subspace, let $U \subseteq C$ be any open set. Then there exists open $V \subseteq B$ such that $i^\ast(V) = f^\ast(U)$ because $i$ is a subspace inclusion. If $\chi_U \colon C \to \mathbf{2}$ and $\chi_V \colon B \to \mathbf{2}$ are the maps to [[Sierpinski space]] that classify these open sets, then by the universal property of the pushout, there exists a unique continuous map $\chi_W \colon D \to \mathbf{2}$ which extends the pair of maps $\chi_U, \chi_V$. It follows that $j^{-1}(W) = U$, so that $j$ is a subspace inclusion. 

If moreover $i$ is an open inclusion, then for any open $U \subseteq C$ we have that $j^\ast(\exists_j(U)) = U$ (since $j$ is monic) and (by Beck-Chevalley) $g^\ast(\exists_j(U)) = \exists_i(f^\ast(U))$ is open in $B$. By the definition of the topology on $D$, it follows that $\exists_j(U)$ is open, so that $j$ is an open inclusion. The same proof, replacing the word "open" with the word "closed" throughout, shows that the pushout of a closed inclusion $i$ is a closed inclusion $j$. 
=-- 

## Michael's selection characterization of paracompactness 

(See also [[Michael's theorems]].)

It is well-known (see [[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity|here]]) that a $T_1$ space $X$ is a paracompactum iff every open cover of $X$ [admits a subordinate partition of unity](/nlab/show/paracompact+Hausdorff+spaces+equivalently+admit+subordinate+partitions+of+unity). Michael's innovation was in working out how the partition of unity characterization may be recast in terms of existence of continuous sections of suitable projection maps. 

From here on out, all spaces will be assumed to be $T_1$ ([[singletons]] are [[closed subset|closed]]); see [[separation property]]. 


Recall that a [[relation]] in a [[category]] is a jointly monic [[span]] 

$$\array{
 & & R & & \\ 
 & \mathllap{p} \swarrow & & \searrow \mathrlap{q} & \\ 
X & & & & Y
}$$ 

and that the relation is [[entire relation|entire]] if $p$ is an [[epimorphism]]. We will be working in the category $Top$, where epimorphisms are the same as surjective continuous functions. A *selection* for such a relation is by definition a [[section]] of $p$, where of course in $Top$ this means a continuous section. (In the category $Set$, the [[axiom of choice]] may be equivalently stated as saying that every entire relation admits a selection, a formulation which is sometimes credited to [[Charles Sanders Peirce|Peirce]].) 

If $X$ is a space, let $\mathcal{O} X$ denote its topology, considered as a subset of the power set $P X$. Adapting the terminology of Michael, we will say a relation $X \stackrel{p}{\leftarrow} R \stackrel{q}{\to} Y$ is *lsc* ("lower semi-continuous") if the composite 

$$P Y \stackrel{q^\ast}{\to} P R \stackrel{\exists_p}{\to} P X$$ 

restricts to a map $\exists_p q^\ast: \mathcal{O} Y \to \mathcal{O} X$. (In more down-to-earth terms, if we consider $R$ as a subspace of $X \times Y$, this says the [[image]] $\pi_X(R \cap (X \times V))$ under the projection $\pi_X: X \times Y \to X$ is open in $X$ whenever $V$ is open in $Y$.) 

Let $B$ be a [[Banach space]] (for an example relevant to paracompactness concerns, $B$ could be $L^1(S)$, the Banach space freely generated by a set $S$ that indexes an open cover $\{U_s\}_{s \in S}$ of a given space $X$). We will say an (entire) relation $(R, p, q)$ from $X$ to $B$ in $Top$ is *closed and convex* if for each $x \in X$ the fiber $R_x = \exists_q p^\ast(x)$ is a closed [[convex set|convex]] subset of $B$. 

+-- {: .num_theorem #Michael} 
###### Theorem 
**(E. Michael's selection theorem)** 
A $T_1$ space $X$ is a paracompactum iff the condition 

* for every [[Banach space]] $B$, every entire, lsc, closed and convex relation $(R, p, q)$ from $X$ to $B$ admits a selection 

is satisfied. 
=-- 

For now we omit giving the proof (given in [Michael](#Michael56)). 

Before applying this theorem, we need a few lemmas that play supporting roles. 

+-- {: .num_lemma #pullback} 
###### Lemma 
If $(R, p, q): X \nrightarrow B$ is entire, lsc, closed and convex, and $f: A \to X$ is a continuous map, then the pullback relation $(f^\ast R, r, q g): A \nrightarrow Y$ (as in the pullback diagram) 

$$\array{
 & & f^\ast R & \stackrel{g}{\to} & R & & \\ 
 & \mathllap{r} \swarrow & (pb) & \swarrow \mathrlap{p} & & \searrow \mathrlap{q} & \\ 
A & \underset{f}{\to} & X & & & & B
}$$ 

is also entire, lsc, closed and convex. 
=-- 

+-- {: .proof} 
###### Proof 
Clearly $r$ is surjective (being a pullback of a surjection), so the relation $f^\ast R$ is entire, and for $a \in A$ we have $(f^\ast R)_a = R_{f(a)}$ so that $f^\ast R$ is closed and convex if $R$ is. We also have 

$$\exists_r (q g)^\ast = \exists_r g^\ast q^\ast = f^\ast \exists_p q^\ast$$ 

where the second equation follows from a Beck-Chevalley equation (induced by the pullback square). The map $\exists_p q^\ast$ preserves openness since $R$ is lsc, and $f^\ast$ preserves openness by continuity, so $\exists_r (q g)^\ast$ preserves openness, which proves $f^\ast R$ is lsc. 
=-- 

The next result is an important observation about extending continuous selections. 

+-- {: .num_lemma #extension} 
###### Lemma 
If $X$ satisfies the condition $\bullet$ of Theorem \ref{Michael} and $f: A \hookrightarrow X$ is a closed embedding, then for every $(R, p, q): X \to B$, every selection $\sigma: A \to f^\ast R$ of $(f^\ast R, r, q g)$ can be extended to a selection of $(R, p, q)$. 
=-- 

+-- {: .proof} 
###### Proof 
Replace the relation $R$ by the relation $S$ from $X$ to $B$ where $S_{f(x)} = \{\sigma(x)\}$ if $x \in A$, and $S_x = R_x$ if $x \notin f(A)$. Clearly every fiber $S_x$ is closed, convex, and inhabited, so $S$ is closed and convex and entire. We check that $S$ is lsc. Let $V$ be open in $Y$; we must verify that every point $x$ of $\pi_X(S \cap (X \times V))$ is an interior point of that set. If $x \in \neg A$, this is clear since 

$$\neg A \cap \pi_X(S \cap (X \times V)) = \neg A \cap \pi_X(R \cap (X \times V)$$ 

is open. If $x \in A$, then by continuity of $\sigma$ there is open neighborhood $U$ of $x$ such that $\sigma(x') \in V$ for all $x' \in U \cap A$, and then one may easily check that 

$$U \cap \pi_X(R \cap (X \times V)) \subseteq \pi_X(S \cap (X \times V))$$ 

so that the left side is an open neighborhood of $x$ contained within the right side. Thus $S$ is lsc. 

Since hypothesis $\bullet$ holds for $X$, we conclude that $S$ admits a selection $\tau$; by construction of $S$ we must have that $\tau |_A = \sigma$, and this completes the proof. 
=-- 

## Applications to colimits of paracompacta 

Now we put Michael's selection theorem to use in developing colimits of paracompacta. 

+-- {: .num_theorem #ClosedEmbeddingsOfParacompactaClosedUnderPushout} 
###### Theorem 
If $X, Y, Z$ are paracompacta and $h: X \to Z$ is a closed embedding and $f: X \to Y$ is a continuous map, then in the pushout diagram in $Top$ 

$$\array{
X & \stackrel{h}{\to} & Z \\ 
\mathllap{f} \downarrow & & \downarrow \mathrlap{g} \\ 
Y & \underset{k}{\to} & W,
}$$

the space $W$ is a paracompactum (and $k: Y \to W$ is a closed embedding, by Lemma \ref{poclosed}). 
=-- 

(Compare a similar result for normal spaces, [here](https://ncatlab.org/nlab/show/colimits+of+normal+spaces#attach).) 

+-- {: .proof} 
###### Proof 
Let $W \stackrel{p}{\leftarrow} R \stackrel{q}{\to} B$ be an entire, lsc, closed and convex relation to a Banach space $B$; by Michael's selection criterion, it suffices to show that $W$ is $T_1$ and $p$ admits a section. That $W$ is $T_1$ is easy: a point $x \in W$ either belongs to the closed subspace $Y \hookrightarrow W$ or it doesn't. If it does, then because $Y$ is Hausdorff, it is a closed point in a closed subspace, so it is a closed point in $W$. If it doesn't, then $k^{-1}(x) = \emptyset$ and $g^{-1}(x)$ is a singleton in $Z$ and thus closed in $Z$ since $Z$ is Hausdorff, i.e., the inverse image of $x$ under the quotient map $(k, g): Y + Z \to W$ is the closed subset $\emptyset + g^{-1}(x)$, so $x$ must be closed in $W$ by definition of quotient topology. 

Thus we have only to prove $p$ admits a section. Using Lemma \ref{pullback}, we pull back $(R, p, q)$ to entire, lsc, closed and convex relations to $B$ from $Y$ and from $Z$: 

$$\array{
X & \stackrel{h}{\to} & Z & & \\ 
\mathllap{f} \downarrow & & \downarrow \mathrlap{g} & \nwarrow & \\ 
Y & \underset{k}{\to} & W & & g^\ast R \\ 
 & \nwarrow & & \nwarrow \mathrlap{p} & \downarrow \\ 
 & & k^\ast R & \to & R.
}$$ 

By paracompactness of $Y$ and the selection criterion, there is a section $s$ of $k^\ast R \to Y$. The composite $s f: X \to k^\ast R$ in turn induces a selection $t: X \to f^\ast k^\ast R \cong h^\ast g^\ast R$. By Lemma \ref{extension}, the selection $t$ may be extended to a selection $u: Z \to g^\ast R$. The two maps 

$$Y \stackrel{s}{\to} k^\ast R \to R, \qquad Z \stackrel{u}{\to} g^\ast R \to R$$ 

may be pasted together (i.e., their respective composites with $f$ and $h$ agree) to give a map out of the pushout, $i: W \to R$, which is easily checked to be a section of $p$. 
=-- 

+-- {: .num_prop #ColimitsOfSequencesOfParacompacta} 
###### Proposition 
If $(i_n: X_n \to X_{n+1})_{n \in \mathbb{N}}$ is a countable sequence of closed embeddings between paracompacta, then the colimit $X = colim_n X_n$ is also a paracompactum. 
=-- 

+-- {: .proof} 
###### Proof 
Clearly $X$ is $T_1$: for any $x \in X$, the intersection $\{x\} \cap X_n$ is closed in $X_n$ for all $n$, so $x$ must a closed point of $X$. 

Let $j_n: X_n \to X$ denote a component of the colimit cocone. Let $(R, p, q)$ from $X$ to a Banach space $B$ be an entire, lsc, closed and convex relation. Pulling this back to $X_0$, by paracompactness we have a selection $X_0 \to j_0^\ast R$. Given a selection $X_n \to j_n^\ast R$, we may extend along $i_n$ to a selection $X_{n+1} \to j_{n+1}^\ast R$ using paracompactness and Lemma \ref{extension}. These selections, being compatible with the inclusions $i_n$, paste together to give a selection $X \to R$. 
=-- 

In particular this may be used to see that _[[CW-complexes are paracompact Hausdorff spaces]]_.

## Related entries

* [[colimits of normal spaces]]

## References 

* {#Michael56} [[Ernest Michael]], *Continuous Selections I*, The Annals of Mathematics, 2nd Series, Vol. 63 No. 2. (March 1956), 361-382. [stable URL](http://www.jstor.org/stable/1969615?seq=1#page_scan_tab_contents), ([pdf](http://www.renyi.hu/~descript/papers/Michael_1.pdf)) 



[[!redirects colimits of paracompact spaces]]
