# Idea #

A **pro-object** of a category $C$ is a "formal [[filtered category|cofiltered]] limit" of objects of $C$.  The category of pro-objects of $C$ is written $pro$-$C$. It is sometimes called a 'pro-category'.

"Pro" is short for "projective limit," an old term for a [[limit]], as contrasted with "ind" in the [[ind-object|dual notion]] for "inductive limit," the old term for [[colimit]].

# Definition #

There are many ways to make this notion precise.  One is to define the objects of $pro$-$C$ to be diagrams $F:D\to C$ where $D$ is a [[small category|small]] [[filtered category|cofiltered]] category.  The set of morphisms between $F:D\to C$ and $G:E\to C$ is then defined to be

\[pro\text{-}C(F,G) = lim_{e\in E} colim_{d\in D} C(F d, G e)\]

This definition is perhaps more intuitive in the dual case of [[ind-object|ind-objects]] (pro-objects in $C^{op}$), where it can be seen as stipulating that the objects of $C$ are [[finitely presentable object|finitely presentable]] in $ind$-$C$.

Another, equivalent, definition is to let $pro$-$C$ be the [[full subcategory]] of $[C,Set]^{op}$ determined by those functors which are cofiltered limits of representables.  This is reasonable since $[C,Set]^{op}$ is the [[free completion]] of $C$, so $pro$-$C$ is the "free completion of $C$ under cofiltered limits."

##References##
One source for the theory of pro-objects is

* J.-M. Cordier and T. Porter, 2008, Shape Theory, categorical methods of approximation, Dover.

(I might as well get a plug in!!  It is a reprint of the 1989 edition without amendments.)

Another good reference is

* P. T. Johnstone, _Stone Spaces_.
