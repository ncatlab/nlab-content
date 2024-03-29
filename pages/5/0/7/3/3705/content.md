

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

##Idea
A **subtopos** of a topos is a generalization of the concept of a subspace of a [[topological space]].

##Definition
For $\mathcal{E}$ a [[topos]], a **subtopos** is another topos $\mathcal{F}$ equipped with a  [[geometric embedding]] $\mathcal{F} \hookrightarrow \mathcal{E}$.

If this is an [[open geometric morphism]] (or an [[essential geometric morphism]]) one speaks of an **[[open subtopos]]** (an **[[essential subtopos]]**, respectively, also called a _[[level of a topos]]_).


##Properties

### Sheaves, localization, closure and reflection

If $\mathcal{E}$ is an [[elementary topos]] then subtoposes correspond to [[Lawvere-Tierney topologies]] $j$ on $\mathcal{E}$,  to [[localization|localizations]] of $\mathcal{E}$ as well as to [[closure operator|universal closure operators]] on $\mathcal{E}$.

### For classifying toposes

Every Grothendieck topos $\mathcal{E}$ over $Set$ is (equivalent to) the [[classifying topos]] of some [[geometric theory]] $T$ and it can be shown that subtoposes of $\mathcal{E}$ correspond precisely to **deductively closed quotient theories** of $T$ ([Caramello (2009)](#Caramello09); thm. 3.6) i.e. passage to a subtopos corresponds to adding further geometric [[axioms]] to $T$ - localizing geometrically amounts to theory refinement logically.


### The lattice of subtoposes
 {#LatticeOfSubtoposes}

The inclusions induce an ordering on the subtoposes of $\mathcal{E}$ that makes them a [[lattice]] with a [[co-Heyting algebra]] structure i.e. the [[join]] operator has a [[left adjoint]] _[[subtraction]]_ operator. This corresponds to a dual [[Heyting algebra]] structure on the [[Lawvere-Tierney topologies]].

The lattice structure is further analyzed in ([Johnstone (2002)](#Johnstone02), [Caramello (2009)](#Caramello09)). We contend us to report

+-- {: .num_prop #subtopos_meet}
###### Proposition
Let $Sh_j(\mathcal{E})$, $Sh_k(\mathcal{E})$ be two subtoposes of a topos  $\mathcal{E}$ and $j,k$ the corresponding topologies with $j\vee k$ their join in the lattice of topologies. Then the following holds: $Sh_j(\mathcal{E})\wedge Sh_k(\mathcal{E})=Sh_{j\vee k}(\mathcal{E})=Sh_j(\mathcal{E})\cap Sh_k(\mathcal{E})$.
=--

(cf. [Johnstone (2002)](#Johnstone02), p.217). In other words, the meet of two subtoposes is just their intersection (and is equivalently given by the subtopos corresponding to the join of their topologies).

+-- {: .num_prop #BooleantoposesAreAtoms}
###### Proposition

The _[[atoms]] in the lattice of subtoposes of $\mathcal{E}$ are precisely the two-valued [[Boolean topos|Boolean]]  subtoposes_ of $\mathcal{E}$.

=--

([Caramello (2009)](#Caramello09); prop. 10.1). This follows from the fact that two-valued and Boolean toposes are opposite extremes when it comes to dense subtoposes: in a two-valued topos every non-trivial subtopos is dense, whereas a Boolean topos has no non-trivial dense subtopos (cf. at [[dense subtopos]] for further details).

## Related pages

* [[open subtopos]]

* [[closed subtopos]]

* [[locally closed subtopos]]

* [[dense subtopos]]

* [[level]]

* [[co-Heyting boundary]]

* [[Artin gluing]]

##References

* {#SGA4}[[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, LNM **269** Springer Heidelberg 1972. (expos&#233; IV, section 9, pp.431ff)

* {#BK91}[[Francis Borceux|F. Borceux]], M. Korostenski, _Open Localizations_ , JPAA **74** (1991) pp.229-238.

* {#Caramello09} [[Olivia Caramello|O. Caramello]], pp.15,58 of _Lattices of theories_,  (2009). ([arXiv:0905.0299](http://arxiv.org/abs/0905.0299))

* H. Forssell, _Subgroupoids and quotient theories_ , TAC **28** no.18 (2013) pp.541-551. ([pdf](http://www.emis.de/journals/TAC/volumes/28/18/28-18.pdf))

* {#Johnstone02}[[Peter Johnstone]], _Sketches of an [[Elephant]] I_, Oxford UP 2002. (pp.195-223)

* {#Johnstone77}[[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977. (Dover reprint 2014, section 3.5)

* {#KL89}[[G. M. Kelly]], [[William Lawvere|F. W. Lawvere]], _On the Complete Lattice of Essential Localizations_ , Bull. Soc. Math. de Belgique **XLI** (1989) 261-299 &lbrack;[[Kelly-Lawvere_EssentialLocalizations.pdf:file]]&rbrack;


[[!redirects Subtopos]]
[[!redirects subtoposes]]
[[!redirects Subtoposes]]

[[!redirects lattice of subtoposes]]
[[!redirects lattices of subtoposes]]

[[!redirects subtopos lattice]]
[[!redirects subtopos lattices]]
