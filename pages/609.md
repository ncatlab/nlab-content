
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

Simplicial groupoids pair the concepts of [[groupoids]] and [[simplicial sets]]. Via the [[Dwyer-Kan loop groupoid]] functor ([Dwyer-Kan 84](#DwyerKan84)) their [[homotopy]] theory is equivalent to the classical homotopy theory of [[simplicial sets]]/[[Kan complexes]] (both being models for [[infinity-groupoids]]).

## Definition

It is probably best to distinguish between the following:

*   A **simplicial groupoid** is a [[simplicial object]] in [[Cat]] (that is, a functor from $\Delta^{op}$ to $Cat$), 
in which is all the categories involved are [[groupoid]]s.

*   A **simplicially enriched groupoid** is a groupoid [[enriched category|enriched]] over the category [[SimpSet]] of [[simplicial set]]s.  

(For a discussion of the terminology of simplicial groupoid and [[simplicial category]], see the entry on the second of these.)


Any simplicially enriched groupoid yields a simplicial groupoid in which the face and degeneracy operators are constant on objects and it is often in this latter form that they are met in homotopy theory.

(Of course, what is 'best' is not always done in the literature, so the reader is best advised to check the meaning being used when the term is met in an article or text.)

##Remarks##
 
*  Simplicially enriched groupoids are related to [[simplicial set|simplicial sets]] via an [[adjoint functor|adjunction]] found independently by Dwyer&#8211;Kan and Joyal&#8211;Tierney; see [[Dwyer-Kan loop groupoid]].  This adjunction gives an [[equivalence of categories|equivalence]] of [[homotopy category|homotopy categories]] so that simplicially enriched groupoids model all [[homotopy type|homotopy types]].

   *  This is the groupoidal version of the equivalence between [[quasi-category|quasi-categories]] and [[simplicially enriched category|simplicially enriched categories]] via the [[homotopy coherent nerve]].

*  A simplicially enriched groupoid having exactly one object is essentially the same as a [[simplicial group]]. Notationally however it is often important to distinguish a simplicial group form the corresponding single object simplicially enriched groupoid.

*  Many constructions on simplicial groups, such as that of its [[Moore complex]] carry over to simplicialy enriched groupoids without difficulty.

## Related concepts

* [[simplicial category]]
  
  * [[simplicially enriched category]]

  * [[simplicial object in Cat]]

* **simplicial groupoid**

* [[relation between quasi-categories and simplicial categories]]

* [[model structure on presheaves of simplicial groupoids]]

## References

* {#DwyerKan84} [[William Dwyer|W. G. Dwyer]] and [[Dan Kan|D. M. Kan]],  _Homotopy theory and simplicial groupoids_,  Nederl. Akad. Wetensch. Indag. Math., 46, (1984), 379 &#8211; 385,


* Philip Ehlers, _Simplicial groupoids as models for homotopy type_ Master's thesis (1991) ([pdf](https://ncatlab.org/nlab/files/Ehlers-MSc-thesis.pdf))

[[!redirects simplicial groupoids]]
[[!redirects simplicially enriched groupoids]]
[[!redirects simplicially enriched groupoid]]