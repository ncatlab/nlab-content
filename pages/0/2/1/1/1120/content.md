#Definition#

A [[category]] $C$ with a class of [[morphism]]s $W$ is said to admit a **category of right fractions** if

* $W$ is a [[wide subcategory]] of $C$
* Given an arrow $v:x\to z$ in $W$ and any arrow $f: y\to z$, there is an arrow $v':w \to y$ in $W$ and an arrow $f':w \to x$ in $C$ such that
$$
\begin{matrix}
  w& \stackrel{f'}{\to} & x \\
  v' \downarrow&&\, \downarrow v\\
  y &\underset{f}{\to} & z
\end{matrix}
$$
commutes
* Given an arrow $v:x\to y$ in $W$ and a pair of [[parallel morphisms]] $f,g: y\to z$ such that $f\circ v = g \circ v$, there is an arrow $v':w\to x$ in $W$ such that $v'\circ f = v' \circ g$.

If the above conditions hold, then the [[hom-set]]s of the [[localization]] of $C$ at $W$ are given by equivalence classes of [[span|spans]].

#Remarks#

* This definition has a [[duality|dual]] version, a category of left fractions. Then the [[hom-set]]s are equivalence classes of [[cospan]]s.


#References#

The above definition is due to Gabriel-Zisman in the book 

* Gabriel-Zisman, _Categories of fractions and homotopy theory_



+-- {: .query}

[[Urs Schreiber|Urs]]: there is overlap/duplication here with the entry [[multiplicative system]]. The only difference in the axioms seems to be that in a [[multiplicative system]] all isomorphisms are required to be included.

we should probably merge the entries and make one a redirect to the other, or something -- any opinions?

=--