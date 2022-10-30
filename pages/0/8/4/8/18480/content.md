
{:principle: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em
;"}


***

This page is about a formalization of the concept of [[directed graphs]] that is usual in combinatorics. For the usual definition of directed graph in category theory, see [[quiver]]. 
For some commentary on how the two formalizations relate to one another, see [[directed graph]].



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

**Digraphs** are one way to formalize the idea of directed connections between [[points]]: digraphs use the [[category of sets]] and its limits, and to choose the desired connections from a usually much larger reservoir of possible connections. This has advantages and disadvantages. Other ways of formalization, such as [[quivers]], from the outset start with *only* the desired connections.


## Definitions


+-- {: .num_defn #Digraph}
###### Definition
**(digraph)**

A digraph is a [[pair]] $(V,A)$ of [[sets]], with $A\subseteq V\times V\setminus\{ (v,v)\colon v\in V\}$.
Here, $V\times V$ denotes the [[product]], and ${}\setminus{}$ the [[relative complement]] in the [[category of sets]].
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

Suppose $D=(V,A)$ is a digraph. A *walk* in $D$ is a [[sequence]] $P\colon\ell\rightarrow V\cup A$, where $\ell$ is an [[ordinal]], with $P(0)\in V$, and such that for all $i\in\ell$,  $P(2i)\in V$, $P(2i+1)\in A$, and $P(2i+1) = (P(2i),P(2i+2))$. 
The [[cardinality]] of the ordinal $\ell$ is called the *length* of $P$.


=--

Note that $\ell=0$ is permitted; then, the only non-vacous condition is that $P(0)$ be an element of $V$. That is, a path cannot start with an arc. 


+-- {: .num_defn #Trail}
###### Definition
**(trail in a digraph)**

Suppose $D=(V,A)$ is a digraph. 
A *trail* in $D$ is a walk $P$ in $D$ such that the [[restriction]] $P|_{  \{2i\colon i\in\ell\} }$ is injective as a [[function]].

=--



+-- {: .num_defn #Path}
###### Definition
**(path in a digraph)**

Suppose $D=(V,A)$ is a digraph. A *path* in $D$ is a trail $P$ in $D$ such that  $P$ itself is [[injective]] as a [[function]]. 

=--

The standard meaning of "path" in (di)graph theory is *somewhat opposite* to the standard topological meaning of [[path]]. 
In (di)graph theory, a "path" never has self-intersections, and hence (essentially) is a (di)graph isomorphisms onto its image, while in topology the term *path* signals that self-intersections *are* permitted. 
The standard term in topology for a path which is *free of self-intersections* is [[arc]] (eg [Kowalksky 1965](#Kowalksky65), Definition 29b). 
As a saving grace, the standard way to rigorously define the arcs of *plane* digraphs uses precisely the topological [[arcs]]. 



+-- {: .num_defn #King}
###### Definition
**(king, coking, $d$-king, $d$-coking, $\omega$-king, $\omega$-coking)**

Suppose $D=(V,A)$ is a digraph. 
A vertex $v$ of $D$ is a *king* (resp. *coking*) of $D$ if and only if $(v,w)\in A$ (resp. $(w,v)\in A$) for all $w\in V\setminus\{v\}$. 

For any finite [[cardinal number|cardinal]] $d$, a vertex $v$ of $D$ is a *$d$-king* if and only if each vertex of $D$ can be reached along a *path*, starting with $v$, the path having at most $d$ arcs. 

For any finite [[cardinal number|cardinal]] $d$, a vertex $v$ of $D$ is a *$d$-coking* if and only if for each $u\in V$ there exists at least one *path* starting with $u$ and ending with $v$ and having at most $d$ arcs. 

A vertex $v$ of $D$ is an *$\omega$-king* if and only if each vertex of $D$ can be reached along a path of $D$, starting with $v$, and having *any finite* number of arcs. 


A vertex $v$ of $D$ is an *$\omega$-coking* if and only if for each $u\in V$ there is at least one path of $D$, starting with $u$, ending with $v$, and having *any finite* number of arcs. 

=--

The term *$\omega$-king* is a natural variant of the usual term *$k$-king* in digraph theory. 

+-- {: .num_defn #PlaneDigraph}
###### Definition
**(plane digraph)**

A *plane digraph* consists of data 

* a subset $V\subseteq\mathbb{R}^2$ of the [[plane]]
* a [[set]] $A$ of [[arcs]] (in the usual topological sense), each $a\in A$ having the form $[0,1]\overset{a}{\rightarrow}\mathbb{R}^2$

and the axioms

(p.v) for each $a\in A$,  $a(0)\in V$ and $a(1)\in V$,

(p.d) if $a,a'\in A$ and if ($a(0) = a'(0)$ or $a(0) = a'(1)$ or $a(1) = a'(0)$ or $a(1) = a'(1)$), then $a=a'$,

(p.i) if $a\in A$ and $0\lt t\lt 1$, then $\neg\,(a(t)\in V)$,

(e.f) if $a,a'\in A$ and ( $\exists t:[0,1]$, $0\lt t \lt 1$ and $\exists t':[0,1]$, $0 \lt t' \lt 1$ and $a(t)=a(t')$ ), then $a=a'$.

=--

Plane digraphs are often introduced into a context like (abstract) digraphs are, i.e. by writing $D=(V,A)$, the type of $D$ being invisible from the notation.

While this article makes essential use of the treatment of plane graphs given in ([Diestel](#DiestelGraphTheoryFourthEd), Chapter 4), there are adaptations made for the present purposes: 

* here, *arc* means arc in the usual topological sense, without exception, while in ([Diestel](#DiestelGraphTheoryFourthEd)) "arc" is defined to be a [[subset]] of the  [[plane]], in particular is not parametrized, in particular does not carry directional information

* in ([Diestel](#DiestelGraphTheoryFourthEd), Chapter 4), both $V$ and $A$ in the definition of plane graphs are required to be [[finite sets]]. Here we make no such restriction.

## Remarks on the definitions

The *convention* to have digraph imply that there be no loops and no parallel arcs, and resort to other terms such as *directed pseudograph* to signal loops or parallel arcs, is widespread in modern combinatorics. 
Two modern examples are ([Gutin and Bang-Jensen](#DG2nd)), and ([Csaba et al](#DecompositionProof)).

Unsurprisingly, while the convention that digraph implies that there be no parallel arrows has been widely adopted nowadays, there is a generous disregard for whether a digraph may contain loops. In this set-theoretical definition given above, this corresponds to the decision whether to allow $A$ to contain elements of the form $(v,v)$. 

The terms *walk*, *trail* and *path* are standard in modern combinatorics. They are in particular compatible with standard usage in the theory of *undirected* graphs, in that upon forgetting (so to speak) the directions in the various definitions, one obtains the standard notions of walk, trail and path in (undirected) graph theory.

Needless to say (since given by the definitions), in a trail, arc-repetitions are forbidden, and in a path, any repetition is forbidden.

The terminology "king" above is standard in modern digraph theory; the term "coking" is not, but in tune with category-theoretic usages. The term "$\infty$-king" appears not to be attested but is in tune with a standard notion of $d$-king in digraph-theory, and a standard usage in contemporary mathematics to use $\infty$ to indicate that some parameter is permitted to take any value.


A reason for treating the concept of $\infty$-kings here is A. J. Power's proof ([Power 1990](#Power1990)) of a *pasting theorem*, a rigorous justification of the notational practice of [[pasting diagrams]]: therein, both $\infty$-kings and $\infty$-cokings play an important role (Power calls $\infty$-kings "sources" and $\infty$-cokings "sinks"; both these terms clash with two standard technical terms in, respectively, contemporary digraph theory and flow theory, which is why the alternative terms were chosen).

The choice of definitions documented here is biased towards (one of) the uses digraphs are put to in category theory, in particular in giving a rigorous justification of [[pasting diagrams]]. 
The most salient example of this is the emphasis given to *plane digraphs* in this article.


## Uses of digraphs in category theory 

One example of why digraphs are relevant to category theory are [[pasting schemes]], which are a rigorous justification of the (older) notational practice of [[pasting diagrams]]. 
Pasting diagrams are fundamental to [[higher category theory]]: already the axioms for various notions of higher categories are formalized in terms of pasting diagrams. 
The formal justification of pasting diagrams was achieved in the late 1980. 
Note that there are more than one definition of [[pasting scheme]] in the literature. 
E.g. there are M. Johnson's pasting schemes (([Johnson 1987](#Johnson1987), Chapter 2), ([Johnson 1989](#Johnson1989), Section 2)) and Power's pasting schemes ([Power 1990](#Power1990)). 
The definition which is strictly relevant to the present article is Power's. He defines defines pasting schemes as a special kind of digraph ([Power 1990](#Power1990), Section 3), details will be found at [[pasting scheme]] .




## References


* B. Csaba, D. K&#252;hn, A. Lo, D. Osthus, A. Treglown: Proof of the 1-factorization and Hamilton decomposition conjectures. Memoirs of the American Mathematical Society, 244 (2016), monograph 1154, 170 pages
{#DecompositionProof}


* {#DiestelGraphTheoryFourthEd} R. Diestel, Graph Theory, 4. ed., Springer 2010

* [[Gregory Gutin]], [[Jørgen Bang-Jensen]]: _Digraphs: Theory, Algorithms and Applications_. Springer Monographs in Mathematics. Second Edition (2009)
{#DG2nd}

* [[Michael Johnson]]: _Pasting Diagrams in $n$-Categories with Applications to Coherence Theorems and Categories of Paths_, Doctoral Thesis, University of Sydney, 1987
{#Johnson1987}

* [[Michael Johnson]]: _The Combinatorics of $n$-Categorical Pasting_, Journal of Pure and Applied Algebra 62 (1989) 
{#Johnson1989}

* [[John Power]]: _A 2-Categorical Pasting Theorem_, Journal of Algebra 129 (1990) 
{#Power1990} 

* {#Kowalksky65} H. J. Kowalksky: Topological Spaces. Academic Press. 1965.

[[!redirects digraph]]
[[!redirects digraphs]]
