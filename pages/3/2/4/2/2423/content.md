+-- {: .standout}

This is a sub-entry of [[geometric models for elliptic cohomology]] and [[A Survey of Elliptic Cohomology]] 

See there for background and context.

This entry here is about the definition of [[cobordism category|cobordism categories]] for [[Riemannian cobordism]]s.

=--


see also 

* [[cobordism]]

* [[Riemannian cobordism]]

* [[cobordism category]]

* [[(infinity,n)-category of cobordisms]]

***

# Contents 

* [part 1 - topological bordism category](#topological)

* [part 2 - Riemannian bordsm category](#Riemannian)


# Part 1 (topological) bordism category {#topological}

**definition sketch**

the [[category]] $d-B$  has 

* as [[object]]s closed $(d-1)$-dimensional _smooth_ [[manifold]]s

* and the [[morphism]]s are [[compact space|compact]] $d$-dimensional smooth [[manifold]]s with boundary, modulo [[diffeomorphism]] "rel boundaries" (i.e. those that restrict to the identy on the boundary)

The composition of [[morphism]]s is given by gluing of manifolds along their boundary


# Part 2 Riemannian bordism category {#Riemannian}

in all of the following

* the symbol $Y$ denotes $d$-dimensional a [[Riemannian manifold]] 

  without boundary. 

* **note on boundaries** technically it is convenient to never ever work with manifolds with Riemannian or other structure with boundary. Instead, we always just mention manifolds without boundary and encoded the way in which they are still to be thouhgt of as [[cobordism]]s by injecting _collars_ into them. The manifolds with boundary could be obtained by cutting of at the _core_ of these collars (see the definition below) but, while this is morally the idea, in the construction this is never explicitly considered.

  Also, later when we generalize [[manifold]]s to [[supermanifold]]s it will be very convenient not to have to talk about boundaries

$d-RB$ is defined using bicollars from the beginning

an object in $d-RB$ is a quintuple

consisting of

* a $d$-dimensional [[Riemannian manifold]] $Y$;

* a **core** $(d-1)$-manifold $Y^c$ sitting $Y^c \hookrightarrow Y$ in a thickening $Y^d$ -- being a $d$-manifold -- 

* $Y^+, Y^- \hookrightarrow Y$ two disjointly embedded open $d$-dimensional manifolds such that

  * $Y^c$ is in the closure of both $Y^+$ and $Y^-$

  * that $Y^+ \coprod Y^- = Y \backslash Y^C$

> so the _picture_ of an object, which is missing in this writeup here for the moment, is a $d-1$-dimensional Riemannian manifold that is thickened a bit in one further othogonal direction

**definition** A **Riemannian bordism** from $(Y_0,Y_0^c, Y_0^{\pm})$ to $(Y_1,Y_1^c, Y_1^{\pm})$ is a triple $(\Sigma, i_0, i_1)$ where

* $\Sigma$ is a $d$-dimensional [[Riemannian manifold]] without boundary

* for $i=0,1$ an open neighbourhood of the core $Y_i^c \hookrightarrow W_i \stackrel{open}{\hookrightarrow} Y_i$

  this defines the intersections $W^\pm_k := W_k \cap Y^\pm_k$ with the two collars for each $k = 0,1$.

* a smooth map $i_k : W_k \to \Sigma$

  such that

  * $i_k : W^+_k \cup Y_k^c \to Z$ is a proper map;

  * (+) for $i^+_k := i_k/W^+_k$ are [[isometry|isometric]] embeddings into $\Sigma \backslash i_1(W^-_1 \cup Y^c_1)$

    i.e. restricted to the (+)-collar the embedding of the thickened object into the would-be cobordisms is isomertric

  * the core $\Sigma^c := \Sigma \backslash (i_0(W^+_0) \cup i_1(W^-_1))$ is compact

    i.e. cutting of the (+)-collar of the incoming object and the (-)-collar of the outgoing object yields a compact manifold


**Remark**. Notice that this builds in an asymmetry: the (+)-side is preferred. This is intentionally: also the category $TV$ of [[topological vector space]]s will have a similar asymmetry (from the fact that for $\infty$-dimensional vector spaces there is an evaluation map but not necessarily a coevaluation/unit for $V \otimes V^*$), similarly, with the above asymmetric definition we have a cobordims $Y \coprod Y^* \to \emptyset$ (where $Y^*$ is obtained from $Y$ by reversing orientation) but _not_ one going the other way round.

A big difference between [[TQFT]]s and the Riemannian QFTs is that for [[TQFT]]s the vector spaces assigned to objects are necessarily finite-dimensional. So this issue here with infinite-dimensional vector spaces and the asymmetry that this introduces is crucial for Riemannian QFTs.

**example** Given any [[isometry]] 

$$
  \phi : W_0 \to W_1
$$

such that $\phi$ preserves the decomposition $W_k^\pm, Y_k^c$ we get a [[Riemannian cobordism]] using

$$
  \Sigma := W_1
$$

and

$$
  i_1 = Id_{W_1}\,,\;\;\;\;\; i_0 = \phi
$$