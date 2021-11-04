

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


This is a subentry of [[(∞,1)-Grothendieck construction]].


#Contents#
* table of contents
{:toc}

## Idea

When [[(∞,1)-categories]] are modeled as [[quasi-categories]], the [[(∞,1)-Grothendieck construction]] takes the form of a [[Quillen equivalence]] 
between
a [[model structure on sSet-enriched presheaves]]
and a [[slice model structure]] of [[simplicial sets]] which has been introduced under the name *straightening and unstraightening* in [Lurie 2009, Sec. 3.2](#Lurie09):

In [[model category]]-theory, in particular in the presentation of the [[(infinity,1)-Grothendieck construction|(∞,0)-Grothendieck construction]], for a [[simplicial set]] $S$, there is a [[pair]] of [[adjoint functors]]
$$
  (St_\phi\dashv Un_\phi) 
  \;\colon\; 
  sSet/S \stackrel{St}{\to} [C^{op}, sSet]
$$
which (under an assumption on the parameter $\phi$) can be shown to be a [[Quillen equivalence]] between the [[slice model structure]] of simplicial sets equipped with the [[model structure for right fibrations]] (also called contravariant model structure in [[Higher Topos Theory|HTT]]) and the category of [[simplicial presheaves]] equipped with [[model structure on simplicial presheaves|global projective model structure]].

There is also a Quillen equivalence
$$
  (St_\phi\dashv Un_\phi) 
  \;\colon\; 
  sSet^+/S \stackrel{St}{\to} [C^{op}, sSet^+]
$$
between the [[model structure for Cartesian fibrations]] and the global projective model structure on functors with values  in the [[model structure on marked simplicial sets]].

Here (in both cases) $St_\phi$ is called *straightening functor* and $Un_\phi$ is called *unstraightening functor*. These names have been chosen due to the fact that objects in the left hand category are defined by existential assertions and choices where on the right side these properties become [[coherence laws]] being part of the structure.

## Related concepts

* [[cartesian fibration]]

* [[Grothendieck fibration]]

* [[cleavage]]

## References

The original result is due to:

* {#Lurie09} [[Jacob Lurie]], Sec. 3.2 of: _[[Higher Topos Theory]]_, Annals of Mathematics Studies 170, Princeton University Press 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))


A considerably simplified presentation is available in

* [[Fabian Hebestreit]], [[Gijs Heuts]], [[Jaco Ruit]], _A short proof of the straightening theorem_ ([arXiv:2111.00069](https://arxiv.org/abs/2111.00069)).

[[!redirects straightening and unstraightening]]
