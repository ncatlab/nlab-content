
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Statement

+-- {: .num_prop #OnePointCompactificationAndSmashProduct}
###### Proposition
**([[one-point compactification]] of [[product topological space|product space]] is [[smash product]] of the compactified factors)

On the [[subcategory]] $Top_{LCHaus}$ in [[Top]] of [[locally compact Hausdorff spaces]] with [[proper maps]] between them, the [[functor]] of [[one-point compactification]] (Prop. \ref{OnePointCompactificationFunctor})

$$
  (-)^{cpt}
  \;\colon\;
  Top_{LCHaus}
  \longrightarrow 
  Top^{\ast/}
$$


1. sends [[coproducts]], hence [[disjoint union topological spaces]], to [[wedge sums]] of [[pointed topological spaces]];

1. sends [[Cartesian products]], hence [[product topological spaces]], to [[smash products]] of [[pointed topological spaces]];

hence constitutes a [[strong monoidal functor]] for both [[monoidal category|monoidal]] structures of these [[distributive monoidal categories]] in that there are [[natural transformation|natural]] [[homeomorphisms]]

$$
  \big(
    X \sqcup Y 
  \big)^{cpt}
  \;\simeq\;
  X^{cpt} \vee Y^{cpt}
  \,,
$$

and

$$
  \big(
    X \times Y 
  \big)^{cpt}
  \;\simeq\;
  X^{cpt} \wedge Y^{cpt}
  \,.
$$

=--

This is briefly mentioned in [Bredon 93, p. 199](#Bredon93).
The argument is spelled out in: [MO:a/1645794](https://math.stackexchange.com/a/1645794/58526), [Cutler 20, Prop. 1.6](#Cutler20).



## References

Basic accounts:

* {#Bredon93} [[Glen Bredon]], p. 199 of: _Topology and Geometry_, Graduate Texts in Mathematics 139, Springer 1993 ([doi:10.1007/978-1-4757-6848-0](https://link.springer.com/book/10.1007/978-1-4757-6848-0), [pdf](http://virtualmath1.stanford.edu/~ralph/math215b/Bredon.pdf))

Review:

* {#Cutler20} Tyrone Cutler, _The category of pointed topological spaces_, 2020 ([pdf](https://www.math.uni-bielefeld.de/~tcutler/pdf/Elementary%20Homotopy%20Theory%20II%20-%20The%20Pointed%20Category.pdf), [[CutlerPointedTopologicalSpaces.pdf:file]])


