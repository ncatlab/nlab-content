
> This article is about "digraphs" in the usual combinatorial sense. 
For the usual notion of directed graph in category theory, see [[quiver]].

#Contents#
* table of contents
{:toc}




## Definition

A digraph is a pair $(V,A)$ of [[sets]], with $A\subseteq V\times V\setminus\{ (v,v)\colon v\in V\}$.

Cf. e.g. [p. 2](#DG2nd).


## Related concepts
 

Unsurprisingly, a generous disregard to issues around allowing loops or not, and sometimes even to allowing parallel arcs, is common in the literature. Because of the additional information given by directions, digraph theory tends to have more technical terms than the theory of undirected graphs, in particular, some systematic prefix-constructions (like *in-neighbor*).

We here list a few, calibrating our conventions according to [BJG2009](#DG2nd), but only in so far as they are fundamental and potentially useful in category theory.[^1] For concision and robustness, we mostly use words.


**arc**: directed edge

**in-neighbour of $v$**: vertex from which there is one (and  because of the prohibition of parallel arcs, only one) arc into $v$ 

**out-neighbour of $v$**: vertex for which there is one (and because of the prohibition of parallel arcs, only one) arc from $v$ to it 

**walk**: [[sequence]] alternating between vertices and (zero or more) arcs, *always* starting with a vertex, each arc pointing towards the next vertex, and either ending it a vertex, or countably infinite 

**trail**: walk without any repeated arcs 

**path**: trail without any repeated vertices 

**cycle**: finite trail with precisely one repetition: the last component of the sequence (necessarily a vertex) being [[equal]] to its first component 

Remarks. For the definitions of _trail_ and _path_, which in particular involve negations, to be sensical, both the vertex [[set]] and the arc [[set]] of the digraph need to have an [[equality]] relation, and one has to work with a logic which allows negating equality.

One of the reasons why digraphs are relevant to category theory (which does not usually study structures which do not have a [[composition]] structure, such as digraphs) are: 

* [[pasting schemes]]

## References

* [[Gregory Gutin]], [[Jørgen Bang-Jensen]]: _Digraphs: Theory, Algorithms and Applications_. Springer Monographs in Mathematics. Second Edition (2009)
{#DG2nd}


[[!redirects digraph]]
[[!redirects digraphs]]