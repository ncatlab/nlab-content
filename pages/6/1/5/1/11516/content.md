
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the context of [[topology]], a _topological $G$-space_ (traditionally just _$G$-space_, for short, if the context is clear) is a [[topological space]] equipped with an [[action]] of a [[topological group]] $G$ (often, but crucially not always, taken to be a [[finite group]]).

There are two evident possibilities for defining a [[homotopy theory]] of [[topological G-spaces]]. While the [[morphisms]] in any case are to be the $G$-equivariant [[continuous functions]], one may or may not require the [[homotopies]] between such maps to equivariant themselves. Not requiring them to respect the $G$ action leads to what is called "naive" [[equivariant homotopy theory]] (which however certainly has its uses, too), while requiring the maps to respect the $G$-action leads to "genuine" [[equivariant homotopy theory]]. On [[G-CW complexes]] these $G$-equivariant [[homotopy equivalences]] are equivalently the [[weak homotopy equivalences]] on all [[fixed point]] spaces for all [[subgroups]] of $G$; and by [[Elmendorf's theorem]] it is equivalent to the [[(∞,1)-presheaves]] over the [[orbit category]] of $G$.  The union of this as $G$ is allowed to vary is the _[[global equivariant homotopy theory]]_. See at [equivariant homotopy -- In topological spaces -- G-Homotopy](equivariant+homotopy+theory#homotopy).


In the context of [[stable homotopy theory]] the [[stabilization]] of $G$-spaces is given by [[spectra with G-action]]; these lead to [[equivariant stable homotopy theory]]. See there for more details. (But beware that in this context one considers the richer concept of [[G-spectra]], which have a [[forgetful functor]] to [[spectra with G-action]] but better homotopy theoretic properties. ) The union of this as $G$ is allowed to vary is the [[global equivariant stable homotopy theory]].

## Properties

### Model structure and homotopy theory

The standard [[homotopy theory]] on $G$-spaces used in [[equivariant homotopy theory]] considers [[weak equivalences]] which are [[weak homotopy equivalence]] on all (ordinary) [[fixed point]] spaces for all suitable [[subgroups]]. By [[Elmendorf's theorem]], this is equivalent to [[(∞,1)-presheaves]] over the [[orbit category]] of $G$.

On the other hand there is also the standard homotopy theory of [[infinity-actions]], presented by the [[Borel model structure]], in this context also called the "coarse" equivariant model structure ([Guillou](#Guillou)).


## Examples

* [[G-CW complex]]

* [[representation sphere]]


## Related concepts

* [[G-set]]

[[!include equivariant homotopy theory -- table]]


## References

See the references at _[[equivariant homotopy theory]]_.

* {#Guillou} [[Bert Guillou]], _A short note on models for equivariant homotopy theory_ ([pdf](http://www.math.uiuc.edu/~bertg/EquivModels.pdf))

[[!redirects topological G-spaces]]

[[!redirects G-space]]
[[!redirects G-spaces]]