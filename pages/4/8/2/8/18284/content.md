
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


# Contents 
* table of contents 
{:toc}

This page will collect some technical material concerning [[colimits]] of [[normal spaces]] as computed in [[Top]]. Here "normal" means $T_4$, i.e., we assume as part of normality that points are closed. 

In particular it shows that [[CW-complexes are paracompact Hausdorff spaces|CW-complexes are normal spaces]] (theorem \ref{CWComplexesAreNormal} below). 

A basic technique is the exploitation of the Tietze extension condition which characterizes normal spaces. Similar techniques may be used to prove a parallel set of results for [[paracompact spaces]]; see [[colimits of paracompact spaces]]. 

## Basic results 

We start with some easy but useful results, using only our "bare hands" (i.e., using the definition of normality and applying simple reasoning). 

The first very easy observation is that normal spaces are closed under [[coproducts]] in [[Top]] (so-called "[[disjoint union spaces]]"). The proof may be safely left to the reader. 

There is no hope that normal spaces are closed under [[coequalizers]] or [[pushouts]]. A first example that comes to mind is the [[line with double origin]], which is the topological [[pushout]] of the diagram 

$$\mathbb{R} \leftarrow \mathbb{R} \setminus \{0\} \to \mathbb{R}$$ 

where both maps are the inclusion map. This space isn't even [[Hausdorff space|Hausdorff]], as every [[neighborhood]] of the point $0_1$ (the image of the origin under the first pushout [[coprojection]]) intersects every neighborhood of the point $0_2$ (the image of the origin under the second coprojection). 

However, there are reasonable conditions under which pushouts will be normal. (Throughout we assume all spaces are $T_1$, i.e., that [[singletons]] are [[closed set|closed]] ([here](separation+axioms#T1InTermsOfClosureOfPoints)), so that "normal" means $T_4$). 

+-- {: .num_prop #normal} 
###### Proposition 
Let $X$ be normal, and suppose $q: X \to Y$ in $Top$ is a [[closed maps|closed]] [[surjective function|surjection]]. Then $Y$ is normal. 
=-- 

+-- {: .proof} 
###### Proof 
First we claim singletons of $Y$ are closed: for each $y \in Y$ there exists $x \in X$ such that $y = q(x)$. Since $\{x\}$ is closed in $X$ and $q$ is closed, $\{y\} = q(\{x\})$ is closed in $Y$. 

Let $C, D$ be disjoint closed sets of $Y$, so that $\neg C, \neg D$ form an open cover of $Y$. Then $A = q^{-1}(\neg C), B = q^{-1}(\neg D)$ form an open cover of $X$. Normality of $X$ (in "[[De Morgan duality|De Morganized]]" form) implies there are closed subsets $E \subseteq A, F \subseteq B$ which together also cover $X$. Then $Y = q(X) = q(E \cup F) = q(E) \cup q(F)$, so the closed sets $q(E), q(F)$ cover $Y$. And we have $q(E) \subseteq q(A) = \neg C$ and similarly $q(F) \subseteq \neg D$, which is equivalent to $C \subseteq \neg q(E)$ and $D \subseteq \neg q(F)$, where $\neg q(E), \neg q(F)$ are disjoint open sets of $Y$, and we are done. 
=-- 

Here is one way in which such closed surjections arise: we know that [[compact Hausdorff spaces]] are normal spaces, and this is an especially nice class because the category of compact Hausdorff spaces is a [[pretopos]]. This is the categorical backdrop for the following observation. (We don't need this lemma in any result below; we include it merely as a handy lemma to have around.) 

+-- {: .num_lemma #pretopos} 
###### Lemma 
Let $X$ be a compact Hausdorff space. Then an equivalence relation $\sim \hookrightarrow X \times X$ is closed as a subset of $X \times X$ iff the quotient map $q: X \to X/\sim$ is a closed map. (In which case $X/\sim$ is compact Hausdorff.) 
=-- 

+-- {: .proof} 
###### Proof 
If $q: X \to X/\sim$ is a closed map, making $X/\sim$ compact Hausdorff, then the diagonal $\Delta \hookrightarrow X\sim \times X/\sim$ is a [[embedding of topological spaces|closed embedding]], so that its pullback along $q \times q$ 

$$\array{
\sim & \hookrightarrow & X \times X \\ 
\downarrow & & \downarrow \mathrlap{q \times q} \\ 
\Delta & \hookrightarrow & X/{\sim} \times X/{\sim}
}$$ 

also defines a closed subset of $X \times X$. 

In the other direction, suppose $\sim$ is closed, and let $A \subseteq X$ be a closed subset of $X$. Consider its $\sim$-*saturation* $\bar{A}$, namely 

$$\{x \in X: (\exists_{a \in A})\; x\sim a\} = \pi_1((\sim)\cap (X \times A)).$$ 

This is a closed set because the first projection $\pi_1$ is a closed map (by compactness of $X$). Moreover, $\bar{A} = q^{-1}(q(A))$, essentially by definition ($x \in q^{-1}(q(A))$ means $q(x) = q(a)$ for some $a \in A$). Since 
$q^{-1}(q(A))$ is closed, $q(A)$ is closed by definition of quotient topology. 
=-- 


+-- {: .num_remark} 
###### Remark 
A [[closed map|closed]] [[surjection]] is a quotient map (a [[regular epimorphism|regular epi]] in [[Top]]), and a closed [[injection]] is an [[embedding of topological spaces|embedding]] (a [[regular monomorphism|regular mono]] in $Top$). 
=-- 

+-- {: .num_lemma #poclosed} 
###### Lemma 
In $Top$, the pushout of a closed embedding along any continuous map is again a closed embedding. 
=-- 

+-- {: .proof} 
###### Proof 
We reproduce the proof given [here](/nlab/show/subspace+topology#pushout). 

Since $U = \hom(1, -): Top \to Set$ is [[faithful functor|faithful]], we have that monos are reflected by $U$; also monos and pushouts are preserved by $U$ since $U$ has both a [[left adjoint]] and a [[right adjoint]]. In $Set$, the pushout of a mono along any map is a mono, so we conclude $j$ is monic in $Top$. Furthermore, such a pushout diagram in $Set$ is also a pullback, so that we have the [[Beck-Chevalley condition|Beck-Chevalley equality]] $\exists_i \circ f^\ast = g^\ast \exists_j \colon P(C) \to P(B)$ (where $\exists_i \colon P(A) \to P(B)$ is the [[direct image]] map between [[power sets]], and $f^\ast: P(C) \to P(A)$ is the [[inverse image]] map). 

To prove that $j$ is a subspace, let $U \subseteq C$ be any open set. Then there exists open $V \subseteq B$ such that $i^\ast(V) = f^\ast(U)$ because $i$ is a subspace inclusion. If $\chi_U \colon C \to \mathbf{2}$ and $\chi_V \colon B \to \mathbf{2}$ are the maps to [[Sierpinski space]] that classify these open sets, then by the universal property of the pushout, there exists a unique continuous map $\chi_W \colon D \to \mathbf{2}$ which extends the pair of maps $\chi_U, \chi_V$. It follows that $j^{-1}(W) = U$, so that $j$ is a subspace inclusion. 

If moreover $i$ is an open inclusion, then for any open $U \subseteq C$ we have that $j^\ast(\exists_j(U)) = U$ (since $j$ is monic) and (by Beck-Chevalley) $g^\ast(\exists_j(U)) = \exists_i(f^\ast(U))$ is open in $B$. By the definition of the topology on $D$, it follows that $\exists_j(U)$ is open, so that $j$ is an open inclusion. The same proof, replacing the word "open" with the word "closed" throughout, shows that the pushout of a closed inclusion $i$ is a closed inclusion $j$. 
=-- 

## Tietze characterization 

A powerful tool for proving theorems about topological colimits of normal spaces is the characterization of normal spaces via the Tietze extension theorem: 

+-- {: .num_theorem} 
###### Theorem 
A space $X$ is normal if and only if, for each closed subset $C \subseteq X$ and map $f: C \to \mathbb{R}$, there is an extension map $g: X \to \mathbb{R}$, i.e., a map whose restriction $g|_C$ coincides with $f$. 
=-- 

+-- {: .num_remark} 
###### Remarks 

1. There are variations on the theorem in which stronger separation properties (such as perfect normality, or $T_6$) may be reformulated in terms of extension conditions. 

1. We remark that the "if" part of the proof is very easy. If $A, B$ are closed disjoint subsets of $X$, then the closed subspace $C = A \cup B$ is the coproduct on $A, B$ in $Top$, and we may define a map $f: A \cup B \to \mathbb{R}$ to be the constant $0$ on $A$ and the constant $1$ on $B$. Let $g: X \to \mathbb{R}$ be any extension of $f$; then $U = g^{-1}(\{x: x \lt 1/3\})$ and $V = g^{-1}(\{x: x \gt 2/3\})$ are separating open sets. 
=-- 

The following is a sample application. 

+-- {: .num_theorem #attach} 
###### Theorem 
If $X, Y, Z$ are normal spaces and $h: X \to Z$ is a closed embedding and $f: X \to Y$ is a continuous map, then in the pushout diagram in $Top$ 

$$\array{
X & \stackrel{h}{\to} & Z \\ 
\mathllap{f} \downarrow & & \downarrow \mathrlap{g} \\ 
Y & \underset{k}{\to} & W,
}$$

the space $W$ is normal (and $k: Y \to W$ is a closed embedding, by the preceding Lemma). 
=-- 

+-- {: .proof} 
###### Proof 
By the Tietze characterization, it suffices to show that any map $\phi: C \to \mathbb{R}$ on a closed subspace $C$ of $W$ can be extended to a map $\psi$ on all of $W$. Pulling back $C \hookrightarrow W$ along $k$, we have a closed subspace $k^{-1}(C) \hookrightarrow Y$ and a composite map $k^{-1}(C) \stackrel{k|}{\to} C \stackrel{\phi}{\to} \mathbb{R}$; call it $\alpha: k^{-1}(C) \to \mathbb{R}$. By normality of $Y$, the map $\alpha: k^{-1}(C) \to \mathbb{R}$ extends to a map $\beta: Y \to \mathbb{R}$. We obtain a map $\beta f: X \to \mathbb{R}$. 

Similarly, pulling $C \hookrightarrow W$ back along $g$, we have a composite map $g^{-1}(C) \stackrel{g|}{\to} C \stackrel{\phi}{\to} \mathbb{R}$. We may now define a map 

$$\gamma: h(X) \cup g^{-1}(C) \to \mathbb{R}$$ 

by $\gamma(h(x)) = \beta f(x)$ for $h(x) \in h(X)$, and $\gamma(z) = \phi(g(z))$ for $z \in g^{-1}(C)$. It is not hard to check that $\gamma$ is well-defined (by commutativity of the pullback square) and is continuous (using the fact that $h|: X \to h(X)$ is a homeomorphism, since $h$ is an embedding), and that $h(X) \cup g^{-1}(C)$ is a closed subset of $Z$ (since $h$ is closed). By normality of $Z$, we may extend $\gamma$ to a map $\delta: Z \to \mathbb{R}$, and we have just observed that $\delta h = \beta f$, so the pair $(\beta, \delta): Y + Z \to \mathbb{R}$ induces a unique map $\psi: W \to \mathbb{R}$ such that $\psi k = \beta$ and $\psi g = \delta$. Finally, the restriction of $\psi$ to $C$ is $\phi$, as required. 
=-- 

## Sequences of normal spaces 

+-- {: .num_prop #sequence} 
###### Proposition 
If $(i_n: X_n \to X_{n+1})_{n \in \mathbb{N}}$ is a countable sequence of closed embeddings between normal spaces, then the colimit $X = colim_n X_n$ is also normal. 
=-- 

+-- {: .proof} 
###### Proof 
Let $A, B$ be disjoint closed subsets of $X$, and for all $n$ put $A_n = X_n \cap A$, $B_n = X_n \cap B$. Working recursively, suppose given disjoint open sets $U_n, V_n$ such that $A_n \subseteq U_n$ and $B_n \subseteq V_n$. Since normality guarantees that we can refine further if necessary, i.e., find an open $O_n$ such that $A_n \subseteq O_n$ and $\widebar{O_n} \subseteq U_n$, we may assume that the closures $\widebar{U_n}$, $\widebar{V_n}$ are disjoint in $X_n$, as are their images in $X_{n+1}$ under the closed embedding $i_n$. The closed sets $i_n(\widebar{U_n}) \cup A_{n+1}$ and $i_n(\widebar{V_n}) \cup B_{n+1}$ are disjoint in $X_{n+1}$: 

* $A_{n+1} \cap B_{n+1} = \emptyset$ since $A \cap B = \emptyset$, 

* $i_n(\widebar{U_n}) \cap i_n(\widebar{V_n}) = i_n((\widebar{U_n} \cap \widebar{V_n}) = i_n(\emptyset) = \emptyset$ where the direct image operator $i_n(-)$ preserves binary intersections since $i_n$ is monic, 

* $i_n(\widebar{U_n}) \cap B_{n+1} = i_n(\widebar{U_n} \cap i_n^{-1}(B_{n+1})) = i_n(\widebar{U_n} \cap B_n) \subseteq i_n((\widebar{U_n} \cap \widebar{V_n}) = \emptyset$ (using Frobenius reciprocity), and similarly, 

* $A_{n+1} \cap i_n(\widebar{V_n}) = \emptyset$. 

Use normality of $X_{n+1}$ to select disjoint open sets $U_{n+1}, V_{n+1}$ such that $i_n(\widebar{U_n}) \cup A_{n+1} \subseteq U_{n+1}$ and $i_n(\widebar{V_n}) \cup B_{n+1} \subseteq V_{n+1}$, thus completing the recursive construction. 

It is clear that $i_n(U_n) \subseteq U_{n+1}$ and the union $U = colim_n U_n$ defines an open set of $X$ (by definition of colimit topology), as does $V = colim_n V_n$. The sets $U, V$ include $A, B$ respectively and are disjoint since any element they have in common must belong to $U_n$ and $V_n$ for sufficiently large $n$, which is impossible. This completes the proof. 
=-- 

+-- {: .num_remark} 
###### Remark 
An alternative proof using the Tietze characterization is easily given: if $C \subseteq colim_n X_n$ is closed and $f: C \to \mathbb{R}$ is continuous, then putting $C_n = X_n \cap C$ and $f_n = f|_{C_n}$, we define a suitable extension of each $f_n: C_n \to \mathbb{R}$ to a map $g_n: X_n \to \mathbb{R}$ by induction. Supposing at stage $n$ the map $g_n$ is given, we have a well-defined map $h_{n+1}: C_{n+1} \cup i_n(X_n) \to \mathbb{R}$ defined as $f_{n+1}$ on $C_{n+1}$ and as the composite $i_n(X_n) \cong X_n \stackrel{g_n}{\to} \mathbb{R}$ on $i_n(X_n)$. Then using normality of $X_{n+1}$, extend $h_{n+1}$ to a map $g_{n+1}: X_{n+1} \to \mathbb{R}$. Clearly $g_{n+1}$ extends $f_{n+1}$ and we have the compatibility equations $g_n = g_{n+1} i_n$, so the $g_n$ paste together to form a map $g: colim_n X_n \to \mathbb{R}$ which extends $f$. 

A little use of notation allows a short exposition of this proof.
Let $Z$ be the topological space corresponding to the partial order $a\lt b\gt c\lt d\gt e$ (where $a,c,d$ are closed points, $b,d$ are open, and closed subsets are $\{a,b,c\},\{c,d,e\},\{a\},\{c\},\{e\},\emptyset$), and let 
$g$ be the map gluing together points $b,c,d$. By Theorem 2.1, 
$f$ has the left lifting property wrt $g$ whenever $f$ is a closed embedding into a normal space. As each $i_n: X_n \to X_{n+1}$, ${n \in \mathbb{N}}$ has the left lifting property wrt $g$, their transfinite composition $\emptyset\to colim_n X_n$ has the same lifting property,
which means that $X$ is normal. 

=-- 

+-- {: .num_theorem #CWComplexesAreNormal} 
###### Theorem 
A [[CW-complex]] is a [[normal space]]. 
=-- 

+-- {: .proof} 
###### Proof 
A CW-complex $X$ is formed by an inductive process where the $n$-skeleton $X_n$ is formed as an [[attachment space]] formed from normal spaces. That is, we start with the normal space $X_{-1} = \emptyset$, and given the normal space $X_{n-1}$ and an attaching map $f: S_{n-1} = \sum_{i \in I} S_i^{n-1} \to X_{n-1}$, we push out the closed embedding $S_{n-1} = \sum_{i \in I} S_i^{n-1} \hookrightarrow \sum_{i \in I} D_i^n = D_n$ along the attaching map $f$ to get a closed embedding 

$$i_n: X_{n-1} \to X_n (= X_{n-1} \cup_{S_{n-1}} D_n)$$ 

and deduce $X_n$ is normal by Theorem \ref{attach}. Then $X = colim_n X_n$ is normal by applying Proposition \ref{sequence}. 
=--  

## Related entries

* [[colimits of paracompact Hausdorff spaces]]