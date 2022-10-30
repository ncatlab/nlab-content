
> This article is about "digraphs" in the usual combinatorial sense. 
For the usual notion of directed graph in category theory, see [[quiver]].
The basic connection is: every directed graph is a quiver, not every quiver is a digraph. 
(In a reasonably loose sense of "is": type-theoretically speaking, not every directed graph is a quiver, the formalizations being different.)

#Contents#
* table of contents
{:toc}


## Ideas

Digraphs are one way to formalize the idea of *(directed) connections between points*. 
Many ways to do so exist. 



The underlying *idea* being that in this formalization the connections have some sort of *material existence*[^1], lying around in a [[set]] of *all* connections there could possibly be, and *some* of them then being selected to form the network. 
This gives this definition a combinatorial flavour. 

Conceptually, this is quite *distinct* from the *idea* underlying the definition of [[quivers]], wherein there are *only as many connections as one would like to have from the get-go*, and one then uses [[functions]], or, in another way of looking at it, [[functors]], to describe what is connected to what, and how. 
This distinction can meaningfully be compared with the distinction between [[material set theory]] and [[structural set theory]]: with digraphs, the connections within a have some material existence.

[^1]: This can be taken quite literally: mathematicians working in combinatorics tend to think of the connections as things lying about, some of them being of interest and selected. 
Moreover, the material point of view leaves the encoding-concept still up to the person using it: e.g. in programming, the connections have a material existence as some part of a data structure, and physically as some mark in some storage device. 
Arguably the most acute illustration of a disadvantage of this approach is the naive implementation of directed graphs via $0$-$1$-valued adjacency matrices containing a *stored* zero for each non-existing arc, resulting in a space complexity quadratic in the number of vertices, even if the graph has much fewer arcs. Needless to say, computer science has various ways to do better, but the point to be made here is that with [[quivers]] you *would not even think* of doing such a thing, having only as many elements in the arc set as you need.

## Definitions


###### Definition
**(digraph in [[material set theory]])**

A digraph is a pair $(V,A)$ of [[sets]], with $A\subseteq V\times V\setminus\{ (v,v)\colon v\in V\}$.


## Remarks on the definitions


The particular sense of "digraph" documented here is a widespread one in the combinatorial literature. 



The convention of having *digraph* imply that there be *no loops* and *no parallel arcs*, and resort to other terms such as *directed pseudograph* to signal loops or parallel arcs, is widespread in modern combinatorics. 

Some modern examples are [p. 2](#DG2nd) [Section 1.2](#DecompositionProof).



## Uses of digraph in category theory 

One reasons why digraphs are *relevant* to category theory (which does not usually study structures which do not have a [[composition]] structure, such as digraphs) are [[pasting schemes]], which are a rigorous justification of the (older) notational practice of [[pasting diagrams]]. 
Pasting diagrams are fundamental to [[higher category theory]]: already the axioms for various notions of higher categories are formalized in terms of pasting diagrams. 
The formal justification of pasting diagrams was achieved in the late 1980. 
Note that there are more than one definition of [[pasting scheme]] in the literature. 
E.g. there are M. Johnson's [Chapter 2](#Johnson1987) [Section 2](#Johnson1989) pasting schemes and  [Power's](#Power1990) pasting schemes. 
The definition which is *strictly relevant* to the present article is Power's: [Section 3](#Power1990) defines pasting schemes as a special kind of digraph, details will be found in one of the sections of [[pasting scheme]].

## References

* J. A. Bondy, U. S. R. Murty: _Graph Theory With Applications_. Fifth Printing. North Holland (1976)
{#BondyMurty}

* R. T. Bumby, D. M. Latch: _Categorical Constructions in Graph Theory_. International Journal of Mathematics and Mathematical Sciences 9(1), 1--16
{#BumbyLatch1986}

* R. Diestel: _Graph Theory_. Fourth Edition. Springer (2010)
{#Diestel2010}

* [[Gregory Gutin]], [[Jørgen Bang-Jensen]]: _Digraphs: Theory, Algorithms and Applications_. Springer Monographs in Mathematics. Second Edition (2009)
{#DG2nd}

* [[Michael Johnson]]: _Pasting Diagrams in $n$-Categories with Applications to Coherence Theorems and Categories of Paths_, Doctoral Thesis, University of Sydney, 1987
{#Johnson1987}

* [[Michael Johnson]]: _The Combinatorics of $n$-Categorical Pasting_, Journal of Pure and Applied Algebra 62 (1989) 
{#Johnson1989}

* [[John Power]]: _A 2-Categorical Pasting Theorem_, Journal of Algebra 129 (1990) 
{#Power1990} 

* Bela Csaba, Daniela K&#252;hn, Allan Lo, Deryk Osthus, Andrew Treglown: Proof of the 1-factorization and Hamilton decomposition conjectures. Memoirs of the American Mathematical Society, 244 (2016), monograph 1154, 170 pages
{#DecompositionProof}

[[!redirects digraph]]
[[!redirects digraphs]]