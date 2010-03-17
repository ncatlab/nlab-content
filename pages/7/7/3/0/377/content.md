
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

[[topological space|Topological spaces]] are very useful, but also admit many pathologies.  (Although it should be admitted that often, one person's pathology is another's primary example.)  Over the years, topologists have accumulated many different conditions to impose on topological spaces to exclude various spaces considered "pathological;" here we list some of the most important of these conditions.

Sometimes one also imposes these conditions to ensure better behavior of the resulting _[[category]]_ of spaces; see [[nice category of spaces]] for more details, and also [[dichotomy between nice objects and nice categories]].  In many cases, a category of nice spaces will be [[reflective subcategory|reflective]] or coreflective.


## List of special nice types of topological spaces


* There is a whole slew of _separation conditions_, of which the most common is the [[Hausdorff space|Hausdorff]] condition (any two points can be separated by disjoint opens).  Hausdorff is also called $T_2$ and fits in a hierarchy ranging from $T_1$ through $T_4$ originally and now (at least) $T_0$ to $T_6$ (with some fractional subscripts too).

* [[sober space|Sobriety]] is a separation condition living in between $T_0$ and $T_2$ (but incomparable with $T_1$), which guarantees a good relationship with [[locale]]s.

* A space is [[compact space|compact]] if any open cover of it has a finite subcover.  Variations include locally compact, countably compact, sequentially compact, etc.

* _Locally compact Hausdorff_ spaces deserve special mention since they are [[exponential object|exponentiable]] in [[Top]].

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

## References 

* Steen and Seebach, _Counterexamples in topology_.


## Discussion

The following discussion has been acted upon by separating this page from [[nice category of spaces]].

+-- {: .query}
[[Tim Porter|Tim]]: As I read the entry on nice topological spaces, it really refers to 'nice categories' rather than 'nice spaces'! I have always thought of spaces such as CW-complexes and polyhedra as being 'locally nice', but the corresponding categories are certainly not 'nice' in the sense of  [[nice topological space]]. Perhaps we need to adjust that other entry in some way.

_Toby_:  You\'re right, I think I\'ve been linking that page wrongly.  (I just now did it again on [[homotopy type]]!)  Perhaps we should write [[locally nice space]] or [[locally nice topological space]] (you pick), and I\'ll fix all of the links tomorrow.

[[Tim Porter|Tim]]:I suggest [[locally nice space]].  (For some time I worked in Shape Theory where local singularities were allowed so the spaces were not locally nice!) There would need to be an entry on locally nice. I suggets various meanings are discussed briefly, e.g. locally contractible, locally Euclidean,  ... and so on, but each with a minimum on it as the real stuff is in CW-complex etc and these are the 'ideas'.

[[Mike Shulman|Mike]]: Why not change the page [[nice topological space]] to be about CW-complexes and so on, and move the existing material there to something like [[convenient category of spaces]], which is also a historically valid term?  I am probably to blame for the current misleading content of [[nice topological space]] and I'd be happy to have this changed.

_Toby_:  I thought that [[nice topological space]] was supposed to be about special kinds of spaces, such as locally compact Hausdorff spaces, whose full subcategories of $\Sp$ are also nice.  (Sort of a counterpoint to the [[dichotomy between nice objects and nice categories]], whose theme is better fit by the example of locally Euclidean spaces).  CW-complexes also apply ---if you\'re interested in the homotopy categories.

[[Mike Shulman|Mike]]: Well, that's not what I thought.  (-:  I don't really know any type of space that is nice _and_ whose corresponding subcategory of [[Top]] is also nice.  The category of locally compact Hausdorff spaces, for instance, is not really all that nice.  In fact, I can't think of anything particularly good about it.  I don't even see any reason for it to be complete or cocomplete!

I think it would be better, and less confusing, to have separate pages for "nice spaces" and "nice categories of spaces," or whatever we call them.  And, as I said, I don't see any need to invent a new term like "locally nice."

When algebraic topologists (and, by extension, people talking about $\infty$-groupoids) say "nice space" they usually mean either (1) an object of some convenient category of spaces, or (2) a CW-complex-like space, between which weak homotopy equivalences are homotopy equivalences.  Actually, there is a precise term for the latter sort: an [[m-cofibrant space]], aka a space of the (non-weak) homotopy type of a CW complex.

_Toby_:  I thought the full subcategory of locally compact Hausdorff spaces was cartesian closed?  Maybe not, and it\'s not mentioned above.

But you can see that most of the examples above list nice properties of their full subcategories.  And the page begins by talking about what a lousy category $\Top$ is.  So it seems clearly wrong that you can\'t make $\Top$ a nicer category by taking a full subcategory of nice spaces.  (Not all of the examples are subcategories, of course.)

[[Mike Shulman|Mike]]: It's true that locally compact Hausdorff spaces are [[exponentiable object|exponentiable]] in $Top$.  However, I don't think there's any reason why the exponential should again be locally compact Hausdorff.

I guess you are right that one could argue that compactly generated spaces themselves are "nice," although I think the main reason they are important is that the category _of_ compactly generated spaces is nice.  I propose the following:

1. Move the current content of this page to [[convenient category of spaces]].
1. Create [[m-cofibrant space]] (I'll do that in a minute).
1. Update most links to point to one or the other of the above, since I think that in most places one or the other of them is what is meant.
1. At [[nice topological space]], list many niceness properties of topological spaces.  Some of them, like compact generation, will also produce a [[convenient category of spaces]]; others, like [[CW complex]]es, will be in particular [[m-cofibrant space|m-cofibrant]]; and yet others, like [[locally contractible space]]es, will do neither.

_Toby_:  I believe that the compact Hausdorff reflection (the Stone&#8211;&#268;ech compactification) of $Y^X$ is an exponential object.

Anyway, your plan sounds fine, although [[nice category of spaces]] might be another title.  (I guess that it\'s up to whoever gets around to writing it first.)  Although I\'m not sure that people really mean m-cofibrant spaces when they speak of nice topological spaces when doing homotopy theory; how do we know that they aren\'t referring to CW-complexes? (which is what I always assumed that *I* meant).

[[Mike Shulman|Mike]]: I guess [[nice category of spaces]] would fit better with the existing cumbersomely-named [[dichotomy between nice objects and nice categories]].  I should have said that when people say "nice topological space" as a means of not having to worry about weak homotopy equivalences, they might as well mean (or maybe even "should" mean) m-cofibrant space.  If people do mean CW-complex for some more precise reason (such as wanting to induct up the cells), then they can say "CW complex" instead.

Re: exponentials, the Stone-&#268;ech compactification of $Y^X$ will (as long as $Y^X$ isn't already compact) have more points than $Y^X$; but by the isomorphism $Hom(1,Y^X)\cong Hom(X,Y)$, points of an exponential space _have_ to be in bijection with continuous maps $X\to Y$.

_Toby_:  OK, I\'ll have to check how exactly they use the category of locally compact Hausdorff spaces.  (One way is to get compactly generated spaces, of course, but I thought that there was more to it than that.)  But anyway, I\'m happy with your plan and will help you carry it out.

=--


[[!redirects nice topological spaces]]