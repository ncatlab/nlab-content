
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _model structure for dendroidal left fibrations_ is an [[operad|operadic]] analog of the _[[model structure for left fibrations]]_. Its fibrant objects over [[Assoc]] are [[A-∞ spaces]], over [[Comm]] they are [[E-∞ spaces]].

## Definition

(...)

## Properties

+-- {: .num_prop}
###### Proposition

For $f : S \to T$ any morphism of [[dendroidal sets]], the induced [[adjunction]] (by [[Kan extension]])


$$
  (f_! \dashv f^* ) : dSet/T \stackrel{\overset{f_!}{\leftarrow}}{\underset{f^*}{\to}}
   dSet/S
$$

is a [[Quillen adjunction]] for the corresponding model structures for dendroidal left fibrations over $S$ and $T$. It is a [[Quillen equivalence]] if $f$ is a weak equivalences in the Cisinki-Moerdijk [[model structure on dendroidal sets]].

=--

This is ([Heuts, prop. 2.4](#Heuts)).

### Relation to other model structures

(...)



## Related concepts

* [[model structure for left fibrations]]

* [[model structure for dendroidal Cartesian fibrations]]

For an overview of models for [[(∞,1)-operads]] see
_[[table - models for (infinity,1)-operads]]_.

## References

* [[Gijs Heuts]], _Algebras over infinity-Operads_ ([arXiv:1110.1776](http://arxiv.org/abs/1110.1776))
 {#Heuts}

