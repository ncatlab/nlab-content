
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

_Higher geometry_ or _homotopical geometry_ is the study of the notions of [[space]] and [[geometry]] in the context of [[higher category theory]] and [[homotopy theory]].

Within higher geometry, there are several possible axiomatizations of the notion of [[geometry]] and of [[spaces]] in that geometry. In this entry we discuss some of these axiomatizations, which are built on [[(∞,1)-topos theory]] or [[stable (∞,1)-category|stable (∞,1)-category theory]]. 

The theory of [[(∞,1)-toposes]] can be used to axiomatize geometry in two different directions: in one direction, an [[(∞,1)-topos]] (with some additional [[structured (∞,1)-topos|structure]]) encodes a [[space]] itself; in another direction, a [[space]] is an object of a ([[cohesive (∞,1)-topos|cohesive]]) [[(∞,1)-topos]] of [[∞-stacks]] on some [[(∞,1)-site]]. These two directions come from the difference between [[big and little topos]]es. This also corresponds to the difference between the two definitions of [[scheme]] in [[algebraic geometry]] via [[locally ringed spaces]] and [[functors of points]].

A third type of axiomatization, used in [[derived noncommutative algebraic geometry]], uses [[stable (∞,1)-categories]] to represent spaces. 

Under forming [[groupoid convolution algebras]] and their higher analog, at least parts of higher geometry translate to [[noncommutative geometry]].

## Axiomatizations

### Structured (∞,1)-toposes

Let $\mathcal{G}$ be an [[(∞,1)-category]] whose objects will be viewed as "local models" or "test spaces" for the geometry to be developed. Following [[Jacob Lurie]], a $\mathcal{G}$-[[structured (∞,1)-topos]] is the data of an [[(∞,1)-topos]] together with a [[structure sheaf]] valued in $\mathcal{G}$. Given an appropriate choice of $\mathcal{G}$, one gets the following hierarchy of generalized spaces:

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

### Cohesive (∞,1)-toposes

As above, let $\mathcal{G}$ be an [[(∞,1)-site]] whose objects are to be viewed as "local models" for a geometry. Following [[Bill Lawvere]], one can give a set of axioms that capture when it is appropriate to view [[(∞,1)-sheaves]] on $\mathcal{G}$ as generalized geometric spaces. This leads to the notion of [[cohesive (∞,1)-topos]].

Given such a [[cohesive (∞,1)-topos]], one may go further and try to identify even more refined geometric objects within it. For thus, it is necessary to endow $\mathcal{G}$ with some additional structure: namely, that of a collection of [[morphisms]] that dictate how the generalized spaces can be formed from the local models by gluing. This leads to the notion of a [[homotopical algebraic geometry]] context, following [[Bertrand Toen]] and [[Gabriele Vezzosi]].

### Stable (∞,1)-categories

In [[derived noncommutative algebraic geometry]], a [[space]] is an [[idempotent complete (∞,1)-category|idempotent complete]] [[stable (∞,1)-category]], or sometimes an idempotent complete [[pretriangulated dg-category]].

Note that, since by the <a href="http://ncatlab.org/nlab/show/stable+(infinity%2C1)-category#StabGiraud">stable Giraud theorem</a>, any [[presentable (∞,1)-category|presentable]] [[stable (∞,1)-category]] is an accessible left-exact [[localization of an (∞,1)-category|localization]] of the [[stabilization of an (∞,1)-category|stabilization]] of some [[(∞,1)-presheaves|(∞,1)-presheaf topos]], this story is, roughly speaking, a stable version of the story above.

## Examples

* [[homotopical algebraic geometry]]

  * [[derived algebraic geometry]]

  * [[étale (∞,1)-site]], [[dg-geometry]], [[Hochschild cohomology]] of [[dg-algebra]]s

  * [[schematic homotopy type]]

* [[higher complex analytic geometry]]

* [[derived noncommutative geometry]]

  * [[noncommutative geometry]]

* [[higher differential geometry]]

  * [[motivation for higher differential geometry]]

  * [[differential geometry]], [[differential topology]]

  * [[higher prequantum geometry]]

  * [[derived smooth manifold]]

  * [[smooth ∞-groupoid]], [[∞-Lie algebroid]]

* [[higher symplectic geometry]]

* [[higher Klein geometry]]

* [[higher Cartan geometry]]

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