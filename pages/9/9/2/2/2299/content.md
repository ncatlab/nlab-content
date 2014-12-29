
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

_Higher geometry_ or _homotopical geometry_ refers to the generalization of [[geometry]] in the context of [[higher category theory]] and [[homotopy theory]]. More specifically, it is the geometry of some [[(infinity,1)-category]] $\mathcal{G}$ of "local models" or "test spaces". Given such a $\mathcal{G}$, together with some additional structure, one gets a hierarchy of "generalized spaces":

* representable or affine $\mathcal{G}$-stacks
  $\hookrightarrow$ $\mathcal{G}$-schemes
  $\hookrightarrow$ $\mathcal{G}$-stacks
  $\hookrightarrow$ $\mathcal{G}$-prestacks

Higher geometry is typically built on [[(∞,1)-topos theory]], which (see [[topos]]) provides a general context in which to speak of generalizations of [[topological space]]s. The axioms of higher geometry typically impose extra structures on [[(∞,1)-topos]]es that encode genuine _geometry_ .

There are two aspects to this, induced from the two aspects of [[big and little topos]]es:

* A _little $(\infty,1)$-topos_ encodes a [[space]] itself. Axioms for equipping little $(\infty,1)$-toposes with geometric structure have been given in ([Lurie](#Lurie)) in terms of the notion of [[structured (∞,1)-topos]]es.

* A _big $(\infty,1)$-topos_ is an [[(∞,1)-category]] whose _[[object]]s_ are generalized spaces. Axioms for characterizing big [[topos]]es that encode geometry have been given in ([Lawvere](#Lawvere)). Their generalization to $(\infty,1)$-topos theory is given by the notion of a [[cohesive (∞,1)-topos]].

Under forming [[groupoid convolution algebras]] and their higher analog, at least parts of higher geometry translate to [[noncommutative geometry]].

## Axiomatizations

Let $\mathcal{G}$ be an [[(infinity,1)-category]] of "local models" or "test spaces". Given the data of a [[Grothendieck topology]] $\tau$ on $\mathcal{G}$, one gets the notion of a $\mathcal{G}$-[[infinity-stack|stack]]. In order to get the finer notion of $\mathcal{G}$-[[infinity-scheme]], one needs to consider some further structure on $\mathcal{G}$. For example, one can consider the structure of a [[geometry (for structured (∞,1)-toposes)|geometry]] (in the sense of the linked page), or the structure of a [[homotopical algebraic geometry]] context. In the former case one gets the following hierarchy of generalized spaces:

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

One notion of generalized [[space]] in higher geometry that does _not_ fit into this pattern is apparently [[derived noncommutative algebraic geometry]] where spaces are modelled as the formal duals to [[dg-categories]]. But dg-categories are presentations for [[stable (∞,1)-categories]] and by the <a href="http://ncatlab.org/nlab/show/stable+(infinity%2C1)-category#StabGiraud">stable Giraud theorem</a> _presentable_ stable $(\infty,1)$-categories play a very similar role to (unstable) [[∞-stack]] [[(∞,1)-topos]]es. In particular they may be obtained from the latter by [[stabilization]]. 



## Examples

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