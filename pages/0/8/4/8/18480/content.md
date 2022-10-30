
{:principle: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em
;"}






***

This page is about a formalization of the concept of [[directed graphs]] that is usual in combinatorics. 
For the usual definition of directed graph in category theory, see [[quiver]]. 
For some commentary on how the two formalizations relate to one another, see [[directed graph]].
The basic connection is: every directed graph is a quiver, not every quiver is a digraph. 
(In a reasonably loose sense of "is": type-theoretically, not every directed graph is a quiver, the formalizations being different.)




$\,$

disambiguation nLab page: _[[directed graph]]_

**this nLab page:** _directed graphs -- the combinatorial definition_: digraph

related nLab page: _directed graphs -- the category-theoretic definition_: [[quivers]]

$\,$

See also [[geometric shape for higher structures]].


***

$\,$

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

#### Graph Theory
+--{: .hide}
[[!include graph theory - contents]]
=--
=--
=--

#Digraphs#
* table of contents
{:toc}

## Idea

Digraphs are one of the ways to formalize the idea of *directed connections between [[points]]*: to use the [[category of sets]] and its limits, and to *choose* the *desired* connections from a usually much larger reservoir of *possible* connections. This has advantages and disadvantages. Other ways of formalization, such as [[quivers]], from the outset *start* with *only* the desired connections.


## Definitions


+-- {: .num_defn #Digraph}
###### Definition
**(digraph; directed graphs via [[material set theory]])**

A digraph is a [[pair]] $(V,A)$ of [[sets]], with $A\subseteq V\times V\setminus\{ (v,v)\colon v\in V\}$.
Here, $V\times V$ is the [[product]] in the [[category of sets]].
The elements of $V$ are called *vertices*, the elements of $A$ are called *arcs*. 


=--

+-- {: .num_defn #Neighbourhoods}
###### Definition
**(in-neighborhood, out-neighbourhood)**

Suppose $D=(V,A)$ is a digraph and $v\in V$. The *in-neighborhood* of $v$ in $D$, denoted $N^{\leftarrow}_D(v)$, is the set $\{ u\in V\colon (u,v)\in A\}$. The *out-neighborhood* of $v$ in $D$, denoted $N^{\rightarrow}_D(v)$, is the set $\{ u\in V\colon (v,u)\in A\}$.


=--


+-- {: .num_defn #Degrees}
###### Definition
**(in-degree, out-degree)**



Suppose $D=(V,A)$ is a digraph and $v\in V$. The *in-degree* of $v$ in $D$, denoted $d^{\leftarrow}_D(v)$, is the [[cardinality]] of the in-neighborhood of $v$ in $D$. The *out-degree* of $v$ in is defined analogously.


=--



+-- {: .num_defn #Walk}
###### Definition
**(walk in a digraph)**

Suppose $D=(V,A)$ is a digraph. A *walk* in $D$ is a [[sequence]] $P\colon\ell\rightarrow V\cup A$ with $P(0)\in V$, and for all $i\in\ell$ with $P(2i)\in V$, $P(2i+1)\in A$, and $P(2i+1) = (P(2i),P(2i+2))$. 

=--

Remark. $\ell=0$ is permitted; then, the only non-vacous condition is $P(0)\in V$.


+-- {: .num_defn #Trail}
###### Definition
**(trail in a digraph)**

Suppose $D=(V,A)$ is a digraph. A *trail* in $D$ is a walk $P$ in $D$ such that the [[restriction]] $P|_{    \{2i\colon i\in\ell\}            }$ is injective as a function.

=--



+-- {: .num_defn #Path}
###### Definition
**(path in a digraph)**

Suppose $D=(V,A)$ is a digraph. A *path* in $D$ is a trail $P$ in $D$ such that  $P$ itself is [[injective]] as a [[function]]. 

=--


+-- {: .num_defn #King}
###### Definition
**(king, coking, $d$-king, $d$-coking, $\infty$-king, $\infty$-coking)**

Suppose $D=(V,A)$ is a digraph. A vertex $v$ of $D$ is a *king* (resp. *coking*) of $D$ if and only if $(v,w)\in A$ (resp. $(w,v)\in A$) for all $w\in V\setminus\{v\}$. For any finite [[cardinal number|cardinal]] $d$, a vertex $v$ of $D$ is a *$d$-king* if and only if each vertex of $D$ can be reached along a path, starting with $v$, with at most $d$ arcs. A vertex $v$ of $D$ is an *$\infty$-king* if and only if each vertex of $D$ can be reached along a path, starting with $v$, having any finite number of arcs. $d$-coking and $\infty$-cokings are dually defined.


=--


## Remarks on the definitions

The *convention* to have *digraph* imply that there be *no loops* and *no parallel arcs*, and resort to other terms such as *directed pseudograph* to signal loops or parallel arcs, is widespread in modern combinatorics. 
Two modern examples are [p. 2](#DG2nd), and [Section 1.2](#DecompositionProof).

Unsurprisingly, while the convention that *digraph* implies that there be no parallel arrows has been widely adopted nowadays, there is a generous disregard for whether a digraph may contain loops. In this set-theoretical definition given above, this corresponds to the decision whether to allow $A$ to contain elements of the form $\{(v,v)\colon v\in V\}$. 

The terms *walk*, *trail* and *path* are standard in modern combinatorics. They are in particular compatible with standard usage in the theory of *undirected* graphs, in that upon forgetting (so to speak) the directions in the various definitions, one obtains the standard notions of *walk*, *trail* and *path* in (undirected) graph theory.

Needless to say (since given by the definitions), in a trail, *arc-repetitions are forbidden*, and in a path, *any repetition is forbidden*.

The terminology *king* above is standard in modern digraph theory; the term *coking* is not, but in tune with category-theoretic usages. The term *$\infty$-king* appears not to be attested but is[^1] in tune with a standard notion of $d$-king in digraph-theory, and a standard usage in contemporary mathematics to use $\infty$ to indicate that some parameter is permitted to take any value.

[^1]: According to recommendations received in email correspondence with mathematicians working in digraph theory.


A reason for treating the concept of $\infty$-kings here is A. J. Power's [proof](#Power1990) of a *pasting theorem*, a rigorous justification of the notational practice of [[diagrams]]: therein, both $\infty$-kings and $\infty$-cokings play an important role (Power calls $\infty$-kings "sources" and $\infty$-cokings "sinks"; both these terms clash with two standard technical terms in contemporary digraph theory, which is why the alternative terms were chosen).

## Uses of digraphs in category theory 

One reasons why digraphs are *relevant* to category theory (which does not usually study structures which do not have a [[composition]] structure, such as digraphs) are [[pasting schemes]], which are a rigorous justification of the (older) notational practice of [[pasting diagrams]]. 
Pasting diagrams are fundamental to [[higher category theory]]: already the axioms for various notions of higher categories are formalized in terms of pasting diagrams. 
The formal justification of pasting diagrams was achieved in the late 1980. 
Note that there are more than one definition of [[pasting scheme]] in the literature. 
E.g. there are M. Johnson's [Chapter 2](#Johnson1987) [Section 2](#Johnson1989) pasting schemes and  [Power's](#Power1990) pasting schemes. 
The definition which is *strictly relevant* to the present article is Power's: [Section 3](#Power1990) defines pasting schemes as a special kind of digraph, details will be found in one of the sections of [[pasting scheme]].




## References


* B. Csaba, D. K&#252;hn, A. Lo, D. Osthus, A. Treglown: Proof of the 1-factorization and Hamilton decomposition conjectures. Memoirs of the American Mathematical Society, 244 (2016), monograph 1154, 170 pages
{#DecompositionProof}

* [[Gregory Gutin]], [[Jørgen Bang-Jensen]]: _Digraphs: Theory, Algorithms and Applications_. Springer Monographs in Mathematics. Second Edition (2009)
{#DG2nd}

* [[Michael Johnson]]: _Pasting Diagrams in $n$-Categories with Applications to Coherence Theorems and Categories of Paths_, Doctoral Thesis, University of Sydney, 1987
{#Johnson1987}

* [[Michael Johnson]]: _The Combinatorics of $n$-Categorical Pasting_, Journal of Pure and Applied Algebra 62 (1989) 
{#Johnson1989}

* [[John Power]]: _A 2-Categorical Pasting Theorem_, Journal of Algebra 129 (1990) 
{#Power1990} 

[[!redirects digraph]]
[[!redirects digraphs]]

