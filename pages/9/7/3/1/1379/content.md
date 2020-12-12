
# Proper classes
* table of contents
{: toc}

## Idea

A _proper class_ is a [[set]] that is too big to be a set.  Exactly what this means depends on the [[foundations]] of mathematics, but something must be said about it to study [[large category|large categories]].


## Definitions

There are several ways to deal with this and define a proper class.

A __proper class__ is a [[large category|large]] [[discrete category]].  But since a large category is usually defined as having a proper class of objects, this just moves the bubble under the wallpaper to 'large category' and something must be applied there.

A __proper class__ is a collection that can be put in [[bijection]] with the class of all [[ordinal number|ordinals]], $Ord$.  But this requires the [[global axiom of choice]] to be correct.

A __proper class__ is a class that is not a [[set]].  So now we have to define 'class'.

A __proper class__ is a class whose cardinality is not the [[cardinal number]] of any set.  This is a  version of the previous definition not violating the [[principle of equivalence]]; however, in some foundations these are actually equivalent (using the [[axiom of replacement]]).

A __class__ is a collection of [[sets]].  Here the bubble is moved to 'collection', but we will be able to pop that bubble below.  Also we might want to allow the members of a proper class to be other than sets (such as [[structured sets]]); certainly it is true, however, that a __pure class__ is a collection of [[pure sets]].

A __class__ is a formula in the language of [[set theory]] for a [[truth value]], equipped with a specified [[free variable]] for a set.  This is a formalisation of the previous definition, but it must be interpreted metamathematically: a __formula for a class__ in a given [[context]] $\Gamma$ is a formula for a truth value in the extension of $\Gamma$ by one more free variable for a set.

A __class__ may even be an undefined concept; the real definition is to define a __[[set]]__ as a class that is itself a member of some class.  With appropriate axioms, this is equivalent to the previous definition (and conservative over set theory without classes), but it\'s also possible to apply stronger axioms here; this choice is the difference between $BNG$ and $MK$ as extensions of [[ZFC]].

A __class__ is a [[subset]] of a [[Grothendieck universe]] $U$, while a ([[small category|small]]) __set__ is merely an element of $U$.  This gives a relative notion, depending on $U$.  As stated here, we get a concept of class like that of the strong theory $MK$; to be more like $BNG$ (and therefore conservative over set theory without an axiom of universes) we should define a __class__ to be a subset of $U$ that is definable in the language of set theory.


## Usage

A __[[large category]]__ is a [[category]] whose class of [[morphisms]] is a proper class.  It is sufficient that the class of [[objects]] be a proper class, which is also necessary if the category is [[locally small category|locally small]].

Category theorists care about proper classes because many examples of categories in practice (such as [[Set]], to begin with!) are large.


## Category of classes

The [[category of classes]] is closed under all large [[colimits]]
and [[small limits]].
See the linked article for more information and precise definitions.

Just as an [[elementary topos]] is an axiomatization of basic properties of the category [[Set]], a [[category with class structure]] is an axiomatization of basic properties of the category $Class$.  See also [[algebraic set theory]].

## References

A paper detailing one approach to the technical side of how classes appear in [[category theory]] (namely using [[Grothendieck universes]]) is

* {#Levy18} Paul Blain Levy, _Formulating Categorical Concepts using Classes_ (arXiv:[1801.08528](https://arxiv.org/abs/1801.08528))

[[!redirects class]]
[[!redirects classes]]
[[!redirects proper class]]
[[!redirects proper classes]]
