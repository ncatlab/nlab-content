
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
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

For $X$ a [[manifold]], 

* a  *simplicial [[triangulation]]* is a [[simplicial complex]] $Tr(X)$ and a [[homeomorphism]] $\left\vert Tr(X)\right\vert \xrightarrow{homeo} X$ from its [[geometric realization]] to the [[underlying]] [[topological space]] of $X$.

* a *combinatorial triangulation* is a simplicial triangulation such that for each simplex $\sigma$ the *link* of $\sigma$ (the [[union]] of all simplices $\tau$ that intersect $\sigma$ such that both $\sigma$ and $\tau$ are faces of a simplex) is [[homeomorphism|homeomorphic]] to a [[sphere]].

A *triangulation conjecture* [[conjecture|conjectures]] and *triangulation theorem* [[proof|proves]] that a given kind of triangulation exists for a given kind of [[manifold]]. Conversely, deep theorems assert that a given kind of triangulation does *not* generally exists for a given class of manifolds.

## Statements

### Existence of triangulations

It is easy to show that every [[piecewise-linear manifold]] admits a combinatorial triangulation, so that combinatorial triangulability is often understood to mean existence of a piecewise-linear structure.

A compatible piecewise-linear structure, hence a combinatorial triangulation, hence a simplicial triangulation, does exist for 

* every [[smooth manifold]] 
  
  ([Cairns 1935](#Cairns35) [Whitehead 1940](#Whitehead40))

* every [[topological manifold]] of [[dimension]] 2, hence every [[surface]] 

  ([Rado 1924](#Rado25))

* every [[topological manifold]] of [[dimension]] 3, hence every [[3-manifold]] 

  ([Moise 1952](#Moise52))

### Non-existence of triangulations

In each dimension $\geq$ 4 there exist [[topological manifolds]] *not* admitting a combinatorial triangulation ([Kirby & Siebenmann 1969](#KirbySiebenmann69)).

In each dimension $\geq$ 5 there exist [[topological manifolds]] *not* even admitting a simplicial triangulation ([Manolescu 2016](#Manolescu16))

For [[topological manifolds]] $X$ of [[dimension of a manifold|dimension]] $dim(X) \leq 3$ triangulations still exist in general, but for every dimension $\geq 4$ there exist topological manifolds which do not admit a triangulation. For $dim(X) \geq 5$ there is an [[obstruction]] class $\Delta(X) \in H^4(X; \mathbb{Z}/2)$ in the [[ordinary cohomology]]  with [[coefficients]] in [[finite group of order 2|$\mathbb{Z}/2$]], in that $X$ admits a triangulation if and only if $\Delta(X) = 0$. 

## Related concepts

* [[equivariant triangulation theorem]]

## References 

Review:

* [[Ciprian Manolescu]], *Triangulations of manifolds* ([pdf](https://web.stanford.edu/~cm5/tm.pdf), [[Manolescu_TriangulationsOfManifolds.pdf:file]])

Proof that every [[surface]] admits a combinatorial triangulation:

* {#Rado25} Rado 1925

Proof that every [[3-manifold]] admits the structure of a [[smooth manifold]] and hence of a combinatorial triangulation:

* {#Moise52} [[Edwin E. Moise ]],  *Affine Structures in 3-Manifolds: V. The Triangulation Theorem and Hauptvermutung*, Annals of Mathematics Second Series, Vol. 56, No. 1 (Jul., 1952), pp. 96-114 (19 pages)

Proof that every [[smooth manifold]] admits a combinatorial triangulation:

* {#Cairns35} Cairns 1935

* {#Whitehead40} Whitehead 1940

Proof that in every dimension $dim \geq 4$ there exist topological manifolds without combinatorial triangulation:

* {#KirbySiebenmann69} Kirby Siebenmann 1969

Proof that in every dimension $dim \geq 5$ there exist topological manifolds without simplicial triangulation:

* {#Manolescu16} [[Ciprian Manolescu]], *$Pin(2)$-equivariant Seiberg-Witten Floer homology and the Triangulation Conjecture*, J. Amer. Math. Soc. 29 (2016), 147-176  ([arXiv:1303.2354](https://arxiv.org/abs/1303.2354), [doi:10.1090/jams829]( https://doi.org/10.1090/jams829))


[[!redirects triangulation theorems]]

