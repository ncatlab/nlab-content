A twisting function is an analogue of a [[twisting cochain]] in the context of [[simplicial set]]s. 

Let $X_\bullet$ be a simplicial set and $G_\bullet$ a simplicial group. Then a __twisting function__ $\phi :X_\bullet\to G_\bullet$ is a family of maps $\phi=\{\phi_n : X_n\to G_{n-1}\}_{n\gt 1}$ such that

$$\array{
d_0 \phi(x) = (\phi(d_0 x))^{-1} \phi(d_1 x)\\
d_i \phi(x) = \phi(d_{i+1}x), i\gt 0,\\
s_i\phi(x) = \phi(s_{i+1}x), i\geq 0,\\
\phi(s_0 x) = 1_G.
}$$

Given a simplicial set $F_\bullet$ with left $G_\bullet$-action, one then defines a __twisted Cartesian product__ $X_\bullet \times_\phi F_\bullet$ with
$(X_\bullet \times_\phi F_\bullet)_n = X_n\times F_n$ and
$$\array{
d_i(x,f) = (d_i x, d_i f), i\gt 0\\
d_0 (x,f) = (d_0 x, \phi(x)(d_0 f)),\\
s_i(x,y) = (s_i x,s_i y).
}$$
Thus the only difference from the usual Cartesian product of simplicial sets is in $d_0$. 