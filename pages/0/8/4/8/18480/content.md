
{:principle: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em
;"}


***

This page is about the concept of [[directed graphs]] that is usual in combinatorics. For the notion of directed graph as commonly understood in category theory, see [[quiver]]. For some commentary on how the two formalizations relate to one another, see [[directed graph]].


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

In combinatorics, a **digraph** (a shortening of *[[directed graph]]*)  consists of a [[set]] and a [[binary relation]] on that set that is [[irreflexive relation|irreflexive]]. The elements of the set are called *nodes* or *vertices*, and elements of the relation are called *edges* or *arcs*; the idea is that whenever an ordered pair $(x, y)$ belongs to the relation, then we depict it as an arrow or directed edge going from node $x$ to node $y$. 
The irreflexivity condition means there is never an edge from a node to itself. 

## Definition and basic notions  

In this section we collect some definitions that are fundamental to digraph theory, but presented largely from the point of view of category theory. 

+-- {: .num_defn #Digraph}
###### Definition
**(digraph)**

A *digraph* is a [[pair]] $(V,A)$ of [[sets]], with $A\subseteq (V\times V)\setminus\{ (v,v)\colon v\in V\}$.
Here, $V\times V$ denotes the [[product]], and ${}\setminus{}$ the [[relative complement]] in the [[category of sets]].
The elements of $V$ are called [[vertices]], the elements of $A$ are called [[arcs]]. For $a = (v, w)$ an arc, we call $v$ the *source* of $a$ and $w$ the *target* of $a$, also denoted $s(a)$ and $t(a)$ respectively. 

A *morphism* from a digraph $(V, A)$ to a digraph $(V', A')$ is a function $f: V \to V'$ such that $(f(v), f(w)) \in A'$ whenever $(v, w) \in A$. Digraphs and their morphisms form a [[category]] denoted $\mathsf{Dgr}$. 

=-- 

A digraph $(V, A)$ may be regarded as a [[quiver]] in an evident way, with source and target functions $s, t: A \rightrightarrows V$. It is straightforward that $\mathsf{Dgr}$ is (equivalent to) a [[full subcategory]] of the category of quivers [[Quiv]]. Of course most quivers are not digraphs since quivers can have parallel edges: distinct edges $a, b$ where $s(a) = s(b)$ and $t(a) = t(b)$. 

Some useful examples of digraphs are based on [[ordinals]]: 

+-- {: .num_example #ExampleDigraph} 
###### Example 
If $\alpha$ is an ordinal, we may form a digraph $(V, A)$ where $V$ is the underlying set of $\alpha$ and $A$ is the relation $\{(i, i+1): i, i+1 \in \alpha\}$. We call this an *ordinal digraph* and denote it by the ordinal itself. 
=-- 

+-- {: .num_defn #Walk}
###### Definition

**(walk in a digraph)**
Suppose $D=(V,A)$ is a digraph. 
A *walk in $D$* is a digraph-morphism $\alpha \to D$ where $\alpha$ is an ordinal digraph. 

=-- 

Notice that for $\alpha = 1$, the hom-set $\mathsf{Dgr}(1, D)$ may be identified with the set of vertices of $D$. The definition of graph morphism implies that the underlying set functor $U = \mathsf{Dgr}(1, -): \mathsf{Dgr} \to Set$ is [[faithful functor|faithful]], and realizes $\mathsf{Dgr}$ as a [[concrete category]]. 

For $\alpha = 2$, the hom-set $\mathsf{Dgr}(2, D)$ may be identified with the set of arcs of $D$. However, the arc-set functor $\mathsf{Dgr}(2, -): \mathsf{Dgr} \to Set$ is very far from being faithful. 

If we let $C$ denote the full subcategory of $\mathsf{Dgr}$ consisting of the ordinal digraphs $1, 2$, then the inclusion $i: C \hookrightarrow \mathsf{Dgr}$ induces a functor $\mathsf{Dgr} \to Set^{C^{op}} = Quiv$ according to the usual "[[nerve]]" construction 

$$\mathsf{Dgr} \to Set^{C^{op}}$$ 

$$D \mapsto (c \mapsto \mathsf{Dgr}(i c, D))$$ 

and this nerve functor is exactly the full embedding $\mathsf{Dgr} \to Quiv$. Since full embeddings reflect and preserve isomorphisms, a digraph morphism $f: D \to D'$ is an isomorphism iff the vertex-function $\mathsf{Dgr}(1, f)$ and arc-function $\mathsf{Dgr}(2, f)$ are isomorphisms (which is in any case obvious from the definition of digraph morphism, but this underscores the general importance of walks). 

Generally we will only be interested in walks $\alpha \to D$ such that $\alpha \leq \omega$ in the sense of ordinals; here $\omega$ is of course the first infinite ordinal. Unwinding the definitions, here is an elementary description of such walks: 

+-- {: .num_defn #WalkElementary}
###### Definition
**(walk in a digraph; elementary definition)**

Suppose $D=(V,A)$ is a digraph. 
A *walk* in $D$ consists of 

* a [[sequence]] $P\colon\alpha\rightarrow V$, with  $\alpha\leq\omega$, 

such that

* for all $i\in\alpha$, if $i+1\in\alpha$, then $(P(i),P(i+1))\in A$.

The phrase *$\alpha$-vertex path* means any *path whose domain is $\alpha$*.

=-- 

Some special cases: If $\alpha=0$, then $P$ is called *the empty walk*. We have already seen that a $1$-walk is tantamount to a vertex, and that a 2-walk is tantamount to an edge. We call a walk $\omega \to D$ a *ray* in $D$. 

+-- {: .num_example #cycle} 
###### Example 
Another useful example of a digraph is a finite [[cyclic order]]. For each $n \geq 2$, there is a digraph $Z_n$ whose vertex set is the underlying set of the finite cyclic group $\mathbb{Z}/n$, and whose arc relation is the set $\{(i, i+1): i \in \mathbb{Z}/n\}$. 
=--

 
## Categorical properties of $\mathsf{Dgr}$ 

The category $\mathsf{Dgr}$ is not especially well-behaved for a category theorist. For example, it doesn't have a terminal object (no, the ordinal digraph $1$ is not terminal), and it does not admit all coequalizers. In both cases the culprit is the irreflexivity condition. 

It does however have products indexed over nonempty sets, and equalizers. These limits are computed as they are in [[Quiv]], e.g., the quiver product of two digraphs is again a digraph and is their product in $\mathsf{Dgr}$. Such limits are easy to compute because $Quiv$, being a presheaf topos $Set^{C^{op}}$, has limits (and colimits) that are computed pointwise/objectwise. 

It follows from these observations that $\mathsf{Dgr}$ has pullbacks which are simply $Quiv$-pullbacks; they are computed objectwise at the objects $c = 1, 2$, i.e., one simply takes pullbacks in $Set$ at each of the vertex and edge levels. 



In our development, it will be useful to characterize various classes of [[monomorphisms]] in $\mathsf{Dgr}$. We begin with plain monomorphisms. 

+-- {: .num_prop #Mono} 
###### Proposition 
A morphism of digraphs $f: D \to D'$ is monic iff its underlying function $U(f)$ is monic ([[injective function|injective]]). 
=-- 

+-- {: .proof} 
###### Proof 
It is well-known that faithful functors $U$ reflect monomorphisms and epimorphisms. For suppose $U(f)$ is monic. Given a diagram in $\mathsf{Dgr}$ of the form 

$$C \underoverset{h}{g}{\rightrightarrows} D \stackrel{f}{\to} D'$$ 

if we have $f \circ g = f \circ h$ then $U(f) \circ U(g) = U(f) \circ U(h)$, whence $U(g) = U(h)$ by monicity of $U(f)$. Since $U$ is faithful, it follows that $g = h$; therefore $f$ is monic. The argument for epimorphisms is dual. 

For the other direction, use the fact that $U = \mathsf{Dgr}(1, -)$ is representable. It follows immediately from the definition of monomorphism that representable functors preserve monomorphisms, so if $f$ is monic, then so is $U(f)$. 
=-- 

(Still to come: characterization of regular monomorphisms.) 

## Paths, trails, and cycles 

+-- {: .num_defn #Path}
###### Definition
**(path in a digraph)**

Suppose $D=(V,A)$ is a digraph. 
A *path* in $D$ is a walk $P: \alpha \to D$ whose underlying function is [[injection|injective]]. 

=--

Or what is the same, that $\mathsf{Dgr}(1, P)$ is a [[monomorphism]] in $Set$. In view of Proposition \ref{Mono}, we may also define a path to be a monic walk. (Notice this digraph concept of path is at variance with the concept of [[path]] in topology which is simply a continuous map $[0, 1] \to X$ into a [[topological space]], where there is no assumption that its underlying function is injective.)

+-- {: .num_defn #Trail}
###### Definition
**(trail in a digraph)**
Suppose $D=(V,A)$ is a digraph. 
A *trail* in $D$ is a walk $\alpha\overset{P}{\longrightarrow}V$ such that the [[partial function]] $e_P: \alpha\rightarrow A$ with $e_P(i)=(P(i),P(i+1))$ is injective.

=--

The domain of $e_P$ is canonically identified with the arc set of $\alpha$, and the trail condition is equivalent to saying that $\mathsf{Dgr}(2, P)$ (which we again denote as $e_P$), as a function between edge sets $\mathsf{Dgr}(2, \alpha) \to \mathsf{Dgr}(2, D)$, is a monomorphism in $Set$. 

We have the following easy result. 

+-- {: .num_prop #PathsAreTrails} 
###### Proposition 
In a digraph $D$, every path is a trail. 
=-- 

+-- {: .proof} 
###### Proof 
Since we just observed that a path $P$ is the same as a monic walk, and since representable functors like $\mathsf{Dgr}(2, -)$ preserve monomorphisms, it follows that $e_P = \mathsf{Dgr}(2, P)$ is a monomorphism. 
=-- 

Continuing the theme of monic digraph morphisms, we introduce the notion of cycle: 

+-- {: .num_defn} 
###### Definition 
An $n$-*cycle* in a digraph $D$ is a monic morphism $P: Z_n \to D$ (see Example \ref{cycle}). A *cycle* in $D$ is just an $n$-cycle in $D$ for some $n$. A digraph $D$ is *acyclic* if it admits no cycles. 
=-- 

There is a natural bijection between digraph morphisms $C: Z_n \to D$ and walks $P: \{0, \ldots, n\} \to D$ such that $P(0) = P(n)$. Indeed we have a digraph quotient map $q: \{0, \ldots, n\} \to Z_n$ defined as the mapping $i \mapsto i \mod n$, and the walk associated with $C: Z_n \to D$ is $P = C \circ q$. The map $q$ induces a bijection on arcs: 

$$\mathsf{Dgr}(2, q): \mathsf{Dgr}(2, \{0, \ldots, n\}) \stackrel{\sim}{\to} \mathsf{Dgr}(2, Z_n).$$ 

Thus if $C: Z_n \to D$ is *monic*, we have a composite injective map in $Set$, 

$$\mathsf{Dgr}(2, \{0, \ldots, n\}) \underoverset{\mathsf{Dgr}(2, q)}{\sim}{\to} \mathsf{Dgr}(2, Z_n) \underset{\mathsf{Dgr}(2, C)}{\to} \mathsf{Dgr}(2, D),$$ 

which implies that the walk $P$ associated with a cycle $C: Z_n \to D$ is a trail. 


## Symmetrizing and "weak" notions 

For various digraph (directed graph) notions above, it can be useful to consider parallel notions for *undirected* graphs. A slick method for doing this is by invoking a "symmetrizing" [[functor]] construction. 

+-- {: .num_defn} 
###### Definition 
For a digraph $D$, we define $Symm(D)$ to have the same vertices as $D$, and the arc relation to be the symmetric closure of the arc relation of $D$. In other words, $(v, w)$ is an arc of $Symm(D)$ iff $(v, w)$ or $(w, v)$ is an arc of $D$. 
=-- 

Clearly the symmetric closure of an irreflexive relation remains irreflexive, so $Symm(D)$ is again a digraph, and the assignment $D \mapsto Symm(D)$ is the object part of an obvious functor $Symm: \mathsf{Dgr} \to \mathsf{Dgr}$. Also the monomorphism $D \to Symm(D)$ that is the identity on vertices is the component $u_D$ of a [[natural transformation]] 

$$u: 1_\mathsf{Dgr} \to Symm.$$ 

+-- {: .num_theorem} 
###### Theorem 
The functor $Symm$ carries an [[idempotent monad]] structure. 
=-- 

+-- {: .proof} 
###### Proof 
It is clear that $u_{Symm(D)}: Symm(D) \to Symm^2(D)$ is an [[isomorphism]] (and even an identity map) because the operation of taking the symmetric closure of a relation is itself idempotent. Similarly $Symm(u_D)$ is also an identity map: $u_{Symm(D)} = Symm(u_D)$. The multiplication $m: Symm^2 \to Symm$ of the monad is defined by taking the inverse: $m = u_{Symm}^{-1}$. Then $m$ is natural and the unit law $m \circ u_{Symm} = 1$ is automatic; the other unit law $m \circ Symm(u_D)$ follows. The associativity of $m$ follows by inverting a naturality square for $u$. 
=-- 

Morally we may consider the category of undirected graphs to be the category of algebras over the monad $Symm$. In any case, this is a full subcategory of $\mathsf{Dgr}$ consisting of digraphs of the form $Symm(D)$. 

We proceed to "weaken" various of the notions above to take into account the undirected graph context, simply by applying the functor $Symm$. For example: 

* If $\alpha$ is an ordinal digraph, a *weak walk* $\alpha \to D$ is defined to be a walk $\alpha \to Symm(D)$. 

(Obviously, a weak walk $\alpha \to D$ need not be literally a walk $\alpha \to D$; cf. [[red herring principle]].)  

Alternatively, we could define a weak walk to be a digraph morphism $Symm(\alpha) \to Symm(D)$ where $\alpha$ is an ordinal digraph: the two ways of defining weak walks are (naturally) equivalent. 

Similarly, 

* A *weak trail* $\alpha \to D$ is defined to be a trail $\alpha \to Symm(D)$. 

* A *weak cycle* $Z_n \to D$ is defined to be a cycle $Z_n \to Symm(D)$. 






## Miscellaneous notions 

In [contemporary](#MO277288) mathematics, ordered pairs $(x,y)$, $(y,x)$ are called *antiparallel arcs*.

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







The axiom implies---digraphs being *irreflexive*--- that always $\neg \, (P(i)=P(i+1))$. Walks are only allowed to be non-injective *every other step*, so to speak. 

+-- {: .num_example #TheLeastInjectiveWalk} 
###### Example 
In a sense the *least injective* walk is obtained by considering any digraph containing a *2-cycle* (see below) $C$, taking $\alpha=\omega$ and defining $P$ to alternate back and forth on $C$ forever. 
This walk has a two-element image. 
=-- 



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


Discussion of weak trails from a previous revision mentioned Power's [proof](#Power1990) of unique interpretability of [[pasting schemes]]. 








The standard term in topology for a path which is *free of self-intersections* is [[arc]] (eg [Kowalksky 1965](#Kowalksky65), Definition 29b). 
As a saving grace, the standard way to rigorously define the arcs of *plane* digraphs uses precisely the topological [[arcs]]. 





Allowing 2-cycles, yet neither loops nor parallel arcs, has become a  standard meaning of *digraph* in combinatorics.


+-- {: .num_defn #Acyclic}
###### Definition
**(acyclic digraph (DAG); classical definition)**

Suppose $D=(V,A)$ is a digraph. 
Then $D$ is called *acyclic* if and only if there does not exist any cycle in $D$. 

A usual abbreviation in combinatorics for *acyclic directed graph* is *DAG*.


=--

Here, "classical" refers to the negative definition. 



The set of all weak cycles of a digraph $D$ is denoted $\mathrm{WeCy}(D)$.


The following non-standard definition is useful in when constructing proofs of Power's pasting theorem:


+-- {: .num_defn #ConstructiveAcyclic}
###### Definition
**(constructive acyclic digraph (cDAG))**

A *constructive acyclic digraph* is a triple $D=(V,A,z)$ of data 

* a digraph $(V,A)$ 
* a function $z\colon\mathrm{WeCy}(D)\rightarrow V$

subject to the axioms

* for each $P\in \mathrm{WeCy}(D)$, $z(P) \in \mathrm{image}(P)$

* for each $P\in \mathrm{WeCy}(D)$, if (        $u\in \mathrm{image}(P)$ [[and]] (  $(u,z(P))\in A$ [[or]] $(z(P),u)\in A$  ) ) , then $(u,z(P))\in A$.

=--

In words, the axioms mean that $z$ gives us one vertex on any given weak cycle $P$ whose out-degree *on $P$* is two.
Then $z(P)$ witnesses $P$'s not being a cycle. 
Evidently, a (classical) DAG can usually be *made* a cDAG in many ways: there usually are many functions $z$ one can specify and that satisfy the axioms. 
We are here not interested in describing or counting these possibilities, rather in doing things with a given cDAG.

There is an apparently inescapable arbitrariness in whether to favor out-neighbors or in-neighbor when defining *constructive DAG*. 
The above definition would to all intents and purposes be equivalent the one obtained by replacing the conclusion in the axiom with "then $(z(P),u)\in A$".


The following concept appears (under another name) in [Power's proof](#Power1990):

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
By definition, for each $k\in\omega$, each $k$-(co)king is an $\omega$-(co)king. 
Of course, a vertex can be a king and a coking simultaneously. (Which is why e.g. in [Power's proof](#Power1990), non-equality of the king and the coking *must be made a separate axiom* in the definition of what Power calls *plane graph with source and sink*).

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

(disjoint.interiors) if $a,a'\in A$ and ( $\exists t:[0,1]$, $0\lt t \lt 1$ and $\exists t':[0,1]$, $0 \lt t' \lt 1$ and $a(t)=a'(t')$ ), then $a=a'$.

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
Note that this example (0) is not a [[pasting scheme|pasting scheme in the sense of Power]] (already for the strong reason that in it there does not exist any $\omega$-coking), and (1), while large, it would make for a rather dull and vacuously-uniquely-interpretable [[pasting diagram]]: there are no arrows that could possibly be composed, let alone is there any 2-cell.

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
Then $\mathrm{Dig}(D)=(V',A')$ is the digraph defined as follows: it has vertex set $V':=V$ and arc set $A' :=      \{    ( a(0)  ,   a(1) )  \colon    a\in A           \}$.

=--

Note that by axiom (v.connect), $A'$ is a subset of $V\times V$, and because each $a$ is an topological arc, and, as such, injective, $A'$ is moreover disjoint from the diagonal $\{(v,v)\colon v\in V\}$, so $A'$ has the type required by def.  \ref{Digraph}.


+-- {: .num_defn #DigraphTheoreticTermsForPlaneDigraph}
###### Definition
All digraph-theoretic technical terms like *out-neighborhood*, *outdegree* which are defined for *digraphs* are defined for *plane digraphs* $D$ by first applying the map $\mathrm{Dig}$ to $D$, then applying the digraph-theoretic definition, then applying the inverse of $\mathrm{Dig}$.

=--




A central technical tool in  [Power's proof](#Power1990) are *boundary walks*: 
boundary walks validate a form of the [[red herring principle]]: each boundary walk is a *weak walk*, yet need not be a walk. 


The boundary walks one works with when using A.J. Power's [application](#Power1990) of plane digraphs to category theory are often weak *trails*, "often" in the sense that most [[pasting diagrams]] one encounters in practice do not have any arc-repetitions.
Equivalently, the 1-cells of usual pasting diagrams have an underlying undirected graphs with is *bridgeless*. 
However, this is not generally true, and to have both *walks* and *trails* is not futile but necessary: a typical example of a pasting diagram occurring naturally in category theory are [[whiskering]] diagrams: the *boundary trail* of the *exterior* face of the typical whiskering diagram *does* have arc-repetions, hence is not a trail but only a walk.





## Remarks on the definitions

The *convention* to have digraph imply that there be no loops and no parallel arcs, and resort to other terms such as *directed pseudograph* to signal loops or parallel arcs, is widespread in modern combinatorics. 
For example, see p. 2 of ([Gutin and Bang-Jensen](#DG2nd)), and Section 1.2 of ([Csaba et al](#DecompositionProof)).



Unsurprisingly, while the convention that digraph implies that there be no parallel arrows has been widely adopted nowadays, there is a generous disregard for whether a digraph may contain loops. In this set-theoretical definition given above, this corresponds to the decision whether to allow $A$ to contain elements of the form $(v,v)$. 

The terms *walk*, *trail* and *path* are standard in modern combinatorics. They are in particular compatible with standard usage in the theory of *undirected* graphs, in that upon forgetting (so to speak) the directions in the various definitions, one obtains the standard notions of walk, trail and path in (undirected) graph theory (for example [Figure 1.8](#BondyMurtyFirstEdition) illustrates precisely this convention).


Many (e.g. [p. 11](#DG2nd) and [Chapter 1](#BondyMurtyFirstEdition)) modern reference define walks to be sequences whose codomain conains both vertices and arcs. 
For simplicity we do not do so. 
Having paths consist of vertices only, and letting the structure of the target space determine the axioms seems cleaner. 
We can afford to make this simplification *only* because digraphs cannot have any parallel arcs: for digraphs, our definition and the vertex-arc-alternating definition of [p. 11](#DG2nd) are equivalent to all intents and purposes.
There is, however a good reason why e.g. [Bondy and Murty](#BondyMurtyFirstEdition) use the latter definition: for them, a *directed graph* is (cf. [10.1](#BondyMurtyFirstEdition), though Bondy--Murty's formalization is different from usual [[quivers]] and a rare hybrid between purely functional and purely relation-theoretic formalizations: they use maps with codomain set $V\times V$) not a *digraph* but a [[quiver]], and---evidently---if multiple parallel arcs are permitted, *then a vertex-sequence does not contain enough information to define a "walk"*. 
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

* Manfred Weis (https://mathoverflow.net/users/31310/manfred-weis), Calculating Cost-Optimal 1-Factors in Digraphs, URL (version: 2017-07-26): https://mathoverflow.net/q/277288
{#MO277288}

* [[James Munkres]]: _Topology_, Prentice Hall. Second Edition (2000) 
{#Munkres2000}


* [[John Power]]: _A 2-Categorical Pasting Theorem_, Journal of Algebra 129 (1990) 
{#Power1990} 

* {#Kowalksky65} H. J. Kowalksky: Topological Spaces. Academic Press. 1965.

[[!redirects digraphs]]

