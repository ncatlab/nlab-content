###Idea###
Given a finite dimensional (pseudo-)Euclidean vector space $V$, the Hodge star operator "completes" a $k$-differential form to the [[volume form]] of $V$. 

###Definition###
Let $(V,g)$ be an $n$-dimensional real vector space endowed with a nondegenerate symmetric bilinear form $g$. The **Hodge star operator** is the linear operator $\wedge^k V^*\to \wedge^{n-k}V^*$ defined by the identity
$$
\alpha\wedge *\beta= (\alpha|\beta)_g vol_g, \qquad \forall\alpha,\beta\in \wedge^k V^*,
$$
where $(\,|\,)$ is the nondegenerate symmetric bilinear form induced by $g$ on $\wedge^k V^*$ and $vol_g$\in wedge^n V^*$ is the [[volume form]] induced by $g$.

If $e_1,\dots, e_n$ is a basis of $V$ and $e^1,\dots, e^n$ is the dual basis, so that $\alpha=\frac{1}{k!}\alpha_{i_1\dots i_k}e^{i_1}\wedge\cdots \wedge e^{i_k}$, then
$$
*\alpha=\frac{1}{k!(n-k)!}\epsilon_{i_1,\dots, i_n}\sqrt{det(g)} \alpha_{j_1\dots j_k} g^{i_1 j_1}\cdots g^{i_k j_k} e^{i_{k+1}}\wedge\cdots\wedge e^{i_n},
$$ 
where $\epsilon_{i_1,\dots,i_n}$ is sign of the permutation $(1,2,\dots,n)\mapsto (i_1,i_2,\dots, i_n)$.