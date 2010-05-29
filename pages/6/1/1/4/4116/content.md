[[!redirects topological topos]]
## Definition

Let [[Top]] be the [[category]] of [[topological space]]s, and let $\Sigma$ be the [[full subcategory]] whose only two [[object]]s are a one-point space and $\mathbb{N}^+$, the one-point compactification of the discrete space of [[natural number]]s. Let $J$ be the [[canonical Grothendieck topology]] on $\Sigma$. 

Johnstone's **topological topos** (specifically, the one described in the eponymous paper referenced below) is the [[topos]] of canonical [[sheaves]] $Sh_J(\Sigma)$ on $\Sigma$. The functor 

$$Top \to Set^{\Sigma^{op}}: X \mapsto Top(-, X)$$ 

is [[faithful functor|faithful]] and factors through $Sh_J(\Sigma)$, and its restriction to the category of [[sequential space]]s is full. 

## Reference 

Peter T. Johnstone, _On a topological topos_, Proc. London Math. Soc. (3) 38 (1979) 237&#8211;271.
