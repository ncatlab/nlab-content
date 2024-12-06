
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

The **weak limited principle of omniscience** ($WLPO$) states that the [[universal quantification]] of any [[decidable proposition]] is again decidable. That is,
$$(\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\forall x, P(x)) \vee \neg(\forall x, P(x)).$$
Equivalently, that the negation of the existential quantifier of any decidable proposition is decidable: 
$$(\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\neg \exists x, P(x)) \vee \neg(\neg \exists x, P(x)).$$

If one takes the domains of quantification to be subsingletons, one get [[weak excluded middle]] $\neg p \vee \neg \neg p$ ($WEM$), which is weaker than $EM$; conversely, $WEM$ implies $WLPO$ (over any domain). Again, Bishop\'s $WLPO$ takes the domain to be $\mathbb{N}$, giving a principle weaker than $WEM$ (and also weaker than $LPO_{\mathbb{N}}$). 

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

Then the **internal WLPO** for a family of sets $(A_z)_{z \in I}$ is the WLPO for each $A_z$ stated in the internal logic of the set theory:

* For any internal predicate $i:P \hookrightarrow A_z$, if there is a function $\chi_P:A_z \to 2$, then the internal universal quantification of $P$, $\forall_{A_z} P = \{f \in P^{A_z} \vert \forall x \in A_z, f(x) \in i^*(x) \}$ has a function $(\forall_{A_z} P) \to 2$ into the boolean domain. 

or equivalently

* For any function $a:A_z \to 2$, the internal universal quantification of $P = \{x \in A_z \vert a(x) = 1\}$, $\forall_{A_z} P = \{f \in P^{A_z} \vert \forall x \in A_z, f(x) \in i^*(x) \}$ has a function $(\forall_{A_z} P) \to 2$ into the boolean domain. 

The internal versions of the weak limited principle of omniscience, like all internal versions of axioms, are weaker than the external version of the the weak limited principle of omniscience, since while [[bounded separation]] implies that one can convert any external predicate $x \in A \vdash P(x)$ on a set $A$ to an internal predicate $\{x \in A \vert P(x)\} \hookrightarrow A$, it is generally not possible to convert an internal predicate to an external predicate without a reflection rule which turns subsingletons in the set theory into propositions in the external logic. 

## Equivalent statements

There are various other results that are equivalent to the weak limited principle of omniscience. Here are a few:

* The [[boolean domain]] is a [[sigma-frame|$\sigma$-frame]] if and only if $\mathrm{WLPO}_\mathbb{N}$ holds.

* The [[analytic WLPO]] for the [[Cauchy real numbers]] is equivalent to the WLPO for the [[natural numbers]]. 

* The [[untruncated LLPO]] for the [[natural numbers]] is equivalent to the WLPO for the natural numbers. 

### Truncated and untruncated versions in dependent type theory

In the context of [[dependent type theory]], the weak limited principle of omniscience can be translated in two ways, by interpreting "or" as [[propositional truncation|propositionally truncated]] ("merely or") or untruncated ("purely or"). Truncated WLPO and untruncated WLPO are equivalent to each other.

## Related statements

* $WLPO$ follows from [[LPO]], but not conversely. If $P(x)$ is a decidable proposition, then so is $\neg{P(x)}$, and so $LPO$ gives
$$(\exists x, \neg{P(x)}) \vee (\forall x, \neg{\neg{P(x)}}), $$
which implies
$$\neg(\forall x, P(x)) \vee (\forall x, P(x))$$
as $P$ is decidable.

* The [[LLPO]] follows from [[WLPO]], since [[WLPO]] is equivalent to untruncated LLPO, which implies truncated LLPO. However, the converse does not necessarily hold, since in <http://www1.maths.leeds.ac.uk/~rathjen/Lifschitz.pdf> is a model by Michael Rathjen that separates WLPO from LLPO. Similarly, [Grossack 24](#Grossack24) shows that Johnstone's topological topos separates WLPO from LLPO. 

## Related concepts

* [[principle of omniscience]]

* [[limited principle of omniscience]]

* [[lesser limited principle of omniscience]]

* [[Markov's principle]]

* [[weak excluded middle]]

## References

* {#Bishop67} [[Errett Bishop]]: _[[Foundations of Constructive Analysis]]_, McGraw-Hill (1967)
 
  > (in the introduction or chapter 1, I forget)

* {#Ishihara06} [[Hajime Ishihara]], _Reverse Mathematics in Bishop's Constructive Mathematics_, Philosophia Scienti&#230;, CS 6 (2006) ([doi:10.4000/philosophiascientiae.406](https://doi.org/10.4000/philosophiascientiae.406),  [pdf](https://philosophiascientiae.revues.org/pdf/406))

* {#Shulman18} [[Mike Shulman]], *Brouwer’s fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* {#Booij20} [[Auke Booij]], *Analysis in univalent type theory* (2020) &lbrack;[etheses:10411]( 	http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)&rbrack;

* {#BirchfieldSwan24} Madeleine Birchfield, Andrew Swan (2024) on Category Theory Zulip, [LPO and sigma-frame structure on booleans](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/LPO.20and.20sigma-frame.20structure.20on.20booleans)

* {#Grossack24} [[Chris Grossack]], *Life in Johnstone's Topological Topos 3 -- Bonus Axioms* ([web](https://grossack.site/2024/07/03/topological-topos-3-bonus-axioms))

* {#CCGM24} [[Felix Cherubini]], [[Thierry Coquand]], [[Freek Geerligs]], [[Hugo Moeneclaey]], *A Foundation for Synthetic Stone Duality* ([arXiv:2412.03203](https://arxiv.org/abs/2412.03203))

[[!redirects WLPO]]
[[!redirects weak limited principle of omniscience]]
[[!redirects weak limited principles of omniscience]]

[[!redirects internal WLPO]]
[[!redirects internal weak limited principle of omniscience]]
[[!redirects internal weak limited principles of omniscience]]