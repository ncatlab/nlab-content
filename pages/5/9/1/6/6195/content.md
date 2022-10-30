
Let $L$ be a finite dimensional Lie algebra over real or complex numbers with basis $\hat{x}_1,\ldots,\hat{x}_n$ and let $x_1,\ldots, x_n$ be the corresponding basis of the symmetric algebra $S(L)$ via the identity and $U(L)$ the [[universal enveloping algebra]] of $L$. Given any $y\in L\hookrightarrow U(L)$ by $\hat{y}$ we denote the same element understood in $L\hookrightarrow S(L)$. This correspondence extends to a coalgebra isomorphism $e: S(L)\to U(L)$, the [[coexponential map]] (or symmetrization map)

$$
e : y_1 \ldots y_k \mapsto \frac{1}{k!}\sum_{\sigma\in \Sigma(k)} \hat{y}_{\sigma 1}\cdots \hat{y}_{\sigma k}
$$

for any $y_1,\ldots, y_n\in L\hookrightarrow S(L)$ (not necessarily basis elements). The coexponential map is the only functorial in $L$ isomorphism of coalgebras and it fixes $k\otimes L$ where $k$ is the ground field. It is also characterized $y^n\mapsto (\hat{y})^n$, where $y\in L\hookrightarrow S(L)$.

The Ra&#353;evskii [[hyper-envelope of a Lie algebra]] $L$ is a completion of $U(L)$ by means of a countable family of norms $\hat{f}\mapsto \|\hat{f}\|_{\epsilon}$ for all $\epsilon$ in an arbitrary fixed family of positive numbers having $0$ as  an accumulation points, where
 
$$
\| \hat{f}\|_{\epsilon} = max_{s_1,\ldots, s_n}\epsilon^{-s} |f_{s_1\ldots s_n}|,
$$ 

for $s_1\plus\cdots \plus s_N = s$, and where   $f_{s_1,\ldots,s_n}$ is the Taylor coefficient in front of $x_1^{s_1}\cdots x_n^{s_n}$ of the commutative polynomial $f = e^{-1}(\hat{f})$. Here $x_1,\ldots, x_n$ is a fixed basis of $L$, viewed as commutative coordinates.

It is nontrivial and proved by Ra&#353;evskii that the algebra multiplication in $U(L)$ is continuous in this topology and hence that the completion of the $U(L)$ as a countably normed vector space carries the unique structure of a topological algebra extending the algebra operations on $U(L)$.  

* P. K. Ra&#353;evskii, _Associative hyper-envelopes of Lie algebras, their regular representations and ideals_, Trudy Mosk. Mat. Ob.

It may be tried to use the same definition with $e$ replaced by another coalgebra isomorphism $S(L)\to U(L)$. 

Remark: It is announced (by author of these lines [[Zoran Škoda|ZŠ]], June 11, 2011), that under mild conditions this modified definition results in the isomorphic completion of $U(L)$ as a topological algebra. 


There is also an non-Archimedean version of the notion in the literature. 


