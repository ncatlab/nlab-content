A category $C$ with a class of arrows $W$ is said to admit a **category of right fractions** if

* $W$ is a [[wide subcategory]] of $C$
* Given an arrow $v:x\to z$ in $W$ and any arrow $f: y\to z$, there is an arrow $v':w \to x$ in $W$ and an arrow $f':w \to y$ in $C$ such that
$$
\begin{matrix}
  w& \stackrel{f'}{\to} & x \\
  v' \downarrow&&\, \downarrow v\\
  y &\underset{f}{\to} & z
\end{matrix}
$$
commutes
* Given an arrow $v:x\to y$ in $W$ and a pair of arrows $f,g: y\to z$ such that $f\circ v = g \circ v$, there is an arrow $v':w\to x$ in $W$ such that $v'\circ f = v' \circ g$.

If the above conditions hold, then the hom-sets of the [[localization]] of $C$ at $W$ are given by equivalence classes of [[span|spans]].

This definition is due to Gabriel-Zisman in the book _Categories of fractions and homotopy theory_, and also admits a dual version, a category of left fractions. Then the hom-sets are equivalence classes of cospans.