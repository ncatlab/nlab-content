
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

*Persistent homotopy* studies [[homotopy types]] (of [[topological spaces]]) as a parameter varies, hence it studies [[filtered object in an (infinity,1)-category|filtered]] [[homotopy types]] (of [[filtered topological spaces]]), which focus on which elements of [[homotopy groups]] at given stage *persist* how far through the filtering to later stages. 
A key application is to [[Vietoris-Rips complexes]] of discrete subsets in a [[metric space]]. 

Notably in [[topological data analysis]] (TDA) these VRcomplexes arise as "point clouds" of datapoints and the corresponding persistent homotopy is thought to detect relevant structure hidden in such data. As such it refines the traditional use of [[persistent homology]] in TDA.

Persistent homotopy theory is to [[persistent homology]] as 
[[homotopy theory]] is to [[homology theory]]. 
In general, [[homotopy]] is a finer invariant than [[homology]]: the former sees the full [[homotopy type]] of a [[topological space]], the latter at most the underlying [[stable homotopy type]].

In other words, homology involves a kind of linearization or [[abelianization]] which loses information that is retained in the homotopy type. Therefore persistent homotopy is in general a finer invariant of [[filtered topological spaces]] than [[persistent homology]].  In fact, traditional [[persistent homology]] considers only *[[ordinary homology]]* which is the coarsest of all [[generalized homology]] invariants. Hence between the coarse invariant of [[persistent homology]] and the fine invariants of persistent homotopy are intermediate invariant that would deserve to be called *persistent generalized homology* -- but these have not yet found much attention.

See also the persistent *[[Cohomotopy|co-homotopy]]* [below](#CohomotopyInTopologicalDataAnalysisReferences).

## Related concepts

* [[Vietoris-Rips complex]]

* [[homotopy theory]]

* [[parameterized homotopy theory]]

* [[persistent homology]]

* [[filtered topological space]]

## References

### General

* [[Andrew J. Blumberg]], [[Michael Lesnick]], *Universality of the Homotopy Interleaving Distance* $[$[arXiv:1705.01690](https://arxiv.org/abs/1705.01690)$]$


* [[J. F. Jardine]], *Data and homotopy types* $[$[arXiv:1908.06323](https://arxiv.org/abs/1908.06323)$]$


* [[J. F. Jardine]], *Persistent homotopy theory* (2020) $[$[pdf](https://www.uwo.ca/math/faculty/jardine/lectures/persist-OSU-beamer.pdf), [[Jardine-PersistentHomotopy.pdf:file]]$]$


* [[Facundo Mémoli]], [[Ling Zhou]], *Persistent Homotopy Groups of Metric Spaces* $[$[arXiv:1912.12399](https://arxiv.org/abs/1912.12399), [talk](Center+for+Quantum+and+Topological+Systems#ZhouAtHomotopicalPerspectivesOnTDAJune2022)$]$


[[!include cohomotopy in topological data analysis -- references]]



[[!redirects persistent homotopy theory]]

[[!redirects persistent homotopy type]]
[[!redirects persistent homotopy types]]

