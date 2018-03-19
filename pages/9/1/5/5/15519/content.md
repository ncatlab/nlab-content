


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}



## Idea

An **injective topos** is a topos-theoretic generalization of the notion of an [[injective object]] familiar from algebra, or in other words, a topos with good extension properties along [[subtopos|subtopos inclusions]].

## Definition

+-- {: .num_defn}
###### Definition
A [[Grothendieck topos]] $\mathcal{E}$ is called _injective_ (with respect to subtopos inclusions) in the [[2-category]] of Grothendieck toposes $GrTop$ if for every inclusion $i:\mathcal{F}\hookrightarrow\mathcal{G}$ and 1-cell $f:\mathcal{F}\to\mathcal{E}$ there exists a 1-cell $g:\mathcal{E}\to\mathcal{G}$ and a 2-isomorphism $g\circ i\cong f$ .
=--

## Properties

The main characterization of injective toposes is achieved by the following result due to Johnstone-Joyal ([1982](#JJ82)).

+-- {: .num_prop}
###### Theorem
There is an equivalence of 2-categories between the full sub-2-category of $GrTop$ with 0-cells the injective toposes and the 2-category of cocomplete ind-small [[continuous category|continuous categories]] with 1-cells the filtered colimit preserving functors. This equivalence sends an injective topos to its [[category of points]].

=-- 

Note, that this gives also a characterization of the continuous categories involved as category of points of injective toposes.

+-- {: .num_prop}
###### Proposition
The lex totally distributive categories with a small dense generator are precisely the injective Grothendieck toposes.

=--

This occurs as theorem 4.5 in Lucyshyn-Wright ([2011](#LW11)).

## Example

 * $Set$ is the only injective [[Boolean topos]] (cf [Johnstone 2002](#JT02), p.740).

## Related entries

* [[injective object]]

* [[continuous category]]

* [[totally distributive category]]

* [[exponentiable topos]]

* [[De Morgan topos]]


## References

* [[Peter Johnstone]], _Injective Toposes_ , pp.284-297 in LNM **871** Springer Heidelberg 1981.

* {#JT02}[[Peter Johnstone]], _Sketches of an Elephant vol. 2_ , Cambridge UP 2002. (section C4.3, pp.738-745)

* {#JJ82}[[Peter Johnstone]], [[André Joyal]], _Continuous categories and exponentiable toposes_ ,  JPAA **25** (1982) pp.255-296.

* {#LW11} [[Rory Lucyshyn-Wright]], _Totally distributive toposes_ , arXiv:1108.4032 (2011). ([abstract](https://arxiv.org/abs/1108.4032))