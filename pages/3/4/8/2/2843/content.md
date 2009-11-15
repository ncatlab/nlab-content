# Levi-Civita connection
* tic
{: toc}

The **Levi-Civita connection** is the unique symmetric [[connection]] on the [[tangent bundle]] of a [[pseudo-Riemannian manifold]] that is compatible with the pseudo-metric.  The [[curvature tensor]] and [[geodesic]]s on a pseudo-Riemannian manifold are taken with respect to this connection.  The existence and uniqueness of the Levi-Civita connection is the so-called **fundamental theorem of Riemannian geometry.**

 
##Definition of Compatibility##

The pseudo-metric $g$ is **compatible** with the connection $\nabla$ if and only if $\nabla_X g = 0$ for all $X$, which is equivalent to the preservation of inner products of tangent vectors under parallel translation.  Since 
\[ X(g(X_1,X_2))  = (\nabla_X g)(X_1,X_2) + g(\nabla_X X_1, X_2) + g(X_1, \nabla_X X_2) ,\]
by the fact that covariant differentiation commutes with contractions and satisfies the derviative identity, compatibility is equivalent to 
\begin{equation}  X (g (X_1,X_2)) = g(\nabla_X X_1, X_2) + g(X_1, \nabla_X X_2),\end{equation}
for all  $X,X_1, X_2$.


##Uniqueness and existence on $\mathbb{R}^n$##

Now assume $M \subset \mathbb{R}^n$ and we have such a connection associated to $g$.  
Then the connection is uniquely determined by its [[Christoffel symbols]], which we can determine in terms of $g$ by a bit of elementary algebra.
In other words, we just need to compute $\nabla_{\partial_i} \partial_j$.
Now
\[ \partial_k g( \partial_i, \partial_j) = g( \nabla_{\partial_k} \partial_i, \partial_j) + g(  \partial_i, \nabla_{\partial_k}\partial_j).\]
We can get two other equations by cyclic permutation:
\[ \partial_i g( \partial_j, \partial_k) = g( \nabla_{\partial_i} \partial_j, \partial_k) + g(  \partial_j, \nabla_{\partial_i}\partial_k)\]
\[ \partial_j g( \partial_k, \partial_i) = g( \nabla_{\partial_j} \partial_k, \partial_i) + g(  \partial_k, \nabla_{\partial_j}\partial_i)\]
So let $S_{i j} := \nabla_{\partial_i} \partial_j = \nabla_{\partial_j} \partial_i$, by symmetry.
Let $T_{i j k} := \partial_i g( \partial_j, \partial_k)$; these are smooth real functions.
These equations can be written
\[ T_{k i j} = g( S_{i k}, \partial_j) + g( S_{j k}, \partial_i) \]
\[ T_{i j k} = g( S_{i j}, \partial_k) + g( S_{i k}, \partial_j) \]
\[ T_{j k i} = g( S_{j k}, \partial_i) + g( S_{i j}, \partial_k) \]
These are three linear equations in the unknowns 
$g( S_{i k}, \partial_j),   g( S_{j k}, \partial_i), g( S_{i j}, \partial_k)$.  The system is nonsingular, so we get a unique solution, and consequently by nondegeneracy a unique possibility for the $S_{i j}$.  

Incidentally, we have in fact shown the uniqueness assertion of the general theorem, since that is local.

We shall now prove existence in this restricted case.  Choose $S_{i j}$ to satisfy the system of three equations outlined above where $i \lt j \lt k$.  Then set $S_{j i} := S_{i j}$, and we have a connection $\nabla$ with $\nabla_{\partial_i} \partial_j := S_{i j}$ since the vector fields $\partial_i$ are a frame (i.e. a basis at each tangent space on $M$).
It is symmetric, since the torsion $T$ vanishes (by $S_{i j}=S_{j i}$) on pairs $(\partial_i,\partial_j)$, and hence identically, since it is a tensor.  

We must check for compatibility.
The difference of the two terms in (1) vanishes when $X,X_1,X_2$ are of the form $\partial_i$.  The vanishing holds generally because the difference of the two sides, which is $(\nabla_X g)(X_1,X_2)$, is a tensor.  Hence compatibility follows.


##Uniqueness and existence in the general case##

We have already shown the uniqueness assertion, since that is local.  Connections restrict to connections on open subsets. 

We have proved the existence of $\nabla$ when $M$ is an open submanifold of $\mathbb{R}^n$ (though not necessarily with the canonical metric $\sum_{i=1}^n d x_i \otimes d x_i$).  In general, cover $M$ by open subsets $U_i$ diffeomorphic to an open set in $\mathbb{R}^n$.  We get connections $\nabla_i$ on $U_i$ compatible with $g|_{U_i}$.  

We claim that $\nabla_i|_{U_i \cap U_j} = \nabla_j|_{U_i \cap U_j}$.  This is an easy corollary of uniquness.  So we can patch the connections together to get the one  Levi-Civita connection on $M$.