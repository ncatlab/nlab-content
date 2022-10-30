#Idea#

The _pushout-product axtiom_ is a compatibility condition between 

1. a [[closed monoidal category|closed]] [[monoidal category|symmetric monoidal]] structure 

2. and [[model category]] structure

on a category.

[[closed monoidal category|Closed]] [[monoidal category|symmetric monoidal categories]] satisfying the pushout-product axiom are called [[monoidal model category|monoidal model categories]] and hence are in particular [[closed monoidal homotopical category|closed monoidal homotopical categories]].

This is relevant in [[enriched homotopy theory]], which pairs [[enriched category theory]] with [[homotopy theory]].

#Definition#

Let $C$ be a [[closed monoidal category|closed]] [[monoidal category|symmetric monoidal category]] equipped with a [[model category]] structure. 

Then $C$ satisfies the _pushout-product axiom_ if for any pair of cofibrations $f : X \to Y$ and $f' : X' \to Y'$ the induced map

$$
  (X \otimes Y') \cup_{X \otimes X'} (Y \otimes X')
  \to
  Y \otimes Y'
$$

is a cofibration which is acyclic if $f$ or $f'$ is.

#Remarks#

* This implies in particular that tensoring with cofibrant objects preserves cofibrations and acyclic cofibrations.

* However the tensor product of two (acyclic) cofibrations is in general not an (acyclic) cofibration.