
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


In [[philosophy]], _structuralism_ is the point of view which emphasises that the entities considered are parts of a system and that their very meaning and identity is defined according to its relation to the rest of the system.  For instance, if one part of the system changes in time, all other parts change as well. The system has features which are not just the composition of features of its constituent parts. 

### In the humanities

In the 20th century, structuralism in the humanities is associated with Emile Durkheim and Georg Simmel in sociology, Ferdinand de Saussure (and later Roman Jakobson) in linguistics, and [[Claude Lévi-Strauss]] in anthropology. 

### In philosophy of mathematics
 {#InThePhilosophyOfMathematics}

Structuralism is also the term given to a position in the [[philosophy of mathematics]] which holds that the entities treated in [[mathematics]] are simply structures. It is associated also with [[structural realism]] in the [[philosophy of science]], which maintains either that all we can know of the world is its structure (epistemological structural realism) or that indeed the world just is structure (ontological structural realism).

One may argue that [[category theory]] and [[type theory]] serve as formalization of these intuitive notions, see [below](#FormalizationInCategoryTheoryAndTypeTheory).

## Formalization of structuralism in category theory and type theory
 {#FormalizationInCategoryTheoryAndTypeTheory}

Since in a [[category]], the nature of any [[object]] is determined only by the system of _[[morphisms]]_ which relate this object to itself and to the other objects  of the category (by the [[Yoneda lemma]]), and not by how the object itself is [[generators and relations|presented]] (if it is at all), it may be argued that [[category theory]] provides a formalization of philosophical structuralism, at least in the [[philosophy of mathematics]] ([Awodey 96](#Awodey96), [Awodey 03](#Awodey03)). [[Yuri Manin]] said (citation?) that [[category theory]] regards [[objects]] as part of a "society". (See also at _[[objective logic]]_ for more on [[categorical logic]] and [[philosophy|philosophical]] notions.)

Notice that the terminology _[[morphism]]_ of course originates in _[[homomorphism]]_, since the morphisms in a category of [[mathematical structures]] (such as [[groups]], [[modules]], etc.) are precisely the maps of the underlying [[sets]] that preserve this structure.

This is essentially [[Bourbaki]]'s emphasis on [[mathematics]] as the science of abstract [[structures]], where structures are important only up to isomorphism and the emphasis is on relations (including) functions which are part of the "structure" (e.g. [Kantor 11](#Kantor11)).

However, a category need not be such a [[concrete category]] of sets with structure. Even when there is no such explicit structure on the objects, the same category-theoretic reasoning still applies and one may detect structure on objects from the morphisms between them.

For instance, while in general an object $X$ in a category does not have an underlying set, if the category has a [[terminal object]] $\ast$ one may still find a set of [[global elements]] of $X$ as the set of morphisms of the form $\ast \to X$.

Accordingly, in a category one only talks about properties invariant under [[isomorphisms]]; from such a point of view an [[object]] is determined by the morphisms to or from other objects. 

This perspective of the nature of objects of a category being determined only by the morphisms between them is fully embodied by the concept of [[equivalence of categories]]: two categories are to be regarded as equivalent if there is a [[functor]] between them that is [[essentially surjective]] in that it does not omit any [[isomorphism class]] of objects and which otherwise is a [[bijection]] on morphisms (precisely: on the [[hom-sets]] between any ordered pair of objects, a [[fully faithful functor]]). 

Given that [[type theories]] of sorts are the [[internal language]] of suitable kinds of [[categories]], with morphisms now being [[terms]] of [[function types]] (see at _[[relation between category theory and type theory]]_), these comments also give that type theory offers some kind of formalization of structuralism ([Awodey 15](#Awodey15), [Corfield 15](#Corfield15)).

Notably in [[homotopy type theory]] with [[univalence]], which is the [[internal language]] of categories called [[(infinity,1)-toposes]], the [[type universe]] reflects all the [[isomorphisms]] ([[equivalences]]) in the category in its [[identity type]], which therefore may be thought of as providing a structuralist concept of [[identity]].

(Notice however that the categories of [[mathematical structures]] such as [[groups]], [[modules]], etc., even when regarded as [[(infinity,1)-categories]], i.e. of [[infinity-groups]], [[(infinity,n)-modules]] etc.) are rarely [[(infinity,1)-toposes]]. The "structure" carried by an object in an $(\infty,1)$-topos is generically more a kind of geometric structure. 


## Related entries

* [[structure identity principle]]

* [[idealism]]

  * [[objective idealism]], [[objective logic]]

  * [[subjective idealism]]

  * [[absolute idealism]]


* [[Salomon Maimon]]


## References

* {#Awodey96} [[Steve Awodey]], _Structure in mathematics and logic: a categorical perspective_, Philosophia Mathematica (3), vol. 4,  p. 209-237, 1996 ([doi:10.1093/philmat/4.3.209](https://doi.org/10.1093/philmat/4.3.209))

* {#Awodey03} [[Steve Awodey]], _An Answer to Hellman's Question: "Does Category Theory Provide a Foundation for Mathematical Structuralism?"_, 2003 ([pdf](http://www.andrew.cmu.edu/user/awodey/preprints/awodeyVhellman.pdf), [doi:10.1093/philmat/12.1.54](https://doi.org/10.1093/philmat/12.1.54))

* {#MacLarty04} [[Colin McLarty]], 2004, _Exploring Categorical Structuralism_, Philosophia Mathematica, 12, 37&#8211;53 ([pdf](http://www.cwru.edu/artsci/phil/PMExploring.pdf))
 
* {#Kantor11} [[Jean-Michel Kantor]], _Bourbaki's Structures and Structuralism_, The Mathematical Intelligencer __33__:1 (2011), 1, [doi](http://dx.doi.org/10.1007/s00283-010-9173-4)

* {#Awodey15} [[Steve Awodey]], _Structuralism, Invariance and Univalence_, 2014 ([pdf](https://www.andrew.cmu.edu/user/awodey/preprints/siu.pdf))

* {#Corfield15} [[David Corfield]], _Expressing 'The Structure of' in Homotopy Type Theory_, 2015 ([pdf](https://dl.dropboxusercontent.com/u/16936016/The_Structure.pdf))

See also

* Wikipedia, _[Structuralism](http://en.wikipedia.org/wiki/Structuralism)_


category: philosophy