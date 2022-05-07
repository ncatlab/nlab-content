
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
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


## Statement

+-- {: .num_prop }
###### Proposition

The [[category]] of [[Delta-generated topological spaces]] carries the [[mathematical structure|structure]] of a [[cofibrantly generated model category]] with the same generating (acyclic) cofibrations as for the [[classical model structure on topological spaces]] and such that the [[coreflective subcategory|coreflection]] into all [[topological spaces]] ([this Prop.](Delta-generated+topological+space#AdjunctionBetweenTopologicalSpacesAndDiffeologicalSpaces)) is a [[Quillen equivalence]] with the [[classical model structure on topological spaces]]:

$$
  Top_{Qu}
  \underoverset
    {\underset{Cdfflg}{\longrightarrow}}
    {\hookleftarrow}
    {\;\;\;\;\;\simeq_{\mathrlap{Qu}}\;\;\;\;\;}
  D Top_{Qu}
$$

=--

([Haraguchi 13, Theorem 3.3](#Haraguchi13))

By the same kind of argument ([Gaucher 2007](#Gaucher07)), this factors by a [[Quillen equivalence]] through the [[model structure on compactly generated topological spaces]]:

$$
  Top_{Qu}
  \underoverset
    { \underset{ k }{\longrightarrow} }
    { {\hookleftarrow} }
    { \;\;\;\;\;\;\simeq_{\mathrlap{Qu}}\;\;\;\;\;\; }
  k Top_{Qu}
  \underoverset
    { \underset{ D }{\longrightarrow} }
    { {\hookleftarrow} }
    { \;\;\;\;\;\;\simeq_{\mathrlap{Qu}}\;\;\;\;\;\; }
  D Top_{Qu}
  \,.
$$


## Related concepts

* [[model structure on topological spaces]]

  * [[classical model structure on topological spaces]] ([[classical model structure on pointed topological spaces|on pointed spaces]])

    * [[model structure on compactly-generated topological spaces]]

    * [[model structure on Delta-generated topological spaces]]

  * [[Strøm model structure]]

* [[model structure on diffeological spaces]]


## References

* {#Gaucher07} [[Philippe Gaucher]], p. 7 of: *Homotopical interpretation of globular complex by multipointed d-space*, Theory and Applications of Categories, vol. 22, number 22, 588-621, 2009 ([arXiv:0710.3553](https://arxiv.org/abs/0710.3553))



* {#Haraguchi13} [[Tadayuki Haraguchi]], _On model structure for coreflective subcategories of a model category_, Math. J. Okayama Univ. 57 (2015), 79–84 ([arXiv:1304.3622](http://arxiv.org/abs/1304.3622), [doi:10.18926/mjou/53040](http://doi.org/10.18926/mjou/53040), MR3289294, Zbl 1311.55027)


[[!redirects model structure on Delta-generated spaces]]

[[!redirects model structure on D-topological spaces]]

