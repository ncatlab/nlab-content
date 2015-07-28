+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea 

A **locally closed subtopos** generalizes the concept of a locally closed subspace in topology to toposes.

## Definition

A [[subtopos]] $\mathcal{E}_j\hookrightarrow\mathcal{E}$ is called _locally closed_ if it is the meet $\mathcal{E}_j=\mathcal{E}_o\cap\mathcal{E}_c$ of an [[open subtopos]] $\mathcal{E}_o$ and a [[closed subtopos]] $\mathcal{E}_c$ in the lattice of subtoposes of $\mathcal{E}$.

## Properties

* Since open and closed subtoposes are complemented in the lattice of subtoposes, the join of the complements $\bar\mathcal{E}_{o}\cup\bar\mathcal{E}_{c}$ provides a **complement** for a locally closed subtopos $\mathcal{E}_j=\mathcal{E}_o\cap\mathcal{E}_c$.

* $\mathcal{E}_j$ is locally closed iff $\mathcal{E}_j\hookrightarrow\mathcal{E}$ can be factored into an open followed by a closed inclusion.

## Related entries

* [[open subtopos]]
* [[closed subtopos]]
* [[dense subtopos]]
* [[co-Heyting boundary]]

## References

* [[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, LNM **269** Springer Heidelberg 1972. (Expos&#233; IV, ex.9.4.9., pp.462-463)

* [[Anders Kock|A. Kock]], T. Plewe, _Glueing analysis for complemented subtoposes_ , TAC **2** (1996) pp.100-112. ([pdf](http://www.tac.mta.ca/tac/volumes/1996/n9/n9.pdf))
