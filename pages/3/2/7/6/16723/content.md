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

A **locally closed subtopos** generalizes the concept of a [[locally closed set|locally closed subspace]] from topology to toposes.

## Definition

A [[subtopos]] $\mathcal{E}_j\hookrightarrow\mathcal{E}$ is called _locally closed_ if it is the meet $\mathcal{E}_j=\mathcal{E}_o\cap\mathcal{E}_c$ of an [[open subtopos]] $\mathcal{E}_o$ and a [[closed subtopos]] $\mathcal{E}_c$ in the lattice of subtoposes of $\mathcal{E}$.

## Properties

* Since $\mathcal{E}$ is closed as well as open in itself, its closed and open subtoposes are trivially locally closed.

* Since open and closed subtoposes are [[complement|complemented]] in the [[lattice of subtoposes]], the join of the complements $\bar\mathcal{E}_{o}\cup\bar\mathcal{E}_{c}$ provides a **complement** for a locally closed subtopos $\mathcal{E}_j=\mathcal{E}_o\cap\mathcal{E}_c$.

* $\mathcal{E}_j$ is locally closed iff $\mathcal{E}_j\hookrightarrow\mathcal{E}$ can be factored into an open followed by a closed inclusion.

* A locally closed subtopos of an [[exponentiable topos]] is itself exponentiable (cf. Johnstone ([2002](#J02), p.749)).

## Examples

* One way to realize a topos $\mathcal{E}_j$ as a locally closed subtoposes is by repeated [[Artin gluing]] to appropriate left exact functors $f_1:\mathcal{E}_j\to \mathcal {F}_1$ and $f_2:\mathcal{F}_2\to Gl(f_1)$. Then $\mathcal{E}$ is open in $Gl(f_1)$ which itself is closed in $Gl(f_2)$ whence by the above remark on factorisations $\mathcal{E}_j\hookrightarrow Gl(f_2)$ is locally closed.

* Locally closed subspaces $Y$ of topological spaces $X$ yield locally closed subtoposes of the corresponding sheaf topos $Sh(Y)\hookrightarrow Sh(X)$ e.g. let $X$ be the space on $\{a,b,c\}$ with non-trivial open subsets $\{a\}$, $\{a,b\}$. Then $\{b\}$ as the intersection of $\{a,b\}$ with the closed subset $\{b,c\}$ is a locally closed subset to which a neither closed nor open but locally closed copy of $Set$ corresponds in the lattice of subtoposes of $Sh(X)$.

## Related entries

* [[open subtopos]]
* [[closed subtopos]]
* [[dense subtopos]]
* [[locally closed set]]
* [[co-Heyting boundary]]

## References

* [[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, LNM **269** Springer Heidelberg 1972. (Expos&#233; IV, ex.9.4.9., pp.462-463)

* [[Peter Johnstone]], _Conditions Related to de Morgan's Law_ , pp.479-491 in LNM **753** Springer Heidelberg 1979.

* {#J02}[[Peter Johnstone]], _Sketches of an Elephant vol. 2_ , Cambridge UP 2002.

* [[Anders Kock|A. Kock]], T. Plewe, _Glueing analysis for complemented subtoposes_ , TAC **2** (1996) pp.100-112. ([pdf](http://www.tac.mta.ca/tac/volumes/1996/n9/n9.pdf))
