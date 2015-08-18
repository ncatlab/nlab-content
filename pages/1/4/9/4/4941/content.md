
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Definition

For $S \subset X$ a [[subset]] of a [[topological space]] $X$, a, **interior point** of $S$ is a point $x \in S$ which has a [[neighbourhood]] in $X$ that is contained in $S$. The union of all interior points is the **interior** $S^\circ$ of $S$. It can be defined as the largest open set contained in $S$. 

In general, we have $S^\circ \subseteq S$.  $S$ is [[open subset|open]] if and only if $S^\circ = S$, so that in particular $S^{\circ\circ} = S^\circ$. This makes the interior operator $P(X) \to P(X): S \mapsto S^\circ$ a [[co-closure operator]]. It also satisfies the equations $(S \cap T)^\circ = S^\circ \cap T^\circ$ and $X^\circ = X$. Moreover, any co-closure operator $c$ on $P(X)$ that preserves finite intersections must be the interior operation for some topology, namely the family consisting of fixed points of $c$; this gives one of many equivalent ways to define a topological space. 

Compare the [[topological closure]] $\bar{S}$ and [[frontier]] $\partial S = \bar{S} \setminus S^\circ$.

## Remark

The _interior of a subtopos_ $\mathcal{E}_j$ of a [[Grothendieck topos]] $\mathcal{E}$, as well as the [[dense subtopos|exterior]], were defined in an exercise in [SGA4](#SGA4): $Int(\mathcal{E}_j)$ as the smallest [[open subtopos]] contained in $\mathcal{E}_j$. The boundary of a subtopos is then naturally defined as the subtopos complementary to the (open) join of the exterior and interior subtoposes in the [[lattice of subtoposes]].

## Related entries 

* [[ionad]]

## Reference

* [[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, LNM **269** Springer Heidelberg 1972. (expos&#233; IV, exercise 9.4.8, pp.461-462) {#SGA4}


[[!redirects interior]]
[[!redirects interiors]]
[[!redirects topological interior]]
[[!redirects topological interiors]]
