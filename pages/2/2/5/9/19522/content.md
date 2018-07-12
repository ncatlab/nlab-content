

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a [[2-category]] $\mathcal{C}$, it induces a [[double category]] $Sq(\mathcal{C})$ whose

* [[objects]] are the objects of $\mathcal{C}$;

* [[horizontal morphisms]] are the [[1-morphisms]] of $\mathcal{C}$;

* [[vertical morphisms]] are also the [[1-morphisms]] of $\mathcal{C}$;

* [[2-morphisms]] are the [[2-morphisms]] of $\mathcal{C}$ between the [[compositions]] of the [[1-morphisms]]. 

## Examples

* The double category $Sq(Cat)$ of squares in [[Cat]] receives a [[double pseudofunctor]] $Ho(-)$ from the [[double category of model categories]] ([this Prop.](double+category+of+model+categories#HomotopyDoublePseudofunctor)) which on objects sends a [[model category]] to its [[homotopy category of a model category]], and which on morphisms sends a left/right [[Quillen functor]] to its left/right [[derived functor]].

## References

The construction goes back to

* {#Ehresmann63} [[Charles Ehresmann]], _Catégories structurées_, Annales scientifiques de l'École Normale Supérieure. Vol. 80. No. 4. Elsevier, 1963 ([EUDML:81794](https://eudml.org/doc/urn:eudml:doc:81794))

[[!redirects double categories of squares]]
