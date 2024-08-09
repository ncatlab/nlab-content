
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

A **bounded total order** is a [[total order]] $(S, \leq)$ which has elements $\bot \in S$ and $\top \in S$ such that for all elements $a \in S$, $\bot \leq a$ and $a \leq \top$. 

Equivalently, a **bounded total order** is a [[distributive lattice]] $(S, \bot, \wedge, \top, \vee)$ which satisfies [[totality]]: for all elements $a \in S$ and $b \in S$, $a \vee b = a$ or $a \vee b = b$. 

Bounded total orders are important in [[dependent type theory]] and [[simplicial type theory]] because they allow for the definition of [[hom types]], [[Segal types]], and [[Rezk types]] which are important for [[synthetic (infinity,1)-category theory]]. 

## Examples

* The [[unit interval]] is a bounded total order. 

* The [[boolean domain]] is a bounded total order. 

* More generally, every [[finite set|finite]] [[total order]] is a bounded total order. 

## Category of bounded total orders

The category of bounded total orders is the category whose objects are bounded total orders and whose morphisms are extrema-preserving [[monotonic functions]] between bounded total orders. 

* The [[boolean domain]] is the [[initial object]] in the category of bounded total orders.

* The trivial bounded total order, where $\bot = \top$, is the [[terminal object]] in the [[category]] of bounded total orders. 

## Related concepts

* [[total order]]

* [[distributive lattice]]

* [[simplicial type theory]]

* [[hom type]], [[Segal type]]

[[!redirects bounded total order]]
[[!redirects bounded total orders]]