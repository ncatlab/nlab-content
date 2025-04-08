## Idea 

A projective frame is a choice of tuple of points in a projective space which enables one to define homogeneous coordinates. 

It is an analogue of a vector space basis/frame and affine frame in a (finite dimensional) projective space. 
 
A basis in a $n$-dimensional vector space has $n$ elements, an affine frame has $(n+1)$-points of an affine space but the projective frame has $(n+2)$ points. 

Let $p:V\backslash \{0\}\to P(V)$ be the canonical projection. Different basis $(e_1,\ldots,e_{n+1})$ which lift an $(n+1)$-tuple $(p_1,\ldots,p_{n+1})=(p(e_1),\ldots, p(e_n))$ of points in $P(V)$ to the vector space $V$ do not yield proportional coordinates $(v^1,\ldots,v^n)$ of a lift $v$ of $x = p(v)\in P(V)$. Indeed, if $(\lambda_1 e_1,\ldots,\lambda_n e_n)$ is another lift, then the new coordinates of $v$ are $(v^1/\lambda_1,\ldots,v^n/\lambda_n)$. Thus  one adds an additional point $p_0$ which will have coordinates $(1,\ldots,1)$ to fix the problem.

## Definition

$(n+1)$-tuple $(p_0,p_1,\ldots,p_{n+1})$ of points in $P(V)$ are a projective frame if there is a $(e_1,\ldots,e_{n+1})$ of $V$ which lifts $(p_1,\ldots,p_{n+1})$
along the projection $p:V\backslash \{0\}\to P(V)$
and such that $p_0 = p(e_1+\ldots+e_{n+1})$. 

This is equivalent to the statement that for any $i\in\{0,1,\ldots,n+1\}$ the set $\{p_j|j\neq i\}$ lifts to a linearly independent family of vectors in $V$ (independence clearly does not depend on a choice of lifts). 

## Homogeneous coordinates

### In P(V)

Given a projective frame choose any basis $(e_1,\ldots,e_{n+1})$ lifting $(p_1,\ldots,p_{n+1})$ and satisfying $p_0 = p(e_1+\ldots+e_{n+1})$. The dependence of the coordinates of a lift $v$ of an $x\in P(V)$ on the lift are up to an overall constant only. Thus they define homogeneous coordinates, that is a line in $P(K^{n+1})$, and the correspondence $x\mapsto [v_1,\ldots,v_{n+1}]$ amounts to a choice of an isomorphism $P(V)\cong P(K^{n+1})$ where $K$ is the ground (skew)field. 



category: geometry
