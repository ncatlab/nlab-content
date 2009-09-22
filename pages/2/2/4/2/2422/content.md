##Idea ##

This page is a spin-off of the [[structural set theory]] described at [[SEAR]]. The aim is to define (individual) natural numbers in SEAR without assuming the axiom of infinity. As a result, there should be a set with $n$ elements for all $n$, but we will not have a set of all natural numbers.

The aim is to use as few axioms as possible

## Zero and One ##

Barring opinions whether zero should be a natural number, in SEAR we have sets $\empty$ and $\mathbf{1}$ with zero and one element respectively. These follow from axioms 0, 1 and 2 at [[SEAR]].

## Two ##

A candidate for $\mathbf{2}$ is clearly $P\mathbf{1}$, but we need to show it has two elements. It would be nice to do this in such a way that doesn't use the result that the metacategory of SEAR-sets is a topos.

+--{: .query}
[[Mike Shulman]]: If you don't want to use powersets, then I'm pretty sure you'll need an axiom of coproducts.  Unless I'm mistaken, the collection of [[subsingleton]] sets satisfies Axioms 0, 1, and 2.

[[David Roberts]]: Actually what I probably mean is not use the result that $Set$ is a topos. I think you are correct on the subsingleton front, because it looks like we have no way of obtaining sets with more than one element without more axioms.

_Toby_:  If you want to be cute, you can make the existence of $\mathbf{2}$ an axiom and then get arbitrary binary coproducts using Collection.  On the other hand, if you\'re happy using power sets, then don\'t bother proving that $P\mathbf{1} = \mathbf{2}$ (which won\'t generalise to the intuitionistic case anyway); instead use Separation to carve out $\{ x \in P\mathbf{1} \;|\; x = \empty \;\vee\; x = \mathbf{1} \}$.  Then $\mathbf{3}$ is a subset of $P\mathbf{2}$, etc; or make $\mathbf{3}$ and $\mathbf{4}$ both subsets of $P\mathbf{2}$, with the general rule going logarithmically.
=--

## Three and many ##

From here we proceed inductively...

+--{: .query}
[[David Roberts]]: This may be overkill, as maybe $\mathbf{n}$ could be $\mathbf{1}\coprod \ldots \coprod \mathbf{1}$ ($n$ times), but I was thinking of mimicking other better-known definitions.
=--