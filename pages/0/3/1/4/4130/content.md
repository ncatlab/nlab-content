
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

## Idea

**Subdivision** is an (often) functorial process which takes as input some combinatorial notion of space (for example, a [[simplicial complex]] or [[simplicial set]]) and produces as output a more finely meshed space. It is related to the notion of [[classical triangulation|classical subdivision]].

There is a more general use of the term in which one simplicial set or complex is a subdivision of another, although the relation may not be functorially generated.  We will briefly look at one such example later.



There are various standard forms of functorial subdivision, the most common of which is **barycentric subdivision**.

## Definition

### For simplicial complexes

Barycentric subdivision is easiest to define for [[simplicial complexes]].  We have a pair of [[functors]]

$$SimpComplex \stackrel{\overset{U}{\to}}{\underset{Flag}{\leftarrow}} Pos$$ 

where

* The functor $U$ sends a [[simplicial complex]] $(V, \Sigma)$ to $\Sigma$, regarded as a [[poset]] ordered by inclusion, and

* The functor $Flag$ sends a poset $P$ to the simplicial complex whose vertex set is $P$ and whose [[simplex|simplices]] are the underlying sets $\{x_0, \ldots, x_n\}$ of flags $x_0 \lt \ldots \lt x_n$.

The composite $Flag \circ U$ is called the **subdivision** $Sd$; it is an endofunctor of $SimpComplex$.  A vertex of $Sd(X)$ is a simplex of $X$. 

Let $\alpha_X : X \to Sd(X)$ be a morphism of simplicial complexes that sends a vertex $v$ of $X$ to the vertex $\{v\}$ of $Sd(X)$. Then ${|f|}: {|X|}\xrightarrow{\cong} {|Sd(X)|}$ is an isomorphism, where $|-|$ is the usual [[geometric realization]] of simplicial complexes. In terms of categories, $\alpha$ is a natural transformation from the identity to the endofunctor $Sd$ whose geometric realization is a natural isomorphism.

This is what it looks like for $X$ the 2-simplex.
 

<img src="http://latex.codecogs.com/gif.latex?\xymatrix{%26%26%26%26\\%26%26%26%26\\%26\ar[ruu]\ar[ldd]%26%26\ar[luu]\ar[rdd]%26\\%26%26\ar[lu]\ar[ru]\ar[lld]\ar[rrd]\ar[uuu]\ar[d]%26%26\\%26%26\ar[ll]\ar[rr]%26%26}" />



The simplicial complex which is the 2-simplex has as its poset of simplices the partially ordered set of non-empty subsets of $\{0,1,2\}$.  The subdivided simplex therefore is the flags of that poset. The diagram shows that nerve of the corresponding category, (or rather its dual), as this is the simplicial set that one gets from this. The central vertex is the whole set $\{0,1,2\}$, the vertices on the long edges are the 2-element subsets and the three extremal vertices are the singletons.

### For simplicial sets

We can now define the barycentric subdivision of a [[simplicial set]] as follows.  [Recall](/nlab/show/simplicial+complex#vsSSet) that we can make any simplicial complex into a simplicial set.  If we do this for the standard $n$-simplex, which as a simplicial complex is the set $([n],P([n])$ for $[n] = \{0,1,\dots,n\}$, then we get the standard $n$-simplex simplicial set $\Delta^n$.  We can then define the subdivision of $\Delta^n$, as a simplicial set, to be the simplicial set corresponding to its simplicial-complex subdivision.  Finally, we can make this functorial on maps between standard simplices, and left [[Kan extension|Kan extend]] to a [[cocontinuous functor|cocontinuous]] endofunctor of $SSet$.

Explicitly: 

+-- {: .num_defn #ColimitFormulaForBarycentricSubdivision}
###### Definition

Write $Sd \Delta[n]$ for the [[nerve]] of [[category of non-degenerate simplices]] in the standard $n$-[[simplex]].

For $X$ an arbitrary [[simplicial set]], its barycentric subdivision is

$$
  Sd X \simeq \underset{\to}{\lim}_{\Delta[n] \to X} Sd \Delta[n]
  \,.
$$

=--

A review is for instance around ([Fiore-Paoli def. 3.1](#FiorePaoli)).


## Properties

### Adjointness with the $Ex$-functor

By construction (or the [[adjoint functor theorem]]), the subdivision functor $Sd$ on simplicial sets has a [[right adjoint]], called $Ex$.  A countably infinite iteration of $Ex$, called $Ex^\infty$, can be used to construct [[Kan fibrant replacements]] in the [[model structure on simplicial sets]].

This functorial subdivision corresponds to the classical [[barycentric subdivision]].  Other [[classical triangulation|classical subdivision]]s that are frequently encountered include the middle edge subdivision.  This latter is closely related to the [[ordinal subdivision]] of simplicial sets.

### Relation to category of simplices
 {#RelationToCategoryOfSimplices}


+-- {: .num_prop }
###### Proposition

If every non-degenerate simplex in $X$ is given by a [[monomorphism]] $\Delta^n \to X$, then the barycentric subdivision of def. \ref{ColimitFormulaForBarycentricSubdivision} is equivalently given by the [[nerve]] of the [[full subcategory]] of its [[category of simplices]] on the non-degenerate simplices.

=--

([Thomason, p. 311](#Thomason))

## References

* [[Rick Jardine]], _Simplicial approximation_, Theory and Applications of Categories, Vol. 12, 2004, No. 2, pp 34-72. ([web](ftp://ftp.math.ethz.ch/EMIS/journals/TAC/volumes/12/2/12-02aabs.html))

A review is in section 3 of 

* [[Thomas Fiore]], [[Simona Paoli]], _A Thomason model structure on the category of small $n$-fold categories_  ([arXiv:0808.4108](http://arxiv.org/abs/0808.4108))
 {#FiorePaoli}

The relation to the [[nerve]] of the [[category of simplices]] is disucssed in 

* R. W. Thomason, _Cat as a closed model category_, Cahiers Topologie G&eacute;om. Diff&eacute;rentielle, 21(3):305&#8211;324, 1980.
 {#Thomason}

[[!redirects subdivisions]]
[[!redirects barycentric subdivision]]
[[!redirects barycentric subdivisions]]
[[!redirects Ex]]
[[!redirects Sd]]
[[!redirects sd]]
