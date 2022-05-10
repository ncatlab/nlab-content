+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea


A [[categorification]] of the notion of [[sigma-frame|$\sigma$-frame]]. 

## Definition ##

A __$\sigma$-pretopos__ is a [[pretopos]] $\mathcal{E}$ where all [[countable]] [[unions]] of [[subobjects]] (exist and) are [[pullback-stable]]. 

### Girard-esque axioms ###

A __$\sigma$-pretopos__ is 

* a [[category]]

* with a [[generating set]],

* with all [[finite limits]],

* with all [[countable]] [[coproducts]], which are [[disjoint]], and [[pullback-stable]],

* where all [[congruences]] have [[effective quotient|effective]] [[quotient objects]], which are also [[pullback-stable]].

## Examples

* Any [[pretopos#infinitary|infinitary pretopos]] is a $\sigma$-topos.

* The category of [[countable sets]] (for instance, [[subquotients]] of the [natural numbers]] $\mathbb{N}$) is a $\sigma$-pretopos.

* The [[category of sets]] in the [[predicative mathematics|predicative]] [[set theory]] $CZF_{Exp}$ from ([Simpson-Streicher 2012](#SimpsonStreicher12)) is a $\sigma$-pretopos.

## See also ##

* [[pretopos]]

* [[Grothendieck topos]]

* [[sigma-frame]]

## References ##


The concept is defined and discussed around Lemma A.1.4.19 in 

* [[Peter Johnstone]], [[Sketches of an Elephant]] -- A Topos Theory Compendium**, Oxford University Press 2002. Volume 1 ([ISBN:9780198534259](https://global.oup.com/academic/product/sketches-of-an-elephant-9780198534259)), Volume 2 ([ISBN:9780198515982](https://global.oup.com/academic/product/sketches-of-an-elephant-9780198515982))


A predicative approach to foundations using $\sigma$-pretoposes is given in

* {#SimpsonStreicher12} [[Alex Simpson]] and [[Thomas Streicher]], _Constructive toposes with countable sums as models of constructive set theory_, Annals of Pure and Applied Logic **163** (2012), 1419–1436.

Simplicial homotopy internal to a $\sigma$-pretopos is studied in:

* {#Low14} [[Zhen Lin Low]], _Internal and local homotopy theory_, [arXiv:1404.7788](https://arxiv.org/abs/1404.7788) (2014).


[[!redirects sigma-pretopoi]]

