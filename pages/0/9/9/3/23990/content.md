
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

*Persistent homotopy* studies [[homotopy types]] (of [[topological spaces]]) as a parameter varies, hence [[filtered object in an (infinity,1)-category|filtered]] [[homotopy types]] (of [[filtered topological spaces]]), with focus on which elements of [[homotopy groups]] at given stage *persist* how far through the filtering to later stages. 
A key application is to [[Vietoris-Rips complexes]] of discrete subsets in a [[metric space]]. 

Notably in [[topological data analysis]] (TDA) these VR complexes arise as "point clouds" of datapoints, and the corresponding persistent homotopy is thought to detect relevant structure hidden in such data. As such, persistent homotopy refines the traditional use of [[persistent homology]] in TDA.

In general, persistent homotopy theory is to [[persistent homology]] as  [[homotopy theory]] is to [[homology theory]]: [[homotopy]] is a finer invariant than [[homology]],  the former sees the full [[homotopy type]] of a [[topological space]], the latter at most the underlying [[stable homotopy type]].

In other words, [[homology]] involves a kind of linearization or [[abelianization]] which loses information that is retained in the homotopy type (see the [Hurewicz theorem](Hurewicz+theorem#HurewiczTheorem)). Therefore persistent homotopy is in general a finer invariant of [[filtered topological spaces]] than [[persistent homology]].  In fact, traditional [[persistent homology]] considers only *[[ordinary homology]]* which is the coarsest of all [[generalized homology]] invariants. Hence in between the coarse invariant of [[persistent homology]] and the fine invariants of persistent homotopy will be intermediate invariants that would deserve to be called *persistent generalized homology* -- but these have not yet found much attention, certainly not in the context of [[topological data analysis]].

However, besides [[homology]] there is, [[duality|dually]], also *[[cohomology]]*, whose analogous [[homotopy theory|homotopy theoretic]] refinement is ([[non-abelian cohomology|non-abelian cohomology theories]], but in particular:) *[[cohomotopy|co-homotopy]]*. The generalization of [[cohomotopy]] to the context of persistence lends itself to the analysis of persistence of [[level sets]] of [[continuous functions]]: see at *[[persistent cohomotopy]]* (and see the references [below](#CohomotopyInTopologicalDataAnalysisReferences)).

| | coarse |  intermediate | fine  |
|--|--|--|--|
| **[[homology]]** | [[ordinary homology]] | [[generalized homology]] | [[homotopy groups|homotopy]] |
| **[[cohomology]]** | [[ordinary cohomology]] | [[Whitehead-generalized cohomology|generalized cohomology]] | [[cohomotopy]] |
|  |  |  |  | 
| **persistent homology** | [[persistent homology|persistent ordinary homology]] | persistent generalized homology | [[persistent homotopy]] |
| **persistent cohomology** | persistent ordinary cohomology | persistent generalized cohomology | [[persistent cohomotopy]] |


## Related concepts

* [[Vietoris-Rips complex]]

* [[homotopy theory]]

* [[parameterized homotopy theory]]

* [[persistent homology]]

* [[filtered topological space]]

## References

### General

Original articles with focus on establishing the homotopy-version of the [[stability of persistence diagrams|stability theorem]]:

* {#BlumbergLesnick17} [[Andrew J. Blumberg]], [[Michael Lesnick]], *Universality of the Homotopy Interleaving Distance* $[$[arXiv:1705.01690](https://arxiv.org/abs/1705.01690)$]$

* {#Jardine19} [[J. F. Jardine]], *Data and homotopy types* $[$[arXiv:1908.06323](https://arxiv.org/abs/1908.06323)$]$

Review:

* [[J. F. Jardine]], *Persistent homotopy theory* (2020) $[$[pdf](https://www.uwo.ca/math/faculty/jardine/lectures/persist-OSU-beamer.pdf), [[Jardine-PersistentHomotopy.pdf:file]]$]$

Further discussion:

* [[Facundo Mémoli]], [[Ling Zhou]], *Persistent Homotopy Groups of Metric Spaces* $[$[arXiv:1912.12399](https://arxiv.org/abs/1912.12399), [talk](Center+for+Quantum+and+Topological+Systems#ZhouAtHomotopicalPerspectivesOnTDAJune2022)$]$

Discussion with focus on the [[van Kampen theorem]], [[excision]] and the [[Hurewicz theorem]] in persistent homotopy:

* Mehmet Ali Batan, Mehmetcik Pamuk, Hanife Varli, *Persistent Homotopy* $[$[arXiv:1909.08865](https://arxiv.org/abs/1909.08865)$]$




[[!include cohomotopy in topological data analysis -- references]]



[[!redirects persistent homotopy theory]]

[[!redirects persistent homotopy type]]
[[!redirects persistent homotopy types]]

