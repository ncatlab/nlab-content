
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

_Higher geometry_ studies the notions of [[space]] and [[geometry]] in [[higher category theory]]. Specifically if the spaces on which the geometry is _modeled_ are themselves objects in higher category theory this is also called _[[derived geometry]]_ .

Higher geometry is typically built on [[(∞,1)-topos theory]], which (see [[topos]]) provides a general context in which to speak of generalizations of [[topological space]]s. The axioms of higher geometry typically impose extra structures on [[(∞,1)-topos]]es that encode genuine _geometry_ .

There are two aspects to this, induced from the two aspects of [[big and little topos]]es:

* A _little $(\infty,1)$-topos_ enocodes itself a [[space]]. Axioms for equipping little $(\infty,1)$-toposes with geometric structure have been given in ([Lurie](#Lurie)) in terms of the notion of [[structured (∞,1)-topos]]es.

* A _big $(\infty,1)$-topos_ is an [[(∞,1)-category]] whose _[[object]]s_ are generalized spaces. Axioms for characterizing big [[topos]]es that encode geometry have been given in ([Lawevere](#Lawevere)). Their generalization to $(\infty,1)$-topos theory is given by the notion of a [[cohesive (∞,1)-topos]].


## Axiomatizatons

### Structured little $(\infty,1)$-toposes

The notion of [[geometry (for structured (∞,1)-toposes)|geometry is formalized]]  in the form of an [[(∞,1)-category]] $\mathcal{G}$ whose objects play the role of test-spaces on which all other [[space]]s are modeled, in a hierarchy of generalized objects:

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

A notable exception to this is possibly the program by [[Maxim Kontsevich]] and others where under the term [[noncommutative geometry]] and [[derived noncommutative geometry]] spaces are modeled as the formal dual to [[A-∞-categories]]. But $A_\infty$-categories are presentations for [[stable (∞,1)-categories]] and by the <a href="http://ncatlab.org/nlab/show/stable+(infinity%2C1)-category#StabGiraud">stable Giraud theorem</a> _presentable_ stable $(\infty,1)$-categories play a very similar role to (unstable) [[∞-stack]] [[(∞,1)-topos]]es. In particular they may be obtained from the latter by [[stabilization]]. 


### Structured big $(\infty,1)$-toposes

(...)

## References

An axiomatization of higher geometry of [[little topos|little]] [[(∞,1)-topos]]es is proposed in

* [[Jacob Lurie]], _[[Structured Spaces]]_ .
{#Lurie}

In 

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))
{#Lawvere}

an axiomatization of generalized geometry is proposed in terms of 1-[[catgegory theory]]. The evident generalization of this to [[(∞,1)-category theory]] provides an axiomatization for higher geometry. This is discussed at

* [[cohesive (∞,1)-topos]].

[[!redirects higher geometries]]