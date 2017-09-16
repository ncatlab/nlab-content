

#Idea#

Following the logic described at

* [[space and quantity]]

  * [[generalized smooth space]]

* [[motivation for sheaves, cohomology and higher stacks]]

* [[(∞,1)-topos]]

a _smooth $\infty$-stack_ is the [[∞-categorification]] of [[smooth space]] and [[differentiable stack]]. It is
an [[∞-stack]] on (a small version of) the [[site]] [[Diff]] of smooth [[manifold]], or correspondingly on $Balls \subset Diff$ or $CartesianSpaces \subset Diff$ (see [[smooth space]] for more on that).

So smooth $\infty$-stacks are the objects in the [[(∞,1)-topos]] that computes _smooth_ generalized [[cohomology]]. (See [[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]] and the disucssion under "Models" below for more on that).

# Definition #

Let $CartesianSpaces = \{ (\mathbb{R}^n \to \mathbb{R}^m) \in Diff| n,m \in \mathbb{N}\} \subset Diff$ be the full subcategory of [[Diff]] on the [[manifold]]s of the simple form $\mathbb{R}^n$, equipped with the standard structure of a [[site]] with the [[coverage]] given by open covers of manifolds.

Then

$$
  \mathbf{H}_{Diff} := (\infty,1)Sh(CartesianSpaces)
$$

is the [[(∞,1)-topos]] given by the [[(∞,1)-category of (∞,1)-sheaves]] on $CartesianSpaces$.


# Models #

There is a large number of [[model category|model structures]] [[presentable (infinity,1)-category|presenting]] $\mathbf{H}_{Diff}$: all the [[model structure on simplicial presheaves|model structures on simplicial (pre)sheaves]] on $CartesianSpaces$.


## In terms of $\infty$-groupoids internal to smooth spaces ##

Notice for instance that there is the [[model structure on simplicial sheaves]] given by the category $SSh(CartesianSpaces)$ equipped with the injective [[local model structure on simplicial presheaves]].

But sheaves on cartesian spaces

$$
  Sh(CartesianSpaces)
  =: SmoothSpaces
$$

is the category of [[smooth spaces]], and $SSh(CartesianSpaces)$ is just the category of [[simplicial objects]] of that

$$
  SSh(CartesialSpaces) 
  \simeq
  SmoothSpaces^{\Delta^{op}}
  \,.
$$

So one model for smooth $\infty$-stacks is given by [[simplicial object|simplicial]] [[smooth spaces]].

Notice that the fibrant object in $SmoothSpaces^{\Delta^{op}}$ are the globally [[Kan complex]] valued sheaves under the [[equivalence of categories]]

$$
  SmoothSpaces^{\Delta^{op}}
  \simeq
  Sh(CartesianSpaces, SSet)
  \,,
$$

that satisfy [[descent]] (see [[descent for simplicial presheaves]]).

Being [[Kan complex]]-valued just means that the fibrant objects are sheaves on $CartesianSpaces$ with values in [[∞-groupoids]].

Moreover, the [[descent]]-condition on $CartesianSpaces$ is comparatively trivial, and in many cases (...details eventually here, but see examples below...) entirely empty, as every cartesian space is (smoothly, even) contractible. 

This means that the fibrant objects in $SSh(CartesianSpaces)$ are pretty much nothing but [[∞-groupoids]] [[internalization|internal to]] [[smooth space]]s. (But notice that the requirement that she corresponding sheaf is [[Kan complex]]-valued is a bit weaker that other notions of "$\infty$-groupoid internal to smooth spaces" that one may come up with).

In particular [[∞-groupoids]] internal to [[diffeological spaces]] are therefore a model for smooth $\infty$-stacks.

Moreover, a morphism between smooth $\infty$-stacks modeled by such internal $\infty$-groupoids is modeled as an $\infty$-[[anafunctor]] (see [[simplicial localization]], [[homotopy category]] and [[category of fibrant objects]] for details).

The model of smooth $\infty$-stacks given by $\infty$-groupoids internal to [[diffeological space]]s with [[anafunctor]]s as morphism between them is the model used in the [[John Baez|Baez]]-ian school description of 
[[principal infinity-bundle|higher principal bundles]] and
[[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]].

### Examples ###

Let $G$ be a [[Lie group]]. Using the embedding

$$
  Diff \hookrightarrow SmoothSpaces
$$

of [[manifolds]] into [[smooth spaces]] we may regard
$G$ naturally as a sheaf on CartesianSpaces.

Write $\mathbf{B} G$ for the [[delooping]] of $G$, a one-object [[groupoid]] [[internalization|internal to]] [[smooth space|SmoothSpaces]]. Postcomposing with the [[nerve]] functor $N : $ [[Grpd]] $\to$ [[SSet]] this yields a [[Kan complex]]-valued [[simplicial presheaf|simplicial sheaf]] $N \mathbf{B} G$ which we shall by convenient and useful abuse of notation just call $\mathbf{B} G$ itself.

Notice that $\mathbf{B} G$ does not satisfy [[descent]] when regarded as a simplicial sheaf on all of [[Diff]]: there its [[∞-stackification]] is instead $G Bund(-)$, the [[stack]] of $G$-[[principal bundle]]s 

$$
  G Bund(-) : U \mapsto groupoid of G-bundles on U
$$

(or rather, in our context of simplicial sheaves, a [[rectified infinity-stack|rectification]] of that).

But restricted to the [[site]] $CartesianSpace$ the [[simplicial presheaf|simplicial sheaf]] $\mathbf{B} G$ _does_ satisfy [[descent]]: there is up to isomorphism only a single $G$-bundle on $\mathbb{R}^n$, so that one finds an [[equivalence of categories]]

$$
  G Bund(\mathbb{R}^n) \simeq (\mathbf{B} G)(\mathbb{R}^n)
  := \mathbf{B}(Diff(\mathbb{R}^n,  G))
$$

for each $\mathbb{R}^n$. This means that  $\mathbf{B}G$ is a fibrant object in the injective [[model structure on simplicial sheaves]]. 
So in particular all the constructions and examples discussed at [[category of fibrant objects]] apply to $\mathbf{B}G$: we get the [[generalized universal bundle|universal G-bundle]] $\mathbf{E} G \to \mathbf{B}G$ regarded as a smooth $\infty$-stack as the [[pullback]]

$$
  \array{
    \mathbf{E}G &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G &\stackrel{d_0}{\to}& \mathbf{B}G
    \\
    \downarrow^{d_1}
    \\
    \mathbf{B}G
  }
$$

in $SmoothSpaces^{\Delta^{op}}$, which, do to the [[nerve]] being [[right adjoint]] is the same as the image under the nerve of the corresponding [[pullback]] in sheaves of [[groupoid]]s (so that still our notational suppressing of $N$ is justified).

etc. 

[[!redirects smooth infinity-stacks]]
[[!redirects smooth ∞-stack]]
[[!redirects smooth ∞-stacks]]