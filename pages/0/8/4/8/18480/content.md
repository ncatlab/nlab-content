
{:principle: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em
;"}


***

This page is about a formalization of the concept of [[directed graphs]] that is usual in combinatorics. For the notion of directed graph as commonly understood in category theory, see [[quiver]]. For some commentary on how the two formalizations relate to one another, see [[directed graph]].


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

# Contents
* table of contents
{:toc}

## Idea

In combinatorics, a **digraph** (a shortening of *directed graph*)  consists of a [[set]] and a [[binary relation]] on that set that is [[irreflexive relation|irreflexive]]. The elements of the set are called *nodes* or *vertices*, and elements of the relation are called *edges* or *arcs*; the idea is that whenever an ordered pair $(x, y)$ belongs to the relation, then we depict it as an arrow or directed edge going from node $x$ to node $y$. The irreflexivity condition means there is never an edge from a node to itself. 

## Definitions

+-- {: .num_defn #Digraph}
###### Definition
**(digraph)**

A digraph is a [[pair]] $(V,A)$ of [[sets]], with $A\subseteq V\times V\setminus\{ (v,v)\colon v\in V\}$.
Here, $V\times V$ denotes the [[product]], and ${}\setminus{}$ the [[relative complement]] in the [[category of sets]].
The elements of $V$ are called *vertices*, the elements of $A$ are called *arcs*. 

=-- 

+-- {: .num_example #ExampleDigraph} 
###### Example 
A basic example of a digraph is an [[ordinal]] $\alpha$ where $V$ is the underlying set of $\alpha$ and $A$ is the relation $\{(i, i+1): i, i+1 \in \alpha\}$. 
=-- 

+-- {: .num_defn #Neighbourhoods}
###### Definition
**(in-neighborhood, out-neighbourhood)**

Suppose $D=(V,A)$ is a digraph and $v\in V$. 
The *in-neighborhood* of $v$ in $D$, denoted $N^{\rightarrow}_D(v)$, is the set $\{ u\in V\colon (u,v)\in A\}$. The *out-neighborhood* of $v$ in $D$, denoted $N^{\leftarrow}_D(v)$, is the set $\{ u\in V\colon (v,u)\in A\}$.

=--

We note that the rationale for the slightly non-standard notation $N^{\leftarrow}_D(v)$ is to have it be intuitively understandable: the arrow points away from the vertex and points to the letter which stands for the set which contains the out-neighbours.


+-- {: .num_defn #Degrees}
###### Definition
**(in-degree, out-degree)**

Suppose $D=(V,A)$ is a digraph and $v\in V$. 
The *in-degree* of $v$ in $D$, denoted $d^{\rightarrow}_D(v)$, is the [[cardinality]] of the in-neighborhood of $v$ in $D$. The *out-degree* is defined analogously.


=--


+-- {: .num_defn #CategoryOfDigraphs}
###### Definition
**(category of digraphs, digraph morphism)**
The *category of digraphs*, denoted $\mathsf{Dgr}$, is the [[concrete category]] whose objects are the digraphs, and which, for arbitrary digraphs $D=(V,A)$ and $D'=(V',A')$ has hom-set $\mathsf{Dgr}(D,D')$ equal to the set of all set-maps $V\overset{f}{\rightarrow}V'$ such that for all $u,v\in V$, $(u,v)\in A$ implies $(f(u),f(v))\in A'$. 
The morphisms of $\mathsf{Dgr}$ are called *digraph-morphisms*. 

=--

Note that the category $\mathsf{Dgr}$ is equivalent to a full subcategory of [[Quiv]].



+-- {: .num_defn #Walk}
###### Definition
**(walk in a digraph)**
Suppose $D=(V,A)$ is a digraph. 
A *walk in $D$* is a *digraph-morphism into $D$ whose domain is an ordinal*. (Note that this is sensical since ordinals are digraphs, compare Example \ref{ExampleDigraph}).

=--


+-- {: .num_defn #WalkElementary}
###### Definition
**(walk in a digraph; elementary definition)**

Suppose $D=(V,A)$ is a digraph. 
A *walk* in $D$ consists of the data 

* a [[sequence]] $P\colon\alpha\rightarrow V$, with  $\alpha\in\omega+1$ (successor of the first [[limit ordinal]]), 

and the axiom

* for all $i\in\alpha$, if $i+1\in\alpha$, then $(P(i),P(i+1))\in A$.

If $\alpha=0$, then $P$ is called *the empty walk*. 
The phrase *$\alpha$-vertex path* means any *path whose domain is $\alpha$*.

=--

The axiom implies---digraphs being *irreflexive*--- that always $\neg \, (P(i)=P(i+1))$. Walks are only allowed to be non-injective *every other step*, so to speak. 

+-- {: .num_example #TheLeastInjectiveWalk} 
###### Example 
In a sense the *least injective* walk is obtained by considering any digraph containing a *2-cycle* (see below) $C$, taking $\alpha=\omega$ and defining $P$ to alternate back and forth on $C$ forever. 
This walk has a two-element image. 
=-- 


Definition \ref{WalkElementary} is evidently equivalent to def.  \ref{Walk}.
We note that $\omega+1=\omega\cup\{\omega\}$, and that $\alpha=0$ is permitted; then the axiom is vacuous (the hypothesis being always false), and $P$ then is the empty function (since $0$ is [[initial]] in [[Set]]) and hence the [[empty set]]. 
Note also that if e.g. $\alpha=\omega$, then the set of indices to which the axiom applies are precisely the finite ordinals. 


+-- {: .num_defn #StartAndEndVertices}
###### Definition
**(start vertex, $A$-$B$-walk in a digraph)**

Suppose $D=(V,A)$ is a digraph. 
Suppose $\alpha\overset{P}{\rightarrow} V$ is a non-empty walk in $D$. 
Then $P(0)$ is called the *start vertex* of $P$. 
Suppose that $A,B$ are [[subsets]] of $V$, not necessarily disjoint. 
Then $P$ is an $A$--$B$-path if and only if $\alpha\gt 0$ is a finite ordinal and $P(0)\in A$, $P(\alpha-1)\in B$ and $0\lt i\lt \alpha-1$ implies $\neg\, (P(i)\in A\cup B)$. 
If $A=\{a\}$ and $B=\{b\}$ are singletons, one also writes $a$--$b$-path for *$\{a\}$--$\{b\}$-path*. 



=--

+-- {: .num_defn #Trail}
###### Definition
**(trail in a digraph)**

Suppose $D=(V,A)$ is a digraph. 
A *trail* in $D$ is a walk $\alpha\overset{P}{\longrightarrow}V$ such that the [[function]] $\alpha\rightarrow A$ with $\alpha(i)=(P(i),P(i+1))$ is  injective.

=--

While having *walk* imply that all the arcs be *aligned* is very *common*, the following is a rather *un*common definition, which nevertheless has an important role in Power's [proof](#Power1990) of unique interpretability of [[pasting schemes]]: 

+-- {: .num_defn #WeakWalkElementary}
###### Definition
**(weak walk in a digraph)**
Read the (elementary) definition of *walk* with  "weak walk" instead of "walk" , and "then (  $(P(i),P(i+1))\in A$   [[or]]    $(P(i+1),P(i))$   )" instead of "then $(P(i),P(i+1))\in A$".

=--

Note that a *weak walk* validates the usual [[red herring principle]]: a red herring need not be a herring (yet may happen to, and a  wealk walk need not be walk (yet may happen to).

Evidently, *weak walks* in $D$ bijectively corresponds to (the weak walks obtained by reinstating the directections of) the walks in the undirected graph underlying $D$.

+-- {: .num_defn #WeakTrail}
###### Definition
**(trail in a digraph)**

Suppose $D=(V,A)$ is a digraph. 
A *weak trail* in $D$ is a weak walk $\alpha\overset{P}{\longrightarrow}V$ such that the [[function]] $\alpha\rightarrow A$ with $\alpha(i)=(P(i),P(i+1))$ is  injective.

=--


+-- {: .num_defn #Path}
###### Definition
**(path in a digraph)**

Suppose $D=(V,A)$ is a digraph. 
A *path* in $D$ is a trail $P$ in $D$ such that $P$ is [[injective]] as a [[function]]. 

=--

Note that the standard meaning of "path" in (di)graph theory is different to the standard topological meaning of [[path]]. 
In (di)graph theory, a path never has self-intersections, and hence is a (di)graph isomorphism onto its image, while in topology the term *path* signals that self-intersections *are* permitted. 
The standard term in topology for a path which is *free of self-intersections* is [[arc]] (eg [Kowalksky 1965](#Kowalksky65), Definition 29b). 
As a saving grace, the standard way to rigorously define the arcs of *plane* digraphs uses precisely the topological [[arcs]]. 


+-- {: .num_defn #Ray}
###### Definition
**(ray in a digraph)**

Suppose $D=(V,A)$ is a digraph. 
A *ray* in $D$ is a path $P$ in $D$ such that $\mathrm{dom}(P)=\omega$ is the first limit ordinal.

=--


+-- {: .num_example} 
###### Example 
Every ray is isomorphic in $\mathsf{Dgr}$ to the digraph $\omega$ from example \ref{ExampleDigraph}.

=--


+-- {: .num_defn #CycleInDigraph}
###### Definition
**(cycle in a digraph)**

Suppose $D=(V,A)$ is a digraph. 
A *cycle* in $D$ is a trail $\alpha\overset{P}{\rightarrow}V$ in $D$ such 

* $2 \lt \alpha \lt \omega$

* the [[restriction]] $P|_{\alpha-1}$ is an [[injective]] function

* $P(0)=P(\alpha-1)$

=--

Note that since $\alpha$ is required to be finite, $\alpha-1$ is defined. 
The image of any cycle is a [[finite set]] of vertices.

We remark (in passing, since there is no use for 2-cycles in the usual [[pasting schemes]]), that, despite its domain having precisely three elements, a cycle $P$ with $\mathrm{dom}(P)=3$ is traditionally called a *2-cycle*. 
The reason is that a 2-cycle "has" (to use a usual abuse of language) precisely two arcs. 
Allowing 2-cycles, yet neither loops nor parallel arcs, has become a  standard meaning of *digraph* in combinatorics.


+-- {: .num_defn #Acyclic}
###### Definition
**(acyclic digraph (DAG); classical definition)**

Suppose $D=(V,A)$ is a digraph. 
Then $D$ is called *acyclic* if and only if there does not exist any cycle in $D$. 

A usual abbreviation in combinatorics for *acyclic directed graph* is *DAG*.


=--

We note that "classical" in the above refers to the negative definition. 




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

A *plane digraph* consists of the data 

* a subset $V\subseteq\mathbb{R}^2$ of the [[plane]]
* a [[set]] $A$ of [[arcs]] (in the usual topological sense), each $a\in A$ of the form $[0,1]\overset{a}{\rightarrow}\mathbb{R}^2$

and the axioms

(v.connect) for each $a\in A$,  $a(0)\in V$ and $a(1)\in V$,

(free.interior) if $a\in A$ and $0\lt t\lt 1$, then $\neg\,(a(t)\in V)$,

(not.par) if $a,a'\in A$ and if $a(0) = a'(0)$ and $a(1) = a'(1)$, then $a=a'$,

(disjoint.interiors) if $a,a'\in A$ and ( $\exists t:[0,1]$, $0\lt t \lt 1$ and $\exists t':[0,1]$, $0 \lt t' \lt 1$ and $a(t)=a(t')$ ), then $a=a'$.

=--

Note that plane digraphs are often introduced into a context like (abstract) digraphs are, i.e. by writing $D=(V,A)$, although 

* the type of $D=(V,A)$ is invisible from this notation (it may be a *digraph* or a *plane digraph*)

* for a plane digraph $D=(V,A)$ we do not in general have $A\subseteq V\times V$. 

We make use of the treatment of *undirected* plane graphs given in ([Diestel](#DiestelGraphTheoryFourthEd), Chapter 4), with some adaptations made for the present purposes: 

* here, *arc* means arc in the usual topological sense, without exception, while, since the author focuses on undirected graphs, in [Diestel](#DiestelGraphTheoryFourthEd), "arc" is defined to be a [[subset]] of the  [[plane]], in particular is not parametrized, in particular does not carry *directional information* (compare   def. \ref{AbstractDigraphOfAPlaneDigraph} where said information is used).

* in ([Diestel](#DiestelGraphTheoryFourthEd), Chapter 4), both $V$ and $A$ in the definition of plane graphs are required to be [[finite sets]]. Here we make no such restriction (cf. \ref{ExamplePlaneDigraph}).

* for ease of reference, we calibrate the point-set topological terminology according to [[Introduction to Topology]] (example: we will say "component" instead of "region") when defining *faces*, and also [Munkres 2000](#Munkres2000).

+-- {: .num_example #ExamplePlaneDigraph} 
###### Example 
An example of a plane digraph with countably infinite vertex set, and whose satisfying the axioms of plane digraphs is evident, is given by $T:=\{\varphi\in\mathbb{R}\colon 0\le \varphi\lt 2\pi,\quad \varphi\in\mathbb{Q} \}$, $D=(V,A)$ with $V:=\{(0,0)\} \cup \{   (  \cos( \varphi )  , \sin( \varphi  ) ) \colon  \varphi\in M    \}$ and $a(\varphi)\colon [0,1]\rightarrow\mathbb{R}^2$ with $a(\varphi)(t) =   (  t\cdot\cos(\varphi), t\cdot \sin(\varphi)   )$ and $A:= \{  a(\varphi)\colon     \varphi\in M      \}$.
Note that this example (0) is not a [[pasting scheme|pasting scheme in the sense of Power]] (already for the strong reason that in it there does not exist any $\omega$-coking), and (1), while large, it would make for a rather dull and vacuously-uniquely-interpretable [[pasting diagram]] : there are no arrows that could possibly be composed, let alone is there any 2-cell.

In combinatorics, this is sometimes referred to as an *infinite star*.

=-- 


Applications of the following standard concept are e.g. the study of [[maps]] on [[surfaces]], and Power's ([proof](#Power1990)) of unique interpretability of [[pasting schemes]]:

+-- {: .num_defn #Face}
###### Definition
**(face of a plane digraph)**

Suppose $D=(V,A)$ is a plane digraph. 
The *set of faces of $D$*, denoted $\mathrm{Fa}(D)$, is the set of [[connected components]], in the sense of [Section 7](Introduction+to+Topology+--+1#subspaces), of the [[relative complement]] $\mathbb{R}^2\setminus\bigcup\{   \mathrm{im}(a) \colon a\in A        \}$, where $\mathrm{im}(a)=\{   a(t)\colon 0\leq t\leq 1    \}$.

A *face of $D$* is a *member of the set $\mathrm{Fa}(D)$*.
Each face of $D$ is an open connected subspace of the plane. 

=--

Of course one needs a map from *plane digraphs* to (abstract) *digraphs*:
+-- {: .num_defn #AbstractDigraphOfAPlaneDigraph}
###### Definition
**(the (abstract) digraph of a plane digraph)**

Suppose $D=(V,A)$ is a plane digraph. 

Then $\mathrm{Dig}(D)$ is the digraph defined as follows: it has vertex set $V$ and arc set $A' :=      \{    ( a(0)  ,   a(1) )  \colon    a\in A           \}$.

=--

Note that by axiom (v.connect), $A'$ is a subset of $V\times V$, and because each $a$ is an topological arc, and, as such, injective, $A'$ is moreover disjoint from the diagonal $\{(v,v)\colon v\in V\}$, so $A'$ has the type required by def.  \ref{Digraph}.


+-- {: .num_defn #DigraphTheoreticTermsForPlaneDigraph}
###### Definition
All digraph-theoretic technical terms like *out-neighborhood*, *outdegree* which are defined for *digraphs* are defined for *plane digraphs* $D$ by first applying the map $\mathrm{Dig}$ to $D$, then applying the digraph-theoretic definition, then applying the inverse of $\mathrm{Dig}$.

=--




A central technical tool in  ([Power's proof](#Power1990)) are *boundary walks*: 
boundary walks validate the [[red herring principle]] in the following way: each boundary walk is a *weak walk*, yet need not be a walk. 

The boundary walks one works with when using A.J. Power's [application](#Power1990) of plane digraphs to category theory, are often weak *trails*, "often" in the sense that most [[pasting diagrams]] one encounters in practice do not have any arc-repetitions, equivalently, the 1-cells of these diagrams have an underlying undirected graphs with is *bridgeless*. 
However, this is not generally true, and to have both *walks* and *trails* is not futile but necessary: a typical example of a pasting diagram occurring naturally in category theory are [[whiskering]] diagrams: for them, the *boundary trail* of the *exterior* face *does* have arc-repetions, hence is not a trail but only a walk.





## Remarks on the definitions

The *convention* to have digraph imply that there be no loops and no parallel arcs, and resort to other terms such as *directed pseudograph* to signal loops or parallel arcs, is widespread in modern combinatorics. 
For example, see p. 2 of ([Gutin and Bang-Jensen](#DG2nd)), and Section 1.2 of ([Csaba et al](#DecompositionProof)).



Unsurprisingly, while the convention that digraph implies that there be no parallel arrows has been widely adopted nowadays, there is a generous disregard for whether a digraph may contain loops. In this set-theoretical definition given above, this corresponds to the decision whether to allow $A$ to contain elements of the form $(v,v)$. 

The terms *walk*, *trail* and *path* are standard in modern combinatorics. They are in particular compatible with standard usage in the theory of *undirected* graphs, in that upon forgetting (so to speak) the directions in the various definitions, one obtains the standard notions of walk, trail and path in (undirected) graph theory (for example [Figure 1.8](#BondyMurtyFirstEdition) illustrates precisely this convention).


Many (e.g. [p. 11](#DG2nd) and [) modern reference define walks to be sequences whose codomain conains both vertices and arcs. 
For simplicity we do not do so. 
Having paths consist of vertices only, and letting the structure of the target space determine the axioms seems cleaner. 
We can afford to make this simplification *only* because digraphs cannot have any parallel arcs: for digraphs, our definition and the vertex-arc-alternating definition of [p. 11](#DG2nd) are equivalent to all intents and purposes.
There is, however a good reason why e.g. [Bondy and Murty](#BondyMurtyFirstEdition)   use the latter definition: for them, a *directed graph* [10.1](#BondyMurtyFirstEdition) is not a *digraph* but a [[quiver]], and---evidently---if multiple parallel arcs are permitted, *then a vertex-sequence does not contain enough information to define a "walk"*. 
Upon stepping from one vertex to the next, a vertex sequence by itself cannot tell one which parallel arc to pick.



Needless to say (since given by the definitions), *in a trail, arc-repetitions are forbidden*, and in a path, any repetition is forbidden.

The perhaps oddly hybrid concept of *trail* has a crucial role in A. J. Power's ([proof](#Power1990)) of unique interpretability of [[pasting schemes]]: any *face* of a *plane digraph* determines a *boundary trail* which always is a *weak trail*. 


 Generically, such a *boundary trail* has many vertex-repetitions, but it never has any arc-repetition. 

The terminology "king" above is standard in modern digraph theory; the term "coking" is not, but in tune with category-theoretic usages. The term "$\omega$-king" appears not to be attested but is in tune with a standard notion of $d$-king in digraph-theory, and also with some usages in mathematics which let $\omega$ signal that some parameter is unconstrained (cf. [[omega-category]] [[omega-groupoid]]).

The choice of definitions documented here is biased towards (one of) the *uses* digraphs are put to in category theory, in particular in giving a rigorous justification of [[pasting diagrams]]. 
The most salient example of this is the emphasis given to *plane digraphs* in this article. 

A reason for treating the concept of $\omega$-kings here is A. J. Power's proof ([Power 1990](#Power1990)) of a *pasting theorem*, a rigorous justification of the notational practice of [[pasting diagrams]]: therein, both $\omega$-kings and $\omega$-cokings play an important role (Power calls $\omega$-kings "sources" and $\omega$-cokings "sinks"; both these terms clash with two standard technical terms in, respectively, contemporary digraph theory and flow theory, which is why the alternative terms were chosen).

Moreover, Power makes crucial use of a concept of *addition of $a$--$b$-paths*, which is one of the reasons why $A$--$B$-paths have been  introduced.


## Uses of digraphs in category theory 

One example of why digraphs are relevant to category theory are [[pasting schemes]], which are a rigorous justification of the (older) notational practice of [[pasting diagrams]]. 
Pasting diagrams are fundamental to [[higher category theory]]: already the axioms for various notions of higher categories are formalized in terms of pasting diagrams. 
The formal justification of pasting diagrams was achieved in the late 1980. 
Note that there are more than one definition of [[pasting scheme]] in the literature. 
E.g. there are M. Johnson's pasting schemes (([Johnson 1987](#Johnson1987), Chapter 2), ([Johnson 1989](#Johnson1989), Section 2)) and Power's pasting schemes ([Power 1990](#Power1990)). 
The definition which is strictly relevant to the present article is Power's. He defines defines pasting schemes as a special kind of digraph ([Power 1990](#Power1990), Section 3), details will be found at [[pasting scheme]].




## Related concepts

* [[geometric shape for higher structures]]

## References


* A. Bondy, U.S.R. Murty: Graph Theory with Applications. Fifth Printing. North Holland 1982.
{#BondyMurtyFirstEdition}


* B. Csaba, D. K&#252;hn, A. Lo, D. Osthus, A. Treglown: Proof of the 1-factorization and Hamilton decomposition conjectures. Memoirs of the American Mathematical Society, 244 (2016), monograph 1154, 170 pages
{#DecompositionProof}


* {#DiestelGraphTheoryFourthEd} R. Diestel, Graph Theory, 4. ed., Springer 2010

* [[Gregory Gutin]], [[Jørgen Bang-Jensen]]: _Digraphs: Theory, Algorithms and Applications_. Springer Monographs in Mathematics. Second Edition (2009)
{#DG2nd}

* [[Michael Johnson]]: _Pasting Diagrams in $n$-Categories with Applications to Coherence Theorems and Categories of Paths_, Doctoral Thesis, University of Sydney, 1987
{#Johnson1987}

* [[Michael Johnson]]: _The Combinatorics of $n$-Categorical Pasting_, Journal of Pure and Applied Algebra 62 (1989) 
{#Johnson1989}


* [[James R. Munkres]]: _Topology_, Prentice Hall. Second Edition (2000) 
{#Munkres2000}


* [[John Power]]: _A 2-Categorical Pasting Theorem_, Journal of Algebra 129 (1990) 
{#Power1990} 

* {#Kowalksky65} H. J. Kowalksky: Topological Spaces. Academic Press. 1965.

[[!redirects digraph]]
[[!redirects digraphs]]

