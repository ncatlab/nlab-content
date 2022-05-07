

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


The [[category]] [[TopSp]] of all [[topological spaces]] serves in the foundations of many subfields of [[mathematics]], as reflected in the widely (but not universally) accepted convention that "space" in [[mathematics]] means "[[topological space]]", by default. However, the great flexibility of the notion of topological spaces also has its drawbacks, as, without further qualification, it tends to be a little too general for usage in any given sub-field.  At the same time, the relevant further conditions typically required on topological spaces in any given application varies, sometimes considerably, and many further such conditions have been and are being introduced. Hence what counts as a well-behaved ("nice") topological spaces strongly depends on context, and the main point to be aware of is the existence of key *classes* of possible extra conditions on topological spaces. 

The foremost among these are certainly the *[[separation axioms]]*, which may be understood as prescribing how exotic (pathological) a topological space is allowed to be, locally, as compared to the archetypical example of *[[Euclidean space]]* (which, it may be good to remember, was the default meaning of "space" for most of human history). In consequence, [[separation conditions]] are typically required of  topological spaces if and to the extent that these are used as models for *space* in the original sense of [[geometry]]. Probably the most prominent among the separation axioms is the [[Hausdorff space|Hausdorff]]-condition "[[T2-space|$T_2$]]", and many authors will by default mean "[[Hausdorff topological space]]" when saying "topological space".

Another class of nicety conditions on topological spaces are not primarily motivated by the look of the individual spaces, but by ensuring that the (preferably ([[coreflective subcategory|co-]])[[reflective subcategory|reflective]]) [[full subcategory]] of spaces satisfying these conditions has good [[category theory|category theoretic]] properties, such as [[cartesian closed category|cartesian closure]]
(but beware that there is a [[dichotomy between nice objects and nice categories]]).
Such *[[convenient categories of topological spaces]]* are of foundational importance in [[algebraic topology]] where it is tolerable to change the [[homeomorphism]]-type of a space as long as its [[homotopy type]] is retained. Prominent examples of classes of topological spaces which are "nice" in a way that their categories are "convenient", in this sense, are the "[subcategory-generated spaces](convenient+category+of+topological+spaces#CategoriesOfColimitsOfGeneratingSpaces)", namely those that may be obtained as [[colimits]] of a given [[full subcategories]] of building blocks. For example, if these building blocks are taken to be all [[compact spaces]] then one speaks of *[[compactly generated topological spaces]]*, while if they are taken to be all [[Euclidean spaces]] one speaks of [[Delta-generated topological spaces]].

Further in this vein of [[algebraic topology]] and [[homotopy theory]] are conditions on a topological space which ensure that it is a good model for its ([[weak homotopy type|weak]]) [[homotopy type]]. For example, the condition that a topological space be a [[CW-complex]] (hence  [[cofibrant object|cofibrant]] in the [[classical model structure on topological spaces|classical model structure]]) ensures that [[continuous functions]] out of it model all [[homotopy classes]] of morphisms out of the homotopy type (as witnessed by [[Whitehead's theorem]]), while the condition that a [[topological group]] be *[[well-pointed topological group|well-pointed]]* (hence [[cofibrant object|cofibrant]] in the [[model category of pointed objects|pointed]] [[Strøm model category]]) ensures that the [[geometric realization of simplicial topological spaces|topological realization]] of its [[nerve]] has the expected [[homotopy type]]. It is this last condition which leads over to the notion of [[nice simplicial topological spaces]].



## Some example conditions

The following is a list -- currently somewhat random and highly incomplete -- of nicety conditions conditions that are considered on topological spaces.

* There is a whole slew of _[[separation conditions]]_, of which the most common is the [[Hausdorff space|Hausdorff]] condition (any two points can be separated by disjoint opens).  Hausdorff is also called $T_2$ and fits in a hierarchy ranging from $T_1$ through $T_4$ originally and now (at least) $T_0$ to $T_6$ (with some fractional subscripts too).

* [[sober space|Sobriety]] is a separation condition living in between $T_0$ and $T_2$ (but incomparable with $T_1$), which guarantees a good relationship with [[locale]]s.

* A space is [[compact space|compact]] if any open cover of it has a finite subcover.  Variations include locally compact, countably compact, sequentially compact, etc.

* _[[locally compact Hausdorff spaces]] deserve special mention since they are [[exponential object|exponentiable]] in [[Top]].

* A [[compactly generated space]] is, essentially, one whose topology is determined by its restriction to compact subspaces.  These are notable because the category of compactly generated spaces is [[cartesian closed category|cartesian closed]].

* A _metrizable_ space is one whose topology can be defined by a [[metric space|metric]].  We also have pseudometric spaces, quasimetric spaces, uniformizable spaces, etc.

* A [[sequential space]] is one whose topology is determined by convergence of sequences.  Note that any topology is determined by convergence of [[net]]s or [[filter]]s.

* A [[CW complex]] is a space built out of nothing by progressively attaching cells of higher and higher dimension.  More generally, a [[cell complex]] is a space built by attaching cells, without regard to dimension (that is, lower-dimensional cells may be attached to higher-dimensional ones), and an [[m-cofibrant space]] is one that is [[homotopy equivalence|homotopy equivalent]] to a CW complex (or equivalently a cell complex).  These types of spaces are important for [[homotopy theory]] because they turn [[weak homotopy equivalence]]s into [[homotopy equivalence]]s.

* A (topological) [[manifold]] is a space that is locally homeomorphic to $\mathbb{R}^n$ for some $n$.

* (add your favorite!)

+-- {: .query}
[[David Roberts]]: How about mentioning [[Alexander Grothendieck]]'s notion of _tame topology_? I saw in the video of [Scharlau's talk](http://www.dailymotion.com/video/x8juek_colloque-grothendieck-winfried-scha_tech) that G. wrote a lot on this, but the manuscript is lost. Do we have any idea past a vague description? (in Recoltes et Semailles or La longue marche I think.)

[[Todd Trimble]]: Quite a few people have thought long and hard about Grothendieck's speculations on tame topology in his _Esquisse d'un Programme_. The approach with which I am most familiar comes from model theory, and falls under the rubric of "o-minimal structures" (the "o" standing for "order"). See the book _Tame topology and o-minimal structures_ by van den Dries. A space which belongs to an o-minimal structure is a subspace of some Euclidean space $\mathbb{R}^n$ and turns out to be indeed nice (it admits nice triangulations for instance). 

In a sense this is more of a "nice categories" approach than a "nice spaces" approach, because there is no known global property which would express what it means for a space to be tame. That is, there are many examples of o-minimal structures, but (it is conjectured) there is no maximal o-minimal structure, therefore no overarching meaning of what it would mean for a space to be tame. 

Basically, an o-minimal structure $T$ is a collection $T_n \subseteq P(\mathbb{R}^n)$ which is closed under all first-order logic operations (e.g., complements, finite intersections, direct images under projections = existentially quantified sets, equality predicates, and the binary predicate $\lt$ on $\mathbb{R}$), and which satisfies the all-important o-minimality condition: the only sets belonging to $T_1$ are finite unions of points and intervals. The elements of $T$ may be called $T$-*definable sets*; the archetypal example is where $T$ is the collection of semi-algebraic sets (loci of polynomial inequalities) -- cf. the Tarski-Seidenberg theorem. The thrust of the o-minimality condition is to forbid sets like $\mathbb{N} \subseteq \mathbb{R}$ from being $T$-definable, which (following G&#246;del, Turing, Robinson, Matiyasevich, and others) would open the door to all sorts of pathological sets being $T$-definable as well. So you could think of o-minimality as a kind of logical "monster-barring" device, which happens to be quite effective. See van den Dries's book for a very illuminating discussion. 

There are other approaches to tame topology (such as via Shiota's $\mathcal{X}$-sets), but I am less familiar with them.
=--

## Related concepts

* [[nice simplicial topological space]]

* [[convenient category of topological spaces]]


## References 

* [[Lynn Arthur Steen]], [[J. Arthur Seebach]], _[[Counterexamples in Topology]]_, Springer 1970/1978 ([doi:10.1007/978-1-4612-6290-9](https://link.springer.com/book/10.1007/978-1-4612-6290-9))




[[!redirects nice topological spaces]]