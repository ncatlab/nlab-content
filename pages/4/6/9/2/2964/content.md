
Let $X\to Y$ be a [[groupoid scheme]] where both schemes are of finite type.  Then we can make two constructions from this scheme:

* The $\mathbb{F}_p$-points $X(\mathbb{F}_p)\to Y(\mathbb{F}_p)$ form a groupoid of finite sets.
* There is a simplicial scheme $X/Y$ sending $\Delta^n$ to $X\times_Y X\times_Y\cdots  \times_Y X$, with the obvious face and degeneracy maps.

  * One special case is when this is an action groupoid.  The resulting simplicial scheme should be thought of as the Borel space for the action on $Y$.

The latter construction can be "linearized" in an analogous way to [[geometric function theory]], except using the [[constructible derived category|derived category of sheaves with finite rank constructible cohomology]] of $X/Y$.  Let $D(X/Y)$ denote this category.  In fact, we will require the graded version of this category, provided by [[mixed sheaves]].  We denote this graded category $D_{mix}(X/Y)$  


There is a map $\alpha_{q,\ell}$ from $K^0(D_{mix}(X/Y)$ to the set of $\mathbb{Q}_\ell$ valued functions on any $\mathbb{F}_q$ point of $X/Y$ where $\ell$ and $q$ where $\ell$ is a prime and $\ell\nmid q$, given by the supertrace of automorphism of the stalk of the sheaf at that point induced by the action of the Frobenius $q^n$ on $X\times_{\mathrm{Spec}\mathbb{Z}}\times  \mathrm{Spec}\overline{\mathbb{F}_q}$.

This map has the property that multiplying by the motive of $\mathbb{A}^1$ (i.e., $m_!m^*$ for the map $m:X\times \mathbb{A}^1\to X$) multiplies the corresponding function by $q$.

Furthermore, no non-zero element of $K^0(D_{mix}(X/Y)$ is killed by this map for all  $q$.

If $X_1/Y_1\overset{f}\leftarrow Z/W \overset{g}\rightarrow X_2/Y_2$ is a span of groupoids of schemes, then we have a functor $g_!f^*:D_{mix}(X_1/Y_1)\to D_{mix}(X_2/Y_2)$, given by pull-back followed by compactly supported pushforward.

Furthermore, there is an induced span of groupoids on this set of $\mathbb{F}_q$-points, which in turn induces a map $(gf)^\dagger$ from $\mathbb{Q}_\ell[X_1/Y_1(\mathbb{F}_q)]\to \mathbb{Q}_\ell[X_2/Y_2(\mathbb{F}_q)]$.

The content of the [[Grothendieck trace formula]] connects these two constructions. 

+--{: .un_theorem}
If $X_1/Y_1\overset{f}\leftarrow Z/W \overset{g}\rightarrow X_2/Y_2$ is a span of groupoids of schemes, then the functor  $g_!f^*:D_{mix}(X_1/Y_1)\to D_{mix}(X_2/Y_2)$ induces a map $(gf)_\dagger:K^0(D_{mix}(X_1/Y_1))\to K^0(D_{mix}(X_1/Y_1))$ such that the diagram
$$
  \array{
      K^0(D_{mix}(X_1/Y_1))&\overset{(gf)_\dagger}\to& K^0(D_{mix}(X_2/Y_2))   \\
     \downarrow^{\alpha_{q,\ell}} && \downarrow^{\alpha_{q,\ell}} 
     \\
    \mathbb{Q}_\ell[X_1/Y_1(\mathbb{F}_q)] &\overset{(gf)^\dagger}\to& \mathbb{Q}_\ell[X_2/Y_2(\mathbb{F}_q)]
  }
$$
=--