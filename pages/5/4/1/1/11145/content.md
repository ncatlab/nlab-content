
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

In [[geometric representation theory]] the _horocycle correspondence_ for $G$ a complex [[reductive group]] and $B \subset G$ a [[Borel subgroup]] is the [[correspondence]] of [[group]] [[quotients]]  given by

$$
  G//_{ad} G \stackrel{p}{\longleftarrow} G_{ad}//B \stackrel{\delta}{\longrightarrow} B \backslash  G / B
 \,.
$$

This generalizes the [[Grothendieck-Springer correspondence]]. ([Ben-Zvi & Nadler 09, example 1.2](#BenZviNadler09))

The pull-push [[integral transform]] of [[D-modules]] from right to left through this correspondence is the _Harish-Chandra transform_

$$
  p_\ast \delta^! \;\colon\; \mathcal{D}(B\backslash G / B) \longrightarrow \mathcal{D}(G/_{ad}G)
$$

from the [[Hecke category]] on the left.

A (unipotent) [[character sheaf]] ([Lusztig 85](#Lusztig85)) for $G$ is a [[simple object]]-[[direct summand]] of a [[D-module]] that is in the image of a [[simple object]] under this transform. ([Ginzburg 89](#Ginzburg89))

## Related concepts

* [[twistor correspondence]], [[Penrose transform]]

* [Schubert calculus -- Correspndences](Schubert+calculus#Correspondences)

## References

Original articles include

* {#Lusztig85} [[George Lusztig]], _Character sheaves I_. Adv. Math 56 (1985) no. 3, 193-237.

* {#Ginzburg89} [[Victor Ginzburg]], _Admissible modules on a symmetric space. Orbites unipotentes et repr&#233;sentations, III. Ast&#233;risque No. 173-174 (1989), 9&#8211;10, 199&#8211;255.

Interpretation in the context of [[extended TQFT]] is in 

* {#BenZviNadler09} [[David Ben-Zvi]], [[David Nadler]], _The Character Theory of a Complex Group_ ([arXiv:0904.1247](http://arxiv.org/abs/0904.1247))

[[!redirects horocycle correspondences]]
[[!redirects Harish Chandra transform]]
[[!redirects Harish Chandra transforms]]
[[!redirects Harish-Chandra transform]]
[[!redirects Harish-Chandra transforms]]

[[!redirects Grothendieck-Springer correspondence]]
[[!redirects Grothendieck-Springer correspondences]]
