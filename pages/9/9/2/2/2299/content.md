
{:bluebox: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

**higher geometry** $\leftarrow$ [[Isbell duality]] $\to$ [[higher algebra]]

***

#Contents#
* table of contents
{:toc}

## Idea

_Higher geometry_ or _homotopical geometry_ is the study of concepts of [[space]] and [[geometry]] in the context of [[higher category theory]] and [[homotopy theory]]. 


+-- {: bluebox}
###### Slogan

higher geometry = [[geometry]] + [[homotopy theory]]/[[higher category theory]]

=--

Higher geometry subsumes notably the theory of [[orbifolds]] and [[geometric stacks]], as well as the theory of more general [[stacks]] such as [[moduli stacks]], and generalizes all this to [[∞-stacks]] and [[derived stacks]]. 
This way higher geometry includes what is called _[[derived geometry]]_ and it subsumes at least parts of (derived) [[noncommutative geometry]]. Many other phenomena are naturally part of higher geometry, see the list of [Examples](#Examples) below.

In any given instance of higher geometry, one starts with a notion of "local models" for the geometry. An _affine space_ will then be a formal dual of such a local model, and a general [[space]] will be formed by "gluing" these affine spaces in some appropriate way. There are two ways of formalizing this idea, coming from [[Alexander Grothendieck]]'s two definitions of [[scheme]] in [[algebraic geometry]] via [[locally ringed spaces]] and [[functors of points]]. Both are built on [[(∞,1)-topos theory]]: in one direction, a [[petit topos|petit]] [[(∞,1)-topos]] (with some additional [[structured (∞,1)-topos|structure]]) encodes a [[space]] itself; in another direction, a [[space]] is an object of a [[gros topos|gros]] [[(∞,1)-topos]] of [[∞-stacks]] on some [[(∞,1)-site]]. We discuss these axiomatizations below in _[Formalization](#Formalizations)_.

These approaches do not apply to [[noncommutative algebraic geometry]], which requires a different approach to deal with a more complicated notion of gluing; we discuss this below in _[Noncommutative algebraic geometry](#NoncommutativeAlgebraicGeometry)_.

## Formalizations
 {#Formalizations}

We discuss two different (but closely related) formalizations of these ideas.

In 

* _[Gros (∞,1)-topos](#GrosHigherToposes)_

we discuss the approach of considering one big [[(∞,1)-topos]] $\mathbf{H}$ (with "big"/[[gros topos|gros]] being formalized for instance by [[cohesion]]) such that (some of) its objects are to be regarded as higher geometric spaces.

In

* _[Petit (∞,1)-toposes](#PetitHigherToposes)_

we discuss the approach of encoding a would-be higher geometric space $X$ by a [[structured (∞,1)-topos]] to be thought of as the [[petit topos|petit]] [[(∞,1)-topos]] of [[(∞,1)-sheaves]] $(Sh_\infty(X), \mathcal{O}_X)$ of $X$, canonically equipped with a [[structure sheaf]] $\mathcal{O}_X$.


### Gros (∞,1)-toposes
 {#GrosHigherToposes}

Let $\mathcal{G}$ be an [[(∞,1)-site]] whose objects are to be viewed as "local models" or "test spaces" for a geometry. Within the context of this geometry, we make the following definitions:

An **affine space** is a formal dual of an object of $\mathcal{G}$, so that the (∞,1)-category of affine spaces is the [[opposite (∞,1)-category|opposite]] of $\mathcal{G}$. A **stack** is an [[∞-stack]] on $\mathcal{G}$, so that the (∞,1)-category of stacks is the [[gros topos|gros]] [[(∞,1)-sheaf (∞,1)-topos]] on $\mathcal{G}$. Finally, a **space** is a [[stack]] $X$ that has a cover by a family of affine spaces $(f_i : U_i \to X)_i$, where each $f_i$ belongs to some nice class of morphisms (e.g. [[open immersions]], [[etale morphisms]] or [[smooth morphisms]]).

When the underlying (∞,1)-category of $\mathcal{G}$ is the (∞,1)-category of [[commutative algebras in a symmetric monoidal (∞,1)-category]], this is known as _[[homotopical algebraic geometry]]_. When it is the (∞,1)-category of [[algebras over a Lawvere theory]], this is discussed at [[derived geometry]].

Following [[Bill Lawvere]], one may ask for a set of [[axioms]] on the [[(∞,1)-sheaf (∞,1)-topos]] $Sh_\infty(\mathcal{G})$ that ensure that it is appropriate to view [[(∞,1)-sheaves]] on $\mathcal{G}$ as generalized geometric spaces. One such set of axioms is _[[cohesion]]_.

### Petit (∞,1)-toposes
 {#PetitHigherToposes}

As above, let $\mathcal{G}$ be an [[(∞,1)-category]] whose objects will be viewed as "local models" for the kind of geometry to be developed. Following [[Jacob Lurie]] (based on the theory of geometry via [[ringed toposes]] by [[Alexander Grothendieck]] and [[Monique Hakim]]), a $\mathcal{G}$-[[structured (∞,1)-topos]] is the data of an [[(∞,1)-topos]] together with a [[structure sheaf]] valued in $\mathcal{G}$. Given an appropriate choice of $\mathcal{G}$, one gets the following hierarchy of generalized spaces this way:

* [[geometry (for structured (∞,1)-toposes)|test spaces]] $\hookrightarrow$
  [[generalized scheme|spaces locally equivalent to test spaces]]
  $\hookrightarrow$
  [[structured (∞,1)-topos|concrete spaces with structure sheaves taking values in test spaces]]
  $\hookrightarrow$
  [[∞-stack|spaces probeable by test spaces]].

technically modeled by:

* [[geometry (for structured (∞,1)-toposes)]] $\mathcal{G}$
  $\hookrightarrow$

  [[generalized scheme]]s
  $\hookrightarrow$
  formal duals to $\mathcal{G}$-[[structured (∞,1)-topos]]es
  $\hookrightarrow$
  [[(∞,1)-topos]] of [[∞-stack]]s on $\mathcal{G}$.

A plethora of proposals for formalizations of higher geometry find their home in this pattern, for instance most of the concepts listed at [[generalized smooth space]].

## Relation between these approaches

Given a gros [[cohesive (∞,1)-topos]] $\mathbf{H}$ and an object $X \in \mathbf{H}$, one may in turn assign to $X$ a petit [[structured (∞,1)-topos]] $Sh_{\mathbf{H}}(X)$ of [[internal sheaves]] over $X$. See at _[[differential cohesion]]_ for how this works. This connects the "gros" perspective back to the "petit" perspective.

Conversely, given a [[structured (∞,1)-topos]] one may consider its associated [[functor of points]], which will be an object in the [[gros topos|gros]] [[(∞,1)-topos]].

## Examples
 {#Examples}

### List of examples

* [[homotopical algebraic geometry]]

  * [[derived algebraic geometry]]

  * [[étale (∞,1)-site]], [[dg-geometry]], [[Hochschild cohomology]] of [[dg-algebra]]s

  * [[schematic homotopy type]]

* [[derived noncommutative geometry]]

  * [[noncommutative geometry]]

* [[higher differential geometry]]

  * [[motivation for higher differential geometry]]

  * [[differential geometry]], [[differential topology]]

  * [[derived smooth manifold]]

  * [[smooth ∞-groupoid]], [[∞-Lie algebroid]]

* [[higher symplectic geometry]]

* [[higher complex analytic geometry]]

* [[higher prequantum geometry]]

* [[higher Klein geometry]]

* [[higher Cartan geometry]]

### Noncommutative algebraic geometry
 {#NoncommutativeAlgebraicGeometry}

The above frameworks for higher geometry are not suitable for describing [[noncommutative algebraic geometry]], because of the more complicated notions of [[localization]], gluing and [[descent]] in the latter setting. Indeed, noncommutative spaces are supposed to be obtained from affine ones (formal duals of [[associative algebras]] or [[dg-algebras]]) by gluing along _[[bimodules]]_. A good setting for such gluing is that of [[pretriangulated dg-categories]] (or [[stable (∞,1)-categories]]). Thus in [[derived noncommutative algebraic geometry]], a noncommutative space is defined to be a [[stable (∞,1)-category]].

### Connes-style noncommutative geometry
 {#ConnesStyleNoncommutativeGeometry}

The process of forming [[groupoid convolution algebras]] is a [[2-functor]] from suitable [[topological stack|topological]] and [[differentiable stacks]] to [[C*-algebras]] with [[Hilbert bimodules]] between them. Much of [[Connes]]-style [[noncommutative geometry]] turns out to deal with objects in the image of this functor, and to the extent that it does, Connes-style noncommutative geometry may be regarded as being a way of speaking about higher geometry, specifically the [[higher differential geometry]] of [[differentiable stacks]]. 

## Related concepts

* [[higher structures]]

* [[higher differential geometry]]

[[!include Isbell duality - table]]

For relation to [[physics]] see

* [[higher category theory and physics]]

* [[geometry of physics]] 

## References
{#Lurie}

Both approaches to higher geometry are described, in the special case of [[derived algebraic geometry]], in

* [[Jacob Lurie]], _[[Derived Algebraic Geometry]]_, Ph.D. thesis.

The gros topos approach is described, in the case of [[homotopical algebraic geometry]], in


* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical algebraic geometry II: geometric stacks and applications_, 2004, [arXiv:math/0404373](http://arxiv.org/abs/math/0404373).

A general exposition of the petit topos approach is proposed in

* [[Jacob Lurie]], _[[Structured Spaces]]_ .
{#Lurie}

In 

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

{#Lawvere}



an axiomatization of generalized geometry is proposed in terms of 1-[[category theory]]. The evident generalization of this to [[(∞,1)-category theory]] provides an axiomatization for higher geometry. This is discussed at

* [[cohesive (∞,1)-topos]].

[[!redirects higher geometries]]