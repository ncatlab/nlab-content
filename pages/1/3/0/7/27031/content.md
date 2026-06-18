

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Definition

The **lesser limited principle of omniscience** ($LLPO$) is a [[principle of omniscience]] which states that, if the existential quantification of the [[conjunction]] of two [[decidable propositions]] on the [[natural numbers]] is false, then one of their separate existential quantifications is false. That is,
$$ (\forall x \in \mathbb{N}, P(x) \vee \neg{P(x)}) \Rightarrow (\forall y \in \mathbb{N}, Q(y) \vee \neg{Q(y)}) \Rightarrow \neg(\exists x \in \mathbb{N}, P(x) \wedge \exists y \in \mathbb{N}, Q(y)) \Rightarrow \neg(\exists x \in \mathbb{N}, P(x)) \vee \neg(\exists y \in \mathbb{N}, Q(y)) ,$$
or equivalently
$$ (\forall x \in \mathbb{N}, P(x) \vee \neg{P(x)}) \Rightarrow (\forall y \in \mathbb{N}, Q(y) \vee \neg{Q(y)}) \Rightarrow \neg(\exists x \in \mathbb{N}, P(x) \wedge \exists y \in \mathbb{N}, Q(y)) \Rightarrow (\forall x \in \mathbb{N}, \neg{P(x)}) \vee (\forall y \in \mathbb{N}, \neg{Q(y)}) .$$

We can also state the principle set-theoretically. The __lesser limited principle of omniscience__ (LLPO) states that given [[subsets]] $P, Q \in \mathcal{P}(\mathbb{N})$, if $P$ and $Q$ are [[decidable subsets]] of $\mathbb{N}$ ($P \cup \bar{P} = \mathbb{N}$, $Q \cup \bar{Q} = \mathbb{N}$), then if it is not true that both $P$ and $Q$ are [[inhabited subsets]] of $\mathbb{N}$, then either $\bar{P} = \mathbb{N}$ or $\bar{Q} = \mathbb{N}$, where $\bar{P}$ and $\bar{Q}$ are the [[complements]] of $P$ and $Q$ respectively. 

One can also use functions to the [[boolean domain]] instead of [[decidable subsets]]: the **lesser limited principle of omniscience** (LLPO) states that, given functions $f, g\colon \mathbb{N} \to \{0,1\}$, if $1 \notin \im f \cap \im g$, then $1 \notin \im f$ or $1 \notin \im g$. 

## Equivalent statements

There are various other results that are equivalent to the principles of omniscience. Here are a few:

* Let $[0,1]/(0 \sim 1)$ be the [[quotient space|quotient]] of the unit [[interval]] that identifies the endpoints, and let $\mathbb{R}/\mathbb{Z}$ be the [[quotient ring]]; both are classically isomorphic to the [[circle]] $\mathbb{S}^1$. (Constructively, we take $\mathbb{S}^1$ to be $\mathbb{R}/\mathbb{Z}$, although $S^1$ can also be constructed as a [[uniform completion|completion]] of $[0,1]/(0 \sim 1)$.)  Constructively, there is an [[injection]] $[0,1]/(0 \sim 1) \hookrightarrow \mathbb{R}/\mathbb{Z}$, which is a [[bijection]] if and only if the $LLPO$ holds (for the appropriate kind of real number).

* The [[analytic LLPO]] for the [[Cauchy real numbers]] is equivalent to the LLPO.

## Related statements

There are various other results that are related to the principles of omniscience. Here are a few:

* The [[limited principle of omniscience]] (LPO) and the [[weak limited principle of omniscience]] (WLPO) for [[natural numbers]] imply LLPO, but not conversely. 

* The [[lesser limited principles of omniscience]] implies that every [[pointwise continuous function]] from the Cauchy [[unit interval]] to the Cauchy [[real numbers]] is a [[uniformly continuous function]]. See section 6.1 of [Diener (2018)](#Diener18). 

* In the presence of the [[weak countable choice]] axiom $\mathrm{AC}_{\mathbb{N}, 2}$, [[existential quantifier|there exists]] a [[radix notation|radix expansion]] in any base (e.g., a decimal expansion or binary expansion) for every [[Cauchy real number]] iff LLPO holds. Without [[weak countable choice]], [[Lifschitz realizability]] gives a model in which LLPO holds but it is not true that there exists a radix expansion in any base for every [[Cauchy real number]]. See [Swan (2024)](#Swan24). 

* In the presence of [[countable choice]], LLPO is equivalent to the claim that the rings of radix expansions in any two bases are isomorphic. See Daniel Mehkeri\'s answer to [Feldman (2010)](#Mehkeri10).

### Untruncated LLPO in dependent type theory

In the context of [[dependent type theory]], the lesser limited principles of omniscience can be translated in two ways, by interpreting "or" as [[propositional truncation|propositionally truncated]] ("merely or") or untruncated ("purely or"). The relationships between the truncated and untruncated LLPO are as follows are:

* Untruncated LLPO is equivalent to WLPO (also due to Martin Escardo).

* In <http://www1.maths.leeds.ac.uk/~rathjen/Lifschitz.pdf> is a model by Michael Rathjen that separates WLPO from (truncated) LLPO. Similarly, [Grossack 24](#Grossack24) shows that Johnstone's topological topos separates WLPO from (truncated) LLPO. 

Thus, untruncated LLPO is strictly stronger than truncated LLPO, unlike the case for [[LPO]] and [[WLPO]].

## Models

* The (analytic) LLPO holds in Johnstone's [[topological topos]], as a consequence of the preservation of finite closed unions by the inclusion of sequential spaces.

## Generalizations

### Choiceless lesser limited principle of omniscience

There is a generalization of the lesser limited principle of omniscience defined in [King 2024](#King24), which was suggested to be called the **choiceless lesser limited principle of omniscience**. The choiceless lesser limited principle of omniscience states that given a pair of [[predicates]] $P$ and $Q$ on the [[natural numbers]] such that $P(x) \vee Q(x)$ holds for all $x \in \mathbb{N}$, and a pair of [[predicates]] $R$ and $S$ such that $R(x) \vee S(x)$ holds for all $x \in \mathbb{N}$, then if it is not true that there exists $x \in \mathbb{N}$ such that $P(x)$ and there exists $x \in \mathbb{N}$ such that $R(x)$ hold, then either for all $x \in \mathbb{N}$, $Q(x)$ or for all $x \in \mathbb{N}$, $S(x)$. 
$$((\forall x \in \mathbb{N}.P(x) \vee Q(x)) \wedge (\forall x \in \mathbb{N}.R(x) \vee S(x))) \Rightarrow \neg (\exists x \in \mathbb{N}.P(x) \wedge \exists x \in \mathbb{N}.R(x)) \Rightarrow ((\forall x \in \mathbb{N}.Q(x)) \vee (\forall x \in \mathbb{N}.S(x)))$$
The idea behind the term "choiceless" is that one isn't forced to choose between $P(x)$ or $Q(x)$ or between $R(x)$ or $S(x)$ in this version of the lesser limited principle of omniscience. One gets back the usual lesser limited principle of omniscience if $P(x)$ and $Q(x)$ are [[mutually exclusive propositions]] for all $x \in \mathbb{N}$ and $R(x)$ and $S(x)$ are [[mutually exclusive propositions]] for all $x \in \mathbb{N}$, from which $Q(x)$ [[if and only if]] $\neg P(x)$ for all $x \in \mathbb{N}$ and $S(x)$ [[if and only if]] $\neg R(x)$ for all $x \in \mathbb{N}$. 

We can also state the principle set-theoretically. The __choiceless lesser limited principle of omniscience__ states that given [[subsets]] $P, Q, R, S \in \mathcal{P}(\mathbb{N})$, if $P \cup Q = \mathbb{N}$ and $R \cup S = \mathbb{N}$), then if it is not true that both $P$ and $R$ are [[inhabited subsets]] of $\mathbb{N}$, then either $Q = \mathbb{N}$ or $S = \mathbb{N}$. One gets back the usual lesser limited principle of omniscience if $P$ and $Q$ are [[disjoint subsets]] $P \cap Q = \emptyset$ and $R$ and $S$ are [[disjoint subsets]] $R \cap S = \emptyset$, from which $Q = \bar{P}$ and $S = \bar{R}$, where $\bar{P}$ and $\bar{S}$ are the [[complements]] of $P$ and $S$ respectively. 

The choiceless lesser limited principle of omniscience implies the [[analytic lesser limited principle of omniscience]] for all sets of [[real numbers]], as shown in [King 2024](#King24).

### Generalizing from the natural numbers to an arbitrary set

One can generalize from the natural numbers $\mathbb{N}$ to any arbitrary set $A$. The **lesser limited principle of omniscience for the set $A$** ($LLPO_A$) is a [[principle of omniscience]] which states that, if the existential quantification of the [[conjunction]] of two [[decidable propositions]] is false, then one of their separate existential quantifications is false.  That is,
$$ (\forall x \in A, P(x) \vee \neg{P(x)}) \Rightarrow (\forall y \in A, Q(y) \vee \neg{Q(y)}) \Rightarrow \neg(\exists x \in A, P(x) \wedge \exists y \in A, Q(y)) \Rightarrow \neg(\exists x \in A, P(x)) \vee \neg(\exists y \in A, Q(y)) ,$$
or equivalently
$$ (\forall x \in A, P(x) \vee \neg{P(x)}) \Rightarrow (\forall y \in A, Q(y) \vee \neg{Q(y)}) \Rightarrow \neg(\exists x \in A, P(x) \wedge \exists y \in A, Q(y)) \Rightarrow (\forall x \in A, \neg{P(x)}) \vee (\forall y \in A, \neg{Q(y)}) .$$

If one takes the sets $A$ to be subsingletons, one get [[de Morgan's law]] $\neg(p \wedge q) \Rightarrow \neg{p} \vee \neg{q}$ ($DM$), which is weaker than $EM$; conversely, $DM$ implies $LLPO$ (over any domain). Again, Bishop\'s $LLPO$ takes the domain to be $\mathbb{N}$, giving a principle weaker than $DM$ (and also weaker than $LPO_{\mathbb{N}}$). 

We can also state the principle set-theoretically. Given a [[set]] $A$, the __lesser limited principle of omniscience for $A$__ ($LLPO_A$) states that given [[subsets]] $P, Q \in \mathcal{P}(A)$, if $P$ and $Q$ are [[decidable subsets]] of $A$ ($P \cup \bar{P} = A$, $Q \cup \bar{Q} = A$), then if it is not true that both $P$ and $Q$ are [[inhabited subsets]] of $A$, then either $\bar{P} = A$ or $\bar{Q} = A$, where $\bar{P}$ and $\bar{Q}$ are the [[complements]] of $P$ and $Q$ respectively. 

One can also use functions to the [[boolean domain]] instead of [[decidable subsets]]: the **lesser limited principle of omniscience for $A$** ($LLPO_A$) states that, given functions $f, g\colon A \to \{0,1\}$, if $1 \notin \im f \cap \im g$, then $1 \notin \im f$ or $1 \notin \im g$.  So Bishop\'s $LLPO$ is $LLPO_{\mathbb{N}}$.

## Related concepts

* [[principle of omniscience]]

* [[limited principle of omniscience]]

* [[weak limited principle of omniscience]]

* [[Markov's principle]]

* [[de Morgan's law]]

## References

* {#Bishop67} [[Errett Bishop]]: _[[Foundations of Constructive Analysis]]_, McGraw-Hill (1967)
 
  > (in the introduction or chapter 1, I forget)

* {#Ishihara06} [[Hajime Ishihara]], _Reverse Mathematics in Bishop's Constructive Mathematics_, Philosophia Scienti&#230;, CS 6 (2006) ([doi:10.4000/philosophiascientiae.406](https://doi.org/10.4000/philosophiascientiae.406),  [pdf](https://philosophiascientiae.revues.org/pdf/406))

* {#Mehkeri10} David Feldman (2010) on Math.Overflow, [Radix notation and toposes](http://mathoverflow.net/questions/49775/radix-notation-and-toposes/)

* {#LombardiQuitté2010} [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

* {#Rathjen13} [[Michael Rathjen]], *Constructive Zermelo-Fraenkel set theory and the limited principle of omniscience*. &lbrack;[arXiv:1302.3037](https://arxiv.org/abs/1302.3037)&rbrack;

* {#Shulman18} [[Mike Shulman]], *Brouwer’s fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* {#Diener18} [[Hannes Diener]], *Constructive reverse mathematics*, Habilitationsschrift Fakultät IV - Naturwissenschaftlich-Technische Fakultät, 2018. ([arXiv:1804.05495](https://arxiv.org/abs/1804.05495), [dspace:ubsi/1306](https://dspace.ub.uni-siegen.de/handle/ubsi/1306))

* {#RathjenSwan20} [[Michael Rathjen]], [[Andrew Swan]], *Lifschitz Realizability as a Topological Construction*. The Journal of Symbolic Logic, Volume 85, Issue 4, December 2020, pp. 1342 - 1375. &lbrack;[doi:10.1017/jsl.2021.1](https://doi.org/10.1017/jsl.2021.1), [arXiv:1806.10047](https://arxiv.org/abs/1806.10047)&rbrack;

* {#BauerHanson} [[Andrej Bauer]], [[James Hanson]], *The Countable Reals* ([arXiv:2404.01256](https://arxiv.org/abs/2404.01256))

* {#Swan24} Andrew Swan (2024) on Category Theory Zulip, [Radix expansions in constructive mathematics](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/Radix.20expansions.20in.20constructive.20mathematics/near/418610091)

* {#Grossack24} [[Chris Grossack]], *Life in Johnstone's Topological Topos 3 -- Bonus Axioms* ([web](https://grossack.site/2024/07/03/topological-topos-3-bonus-axioms))

* {#CCGM24} [[Felix Cherubini]], [[Thierry Coquand]], [[Freek Geerligs]], [[Hugo Moeneclaey]], *A Foundation for Synthetic Stone Duality* ([arXiv:2412.03203](https://arxiv.org/abs/2412.03203))

* {#King24} Christopher King, *What are these generalizations of the principles of omniscience called?*, MathOverflow, 15 February 2024. ([web](https://mathoverflow.net/questions/464247/what-are-these-generalizations-of-the-principles-of-omniscience-called))

[[!redirects LLPO]]
[[!redirects lesser limited principle of omniscience]]
[[!redirects lesser limited principles of omniscience]]

[[!redirects internal LLPO]]
[[!redirects internal lesser limited principle of omniscience]]
[[!redirects internal lesser limited principles of omniscience]]

[[!redirects truncated LLPO]]
[[!redirects truncated lesser limited principle of omniscience]]
[[!redirects truncated lesser limited principles of omniscience]]

[[!redirects untruncated LLPO]]
[[!redirects untruncated lesser limited principle of omniscience]]
[[!redirects untruncated lesser limited principles of omniscience]]

[[!redirects choiceless LLPO]]
[[!redirects choiceless lesser limited principle of omniscience]]
[[!redirects choiceless lesser limited principles of omniscience]]