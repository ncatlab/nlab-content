## Definition in an additive category

Let $\mathcal{C}$ be an [[additive category]]; that is, $\mathcal{C}$ is enriched over [[abelian groups]]. For $A, B$ a [[pair]] of objects in $\mathcal{C}$, a biproduct ((#MacLane) p.194) is an object $A \oplus B$ together with maps

\begin{tikzcd}
A \arrow[rr, "i_{1}"', shift right] &  & A \oplus B \arrow[ll, "p_{1}"', shift right] \arrow[rr, "p_{2}", shift left] &  & B \arrow[ll, "i_{2}", shift left]
\end{tikzcd}

which satisfy the identities

$$
i_{1};p_{1}=1_{a}, \quad i_{2};p_{2}=1_{b}, \quad p_{1};i_{1} + p_{2};i_{2}
$$