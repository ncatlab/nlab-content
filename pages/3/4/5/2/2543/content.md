<div class="rightHandSide toc">
[[!include synthetic differential geometry - contents]]
</div>


Every [[lined topos]] $(\mathcal{T}, R)$ has a canonical [[cosimplicial object]]

$$
  \Delta_{\mathcal{T}} : \Delta \to \mathcal{T}
$$

given by the [[simplex in a lined topos|standard simplices in the lined topos]].

This induces a functor

$$
  \Pi : \mathcal{T} \to [\Delta^{op},\mathcal{T}]
$$

from $\mathcal{T}$ to [[simplicial object]]s in $\mathcal{T}$ given by

$$
  \Pi(X) := X^{\Delta^n_{\mathcal{T}}}
  \,.
$$

Using the standard [[model structure on simplicial objects in a topos]] this [[presentable (infinity,1)-category|presents]] an [[∞-groupoid]] internal to $\mathcal{T}$, the **path $\infty$-groupoid** of $X$.

If $(\mathcal{T},R)$ is even a [[smooth topos]], then there is also the construction of the [[infinitesimal path infinity-groupoid in a smooth topos]] $\Pi^{inf}(X)$ for each $X$ and a canonical inclusion

$$
  \Pi^{inf}(X) \hookrightarrow  
  \Pi(X)
  \,.
$$

[[!redirects path ∞-groupoid in a lined topos]]
[[!redirects path ∞-groupoid in a smooth topos]]
[[!redirects path infinity-groupoid in a smooth topos]]