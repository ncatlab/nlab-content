
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A free [[operad]] is [[free functor|free]] on its underlying collection of operations.

## Definition

Let $V$ be a [[symmetric monoidal category]].

For $G$ a [[discrete group]], write $V^G$ for the category of objects of $V$ equipped with a $G$-[[action]]. For $V$ symmetric monoidal this is again a [[symmetric monoidal category]] and the [[forgetful functor]] $V^G \to V$ is symmetric monoidal.

+-- {: .un_defn}
###### Definition

The category of **collections** of $V$ is

$$
  V Coll := \prod_{n \in \mathbb{N}} V^{S_n}
  \,.
$$

=--

Notice that both $S_0$ and $S_1$ are the trivial group.

So a $V$-operad $P$ is a special $V$-collection with extra structure relating its components. This gives an evident [[forgetful functor]] $U : V Operad \to V Coll$ and its [[left adjoint]], the free operad functor

$$
  F : V Coll \stackrel{\leftarrow}{\to} V Operad : U
  \,.
$$

This is for instance used to define the [[model structure on operads]] by [[transferred model structure|transfer]] along this adjunction from a model struucture on $V$.

The free operad functor may more explcitly be described as follows (for instance [BerMor03 section 5.8](http://arxiv.org/PS_cache/math/pdf/0206/0206094v3.pdf#page=22))

Let $\mathbf{T} := Core(\Omega_pl)$ be the [[core]] of the category of planar rooted [[tree]]s. Write

* $t_n \in \Omega_n$ for the $n$-corolla (the tree with a single vertex, $n$ inputs and its unique output root)

* for $T$ any tree with $n$-ary root vertex let $\{T_i\}_{i=1}^n$ be the sub-trees such that $T = t_n(T_1, \cdots, T_n)$.

Then every $K \in V Coll$ defines a functor $\bar K : \mathbf{T}^{op} \to V$ by the inductive formula

$$
  \bar K : | \mapsto I
$$

$$
  \bar K : T \mapsto \bar K(t_n(T_1, \cdots, T_n))
  := K(n) \otimes K(T_1) \otimes \cdots K(T_n)
  \,.
$$

Let moreover $\lambda : \mathbf{T} \to Sez$ be the functor that sends a tree to the set of numbering of its incoming edges, and let $\bar \lambda : \mathbf{T} \to V$ be given by postcomposition with $S \mapsto \coprod_{s \in S} I$.

Then the **free operad** on a collection $K$ is the [[coend]]

$$
  \bar K \otimes_{\mathbf{T}} \bar \lambda
  =
  \int^{T \in \mathbf{T}}
   \bar K(T) \otimes \bar \lambda(T)
  \,.
$$

## Examples

Let $V$ be a [[cartesian monoidal category]] and $K = {*}$ the terminal collection, which is the [[terminal object]] in each degree, with, necessarily, trivial $S_n$-action.

The free operad on this should be the $V$-[[A-infinity operad]] it consists in degree $n$ of precisely $|S_n|$-operations per $n$-ary planar tree. So every planar $n$-ary tree is regarded by the operad as one distinct operation to multiply $n$ elements, and freely adjoining to each tree a $S_n$-action amounts to not dividing out any commutativity symmetry on these operations.

Riemann surfaces operad (TO BE EXPANDED)

Deligne-Mumford opeard (TO BE EXPANDED)

Little discs operad, framed little discs operad (TO BE EXPANDED) -- See [[Deligne conjecture]]

## References





[[!redirects collection]]
[[!redirects collections]]