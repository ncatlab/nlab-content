# Idea #

An **ind-object** of a category $C$ is a "formal [[filtered category|filtered]] colimit" of objects of $C$.  The category of ind-objects of $C$ is written $ind$-$C$.

"Ind" is short for "inductive limit," an old term for a [[colimit]], as contrasted with "pro" in the [[pro-object|dual notion]] for "projective limit," the old term for [[limit]].

# Definition #

There are many ways to make this notion precise.  One is to define the objects of $ind$-$C$ to be diagrams $F:D\to C$ where $D$ is a [[small category|small]] [[filtered category|filtered]] category.  We identify an ordinary object of $C$ with the corresponding diagram $1\to C$.  To see what the morphisms should be between $F:D\to C$ and $G:E\to C$, we stipulate that

1. The embedding $C\to ind$-$C$ should be full and faithful,
1. each diagram $F:D\to C$ should be the colimit of itself (considered as a diagram in $ind$-$C$ via the above embedding), and
1. the objects of $C$ should be [[finitely presentable object|finitely presentable]] in $ind$-$C$.

Thus, we have

$$
\begin{aligned}
  ind\text{-}C(F,G) &= ind\text{-}C(colim_{d\in D} F d, colim_{e\in E} G   e)\\
   &\cong lim_{d\in D}\; ind\text{-}C(F d, colim_{e\in E} G \\
   &\cong lim_{d\in D} colim_{e\in E}\; ind\text{-}C(F d, G e)\\
   &\cong lim_{d\in D} colim_{e\in E}\; C(F d, G e)
\end{aligned}$$

Another, equivalent, definition is to let $ind$-$C$ be the [[full subcategory]] of the presheaf category $[C^{op},Set]$ determined by those functors which are filtered colimits of representables.  This is reasonable since $[C^{op},Set]$ is the [[free cocompletion]] of $C$, so $ind$-$C$ defined in this way is its "free cocompletion under filtered colimits."
