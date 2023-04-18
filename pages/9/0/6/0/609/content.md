
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
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
 {#Idea}

The notion of *simplicial groupoids* pairs the concepts of *[[groupoids]]* and *[[simplicial sets]]*. Via the [[Dwyer-Kan loop groupoid]] functor &lbrack;[Dwyer & Kan (1984)](#DwyerKan84)&rbrack; their [[homotopy]] theory is equivalent to the [[classical model structure on simplicial sets|classical]] homotopy theory of [[simplicial sets]]/[[Kan complexes]] (both being models for [[infinity-groupoids|$\infty$-groupoids]]).


## Definition
 {#Definition}

A priori, the term *simplicial groupoid* may refer to [[simplicial objects]] in the ([[1-category|1-]])[[category]] [[Grpd]] of ([[small category|small]]) [[strict category|strict]] [[groupoids]].

However (cf. discussion at *[[simplicial category]]*), in applications (notably in [[homotopy theory]]) one is interested only in those simplicial objects in [[Grpd]] whose [[underlying]] simplicial [[sets]] of [[objects]] are *simplicially constant*. This more restrictive notion is traditionally still referred to as "simplicial groupoids" &lbrack;e.g. [Dwyer & Kan (1984),  §1.2.(ii)](#DwyerKan84), [Goerss & Jardine (2009), V.7](GoerssJardine09)&rbrack;; but for the moment let us call these instead "simplicial DK-groupoids", for clarity, and let us denote the [[full subcategory]] they form by

$$
  sGrpd_{DK} 
    \overset{\phantom{---}}{\hookrightarrow} 
  Func(\Delta^{op}, Grpd)
  \,.
$$

So given such a simplicial DK-groupoid $\mathcal{C}_\bullet \,\in\, sGrpd_{DK}$ we have:

1. a plain [[set]] of [[objects]] $Obj(\mathcal{C}_\bullet) \,\in\, Sets$;

1. for every [[pair]] $x, y \,\in\, Obj(\mathcal{C}_\bullet)$ of [[objects]] the degree-wise [[hom-sets]] form a [[simplicial set]] 

   $$
     \mathcal{C}_\bullet(x,y)
     \;\coloneqq\;
     Hom_{\mathcal{C}_\bullet}(x,y)
     \;\in\;
     sSet
     \,;
   $$

1. where the degreewise [[composition]] operations constitutes an [[sSet]]-[[enriched category|enriched]] composition operation

   $$
     \mathcal{C}_\bullet(x,y)
     \,\times\,
     \mathcal{C}_\bullet(y,z)
     \overset{\circ}{\longrightarrow}
     \mathcal{C}_\bullet(x,z)
   $$

1. making $\mathcal{C}_\bullet$ an [[sSet-enriched category]].

Conversely, simplical DK-groupoids are therefore in [[bijection]] to those [[sSet-enriched categories]] whose degreewise [[categories]] formed by the $n$-cell [[morphisms]] for any $n \,\in\, \mathbb{N}$ are [[groupoids]].

This makes the category $sGrpd_{DK}$ be a [[full subcategory]] of the category of ([[small category|small]]) [[sSet-enriched categories]]:

$$
  sGrpd_{DK} 
    \overset{\phantom{---}}{\hookrightarrow} 
  sSet Cat
  \,.
$$


## Remarks
 
*  Simplicially enriched groupoids are related to [[simplicial set|simplicial sets]] via an [[adjoint functor|adjunction]] found independently by Dwyer & Kan and Joyal & Tierney; see *[[Dwyer-Kan loop groupoid]]*.  This adjunction gives an [[equivalence of categories|equivalence]] of [[homotopy category|homotopy categories]] so that simplicially enriched groupoids model all [[homotopy type|homotopy types]].

   *  This is a groupoidal version of the equivalence between [[quasi-category|quasi-categories]] and [[simplicially enriched category|simplicially enriched categories]] via the [[homotopy coherent nerve]].

*  A simplicially enriched groupoid having exactly one object is essentially the same as a [[simplicial group]]. Notationally however it is often important to distinguish a simplicial group form the corresponding single object simplicially enriched groupoid.

*  Many constructions on simplicial groups, such as that of its [[Moore complex]] carry over to simplicialy enriched groupoids without difficulty.

## Related concepts

* [[model structure on simplicial groupoids]]

* [[simplicial category]]
  
  * [[simplicially enriched category]]

  * [[simplicial object in Cat]]

* [[relation between quasi-categories and simplicial categories]]

* [[model structure on presheaves of simplicial groupoids]]

## References

Original discussion in the context of a [[model structure on simplicial groupoids]]:

* {#DwyerKan84} [[William Dwyer]], [[Daniel Kan]],  _Homotopy theory and simplicial groupoids_, Indagationes Mathematicae (Proceedings) **87** 4 (1984) 379-385 &lbrack;<a href="https://doi.org/10.1016/1385-7258(84)90038-6">doi:10.1016/1385-7258(84)90038-6</a>&rbrack;
 
with a detailed textbook account in:

* {#GoerssJardine09} [[Paul Goerss]], [[J. F. Jardine]], Section V.7 of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) &lbrack;[doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/)&rbrack; 

See also:

* [[Philip Ehlers]], _Simplicial groupoids as models for homotopy type_ Master's thesis (1991) ([pdf](https://ncatlab.org/nlab/files/Ehlers-MSc-thesis.pdf))

[[!redirects simplicial groupoids]]
[[!redirects simplicially enriched groupoids]]
[[!redirects simplicially enriched groupoid]]