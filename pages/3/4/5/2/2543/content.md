<div class="rightHandSide toc">
[[!include synthetic differential geometry - contents]]
</div>


In every [[lined topos]] $(\mathcal{T}, R)$ the line $R$ may canonically be regarded as an [[interval object]]

$$
  {*} \stackrel{0}{\to} R \stackrel{1}{\leftarrow} {*}
  \,.
$$

As discussed there, this inuces a [[cosimplicial object]]

$$
  \Delta_{\mathcal{T}} : \Delta \to \mathcal{T}
$$

and then in turn a functor

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