
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

## Definition

A [[proposition]] or [[truth value]] $P$ is **semi-decidable** or **semidecidable** if and only if [[existential quantifier|there exists]] a [[sequence]] of [[booleans]] $f \in 2^\mathbb{N}$ such that $P$ if and only if there exists a natural number $x \in \mathbb{N}$ such that $f(x) = 1$. 

$$\mathrm{isSemiDecidable}(P) \coloneqq \exists f \in 2^\mathbb{N}.P \iff \exists x \in \mathbb{N}.f(x) = 1$$

The set of all semi-decidable propositions is typically called the **[[Rosolini dominance]]**, though it may not be a [[dominance]] without certain assumptions such as [[countable choice]] or [[excluded middle]]. 

If the [[foundations of mathematics]] has the [[Cauchy real numbers]] $\mathbb{R}_C$ as well, then $P$ is semideciable if and only if there exists a Cauchy real number $x \in \mathbb{R}_C$ such that $P$ if and only if $x \gt 0$.

$$\mathrm{isSemiDecidable}(P) \coloneqq \exists x \in \mathbb{R}_C.P \iff x \gt 0$$

The [[limited principle of omniscience]] for the [[natural numbers]] $\mathrm{LPO}_\mathbb{N}$ implies that every semi-decidable proposition is a [[decidable proposition]]. 

### In dependent type theory

In dependent type theory, the definition of semi-decidable makes sense for any type, not just the mere propositions. However, like many other definitions in [[dependent type theory]], one has to make sure to use an [[equivalence of types]] instead of [[logical equivalence]] in the definition of a semi-decidable type; this ensures that, like for decidable types, all semi-decidable types are propositions. 

\begin{definition}
A type $P$ is semi-decidable if [[existential quantifier|there exists]] a [[sequence]] of [[booleans]] $f:\mathbb{N} \to \mathrm{bool}$ such that $P$ is equivalent to that there exists a natural number $x:\mathbb{N}$ such that $f(x) = 1$. 

$$\mathrm{isSemiDecidable}(P) \coloneqq \left[\sum_{f:\mathbb{N} \to \mathrm{bool}} P \simeq \left[ \sum_{x:\mathbb{N}}f(x) =_{\mathrm{bool}} 1\right]\right]$$
\end{definition}

where $[A]$ is the [[bracket type]] of the type $A$. 

There is also a partially untruncated version of this, which is the type 

$$\sum_{f:\mathbb{N} \to \mathrm{bool}} P \simeq \left[\sum_{x:\mathbb{N}}f(x) =_{\mathrm{bool}} 1\right]$$

of all boolean sequences $f$ for which $P$ is equivalent to there exists a natural number $x:\mathbb{N}$ such that $f(x) = 1$. 

## Generalizations

### Ordinal decidable propositions

Given an [[ordinal]] $\alpha$, there exists a notion of **$\alpha$-decidable propositions** ([de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26)), where the usual notion of semi-decidable proposition is an $(\omega + 1)$-decidable proposition. 

### Sierpiński semi-decidable propositions

Semi-decidable propositions are not closed under [[existential quantification]] over the [[natural numbers]]. The closure of semi-decidable propositions under the logical operations of finite [[conjunctions]] and [[existential quantification]] over the [[natural numbers]] are the **quasi-decidable propositions** ([Escardo 2020](#Escardo20)) or **Sierpiński semi-decidable propositions** ([de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26)). 

+-- {: .num_defn }
###### Definition
The **set of Sierpiński semi-decidable truth values** or **set of quasi-decidable truth values** $\Sigma$ is defined in the following equivalent ways:

* as the [[initial object|initial]] [[sigma-frame|$\sigma$-frame]]
* as the [[partial map classifier]] of [[generalized the|the]] set with one element, for the definition of the partial map classifier given in [Altinkirch, Danielsson, & Kraus 2016](#ADK16)
* as the [[free object|free]] [[omega-cpo|$\omega$-cpo]] on the [[boolean domain]]
* [[impredicative mathematics|impredicatively]] as the [[intersection]] of all [[subobject|sub]]-$\sigma$-frames of the [[frame of truth values]] $\Omega$
=--

Here a [[subobject|sub]]-$\sigma$-frame of $\Omega$ is one that is closed under [[existential quantifiers]] on the [[natural numbers]].  

The set of Sierpiński semi-decidable truth values is also called **[[Sierpiński space]]** ([Altinkirch, Danielsson, & Kraus 2016](#ADK16), [Gilbert 2017](#Gilbert17), [Bidlingmaier, Faissole, & Spitters 2019](#BFS19)) or the **Sierpiński type** ([de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26)). 

> Comment: since the set of Sierpiński semi-decidable truth values always forms a [[dominance]], perhaps it can be called the **Sierpinski dominance**, though this term is not yet used in the literature. The term *Sierpiński space* is overloaded since it is more commonly used to refer to the [[topological space]] of the [[set of truth values]] equipped with the [[Scott topology]], and the term *Sierpiński type* has type theoretic connotations that are not appropriate in [[set theory]] based foundations. 

+-- {: .num_defn }
###### Definition
A **Sierpiński semi-decidable proposition** or **quasi-decidable proposition** is a [[proposition]] $P$ such that there exist an element $p \in \Sigma$ such that $P$ holds [[if and only if]] $p = \top$, where $\top$ is the [[top]] of $\Sigma$. 
=--

The set of Sierpiński semi-decidable truth values $\Sigma$ sits in a hierarchy of subsets of the set of truth values:

$$\mathbb{2} \subseteq \Sigma^0_1 \subseteq \Sigma \subseteq \Omega$$

where $\mathbb{2}$ is the [[boolean domain]], $\Sigma^0_1$ is the set of [[semi-decidable truth values]] of the usual notion, and $\Omega$ is the set of all truth values.

The set of Sierpiński semi-decidable truth values is an important structure in [[constructive mathematics|constructive]] [[topology]] and [[real analysis]], as it represents the set of [[open truth values]] in [[synthetic topology]] ([Bidlingmaier, Faissole & Spitters 2019](#BFS19)) and is used to construct a distinct and smaller version of the [[Dedekind real numbers]] ([Univalent Foundations Project 2013](#UFP13), [Gilbert 2017](#Gilbert17), [Bidlingmaier, Faissole & Spitters 2019](#BFS19)) that is not provably equivalent to either the usual [[Dedekind real numbers]] or the [[Cauchy real numbers]] in the absence of [[excluded middle]] or [[countable choice]]. Unlike the [[Rosolini dominance]], the set of Sierpiński semi-decidable truth values is always a [[dominance]]. 

In [[classical mathematics]], and in [[constructive mathematics]] which accept the [[limited principle of omniscience]], the set of Sierpiński semi-decidable truth values is just the [[boolean domain]] $\mathbb{2}$; in fact, that the [[boolean domain]] is the set of Sierpiński semi-decidable truth values is equivalent to the [[limited principle of omniscience]]. In [[classical mathematics]] and in [[constructive mathematics]] which accepts [[countable choice]] or the [[weak countable choice]] axiom $\mathrm{AC}_{\mathbb{N}, \mathbb{2}}$, the set of Sierpi&#324;ski semi-decidable truth values is just the [[Rosolini dominance]]. The [[limited principle of omniscience]] also implies that the set of Sierpiński semi-decidable truth values is the [[Rosolini dominance]] since both are equivalent to the [[boolean domain]] under the assumption. 

## Related concepts

* [[decidable proposition]]

* [[proposition]], [[truth value]]

* [[synthetic topology]], [[dominance]]

* [[sigma-frame|$\sigma$-frame]]

## References

* [[Andrej Bauer]], [[Davorin Lešnik]], _Metric Spaces in Synthetic Topology_, 2010 ([pdf](http://math.andrej.com/wp-content/uploads/2010/01/csms_in_synthtop.pdf))

* {#EK17} [[Martín Escardó]], [[Cory Knapp]]. *Partial Elements and Recursion via Dominances in Univalent Type Theory.* In 26th EACSL Annual Conference on Computer Science Logic (CSL 2017). Leibniz International Proceedings in Informatics (LIPIcs), Volume 82, pp. 21:1-21:16, Schloss Dagstuhl – Leibniz-Zentrum für Informatik (2017) &lbrack;[10.4230/LIPIcs.CSL.2017.21](https://doi.org/10.4230/LIPIcs.CSL.2017.21)&rbrack;

* {#Escardo20} [[Martin Escardo]]. *Quasidecidable propositions*. [[Agda]] code with comments, 2020. ([URL](https://cs.bham.ac.uk/~mhe/TypeTopology/NotionsOfDecidability.QuasiDecidable.html)).

* {#JKMF26} [[Tom de Jong]], [[Nicolai Kraus]], [[Aref Mohammadzadeh]], [[Fredrik Nordvall Forsberg]], *Generalized Decidability via Brouwer Trees* ([arXiv:2602.10844](https://arxiv.org/abs/2602.10844))

* {#UFP13} Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

* {#ADK16} [[Thorsten Altenkirch]], [[Nils Anders Danielsson]], [[Nicolai Kraus]], Partiality, Revisited: The Partiality Monad as a Quotient Inductive-Inductive Type ([abs:1610.09254](https://arxiv.org/abs/1610.09254))

* {#Gilbert17} Gaëtan Gilbert. *Formalising real numbers in homotopy type theory.* In CPP’17, Proceedings of the 6th ACM SIGPLAN Conference on Certified Programs and Proofs, pages 112–124, 2017. &lbrack;[doi:10.1145/3018610.3018614](https://doi.org/10.1145/3018610.3018614)&rbrack;.

* {#BFS19} Martin E. Bidlingmaier, Florian Faissole, [[Bas Spitters]], *Synthetic topology in Homotopy Type Theory for probabilistic programming*. Mathematical Structures in Computer Science, 2021;31(10):1301-1329. &lbrack;[doi:10.1017/S0960129521000165](https://doi.org/10.1017/S0960129521000165), [arXiv:1912.07339](https://arxiv.org/abs/1912.07339)&rbrack;

[[!redirects semi-decidable]]

[[!redirects semidecidable]]

[[!redirects semi-decidable proposition]]
[[!redirects semi-decidable propositions]]

[[!redirects semidecidable proposition]]
[[!redirects semidecidable propositions]]

[[!redirects semi-decidable truth value]]
[[!redirects semi-decidable truth values]]

[[!redirects semidecidable truth value]]
[[!redirects semidecidable truth values]]

[[!redirects semi-decidable type]]
[[!redirects semi-decidable types]]

[[!redirects semidecidable type]]
[[!redirects semidecidable types]]

[[!redirects quasi-decidable]]

[[!redirects quasidecidable]]

[[!redirects quasi-decidable proposition]]
[[!redirects quasi-decidable propositions]]

[[!redirects quasidecidable proposition]]
[[!redirects quasidecidable propositions]]

[[!redirects quasi-decidable truth value]]
[[!redirects quasi-decidable truth values]]

[[!redirects quasidecidable truth value]]
[[!redirects quasidecidable truth values]]

[[!redirects set of quasi-decidable propositions]]
[[!redirects set of quasidecidable propositions]]

[[!redirects set of quasi-decidable truth values]]
[[!redirects set of quasidecidable truth values]]

[[!redirects quasi-decidable type]]
[[!redirects quasi-decidable types]]

[[!redirects quasidecidable type]]
[[!redirects quasidecidable types]]

[[!redirects Sierpinski semidecidable]]
[[!redirects Sierpinski semi-decidable]]
[[!redirects Sierpiński semidecidable]]
[[!redirects Sierpiński semi-decidable]]

[[!redirects Sierpinski-semidecidable]]
[[!redirects Sierpinski-semi-decidable]]
[[!redirects Sierpiński-semidecidable]]
[[!redirects Sierpiński-semi-decidable]]

[[!redirects Sierpinski semi-decidable proposition]]
[[!redirects Sierpinski semi-decidable propositions]]
[[!redirects Sierpiński semi-decidable proposition]]
[[!redirects Sierpiński semi-decidable propositions]]

[[!redirects Sierpinski-semi-decidable proposition]]
[[!redirects Sierpinski-semi-decidable propositions]]
[[!redirects Sierpiński-semi-decidable proposition]]
[[!redirects Sierpiński-semi-decidable propositions]]

[[!redirects Sierpinski semidecidable proposition]]
[[!redirects Sierpinski semidecidable propositions]]
[[!redirects Sierpiński semidecidable proposition]]
[[!redirects Sierpiński semidecidable propositions]]

[[!redirects Sierpinski-semidecidable proposition]]
[[!redirects Sierpinski-semidecidable propositions]]
[[!redirects Sierpiński-semidecidable proposition]]
[[!redirects Sierpiński-semidecidable propositions]]

[[!redirects Sierpinski semi-decidable truth value]]
[[!redirects Sierpinski semi-decidable truth values]]
[[!redirects Sierpiński semi-decidable truth value]]
[[!redirects Sierpiński semi-decidable truth values]]

[[!redirects Sierpinski-semi-decidable truth value]]
[[!redirects Sierpinski-semi-decidable truth values]]
[[!redirects Sierpiński-semi-decidable truth value]]
[[!redirects Sierpiński-semi-decidable truth values]]

[[!redirects Sierpinski semidecidable truth value]]
[[!redirects Sierpinski semidecidable truth values]]
[[!redirects Sierpiński semidecidable truth value]]
[[!redirects Sierpiński semidecidable truth values]]

[[!redirects Sierpinski-semidecidable truth value]]
[[!redirects Sierpinski-semidecidable truth values]]
[[!redirects Sierpiński-semidecidable truth value]]
[[!redirects Sierpiński-semidecidable truth values]]

[[!redirects set of Sierpinski semi-decidable propositions]]
[[!redirects set of Sierpinski-semi-decidable propositions]]
[[!redirects set of Sierpinski semidecidable propositions]]
[[!redirects set of Sierpinski-semidecidable propositions]]

[[!redirects set of Sierpinski-semi-decidable truth values]]
[[!redirects set of Sierpinski semi-decidable truth values]]
[[!redirects set of Sierpiński-semidecidable truth values]]
[[!redirects set of Sierpiński semidecidable truth values]]

[[!redirects Sierpinski semi-decidable type]]
[[!redirects Sierpinski semi-decidable types]]
[[!redirects Sierpiński semi-decidable type]]
[[!redirects Sierpiński semi-decidable types]]

[[!redirects Sierpinski-semi-decidable type]]
[[!redirects Sierpinski-semi-decidable types]]
[[!redirects Sierpiński-semi-decidable type]]
[[!redirects Sierpiński-semi-decidable types]]

[[!redirects Sierpinski semidecidable type]]
[[!redirects Sierpinski semidecidable types]]
[[!redirects Sierpiński semidecidable type]]
[[!redirects Sierpiński semidecidable types]]

[[!redirects Sierpinski-semidecidable type]]
[[!redirects Sierpinski-semidecidable types]]
[[!redirects Sierpiński-semidecidable type]]
[[!redirects Sierpiński-semidecidable types]]

[[!redirects Sierpinski type]]
[[!redirects Sierpiński type]]

[[!redirects Sierpinski dominance]]
[[!redirects Sierpiński dominance]]

[[!redirects initial sigma-frame]]
[[!redirects initial sigma-frames]]
[[!redirects initial σ-frame]]
[[!redirects initial σ-frames]]