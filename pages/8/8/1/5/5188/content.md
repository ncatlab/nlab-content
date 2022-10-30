
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

A _free [[operad]]_ is [[free functor|free]] on a collection of operations.

Given a collection $k$-ary operations-to-be for each $k \in \mathbb{N}$, the free operad on this collection has as $n$-ary operations the collection of all [[trees]] with $n$ leaves equipped with a labelling of each vertex $v$ with a $k$-ary operation, for $k$ the incoming edges to $v$.

## Definition

Let $V$ be a [[symmetric monoidal category]].

For $G$ a [[discrete group]], write $V^G$ for the category of objects of $V$ equipped with a $G$-[[action]]. For $V$ symmetric monoidal this is again a [[symmetric monoidal category]] and the [[forgetful functor]] $V^G \to V$ is symmetric monoidal.

+-- {: .num_defn}
###### Definition

The category of **collections** ([Berger-Moerdijk](#BergerMoerdijk)) or **$\mathbb{S}$-modules** ([Getzler-Kapranov](#GetzlerKapranov)) of $V$ is

$$
  V Coll := \prod_{n \in \mathbb{N}} V^{S_n}
  \,.
$$

=--

Notice that both $S_0$ and $S_1$ are the trivial group.

So a $V$-operad $P$ is a special $V$-collection with extra structure relating its components. This gives an evident [[forgetful functor]] 

$$
  U : V Operad \to V Coll
  \,.
$$ 

+-- {: .num_defn}
###### Definition

The [[free functor]] [[left adjoint]] to this forgetful functor is the  the **free operad functor**

$$
  F : V Coll \stackrel{\leftarrow}{\to} V Operad : U
  \,.
$$

For $C$ a given collection, we call $F(C)$ the operad _free on the collection $C$_.

=--

+-- {: .num_remark}
###### Remark

This free/forgetful [[adjunction]] is used to define the [[model structure on operads]] by [[transferred model structure|transfer]].

=--

## Properties

### Explicit construction

The free operad functor may more explcitly be described as follows (see ([Berger-Moerdijk, section 5.8](#BergerMoerdijk))).

+-- {: .num_defn}
###### Definition

Let $\mathbb{T} := Core(\Omega_pl)$ be the [[core]] of the category of planar rooted [[trees]] and _non-planar_ morphisms (so the morphisms need not respect the given planar structure).

Write

* $t_n \in \Omega_n$ for the $n$-corolla (the tree with a single vertex, $n$ inputs and its unique output root);

* for $T$ any tree with $n$-ary root vertex let $\{T_i\}_{i=1}^n$ be the sub-trees such that $T = t_n \circ (T_1, \cdots, T_n)$.

Then every collection $K \in V Coll$ defines a functor $\bar K : \mathbb{T}^{op} \to V$ by the inductive formula

$$
  \bar K : | \mapsto I
$$

$$
  \bar K : T \mapsto \bar K(t_n(T_1, \cdots, T_n))
  := K(n) \otimes K(T_1) \otimes \cdots K(T_n)
  \,.
$$

Define moreover the functor

$$
  \lambda : \mathbb{T} \to Set
$$

to be the functor that sends a tree to the set of numberings of its leaves, and let $\bar \lambda : \mathbb{T} \to V$ be given by postcomposition with $S \mapsto \coprod_{s \in S} I$, where on the right we have the [[coproduct]] of ${\vert S \vert}$ copies of the tensor unit in the [[monoidal category]] $V$.

=--

So for $T$ a tree with $n$ leaves we have

$$
  \bar \lambda(T) \simeq \coprod_{\sigma \in \Sigma_n} I
  \,,
$$

where the coproduct ranges over the elements of the [[symmetric group]] on $n$ elements.
+-- {: .num_prop}
###### Proposition

The **free operad** on a collection $K$ is isomorphic to the [[coend]]

$$
  \bar K \otimes_{\mathbb{T}} \bar \lambda
  =
  \int^{T \in \mathbb{T}}
   \bar K(T) \otimes \bar \lambda(T)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The groupoid $\mathbb{T}$ is equivalent to the [[disjoint union]] over isomorphism classes of planar trees of the one-object groupoids with morphisms the given [[automorphism group]]

$$
  \mathbb{T} \simeq \coprod_{[T] \in \pi_0\mathbb{T}}
  \mathbf{B} Aut(T)
  \,.
$$

Therefore the above coend is equivalently

$$
  \bar K \otimes_{\mathbb{T}} \bar \lambda
  =
  \coprod_{[T] \in \pi_0\mathbb{T}}
   \bar K(T) \otimes_{Aut(T)} \bar \lambda(T)
  \,.
$$


=--

## Examples

### Rooted tree operad

Let $K$ be the collection with $K(0) = \emptyset$ and $K(n) = I$ for $n \gt 0$. The corresponding free operad has as $n$-ary operations all rooted trees with $n$ leaves. And composition of operations is given by grafting of trees.

## Related concepts

* [[free category]], [[free monoid]]

Riemann surfaces operad (TO BE EXPANDED)

Deligne-Mumford opeard (TO BE EXPANDED)

[[little discs operad]], [[framed little discs operad]] (TO BE EXPANDED) -- See [[Deligne conjecture]]

## References

A brief remark on free operads is in (1.12) of

* [[Ezra Getzler]], [[Mikhail Kapranov]], _Cyclic operads and cyclic homology_, Conf. Proc. Lect. Notes Geom. Topology IV, Int. Press Camb. (1995), 167&#8211;201.
 {#GetzlerKapranov}

A detailed discussion is in Part II, chapter I, section 1.9 of

* [[Martin Markl]], S. Shnider, [[Jim Stasheff]], _Operads in Algebra, Topology and Physics_, Surveys and Monographs of the Amer. Math. Soc. 96 (2002).

and in section 3 of 

* [[Clemens Berger]], [[Ieke Moerdijk]], _The Boardman-Vogt resolution of operads in monoidal model categories_ , Topology 45 (2006), 807&#8211;849. ([pdf](http://math.unice.fr/~cberger/BV.pdf))
{#BergerMoerdijkResolution}

The [[coend]]-description is given in section 5.8 of

* [[Clemens Berger]], [[Ieke Moerdijk]], _Axiomatic homotopy theory for operads_ ([arXiv:0206094](http://arxiv.org/abs/math/0206094v3))
 {#BergerMoerdijk}



[[!redirects collection]]
[[!redirects collections]]

[[!redirects free operads]]
