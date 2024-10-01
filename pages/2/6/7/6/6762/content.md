\tableofcontents

## Idea 

Day's reflection theorem &lbrack;[Day (1972)](#Day72)&rbrack; gives conditions under which a [[reflective subcategory]] of a [[symmetric monoidal closed category]] is closed under [[internal homs]]. 

One memorable consequence of the theorem is that the subcategory is closed under [[internal homs]] if the [[reflector]] is symmetric [[strong monoidal functor|strong monoidal]]. 

## Statement and Proof

\begin{theorem} (Day)
Let $R: C \to D$ be a [[fully faithful functor]] with [[left adjoint]] $L \colon D \to C$, and suppose given a symmetric monoidal closed structure on $D$ with tensor $\otimes$ and internal hom $[-, -]$. Then for objects $c$ of $C$ and $d, d'$ of $D$, the following are equivalent: 

1. $u[d, R c] \colon [d, R c] \to R L[d, R c]$ is an isomorphism; 

1. $[u, 1] \colon [R L d, R c] \to [d, R c]$ is an isomorphism; 

1. $L(u \otimes 1) \colon L(d \otimes d') \to L(R L d \otimes d')$ is an isomorphism; 

1. $L(u \otimes u) \colon L(d \otimes d') \to L(R L d \otimes R L d')$ is an isomorphism. 

\end{theorem}

Some remarks before the proof: 

* (a) Since $R$ is fully faithful, the [[monad]] $R L$ is [[idempotent monad|idempotent]]. Consequently, $R: C \to D$ is [[monadic functor|monadic]], and algebra structures on an object $d$ are unique when they exist. This makes algebra structure on $d$ a [[stuff, structure, property
|property]], that $d \cong R c$ for some $c$ in $C$, unique up to isomorphism. Call this property "being in $C$". Thus condition $\text{1.}$ says that $[d, d']$ is in $C$ for a particular $d' \cong R c$ in $C$. (If $D$ is [[cartesian closed category|cartesian closed]] and $[d, d'] \in C$ whenever $d' \in D$, we say $C$ is an [[exponential ideal]] in $D$.) Notice that all $D$-maps between objects in $C$ are algebra maps, by full faithfulness of $R$. 

* (b) If $d$ is in $C$, then for any $d'$ the unit $u\colon d' \to R L d'$ induces an isomorphism $D(R L d', d) \cong D(d', d)$, since every $f \in D(R L d', d)$ is an algebra map $R L d' \to d$ and $R L d'$ is the [[free object|free algebra]] on $d'$. 

\begin{proof} 
We prove $\text{3.} \Rightarrow \text{4.} \Rightarrow \text{1.}\; \Rightarrow\; \text{3.}$, and then $\text{2.} \Leftrightarrow \text{3.}$. Some parts are merely sketched; refer to Day for full details. 

$\text{3.}\; \Rightarrow\; \text{4.}$ is obvious from the symmetric structure and 

\begin{center}
\begin{tikzcd}
L(d \otimes d') \ar[rr, "L(u \otimes u)"] \ar[dr, swap, "L(u \otimes 1)"] 
& & L(R L d \otimes R L d') \\ 
& L(R L d \otimes d') \ar[ur, swap, "L(1 \otimes u)"] &
\end{tikzcd} 
\end{center} 

$\text{4.} \Rightarrow \text{1.}$ is proven by giving an algebra structure $R L[d, R c] \to [d, R c]$, obtained by [[currying]] the following composite:  

\begin{tikzcd} 
R L[d, R c] \otimes d 
\ar[r, "1 \otimes u"] 
& R L[d, R c] \otimes R L d 
\ar[r, "u"] 
& R L(R L[d, R c] \otimes R L d) 
\ar[r, "R (L(u \otimes u)^{-1})"] 
& R L([d, R c] \otimes d) 
\ar[r, "R L eval"] 
& R L R c 
\ar[r, "\cong"] 
& R c
\end{tikzcd} 

 
(by idempotence of $R L$, to prove this map is an algebra structure, it suffices to show it is left inverse to the unit). 

$\text{1.} \Rightarrow \text{3.}$ is proven by considering the diagram 

\begin{tikzcd} 
C(L(R L d \otimes d'), c) 
\ar[r, "{C(L(u \otimes 1), 1)}"] 
\ar[d, "\cong"] 
& C(L(d \otimes d'), c) 
\ar[d, "\cong"] 
\\ 
D(R L d \otimes d', R c) \ar[r, "{D(u \otimes 1, 1)}"] \ar[d, "\cong"] & D(d \otimes d', R c) \ar[d, "\cong"] \\ 
D(R L d, [d', R c]) \ar[r, "{D(u, 1)}"] \ar[d, swap, "{D(1, u)}"] & D(d, [d', R c]) \ar[d, "{D(1, u)}"] \\ 
D(R L d, R L[d', R c]) \ar[r, "{D(u, 1)}"] & D(d, R L[d', R c]) 
\end{tikzcd}

which commutes by functoriality and naturality, and where the maps labeled $D(1, u)$ are isomorphisms by assuming $\text{1.}$, and the bottom map labeled $D(u, 1)$ is an isomorphism by invoking remark (b). It follows that the top horizontal map is also an isomorphism. Since this holds for all objects $c$ of $C$, the map $L(u \otimes 1)$ is an isomorphism by the Yoneda lemma, so that $\text{4.}$ holds. 

Finally, $\text{2.} \Leftrightarrow \text{3.}$ is proven by considering the diagram 

\begin{tikzcd} 
C(L(R L d \otimes d'), c) 
\ar[r, "{C(L(u \otimes 1), 1)}"] 
\ar[d, "\cong"] 
& C(L(d \otimes d'), c) 
\ar[d, "\cong"] 
\\ 
D(R L d \otimes d', R c) \ar[r, "{D(u \otimes 1, 1)}"] \ar[d, "\cong"] & D(d \otimes d', R c) \ar[d, "\cong"] \\ 
D(d', [R L d, R c]) \ar[r, "{D(1, [u, 1])}"] & D(d', [d, R c]) 
\end{tikzcd}

and again applying a Yoneda lemma argument. \end{proof} 

## Consequences 

\begin{corollary} 
If $L$ is a strong [[symmetric monoidal functor]], then for any $c$ in $C$ and $d$ in $D$, the internal hom $[d, c]$ is in $C$. 
\end{corollary} 

\begin{proof} 
Full faithfulness of $R$ is equivalent to the [[counit]] $\varepsilon \colon L R \to 1_C$ being an isomorphism. By a [[triangle identity]], this forces $L u$ to be an isomorphism for any unit $u: d \to R L d$. This in turn forces the arrow $L(u \otimes u)$ in the diagram 

\begin{tikzcd} 
L d \otimes L d' \ar[r, "L u \otimes L u"] \ar[d] & L R L d \otimes L R L d' \ar[d] \\ 
L(d \otimes d') \ar[r, "L(u \otimes u)"] & L(R L d \otimes R L d') 
\end{tikzcd} 
to be an isomorphism, where the vertical arrows are invertible symmetry constraints and the maps $L u$ are isomorphisms. Now apply the equivalence between $\text{4.}$ and $\text{1.}$ from the reflection theorem. 
\end{proof} 

\begin{corollary} 
If $D$ is cartesian closed, and the reflector $L \colon D \to C$ preserves products, then $C$ is cartesian closed. Conversely, if $C$ is cartesian closed and $C \to D$ is a [[dense functor]], then the reflector preserves products.
\end{corollary} 

\begin{proof} 
We have already seen under the hypotheses that if $c, c'$ are in $C$, then the exponential $c^{c'}$ as calculated in $D$ is in $C$. Furthermore, $C$ inherits products from $D$, because $R \colon C \to D$ is monadic and monadic functors reflect limits. The adjunction $C(c'' \times c', c) \cong C(c'', c^{c'})$ holds because it holds when interpreted in $D$ and $C$ is fully embedded in $D$.

For the converse, see Theorem 3.10 of [Street 1980](#Street80).
\end{proof} 

## Reference 

* {#Day72} [[Brian Day]], *A reflection theorem for closed categories*, Journal of Pure and Applied Algebra **2** 1 (1972), 1-11. &lbrack;<a href="https://doi.org/10.1016/0022-4049(72)90021-7">doi:10.1016/0022-4049(72)90021-7</a>&rbrack;

* {#Street80} [[Ross Street]], *Cosmoi of internal categories*, Transactions of the American Mathematical Society **258** 2 (1980) 271-318 &lbrack;[doi:10.2307/1998059](https://doi.org/10.2307/1998059)&rbrack;

A version for [[skew monoidal categories]] is given in:

* [[Steve Lack]] and [[Ross Street]], _Skew-monoidal reflection and lifting theorems_, Theory & Applications of Categories 30 (2015).
