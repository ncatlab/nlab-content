A **pseudo-Riemannian "metric"** is a nondegenerate [[quadratic form]] on a real vector space $\mathbb{R}^n$. A [[Riemannian metric]] is a positive-definite quadratic form on a real vector space. The data of such a quadratic form may be equivalently given by a nondegenerate symmetric bilinear pairing $\langle\, , \, \rangle$ on $\mathbb{R}^n$. 

A pseudo-Riemannian metric 

$$Q: \mathbb{R}^n \to \mathbb{R}$$ 

can always be diagonalized: there exists a basis $e_1, \ldots, e_n$ such that 

$$Q(\sum_{1 \leq i \leq n} x_i e_i) = x_1^2 + \ldots + x_p^2 - x_{p+1}^2 - \ldots - x_n^2$$ 

where the pair $(p, n-p)$ is called the **signature** of the form $Q$. Pseudo-Riemannian metrics on $\mathbb{R}^n$ are classified by their signatures; thus we have a standard metric of signature $(p, n-p)$ where $\{e_1, \ldots, e_n\}$ is the standard basis of $\mathbb{R}^n$. 

More generally, there is a notion of **pseudo-Riemannian manifold** (of type $(p, n-p)$, which is an $n$-dimensional [[manifold]] $M$ equipped with a global section 

$$\sigma: M \to S^2(T^* M)$$ 

of the bundle of symmetric bilinear forms over $M$, such that each $\sigma(x)$ is a nondegenerate form on the 
tangent space $T_x(M)$. 

Certain theorems of Riemannian geometry carry over to the more general pseudo-Riemannian setting; for example, pseudo-Riemannian manifolds admit [[Levi-Civita connection]]s, or in other words a unique notion of covariant differentiation 
of vector fields 

$$\nabla: (X, Y) \mapsto \nabla_X(Y)$$ 

such that 

$$X \cdot \langle Y, Z\rangle = \langle \nabla_X Y, Z\rangle + \langle Y, \nabla_X Z\rangle$$ 

$$[X, Y] = \nabla_X Y - \nabla_Y X$$ 

In that case, one may define a notion of [[geodesic]] in pseudo-Riemannian manifolds $M$, and we have a notion of "distance squared" between the endpoints along any geodesic path $\alpha: [0, 1] \to M$ (which might be a negative number of course). The term "pseudo-Riemannian metric" may refer to such distances in general pseudo-Riemannian manifolds. _(I guess.)_

+--{.query}

Is there an accepted notion of "distance squared" between two points in a pseudo-Riemannian manifold, in cases where there are multiple geodesics between them? How does one choose? (Edit: might one choose the value which is least in absolute value?) 

=--

A typical example of pseudo-Riemannian manifold is a [[Lorentzian manifold]], where the metric is of type $(1, n-1)$. This is particularly so in the case $n = 4$, where such manifolds are the mathematical backdrop for studying [[general relativity]] and cosmological models. 

* The terminology "metric" is not optimal of course: the values of the quadratic form would need to be nonnegative to avoid terminological conflict with [[metric space|metric]] as it is more commonly understood (and even in that case, the values of "metric" refer to the square of the metric rather than the metric itself). _Caveat lector._ 
