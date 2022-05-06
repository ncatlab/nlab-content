

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Stratifolds are a generalization of smooth [[manifolds]] -- a notion of [[generalized smooth space]] --  which were introduced by [[Matthias Kreck|Kreck]]; see his [lecture notes](#Kreck).

Stratifolds comprise one of the many variants of the concept of a _[[stratified space]]_, and they may include some types of singularities.

## Definition

Stratifolds form a class of [[differential module|differential modules]], which are pairs $(S,C)$ of a [[topological space]] $S$ together with a subalgebra $C$ of the algebra of [[continuous function|continuous]] real-valued functions $S\to R$ such that 

1. $C$ is locally detectable, i.e. for all continuous functions $f: S\to R$, $f$ is in $C$ iff for every $x\in S$ there exist an open neighborhood $U\ni x$ and $g\in C$ such that $g|_U = f|_U$,  

1. let $f_1,\ldots,f_n$ be elements of $C$ and $\phi : R^n\to R$ a smooth function. Then $\phi \circ (f_1,\ldots,f_n) : S\to R$ is in $C$.

Local detectability is equivalent to requiring that $C$ is an algebra of global sections of a given subsheaf of the [[sheaf]] of all continuous functions on $S$; in particular [[germ]]s at every point can be defined. 

For a [[manifold]] $C= C^\infty(S)$. For a differentiable space $S = (S,C)$ a [[tangent space]] $T_x S$ can be defined at each $x\in S$. Define $S^i = \{x\in S | \mathrm{dim} T_x S = i\}$. By construction, $S$ decomposes into a [[disjoint union]] $S = \biguplus_{i=0}^\infty S^i$. There is an induced stratifold structure on the topological subspace $S^i\subset S$, which we denote by $(S^i, C(S^i))$.  

+-- {: .num_defn }
###### Definition

A __$k$-dimensional stratifold__ $(S,C)$ is a differential space such that 

* $S$ is _locally compact [[Hausdorff space]] with countable basis,

* $T_x S \leq k$ for all $x\in S$ (i.e. $S = \bigcup_{i=0}^k S^i$), 

* $(S^i,C(S^i))$ is isomorphic to a smooth [[manifold]],

* the restriction map $C(S)\to C(S^i)$ induces an isomorphism of [[stalk]]s of germs $C(S)_x\to C(S_i)_x = C^\infty(S^i)_x$ in all points $x\in S^i$,

* for all $y\in S$, and all $U\ni y$ open, there is a "bump function" $\rho\in C$ nonvanishing at $y$, but whose support is contained in $U$.

=--


## References

* [The stratifold page](https://www.hcm.uni-bonn.de/homepages/prof-dr-matthias-kreck/the-stratifold-page/)

* [[Matthias Kreck]], _Differential Algebraic Topology_ ([pdf](http://www.hausdorff-research-institute.uni-bonn.de/files/kreck-DA24_08_07.pdf))
 {#Kreck}

[[!redirects stratifolds]]

