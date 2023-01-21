
> This entry is about a general concepts of "mathematical structure" in [[category theory]]. It subsumes but is more general than the concept of [[structure in model theory]].

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

It is common in informal language to speak of mathematical objects "equipped with [[extra structure]]" of some sort. The archetypical examples are [[algebras over a Lawvere theory]] in [[Set]]: these are [[sets]] equipped with the structure of certain algebraic operations. For instance a [[group]] $(G, e, {\cdot})$ is a [[set]] $G$ equipped with a binary operation ${\cdot} : G \times G \to G$, etc.

One may formalize the notion of structure using the language of [[category theory]]. This is discussed at _[[stuff, structure, property]]_. In that formalization [[objects]] in some [[category]] $D$ are objects in some category $C$ _equipped with extra structure_ if there is a [[functor]] $p \colon D \to C$ such that

* $p$ is a [[faithful functor]].

{#InCategoryTheory} Depending on author and situation, more properties are required of this functor ([Ehresmann 57](#Ehresmann57), [Ehresmann 65](#Ehresmann65), [Adamek-Rosicky-Vitale 09, remark 13.18](#AdamekRosickyVitale)):

* $p$ is an [[amnestic functor]] ($p$-vertical [[isomorphisms]] are [[identities]]),

* $p$ is an [[isofibration]] (isomorphisms can be lifted along $p$).

{#StrictStructure} However, notice that these two conditions violate the [[principle of equivalence]] for [[categories]]. In the terminology of _[[strict categories]]_ one might hence refer to these conditions as expressing "strict extra structure".


## Notions of structure 

A special class of examples of this is the notion of [[structure in model theory]]. In this case one defines a "language" $L$ that describes the constants, functions (say operations) and relations with which we want to equip sets, and then sets equipped with those operations and relations are called $L$-[[structure in model theory|structures]] for that language. (Equivalently one might say "sets with $L$-structure". Or one might generally say "$X$-structure" for "set with $X$-structure".) In this case there is a [[faithful functor]] from $L$-structures to their underlying sets, and so this is a special case of the general definition.

We instead say [[model]] of a [[theory]] when we restrict to those structures which satisfy the axioms of a theory (in other words, satisfy _properties_ specified by the axioms). In this case there is a full and faithful functor from the category of models of a theory $T$ to the category of structures of the underlying language $L(T)$, while the composition of forgetful functors 

$$Mod_T \to Struct_{L(T)} \to Set$$ 

is again faithful. 

+-- {: .num_remark}
###### Remarks 
Thus, the English word "structure" is used in several slightly differing mathematical senses. 

1. Within category theory itself, "structure" can function as a kind of mass noun, as in a phrase like "forgetting structure". Here it refers to data comprising operations, relations, constants, and _also properties_ borne by models of a theory or relative theory, considered abstractly (for example, the functor $Grp \to Set$ which forgets group structure, or the functor $Ring \to Ab$ which forgets multiplicative structure). On the other hand, it can also operate in the singular, where one says for example "a topological group is a topological space equipped with a group structure, such that..." 

1. In model theory, however, the term _structure_ is not a mass noun; it refers to a _particular_ set (or "structures" for a family of sets) together with functions, relations, and elements that interpret the symbols of operations, predicates, and constants of a _language_. When one adds axioms to a language to make a _theory_, then a structure of the language where those axioms get interpreted as properties _satisfied_ by the structure is called a _model_ of the theory. Thus, in summary, the category theorist might refer to "the structure of a group" as consisting of a multiplication, a unit, etc., satisfying group axioms, while the model theorist would say that each particular group (like $\mathbb{Z}$) is a model of a theory of groups.  For a model theorist, being a model does entail being a structure for the language of groups, but she would also say that a structure for the language of groups need not satisfy any of the axioms of a group (like associativity or unitality).
=-- 

## Examples

There are gazillions of examples of objects equipped with extra structure. The most familiar is maybe

* [[algebraic structure]].

Generally the [[forgetful functor]] from a category of algebras over an [[algebraic theory]] down to the base category exhibits the equipment with the corresponding algebraic structure.

## Structures in dependent type theory
 {#InDependentTypeTheory}

In [[dependent type theory]] the notion of "mathematical structure" and/or *data structure* on a base $B \,\colon\, Type$ is given by iterated [[dependent pairs|dependent pairing]] with $B$-dependent types encoding operations on/with this type together with their behavioural specification.


The following shows some examples, using the notation for [[dependent pairs]] from [[dependent functions and dependent pairs -- table|here]].

Via the [[extension (semantics)|extensionality]] principles for [[dependent pairs]] ([here](dependent+sum+type#ExtensionalityPrinciple)) and for [[dependent functions]] ([here](function+extensionality#StatementForDependentFunctions)) 

<img src="/nlab/files/DependentPairExtensionality-230121.jpg" width="600">

<img src="/nlab/files/DependentFunctionExtensionality-230121.jpg" width="600">


such type theoretic structure automatically obey the *[[structure identity principle]]*.


### Lensed data structure

To say that a given data (base) type $B \,\colon\, Set$ is

1. equipped with

   1. a [[function type|function]] $read_D \,\colon\, B \to D $ reading out $D$-data;

   1. a [[function type|function]] $write_D \,\colon\, D \times B \to B$ (over-)writing $D$-data;

1. such that this does behave as expected, namely as a [well-behaved](lens+in+computer+science#LensesAreCostateCoalgebras) $D$-[[lens (in computer science)|lens]]-structure on $B$

means to declare it to be of the following iterated [[dependent pair]]-type:

<img src="/nlab/files/WellBehavedLensDataStructure-210121.jpg" width="740">


### Group data structure
 {#GroupDataStructure}

The [[dependent pair]]-type declaration of [[group objects|group structure]]:

<img src="/nlab/files/GroupDataType-230121.jpg" width="740">


## Related entries

* Evident as the notion of _mathematical structure_ may seem these days, it was at least not made explicit until the middle of the 20th century. Then it was the influence of the _[[Bourbaki]]_-project (see there for more) and then later the development of [[category theory]] which made the notion explicit and finally led to the above formalization.

* [[functions]] that preserves extra structure are called _[[homomorphisms]]_; [[relations]] that preserve extra structure are called [[logical relations]]_

* [[Birkhoff's HSP theorem]]

* [[structuralism]], [[structure identity principle]]

* [[exceptional structure]]

## References

* {#Ehresmann57} [[Charles Ehresmann]], _Gattungen in Lokalen Strukturen_, 1957

* {#Ehresmann65} [[Charles Ehresmann]], _Cat&#233;gories et Structures_, Dunod, 1965

* {#AdamekRosickyVitale09} Adamek, Rosicky, Vitale, _Algebraic theories_ [pdf](http://www.iti.cs.tu-bs.de/~adamek/algebraic_theories.pdf) (2009)


[[!redirects structure]]
[[!redirects structures]]

[[!redirects mathematical structure]]
[[!redirects mathematical structures]]


