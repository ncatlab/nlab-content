
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

Higher gometry subsumes notably the theory of [[orbifolds]] and [[geometric stacks]], as well as the theory of more general [[stacks]] such as [[moduli stacks]], and generalizes all this to [[∞-stacks]] and [[derived stacks]]. 
This way higher geometry includes what is called _[[derived geometry]]_ and it subsumes at least parts of (derived) [[noncommutative geometry]]. Many other phenomena are naturally part of higher geometry, see the list of [Examples](#Examples) below.

Within the context of higher geometry, there are several different (but related) ways of formalizing concepts of [[geometry]] and of [[spaces]] in that geometry. Below in _[Formalization](#Formalizations)_ we discuss some of these axiomatizations, which are built on [[(∞,1)-topos theory]] or [[stable (∞,1)-category|stable (∞,1)-category theory]]. 

The theory of [[(∞,1)-toposes]] can be used to axiomatize geometry in two different directions: in one direction, an [[(∞,1)-topos]] (with some additional [[structured (∞,1)-topos|structure]]) encodes a [[space]] itself; in another direction, a [[space]] is an object of a [[gros topos|gros]] (e.g. [[cohesive (∞,1)-topos|cohesive]]) [[(∞,1)-topos]] of [[∞-stacks]] on some [[(∞,1)-site]]. These two directions come from the difference between [[big and little toposes]]. This also corresponds to the difference between the two definitions of [[scheme]] in [[algebraic geometry]] via [[locally ringed spaces]] and [[functors of points]].
A third type of axiomatization, used in [[derived noncommutative algebraic geometry]], uses [[stable (∞,1)-categories]] to represent spaces. 


## Formalizations
 {#Formalizations}

We discuss three different (but related) formalizations of these ideas.


In

* _[Structured (∞,1)-toposes](#StructuredHigherToposes)_

we disucss the approach of encoding a would-be higher geometric space $X$ by a [[structured (∞,1)-topos]] to be thought of as the [[(∞,1)-topos]] of [[(∞,1)-sheaves]] $(Sh_\infty(X), \mathcal{O}_X)$ of $X$, canonically equipped with a [[structure sheaf]] $\mathcal{O}_X$.


In 

* _[Stable (∞,1)-categories](#StableInfinityCategories)_

we disucss the approach of encoding a would-be higher geometric space $X$ by a [[stable (∞,1)-category]] to be thought of as that of [[quasicoherent (∞,1)-sheaves]] of modules $QCoh_\infty(X)$ of $X$

In 

* _[Cohesive (∞,1)-topos](#CohesiveHigherToposes)_

we discuss the approach of considering one big [[(∞,1)-topos]] $\mathbf{H}$ (with "big"/[[gros topos|gros]] being formalized for instance by [[cohesion]]) such that (some of) its objects are to be regarded as higher geometric spaces.

### Structured (∞,1)-toposes 
 {#StructuredHigherToposes}

Let $\mathcal{G}$ be an [[(∞,1)-category]] whose objects will be viewed as "local models" or "test spaces" for the kind of geometry to be developed. Following [[Jacob Lurie]] (based on the theory of geometry via [[ringed toposes]] by [[Alexander Grothendieck]] and [[Monique Hakim]]), a $\mathcal{G}$-[[structured (∞,1)-topos]] is the data of an [[(∞,1)-topos]] together with a [[structure sheaf]] valued in $\mathcal{G}$. Given an appropriate choice of $\mathcal{G}$, one gets the following hierarchy of generalized spaces this way:

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

See also at _[[homotopical algebraic geometry]]_.


### Stable (∞,1)-categories
 {#StableInfinityCategories}

In [[derived noncommutative algebraic geometry]], one considers a [[space]] to be embodied by an [[idempotent complete (∞,1)-category|idempotent complete]] [[stable (∞,1)-category]], or sometimes an idempotent complete [[pretriangulated dg-category]]. The idea is to think of this as the category of [[quasicoherent sheaves]] on the would-be space.

Since by the [stable Giraud theorem](stable+(infinity%2C1)-category#StabGiraud), any [[presentable (∞,1)-category|presentable]] [[stable (∞,1)-category]] is an accessible left-exact [[localization of an (∞,1)-category|localization]] of the [[stabilization of an (∞,1)-category|stabilization]] of some [[(∞,1)-presheaves|(∞,1)-presheaf topos]], this might be thought of as a direct stable analog of the above story.

But [[quasicoherent sheaves]] of an actual [[scheme]] form even a [[symmetric monoidal category]] -- i.e. [[tensor triangulated category]], [[symmetric monoidal (∞,1)-category]]) $(QCoh(X),\otimes)$. Now, one may regard monoidal stable $\infty$-categories as a [[categorification]] of [[commutative rings]] -- as _[[2-rigs]]_ -- and then there is a categorified concept of [[spectrum of a ring]] for them, see at _[[spectrum of a tensor triangulated category]]_ and _[[prime spectrum of a symmetric monoidal stable (∞,1)-category]]_. Therefore regarding (affine) spaces as being formally dual to symmetric monoidal stable $(\infty,1)$-categories is an $(\infty,2)$-higher version of the basic idea in [[algebraic geometry]] of regarding spaces as formally dual to commutative rings. For more on this perspective see at _[[Bondal-Orlov reconstruction theorem]]_, _[[Tannaka duality for geometric stacks]]_, see also ([Brandenburg 14](2-rig#Brandenburg14)).

However, much of the literature (notably in the context of [[homological mirror symmetry]]) disregards the monoidal structure and developes a higher geometry of spaces foramlly dual to just plain stable monoidal $(\infty,1)$-categories (or their presentations by [[A-infinity categories]] or [[triangulated categories]] etc.)

### Cohesive (∞,1)-toposes
 {#CohesiveHigherToposes}

As above, let $\mathcal{G}$ be an [[(∞,1)-site]] whose objects are to be viewed as "local models" for a geometry. Following [[Bill Lawvere]], one may ask for a set of [[axioms]] on the [[(∞,1)-sheaf (∞,1)-topos]] $Sh_\infty(\mathcal{G})$ that ensure that it is appropriate to view [[(∞,1)-sheaves]] on $\mathcal{G}$ as generalized geometric spaces. One such set of axioms is _[[cohesion]]_.

Given such a "big" [[cohesive (∞,1)-topos]] $\mathbf{H}$ and an object $X \in \mathbf{H}$, one may in turn assign to $X$ a "petit" [[structured (∞,1)-topos]] $Sh_{\mathbf{H}}(X)$ of [[internal sheaves]] over $X$. See at _[[differential cohesion]]_ for how this works. This connects the "gros" perspective back to the "petit" perspective [above](#StructuredHigherToposes).



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

### Connes-style noncommutative geometry
 {#ConnesStyleNoncommutativeGeometry}

The process of forming [[groupoid convolution algebras]] is a [[2-functor]] from suitable [[topological stack|topological]] and [[differentiable stacks]] to [[C*-algebras]] with [[Hilbert bimodules]] between them. Much of [[Connes]]-style [[noncommutative geometry]] turns out to deal with objects in the image of this functor, and to the extent that it does, Connes-style noncommutative geometry may be regarded as being a way of speaking about higher geometry, specifically the [[higher differential geometry]] of [[differentiable stacks]]. 


## Related concepts

[[!include Isbell duality - table]]

For relation to [[physics]] see

* [[higher category theory and physics]]

* [[geometry of physics]] 

## References

An axiomatization of higher geometry of [[little topos|little]] [[(∞,1)-topos]]es is proposed in

* [[Jacob Lurie]], _[[Structured Spaces]]_ .
{#Lurie}

In 

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

{#Lawvere}



an axiomatization of generalized geometry is proposed in terms of 1-[[category theory]]. The evident generalization of this to [[(∞,1)-category theory]] provides an axiomatization for higher geometry. This is discussed at

* [[cohesive (∞,1)-topos]].

[[!redirects higher geometries]]