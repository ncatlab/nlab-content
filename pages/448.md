+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

##Idea and definition##

A polyhedron (beware remark \ref{RemarkOnTerminology}) is a [[topological space]] made up of very simple bits 'glued' together. The 'bits' are **[[simplices]]** of different [[dimensions]]. An abstract _simplicial complex_ is a neat combinatorial way of giving the corresponding 'gluing' instructions, a bit like the plan of a construction kit!

+--{: .num_defn}
######Definition#######

A **simplicial complex** $K$ (sometimes called an **abstract** simplicial complex) consists of 

1. a [[set]] of objects, $V(K)$, called **vertices** 

1. a set, $S(K)$, of finite non-empty subsets of $V(K)$, called **[[simplex|simplices]]**.  

such that the simplices satisfy the following conditions: 

1. if $\sigma \subset V(K)$ is a simplex and $\tau \subset \sigma$, $\tau \ne \emptyset$, then $\tau$ is also a simplex; 

1. every singleton $\{v\}$, $v \in V(K)$, is a simplex.  

=--

We say $\tau$ is a **face** of $\sigma$.  If $\sigma \in S(K)$ has $p+1$ elements it is said to be a **$p$-simplex**.  The set of $p$-simplices of $K$ is denoted by $K_p$. The **dimension** of $K$ is the largest $p$ such that $K_p$ is non-empty. 

A **map** of simplicial complexes $K \to L$ is a function $f: V(K) \to V(L)$ such that whenever $\sigma \subseteq V(K)$ belongs to $S(K)$, the [[image]] $f(\sigma)$ belongs to $S(L)$. 


+--{: .num_remark #RemarkOnTerminology}
###### Remark

The word 'polyhedron' is used here as it is often used by [[algebraic topology|algebraic topologists]], as a space described by a simplicial complex. Elsewhere in mathematics, it might mean a finite union of finite intersections of sets in Euclidean space defined by linear inequalities, usually assumed compact, and often with other assumptions as well (e.g., connected or convex). The various usages have a long history, as recounted in detail in Lakatos's _Proofs and Refutations_. 

=--


##Examples##
1. Recall that a 'simple' graph is an undirected [[graph]] with no loops or multiple edges. A simple graph is essentially the same thing as a 1-dimensional simplicial complex, by interpreting edges as simplices and vice versa (see [[graph#undirected_graphs_as_1complexes_barycentric_subdivision|undirected graphs as 1-complexes]]). (On the other hand, a 1-dimensional [[simplicial set]] is essentially the same thing as a 'directed multigraph', i.e., a [[quiver]].)

1. Given a space and an [[open cover]], the nerve of the cover is a simplicial complex (see [[Čech methods]] and the discussion there). The [[Vietoris complex]] is another given by a related method.

1. Given any two sets $X$ and $Y$, and a relation $R\subseteq X\times Y$, there are two simplicial complexes that encode information on the relation. These are generalisations of the nerve and the Vietoris complex. They are studied in detail in [[Dowker's theorem]].

1.  If $(P,\leq)$ is a [[poset]], then the [[nerve]] of the associated category has a simple description. The vertices are the points of $P$ and the simplices are the [[flag|flags]].


1. **Buildings:**
An important class of simplicial complexes is provided by the notion of [[building]], due to Jacques Tits.  


##Simplicial complexes v. simplicial sets {#vsSSet}

Simplicial complexes are, in some sense, special cases of [[simplicial set|simplicial sets]], but only 'in some sense'. 

To get from a simplicial complex to a fairly small simplicial set, you  pick a [[total order]] on the set of vertices. Without an order on the vertices, you cannot speak of the $k^{th}$ face of a simplex, which is an essential feature of a simplicial set! The degeneracies are obtained by repeating an element when listing the vertices of a simplex. If $\sigma = \{v_0,v_1,\ldots, v_n\}$, with $v_0\lt v_1\lt \ldots \lt v_n$ then, for instance, $s_0(\sigma) = \{v_0,v_0, v_1,\ldots, v_n\}$. 

If you do not want to pick an order then you can still form a simplicial set where to each $n$-simplex of the original simplicial complex will correspond to $(n+1)!$ simplices of that associated simplicial set. The result is more unwieldy, but can be useful under some circumstances as it defines a functor from the category of simplicial complexes to that of simplicial sets.  This is very important when discussing group actions on simplicial complexes and how this transfers to the associated simplicial set.

##Simplicial complexes as sheaves on a site##

Simplicial sets are essentially (that is, up to equivalence) [[presheaves]] on the [[simplex category]] of finite nonempty totally ordered sets, whereas simplicial complexes may be regarded as [[concrete sheaf|concrete presheaves]] on the category $Fin_{+}$ of finite nonempty sets and functions between them. This works as follows: given a simplicial complex, $K = (V(K), S(K))$, define a presheaf $K^\sim: Fin_{+}^{op} \to Set$ whose values are sets of functions $\phi$: 

$$K^\sim(B) \stackrel{def}{=} \{\phi: B \to V(K)| \phi(B) \in S(K)\}, \qquad K^\sim(f: A \to B)(\phi) \stackrel{def}{=} \phi \circ f$$ 

This defines an evident [[functor]] 

$$SimpComplex \to Set^{Fin_{+}^{op}}: K \mapsto K^\sim$$ 

that is [[full and faithful functor|full and faithful]]. The essential image is the subcategory of concrete presheaves, where a presheaf $F \colon Fin_{+}^{op} \to Set$ is **concrete** if the canonical map 

$$F(B) \to F(1)^{\hom(1, B)}$$ 

is an injection. The point is that a morphism of concrete presheaves $F \to G$ is uniquely determined from the function $F(1) \to G(1)$ between their underlying sets (i.e., the underlying-set functor on concrete presheaves is [[faithful functor|faithful]], so that a concrete presheaf is a set equipped with extra [[stuff, structure, property|structure]] -- that's what makes it "concrete"). 

(Equivalently but somewhat more elaborately, the category of concrete presheaves is the same as the full subcategory of [[concrete sheaf|concrete sheaves]] on $Fin_{+}$ with respect to the trivial [[Grothendieck topology|topology]], where the only covering sieve $F \hookrightarrow hom(-, D)$ is the maximal sieve.) 

From this point of view, it is immediate that simplicial complexes are the [[separated presheaf|separated objects]] for the [[Lawvere-Tierney topology]] on $Set^{Fin_{+}^{op}}$ whose sheaves are sets, via the sheafification functor 

$$\Gamma = \hom(\mathbf{1}, -) = ev_1 \colon Set^{Fin_{+}^{op}} \to Set$$ 

which has a right adjoint. (See [[local topos]].) It follows from this characterization that the category of simplicial complexes is a [[quasitopos]], and in particular is locally cartesian closed. The category of simplicial sets on the other hand is a [[topos]]. 

##Geometric realisations and Polyhedra##

An abstract simplicial complex is a combinatorial gadget that models certain aspects of a spatial configuration.  Sometimes it is useful, perhaps even necessary, to produce a topological space from that data in a simplicial complex. 

### Idea
To each simplicial complex $K$, one can associate a topological space called the _polyhedron_ of $K$ often also called the  _geometric realisation_ of $K$ and denoted $|K|$.   (This is essentially a special case of the geometric realisation of a simplicial sets.)


This can be constructed by taking a copy $K(\sigma)$ of a standard topological $p$-simplex for each $p$-simplex of $K$ and then 'gluing' them together according to the face relations encoded in $K$.

We therefore first need the definition of a standard $p$-simplex

+--{: .num_defn}
######Definition######
The _standard (topological) $p$-simplex_ is (usually)  taken to be the convex hull of the basis vectors $\mathbf{e}_1, \mathbf{e}_2,\ldots, \mathbf{e}_{p+1}$ in $\mathbb{R}^{p+1}$.
=--

###Intuition
The geometric realisation $|K|$ of a simplicial complex, $K$  is then constructed by taking, for each abstract $p$-simplex, $\sigma\in S(K)$, a copy, $K(\sigma)$ of such a standard topological $p$-simplex, and then 'gluing' faces together, so whenever $\tau$ is a face of $\sigma$ we identify $K(\tau)$ with the corresponding face of $K(\sigma)$. This space is usually denoted $\Delta^p$.

###Canonical construction

As a set, $|K|$ is constructed as follows: 

$|K|$ is the set of all functions from $V(K)$ to  the closed interval $[0,1]$ such that

* if $\alpha \in {|K|}$, the set
 
$$\{v \in V(K) \mid \alpha(v)  \neq  0\}$$

is a simplex of $K$;

 * for each $\alpha \in {|K|}$,  
$$\sum_{v \in V(K)} \alpha (v) = 1.$$

There are two commonly used topologies on the set $|K|$. The first is the _metric topology_: we put a metric $d$ on $|K|$ by 

$$d(\alpha,\beta) = \Big(\sum_{v\in V(K)} (\alpha(v) - \beta(v))^2\Big)^\frac{1}{2}.$$

$|K|$, when endowed with the metric space topology, will be denoted $|K|_d$. Notice that when $V(K)$ is finite, this gives $|K|_d$ as a subspace of the metric space $\mathbb{R}^{\#(V(K))}$ (which is usually of much higher dimension than might seem geometrically significant in a given context). 

The second topology is the _coherent topology_: each geometric simplex $|s|$ consists of all $\alpha \in {|K|}$ supported in $s$, and is given the subspace topology inherited as a subset of $|K|_d$; then the coherent topology on $|K|$ is the largest topology for which all inclusions ${|s|} \hookrightarrow {|K|}$ are continuous. This topological space is normally denoted just $|K|$, reflecting the fact that the coherent topology is regarded as the default topology to put on the set $|K|$. 

Note that if $s \subseteq t$ is an inclusion of simplices in $K$, then there is an induced subspace inclusion ${|s|} \hookrightarrow {|t|}$. The space $|K|$ may then be characterized as the colimit in $Top$ of the diagram consisting of geometric simplices $|s|$ and inclusions between them, so that a function $f: {|K|} \to X$ is continuous if and only if its restriction to each simplex $|s|$ is continuous. In particular, the identity function ${|K|} \to {|K|}_d$ is continuous, so that the coherent topology contains the metric topology (and is often strictly larger). 

* **Warning:** The geometric realization of a simplicial complex does not preserve products. Indeed, the product of two intervals in the category of simplicial complexes is the tetrahedron! 

## Triangulable spaces

If a topological space can be described up to homeomorphism as the geometric realization of a simplicial complex, we say it is **triangulable**, and a **triangulation** of a space $X$ is a simplicial complex $K$ together with a homeomorphism $h: |K| \to X$. (This is discussed in a bit more detail in the entry on [[classical triangulation]]. 

There is another stronger notion of triangulation used by geometric topologists: a **piecewise-linear (PL) structure** on a [[topological manifold]] $X$ is given by a [[manifold|PL atlas]], where the transition functions are piecewise-linear homeomorphisms. (A homeomorphism $U \to V$ is **piecewise linear** if its graph is the intersection of $U \times V$ with a semilinear set $S$, meaning that $S$ is given by a finite Boolean combination of solution sets of linear inequalities.)  



#### Examples from manifold theory

* All [[manifold|smooth manifolds]] are triangulable and, in fact, admit PL structures. 

* All topological manifolds in dimensions 2 and 3 admit PL structures, and are in fact smoothable (admit a smooth manifold structure). 

* The $E_8$ [[E8 manifold|manifold]] does not admit a triangulation, much less a PL structure. 

* In dimensions $n \geq 5$, the $(n-2)$-fold suspension of the [[Poincaré sphere]] is homeomorphic to the $n$-sphere, hence is triangulable, but it does not admit a PL structure. 

#### Relation to simplicial sets

The following statement may seem obvious, but it requires careful proof: 

* A space is triangulable if and only if it is homeomorphic to the geometric realization of a simplicial set. 

As an important step: 

* The geometric realization of the nerve of a poset is triangulable. 

The basic technique is to use [[subdivision]]. 

## Related concepts

* [[triangulation]], [[triangulation theorem]]


## References

Textbook account:

* {#Spanier66} [[Edwin Spanier]], _Algebraic topology_, Springer 1966 ([doi:10.1007/978-1-4684-9322-1](https://link.springer.com/book/10.1007/978-1-4684-9322-1))

Exposition:

* {#Erleben2010} Kenny Erleben, *Simplicial complexes*, 2010 ([[Erleben_SimplicialComplexes.pdf:file]])

On simplicial complexes forming a [[quasitopos]] of [[concrete sheaves]]:

* [[John Baez]] and [[Alex Hoffnung]], _Convenient Categories of Smooth Spaces_, Trans. Amer. Math. Soc. 363 (2011), 5789&#8211;5825. [(arXiv)](http://arxiv.org/abs/0807.1704)


[[!redirects simplicial complexes]]