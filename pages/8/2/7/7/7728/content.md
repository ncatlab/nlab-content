
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Philosophy
+-- {: .hide}
[[!include philosophy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

> These many different things stand in essential reciprocal action via their properties; the property is this reciprocal relation itself and apart from it the thing is nothing; ([WdL &#167;1065a](Science+of+Logic#1065a))


In [[philosophy]], _structuralism_ is the point of view (especially in humanities) which emphasises that the entities considered are parts of a system and that their very meaning and identity is defined according to its relation to the rest of the system.  For instance if one part of the system changes in time all other parts change as well. The system has features which are not just the added features of its constituents. 

Structuralism is an influential direction in science in 20th century with Ferdinand de Saussure (and later Roman Jakobson) in linguistics, Claude L&#233;vi-Strauss in anthropology and so on. 

## Formalization in category theory and type theory

To some extent, [[category theory]] provides a formalization of the idea of structuralism ([Awodey 96](#Awodey96), [Awodey 03](#Awodey03)). Manin says that category theory regards objects as part of a "society". (See also at _[[objective logic]]_ for more on categorical logic and philosophical notions.)

In a [[category]], the nature of any [[object]] is determined only by the system of  _[[morphisms]]_ which relate this object to the other objects of the category. 

Here the terminology _morphism_ originates in _[[homomorphism]]_ since the morphisms in the category of [[mathematical structures]] (such as [[groups]], [[modules]], etc.) are precisely the maps of the underlying [[sets]] that preserve this structure.

So far this is essentially [[Bourbaki]]'s emphasis on [[mathematics]] as the science of abstract [[structures]], which has earlier also taken a similar point of view where structures are important only up to isomorphism and the emphasis is on relations (including) functions which are part of the "structure". (e.g. [Kantor 11](#Kantor11))

But more generally a category need not be such a [[concrete category]] of sets with structure, and then while there is no explicit structure on the objects, the same category-theoretic reasoning still applies and one may detect structure on objects form the morphisms between them.

For instance while in general an object $X$ in a category does not have an underlying set, if the category has a [[terminal object]] $\ast$ one may still find a set of [[global elements]] of $X$ as the set of morphisms of the form $\ast \to X$.

Accordingly, in a category one only talks about properties invariant under [[isomorphisms]]; from the point of such an [[object]] is determined by the morphisms to or from other objects. 

This perspective of the nature objects of a category being determined only by the morphisms between them is fully embodied by the concept of [[equivalence of categories]]: two categories are to be regarded as equivalent if there is a [[functor]] between them that is [[essentially surjective]] in that it does not omit any [[isomorphism class]] of objects and which otherwise is a [[bijection]] on morphisms (precisely: on the [[hom-sets]] between any ordered pair of objects, a [[fully faithful functor]]). 

Given that [[type theories]] of sorts are the [[internal language]] of suitable kinds of [[categories]], with morphisms now being [[terms]] of [[function types]] (see at _[[relation between category theory and type theory]]_), these comments also give that type theory offers some kind of formalization of structuralism ([Awodey 15](#Awodey15), [Corfield 15](#Corfield15)).

Notably in [[homotopy type theory]] with [[univalence]], which is the [[internal language]] of categories called [[(infinity,1)-toposes]], the [[type universe]] reflects all the [[isomorphisms]] ([[equivalences]]) in the category in its [[identity type]], which therefore may be thought of as providing a structuralist concept of [[identity]].

(Notice however that the categories of [[mathematical structures]] such as [[groups]], [[modules]], etc., even when regarded as [[(infinity,1)-categories]], i.e. of [[infinity-groups]], [[(infinity,n)-modules]] etc.) are rarely [[(infinity,1)-toposes]]. The "structure" carries by an object in an $(\infty,1)$-topos is generically more a kind of geometric structure. 


## References

* wikipedia [structuralism](http://en.wikipedia.org/wiki/Structuralism)

* {#Awodey96} [[Steve Awodey]], _Structure in mathematics and logic: a categorical perspective_, Philosophia Mathematica (3), vol. 4,  p. 209-237 (1996)

* {#Awodey03} [[Steve Awodey]], _An Answer to Hellman's Question: "Does Category Theory Prove a Foundation for Mathematical Structuralism?_, 2003 ([pdf](http://www.andrew.cmu.edu/user/awodey/preprints/awodeyVhellman.pdf))

* {#MacLarty04} [[Colin McLarty]], 2004, _Exploring Categorical Structuralism_, Philosophia Mathematica, 12, 37&#8211;53 ([pdf](http://www.cwru.edu/artsci/phil/PMExploring.pdf))
 
* {#Kantor11} [[Jean-Michel Kantor]], _Bourbaki's Structures and Structuralism_, The Mathematical Intelligencer __33__:1 (2011), 1, [doi](http://dx.doi.org/10.1007/s00283-010-9173-4)

* {#Awodey15} [[Steve Awodey]], _Structuralism, Invariance and Univalence_, 2014 ([pdf](https://www.andrew.cmu.edu/user/awodey/preprints/siu.pdf))

* {#Corfield15} [[David Corfield]], _A note on 'The' and 'The structure of' in Homotopy Type theory_, 2015 ([pdf](https://dl.dropboxusercontent.com/u/16936016/The_Structure.pdf))
category: philosophy