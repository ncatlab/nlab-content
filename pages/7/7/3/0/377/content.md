

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

[[topological space|Topological spaces]] are very useful, but also admit many pathologies.  (Although it should be admitted that often, one person's pathology is another's primary example.)  Over the years, topologists have accumulated many different conditions to impose on topological spaces to exclude various spaces considered "pathological;" here we list some of the most important of these conditions.

Sometimes one also imposes these conditions to ensure better behavior of the resulting _[[category]]_ of spaces; see [[nice category of spaces]] for more details, and also [[dichotomy between nice objects and nice categories]].  In many cases, a category of nice spaces will be [[reflective subcategory|reflective]] or coreflective.


## List of special nice types of topological spaces


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

* Steen and Seebach, _Counterexamples in topology_.




[[!redirects nice topological spaces]]