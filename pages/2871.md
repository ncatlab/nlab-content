
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

A _cellular model category_ is a particularly convenient form of a [[model category]].

It is similar to a [[combinatorial model category]]. (For the moment, see there for more details.)


## Definition ##

A **cellular model category** is a [[cofibrantly generated model category]] such that there is a [[set]] of generating [[cofibrations]] $I$ and a set of generating [[acyclic cofibrations]] $J$, such that:

* all [[domain]] and [[codomain]] [[objects]] of elements of $I$ are [[compact objects]] relative to $I$ (in the sense of Hirschhorn);

* the domain objects of the elements of $J$ are [[small objects]] relative to $I$;

* the [[cofibrations]] are [[effective monomorphism]]s.


## Examples ##

* [[Top]] with the standard [[Quillen model structure on topological spaces]] (same for [[pointed topological spaces]])

* [[SSet]] with the standard [[Quillen model structure on simplicial sets]] (same for pointed simplicial sets).

For $C$ a cellular model category we have that

* the [[functor category]] $[D,C]$ for any [[small category]], $D$, with its projective [[global model structure on functors]] is again a cellular model category;

* for $c \in C$ any object, the [[over category]] $C/c$ is again a cellular model category.


## Applications ##

For cellular model categories $C$ that are [[proper model category|left proper model categories]] all left [[Bousfield localization]]s $L_S C$ at any set $S$ of morphisms are guaranteed to exist.

## Related concepts

* the notions of *[[cellular categories]]* and of *cellular model categories* are vaguely related, but not as systematically as the (independently chosen) terminology might suggest

* [[combinatorial model category]]

## References

Textbook account:

* {#Hirschhorn02} [[Philip Hirschhorn]], Section 12 of: _[[Model Categories and Their Localizations]]_, AMS Math. Survey and Monographs Vol 99 (2002) &lbrack;[ISBN:978-0-8218-4917-0](https://bookstore.ams.org/surv-99-s/), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf)&rbrack;

Discussion in the context of [[algebraic model categories]]:

* [[Emily Riehl]], _Cellularity in algebraic model structures_ ([blog post](http://golem.ph.utexas.edu/category/2011/12/cellularity_in_algebraic_model.html#c040417))


[[!redirects cellular model categories]]



