> This entry is meant to be a **disambiguation page**, plus some **commentary** that would not fit well on either of the pages [[digraph]] and [[quiver]]. 
The term "directed graph" is somewhat intermediate between two rather precisely delineated terms: [[digraph]] and [[quiver]].
In a sense, "directed graph" is an undefined term, but the latter two both are defined. 
Every digraph is a quiver, not every quiver is a [[digraph]].

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Commentary

The term _directed graph_ is used in both [[graph theory]] and [[category theory]].
The definition varies---even within *one* of the two theories.

In [[graph theory]], _directed graph_ (often abbreviated to the contraction _digraph_) usually mean a [[digraph]], while in [[category theory]], directed graph/digraph usually means a [[quiver]]; the difference is: [[quivers]] may have multiple parallel arrows in the same direction, and also loops, while [[digraphs]] may not have any of those.

### Table of definitions of directed graphs in various references

This is to give a compressed look-up table, more or less usable without wandering anywhere else, telling you what definition of directed graph is being used in the reference you happen to be working with.



| reference | kind of directed graph | formalization used  | *word* used in reference | miscellaneous further comments |
|---------------------|---|-----|---------------|----------------------|
|  [BangJensenGutin2nd]({#DG2nd}) |    [[digraph]]               | the one in [[digraph]], except for a needless assumption of a vertex-set being non-empty: an empty vertex-set implies that the binary relation is the empty relation, but this *is* a [[digraph]] |  *digraph*  | beware that that book sometimes treats [[quivers]], but calls them *directed pseudographs* and formalizes those using [[multisets]] of ordered pairs |
| [BondyMurtyt1st](#BondyMurtyFirstEdition) | [[quiver]] | unusually hybrid functional-relational formalization via *families of ordered pairs* | *digraph*; beware that Bondy-Murty-digraphs are *not* [[digraphs]] | aversion to the void: needless assumption of vertex-sets being non-empty; essentially, Bondy-Murty-digraphs$\simeq$Schrijver-digraphs|
| [ChartrandLesniakZhang6th](#CLZ2016) | [[digraph]] | the one in [[digraph]], except for a needless assumption of a digraph being non-empty set: the empty set *is* a [[digraph]] | *digraph* | beware that what the authors call "The First Theorem of Digraph Theory" is a *not* a theorem of "Digraph Theory" in the strictest technical sense of "Digraph Theory"($=$the first-order theory of irreflexive binary relations) since it *uses the language of arithmetic*|
|  [CsabaEtAl2016]({#DecompositionProof}) |    [[digraph]]               | the one in [[digraph]] |  *digraph*  | |
|  [DiestelGraphTheory4th]({#Diestel2010}) |    [[quiver]]               | usual one: the "nuts-and-bolts-definition" in [[quiver]] | *directed graph*; contraction *digraph* used but once in main text  | beware that *directed path* in the book means something different, type-theoretically at least, from *path in a [[digraph]]*: in the book, a *directed path* is itself a [[digraph]], not a sequence of vertices |
|  [FlajoletSedgewick1st]({#AnalyticCombinatorics2009}) |   [[binary relation]]               | [[binary relations]], formalized in [[material set theory]]-style, cf. [V.5.1](#AnalyticCombinatorics2009) | both  *digraph* and *directed graph* used interchangeably | beware that Flajolet-Sedgwewick-digraphs are just [[binary relations]], *not* [[digraphs]] |
|  [SchrijverComOpt1st]({#Schriver2003}) |    [[quiver]]               | unusually hybrid formalization via *families of ordered pairs*; Bondy-Murty formalise Schrijver's *family* using a function called $\psi_D$ | *digraph*; beware that Schrijver-digraphs are *not* [[digraphs]] | no aversion to the void here; moreover, note that SchrijverDigraphs$\simeq$Bondy-Murty-digraphs  |

Note that "kind of directed graph" is a used in a loose, undefined sense, sufficiently clear from the context. 

### Further Commentary

#### Connections to category theory

Herein some evident aspects are pointed out explicitly.

##### Underlying quivers

A *nonempty* [[digraph]] never is isomorphic to the [[quiver]] [[forgetful functor|underlying]] any category: such a quiver *always* has a loop at each vertex, which is already enough to rule out any isomorphism. 


##### A genuine applications of [[digraphs]] to [[category theory]]

An example of a use of digraph theory in category theory is giving a rigorous justification of the  notational practice of [[pasting diagrams]]. 
This was achieved in the late 1980s (cf. e.g. [Johnson 1987](#Johnson1987), [Johnson 1989](#Johnson1989), [Power 1990](#Power1990)). 
In this approach, parallel arcs or loops are of secondary importance, and sometimes expressly forbidden, so the work of Johnson and Power can be seen as a genuine application of graph theory to category theory. 


##### *All* quivers deemed irreflexive by Lawvere


There is an article of [[William Lawvere]] which is relevant in one precise respect to a disambiguation page such as the present one: *an unusual use of the adjective "irreflexive"*. 
Therein, one reads (cf. ([Lawvere 1989](#GeneralizedGraphs), page 272)) 

> [..] the elementary "parallel process" $E= \bullet\overset{\rightarrow}{\rightarrow}\bullet$ is a reflexive graph which happens to admit only one definition of composition making it into a category $\mathbf{P}$. [..] Its [[actions]] $S^{\mathbf{P}^{\mathrm{op}}}$ are the **irreflexive** graphs (the negative is in a way appropriate even for those objects which happen to have loops at some point $p$, for morphisms are allowed to interchange *any* two such loops).

With "the negative is in a way appropriate" Lawvere explains the use of the strong negation *irr-*, despite such an "irreflexive graph" being permitted to contain loops at *some* of its vertices, which is obviously different from what one would expect from the usual sense of [[irreflexive relation]]. 
This is a usage in need of explanation, all the more against the backdrop of contemporary teaching where the term "simple undirected graph" is often literally defined as symmetric irreflexive relation (on the vertex set).

Some authors have adopted this interesting variant sense of "irreflexive", prompting an additional use of the a modifier "strict" to form a composite "strict irreflexive graph". (cf. ([Brown et al 2008](#GraphsOfMorphismsOfGraphs)), which uses "digraph" as a synonym for "strict irreflexive graph", and this sense of "digraph" is precisely the one in [[digraph]]). 
In a sense, a [[digraph]] is a "strictly-Lawvere-irreflexive graph".



From a graph-theoretical point of view, every digraph is a quiver, but not every quiver is a digraph (again, in the sense of [Gutin and Bang-Jensen 2009](#DG2nd)).

##### Cultural differences in what to regard as simpler 

The convention of formalising directed graphs like in [[digraph]] is widespread in modern combinatorics, but it is mostly just that: conventional. 
In particular, forbidding parallel arcs, and in particular, forbidding loops by yaking the  [[relative complement]] of $V\times V$ and the diagonal $\{(v,v)\colon v\in V\}$ is sometimes [^1] regarded to a *needless and negative complication* , and sometimes ([p.2,first paragraph]](#BumbyLatch1986) regarded the typical way of doing things in category theory. 
This is a matter of opinion and culture; similar comparisons can be found in what is perhaps the earliest article reviewing graph theory from a category theoretic perspective (cf. [Bumby-Latch 1986](#BumbyLatch1986)).

[^1]: T. Leinster: " ...  the irreflexivity condition tastes strange on a category theorist's tongue. We're suspicious of negatives. " In: [The n-Category Caf&#233;: April 12, 2013](https://golem.ph.utexas.edu/category/2013/04/colouring_a_graph.html)



Some reasonably distinct aspects of this: 

* While arguably the *simplest nontrivial limit of all*, the definition of [[digraphs]] uses a [[limit]] of the [[category of sets]], the [[cartesian product]] of the vertex set with itself, while the definition of [[quivers]] avoids doing so, and can therefore be interpreted in categories which do not have all binary products. 

* It is a fact that [[quivers]] are more general than [[digraph]]s: to have [[digraph]] offer multiple arcs or loops requires additional patching, like using *families of ordered pairs* (this is done in e.g. BondyMurty) or switching to other definitions.
Many references in the combinatorial literature are aware of that,  of course, e.g. ([Diestel 2010](#Diestel2010)) defines a "directed graph" precisely to be a [[quiver]], without mentioning the word.  

* The restriction to loopless quivers without parallel arcs is mostly a result of 

** the kind *questions* that are answered in the combinatorial literature, which are often of a counting or decomposing kind,
** a tendency in combinatorics to formalize *multiplicities* by *attaching weights* of some "alien" type (mostly [[number]]s) to the single arc of a graph; in category theory, on the other hand, there is a tendency to prefer doing constructions for a given purpose by a more uniform method, instead of attaching objects of different types to another structure. 


The difference between the two formalizations, given in [[digraph]] and [[quiver]], can be seen to be similar to the differences between [[material set theory]] and [[structural set theory]].

The material point of view makes the decision of how to represent the connections loom large (examples are the various different data structures for digraphs, such as signed adjacency matrices, signed incidence matrices, linked lists for adjacency *lists*, one often vastly more efficient than the other).  

The structural point of view, exemplified by [[quivers]], in a way already fixes the formalizing concept: functions. 
It then only remains to be decided how to represent function. 

All these points of view have disadvantages and advantages and it depends on what one is trying to do what one should use.

## Related concepts

* [[digraph]] 
* [[graph]]
* [[quiver]]
* [[n-quiver]]
* [[ribbon graph]]



## References


* A. Bondy, U.S.R. Murty: Graph Theory with Applications. Fifth Printing. North Holland 1982.
{#BondyMurtyFirstEdition}

* Gary Chartrand, Linda Lesniak, Ping Zhang: _Graphs & Digraphs_. Sixth edition. CRC Press. 2016
{#CLZ2016}


* B. Csaba, D. K&#252;hn, A. Lo, D. Osthus, A. Treglown: Proof of the 1-factorization and Hamilton decomposition conjectures. Memoirs of the American Mathematical Society, 244 (2016), monograph 1154, 170 pages
{#DecompositionProof}


* [[Ronald Brown]], I. Morris, J. Shrimpton, C.D. Wensley: _Graphs of morphisms of graphs_, The Electronic Journal of Combinatorics 15 (2008), A1
{#GraphsOfMorphismsOfGraphs}

* R. Diestel: _Graph Theory_. Fourth Edition. Springer (2010)
{#Diestel2010}


* [[Philippe Flajolet]], Robert Sedgewick, _Analytic Combinatorics_, 2009 ([pdf](http://algo.inria.fr/flajolet/Publications/book.pdf))
{#AnalyticCombinatorics2009}

* [[Gregory Gutin]], [[Jørgen Bang-Jensen]]: _Digraphs: Theory, Algorithms and Applications_. Springer Monographs in Mathematics. Second Edition (2009)
{#DG2nd}

* [[Michael Johnson]]: _Pasting Diagrams in $n$-Categories with Applications to Coherence Theorems and Categories of Paths_, Doctoral Thesis, University of Sydney, 1987
{#Johnson1987}

* [[Michael Johnson]]: _The Combinatorics of $n$-Categorical Pasting_, Journal of Pure and Applied Algebra 62 (1989) 
{#Johnson1989}

* [[William Lawvere]]: _Qualitative Distinctions Between Some Toposes of Generalized Graphs_, Contemporary Mathematics 92 (1989) 
{#GeneralizedGraphs}

* [[John Power]]: _A 2-Categorical Pasting Theorem_, Journal of Algebra 129 (1990) 
{#Power1990}

* [[Alexander Schrijver]]: _Combinatorial Optimization_. Volume A. Springer. First  Edition (2003)
{#Schrijver2003}


[[!redirects directed graph]]
[[!redirects directed graphs]]
[[!redirects Directed graph]]
[[!redirects Directed graphs]]