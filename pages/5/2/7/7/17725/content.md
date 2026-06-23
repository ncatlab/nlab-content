
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents 

## Idea

In [[synthetic topology]] done as a branch of [[constructive mathematics]], a *dominance* is a set $\Sigma$ that functions as an analogue of the [[Sierpinski space]].  In particular, it allows us to define synthetically a notion of [[open subset]]: $\Sigma$ is a [[subset]] of the set of [[truth values]] $\Omega$, and a subset of a set $A$ is called "open" if its classifying map $A\to \Omega$ lands in $\Sigma$.

The name *dominance* is meant to evoke that the set is used to define the domains of a class of [[partial functions]]. I.e., in synthetic topology the partial functions whose domain is an open set and in [[synthetic computability theory]] the domains of [[computable functions|partial computable functions]]. 

## Definition

Let $\Omega$ be the set of [[truth values]].  A **dominance** is a subset $\Sigma\subseteq \Omega$ such that

1. $\top \in \Sigma$, and
1. If $U\in\Sigma$ and $P\in\Omega$ and $U\Rightarrow (P\in \Sigma)$, then $U\wedge P \in \Sigma$.

The second condition implies that $\Sigma$ is closed under binary [[meets]] $\wedge$, and hence is a sub-meet-[[semilattice]] of $\Omega$.  In [[type theory|type-theoretic]] language, the second condition says that $\Sigma$ is closed under [[dependent sums]].

The elements of $\Sigma$ are called **open** truth values.

## Open subsets

We define a subset $U\subseteq A$ of an arbitrary set $A$ to be **open** if for each $x\in A$, the proposition "$x\in U$" is an open truth value.  The second condition above is equivalent to saying that if $U\subseteq A$ is open and also $V\subseteq U$ is open, then $V\subseteq A$ is open.

Note that for any function $f:A\to B$, the preimage of any open set is open, since $(x\in f^{-1}(U))\iff (f(x) \in U)$.  Thus, any function is "[[continuous function|continuous]]" with respect to this "intrinsic topology."

## Overt sets

It is hard to get very far without an additional assumption that $\Sigma$ is closed under some [[joins]] as well.  However, if it were closed under *all* joins, then it would be all of $\Omega$, since any $P\in \Omega$ is the join $\bigvee_{i\in \{\star | P\}} \top$.

Given a dominance $\Sigma$, we say that a set $I$ is **overt** if $\Sigma$ is closed under $I$-indexed joins.  (This is related to, but not identical to, the notion of [[overt space]].)  In general it is reasonable to expect [[discrete object|discrete]] sets to be overt in this sense.  In some frameworks such as [[spatial type theory]] there is a formal notion of "discrete" and we can actually assert that all discrete sets are overt.   Otherwise we can assume that specific sets that we expect to be discrete are overt.  For instance, we might assume that:

* The [[empty set]] is overt, i.e. $\bot\in\Sigma$.
* The [[boolean domain]] is overt, i.e. $\Sigma$ is also a sub-join-semilattice of $\Omega$.
* The [[natural numbers]] are overt, i.e. $\Sigma$ is closed under countable joins in $\Omega$.

## Examples

* The singleton $\{\top\}$ is a dominance, for which only singletons are overt.

* The [[boolean domain]] $\{\bot,\top\}$ is a dominance.  This is the smallest dominance such that the empty set is overt and the smallest dominance such that the boolean domain is overt. (In [[classical mathematics]], of course, this and the previous example are the only two dominances, and the theory trivializes.)

* The set of [[quasidecidable propositions]] $\Sigma$ is a dominance. This is the smallest dominance such that the [[natural numbers]] $\mathbb{N}$ is overt. In the case that every [[quasidecidable proposition]] is a [[semidecidable proposition]], such as if we assume [[Rosolini's dominance axiom]] ([de Jong 2021](#deJong21)) or [[Rosolini propositional choice]] ([Escardo & Knapp 2017](#EK17), [de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26)), this dominance is called the *[[Rosolini dominance]]*. 

* Under certain assumptions, such as [[analytic LPO]], the set of all truth values of the form $x \gt 0$ for some [[Dedekind real number]] $x$ is also a dominance. 

## See also

* [[Sierpinski space]]

* [[streak]]

## References

*  [[Pino Rosolini]], *Continuity  and  Effectiveness  in  Topoi*, (PhD thesis, 1986), University of Oxford, ([pdf](https://www.researchgate.net/publication/35103849_Continuity_and_effectiveness_in_topoi))

* [[Martin Escardo]], *Topology via higher-order intuitionistic logic.*, unfinished paper, [pdf](http://www.cs.bham.ac.uk/~mhe/papers/pittsburgh.pdf)

* [[Martin Escardo]], *Synthetic  topology  of  data  types  and  classical  spaces.*  Electronic Notes in Theoretical Computer Science, 87:21--156, 2004.  [pdf](http://www.cs.bham.ac.uk/~mhe/papers/entcs87.pdf)

* {#EK17} [[Martín Escardó]], [[Cory Knapp]]. *Partial Elements and Recursion via Dominances in Univalent Type Theory.* In 26th EACSL Annual Conference on Computer Science Logic (CSL 2017). Leibniz International Proceedings in Informatics (LIPIcs), Volume 82, pp. 21:1-21:16, Schloss Dagstuhl – Leibniz-Zentrum für Informatik (2017) &lbrack;[10.4230/LIPIcs.CSL.2017.21](https://doi.org/10.4230/LIPIcs.CSL.2017.21)&rbrack;

* [[Andrej Bauer]] and Davorin Lesnik, *Metric Spaces in Synthetic Topology*, [pdf](http://math.andrej.com/wp-content/uploads/2010/01/csms_in_synthtop.pdf)

* Martin E. Bidlingmaier, Florian Faissole, [[Bas Spitters]], *Synthetic topology in Homotopy Type Theory for probabilistic programming*. Mathematical Structures in Computer Science, 2021;31(10):1301-1329. &lbrack;[doi:10.1017/S0960129521000165](https://doi.org/10.1017/S0960129521000165), [arXiv:1912.07339](https://arxiv.org/abs/1912.07339)&rbrack;

* {#deJong21} [[Tom de Jong]]. *Semidecidable propositions*. [[Agda]] code with comments, 2021. ([URL](https://martinescardo.github.io/TypeTopology/NotionsOfDecidability.SemiDecidable.html)).

* {#JKMF26} [[Tom de Jong]], [[Nicolai Kraus]], [[Aref Mohammadzadeh]], [[Fredrik Nordvall Forsberg]], *Generalized Decidability via Brouwer Trees* ([arXiv:2602.10844](https://arxiv.org/abs/2602.10844))

[[!redirects dominance]]
[[!redirects dominances]]
[[!redirects open truth value]]
[[!redirects open truth values]]
[[!redirects open proposition]]
[[!redirects open propositions]]
