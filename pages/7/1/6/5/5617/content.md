
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Riemannian geometry
+-- {: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The _volume form_ on a finite-[[dimension|dimensional]] [[orientation|oriented]] (pseudo)-[[Riemannian manifold]] $(X,g)$ is the [[differential form]] whose [[integral]] over pieces of $X$ computes the [[volume]] of $X$ as measured by the [[metric]] $g$.

If the manifold is unoriented, then we get a _volume [[pseudoform]]_ instead, or equivalently a volume [[density]] (of weight $1$).  We can also consider volume (pseudo)-forms in the absence of a metric, in which case we have a choice of volume forms.


## Definition

### General

For $X$ a general [[smooth manifold]] of finite [[dimension]] $n$, a __volume form__ on $X$ is a nondegenerate (nowhere vanishing) differential $n$-[[differential form|form]] on $X$, equivalently a nondegenerate [[section]] of the [[canonical line bundle]] on $X$.  A __volume pseudoform__ or __volume element__ on $X$ is a positive definite [[density]] (of rank $1$) on $X$, or equivalently a positive definite differential $n$-[[pseudoform]] on $X$.

A volume form defines an [[orientation]] on $X$, the one relative to which it is positive definite.  If $X$ is already oriented, then we require the orientations to agree (to have a volume form on $X$ qua oriented manifold); that is, a volume form on an oriented manifold must be positive definite (just as a volume pseudoform on any manifold must be).  In this situation, there is essentially no difference between a form and a pseudoform, hence no difference between a volume form and a volume pseudoform or volume element.


### For Riemannian manifolds

More specifically, for $(X,g)$ a (pseudo)-[[Riemannian manifold]] of [[dimension]] $n$, *the* __volume pseudoform__ or __volume element__ $vol_g$ is a specific differential $n$-[[pseudoform]] that measures the volume as seen by the metric $g$.  If $X$ is [[orientation|oriented]], then we may interpret $vol_g \in \Omega^n(X)$ as a differential $n$-form, also denoted $vol_g$.

This $vol_g$ is characterized by any of the following equivalent statements:

* The symmetric square $vol_g \cdot vol_g$ is equal to the $n$-fold [[wedge product]] $g \wedge \cdots \wedge g$, as elements of $\Omega^n(X) \otimes \Omega^n(X)$, and $vol_g$ is [[positive n-form|positive]] (meaning that its [[integral]] on any [[open submanifold]] is nonnegative).

* The volume form is the image under the [[Hodge star]] operator $\star_g\colon \Omega^k(X) \to \Omega^{n-k}(X)$ of the [[smooth function]] $1 \in \Omega^0(X)$

  $$
    vol_g = \star_g 1
    \,.
  $$

* In local oriented coordinates, $vol_g = \sqrt{|det(g)|}$, where $det(g)$ is the [[determinant]] of the [[matrix]] of the coordinates of $g$.  In the case of a Riemannian (not pseudo-Riemannian) metric, this simplifies to $vol_g = \sqrt{\det(g)}$.  (Note that local coordinates for a pseudoform include a local orientation, so this makes sense regardless of whether $X$ is oriented.)

* For $(E, \Omega)\colon T X \to iso(n)$ the [[Lie algebra valued differential form]] on $X$ with values in the [[Poincare Lie algebra]] $iso(n)$ that encodes the metric and orientation (the _[[spin connection]]_ $\Omega$ with the _[[vielbein]]_ $E$), the volume form is the image of $(E,\Omega)$ under the canonical volume [[Lie algebra cohomology|Lie algebra cocycle]] $vol \in CE(iso(n))$:

  $$
    vol_g = vol(E)
    \,.
  $$

  See [[Poincare Lie algebra]] for more on this.


### Degenerate cases

If we allow a volume (pseudo)form to be degenerate, then most of this goes through unchanged.  In particular, a degenerate (pseudo)-[[Riemannian metric]] defines a degenerate volume pseudoform (and hence a degenerate volume form on an oriented manifold).

However, a degenerate $n$-form $\omega$ does not specify an orientation in general, so there is not necessarily a good notion of volume form on an unoriented manifold.  On the other hand, if the open submanifold on which $\omega \ne 0$ is [[dense subspace|dense]], then there is at most one compatible orientation, although there still may be none.  Of course, on an oriented manifold, forms are equivalent to pseudoforms, so we still know what a degenerate volume form is there.

To remove the requirement of positivity is much more drastic; an arbitrary $n$-pseudoform is simply a $1$-[[density]] (and an arbitrary $n$-form is a $1$-pseudodensity).  This is at best a notion of *signed* volume, rather than volume.


## Properties

Since an $n$-(pseudo)form is [[positive n-form|positive]] iff its [[integration of differential forms|integral]] on any [[open submanifold]] is nonnegative and nondegenerate iff its integral on sufficiently small [[inhabited subspace|inhabited]] open submanifolds is nonzero, a volume (pseudo)form may be defined as one whose integral on any inhabited open submanifold is (strictly) positive.

A volume (pseudo)form is also equivalent to an [[absolutely continuous measure|absolutely continuous]] positive [[Radon measure]] on $X$.  Here, nondegeneracy corresponds precisely to absolute continuity.

If I remember correctly, every volume (pseudo)form comes from a metric, which is unique iff $n \leq 1$.


## Related concepts

* [[density]]

* [[divergence]]


[[!redirects volume form]]
[[!redirects volume forms]]
[[!redirects volume pseudoform]]
[[!redirects volume pseudoforms]]
[[!redirects volume element]]
[[!redirects volume elements]]
