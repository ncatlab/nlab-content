
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

It is common in informal language to speak of mathematical objects "equipped with extra structure" of some sort. The archetypical examples are [[algebras over a Lawvere theory]] in [[Set]]: these are [[sets]] equipped with the structure of certain algebraic operations. For instance a [[group]] $(G, e, {\cdot})$ is a [[set]] $G$ equipped with a binary operation ${\cdot} : G \times G \to G$, etc.

One may formalize the notion of structure using the language of [[category theory]]. This is discussed at _[[stuff, structure, property]]_. In that formalization [[objects]] in some [[category]] $D$ are objects in some category $C$ _equipped with extra structure_ if there is a [[faithful functor]] $D \to C$.

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


## Related entries

* Evident as the notion of _mathematical structure_ may seem these days, it was at least not made explicit until the middle of the 20th century. Then it was the influence of the _[[Bourbaki]]_-project (see there for more) and then later the development of [[category theory]] which made the notion explicit and finally led to the above formalization.

* [[functions]] that preserves extra structure are called _[[homomorphisms]]_; [[relations]] that preserve extra structure are called _[[logical relations]]_

[[!redirects structure]]
[[!redirects structures]]
