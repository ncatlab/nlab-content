
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{: toc}


## Idea

The **Levi-Civita connection** is the unique symmetric [[connection on a bundle|connection]] on the [[tangent bundle]] of a [[Riemannian manifold]] or [[pseudo-Riemannian manifold]] that is compatible with the [[Riemannian metric|metric]] or [[pseudo-Riemannian metric|pseudo-metric]].  The [[curvature]] and [[geodesic]]s on a pseudo-Riemannian manifold are taken with respect to this connection.  The existence and uniqueness of the Levi-Civita connection is called the _[[fundamental theorem of Riemannian geometry]]_.

 
## Definition

+-- {: num_defn}
###### Definition

For $(X,g)$ a [[Riemannian manifold]], the **Levi-Civita connection** $\nabla_g$ on $X$ is the unique [[connection on a bundle|connection]] on the [[tangent bundle]] $T X$ that

1. the [[covariant derivative]] of the metric vanishes, $\nabla_{g} g = 0$;

1. $\nabla_g$ has vanishing [[torsion of a metric connection|torsion]].

=--

We say in detail what this means in "[[first order formulation of gravity|first order formalism]]"/[[Cartan geometry]].

+-- {: .num_defn}
###### Definition

For $(X,g)$ a $(d-k,k)$-[[dimension]]al [[Riemannian manifold]] (for $k = 0$) or [[pseudo-Riemannian manifold]] (for $k = 1$), the **Levi-Civita connection** $\nabla_g$ on $X$ is the unique $ISO(d-k,k)$-[[connection on a bundle]] $\nabla$ (for $ISO(d-k)$ the [[Poincare group]]) such that

1. **metric compatibility**:  the [[vielbein]] $e$ gives the metric: $g = e \cdot e$;

1. **torsion freeness**: the curvature of the vielbein (the [[torsion]]) vanishes: $T = 0$.


=--



More in detail, locally on a patch $U_i \subset X$ the $ISO(d-k,k)$-connection $\nabla$ is given by a [[Poincare Lie algebra]]-[[Lie algebra valued 1-form|valued 1-form]]

$$
  (e, \omega) : T U_i \to \mathfrak{iso}(d-k,k) \simeq \mathbb{R}^d \ltimes \mathfrak{so}(d-k,k) 
$$

with 

1. $e_i$ an $\mathbb{R}^d$-valued form -- the [[vielbein]];

1. $\omega_i$ a [[special orthogonal Lie algebra]]-valued form -- the "[[spin connection]]".

The [[curvature]] 2-form of this similarly decomposes into

1. the [[torsion]] $T^a := F_{e}^a = d e^a + \omega^a{}_b \wedge e^b$, 

   (this equation is also called the **first Cartan structure equation**)

1. the [[Riemann curvature]] $R_{g}{}^a{}_b := F_{\omega}^a{}_b = d \omega^a{}_b + \omega^a{}_c \wedge \omega^c{}_d$.

   (this equation is also called the **second Cartan structure equation**)

The [[Bianchi identity]] satisfied by this curvature is

1. $d F_e^a + \omega^a{}_b \wedge F_e^b = F_\omega^a{}_b \wedge e^b$;

1. $d F_\omega^a{}_b + \omega^a{}_c \wedge F_\omega^c{}_b - F_\omega^a{}_c \wedge \omega^c{}_b = 0$.

The metric compatibility condition in the definition of Levi-Civita connection says that

$$
  g = e^a \otimes e_a
  \,.
$$

The torsion-freeness condition says that

$$
  F_e = 0
  \,.
$$





## In terms of Christoffel symbols

The Levi-Civita connection may be discussed in terms of its components -- called [[Christoffel symbol]]s -- given by the canonical local trivialization of the [[tangent bundle]] over a coordinate patch. This has been the historical route and is still widely used in the literature.

**Metric compatibility**

Here a metric $g$ is **compatible** with the connection $\nabla$ or _preserved_ by it (here thought of in its incarnation as a [[covariant derivative]]) if and only if $\nabla_X g = 0$ for all $X$, which is equivalent to the preservation of the metric inner product of tangent vectors under [[parallel transport|parallel translation]].  Since 
\[ X(g(X_1,X_2))  = (\nabla_X g)(X_1,X_2) + g(\nabla_X X_1, X_2) + g(X_1, \nabla_X X_2) ,\]
by the fact that covariant differentiation commutes with contractions and satisfies the derviative identity, compatibility is equivalent to 
\begin{equation}  X (g (X_1,X_2)) = g(\nabla_X X_1, X_2) + g(X_1, \nabla_X X_2),\end{equation}
for all  $X,X_1, X_2$.



**Uniqueness and existence on $\mathbb{R}^n$**

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


**Uniqueness and existence in the general case**

We have already shown the uniqueness assertion, since that is local.  Connections restrict to connections on open subsets. 

We have proved the existence of $\nabla$ when $M$ is an open submanifold of $\mathbb{R}^n$ (though not necessarily with the canonical metric $\sum_{i=1}^n d x_i \otimes d x_i$).  In general, cover $M$ by open subsets $U_i$ diffeomorphic to an open set in $\mathbb{R}^n$.  We get connections $\nabla_i$ on $U_i$ compatible with $g|_{U_i}$.  

We claim that $\nabla_i|_{U_i \cap U_j} = \nabla_j|_{U_i \cap U_j}$.  This is an easy corollary of uniquness.  So we can patch the connections together to get the one  Levi-Civita connection on $M$.



## Applications 

### In physics

In the [[physics]], the theory of [[general relativity]] models the field of [[gravity]] in terms of the Levi-Civita connection on a [[Lorentzian manifold]]. See there for more details.

## Related concepts

* [[Weitzenböck connection]]

* [[connection on a bundle]]

  * [[parallel transport]], [[holonomy]]

* [[principal connection]]

  * [[affine connection]], **Levi-Civita connection**, [[Cartan connection]]

* [[connection on a 2-bundle]]

* [[connection on an infinity-bundle]]

  * [[higher parallel transport]]




## References

A discussion in terms of [[synthetic differential geometry]] is in 

* [[Gonzalo Reyes]], _General Relativity: 

  _Metrics, connections and curvature_ ([pdf](http://po-start.com/reyes/wp-content/uploads/2007/01/metrics.pdf))

  _The Riemann-Christoffel tensor_ ([pdf](http://po-start.com/reyes/wp-content/uploads/2007/01/the-riemann-christoffel-tensor.pdf))

  _Affine connections, parallel
transport and sprays_ ([pdf](http://po-start.com/reyes/wp-content/uploads/2009/01/affineconnections.pdf))


[[!redirects Levi-Civita connections]]
[[!redirects metric connecitons]]
