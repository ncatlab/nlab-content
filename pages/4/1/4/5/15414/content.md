
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
* automatic table of contents goes here
{:toc}


[[!redirects QD topos]]
[[!redirects locally decidable object]]

##Idea
Loosely speaking a _locally decidable topos_ is a topos that is locally Boolean. Whereas in a [[Boolean topos]] every object is decidable, in a locally decidable topos every object is a quotient of a [[decidable object]]. This results in a reasonable approximation to the concept of 'being almost Boolean'.

In Lawvere's approach to cohesion locally decidable toposes are one of the principal classes of **petit toposes** (Lawvere 1991).
In the 1991 paper Lawvere also hypothesizes the discrete base topos $\mathcal{S}$ that he contrasts with the cohesive topos of spaces, to be locally decidable.[^fine]

[^fine]: Lawvere uses the term 'QD'-topos ( _quotient of decidable_) for 'locally
decidable topos' in this paper. He also uses 'SUD'-object (from _separable-unramified-decidable_ to indicate equivalent concepts in algebra-topology-logic) for what we call a locally decidable object. In later papers Lawvere uses also the terms 'locally separable'or 'adequately separable'. The idea to take a locally decidable base topos is probably suggested by [[Galois theory]] where 'locally decidable' corresponds roughly to 'product of separable field extensions' for an algebra over a field $k$. This also connects the notion '[[decidable object|decidable]]' via Grothendieck's Galois theory to the topological notion 'unramified'.

##Definition
An object $X$ in a topos $\mathcal{E}$ is called _locally decidable_ (or, a _quotient of a decidable object_) iff there is an epimorphism $Y\twoheadrightarrow X$ such that $Y$ is a [[decidable object]]. $\mathcal{E}$ is called _locally decidable_ iff every object $X$ is locally decidable.

##Examples

* The [[classifying topos]] $Set[\mathbf{D}]=[FinSet_{mono},Set]$ for the [[theory of decidable objects]] $\mathbf{D}$ is locally decidable. Here $FinSet_{mono}$ is the category of finite sets and monomorphisms, whose opposite category is the carrier of the site for the so called (Myhill-) _[[Schanuel topos]]_.

* Every [[localic topos]] is locally decidable.

* For every [[Grothendieck topos]] $\mathcal{E}$ the full subcategory $\mathcal{E}_{QD}$ of locally decidable objects is a locally decidable topos.

##Properties

* **Proposition**. A topos $\mathcal{E}$ is locally decidable iff there is a [[localic topos|localic]] geometric morphism to a Boolean topos, or iff $\mathcal{E}$ has a site $(\mathcal{C}, J)$ with all morphisms in $\mathcal{C}$ epic.

* Locally decidable toposes are 'co-&#233;tendues' in the sense that for a small $\mathcal{C}$ the functor category $[\mathcal{C},Set]$ is locally decidable precisely if $[\mathcal{C}^{op},Set]$ is an [[étendue]]. Also the all-epic-site property is dual to the all-monic-site property of &#233;tendues. Both concepts are subsumed under the notion of having a (sub canonical) site representation with no (non-trivial) [[idempotents]] (McLarty 2006, Lawvere 2007,2008).

##Related concepts

* [[Boolean topos]]
* [[petit topos]]
* [[étendue]]
* [[decidable object]]
* [[theory of decidable objects]]


##References

* [[Peter Freyd]], _All topoi are localic - or, why permutation models prevail_ , JPAA **46** (1987) pp.49-58.

* [[Peter Johnstone]], _Quotients of decidable objects in a topos_ , Math. Proc. Camb. Phil. Soc. **93** (1983) pp.409-419.

* [[Peter Johnstone]], _How general is a generalized space?_ , London Math. Soc. LNS **93** (1985) pp.77-111.

* [[Peter Johnstone]], _Sketches of an Elephant II_, Oxford UP 2002. (sec. C5.4 pp.792-803)

* [[F. William Lawvere]], _Qualitative Distinctions between some Toposes of Generalized Graphs_ , Cont. Math. **92** (1989) pp.261-299.

* [[F. William Lawvere]], _Some Thoughts on the Future of Category Theory_ , pp.1-13 in Springer LNM vol. 1488 (1991).

* [[F. William Lawvere]], _Axiomatic Cohesion_ , TAC **19** no. 3 (2007) pp.41-49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

* [[F. William Lawvere]], _Cohesive Toposes: Combinatorial and Infinitesimal Cases_, Como Ms. 2008. ([pdf](http://comocategoryarchive.com/Archive/temporary_new_material/FWLawvere-Cohesive-Toposes-Como-January-2008.pdf))

* [[Colin McLarty]], _Every Grothendieck Topos has a One-Way Site_ , TAC **16** no. 5 (2006) pp.123-126. ([pdf](http://www.tac.mta.ca/tac/volumes/16/5/16-05.pdf))