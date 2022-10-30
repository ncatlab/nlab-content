> This entry is meant to be a **disambiguation page**, plus some commentary that would not fit well on either of the pages [[digraph]] and [[quiver]]. 
The term "directed graph" is somewhat intermediate between two rather precisely delineated terms: [[digraph]] and [[quiver]].
In a sense, "directed graph" is an undefined term, but the latter two both are defined. 
Each digraph is a quiver, not every quiver is a digraph (sensu stricto).

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

In [[graph theory]], _directed graph_ (often abbreviated to the contraction _digraph_) usually means [[simple directed graph]], and in [[category theory]], _directed graph_ or _digraph_ usually means [[quiver]], hence may have multiple edges and loops. 
The basic *difference* is (according to one *widespread convention*) to have *digraphs* imply that there be neither any loop nor any *parallel* arc (directed cycles of length two *are* allowed in a digraph; cf. e.g. [Section 1.2](#DG2nd)). 

From a category-theoretic point of view, it is not superfluous to state the obvious fact that this is somewhat orthogonal to how the underlying [[quiver]] of a category looks like: _such_ a quiver *always* has a loop at each vertex, and, usually, many parallel arcs. 
In particular, the *underlying quiver of a category is never a digraph* (in the sense of, e..g,[BJG2009](#DG2nd)).

There is an influential (in that it made some authors use the term "irreflexive" within the composite "irreflexive graph" even though sensu stricto the term is wrong, at least when taken in the same sense as in "irreflexive binary relation") of [[William Lawvere]], very relevant to the above: in [p. 272](#GeneralizedGraphs) one reads


> [..] the elementary "parallel process" $E= \bullet\overset{\rightarrow}{\rightarrow}\bullet$ is a reflexive graph which happens to admit only one definition of composition making it into a category $\mathbf{P}$. [..] Its actions $S^{\mathbf{P}^{\mathrm{op}}}$ are the **irreflexive** graphs (the negative is in a way appropriate even for those objects which happen to have loops at some point $p$, for morphisms are allowed to interchange *any* two such loops).

[Editorial note: the author of the above passage drew a box around the (diagram of) the category E, but this is not done here, for technical reasons.]


An example of a use of digraph theory *sensu stricto* in category theory is giving a rigorous justification of the  notational practice of [[pasting diagrams]]. 
This was achieved in the late 1980s (cf. e.g. [Johnson87](#Johnson1987), [Johnson89](#Johnson1989), [Power90](#Power1990)). 
In this approach, parallel arcs or loops are of secondary importance. 



From a graph-theoretical point of view, it is not superfluous to emphasize the obvious fact that *every digraph is a quiver*, but *not every quiver is a digraph* (again, in the sense of [BJG2009](#DG2nd)).



## Related concepts

  * [[digraph]] (briefly, _a_ usual meaning of this term is a rather strict one: quiver with*out* any loop and with*out* any parallel edges)

  * [[graph]]

  * [[quiver]] (briefly, _the_ usual meaning of this term is _presheaf on the finite, two-object, four-morphism category with two parallel non-endomorphisms_, aka "the walking quiver" or "the elementary parallel process")

  * [[n-quiver]]

* [[ribbon graph]]



## References

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


[[!redirects directed graph]]
[[!redirects directed graphs]]
[[!redirects Directed graph]]
[[!redirects Directed graphs]]