<div class="rightHandSide toc">

[[!include functorial quantum field theory - contents]]

</div>


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

**definition (morphisms in $d-RBord$)** morphisms from $Y_0$ to $Y$ in $R Bord_d$ (or $d-RB$ or whatever the notation is) are [[isometry]] classes _rel. boundary_ (see below) of [[Riemannian cobordism]]s from $Y_0$ to $Y_1$.

We require the commutativity of the following diagram

$$
  \array{
    V_1 &\stackrel{i_1}{\to}& 
    X
    &\stackrel{i_0}{\leftarrow}&
     V_0
    \\
    \downarrow^{f_1} &&
    \downarrow &&
    \downarrow^{f_0}
    \\
    V'_1 &\stackrel{i'_1}{\to}&
    X'
    &\stackrel{i'_0}{\leftarrow}&
    V'_0
  }
$$

The [[isometry]] $(F,f_0, f_1)$ is "rel. boundary" if $f_0 = Id$ and $f_1 = Id$

so an isomorphism "rel boundary" in the sense here (more "rel collars", really) is an [[isometry]] $F$ sitting in a diagram

$$
  \array{
    V_1 &\stackrel{i_1}{\to}& 
    X
    &\stackrel{i_0}{\leftarrow}&
     V_0
    \\
    \downarrow^{Id} &&
    \downarrow &&
    \downarrow^{Id}
    \\
    V'_1 &\stackrel{i'_1}{\to}&
    X'
    &\stackrel{i'_0}{\leftarrow}&
    V'_0
  }
$$


## description for $d=1$

we decribe $R Bord_1$ (or $1-R B$) 

it has at least the object

$$
 pt = 
  \left(
    \array{
        pt^- & pt^c & pt^+
        \\
        -- & \bullet & --
    }
  \right)
  =
  (\mathbb{R}, \{0\}, \mathbb{R}_\pm)
$$

which is a point with collar all of $\mathbb{R}$.

**Lemma** every object in $R Bord_1$ which is _connected_ and not the empty set is [[isomorphism|isomorphic]] to this $pt$

now for $t \in \mathbb{R}_+$ consider the morphism

$$
  I_t \in R Bord_1(pt,pt)
$$

defined as the triple $(\mathbb{R}, i_0, i_1)$ where $i_0 : \mathbb{R} \to \mathbb{R}$ is the identity map, and where $i_1 : \mathbb{R} \to \mathbb{R}$ is translation by $t$.

This means that $i_0$ takes the core of in the incoming point to $0 \in \mathbb{R}$ while $i_1$ takes the core of the outgoing point to $t \in \mathbb{R}$. Everything in $\mathbb{R}$ outside of $[0,1]$ is hence "collar" and this describes what naively one would think of as just the [[interval]] $[0,1]$ regarded as a [[Riemannian cobordism]].


**Lemma** The composition of these cobordisms is given by

$$
  I_t \circ I_{t'} = I_{t+t'}
$$

There are also morphisms

$$
  L_+ : pt \coprod pt \to \emptyset
$$

and

$$
  R_+ : \emptyset \to pt \coprod pt 
$$

which describe morally the same cobordisms as $I_t$ does, but where both boundary components are regarded as incoming or noth as outgoing, respectively.

Here $L_t$ is formall given exactly as $I_t$ only that the map $i_0 : \mathbb{R} \to \mathbb{R}$ is not the identity, but reflection at the origin. This encodes the orientation reversal at that end.

This is defined for $t \gt 0$. For $t= 0$ the morphism $L_0$ is still defined, but R_0$ is not!! Exercise: check carefully with the above definition, keeping the asymmetry mentioned there in mind, to show that the obvious definition of $R_0$ does not satisfy the axioms above.

So this means that we have a cobordism of length 0 going $\emptyset \to pt \coprod pt$, but all cobordisms going the other way round $pt \coprod pt \to \emptyset$ will have to have non-vanishing length.

Another morphism in $R Bord_1$ is the morphism

$$
  \sigma : pt \coprod pt \to pt \coprod pt
$$

which just interchanges the two points, without having any length.

**Lemma** We have the following composition laws:

* $L_t \circ \sigma = L_t$

* $R_t = \sigma \circ R_t$

* $R_t \circ_{L_0} R_{t'} = R_{t+t'}$

where in the last line we have the composition that is obvious once you draw the corresponding picture, which in full beuaty is

$$
  (Id_{pt} \otimes L_0 \otimes Id_{pt}) \circ (R_t \otimes R_{t'})
$$

where the [[tensor product]] $\otimes$ is given by disjoint union.

**theorem** the [[symmetric monoidal category]] $R Bord_1$ is _generated_ as a symmetric monoidal category by 

* the object $pt$

* the morphisms $L_0$, $\{R_t\}_{t \gt 0}$

subject to the relations

$$
  L_0 \circ \sigma = L_0
$$

$$
  \sigma \circ R_t = R_t
$$

$$
  \forall t,t' \gt 0 : R_t \circ_{L_0} R_{t'} = R_{t + t'} 
$$

**corollary** symmetric monoidal functors 

$$
  E \in Fun^\otimes(R Bord_1, TV)
$$

to the category $TV_\mathbb{R}$ of [[topological vector space]]s are specified by their imagges of these generators. We have

* $E : pt \mapsto V$

* $E : L_0 \mapsto (\lambda :  \otimes V \to \mathbb{R}$

* $E : R_t \mapsto \rho_t \in V \otimes V$

the $\rho_t$ form a [[semigroup]] (for instance a typical example would be $V = \Gamma(E)$ a space of sections of a vector bundle and $\rho_t = e^{-t \Delta}$ for $\Delta$ a [[Laplace operator]] on $E$).

**note** for $\lambda : V \otimes V \to \mathbb{R}$ to be continuous, one cannot use the Hilbert tensor product $\otimes_H$

the reason is that we have the folloing possible mpas out of the following possible tensor products

$$
  \mathbb{R}
  \stackrel{\lambda}{\leftarrow}
  V \otimes_{algebraic} V \stackrel{finite rank}{\hookrightarrow}
  End(V)
$$

$$
  \mathbb{R}
  \stackrel{\lambda}{\leftarrow}
  V \otimes V \stackrel{trace class}{\hookrightarrow}
  End(V)
$$

$$
  \mathbb{R}
  \stackrel{\lambda}{\leftarrow}
  V \otimes_H V \stackrel{Hilbert Schmitdt}{\hookrightarrow}
  End(V)
$$

(so here the middle one is the one we are actually using)