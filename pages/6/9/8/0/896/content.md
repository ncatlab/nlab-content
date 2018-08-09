
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


## Idea

A [[subcategory]] 

$$
  \mathcal{C}
  \overset{\iota}{\hookrightarrow}
  \mathcal{D}
$$

of a given [[category]] $\mathcal{D}$ is meant to be _full_, if it includes "some [[objects]] but _all_ the [[morphisms]] between these objects".

This means _at least_ that $\iota$ is a [[fully faithful functor]]. In fact, that is the most one may demand while respecting the [[principle of equivalence]] of [[category theory]] and hence constitutes an invariant definition of _full subcategory_ (Def. \ref{InvariantDefinition} below).

However, a [[fully faithful functor]] need not be an [[injective function]] on [[objects]] (it is so only up to [[equivalence of categories]]). If one insists on defining a _[[subcategory]]_ inclusion to involve an [[injective function]] on the sets of objects and morphisms, this condition must be added to the condition of the inclusion functor being fully faithful. This leads to a non-invariant definition, discussed [below](#NonInvariantDefinition).

See also the discussion at _[[subcategory]]_ ([here](subcategory#VariantsInAccordWithThePrincipleOfEquivalence)).

## Definition



### Non-invariant definition
 {#NonInvariantDefinition}

If one accepts the notion of [[subcategory]] without any qualification (as discussed there), then:

A [[subcategory]] $S$ of a category $C$ is a **full subcategory** if for any $x$ and $y$ in $S$, every morphism $f : x \to y$ in $C$ is also in $S$ (that is, the inclusion [[functor]] $S \hookrightarrow C$ is [[full functor|full]]).

This inclusion functor is often called a __full embedding__ or a __full inclusion__.

Notice that to specify a full subcategory $S$ of $C$, it is enough to say which [[objects]] belong to $S$.  Then $S$ must consist of all [[morphism]]s whose [[source]] and [[target]] belong to $S$ (and no others).  One speaks of the _full subcategory on_ a given set of objects.

This means that equivalently we can say:

A [[subcategory]]-inclusion functor $F : S \to C$ exhibits $S$ as a **full subcategory** of $C$ precisely if it is a [[full and faithful functor]].
($S$ is the [[essential image]] of $F$).

Up to [[equivalence of categories]], every [[fully faithful functor]] is equivalent to a [[subcategory]]-inclusion in these sense of being an [[injection]] on the set of objects.


### Invariant definition
 {#InvariantDefinitionSection}

Therefore, the definition of _full subcategory_ which respects the [[principle of equivalence]] is simply this:

+-- {: .num_defn #InvariantDefinition}
###### Definition
**(invariant definition)**

A _full subcategory_-inclusion is a [[fully faithful functor]].

=--


## Properties

+-- {: .num_example #FullSubcategoryInclusionsReflectCoLimits}
###### Example

A [[fully faithful functor]] (hence a [[full subcategory]] inclusion) [[reflected limit|reflects]] all [[limits]] and [[colimits]].

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