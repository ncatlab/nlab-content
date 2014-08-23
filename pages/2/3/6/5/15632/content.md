
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

A primary example for that kind of deferred analysis is the study of [[topological spaces]] via the [[homotopy category]] (hence via the [[homotopy types]] which they represent). So in a very broad sense, quality types are intended as ingredients to a  _synthetic homotopy theory_[^SHT] where the (homotopy) contraction of a space (the collapsing of a [[cylinder object|cylinder]]/two [[idempotents]]) is extracted as essence of the concept of a spatial 'attribute'. 

Technically, a quality type amounts to a special sort of [[essential geometric morphism|essential localization]] and is therefore called a **quintessential localization**  in ([Johnstone 1996](#JS96)).

In typical (topos) cases these come in the form of [[adjoint modalities|adjoint cylinders]] $\Pi\dashv\Delta\dashv\Gamma$ (with $\Delta$ [[fully faithful functor|fully faithful]]) such that the [[connected components]] and the [[section|section functor]] coincide (="collapse"): $\Pi\cong\Gamma$ (cf. [[points-to-pieces transform]]). This implies for the domain space of the functors that  every connected component contains exactly one point. Spaces with this property are called **infinitesimal spaces** in ([Lawvere 2008](#Law08)).

Hence from a more _geometrical point of view_, a quality type is a particular simple kind of space with 'degenerate' components, or, if you prefer, a space with 'thick' or 'coarse' points which in turn can be viewed as a minimal vestige of cohesion: when a set is a space with no cohesion, a quality type is a space with _almost_ no cohesion.[^GoC] (For an elaboration of this perspective in the context of [[cohesive toposes]] see at [[infinitesimal cohesion]].)

Quality types together with the _continuity axiom_ are an essential ingredient to Lawvere's [2007 axioms](#Law07) for geometry. ([Lawvere 2008](#Law08)) points to the role of continuity in ensuring that the Hurewicz homotopy category becomes a quality type. The definition of quality type yields important contrasts with _pure variation_ and _sufficient cohesion_ permitting to attend to the _fine structure_ of the [[gros topos|petit-gros]] landscape. So we can say with only slight exaggeration that the 2007 axioms revolve around the concept of a quality type and that cohesive spaces are those that admit qualitative (homotopical) analysis!

In the following we discuss the case for ordinary categories, for the higher order generalization see [[infinitesimal cohesive (infinity,1)-topos]].

## Definition

Let $\mathcal{S},\mathcal{F}$ be [[extensive categories]]. A [[fully faithful functor]] $q^*:\mathcal{S}\to\mathcal{F}$ is said to exhibit $\mathcal{F}$ as a **quality type** over $\mathcal{S}$ if $q^*$ has both a left and a right adjoint which moreover coincide: $q_!\dashv q^*\dashv q_*$ and $q_!\cong q_*$.

## Examples

> If we divest smooth spaces of all global cohesion, keeping only the jets (on which the Thom-Mather singularities depend), we obtain a category in which every connected component of any object has exactly one point, so that the natural map between those functors is an isomorphism.  Lawvere (2004, p.108)

* Kan complexes over $Set$ (...)

* Galois theory - presheaves on the opposite of the category of finite-dimensional local k-algebras (Lawvere 2004) (...)

* First example of quality type over topos of reflexive graphs (...)

## Properties

## Related entries

* [[cohesive topos]]

* [[infinitesimal cohesive (infinity,1)-topos]]

* [[Nullstellensatz]]

* [[Aufhebung]]

## Remarks on the literature

The definition of quality types occurs in ([Lawvere 2007](#Law07)) with important additional remarks in ([Lawvere 2008](#Law08)). The first occurrence of a quality type is in the work of the 1980s in the context of the gros topos of graphs: a discussion of this example is in ([Lawvere 1989](#Law89a),  p.277) where already the contrast to sufficient cohesion is observed. They resurface without an explicit definition in the [2004 paper](Law04) on data types.

Under the name of quintessential localization they are the focus of ([Johnstone 1996](JS96)) where the characterization via central idempotents is given. Some additional results occur in the context of the [[Nullstellensatz]] in ([Johnstone 2011](#JS11)). ([Menni 2014](#Menni14b)) attends to the contrast between quality types and sufficient cohesion.

## References

* {#JS96}[[Peter Johnstone|P. Johnstone]], _Remarks on Quintessential and Persistent Localizations_ , TAC **2** no.8 (1996) pp.90-99. ([pdf](http://www.tac.mta.ca/tac/volumes/1996/n8/n8.pdf))

* {#JS11} [[Peter Johnstone|P. Johnstone]], _Remarks on Punctual Local Connectedness_ , TAC **25** no.3 (2011) pp.51-63. ([pdf](http://www.tac.mta.ca/tac/volumes/25/3/25-03abs.html))

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Generic Figures and their Glueings_ , Polimetrica Milano 2004.

* [[F. W. Lawvere]], _Categories of Spaces may not be Generalized Spaces as Exemplified by Directed Graphs_, Revista Colombiana de Matem&#225;ticas **XX** (1986) pp.179-186. Reprinted with commentary in TAC **9** (2005) pp.1-7. ([pdf](ftp://ftp.tac.mta.ca/tac/html/tac/reprints/articles/9/tr9.pdf))

* {#Law89a} [[F. W. Lawvere]], _Qualitative Distinctions between some Toposes of Generalized Graphs_ , Cont. Math. **92** (1989) pp.261-299.

* {#Law91a} [[F. W. Lawvere]], _Some Thoughts on the Future of Category Theory_ , pp.1-13 in Springer LNM **1488** (1991).

* {#Law92} [[F. W. Lawvere]], _Categories of Space and Quantity_, pp.14-30 in: J. Echeverria et al (eds.), _The Space of Mathematics_ , de Gruyter Berlin 1992.

* {#Law96} [[F. W. Lawvere]], _Unity and Identity of Opposites in Calculus and Physics_ , App. Cat. Struc **4** (1996) pp.167-174.

* {#Law99} [[F. W. Lawvere]], _Kinship and Mathematical Categories_ , pp.411-425 in: R. Jackendoff, P. Bloom, K. Wynn (eds), _Language, Logic, and Concepts - Essays in Memory of John Macnamara_, MIT Press 1999.

* {#Law04} [[F. W. Lawvere]], _Left and right adjoint operations on spaces and data types_ , Theorectical Computer Science **316** (2004) pp.105-111.

* {#Law07} [[F. W. Lawvere]], _Axiomatic cohesion_ , TAC **19** no.3 (2007) pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

* {#Law08} [[F. W. Lawvere]], _Cohesive Toposes: Combinatorial and Infinitesimal Cases_, Como Ms. 2008. ([pdf](http://comocategoryarchive.com/Archive/temporary_new_material/FWLawvere-Cohesive-Toposes-Como-January-2008.pdf))

* {#Menni14a} [[Matías Menni|M. Menni]], _Continuous Cohesion over Sets_ , ms. (2014). ([pdf](https://sites.google.com/site/matiasmenni/continuityOverSets12.pdf?attredirects=0))

* {#Menni14b} [[Matías Menni|M. Menni]], _Sufficient Cohesion over Atomic Toposes_ , Cah.Top.G&#233;om.Diff.Cat. **LV** (2014). ([preprint](https://sites.google.com/site/matiasmenni/SufCohesion12.pdf?attredirects=0))


[^SHT]: The term _synthetic homotopy theory_ is slightly misleading here as Lawvere's reflections don't provide a fully fledged homotopy theory but are rather observations or meditations on the role of the cylinder configuration in the analysis of space. Important facets of his views are documented in Lawvere [1992](#Law92), [1994](#Law94), [1999](#1999).
In a complementary direction, _[[homotopy type theory]]_ provides a synthetic formulation of [[homotopy theory]] proper, not just of the [[homotopy category]], and _[[cohesive homotopy type theory]]_ implements [[cohesion]] _in_ that natively homotopy-theoretic context. 

[^GoC]: From another perspective, one could view a quality type as a set with germs of cohesion.