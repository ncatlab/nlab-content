
#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

The [[Denis-Charles Cisinski|Cisinski]]-[[Ieke Moerdijk|Moerdijk]] [[model category]] structure on the [[category]] of [[dendroidal set]]s models [[(∞,1)-operad]]s in generalization of the way the [[Andre Joyal|Joyal]] [[model structure on simplicial sets]] models [[(∞,1)-category|(∞,1)-categories]].

## Overview ##


we have the following diagram of [[model category|model categories]]:

$$
  \array{
    SSet\text{-}Operad 
     &\stackrel{\simeq}{\to}& 
    dSet
     &\stackrel{\simeq}{\to}& 
    dSpaces
    &&&&& models\;for\;(\infty,1)-operads
    \\
    \uparrow && \uparrow && \uparrow
    \\
    SSet\text{-}Cat 
     &\stackrel{\simeq}{\to}& 
    sSet
     &\stackrel{\simeq}{\to}& 
    sSpaces   
    &&&&&
    models;for\;(\infty,1)-categories
  }
  \,,
$$

where the entries are

* the category $SSet Cat$ of [[simplicially enriched category|simplicially enriched categories]] equipped with the [[Julie Bergner|Bergner]]-model structure;

* the category [[SSet]] of [[simplicial set]]s equipped with the [[model structure on simplicial sets|Joyal model structure]] for [[quasi-category|quasi-categories]];

* the category $dSet$ of [[dendroidal set]]s

and where 

* the horizontal morphisms are [[Quillen equivalence]]s

* the vertical morphisms are [[homotopy full functor|homotopy full]] embeddings.

## Definition ##


A **quasi-operad** is a [[dendroidal set]] such that...

A _trivial fibration of quasi-operads_ is a morphism of [[dendroidal set]]s such that...

An **inner anodyne extension** of [[dendroidal set]]s is a morphism such that... 

+-- {: .un_def }
###### Definition
**(model structure on dendroidal sets)**

On the category of [[dendroidal set]]s let

* the cofibrations be the normal monomorphisms

* the fibrant objects are the quasi-operads

* the fibrations between fibrant objects are the are the inner Kan fibrations such that...

* the weak equivalences are the smallest class of maps that satisfy

  * [[category with weak equivalences|2-out-of-3]]

  * every inner anodyne extension is a weak equivalence

  * every trivial fibration between quasi-operads is a weak equivalence.

=--

## Properties ##


+-- {: .un_theorem }
###### Theorem

The above choices of cofibrations, fibrations and weak equivalences equips the category of dendroidal with the structure of a [[model category]]. This model structure is

* a left [[proper model category]]

* a [[cofibrantly generated model category]]

* a [[combinatorial model category]]

* a [[symmetric monoidal category|symmetric]] [[monoidal model category]]. 

=--

+-- {: .proof}
###### Proof

This is prop. 2.6 in [CisMoe](http://arxiv.org/abs/0902.1954)

=--


## References ##

* [[Denis-Charles Cisinski]], [[Ieke Moerdijk]], _Dendroidal sets as models for homotopy operads_ ([arXiv](http://arxiv.org/abs/0902.1954))