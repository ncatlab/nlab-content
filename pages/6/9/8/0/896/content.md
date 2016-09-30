
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Notions of subcategory
+-- {: .hide}
[[!include notions of subcategory]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

If one accepts the notion of [[subcategory]] without any qualification (as discussed there), then:

A [[subcategory]] $S$ of a category $C$ is a **full subcategory** if for any $x$ and $y$ in $S$, every morphism $f : x \to y$ in $C$ is also in $S$ (that is, the inclusion [[functor]] $S \hookrightarrow C$ is [[full functor|full]]).

This inclusion functor is often called a __full embedding__ or a __full inclusion__.

Notice that to specify a full subcategory $S$ of $C$, it is enough to say which [[object]]s belong to $S$.  Then $S$ must consist of all [[morphism]]s whose [[source]] and [[target]] belong to $S$ (and no others).  One speaks of the _full subcategory on_ a given set of objects.

This means that equivalently we can say:

A functor $F : S \to C$ exhibits $S$ as a **full subcategory** of $C$ precisely if it is a [[full and faithful functor]].
($S$ is the [[essential image]] of $F$).

## Properties

+-- {: .num_example #FullSubcategoryInclusionsReflectCoLimits}
###### Example

A [[fully faithful functor]] (hence a [[full subcategory]] inclusion) reflects all limits and colimits.

=--

This is evident from inspection of the defining [[universal property]].


## Related concepts

* [[reflective subcategory]]

* [[coreflective subcategory]]

* [[fully faithful functor]]

* [[sub-(infinity,1)-category]]

[[!redirects full subcategories]]
[[!redirects full embedding]]
[[!redirects full embeddings]]
[[!redirects full imbedding]]
[[!redirects full imbeddings]]
[[!redirects full inclusion]]
[[!redirects full inclusions]]