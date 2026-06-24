
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

Equivalently, a [[proposition]] or [[truth value]] $P$ is **semi-decidable** or **semidecidable** if and only if [[existential quantifier|there exists]] a [[decidable subset]] $Q$ of the [[natural numbers]] $\mathbb{N}$ such that $P$ if and only if there exists a natural number $x \in \mathbb{N}$ such that $Q(x)$. 

$$\mathrm{isSemiDecidable}(P) \coloneqq \exists Q \in \mathcal{P}(\mathbb{N}).\mathrm{isDecidable}(Q) \wedge (P \iff \exists x \in \mathbb{N}.x \in Q)$$

where a [[subset]] $Q$ is decidable if and only if for all $x \in \mathbb{N}$, $x \in Q \vee x \notin Q$. 

### Semidecidability structures

One can also consider propositions having the structure of a [[sequence]] of [[booleans]] where one of the booleans in the sequence is true, rather than there existing a [[sequence]] of [[booleans]] where one of the booleans in the sequence is true. 

\begin{definition}
A **semidecidability structure** ([de Jong 2021](#deJong21)) or a **Rosolini structure** ([Escardo & Knapp 2017](#EK17)) on a proposition $P$ is a [[sequence]] $f$ of [[booleans]] such that $P$ if and only if there exists a natural number $x \in \mathbb{N}$ such that $f(x) = 1$. 
\end{definition}

The set of semidecidability structures on a proposition $P$ is given by the set 

$$\{f \in 2^\mathbb{N} \vert P \iff \exists x \in \mathbb{N}.f(x) = 1\}$$

Semidecidability structures are used to define a weak form of [[axiom of choice|choice]] called *Rosolini propositional choice* ([Escardo & Knapp 2017](#EK17)) or *Escardo-Knapp choice* ([de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26)), see [below](#RosoliniPropositionalChoice). 

### Set of semi-decidable propositions

The set of all semidecidable propositions $\Sigma_0^1$ is defined as a [[subset]] of the [[set of propositions]] $\Omega$ containing all the semidecidable propositions:

$$\Sigma_0^1 \coloneqq \{P \in \Omega \vert \exists f \in 2^\mathbb{N}.(P = \top) \iff \exists x \in \mathbb{N}.f(x) = 1$$

In [[predicative mathematics]], the set of *all* [[propositions]] may not exist, so instead in order to construct the set of all semidecidable propositions, we take any [[subobject|sub]]-[[sigma-frame|$\sigma$-frame]] of propositions $\Sigma$ and collect the ones that are semidecidable:

$$\Sigma_0^1 \coloneqq \{P \in \Sigma \vert \exists f \in 2^\mathbb{N}.(P = \top) \iff \exists x \in \mathbb{N}.f(x) = 1$$

Such [[sigma-frame|$\sigma$-frames]] $\Sigma$ are usually found by collecting the [[subsingletons]] of a [[universe of sets]] $U$ in the theory into a set $\Omega_U$, or minimally, by the set of quasi-decidable truth values defined later in this article. 

## Constructive taboos

There are a few constructive [[taboos]] related to the set of semidecidable propositions. 

### Rosolini dominance

In [[classical mathematics]] and in [[constructive mathematics]] which accepts [[countable choice]], every [[quasidecidable proposition]] is a semidecidable proposition ([Sterling & Ye 2025](#SY25), [de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26)), and in this case the set of semidecidable propositions is called the **Rosolini dominance**, since the set of quasidecidable propositions is an $\mathbb{N}$-overt [[dominance]]. 

However, more generally, one cannot prove that the set of semidecdiable propositions is an $\mathbb{N}$-overt dominance and thus coincide with the set of quasidecidable propositions. That the set of semidecdiable propositions is a [[dominance]] is called **Rosolini's dominance axiom** ([de Jong 2021](#deJong21)). 

{#RosoliniDominanceAxiom}
\begin{definition} 
**Rosolini's dominance axiom** states that given a semidecidable proposition $P$, if $P$ implies that a proposition $Q$ is semidecidable, then their [[conjunction]] $P \wedge Q$ is semidecidable. 
\end{definition}

The Rosolini dominance axiom is equivalent to a form of [[axiom of choice|choice]] called *Rosolini propositional choice* ([Escardo & Knapp 2017](#EK17)) or *Escardo-Knapp choice* ([de Jong 2021](#deJong21), [de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26)), which follows from the [[propositional axiom of choice]]. 

{#RosoliniPropositionalChoice} 
\begin{definition} 
**Rosolini propositional choice** or **Escardo-Knapp choice** states that given a semidecidable proposition $P$, if $P$ implies that $Q$ is semidecidable, then there merely exists a function from (the corresponding [[subsingleton]] of) $P$ to the set of semidecidability structures on $Q$. 
\end{definition}

See section 2.8 of [Escardo & Knapp 2017](#EK17) and also [de Jong 2021](#deJong21) for more details. 

Rosolini propositional choice then in turn is equivalent to the statement that every quasidecidable proposition is a semidecidable proposition; see [de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26) for more details. 

### LPO and Phoa's principle

In [[classical mathematics]], and in [[constructive mathematics]] which accept the [[limited principle of omniscience]] (LPO), the set of semideciable truth values is just the [[boolean domain]] $\mathbb{2}$. In fact, we have the following: 

\begin{theorem}
LPO holds if and only if the set of semideciable propositions coincides with the [[boolean domain]]. 
\end{theorem}

\begin{proof}
LPO implies that for all sequences $f$ in the [[boolean domain]], the existential quantification $\exists n \in \mathbb{N}, f(n) = 1$ is [[decidable proposition|decidable]]; hence valued in the [[booleans]]. Thus, the [[boolean domain]] is closed under [[existential quantification]] over the [[natural numbers]]. Since the [[boolean domain]] is a [[subset]] of the set of semideciable propositions, this implies that the boolean domain coincide with the set of semideciable propositions by definition of the set of semideciable propositions. 

Conversely, suppose that the [[booleans]] coincide with the set of semideciable propositions. Then we have that the existential quantification $\exists n \in \mathbb{N}, f(n) = 1$ is a [[boolean]], which implies LPO. 
\end{proof}

On the other hand, in [[synthetic topology]] and [[synthetic domain theory]], one sometimes sees [[Phoa's principle]] or [[synthetic quasi-coherence]] assumed for an $\mathbb{N}$-overt [[dominance]], in order to emulate the behavior of [[Sierpinski space]], where every function is [[monotonic]]. Under Rosolini propositional choice, the set of semideciable propositions is an $\mathbb{N}$-overt [[dominance]], so it is consistent to assume such axioms for the set of semideciable propositions, such as [[Phoa's principle]] for the set of semideciable propositions in the [[effective topos]]. Moreover, since the set of semidecidable propositions is a [[distributive lattice]], and [[Phoa's principle]] or [[synthetic quasi-coherence]] do not rely on the structure of an $\mathbb{N}$-overt dominance, but only on the set of semidecidable propositions being a [[distributive lattice]], such axioms can be assumed of the set of semidecidable propositions even in the absence of Rosolini propositional choice. However, such axioms are inconsistent with LPO: 

\begin{theorem}
LPO is inconsistent with [[Phoa's principle]] for the set of semideciable propositions $\Sigma$. 
\end{theorem}

\begin{proof}
LPO is equivalent to the fact that the [[boolean domain]] coincides with the set of semideciable propositions. However, the [[logical negation]] function $x \mapsto \neg x$ on the [[boolean domain]] does not satisfy the linear interpolation condition for Phoa's principle for the booleans; it is not true that $\neg x = (\neg 1) \wedge (x \vee \neg 0) = 0 \wedge (x \vee 1) = x$ on the booleans. As a result, LPO is inconsistent with Phoa's principle for set of semideciable propositions. 
\end{proof}

In traditional [[point-set topology]] in [[classical mathematics]], one already has that negation on the booleans is not a [[continuous function]] with respect to the [[Scott topology]] of the [[booleans]]. 

\begin{lemma}
LPO is inconsistent with [[synthetic quasi-coherence]] for the set of semideciable propositions $\Sigma$; that is, let $A$ be a finitely presented $\Sigma$-algebra, in the sense that $A$ is a [[distributive lattice]] equivalent to the quotient of $\Sigma[x_1 \ldots x_n]$ by finitely many relations, and let $\mathrm{Spec}_\Sigma(A)$ be the set of $\Sigma$-algebra homomorphisms. Then the canonical lattice homomorphism

$$a \mapsto (f \mapsto f(a)):A \to \Sigma^{\mathrm{Spec}_\Sigma(A)}$$

is an [[isomorphism]]
\end{lemma}

\begin{proof}
Synthetic quasi-coherence for the set of semideciable propositions $\Sigma$ implies [[Phoa's principle]] for $\Sigma$, and so is thus inconsistent with LPO.  
\end{proof}

## Generalizations

### Ordinal decidable propositions

Given an [[ordinal]] $\alpha$, there exists a notion of **$\alpha$-decidable propositions** ([de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26)), where the usual notion of semi-decidable proposition is an $(\omega + 1)$-decidable proposition. 

### Sierpiński semi-decidable propositions

One can also consider the closure of semi-decidable propositions under existential quantification over the [[natural numbers]]; these are the *[[quasi-decidable propositions]]* or the *Sierpiński semi-decidable propositions*. 

## Related concepts

* [[decidable proposition]]

* [[proposition]], [[truth value]]

* [[quasidecidable proposition]]

* [[synthetic topology]], [[synthetic domain theory]]

* [[distributive lattice]]

* [[Smyth's dictionary]]

## References

* {#Bauer06} [[Andrej Bauer]], *First Steps in Synthetic Computability Theory*, Electronic Notes in Theoretical Computer Science, volume 155, pages 5–13, 2006. Proceedings of the 21st Annual Conference on Mathematical Foundations of Programming Semantics (MFPS XXI) &lbrack;[doi:10.1016/j.entcs.2005.11.049](https://doi.org/10.1016/j.entcs.2005.11.049)&rbrack;

* {#BL12} [[Andrej Bauer]], [[Davorin Lešnik]], *Metric Spaces in Synthetic Topology*, Annals of Pure and Applied Logic, Volume 163, Issue 2, February 2012, Pages 87-100 &lbrack;[doi:10.1016/j.apal.2011.06.017](https://doi.org/10.1016/j.apal.2011.06.017), [pdf](http://math.andrej.com/wp-content/uploads/2010/01/csms_in_synthtop.pdf)&rbrack;

* {#EK17} [[Martín Escardó]], [[Cory Knapp]]. *Partial Elements and Recursion via Dominances in Univalent Type Theory.* In 26th EACSL Annual Conference on Computer Science Logic (CSL 2017). Leibniz International Proceedings in Informatics (LIPIcs), Volume 82, pp. 21:1-21:16, Schloss Dagstuhl – Leibniz-Zentrum für Informatik (2017) &lbrack;[10.4230/LIPIcs.CSL.2017.21](https://doi.org/10.4230/LIPIcs.CSL.2017.21)&rbrack;

* {#deJong21} [[Tom de Jong]]. *Semidecidable propositions*. [[Agda]] code with comments, 2021. ([URL](https://martinescardo.github.io/TypeTopology/NotionsOfDecidability.SemiDecidable.html)).

* {#SY25} [[Jonathan Sterling]], [[Lingyuan Ye]], *Domains and Classifying Topoi* ([arXiv:2505.13096](https://arxiv.org/abs/2505.13096))

* {#JKMF26} [[Tom de Jong]], [[Nicolai Kraus]], [[Aref Mohammadzadeh]], [[Fredrik Nordvall Forsberg]], *Generalized Decidability via Brouwer Trees* ([arXiv:2602.10844](https://arxiv.org/abs/2602.10844))

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

[[!redirects set of semi-decidable propositions]]
[[!redirects set of semidecidable propositions]]

[[!redirects set of semi-decidable truth values]]
[[!redirects set of semidecidable truth values]]

[[!redirects semi-decidable type]]
[[!redirects semi-decidable types]]

[[!redirects semidecidable type]]
[[!redirects semidecidable types]]

[[!redirects semi-decidability]]

[[!redirects semidecidability]]

[[!redirects semi-decidability structure]]
[[!redirects semi-decidability structures]]

[[!redirects semidecidability structure]]
[[!redirects semidecidability structures]]

[[!redirects Rosolini structure]]
[[!redirects Rosolini structures]]

[[!redirects Rosolini propositional choice]]
[[!redirects Escardo-Knapp choice]]

[[!redirects Rosolini dominance]]
[[!redirects Rosolini dominance axiom]]
[[!redirects Rosolini's dominance axiom]]