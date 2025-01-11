

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

The **lesser limited principle of omniscience** ($LLPO$) is a [[principle of omniscience]] which states that, if the existential quantification of the [[conjunction]] of two [[decidable propositions]] is false, then one of their separate existential quantifications is false.  That is,
$$ (\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\forall y, Q(y) \vee \neg{Q(y)}) \Rightarrow \neg(\exists x, P(x) \wedge \exists y, Q(y)) \Rightarrow \neg(\exists x, P(x)) \vee \neg(\exists y, Q(y)) ,$$
or equivalently
$$ (\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\forall y, Q(y) \vee \neg{Q(y)}) \Rightarrow \neg(\exists x, P(x) \wedge \exists y, Q(y)) \Rightarrow (\forall x, \neg{P(x)}) \vee (\forall y, \neg{Q(y)}) .$$

If one takes the domains of quantification to be subsingletons, one get [[de Morgan's law]] $\neg(p \wedge q) \Rightarrow \neg{p} \vee \neg{q}$ ($DM$), which is weaker than $EM$; conversely, $DM$ implies $LLPO$ (over any domain). Again, Bishop\'s $LLPO$ takes the domain to be $\mathbb{N}$, giving a principle weaker than $DM$ (and also weaker than $LPO_{\mathbb{N}}$). 

Stated set-theoretically, the **lesser limited principle of omniscience for $A$** ($LLPO_A$) states that, given functions $f, g\colon A \to \{0,1\}$, if $1 \notin \im f \cap \im g$, then $1 \notin \im f$ or $1 \notin \im g$.  So Bishop\'s $LLPO$ is $LLPO_{\mathbb{N}}$.

## In the internal logic

In [[set theory]], there are actually two different notions of logic: there is the external predicate logic used to define the set theory itself, and there is the internal predicate logic induced by the set operations on [[subsingletons]] and [[injections]]. In particular, 

* An internal *[[proposition]]* is a set $P$ such that for all elements $x \in A$ and $y \in A$, $x = y$. 

* The internal proposition *[[true]]* is a [[singleton]] $\top$. 

* The internal proposition *[[false]]* is the [[empty set]]

* The internal conjunction of two internal propositions $P$ and $Q$ is the [[cartesian product]] $P \times Q$ of $P$ and $Q$. 

* The internal disjunction of two internal propositions $P$ and $Q$ is the [[image]] of the [[uniqueness quantifier|unique]] function $!_{P \uplus Q}:P \uplus Q \to 1$ from the [[disjoint union]] of $P$ and $Q$ to the [[singleton]] $\top$. 

$$P \vee Q = \mathrm{im}(!_{P \uplus Q})$$

* The internal implication of two internal propositions $P$ and $Q$ is the [[function set]] $P \to Q$ between $P$ and $Q$. 

* The internal negation of an internal proposition $P$ is the function set from $P$ to the [[empty set]]

$$\neg P = P \to \emptyset$$

* An internal proposition $P$ is a [[decidable proposition]] if it comes with a function $\chi_P:P \to 2$ from $P$ to the [[boolean domain]] $2$. 

* An *internal predicate* on a set $A$ is a [[set]] $P$ with [[injection]] $i:P \hookrightarrow A$, whose family of propositions indexed by $x \in A$ is represented by the [[preimages]] $i^*(x)$.

* The internal [[existential quantifier]] of an internal predicate $i:P \hookrightarrow A$ is the [[image]] of the [[uniqueness quantifier|unique]] function $!_P:P \to \top$ into the singleton $\top$.

$$\exists_A P = \im(!_P)$$

* The internal [[universal quantifier]] of an internal predicate $i:P \hookrightarrow A$ is the [[dependent product]] of the preimages
 
$$\forall_A P = \{f \in P^A \vert \forall x \in A, f(x) \in i^*(x) \}$$

* An internal predicate $i:P \hookrightarrow A$ is a [[decidable proposition]] if it comes with a function $\chi_P(x):i^*(x) \to 2$ into the [[boolean domain]] for all elements $x \in A$, or equivalently if it comes with a function $\chi_P:A \to 2$ from $A$ to the [[boolean domain]] $2$. 

The **internal LLPO** for a family of sets $(A_z)_{z \in I}$ is the LLPO for each $A_z$ stated in the internal logic of the set theory:

* The internal LPO for a family of sets $(A_z)_{z \in I}$ holds only for the internal predicates $i:P \hookrightarrow A_z$ which comes with an internal predicate $j:Q \hookrightarrow A_z$ such that $i^*(x) = \neg j^*(x)$ for all $x \in A_z$. 

In particular, the internal LLPO for the family of all sets in $U$ is [[weak excluded middle]] in $U$. 

The internal LLPO, like all internal versions of axioms, are weaker than the external version of LLPO, since while [[bounded separation]] implies that one can convert any external predicate $x \in A \vdash P(x)$ on a set $A$ to an internal predicate $\{x \in A \vert P(x)\} \hookrightarrow A$, it is generally not possible to convert an internal predicate to an external predicate without a reflection rule which turns subsingletons in the set theory into propositions in the external logic. 

## Equivalent statements

There are various other results that are equivalent to the principles of omniscience. Here are a few:

* Let $[0,1]/(0 \sim 1)$ be the [[quotient space|quotient]] of the unit [[interval]] that identifies the endpoints, and let $\mathbb{R}/\mathbb{Z}$ be the [[quotient ring]]; both are classically isomorphic to the [[circle]] $\mathbb{S}^1$. (Constructively, we take $\mathbb{S}^1$ to be $\mathbb{R}/\mathbb{Z}$, although $S^1$ can also be constructed as a [[uniform completion|completion]] of $[0,1]/(0 \sim 1)$.)  Constructively, there is an [[injection]] $[0,1]/(0 \sim 1) \hookrightarrow \mathbb{R}/\mathbb{Z}$, which is a [[bijection]] if and only if the $LLPO$ holds (for the appropriate kind of real number).

* The [[analytic LLPO]] for the [[Cauchy real numbers]] is equivalent to the LLPO for the [[natural numbers]].

## Related statements

There are various other results that are related to the principles of omniscience. Here are a few:

* The [[limited principle of omniscience]] $\mathrm{LPO}_\mathbb{N}$ and the [[weak limited principle of omniscience]] $\mathrm{WLPO}_\mathbb{N}$ for [[natural numbers]] imply $\mathrm{LLPO}_\mathbb{N}$, but not conversely. 

* The [[lesser limited principles of omniscience]] implies that every [[pointwise continuous function]] from the Cauchy [[unit interval]] to the Cauchy [[real numbers]] is a [[uniformly continuous function]]. See section 6.1 of [Diener (2018)](#Diener18). 

* In the presence of [[weak countable choice]], [[existential quantifier|there exists]] a [[radix notation|radix expansion]] in any base (e.g., a decimal expansion or binary expansion) for every [[Cauchy real number]] iff $\mathrm{LLPO}_\mathbb{N}$ holds. Without [[weak countable choice]], [[Lifschitz realizability]] gives a model in which $\mathrm{LLPO}_\mathbb{N}$ holds but it is not true that there exists a radix expansion in any base for every [[Cauchy real number]]. See [Swan (2024)](#Swan24). 

* In the presence of [[countable choice]], $\mathrm{LLPO}_\mathbb{N}$ is equivalent to the claim that the rings of radix expansions in any two bases are isomorphic. See Daniel Mehkeri\'s answer to [Feldman (2010)](#Mehkeri10).

### Untruncated LLPO in dependent type theory

In the context of [[dependent type theory]], the lesser limited principles of omniscience can be translated in two ways, by interpreting "or" as [[propositional truncation|propositionally truncated]] ("merely or") or untruncated ("purely or"). The relationships between the truncated and untruncated LLPO are as follows are:

* Untruncated LLPO is equivalent to WLPO (also due to Martin Escardo).

* In <http://www1.maths.leeds.ac.uk/~rathjen/Lifschitz.pdf> is a model by Michael Rathjen that separates WLPO from (truncated) LLPO. Similarly, [Grossack 24](#Grossack24) shows that Johnstone's topological topos separates WLPO from (truncated) LLPO. 

Thus, untruncated LLPO is strictly stronger than truncated LLPO, unlike the case for [[LPO]] and [[WLPO]].

## Models

* The (analytic) LLPO holds in Johnstone's [[topological topos]], as a consequence of the preservation of finite closed unions by the inclusion of sequential spaces.

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