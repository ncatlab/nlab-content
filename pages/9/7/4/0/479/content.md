
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **Boolean category** is a [[coherent category]] (such as a [[topos]] or [[pretopos]]) in which every [[subobject]] has a complement, i.e., for any [[monomorphism]] $A\hookrightarrow X$ there is a monomorphism $B\hookrightarrow X$ such that $A\cap B$ is [[initial object|initial]] and $A\cup B = X$.  Therefore, the [[subobject lattice]] $Sub(X)$ of any [[object]] $X$ is a [[Boolean algebra]].

## Properties

Any Boolean category is, in particular, a [[Heyting category]] and therefore supports a full [[first-order logic|first-order]] [[internal logic]].  However, unlike that of an arbitrary Heyting category, the internal logic of a Boolean category satisfies the principle of [[excluded middle]]; it is [[first-order logic|first-order]] [[classical logic]].

In addition, every Boolean category $\mathcal{C}$ is a [[first-order hyperdoctrine|first order]] [[Boolean hyperdoctrine]] given by the [[subobject poset]] [[functor]] $\mathrm{sub}:\mathcal{C}^{op} \to BoolAlg$. 

## Related entries

* [[pretopos]]
* [[De Morgan Heyting category]]
* [[positive category]]

[[!include categories and logic - table]]

[[!redirects Boolean category]]
[[!redirects Boolean categories]]
[[!redirects boolean category]]
[[!redirects boolean categories]]


