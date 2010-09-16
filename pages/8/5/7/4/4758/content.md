
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Strict $2$-groupoids
* table of contents
{: toc}

## Idea

The general notion of [[2-groupoid]] is also called _weak $2$-groupoid_ to distinguish from the special case of strict $2$-groupoids.


## Definitions

A __strict $2$-groupoid__ is equivalently:

*  a [[strict 2-category]] in which all morphisms are strictly invertible.
*  a [[Grpd]]-[[enriched category]].
*  a [[2-groupoid]] that is a [[strict 2-category]].
*  a [[strict omega-groupoid]] that is $2$-[[truncated]].


## Properties

This is a [[strict omega-groupoid]] in which all [[k-morphism]]s for $k \gt 2$ are [[identities]]. This is equivalently a [[crossed complex]] of the form $(G_2 \to G_1 \stackrel{\to}{\to} G_0)$.

Strict $2$-groupoids embed into all $2$-groupoids (modeled by [[bigroupoids]]) by regarding a strict $2$-category as a special case of a [[bicategory]].

They embed into all $2$-groupoids modeled as [[Kan complex]]es via the [[omega-nerve]].

## Examples

Amongst the simplest examples will be the [[strict 2-group]]s, as these are __strict 2-groupoids__ with a single object. About the simplest example of such an object then comes from a group homomorphism:

$$\phi: H\to G$$
as follows.

Just as a function between sets, $f : X\to Y$ defines as an equivalence relation on $X$ by $x_0\sim x_1$ if and only if $\phi x_0 = \phi x_1$, so here we get an equivalence relation on the group $H$.  That equivalence relation is a [[congruence]] so is an internal equivalence relation, that is, it is internal to the category of groups.  An equivalence relation is also a [[groupoid]] in a well known way, and here we get an internal groupoid within the category of groups.  There will be a group of objects, namely $H$, and a group of arrows, given by $H \times_G H$, the pullback of $\phi$ along itself. Working this out, clearly this group consists of the pairs $(h_0,h_1)$ of elements having the same image in $G$.Such a pair goes from $h_0$ to $h_1$. The composition is then very simple:
$$(h_0,h_1)\star (h_1,h_2) = (h_0,h_2)$$
and inverses are given by swapping the two entries, $(h_0,h_1)^{-1} = (h_1,h_0)$. All this is happening within that same group theoretic context and there is a group multiplication on each of the sets given by $(h_0,h_1).(h^\prime_0,h^\prime_1) = (h_0h^\prime_0,h_1h^\prime_1)$. With this the maps giving the source and target of an 'arrow' are homomorphisms as is the composition.







[[!redirects strict 2-groupoid]]
[[!redirects strict 2-groupoids]]
