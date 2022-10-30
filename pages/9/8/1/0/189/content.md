+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

A quiver is a collection of edges which may stretch between (ordered) pairs of "points", called _vertices_.

A quiver is like a [[category]] with units and composition forgotten. Indeed, a [[category]] is a quiver with extra structure.  To formalize this idea, we say there is a [[forgetful functor]] 

$$U\colon Cat \to Quiv$$

where [[Quiv]] is the category of quivers and [[Cat]] is the category of ([[small category|small]] [[strict category|strict]]) categories.  Moreover, this forgetful functor has a [[left adjoint]] 

$$F\colon Quiv \to Cat $$

sending each quiver to the [[free category]] on that quiver.

A quiver is a kind of [[graph]] and is often called a [[directed graph]] (or [[digraph]]) by category theorists.  However, in the context of graph theory, the term "directed graph" is often taken to mean that there is at most one edge from one vertex to another. See [[directed graph]].


## Definitions

### Slick definition

The **[[walking structure|walking]] quiver**[^1] $X$ is the [[category]] with

* one [[object]] $X_0$, called the object of _vertices_;

* one object $X_1$, called the object of _edges_;

* two [[morphisms]] $s, t\colon X_1 \to X_0$, called
the _source_ and _target_;

* together with [[identity morphisms]].

A **quiver** is a [[functor]] $G\colon X \to$ [[Set]].

More generally, a **quiver [[internalization|in]] a category $C$** is a [[functor]] $G\colon X \to C$.

The category of quivers in $C$, [[Quiv]]$(C)$, is the [[functor category]] $C^{X}$, where:

* objects are functors $G\colon X \to C$,

* morphisms are [[natural transformation|natural transformations]] between such functors.

In the basic case where $C$ is [[Set]], the category Quiv(Set) is equivalent to the category of [[presheaves]] on $X^{op}$.  So: the category of quivers, [[Quiv]], is the category of presheaves on the category $X^{op}$.


[^1]: Also called "the elementary "parallel process" " by [[William Lawvere|Lawvere]] in [p. 272](#GeneralizedGraphs), "a category that has no compositions in it" and "the graph that is also a category, automatically" again by  [[William Lawvere|Lawvere]], this time in his lecture at [[Como]].

### Nuts-and-bolts definitions 

A __quiver__ $G$ consists of two sets $E$ (the set of _edges_ of $G$), $V$ (the set of _vertices_ of $G$) and two functions 

$$s, t\colon E \rightrightarrows V$$ 

(the source and target functions). More generally, a __quiver internal to a category__ (more simply, *in* a category) $C$ consists of two objects $E$, $V$ and two morphisms $s, t\colon E \rightrightarrows V$. 

If $G = (E, V, s, t)$ and $G' = (E', V', s', t')$ are two quivers in a category $C$, a __morphism__ $g\colon G \to G'$ is a pair of morphisms $g_0\colon V \to V'$, $g_1\colon E \to E'$ such that $s' \circ g_1 = g_0 \circ s$ and $t' \circ g_1 = g_0 \circ t$.

In [[graph theory]], a quiver is often (cf. [p. 4](#DG2nd) or [Figure 2-2](#White84)) called a __directed pseudograph__ (or some variation on that theme), but category theorists often just call them __directed graphs__.


## Remarks

Let $G_0 = G(X_0)$ and $G_1 = G(X_1)$.

* A quiver in $C$ is a [[presheaf]] on $X^{op}$ with values in $C$.

* A quiver is a [[globular set]] which is concentrated in the first two degrees.

* A quiver can have distinct edges $e,e'\in G_1$ such that $s(e) = s(e')$ and $t(e) = t(e')$. A quiver can also have loops, namely, edges with $s(e) = t(e)$.

* A quiver is **[[complete graph|complete]]** if for any pair of vertices $v,v'\in G_0$, there exists a unique directed edge $e\in G_1$ with $s(e) = v, t(e) = v'$.


## Terminology

Saying _quiver_ instead of _directed (multi)graph_ indicates focus on a certain set of operation intended on that graph. Notably there is the notion of a [[quiver representation]].

Now, one sees that a _representation_ of a graph $G$ in the sense of quiver representation is nothing but a [[functor]] $\rho\colon Q := F(G) \to Vect$ from the _free category_ $F(G)$ on the quiver $G$:

Given a graph $G$ with collection of vertices $G_0$ and collection of edges $G_1$, there is the free category $F(G)$ on the graph whose collection of objects coincides with the collection of vertices, and whose collection of morphisms consists of finite [[sequence]]s of edges in $G$ that fit together head-to-tail (also known as _[[path]]s_). The composition operation in this free category is the concatenation of sequences of edges.

Here we are taking advantage of the [[adjoint functor|adjunction]] between [[Cat]] (the category of small categories) and [[Quiv]] (the category of directed graphs).  Namely, any category has an underlying directed graph:

$$U\colon Cat \to Quiv$$

and the left adjoint of this functor gives the free category on a directed graph:

$$F\colon Quiv\to Cat $$

Since this is the central operation on quivers that justifies their distinction from the plain concept of directed graph, we may adopt here the point of view that _quiver_ is synonymous with _free category_.

So a [[representation]] of a quiver $Q = F(G)$ is a functor

$$R\colon Q \to Vect $$

Concretely, such a thing assigns a vector space to each vertex of the graph $G$, and a linear operator to each edge.  Representations of quivers are fascinating things, with connections to ADE theory, quantum groups, string theory, and more.


## Properties

### Relation to free categories

It may be handy to *identify* a quiver with its free category.  This can be justified in the sense that the functor $F\colon Quiv \to Cat$ is an embedding ($k$-[[k-surjectivity|surjective]] for all $k \gt 0$) on the [[cores]].  In other words, [[isomorphisms]] between quivers may be identified with [[equivalence of categories|equivalences]] between free categories with no ambiguity.

However, at the level of noninvertible morphisms, this doesn\'t work; while $U$ is [[faithful functor|faithful]], it is *not* [[full functor|full]].  In other words, there are many [[functors]] between free categories that are not morphisms of quivers.

Nevertheless, if we fix a quiver $G$ and a category $D$, then a [[quiver representation|representation]] of $G$ in $D$ is precisely a functor from $F(G)$ to $D$ (or equivalently a quiver morphism from $G$ to $U(D)$), and we may well want to think of this as being a morphism (a [[heteromorphism]]) from $G$ to $D$.  As long as $D$ is not itself a free category, this is unlikely to cause confusion.


### Relation to representation theory of algebras

For $Q$ a quiver, write $k Q$ for the _path algebra_ of $Q$
over a ground field $k$.  That is, $k Q$ is an algebra with $k$-basis given by finite composable sequences of arrows in $Q$, including a "lazy path" of
length zero at each vertex. The product of two paths composable paths is their composite, and the product of non-composable paths is zero. 

A module over $k Q$ is the same thing as a representation of $Q$, so the theory of representations of quivers can be viewed within the broader context of representation theory of (associative) algebras.  

If $Q$ is acyclic, then $k Q$ is finite-dimensional as a vector space, so in studying representations of $Q$, we are really studying representations of a finite dimensional algebra, for which  many interesting tools exist 
(Auslander-Reiten theory, tilting, etc.).

### Classification 
 {#Classification}

[[Gabriel's theorem]] says that connected quivers of finite type are precisely those whose underlying [[undirected graph]] is a [[Dynkin diagram]] in the ADE series, and that the indecomposable [[quiver representations]] are in [[bijection]] with the positive roots in the [[root system]] of the Dynkin diagram. ([Gabriel 72](#Gabriel72)).

## Related concepts

* [[quiver gauge theory]]

## References

Some general-purpose references include

* Harm Derksen, Jerzy Weyman, [Quiver representations](http://www.ams.org/notices/200502/fea-weyman.pdf) _AMS Notices_, 2005.

* William Crawley-Boevy, _Lectures on quiver representations_ ([pdf](http://www.amsta.leeds.ac.uk/~pmtwc/quivlecs.pdf)).
 
* Alistair Savage, _Finite-dimensional algebras and quivers_ ([arXiv:math/0505082](http://www.arxiv.org/abs/math/0505082)), _Encyclopedia of Mathematical Physics_, eds. J.-P. Fran&#231;oise, G.L. Naber and Tsou S.T., Oxford, Elsevier, 2006, volume 2, pp. 313-320.

Classification results for quivers appeared in 

* [[Peter Gabriel]], _Unzerlegbare Darstellungen. I_, Manuscripta Mathematica 6: 71&#8211;103, (1972) [MR332887](http://www.ams.org/mathscinet-getitem?mr=332887) [doi](http://dx.doi.org/10.1007/BF01298413) 
 {#Gabriel72}

Quivers (referred to as _directed pseudographs_) were a tool in parts of the work of Ringel and Youngs in the second half the twentieth century to prove Heawood's formula for every finite genus, cf. e.g. Fig. 2.3 the monograph 

* Gerhard Ringel: _Map Color Theorem_. Springer. Grundlehren Band 209. 1974
{#Ringel1974}

Beware that, strictly speaking, for Ringel, "quiver" means "embedded quiver" (into a given surface);  in particular the author distinguishes between the two possible  orientations of an embedded loop.

Quivers embedded in surfaces are studied in: 

* Arthur T. White: _Graphs, Groups and Surfaces_. North Holland. Completely revised and enlarged edition (1985)
{#White84}

A special kind of quiver (finite, no loops, no parallel arcs) is treated in

* [[Gregory Gutin]], [[Jørgen Bang-Jensen]]: _Digraphs: Theory, Algorithms and Applications_. Springer Monographs in Mathematics. Second Edition (2009)
{#DG2nd}


* [[William Lawvere]]: _Qualitative Distinctions Between Some Toposes of Generalized Graphs_, Contemporary Mathematics 92 (1989) 
{#GeneralizedGraphs}

[[!redirects quiver]]
[[!redirects quivers]]
[[!redirects directed pseudograph]]
[[!redirects directed pseudographs]]
