# Kriegl and Michor's Cartesian Closed Category of Smooth Manifolds # {: #title}

+-- {: .num_section #sectiona }
=--
## Introduction ## {: .num_section}

In ([Michor 1984a](#MR764972)) and ([Michor 1984b](#MR767683)), Michor gives a description of a category of "smooth manifolds" due to himself and Kriegl which is [[cartesian closed]]. The key to achieving this is to replace charts and atlases by notions based on smooth curves. The resulting objects have a considerable amount of structure built in, but nonetheless replicate ordinary smooth manifolds in the finite dimensional situation. This is also true in the Banach space situation; it is not stated in the paper, but easy to generalize from the finite dimensional situation.


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

+-- {: .num_section #sectionc }
=--
## In Details ## {: .num_section}

The actual definition is built up in stages. The first definition given is that of a *pre-manifold*. This consists of the first six conditions in the above, to wit:

+-- {: .num_defn #defna .thdefn }
###### Definition ######
A *pre-manifold* consists of the following data.

&#160;

1. Two sets, $M$ and $T M$, and a mapping $\pi _{M} \colon T M \to M$ such that each fibre is a [[locally convex space]] of a certain type.

1. A set $\mathcal{S} (\mathbb{R},M)$ of curves in $M$, closed under $C^{\infty } $--reparametrisations and containing all constants.

1. For each $t \in \mathbb{R} $, a mapping $\delta _{t} \colon \mathcal{S} (\mathbb{R},M) \to T M$ such that: &#160;

   1. $\pi _{M} \circ \delta _{t} = \ev_{t}$,

   1. $\delta _{t} (c \circ f) = f'(t) \delta _{f(t)} c$,

   1. $c$ is constant if for all $t$ then $\delta _{t} c = 0$.

1. A mapping $\Pt^{T M} = \Pt\colon \mathcal{S} (\mathbb{R},M) \times \mathbb{R} \to \mathcal{L} (T M, T M)$ such that: &#160;

   1. $\Pt(c,t) \colon T_{c(0)} M \to T_{c(t)} M$ is linear and continuous,

   1. $\Pt(c,0) = \Id$,

   1. $\Pt(c,f(t)) = Pt(c \circ f,t) \Pt(c,f(0))$.

1. $t \mapsto \Pt(c,t)^{-1} (\delta _{t} c)$ is a $C^{\infty } $--curve in the locally convex space $T_{c(0)} M$.

1. A mapping $\Geo^{M} = \Geo\colon T M \to \mathcal{S} (\mathbb{R},M)$ such that: &#160;

   1. $\Geo(t \cdot v)(s) = \Geo(v)(t s)$,

   1. $\delta _{t}( \Geov) = \Pt(\Geo(v),t) \cdot v$,

   1. $\Geo(\delta _{t} \Geo(v))(s) = \Geo(v)(t + s)$.
=--

There is an auxiliary concept of a *pre-vector bundle* over a pre-manifold which is also introduced. A pre-manifold defines a pre-vector bundle in a natural way, modelling the fact that the tangent bundle of an ordinary manifold is a vector bundle. The initial reason for introducing pre-vector bundles is that it can be shown that the total space of a pre-vector bundle is again a pre-manifold, and thus if $M$ is a pre-manifold then we can define an associated pre-manifold $T M$ and so on.

The next important concept is that of a *smooth map*, and this leads to a category of pre-manifolds. In fact, two definitions of morphisms between pre-manifolds are given in the two papers. The main one is that of a smooth map. The second, called $S^{1}$ in the papers, is a truncated version.

+-- {: .num_defn #defnb .thdefn }
###### Definition ######
Let $M$ and $N$ be pre-manifolds. A set map $f \colon M \to N$ is smooth if there is a sequence of maps $T^{n} f \colon T^{n} M \to T^{n} N$ with the property that for each $n$, $(T^{n} f)_{*} \colon \mathcal{S} (\mathbb{R},M) \to \mathcal{S} (\mathbb{R},N)$ makes sense and satisfies $(T^{n} f)_{*} \delta _{0} = \delta _{0} (T^{n-1} f)_{*}$.
=--

An $S^{1}$ map is simply a map $f \colon M \to N$ for which $f_{*} \colon \mathcal{S} (\mathbb{R},M) \to \mathcal{S} (\mathbb{R},N)$ is defined.

+-- {: .num_section #sectiond }
=--
## Relationship to Other Theories ## {: .num_section}

Underneath the structure of a pre-manifold is a notion of a [[generalised smooth space|generalized smooth space]] which fits in with the scheme defined in ([Stacey 2011](#MR2805746)). It is formed by taking the category of test spaces to be the one-object category associated to the monoid $C^{\infty } (\mathbb{R},\mathbb{R})$, the underlying category to be $\Set$, the input forcing condition is the input terminal condition (all constant maps are smooth), and the output forcing condition is saturation (whence output functions can be safely ignored).

+-- {: .num_defn #defnc .thdefn }
###### Definition ######
Let $\mathcal{KM} $ be the category of generalised smooth spaces so described.
=--

The input forcing condition is extremely weak. This means that it sits far to the left in the diagram at [[generalised smooth spaces|generalized smooth spaces]]. However, the fact that the category of test objects is extremely small means that there is less potential for variation than with those categories where the test category is somewhat larger.

In the literature, Chen's first (1973) definition comes closest to this in terms of forcing condition but the category of [[Frölicher spaces]] is closest in terms of underlying category and test category.

There is an inclusion functor $\mathcal{Fr} \to \mathcal{KM} $ and this has a left adjoint which is found by saturating the smooth curves with respect to the smooth functions to $\mathbb{R} $.

For [[Chen spaces]] and [[diffeological spaces]], the story is similar. Each category has a functor to $\mathcal{KM} $ but it is no longer an inclusion (for example, $\mathbb{R} ^{2}$ with the standard diffeology and with the wire diffeology give the same object in $\mathcal{KM} $). These functors have left adjoints where a plot is smooth if it locally factors through one of the original smooth curves. Note that this means that for $\mathbb{R} ^{2}$ we recover the wire diffeology and not the standard one.


## References ##

* {: #MR764972 } P. Michor, (1984). A convenient setting for differential geometry and global analysis. _Cahiers Topologie G&#233;om. Diff&#233;rentielle_, _25_, 63&#8211;109.

* {: #MR767683 } P. Michor, (1984). A convenient setting for differential geometry and global analysis. II. _Cahiers Topologie G&#233;om. Diff&#233;rentielle_, _25_, 113&#8211;178.

* Andreas Kriegl, [[Peter Michor]], [[The Convenient Setting of Global Analysis]], Mathematical Surveys and Monographs, 53 AMS (1997) [pdf](http://www.mat.univie.ac.at/~michor/apbookh-ams.pdf)

* {: #MR2805746 } Stacey, A. (2011). Comparative smootheology. _Theory Appl. Categ._, _25_, No. 4, 64&#8211;117.