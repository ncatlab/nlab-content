
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

The [[operad|operadic]] generalization of the [[model structure on sSet-categories]]: a [[presentable (infinity,1)-category|presentation]] of [[(∞,1)Operad]].

## Definition

All operads considered here are multi-coloured [[symmetric operads]] ([[symmetric multicategories]]).

+-- {: .num_defn}
###### Definition

Call a morphism of [[simplicial operads]] $f : P \to Q$ 

* _fully faithful_ if it is a [[weak homotopy equivalence]] on all component simplicial sets.

* _essentially surjective_ if the induced morphism $\pi_0(f)$ on [[homotopy categories]] is an [[essentially surjective functor]].

* a _weak equivalence_ if it is fully faithful and essentially surjective.

* a _local fibration_ if it is componentwise a [[Kan fibration]]. 

* a _fibration_ if it is a local fibration and the underlying [[functor]] $\pi_0(f) : Ho(j^* P) \to Ho(j^* Q)$ on the [[homotopy categories]] of the underlying [[simplicial categories]] is an [[isofibration]].

=--

+-- {: .num_theorem}
###### Theorem

This defines on $sSet Operad$ the structure of a [[model category]] which is

* [[cofibrantly generated model category|cofibrantly generated]]; 

* [[right proper model category|right proper]].

=--

This is ([Cisinski-Moerdijk, theorem 1.14](#CisinskiMoerdijk)).

+-- {: .num_remark}
###### Remark

For $C \in $ [[Set]], let $sSet Operad_C \hookrightarrow sSet Operad$
be the full subcategory on operads with $C$ as their set of colours.

Then $sSet Operad_C \simeq (Operad_C)^{\Delta^{op}}$ is the category of [[simplicial objects]] in $C$-coloured [[symmetric operads]], and restricted to this the above model category structure is corresponding the [[model structure on simplicial algebras]].

=--

See ([Cisinski-Moerdijk, remark 1.9](#CisinskiMoerdijk)).


+-- {: .num_remark}
###### Remark

Restricted along the inclusion

$$
  j_! : sSet Cat \hookrightarrow sSet Operad
$$

the above model structure restricts to the [[model structure on sSet-categories]] by [[Julie Bergner]].

=--

## Properties

+-- {: .num_remark}
###### Remark

A morphism in $sSet Operad$ is an acyclic fibration precisely
if it is componentwise an acyclic [[Kan fibration]].

=--



## Related concepts

[[!include table - models for (infinity,1)-operads]]

## References

* [[Denis-Charles Cisinski]], [[Ieke Moerdijk]], _Dendroidal sets and simplicial operads_ ([arXiv:1109.1004](http://arxiv.org/abs/1109.1004))
 {#CisinskiMoerdijk}

[[!redirects model structure on simplicial operads]]
