This theorem for [[filtered space]]s involves the fundamental [[crossed complex]] $\Pi X_*$ of a [[filtered space]] $X_*$, and the notion of [[connected filtered space]].

# Statement # 

Suppose $X_*$ is a filtered space and $X$ is the union of the interiors of sets $U^i$, $i \in I$. Let $U^i_*$ be the filtered space given by the intersections $U^i \cap X_n$ for $n \geq 0$. If $d=(i,j) \in I^2$ we write $U^d$ for $U^i \cap U^j$. We then have a coequaliser diagram of filtered spaces 

$$\bigsqcup_{d \in I^2} U^d_* \rightrightarrows ^a_b \bigsqcup _{i \in I} U^i_* \to ^c X_*.$$

+-- {: .un_theorem}
######Higher Homotopy van Kampen Theorem
If the filtered spaces $U^f_*$ are [[connected filtered space]]s for all finite intersections $U^f_*$ of the filtered spaces $U^i_*$, then
1. (Conn) The filtered space $X_*$ is connected; and
1. (Iso) The fundamental [[crossed complex]] functor $\Pi$ takes the above coequaliser diagram of filtered spaces to a coequaliser diagram of crossed complexes.
=--

# Remarks #

* Note that because $\Pi$ uses groupoids, it obviously takes disjoint unions $\bigsqcup$ of filtered spaces into disjoint unions (= coproducts) $\bigsqcup$ of crossed complexes. 

* The proof of the theorem is not direct but goes via the fundamental [[cubical omega-groupoid]] with connections of the filtered spaces, as that context allows the notions of _algebraic inverse to subdivision_ and of _commutative cube_. However the proof is a direct generalisation of a proof for the [[van Kampen theorem]] for the [[fundamental groupoid]].  

* Applications of this theorem include many basic facts in algebraic topology, such as the Relative Hurewicz Theorem, the Brouwer degree theorem, and new nonabelian results on 2nd relative homotopy groups, not of course obtainable by the traditional wholly abelian methods. No use is made of _singular homology theory_ or of _simplicial approximation_.

## Sample application ## 

Here is one application in dimension 2 not easily obtainable by traditional algebraic topology. Let $0 \to P \to Q \to R \to 0$ be an exact sequence of abelian groups. Let $X$  be the mapping cone of the induced map $K(P,1) \to K(Q,1)$ of [[Eilenberg-Mac Lane space]]s. Then a [[crossed module]] representing the [[homotopy 2-type]] of $X$ is $\mu: C \to Q$ where $C$ is abelian and is the direct sum $\oplus_{r \in R} P^r$  of copies of $P$ one for each $r \in R$ and the action of $Q$ is via $R$ and permutes the copies by $(p,r)^s=(p,r+s)$. Similar examples for $P,Q,R$ nonabelian are do-able,   more complicated, and certainly **not** obtainable by traditional methods.


[[!redirects Higher Homotopy van Kampen Theorem]]