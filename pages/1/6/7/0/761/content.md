For the van Kampen theorem for the [[fundamental groupoid]] it is convenient to define $\pi_1(X,A)$ of a space $X$ and a set $A$ to be the full subgroupoid of $\pi_1 X$ on the set $X \cap A$. 

Suppose $X$ is the union of the interiors of subsets  $U_i$, $i \in I$. For a finite subset $F$ of $I$ let $U_F$ be the intersection of the sets $U_i, i \in F$. Suppose $I$ has a total order. Then we have two morphisms $a,b: \bigsqcup _{|F|=2} \pi_1(U_F,A) \to \bigsqcup _{|F|=1} \pi_1(U_F,A)$ induced by the inclusions into the first and second of the $U_i$s. let $c:\bigsqcup _{|F|=1} \pi_1(U_F,A) \to \pi_1(X,A)$ be induced by the inclusions. 

+--{.un_thm}
######Van Kampen Theorem.
_If $A$ meets each path component of each three-fold intersection of the $U_i$ then (Conn) $A$ meets each path-component of $X$; and (Iso) $c$ is the coequaliser of $a,b$ in the category of groupoids._
=--

Note:

1. _three-fold_ here includes two- and one-fold! 

1. Emphasising the connectivity result becomes more  important for higher dimensional versions. 

 

