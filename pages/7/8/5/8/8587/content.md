# Kriegl and Michor's Cartesian Closed Category of Smooth Manifolds # {: #title}

+-- {: .num_section #sectiona }
=--
## Introduction ## {: .num_section}

In [MR764972](#MR764972) and [MR767683](MR767683), Michor gives a description of a category of "smooth manifolds" due to himself and Kriegl which is [[cartesian closed]]. The key to achieving this is to replace charts and atlases by notions based on smooth curves. The resulting objects have a considerable amount of structure built in, but nonetheless replicate ordinary smooth manifolds in the finite dimensional situation.


+-- {: .num_section #sectionb }
=--
## Definition ## {: .num_section}

The final data of a "smooth manifold" is the following:

1. Two sets, $M$ and $T M$, and a mapping $\pi _{M} \colon T M \to M$ such that each fibre is a [[locally convex space]] of a certain type.

1. A set $\mathcal{S} (\mathbb{R},M)$ of curves in $M$, closed under $C^\infty$--reparametrisations and containing all constants.

1. For each $t \in \mathbb{R} $, a mapping $\delta _{t} \colon \mathcal{S} (\mathbb{R},M) \to T M$ such that:

   1. $\pi _{M} \circ \delta _{t} = \ev_{t}$,

   1. $\delta _{t} (c \circ f) = f'(t) \delta _{f(t)} c$,

   1. $c$ is constant if for all $t$ then $\delta _{t} c = 0$.

1. A mapping $\Pt^{T M} = \Pt\colon \mathcal{S} (\mathbb{R},M) \times \mathbb{R} \to \mathcal{L} (T M, T M)$ such that:

   1. $\Pt(c,t) \colon T_{c(0)} M \to T_{c(t)} M$ is linear and continuous,

   1. $\Pt(c,0) = \Id$,

   1. $\Pt(c,f(t)) = Pt(c \circ f,t) \Pt(c,f(0))$.

1. $t \mapsto \Pt(c,t)^{-1} (\delta _{t} c)$ is a $C^\infty$--curve in the locally convex space $T_{c(0)} M$.

1. A mapping $\Geo^{M} = \Geo\colon T M \to \mathcal{S} (\mathbb{R},M)$ such that:

   1. $\Geo(t \cdot v)(s) = \Geo(v)(t s)$,

   1. $\delta _{t}( \Geov) = \Pt(\Geo(v),t) \cdot v$,

   1. $\Geo(\delta _{t} \Geo(v))(s) = \Geo(v)(t + s)$.

1. $\Pt\colon \mathcal{S} (\mathbb{R},M) \times \mathbb{R} \to L(T M, T M)$ is smooth.

1. $\Geo\colon T M \to \mathcal{S} (\mathbb{R},M)$ is smooth.

There is a notion of a *smooth map* between such objects (and in which the last two conditions must be interpreted). The resulting category is cartesian closed.

## References ##

* {: #MR764972 } Michor, P. (1984). A convenient setting for differential geometry and global analysis. _Cahiers Topologie G&#233;om. Diff&#233;rentielle_, _25_, 63&#8211;109.

* {: #MR767683 } Michor, P. (1984). A convenient setting for differential geometry and global analysis. {II}. _Cahiers Topologie G&#233;om. Diff&#233;rentielle_, _25_, 113&#8211;178.


