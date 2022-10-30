This is a subentry of [[(infinity,1)-Grothendieck construction]].

In [[model category theory]] , in particular in the presentation of the [[(infinity,1)-Grothendieck construction|(∞,0)-Grothendieck construction]], for a simplicial set $S$, there is a pair of adjoint functors

$$
  (St_\phi\dashv Un_\phi) : sSet/S \stackrel{St}{\to} [C^{op}, sSet]
$$

which (under an assumption on the parameter $\phi$) can be shown to be a [[Quillen equivalence]] between the overcategory of simplicial sets equipped with the [[model structure for right fibrations]] (also called contravariant model structure in [[Higher Topos Theory|HTT]]) and the category of simplicial presheaves equipped with [[model structure on functors|global projective model structure]].

There is also a Quillen equivalence

$$
  (St_\phi\dashv Un_\phi) : sSet^+/S \stackrel{St}{\to} [C^{op}, sSet^+]
$$

between the [[model structure for Cartesian fibrations]] and the global projective model structure on functors with values  in the [[model structure on marked simplicial sets]].

Here (in both cases) $St_\phi$ is called *straightening functor* and $Un_\phi$ is called *unstraightening functor*. These names have been chosen due to the fact that objects in the left hand category are defined be existential assertions and choices where on the right side these properties become coherence laws being part of the structure.