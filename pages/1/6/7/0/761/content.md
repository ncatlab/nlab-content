


For the van Kampen theorem for the [[fundamental groupoid]] it is convenient to define $\pi_1(X,X_0)$ of a space $X$ and a set $X_0$ to be the full subgroupoid of $\pi_1 X$ on the set $X \cap X_0$. Suppose $X_* =(X,X_0)$ is a pair consisting of a space $X$ and a set $X_0$ of base points. We say $X_*$ is _connected_ if $X_0$ meets each path component of $X$. 


Let  $X$ be the union of the interiors of sets $U^i$, $i \in I$.  If $d=(i,j) \in I^2$ we write $U^d$ for $U^i \cap U^j$, and  let $U^e_*$ be the pair $(U^e,X_0 \cap U^e)$, $e \in I \cup I^2$.  We then have a [[coequaliser]] diagram of pairs of  spaces where $a,b,c$ are determined by inclusions: 

$$\bigsqcup_{d \in I^2} U^d_* \rightrightarrows ^a_b \bigsqcup _{i \in I} U^i_* \to ^c X_*.$$


##van Kampen theorem## 

If the pairs of  spaces $U^f_*$ are  connected for all 1-,2-, or 3-fold  intersections $U^f_*$ of the pairs $U^i_*$, then
1. (Conn) The pair  $X_*$ is connected; and
1. (Iso) The [[fundamental groupoid]] functor $\pi_1$ takes the above coequaliser diagram of pairs of  spaces to a coequaliser diagram of groupoids.


## Notes## 

1. Emphasising the connectivity result becomes more  important for [[higher homotopy van Kampen theorem]]s. 

1. This uses the idea of Lebesgue covering dimension to reduce to the 3-fold intersection condition.  

1. Naturally the proof can and should go by verifying the universal property for a coequaliser. The  basic techniques of the proof include: subdivide a path;  deform a subdivision so that it is product of paths joining points of $X_0$; subdivide a homotopy rel end points, and deform this subdivision so that _all_ subpaths join points of $X_0$; any composition of [[commutative square]]s in a groupoid is commutative.  