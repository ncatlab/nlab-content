

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
=--
=--


# Past and future
* table of contents
{: toc}


## Idea

The _past_ of any physical event (object, system, etc) consists of everything that might (by the principles of [[causality]]) have potentially influenced that event; while its _future_ consists of everything that it might potentially influence.


## Definitions

Let $(X,g,o)$ be a [[spacetime]], that is a [[Lorentzian manifold]] $(X,g)$ equipped with [[time orientation]].  This time-orientation consists precisely of specification of which [[timelike]] and [[lightlike]] [[curves]] are _future-directed_ (and which are complementarily _past-directed_).

Let $x$ be a [[point]] in this spacetime.  Then:

* the **future** of $x$ is the subset $J^+(x)$ of all points of $X$ connected to $x$ by a future-directed [[timelike]] or [[lightlike]] [[curve]] *starting* at $x$;

* the **past** of $x$ is the subset $J^-(x)$ of all points of $X$ connected to $x$ by a future-directed [[timelike]] or [[lightlike]] [[curve]] *ending* at $x$.

Let $A$ be a more general [[subset]] of this spacetimes.  Then:

* the **future** of $A$ is the subset $J^+(A)$ defined as the [[union]] of $J^+(x)$ for all $x \in A$;

* the **past** of $A$ is the subset $J^-(A)$ defined as the [[union]] of $J^-(x)$ for all $x \in A$.


## Properties

A [[Cauchy surface]] $\Sigma$ in $(X,g)$ is a minimal subset of $X$ with the property that $X$ is the [[union]] of the future and past of $\Sigma$.  (Does this suffice to *define* Cauchy surfaces in the case of a Lorentzian manifold that admits a time-orientation?)

The operations $J^+$ and $J^-$ are (separately) [[Moore closures]] on the [[power set]] of $X$.  Stated explicitly (for $J^+$):

*  the future of $A$ contains $A$;
*  the future of the future of $A$ is simply the future of $A$;
*  if $A$ contains $B$, then the future of $A$ contains the future of $B$.


## Variations

Sometimes one wants to remove $x$ itself from $J^+(x)$ and $J^-(x)$ (or more precisely, to include $x$ only in the case of a [[closed timelike curve]] through $x$).  However, the operations $J^+$ and $J^-$ are not quite as mathematically well-behaved in this case.  (Note that $J^+(A)$ may still intersect $A$, or even contain all of $A$, even in the absence of closed timelike curves.)

## Related concepts

* [[future causal cone]], [[past causal cone]]

* [[advanced propagator]], [[retarded propagator]]


[[!redirects past]]
[[!redirects pasts]]
[[!redirects future]]
[[!redirects futures]]

[[!redirects causal future]]

[[!redirects causal past]]
