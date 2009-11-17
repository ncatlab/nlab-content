
#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

The [[Denis-Charles Cisinski|Cisinski]]-[[Ieke Moerdijk|Moerdijk]] [[model category]] structure on the [[category]] $dSet$ of [[dendroidal set]]s models [[(∞,1)-operad]]s in generalization of the way the [[Andre Joyal|Joyal]] [[model structure on simplicial sets]] models [[(∞,1)-category|(∞,1)-categories]].

## Overview ##


We have the following diagram of [[model category|model categories]]:

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


### Special morphisms ###

Recall frrom the entry on [[dendroidal set]]s the definition of inner and outer faces, boundaries and inner and outer horns.

The following definition are the obvious generalizations of the corresponding notions for the [[model structure on simplicial sets]], in particular for the [[Andre Joyal|Joyal]]-model structure.

+-- {: .un_defn}
###### Definition
**(inner anodyne extension)**

The class of morphisms in $dSet$ generated from the inner horn inclusions $\Lambda^e \Omega[T] \to \Omega[T]$ under

* [[pushout]]

* [[transfinite composition]]

* [[retract]]s

is called the **inner anodyne extensions**.

=--

+-- {: .un_defn}
###### Definition
**(inner Kan fibration)**

A [[morphism]] $A \to B$ in $dSet$ is an **inner Kan fibration** if it has the [[right lifting property]] with respect to all inner horn inclusions.

$$
  \array{
    \Lambda^e[T] &\to& A
     \\
    \downarrow && \downarrow
    \\
    \Omega[T] &\to& B
  }
$$

or equivalently with respect to the class of inner anodyne extensions.

=--


+-- {: .un_defn}
###### Definition
**(inner Kan complex / quasi-operad)**

A dendroidal set $X$ is an **inner Kan complex** or **quasi-operad** if the canonical morphism $X\to {*}$ to the [[terminal object]] is an inner Kan fibration.

=--

+-- {: .un_defn}
###### Definition
**(trivial fibration)**

A morphism $A \to B$ of dendroidal sets is an **acyclic fibration** if it has the [[right lifting property]] with respect to all monomorphisms (equivalently: with respect to all normal monomorphisms).

=--




### The model structure ###

A **quasi-operad** is a [[dendroidal set]] such that...

A _trivial fibration of quasi-operads_ is a morphism of [[dendroidal set]]s such that...

An **inner anodyne extension** of [[dendroidal set]]s is a morphism such that... 

+-- {: .un_def }
###### Definition
**(model structure on dendroidal sets)**

On the category of [[dendroidal set]]s let

* the cofibrations be the normal monomorphisms

* the fibrant objects are the weak Kan complexes/quasi-operads

* the fibrations between fibrant objects are the are the inner Kan fibrations $f : A \to B$ between quasi-operads such that the image $\tau_d(f)$ under the functor $\tau_d : dSet \to Operads$ is an operadic fibration

* the weak equivalences form the smallest class of maps that satisfy

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

This is prop. 2.6 in [CisMoe](http://arxiv.org/abs/0902.1954).

=--

+-- {: .un_corollary }
###### Corollary

With this model structure and the standard [[model structure on operads]] the dendroidall [[nerve]] [[adjunction]]

$$
  \tau_d : dSet \stackrel{\leftarrow}{\to} Operad : N
$$

is a [[Quillen adjunction]] and both functors preserve all weak equivalences. So in particular a morphism of operads is a weak equivalence precisely if the induced morphism between dendroidal nerves is a weak equivalence.

=--

+-- {: .proof}
###### Proof

This is cor. 6.17 in [CisMoe](http://arxiv.org/abs/0902.1954).

=--



## References ##

* [[Denis-Charles Cisinski]], [[Ieke Moerdijk]], _Dendroidal sets as models for homotopy operads_ ([arXiv](http://arxiv.org/abs/0902.1954))