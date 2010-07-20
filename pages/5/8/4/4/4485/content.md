
#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A [[differentiable map]] $f : X \to Y$ between two [[manifold]]s is called a __submersion__ precisely if its [[differential]] $d f\colon T X \to T Y$ is for every point $x \in X$ a [[surjection]] $d f_x\colon T_x X \to T_{f(x)} Y$.

In terms of coordinates, the map $f$ is a submersion at a point $p\colon X$ if and only if there exists a coordinate chart on $X$ near $p$ and a coordinate chart on $Y$ near $f(p)$ relative to which $f$ is the projection $f(x_1,\ldots,x_n) = (x_1,\ldots,x_m)$.  This definition applies to non-differentiable maps, even between non-differentiable manifolds.


## Properties

While the [[category]] [[Diff]] of (finite dimensional) [[smooth manifold]]s does not have all [[pullback]]s,  the [[pullback]] along a submersion always exists. This is because a submersion is [[transverse maps|transversal]] to every other smooth map into its codomain.

The [[surjection|surjective]] submersions (that is the submersions that are also [[epimorphism]]s in [[Diff]]) are [[regular epimorphism]]s.

Surjective submersions form a singleton [[Grothendieck pretopology]] on [[Diff]], and so may be used in [[internal category|internal]] [[category theory]] when using $Diff$ as the ambient category. They appear notably in the definition of [[Lie groupoid]]s.

[[Ehresmann's theorem]] states that a [[proper morphism|proper]] submersion is a locally trivial [[fibration]].


## Variants

The [[algebraic geometry]] analogue of a submersion is a [[smooth morphism]].

The analogue between arbitrary [[topological spaces]] (not manifolds) is simply an [[open map]]. There is also [[topological submersion]], of which there are two versions.


[[!redirects submersion]]
[[!redirects submersions]]

[[!redirects surjective submersion]]
[[!redirects surjective submersions]]
