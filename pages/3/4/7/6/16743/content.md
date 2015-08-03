+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

[[!redirects demorgan topos]]
[[!redirects de Morgan topos]]
[[!redirects De Morganisation]]
[[!redirects De Morgan toposes]]
[[!redirects de Morgan toposes]]
[[!redirects DeMorgan topos]]


## Idea
A **De Morgan topos** $\mathcal{E}$ is a middle thing between a [[Boolean topos]] with a [[classical logic|classical internal logic]] and a general [[topos]] with an [[intuitionistic logic|intuitionistic internal logic]], in that the lattices of [[subobjects]] in $\mathcal{E}$ obey a weak form of the [[law of excluded middle]] which defines a [[De Morgan algebra]].

The de Morgan property has many equivalent formulations and many facets making the class of de Morgan toposes an important one in [[topos theory]]. From the perspective on toposes as generalized spaces they correspond to _extremally disconnected spaces_ in [[topology]].

## Definition

A topos $\mathcal{E}$ is called a _De Morgan topos_ if its [[subobject classifier]] $\Omega$ is an internal [[De Morgan algebra]].

## Examples

* Every [[Boolean topos]] is a De Morgan topos.

* The topos $Sh(X)$ of sheaves on a topological space $X$ is De Morgan precisely iff $X$ is extremally disconnected, i.e. the closure of every open subset is open.

## Properties

+-- {: .num_prop}
###### Proposition
Let $\mathcal{C}$ be a small category. The [[presheaf topos]] $Set^{\mathcal{C}^{op}}$ is De Morgan precisely if $\mathcal{C}^{op}$ satifies the [[Ore condition]].
=--

This result due to [[Peter Johnstone]] appears e.g. as an exercise in [Johnstone (1977, p.162)](#Johnstone77), or with a proof in [Johnstone (1979)](#Johnstone79). Compare also the generalizations to other intermediate logics in [Caramello (2012)](#Caramello12).

## Related entries

* [[De Morganization]]
* [[De Morgan algebra]]
* [[Ore condition]]
* [[Boolean topos]]
* [[law of excluded middle]]

## References

* [[Francis Borceux]], _Handbook of Categorical Algebra vol.3_ , Cambridge UP 1994. (sections 1.2, 7.3)

* {#Caramello09}[[Olivia Caramello]], _De Morgan classifying toposes_ , Adv. in Math. **222** (2009) pp.2117-2144. ([arXiv:0808.1519](http://arxiv.org/abs/0808.1519))

* {#Caramello12}[[Olivia Caramello]], _Topologies for intermediate logics_ , arXiv:1205.2547 (2012). ([arXiv:1205.2547](http://arxiv.org/abs/1205.2547))

* {#CJ09}[[Olivia Caramello]], [[Peter Johnstone]], _De Morgan's law and the Theory of Fields_ , Adv. in Math. **222** (2009) pp.2145-2152. ([arXiv:0808.1572](http://arxiv.org/abs/0808.1572))

* {#Johnstone77}[[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977. (Dover reprint New York 2014)

* {#Johnstone79}[[Peter Johnstone]], _Conditions Related to De Morgan's Law_ , pp.479-491 in LNM **753** (1979).

* {#Johnstone79b}[[Peter Johnstone]], _Another Condition Equivalent to De Morgan's Law_ , Comm. Alg. **7** (1979) pp.1309-1312.

* {#Johnstone80}[[Peter Johnstone]], _The Gleason Cover of a Topos I_ , JPAA **19** (1980) pp.171-192. 

* {#Johnstone81}[[Peter Johnstone]], _The Gleason Cover of a Topos II_ , JPAA **22** (1981) pp.229-247. 

* {#Johnstone}[[Peter Johnstone]], _[[Sketches of an Elephant]] vol. II_, Oxford UP 2002. (section D4.6, pp.498ff)

* {#Johnstone13}[[Peter Johnstone]], _The Gleason Cover of a Realizability Topos_ , TAC **28** no.32 (2013) pp.1139-1152. ([abstract](http://www.tac.mta.ca/tac/volumes/28/32/28-32abs.html))

* [[Anders Kock]], [[Gonzalo E. Reyes]], _Relatively Boolean and De Morgan Toposes and Locales_ , Cah. Top. G&#233;om. Diff. Cat. **35** no.3 (1994) pp.249-261. ([numdam](http://www.numdam.org/numdam-bin/item?id=CTGDC_1994__35_3_249_0))

* {#LawvereMenni15} [[William Lawvere]], [[Matías Menni]], _Internal choice holds in the discrete part of any cohesive topos satisfying stable connected codiscreteness_ , TAC **30** no.26 (2015) pp.909-932. ([abstract](http://www.tac.mta.ca/tac/volumes/30/26/30-26abs.html))

* {#Mielke84} M. V. Mielke, _Homotopically Trivial Toposes_ , Pacific J. Math. **110** no.1 (1984) pp.171-182. ([euclid](https://projecteuclid.org/euclid.pjm/1102711108))

* [[Chris Mulvey]], _The Maximality of Filters_ , JPAA **68** (1990) pp.253-258.

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Generic Figures and their Glueings_ , Polimetrica Milano 2004.
