
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

[[!redirects scattered set]]
[[!redirects dense-in-itself subset]]
[[!redirects scattered spaces]]

#Contents#
* automatic table of contents goes here
{:toc}

## Idea
A **scattered space** is a [[topological space]] that on the scale of 'connectivity' is at the extreme opposite of [[perfect space|perfect spaces]].

Scattered spaces are used to provide topological models of [[provability logic]].

## Definition

A subset $A$ of a topological space is called _dense in itself_ if  each point of $A$ is a [[limit point]] of $A$.

A topological space $X$ is called _scattered_ if $X$ doesn't contain nonempty dense-in-itself subsets.

## Example

* The [[Sierpinski space]] $X=\{a,b\}$ with topology $\{\emptyset ,\{a\}, X\}$ is scattered: whereas $b$ is a limit point of $X$, $a$ isn't, whence $X$ fails to be dense in itself. $\{a\}$ fails to be dense in itself since, whereas $b$ is a limit point, $a$ isn't. Finally, $\{b\}$ has no limit points at all. 

* Discrete spaces are scattered.

## Properties

* Every topological space $X$ is the disjoint union of a scattered subset and a [[perfect space|perfect]] subset.

## Remark

Given a space $X$, using the derivative $\partial : 2^X\to 2^X$ that maps a subset to the set of its limit points, the property of being dense-in-itself amounts to $A\subseteq\partial A$. Sierpi&#324;ski ([1927](#Sierpinski27)) studies the abstract properties of dense-in-itself and corresponding scattered subsets relative to arbitrary monotone maps $2^X\to 2^X$.

## Related entries

* [[scattered topos]]

* [[perfect space]]

* [[Magari algebra]]

* [[provability logic]]

## Reference

* L. Beklemishev, D. Gabelaia, _Topological interpretations of provability logic_ , arXiv:1210.7317 (2012).  ([abstract](http://arxiv.org/abs/1210.7317))

* {#Sierpinski27} W. Sierpi&#324;ski, _La notion de deriv&#233;e comme base d'une th&#233;orie des ensembles abstraits_ , Math. Ann. **97** (1927) pp.321-337. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PID=PPN235181684_0097%7CLOG_0017))

* S. Willard, _General Topology_ , Addison-Wesley Reading 1970. (Dover reprint 2004, p.219)

