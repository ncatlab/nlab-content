
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _hypercompletion_ ([Lurie](#Lurie)) or _$t$-completion_ ([Rezk](#Rezk), [To&#235;nVezzosi](#ToenVezzosi)) of an [[(∞,1)-topos]] of [[(infinity,1)-category of (infinity,1)-sheaves|(∞,1)-sheaves]] is a further localization/[[(infinity,1)-category of (infinity,1)-sheaves|(∞,1)-sheafification]] which corresponds to retaining only those [[(∞,1)-sheaves]] which satisfy [[descent]] with respect to all [[hypercover|hypercovers]] (the [[hypersheaf|hypersheaves]]).

## Definition

+-- {: .un_defn}
###### Definition

An [[(∞,1)-topos]] of [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaves]] is a **[[hypercomplete (∞,1)-topos]]**  if every $\infty$-[[n-connective|connective]] morphism is an [[equivalence in an (∞,1)-category|equivalence]].

=--

+-- {: .un_remark}
###### Remark

This may be read as saying that the [[Whitehead theorem]] is valid in the [[(∞,1)-topos]].

=--



## Examples

* The $(\infty,1)$-category defined by the Joyal-Jardine [[local model structure on simplicial presheaves]] with weak equivalences those morphisms that induce isomorphisms on homotopy sheaves is the hypercompletion of the [[localization]] of simplicial presheaves at ordinary covers. For more details see [[descent for simplicial presheaves]].

## Related concepts

* [[topological localization]]
* [[cotopological localization]]

## References

Section 10 of 

* [[Charles Rezk]], _Toposes and homotopy toposes_ ([pdf](https://rezk.web.illinois.edu/homotopy-topos-sketch.pdf))
{#Rezk}

Section 6.5 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

* [[Bertrand Toën]], [[Gabriele Vezzosi]], ([pdf](http://poincare.dma.unifi.it/~vezzosi/papers/msri.pdf))
{#ToenVezzosi}

[[!redirects hypercompletions]]