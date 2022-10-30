
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

## Terminology

The term _directed graph_ is used in both [[graph theory]] and [[category theory]] and the precise definition varies depending on the particular reference under consideration---even within one of the two theories.

In [[graph theory]], _directed graph_ (often abbreviated to the contraction _digraph_[^1]) usually means a [[simple directed graph]], and [[category theory]], _directed graph_ or _digraph_ usually means a [[quiver]], which may have multiple edges and loops; the basic *difference* being that (according to one *widespread convention*), the word *digraph* implies that there are neither loops nor *parallel* arcs (while directed cycles of length two *are* allowed in a digraph; cf. e.g. [Section 1.2](#DG2nd)). 

[^1]: In the nLab, this term tends to be avoided, since the prefix *di-* in this portmanteau is reminiscent of the prefix *bi-* in terms like *bicategory*, but does not have the same function (simply coming from contracting *directed*).

From a category-theoretic point of view, it is not superfluous to state the obvious fact that this is somewhat orthogonal to how the underlying [[quiver]] of a category looks like: that quiver *always* has a loop at each vertex, and, usually, many parallel arcs. In particular, the *underlying quiver of a category is never a digraph* (in the sense of, e..g,[BJG2009](#DG2nd)).

From a graph-theoretical point of view, it is not superfluous to emphasize the obvious fact that *every digraph is a quiver*, but *not every quiver is a digraph* (again, in the sense of [BJG2009](#DG2nd)).

Unsurprisingly, a generous disregard to issues around allowing loops or not, and sometimes even to allowing parallel arcs, is common in the literature. Because of the additional information given by directions, digraph theory tends to have more technical terms than the theory of undirected graphs, in particular, some systematic prefix-constructions (like *in-neighbor*).

We here list a few, calibrating our conventions according to [BJG2009](#DG2nd), but only in so far as they are fundamental and potentially useful in category theory.[^2] For concision and robustness, we mostly use words.


**arc**: directed edge

**in-neighbour of $v$**: vertex from which there is one (and  because of the prohibition of parallel arcs, only one) arc into $v$ 

**out-neighbour of $v$**: vertex for which there is one (and because of the prohibition of parallel arcs, only one) arc from $v$ to it 

**walk**: [[sequence]] alternating between vertices and (zero or more) arcs, *always* starting with a vertex, each arc pointing towards the next vertex, and either ending it a vertex, or countably infinite 

**trail**: walk without any repeated arcs 

**path**: trail without any repeated vertices 

**cycle**: finite trail with precisely one repetition: the last component of the sequence (necessarily a vertex) being [[equal]] to its first component 

Remarks. For the definitions of _trail_ and _path_, which in particular involve negations, to be sensical, both the vertex [[set]] and the arc [[set]] of the digraph need to have an [[equality]] relation, and one has to work with a logic which allows negating equality.


[^2]: One example of a use of digraph theory *sensu stricto* in category theory is giving a rigorous justification of the  notational practice called [[pasting scheme]]s, which was achieved in the late 1980s (cf. e.g. [Johnson87](#Johnson1987), [Johnson89](#Johnson1989), [Power90](#Power1990) ). 
There, parallel arcs or loops are of secondary importance. 



## Related concepts

  * [[graph]]

  * [[quiver]]

  * [[n-quiver]]

* [[ribbon graph]]



## References

* [[Gregory Gutin]], [[Jørgen Bang-Jensen]]: _Digraphs: Theory, Algorithms and Applications_. Springer Monographs in Mathematics. Second Edition (2009)
{#DG2nd}

* [[Michael Johnson]]: _Pasting Diagrams in $n$-Categories with Applications to Coherence Theorems and Categories of Paths_, Doctoral Thesis, University of Sydney, 1987
{#Johnson1987}

* [[Michael Johnson]]: _The Combinatorics of $n$-Categorical Pasting_, Journal of Pure and Applied Algebra 62 (1989) 
{#Johnson1989}


* [[John Power]]: _A 2-Categorical Pasting Theorem_, Journal of Algebra 129 (1990) 
{#Power1990}


[[!redirects directed graph]]
[[!redirects directed graphs]]
[[!redirects digraph]]
[[!redirects digraphs]]
[[!redirects Directed graph]]
[[!redirects Directed graphs]]