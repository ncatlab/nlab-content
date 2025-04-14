

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}


The [[category]] [[TopSp]] of all [[topological spaces]] serves in the foundations of many subfields of [[mathematics]], as reflected in the widely (but not universally) accepted convention that "space" in [[mathematics]] means "[[topological space]]", by default. However, the great flexibility of the notion of topological spaces also has its drawbacks, as without further qualification it tends to be a little too general for usage in any given sub-field.  At the same time, the relevant further conditions typically required on topological spaces in any given application varies, sometimes considerably, and many further such conditions have been and are being introduced. Hence what counts as a well-behaved ("nice") topological spaces strongly depends on context, and the main point to be aware of is the existence of key *classes* of possible extra conditions on topological spaces. 

The foremost among these are certainly the *[[separation axioms]]*, which may be understood as prescribing how exotic (pathological) a topological space is allowed to be, locally, as compared to the archetypical example of *[[Euclidean space]]* (which, it is worthwhile to remember, was the default meaning of "space" for most of human history). In consequence, [[separation conditions]] are typically required of  topological spaces if and to the extent that these are used as models for *space* in the original sense of [[geometry]]. Probably the most prominent among the separation axioms is the [[Hausdorff space|Hausdorff]]-condition "[[T2-space|$T_2$]]", and many authors will by default mean "[[Hausdorff topological space]]" when saying "topological space".

Another class of nicety conditions on topological spaces are not primarily motivated by the look of the individual spaces, but by ensuring that the (preferably ([[coreflective subcategory|co-]])[[reflective subcategory|reflective]]) [[full subcategory]] of spaces satisfying these conditions has good [[category theory|category theoretic]] properties, such as [[cartesian closed category|cartesian closure]]
(but beware that there is a [[dichotomy between nice objects and nice categories]]).
Such *[[convenient categories of topological spaces]]* are of foundational importance in [[algebraic topology]] where it is tolerable to change the [[homeomorphism]]-type of a space as long as its [[homotopy type]] is retained. Prominent examples of classes of topological spaces which are "nice" in a way that their categories are "convenient", in this sense, are the "[subcategory-generated spaces](convenient+category+of+topological+spaces#CategoriesOfColimitsOfGeneratingSpaces)", namely those that may be obtained as [[colimits]] of building block spaces taken from a given [[full subcategory]]. For example, if these building blocks are taken to be all [[compact spaces]] then one speaks of *[[compactly generated topological spaces]]*, while if they are taken to be all [[Euclidean spaces]] one speaks of [[Delta-generated topological spaces]].

Further in this vein of [[algebraic topology]] and [[homotopy theory]] are conditions on a topological space which ensure that it is a good model for its ([[weak homotopy type|weak]]) [[homotopy type]]. For example, the condition that a topological space be a [[CW-complex]] (hence  [[cofibrant object|cofibrant]] in the [[classical model structure on topological spaces|classical model structure]]) ensures that [[continuous functions]] out of it model all [[homotopy classes]] of morphisms out of the homotopy type (as witnessed by [[Whitehead's theorem]]), while the condition that a [[topological group]] be *[[well-pointed topological group|well-pointed]]* (hence [[cofibrant object|cofibrant]] in the [[model category of pointed objects|pointed]] [[Strøm model category]]) ensures that the [[geometric realization of simplicial topological spaces|topological realization]] of its [[nerve]] has the expected [[homotopy type]]. It is this last condition which leads over to the notion of [[nice simplicial topological spaces]].



## Some example conditions

The following is a list -- currently somewhat random and highly incomplete -- of nicety conditions that are considered on topological spaces.

* There is a whole slew of _[[separation conditions]]_, of which the most common is the [[Hausdorff space|Hausdorff]] condition (any two points can be separated by disjoint opens).  Hausdorff is also called $T_2$ and fits in a hierarchy ranging from $T_1$ through $T_4$ originally and now (at least) $T_0$ to $T_6$ (with some fractional subscripts too).

* [[sober space|Sobriety]] is a separation condition living in between $T_0$ and $T_2$ (but incomparable with $T_1$), which guarantees a good relationship with [[locale]]s.

* A space is [[compact space|compact]] if any open cover of it has a finite subcover.  Variations include locally compact, countably compact, sequentially compact, etc.

* _[[locally compact Hausdorff spaces]] deserve special mention since they are [[exponential object|exponentiable]] in [[Top]].

* A [[compactly generated space]] is, essentially, one whose topology is determined by its restriction to compact subspaces.  These are notable because the category of compactly generated spaces is [[cartesian closed category|cartesian closed]].

* A _metrizable_ space is one whose topology can be defined by a [[metric space|metric]].  We also have pseudometric spaces, quasimetric spaces, uniformizable spaces, etc.

* A [[sequential space]] is one whose topology is determined by convergence of sequences.  Note that any topology is determined by convergence of [[net]]s or [[filter]]s.

* A [[CW complex]] is a space built out of nothing by progressively attaching cells of higher and higher dimension.  More generally, a [[cell complex]] is a space built by attaching cells, without regard to dimension (that is, lower-dimensional cells may be attached to higher-dimensional ones), and an [[m-cofibrant space]] is one that is [[homotopy equivalence|homotopy equivalent]] to a CW complex (or equivalently a cell complex).  These types of spaces are important for [[homotopy theory]] because they turn [[weak homotopy equivalence]]s into [[homotopy equivalence]]s.

* A [[locally Euclidean space]] such as a [[topological manifold]] is a space that is locally homeomorphic to $\mathbb{R}^n$ for some $n$.

* (add your favorite!)

## Related concepts

* [[nice simplicial topological space]]

* [[convenient category of topological spaces]]


## References 

Discussion of notorious subtleties:

* [[Lynn Arthur Steen]], [[J. Arthur Seebach]], _[[Counterexamples in Topology]]_, Springer 1970/1978 ([doi:10.1007/978-1-4612-6290-9](https://link.springer.com/book/10.1007/978-1-4612-6290-9))




[[!redirects nice topological spaces]]