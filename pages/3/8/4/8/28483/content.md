
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

Semi-decidable propositions are not closed under [[existential quantification]] over the [[natural numbers]]: Given a [[predicate]] $P$ over the [[natural numbers]] where each $P(n)$ is semi-decidable for all $n \in \mathbb{N}$, the existential quantifier $\exists n \in \mathbb{N}.P(n)$ is not always semi-decidable. The closure of semi-decidable propositions under the logical operations of finite [[conjunctions]] and [[existential quantification]] over the [[natural numbers]] are the **quasidecidable propositions** ([Escardo 2020](#Escardo20)) or **Sierpiński semidecidable propositions** ([de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26)). 

The set of quasidecidable propositions is an important structure in [[constructive mathematics|constructive]] [[topology]] and [[real analysis]], as it represents the set of [[open propositions]] in [[synthetic topology]] ([Bidlingmaier, Faissole & Spitters 2019](#BFS19)) and is used to construct a distinct and smaller version of the [[Dedekind real numbers]] ([Univalent Foundations Project 2013](#UFP13), [Bidlingmaier, Faissole & Spitters 2019](#BFS19)) that is not provably equivalent to either the usual [[Dedekind real numbers]] or the [[Cauchy real numbers]] in the absence of [[excluded middle]] or [[countable choice]]. In addition, positivity (i.e. $0 \lt x$) of the [[HoTT book real numbers]] is quasidecidable ([Gilbert 2017](#Gilbert17)). 

The set of quasidecidable propositions is also used for the [[dominance]] in [[synthetic domain theory]], such as in the [[effective topos]] ([Sterling & Ye 2025](#SY25)), where by [[countable choice]] it coincides with the set of [[semidecidable propositions]] and is thus called the *[[Rosolini dominance]]*. However, unlike the set of semidecidable propositions, even in the absence of [[countable choice]], the set of quasidecidable propositions is always an $\mathbb{N}$-overt [[dominance]] ([Bidlingmaier, Faissole & Spitters 2019](#BFS19), [Escardo 2020](#Escardo20)). 

## Definition

+-- {: .num_defn }
###### Definition
The **set of Sierpiński semidecidable truth values** or **set of quasidecidable truth values** $\Sigma$ is defined in the following equivalent ways:

* as the [[initial object|initial]] [[sigma-frame|$\sigma$-frame]]
* as the [[omega-cpo|$\omega$-cpo]] completion of the [[partial order]] of the [[boolean domain]], see [Bidlingmaier, Faissole, & Spitters 2019](#BFS19)
* as the [[pointed object|pointed]] [[omega-cpo|$\omega$-cpo]] completion of the set with one element ([Bidlingmaier, Faissole, & Spitters 2019](#BFS19)), or equivalently the [[partial map classifier]] of [[generalized the|the]] set with one element, for the definition of the partial map classifier given in [Altinkirch, Danielsson, & Kraus 2016](#ADK16)
* [[impredicative mathematics|impredicatively]] as the smallest subset of the [[set of truth values]] $\Omega$ closed under [[truth]], [[falsehood]], and [[existential quantification]] over the [[natural numbers]], see [Escardo 2020](#Escardo20). 
=--

The set of quasidecidable truth values is also called **Sierpiński space** ([Altinkirch, Danielsson, & Kraus 2016](#ADK16), [Gilbert 2017](#Gilbert17), [Bidlingmaier, Faissole, & Spitters 2019](#BFS19)) or the **Sierpiński type** ([de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26)). 

> Comment: since the set of Sierpiński semi-decidable truth values always forms a [[dominance]], perhaps it can be called the **Sierpinski dominance**, though this term is not yet used in the literature. The term *[[Sierpiński space]]* is overloaded since it is more commonly used to refer to the [[topological space]] of the [[set of truth values]] equipped with the [[Scott topology]], and the term *Sierpiński type* has type theoretic connotations that are not appropriate in [[set theory]] based foundations. 

+-- {: .num_defn }
###### Definition
A **Sierpiński semidecidable proposition** or **quasidecidable proposition** is a [[proposition]] $P$ such that there exist an element $p \in \Sigma$ such that $P$ holds [[if and only if]] $p = \top$, where $\top$ is the [[top]] of $\Sigma$. 

$$\mathrm{isQuasiDecidable}(P) \coloneqq \exists p \in \Sigma.P \iff p = \top$$
=--

The set of quasidecidable truth values $\Sigma$ sits in a hierarchy of subsets of the set of truth values:

$$\mathbb{2} \subseteq \Sigma^0_1 \subseteq \Sigma \subseteq \Omega$$

where $\mathbb{2}$ is the [[boolean domain]], $\Sigma^0_1$ is the set of [[semi-decidable truth values]] of the usual notion, and $\Omega$ is the set of all truth values.

## Constructive taboos

There are a few constructive [[taboos]] related to the set of quasidecidable propositions. 

### Rosolini propositional choice

In [[classical mathematics]] and in [[constructive mathematics]] which accepts [[countable choice]], the set of quasidecidable propositions is equivalent to the [[Rosolini dominance]] ([Sterling & Ye 2025](#SY25), [de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26)). 

However, more generally, one cannot prove that the set of semidecdiable propositions is an $\mathbb{N}$-overt dominance and thus coincide with the set of quasidecidable propositions. That the set of semidecdiable propositions is $\mathbb{N}$-overt is equivalent to a form of choice called *[[Rosolini propositional choice]]* ([Escardo & Knapp 2017](#EK17)) or *[[Escardo-Knapp choice]]* ([de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26)). 

### LPO and Phoa's principle

In [[classical mathematics]], and in [[constructive mathematics]] which accept the [[limited principle of omniscience]] (LPO), the set of quasidecidable truth values is just the [[boolean domain]] $\mathbb{2}$. In fact, we have  the following: 

\begin{theorem}
LPO holds if and only if the set of quasidecidable propositions coincides with the [[boolean domain]]. 
\end{theorem}

\begin{proof}
LPO implies that for all sequences $f$ in the [[boolean domain]], the existential quantification $\exists n \in \mathbb{N}, f(n) = 1$ is [[decidable proposition|decidable]]; hence valued in the [[booleans]]. Thus, the [[boolean domain]] is closed under [[existential quantification]] over the [[natural numbers]]. Since the [[boolean domain]] is a [[subset]] of the set of quasidecidable propositions, this implies that the boolean domain coincide with the set of quasidecidable propositions by definition of the set of quasidecidable propositions. 

Conversely, suppose that the [[booleans]] coincide with the set of quasidecidable propositions. Then we have that the existential quantification $\exists n \in \mathbb{N}, f(n) = 1$ is a [[boolean]], which implies LPO. 
\end{proof}

This result also implies that every [[semidecidable proposition]] is a [[decidable proposition]] if and only if LPO holds, since the set of semidecidable propositions is a [[superset]] of the [[booleans]] and a subset of the set of quasidecidable propositions. 

On the other hand, in [[synthetic topology]] and [[synthetic domain theory]], one sometimes sees [[Phoa's principle]] or [[synthetic quasi-coherence]] assumed for the $\mathbb{N}$-overt [[dominance]], in order to emulate the behavior of [[Sierpinski space]], where every function is [[monotonic]]. Since the set of quasidecidable propositions is an $\mathbb{N}$-overt [[dominance]], it is consistent to assume such axioms for the set of quasidecidable propositions, such as [[Phoa's principle]] for the set of quasidecidable propositions in the [[effective topos]]. However, such axioms are inconsistent with LPO: 

\begin{theorem}
LPO is inconsistent with [[Phoa's principle]] for the set of quasidecidable propositions $\Sigma$. 
\end{theorem}

\begin{proof}
LPO is equivalent to the fact that the [[boolean domain]] coincides with the set of quasidecidable propositions. However, the [[logical negation]] function $x \mapsto \neg x$ on the [[boolean domain]] does not satisfy the linear interpolation condition for Phoa's principle for the booleans; it is not true that $\neg x = (\neg 1) \wedge (x \vee \neg 0) = 0 \wedge (x \vee 1) = x$ on the booleans. As a result, LPO is inconsistent with Phoa's principle for set of quasidecidable propositions. 
\end{proof}

In traditional [[point-set topology]] in [[classical mathematics]], one already has that negation on the booleans is not a [[continuous function]] with respect to the [[Scott topology]] of the [[booleans]]. 

\begin{lemma}
LPO is inconsistent with [[synthetic quasi-coherence]] for the set of quasidecidable propositions $\Sigma$; that is, let $A$ be a finitely presented $\Sigma$-algebra, in the sense that $A$ is a [[distributive lattice]] equivalent to the quotient of $\Sigma[x_1 \ldots x_n]$ by finitely many relations, and let $\mathrm{Spec}_\Sigma(A)$ be the set of $\Sigma$-algebra homomorphisms. Then the canonical lattice homomorphism

$$a \mapsto (f \mapsto f(a)):A \to \Sigma^{\mathrm{Spec}_\Sigma(A)}$$

is an [[isomorphism]]
\end{lemma}

\begin{proof}
Synthetic quasi-coherence for the set of quasidecidable propositions $\Sigma$ implies [[Phoa's principle]] for $\Sigma$, and so is thus inconsistent with LPO.  
\end{proof}

## Related concepts

* [[decidable proposition]]

* [[proposition]], [[truth value]]

* [[semidecidable proposition]]

* [[synthetic topology]], [[synthetic domain theory]]

* [[dominance]]

* [[sigma-frame|$\sigma$-frame]]

* [[effective topos]]

## References

* {#EK17} [[Martín Escardó]], [[Cory Knapp]]. *Partial Elements and Recursion via Dominances in Univalent Type Theory.* In 26th EACSL Annual Conference on Computer Science Logic (CSL 2017). Leibniz International Proceedings in Informatics (LIPIcs), Volume 82, pp. 21:1-21:16, Schloss Dagstuhl – Leibniz-Zentrum für Informatik (2017) &lbrack;[10.4230/LIPIcs.CSL.2017.21](https://doi.org/10.4230/LIPIcs.CSL.2017.21)&rbrack;

* {#Escardo20} [[Martin Escardo]]. *Quasidecidable propositions*. [[Agda]] code with comments, 2020. ([URL](https://martinescardo.github.io/TypeTopology/NotionsOfDecidability.QuasiDecidable.html)).

* {#JKMF26} [[Tom de Jong]], [[Nicolai Kraus]], [[Aref Mohammadzadeh]], [[Fredrik Nordvall Forsberg]], *Generalized Decidability via Brouwer Trees* ([arXiv:2602.10844](https://arxiv.org/abs/2602.10844))

* {#UFP13} Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

* {#ADK17} [[Thorsten Altenkirch]], [[Nils A. Danielsson]], [[Nicolai Kraus]], *Partiality, Revisited: The Partiality Monad as a Quotient Inductive-Inductive Type*, FoSSaCS 2017, Lecture Notes in Computer Science **10203** Springer (2017) &lbrack;[doi:10.1007/978-3-662-54458-7_31](https://doi.org/10.1007/978-3-662-54458-7_31), [arXiv:1610.09254](https://arxiv.org/abs/1610.09254)&rbrack; 

* {#Gilbert17} Gaëtan Gilbert. *Formalising real numbers in homotopy type theory.* In CPP’17, Proceedings of the 6th ACM SIGPLAN Conference on Certified Programs and Proofs, pages 112–124, 2017. &lbrack;[doi:10.1145/3018610.3018614](https://doi.org/10.1145/3018610.3018614)&rbrack;.

* {#BFS19} Martin E. Bidlingmaier, Florian Faissole, [[Bas Spitters]], *Synthetic topology in Homotopy Type Theory for probabilistic programming*. Mathematical Structures in Computer Science, 2021;31(10):1301-1329. &lbrack;[doi:10.1017/S0960129521000165](https://doi.org/10.1017/S0960129521000165), [arXiv:1912.07339](https://arxiv.org/abs/1912.07339)&rbrack;

* {#SY25} [[Jonathan Sterling]], [[Lingyuan Ye]], *Domains and Classifying Topoi* ([arXiv:2505.13096](https://arxiv.org/abs/2505.13096))

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
