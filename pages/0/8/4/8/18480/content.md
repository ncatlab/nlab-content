
> This article is about "digraphs" in the usual combinatorial sense. 
For the usual notion of directed graph in category theory, see [[quiver]].
The basic connection is: every directed graph is a quiver, not every quiver is a digraph. 
(In a reasonably loose sense of "is": type-theoretically speaking, not every directed graph is a quiver, the formalizations being different.)

#Contents#
* table of contents
{:toc}


## Ideas

Digraphs are one way to formalize the idea of a *network* consisting *points with connections*. 

Many ways to do so exist. The particular sense of "digraph" documented here is a widespread one in the combinatorial literature, the underlying *idea* being that in this formalization the connections have some sort of *material existence*, lying around in a [[set]] of *all* connections there could possibly be, and *some* of them then being selected to form the network. 
This gives this definition a combinatorial flavour. 

Conceptually this is quite *distinct* from the *idea* underlying the definition of [[quivers]], wherein there are *only as many connections as one would like to have from the get-go*, and one then uses [[functions]], or, in another way of looking at it, [[functors]], to describe what is connected to what, and how. 

Conceptually, this distinction can meaningfully be compared with the distinction between [[material set theory]] and [[structural set theory]]: with digraphs, the connections within a have some material existence.



## Definitions


###### Definition
**(digraph in [[material set theory]]; cf. [p. 2](#DG2nd))**

A digraph is a pair $(V,A)$ of [[sets]], with $A\subseteq V\times V\setminus\{ (v,v)\colon v\in V\}$.


## Remarks on the definitions
 
The convention of having *digraph* imply that there be *no loops* and *no parallel arcs*, and resort to other terms such as *directed pseudograph* to signal loops or parallel arcs, is widespread in modern combinatorics, which is why we document it here, but it is mostly just that: conventional. 
In particular there is no mathematical reason to take the [[relative complement]] of $V\times V$ and the diagonal $\{(v,v)\colon v\in V\}$. 

It can be seen as either needlessly complicated and negative, or simpler and more intuitive than [[quivers]]. 
This is a matter of opinion and culture, and explicitly commented on in perhaps the earliest article reviewing graph theory from a category theoretic perspective (cf. [p. 2](#BumbyLatch1986)).

It is a matter of fact that [[quivers]] are more general. 
To have digraphs in the above sense offer multiple arcs or loops requires additional patching or switching to another definition. 



One of the reasons why digraphs are relevant to category theory (which does not usually study structures which do not have a [[composition]] structure, such as digraphs) are: 

* [[pasting schemes]]

## References

* J. A. Bondy, U. S. R. Murty: _Graph Theory With Applications_. Fifth Printing. North Holland (1976)
{#BondyMurty}

* R. T. Bumby, D. M. Latch: _Categorical Constructions in Graph Theory_. International Journal of Mathematics and Mathematical Sciences 9(1), 1--16
{#BumbyLatch1986}

* [[Gregory Gutin]], [[Jørgen Bang-Jensen]]: _Digraphs: Theory, Algorithms and Applications_. Springer Monographs in Mathematics. Second Edition (2009)
{#DG2nd}


[[!redirects digraph]]
[[!redirects digraphs]]