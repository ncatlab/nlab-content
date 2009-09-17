#Definition#

A _simplicial sheaf_ $A$ is equivalently

* a [[simplicial object]] 

  $$
    A \in SSh(C) := [\Delta^{op}, Sh(C)]
  $$ 

  in a [[category of sheaves]] $Sh(C)$ for some [[site]] $C$;

* a [[simplicial presheaf]] 

  $$
    A \in SPSh(C) := [\Delta^{op}, PSh(C)] \simeq [\Delta^{op}, [C^{op}, C]]
  $$

  that satisfies degreewise the [[sheaf]] condition;

* an [[SSet]]-valued [[presheaf]] 

  $$
    A \in PSh(C,SSet) := [C^{op}, SSet] \simeq [C^{op}, [\Delta^{op}, Set]]
  $$
 
  which, when regarded under the equivalence

  $$
    PSh(C,SSet) \simeq SPSh(C)
  $$

  is degreewise a [[sheaf]].

# Model structure #

The standard [[model structure on simplicial presheaves]] restricts to the standard [[model structure on simplicial sheaves]], this restriction is a [[Quillen equivalence]] and equipped with this model structure $SSh(C)$ is one of the standard [[models for ∞-stack (∞,1)-toposes]] for the site $C$.

# Simplicial concrete sheaves #

Sometimes it is useful to restrict further to [[simplicial object]]s in the category of [[concrete sheaf|concrete sheaves]] on $C$. 

For instance for  $C$ a suitable [[site]] of smooth test spaces a simplicial concrete sheaf is a simplicial [[diffeological space]].
