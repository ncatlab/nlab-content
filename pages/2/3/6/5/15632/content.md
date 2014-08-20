
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quality type
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}
[[!redirects quality]]
[[!redirects Quality type]]
[[!redirects extensive quality]]
[[!redirects intensive quality]]
[[!redirects quintessential localization]]

## Idea

A **quality type** is a key concept in [[W. Lawvere]]'s axiomatic approach to cohesion which permits to analyze a space understood as a domain of quantitative variation via its qualitative aspects. This can be viewed as an axiomatisation of the commonly encountered situation in geometry and dynamics that problems permit only a qualitative analysis. The primary example is the **homotopy category**.

Technically, a quality type amounts to a special sort of [[essential geometric morphism|essential localization]] and is therefore called a _quintessential localization_  in [Johnstone (1996)](#JS96).

Quality types are basically together with the _contuinity axiom_ (2b) the essential new ingredients in Lawvere's [2007 axioms](#Law07) for geometry wheras all the other axioms for a [[gros topos]] are actually around since the 80s in one form or another. In particular, the other axioms are tuned to yield homotopic qualities of spaces, or in other words, cohesive spaces are those that admit qualitative analysis!

In the following we discuss the case for ordinary categories, for the higher order generalization see [[infinitesimal cohesive (infinity,1)-topos]].

## Definition

Let $\mathcal{S},\mathcal{F}$ be [[extensive categories]]. A fully faithful functor $q^*:\mathcal{S}\to\mathcal{F}$ is said to exhibit $\mathcal{F}$ as a **quality type** over $\mathcal{S}$ if $q^*$ has both a left and a right adjoint which moreover coincide: $q_!\dashv q^*\dashv q_*$ and $q_!=q_*$.

## Examples

> If we divest smooth spaces of all global cohesion, keeping only the jets (on which the Thom-Mather singularities depend), we obtain a category in which every connected component of any object has exactly one point, so that the natural map between those functors is an isomorphism.  Lawvere (2004, p.108)

* Kan complexes over $Set$ (...)

* Galois theory - presheaves on the opposite of the category of finite-diemnsional local k-algebras (Lawvere 2004) (...)

* First example of quality type over topos of reflexive graphs (...)

## Related entries

* [[cohesive topos]]

* [[infinitesimal cohesive (infinity,1)-topos]]

* [[Aufhebung]]


## References

* {#JS96}[[Peter Johnstone|P. Johnstone]], _Remarks on Quintessential and Persistent Localizations_ , TAC **2** no.8 (1996) pp.90-99. ([pdf](http://www.tac.mta.ca/tac/volumes/1996/n8/n8.pdf))

* {#Johnstone} [[Peter Johnstone]], _Remarks on punctual local connectedness_ , TAC **25** no.3 (2011) pp.51-63. ([pdf](http://www.tac.mta.ca/tac/volumes/25/3/25-03abs.html))

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Generic Figures and their Glueings_ , Polimetrica Milano 2004.

* [[F. William Lawvere]], _Categories of Spaces may not be Generalized Spaces as Exemplified by Directed Graphs_, Revista Colombiana de Matem&#225;ticas **XX** (1986) pp.179-186. Reprinted with commentary in TAC **9** (2005) pp.1-7. ([pdf](ftp://ftp.tac.mta.ca/tac/html/tac/reprints/articles/9/tr9.pdf))

* {#Law89a} F. W. Lawvere, _Qualitative Distinctions between some Toposes of Generalized Graphs_ , Cont. Math. **92** (1989) pp.261-299.

* {#Law91a} F. W. Lawvere, _Some Thoughts on the Future of Category Theory_ , pp.1-13 in Springer LNM **1488** (1991).

* {#Law92} F. W. Lawvere, _Categories of Space and Quantity_, pp.14-30 in: J. Echeverria et al (eds.), _The Space of mathematics_ , de Gruyter Berlin 1992.

* {#Law99} F. W. Lawvere, _Kinship and Mathematical Categories_ , pp.411-425 in: R. Jackendoff, P. Bloom, K. Wynn (eds), _Language, Logic, and Concepts - Essays in Memory of John Macnamara_, MIT Press 1999.

* {#Law04} F. W. Lawvere, _Left and right adjoint operations on spaces and data types_ , Theorectical Computer Science **316** (2004) pp.105-111.

* {#Law07} F. W. Lawvere, _Axiomatic cohesion_ , TAC **19** no.3 (2007) pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

* [[F. William Lawvere]], _Cohesive Toposes: Combinatorial and Infinitesimal Cases_, Como Ms. 2008. ([pdf](http://comocategoryarchive.com/Archive/temporary_new_material/FWLawvere-Cohesive-Toposes-Como-January-2008.pdf))

* {#Menni14} [[Matías Menni]], _Continuous Cohesion over sets_ ([pdf](https://sites.google.com/site/matiasmenni/continuityOverSets12.pdf?attredirects=0))

* [[Matías Menni]], _Sufficient Cohesion over Atomic Toposes_ , Cah.Top.G&#233;om.Diff.Cat. **LV** (2014). ([preprint](https://sites.google.com/site/matiasmenni/SufCohesion12.pdf?attredirects=0))
