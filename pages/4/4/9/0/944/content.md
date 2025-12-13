
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

+-- {: .num_defn }
###### Definition

The __Sierpi&#324;ski space__ $\Sigma$ is the [[topological space]] 

1. whose underlying set has two elements, say $\{0,1\}$,

1. whose set of [[open subsets]] is $\left\{ \emptyset, \{1\}, \{0,1\}  \right\}$.

(We could exchange "0" and "1" here, the result would of course be [[homeomorphism|homeomorphic]]).

Equivalently we may think of the underlying [[set]] as the set of [[classical mathematics|classical]] [[truth values]]  $\{\bot, \top\}$, equipped with the [[specialization topology]], in which $\{\bot\}$ is [[closed subset|closed]] and $\{\top\}$ is an [[open subset|open]] but not conversely.

The corresponding [[locale]] is given by the three-element frame $\{\bot \lt \omega \lt \top\}$.

=--


+-- {: .num_remark }
###### Remark

In [[constructive mathematics]], the Sierpi&#324;ski locale is given by the free frame over one element. More concretely, its opens are $O_{p \le q}$ indexed by pairs of truth values $(p, q)$ such that $p \le q$. The partial order is given by $O_{p \le q} \le O_{p' \le q'}$ iff $p \le p'$ and $q \le q'$. This is also the [[specialization topology|Alexandroff locale]] over the poset of *classical* truth values.

The corresponding topological space however, has the point set given by *all* truth values. The open subsets are $O_{p \le q} = \{\varphi \mid p \vee (q \wedge \varphi)\}$. Importantly, it is not homeomorphic to the Alexandroff topology on the set of truth values, or classical truth values.

=--

## Properties

### As a topological space

This Sierpinski space 

* is a [[contractible space]];

* is a [[locally contractible space]];

* has a [[focal point]];

* is a [[sober topological space]] (but not [[separation axiom|T1]]).

According properties are inherited by the [[Sierpinski topos]] and the [[Sierpinski (∞,1)-topos]] over $Sierp$.


### As a classifier for open/closed subspaces

The Sierpinski space $S$ is a classifier for [[open subspaces]] of a [[topological space]] $X$ in that for any open subspace $A$ of $X$ there is a unique [[continuous function]] $\chi_A: X \to S$ such that $A = \chi_A^{-1}(\top)$.  

Dually, it classifies [[closed subsets]] in that any closed subspace $A$ is $\chi_A^{-1}(\bot)$.  Note that the closed subsets and open subsets of $X$ are related by a [[bijection]] through [[complement|complementation]]; one gets a topology on the set of either by identifying the set with $\Top(X,\Sigma)$ for a suitable [[function space]] topology.  (This part does not work as well in [[constructive mathematics]].)

## Predicative Sierpi&#324;ski space
{#Predicative}

In [[constructive mathematics]], there is also a distinct version of Sierpi&#324;ski space which is only a [[sigma-frame|$\sigma$-frame]] ([Altinkirch, Danielsson, & Kraus 2016](#ADK16), [Gilbert 2017](#Gilbert17), [Bidlingmaier, Faissole, & Spitters 2019](#BFS19)). In general, this notion of Sierpi&#324;ski space will not coincide with the version defined above as a frame unless a classical axiom like [[excluded middle]] is assumed. This version of the Sierpi&#324;ski space is predicative in the sense that it does not require the use of impredicative definitions, and so can probably be called the *predicative Sierpi&#324;ski space* to distinguish it from the usual version of the Sierpi&#324;ski space defined above. 

This version of the Sierpi&#324;ski space is an important structure in [[constructive mathematics|constructive]] [[topology]] and [[real analysis]], as it represents the set of [[open propositions]] in [[synthetic topology]] ([Bidlingmaier, Faissole & Spitters 2019](#BFS19)) and is used to construct a distinct and smaller version of the [[Dedekind real numbers]] ([Univalent Foundations Project 2013](#UFP13), [Gilbert 2017](#Gilbert17), [Bidlingmaier, Faissole & Spitters 2019](#BFS19)) that is not provably equivalent to either the usual [[Dedekind real numbers]] or the [[Cauchy real numbers]] in the absence of [[excluded middle]] or [[countable choice]]. 

+-- {: .num_defn }
###### Definition
The **Sierpi&#324;ski space** $\Sigma$ is defined in the following equivalent ways:

* as the [[initial object|initial]] [[sigma-frame|$\sigma$-frame]]
* as the [[partial map classifier]] of [[generalized the|the]] set with one element, for the definition of the partial map classifier given in [Altinkirch, Danielsson, & Kraus 2016](#ADK16)
* as the [[free object|free]] [[omega-cpo|$\omega$-cpo]] on the [[boolean domain]]
* [[impredicative mathematics|impredicatively]] as the [[intersection]] of all [[subobject|sub]]-$\sigma$-frames of the $\sigma$-frame of [[truth values]] $\Omega$
=--

Here a [[subobject|sub]]-$\sigma$-frame of $\Omega$ is one that is closed under [[existential quantifiers]] on the [[natural numbers]]. 

In [[dependent type theory]], the first three definitions of the Sierpi&#324;ski space are formulated using [[higher inductive types]] or [[higher inductive-inductive types]]. 

The Sierpi&#324;ski space $\Sigma$ sits in a hierarchy of subsets of the set of truth values:

$$\mathbb{2} \subseteq \Sigma^0_1 \subseteq \Sigma \subseteq \Omega$$

where $\mathbb{2}$ is the [[boolean domain]] and $\Sigma^0_1$ is the set of [[semidecidable truth values]].

In [[classical mathematics]], and in [[constructive mathematics]] which accept the [[limited principle of omniscience]], the (underlying [[set]] of) Sierpi&#324;ski space is just the [[boolean domain]] $\mathbb{2}$; in fact, that the [[boolean domain]] is the (underlying [[set]] of) Sierpi&#324;ski space is equivalent to the [[limited principle of omniscience]]. In [[classical mathematics]] and in [[constructive mathematics]] which accepts [[countable choice]] or the [[weak countable choice]] axiom $\mathrm{AC}_{\mathbb{N}, \mathbb{2}}$, the Sierpi&#324;ski space is just the [[Rosolini dominance]]. The [[limited principle of omniscience]] also implies that the Sierpi&#324;ski space is the [[Rosolini dominance]] since both are equivalent to the [[boolean domain]] under the assumption. 

## Related concepts

* [[empty space]], [[point space]]

* [[Cantor space]]

* [[Sierpinski topos]], [[Sierpinski (∞,1)-topos]]

* [[Stone duality]]

* [[separation axioms in terms of lifting properties]]

* In [[synthetic topology]], an analogue of the Sierpinski space is called a [[dominance]].

* [[sigma-frame|$\sigma$-frame]]


## References

* Wikipedia, _[Sierpinski space](https://en.wikipedia.org/wiki/Sierpi%C5%84ski_space)_

* [[Paul Taylor]],  _Foundations for computable topology -- 7 The Sierpinski space_ ([html](http://www.paultaylor.eu/ASD/foufct/sierpinski.html))

* [[Andrej Bauer]], [[Davorin Lešnik]], *Metric spaces in synthetic topology* Annals of Pure and Applied Logic, Volume 163, Issue 2, February 2012, Pages 87-100 ([doi:10.1016/j.apal.2011.06.017](https://doi.org/10.1016/j.apal.2011.06.017))

* {#UFP13} Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

* {#ADK16} [[Thorsten Altenkirch]], [[Nils Anders Danielsson]], [[Nicolai Kraus]], Partiality, Revisited: The Partiality Monad as a Quotient Inductive-Inductive Type ([abs:1610.09254](https://arxiv.org/abs/1610.09254))

* {#Gilbert17} Gaëtan Gilbert. *Formalising real numbers in homotopy type theory.* In CPP’17, Proceedings of the 6th ACM SIGPLAN Conference on Certified Programs and Proofs, pages 112–124, 2017. &lbrack;[doi:10.1145/3018610.3018614](https://doi.org/10.1145/3018610.3018614)&rbrack;.

* {#BFS19} Martin E. Bidlingmaier, Florian Faissole, [[Bas Spitters]], *Synthetic topology in Homotopy Type Theory for probabilistic programming*. Mathematical Structures in Computer Science, 2021;31(10):1301-1329. &lbrack;[doi:10.1017/S0960129521000165](https://doi.org/10.1017/S0960129521000165), [arXiv:1912.07339](https://arxiv.org/abs/1912.07339)&rbrack;

[[!redirects Sierpinski space]]
[[!redirects Sierpiński space]]
[[!redirects Sierpinski topology]]
[[!redirects Sierpiński topology]]

[[!redirects predicative Sierpinski space]]
[[!redirects predicative Sierpiński space]]

[[!redirects initial sigma-frame]]
[[!redirects initial σ-frame]]
[[!redirects initial sigma frame]]