
> This page is concerned with notions of locality in [[category theory]]. For notions in [[physics]] see instead e.g. *[[causal locality]]* or *[[local field theory]]* (which overlaps with a category-theoretic meaning via the notion of *[[extended functorial field theories]]*).


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--

# locally
* table of contents
{: toc}

## Meanings

In [[category theory]], 
the term "locally" is used in several ways with different (and not always compatible) meanings.

### Slice-wise

A [[category]] $C$ may be called "locally $P$" (for some property $P$) if each [[slice category]] $C/X$ is $P$. 

Examples include the notion of *[[locally cartesian closed categories]]*, i.e. those categories all whose [[slice categories]] are [[cartesian closed categories]].

### Hom-wise

A [[2-category]] $K$ (or more generally an [[enriched category]]) may be called "locally $P$" (for some property $P$) if each [[hom-category]] (or more generally [[hom-object]]) $K[X, Y]$ is $P$. Examples include [[locally-small categories]], [[locally discrete 2-categories]], and locally graded and locally indexed categories. Corresponding, we have terminology like [[local colimits]].

### Stalk-wise

In [[topos theory]] the term "local" typically refers to properties that hold after, possibly, passage to a [[cover]] or (if there are [[enough points]]) [[stalk]]-wise. 

Compare the notion of *[[local isomorphism]]* or the term *Local Homotopy Theory* for [[(infinity,1)-sheaf|$\infty$-sheaf]]-[[(infinity,1)-topos theory|theory]] &lbrack;[Jardine 2015](infinity-stack#Jardine15)&rbrack;

Via the case of [[2-sheaves]], i.e. [[category]]-valued [[stacks]] or [[internal categories]] in [[toposes]], this notion of "local" also applies to categories.

### Local presentability

Categories are called *[[locally presentable]]* if they are [[accessible category|accessible]] and [[cocomplete]]. The "locally" in the name is intended to disambiguate between such categories and the [[finitely presentable objects]] in the 2-category [[Cat]].

## Ambiguity

Unfortunately, these meanings can overlap. For instance, the term "locally cartesian closed 2-category" could in principle refer either to 

* a 2-category whose [[slice 2-categories]] are [[locally cartesian closed]]

or 

* a 2-category each of whose [[hom-categories]] are ([[locally cartesian closed category|locally]]) [[cartesian closed category|cartesian closed]]. 

For this reason, it is often worth considering whether a different term than "locally" may be used when naming such a concept.

(Note that for the [[bicategory of spans]] in some [[finitely complete category]] $E$ the [[hom-category]] $Span(E)(A, B)$ is the [[slice category]] $E/(A \times B)$.  Thus, hom-wise properties of $Span(E)$ coincide with slice-wise properties of $E$.)

## Related pages

- [[bi-]]

category: disambiguation
