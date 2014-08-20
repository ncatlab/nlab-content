
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesion
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

A **quality type** is a key concept in [[W. Lawvere]]'s axiomatic approach to [[cohesion]] which permits to analyze a [[space]] understood as a domain of _quantitative_ variation via its _qualitative_ aspects. This can be viewed as an [[axiom|axiomatisation]] of the commonly encountered situation in [[geometry]] or [[dynamics]] that problems permit (only) a qualitative analysis.

A primary example for that kind of deferred analysis is the study of [[topological spaces]] via the [[homotopy category]] (hence via the [[homotopy types]] which they represent). So in broad a sense, quality types are intended as ingredients to a _synthetic homotopy theory_ where the (homotopy) contraction of a space (the collapsing of a cylinder/two idempotents) is extracted as essence of the concept of a spatial 'attribute'. 

Technically, a quality type amounts to a special sort of [[essential geometric morphism|essential localization]] and is therefore called a **quintessential localization**  in [Johnstone (1996)](#JS96).

In typical (topos) cases these come as [[adjoint triples|adjoint strings]] $\Pi\dashv\Delta\dashv\Gamma$ with $\Delta$ [[fully faithful functor|fully fiathful]] (hence: [[adjoint modalities]]) such that the [[connected components]] and the [[section|section functor]] coincide: $\Pi\cong\Gamma$ (cf. [[points-to-pieces transform]]).

Hence from a more geometrical point of view, a quality type is a particular simple kind of space with 'degenerate' components, or, if you prefer, a space with 'thick' points which in turn can be viewed as an _infinitesimal_ or 'minimal' vestige of cohesion: when a set is a space with no cohesion, a quality type is a space with _almost_ no cohesion. (For an elaboration of this perspective in the context of [[cohesive toposes]] see at [[infinitesimal cohesion]].)

Quality types together with the _continuity axiom_ are basically the essential new ingredients in Lawvere's [2007 axioms](#Law07) for geometry, wheras all the other axioms for a [[gros topos]] in one form or another are already around since the 80s. In particular, the axioms are fine-tuned to yield (homotopical) qualities of spaces, or in other words, cohesive spaces are those that admit qualitative analysis!

In the following we discuss the case for ordinary categories, for the higher order generalization see [[infinitesimal cohesive (infinity,1)-topos]].

## Definition

Let $\mathcal{S},\mathcal{F}$ be [[extensive categories]]. A fully faithful functor $q^*:\mathcal{S}\to\mathcal{F}$ is said to exhibit $\mathcal{F}$ as a **quality type** over $\mathcal{S}$ if $q^*$ has both a left and a right adjoint which moreover coincide: $q_!\dashv q^*\dashv q_*$ and $q_!\cong q_*$.

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

* {#Johnstone} [[Peter Johnstone|P. Johnstone]], _Remarks on Punctual Local Connectedness_ , TAC **25** no.3 (2011) pp.51-63. ([pdf](http://www.tac.mta.ca/tac/volumes/25/3/25-03abs.html))

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Generic Figures and their Glueings_ , Polimetrica Milano 2004.

* [[F. W. Lawvere]], _Categories of Spaces may not be Generalized Spaces as Exemplified by Directed Graphs_, Revista Colombiana de Matem&#225;ticas **XX** (1986) pp.179-186. Reprinted with commentary in TAC **9** (2005) pp.1-7. ([pdf](ftp://ftp.tac.mta.ca/tac/html/tac/reprints/articles/9/tr9.pdf))

* {#Law89a} [[F. W. Lawvere]], _Qualitative Distinctions between some Toposes of Generalized Graphs_ , Cont. Math. **92** (1989) pp.261-299.

* {#Law91a} [[F. W. Lawvere]], _Some Thoughts on the Future of Category Theory_ , pp.1-13 in Springer LNM **1488** (1991).

* {#Law92} [[F. W. Lawvere]], _Categories of Space and Quantity_, pp.14-30 in: J. Echeverria et al (eds.), _The Space of Mathematics_ , de Gruyter Berlin 1992.

* {#Law99} [[F. W. Lawvere]], _Kinship and Mathematical Categories_ , pp.411-425 in: R. Jackendoff, P. Bloom, K. Wynn (eds), _Language, Logic, and Concepts - Essays in Memory of John Macnamara_, MIT Press 1999.

* {#Law04} [[F. W. Lawvere]], _Left and right adjoint operations on spaces and data types_ , Theorectical Computer Science **316** (2004) pp.105-111.

* {#Law07} [[F. W. Lawvere]], _Axiomatic cohesion_ , TAC **19** no.3 (2007) pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

* {#Law08} [[F. W. Lawvere]], _Cohesive Toposes: Combinatorial and Infinitesimal Cases_, Como Ms. 2008. ([pdf](http://comocategoryarchive.com/Archive/temporary_new_material/FWLawvere-Cohesive-Toposes-Como-January-2008.pdf))

* {#Menni14a} [[Matías Menni|M. Menni]], _Continuous Cohesion over Sets_ , ms. (2014). ([pdf](https://sites.google.com/site/matiasmenni/continuityOverSets12.pdf?attredirects=0))

* {#Menni14b} [[Matías Menni|M. Menni]], _Sufficient Cohesion over Atomic Toposes_ , Cah.Top.G&#233;om.Diff.Cat. **LV** (2014). ([preprint](https://sites.google.com/site/matiasmenni/SufCohesion12.pdf?attredirects=0))
