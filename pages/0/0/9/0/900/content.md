

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

A **pro-object** of a category $C$ is a "formal [[filtered category|cofiltered]] limit" of objects of $C$.  The category of pro-objects of $C$ is written $pro$-$C$. Such a category is sometimes called a 'pro-category', but notice that that is *not* the same thing as a pro-object in [[Cat]].

"Pro" is short for "projective limit," an old term for a [[limit]], as contrasted with "ind" in the [[ind-object|dual notion]] for "inductive limit," the old term for [[colimit]].

## Definition 

There are many ways to make this notion precise.  One is to define the objects of $pro$-$C$ to be diagrams $F:D\to C$ where $D$ is a [[small category|small]] [[filtered category|cofiltered]] category.  The set of morphisms between $F:D\to C$ and $G:E\to C$ is then defined to be

\[pro\text{-}C(F,G) = lim_{e\in E} colim_{d\in D} C(F d, G e)\]

This definition is perhaps more intuitive in the dual case of [[ind-object|ind-objects]] (pro-objects in $C^{op}$), where it can be seen as stipulating that the objects of $C$ are [[finitely presentable object|finitely presentable]] in $ind$-$C$.

Another, equivalent, definition is to let $pro$-$C$ be the [[full subcategory]] of $[C,Set]^{op}$ determined by those functors which are cofiltered limits of representables.  This is reasonable since the [[presheaf category|copresheaf category]] $[C,Set]^{op}$ is the [[free completion]] of $C$, so $pro$-$C$ is the "free completion of $C$ under cofiltered limits."

## Related concepts

* [[ind-object]] / [[ind-object in an (∞,1)-category]]

* **pro-object** / [[pro-object in an (∞,1)-category]]

## References

One source for the theory of pro-objects is

* J.-M. Cordier and [[Tim Porter]],  _Shape Theory_ , categorical methods of approximation, Dover (2008)

(It is a reprint of the 1989 edition without amendments.)

Another good reference is

* [[Peter Johnstone]], _[[Stone Spaces]]_.


[[!redirects pro-objects]]
