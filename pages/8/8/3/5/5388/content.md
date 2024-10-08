
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The _Lorentz group_ is the [[orthogonal group]] for an invariant [[bilinear form]] of [[signature of a quadratic form|signature]] $(-+++\cdots)$, $O(d-1,1)$.  

In [[physics]], in the [[theory (physics)|theory]] of _[[relativity]]_ the Lorentz group [[action|acts]] canonically as the group of linear [[isometries]] of [[Minkowski spacetime]] preserving a chosen basepoint. This is called the action by _Lorentz transformations_.

The elements in the Lorentz group in the image of the [[special orthogonal group]] $SO(d-1) \hookrightarrow O(d-1,1)$ are _[[rotations]]_ in space. The further elements in the special Lorentz group $SO(d-1,1)$, which mathematically are "hyperbolic rotations" in a space-time plane, are called _[[boost|boosts]]_ in [[physics]].

One distinguishes the following further [[subgroups]] of the [[Lorentz group]] $O(d-1,1)$:

* the _proper Lorentz group_ $SO(d-1,1)$ is the subgroup of elements which have [[determinant]] +1 (as elements  $SO(d-1,1)\hookrightarrow GL(d)$ of the [[general linear group]]);

* the _proper orthochronous_ (or _restricted_) Lorentz group $SO^+(d-1,1) \hookrightarrow SO(d-1,1)$ is the further [[subgroup]] of elements which do not act by [[reflection]] along the [[timelike]] axis. 

## Properties

### Connected components
 {#ConnectedComponents}

As a [[smooth manifold]], the Lorentz group $O(3,1)$ has four [[connected components]]. The connected component of the identity is the the proper orthochronous group $SO^+(3,1)$. The other three components are

1. $SO^+(3,1)\cdot P$

1. $SO^+(3,1)\cdot T$

1. $SO^+(3,1)\cdot P T$,

where, as [[matrices]]

$$
  P \coloneqq diag(1,-1,-1, \cdots, -1) 
$$

is the operation of point reflection at the origin in space,  where

$$
  T \coloneqq diag(-1,1,1, \cdots, 1)
$$

is the operation of reflection in time and hence where

$$
  P T = T P = diag(-1,-1, \cdots, -1)
$$

is point reflection in spacetime.

### Spin cover
 {#SpinCover}

While the proper orthochronous Lorentz group $SO^+(d-1,1)$ is [[connected topological space|connected]], it is not [[simply connected]]. Its [[universal covering space|universal]] [[double cover]] is the Lorentzian [[spin group]] $Spin(d-1,1)$.


## Related concepts

* [[Lorentz Lie algebra]]

* [[quantum group]] version: [[quantum Lorentz group]]

* [[Lorentzian manifold]]

* [[rapidity]]

* [[Galilean group]]

* [[Minkowski spacetime]]

* [[de Sitter spacetime]]

* [[anti de Sitter spacetime]]

[[!include table of orthogonal groups and related]] 

## References

Named after [[Hendrik Lorentz]]. (Not to be confused with [[Ludvik Lorenz]], whose name is attached to the [[Lorenz gauge]].)

* Wikipedia, _[Lorentz group](https://en.wikipedia.org/wiki/Lorentz_group)_

[[!redirects Lorentz groups]]

[[!redirects Lorentz transformation]]
[[!redirects Lorentz transformations]]

[[!redirects proper Lorentz group]]
[[!redirects proper Lorentz groups]]

[[!redirects proper orthochronous Lorentz group]]
[[!redirects proper orthochronous Lorentz groups]]

