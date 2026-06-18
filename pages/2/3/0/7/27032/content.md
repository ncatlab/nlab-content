
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

The **weak limited principle of omniscience** ($WLPO$) states that the [[universal quantification]] of any [[decidable proposition]] on the [[natural numbers]] is again decidable. That is,
$$(\forall x \in \mathbb{N}, P(x) \vee \neg{P(x)}) \Rightarrow (\forall x \in \mathbb{N}, P(x)) \vee \neg(\forall x \in \mathbb{N}, P(x)).$$
Equivalently, that the negation of the existential quantifier of any decidable proposition is decidable: 
$$(\forall x \in \mathbb{N}, P(x) \vee \neg{P(x)}) \Rightarrow (\neg \exists x \in \mathbb{N}, P(x)) \vee \neg(\neg \exists x \in \mathbb{N}, P(x)).$$

We can also state the principle set-theoretically. The __weak limited principle of omniscience__ ($WLPO$) states that given a [[subset]] $P \in \mathcal{P}(\mathbb{N})$, if $P$ is a [[decidable subset]] of $\mathbb{N}$ ($P \cup \bar{P} = \mathbb{N}$), then either $\bar{P} = \mathbb{N}$ or $\neg (P = \emptyset)$, where $\bar{P}$ is the [[complement]] of $P$. 

## In the internal logic

In [[set theory]], there are actually two different notions of logic: there is the external predicate logic used to define the set theory itself, and there is the internal predicate logic induced by the set operations on [[subsingletons]] and [[injections]]. In particular, 

* An internal *[[proposition]]* is a set $P$ such that for all elements $x \in P$ and $y \in P$, $x = y$. 

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

Then the **internal WLPO** states that:

* For any internal predicate $i:P \hookrightarrow \mathbb{N}$, if there is a function $\chi_P:\mathbb{N} \to 2$, then the internal universal quantification of $P$, $\forall_{\mathbb{N}} P = \{f \in P^{\mathbb{N}} \vert \forall x \in \mathbb{N}, f(x) \in i^*(x) \}$ has a function $(\forall_{\mathbb{N}} P) \to 2$ into the boolean domain. 

or equivalently

* For any function $a:\mathbb{N} \to 2$, the internal universal quantification of $P = \{x \in \mathbb{N} \vert a(x) = 1\}$, $\forall_{\mathbb{N}} P = \{f \in P^{\mathbb{N}} \vert \forall x \in \mathbb{N}, f(x) \in i^*(x) \}$ has a function $(\forall_{\mathbb{N}} P) \to 2$ into the boolean domain. 

The internal versions of the weak limited principle of omniscience, like all internal versions of axioms, are weaker than the external version of the the weak limited principle of omniscience, since while [[bounded separation]] implies that one can convert any external predicate $x \in \mathbb{N} \vdash P(x)$ on the [[natural numbers]] to an internal predicate $\{x \in \mathbb{N} \vert P(x)\} \hookrightarrow \mathbb{N}$, it is generally not possible to convert an internal predicate to an external predicate without a reflection rule which turns subsingletons in the set theory into propositions in the external logic. 

## Equivalent statements

There are various other results that are equivalent to the weak limited principle of omniscience. Here are a few:

* The [[boolean domain]] is a [[sigma-frame|$\sigma$-frame]] if and only if WLPO holds.

* The [[analytic WLPO]] for the [[Cauchy real numbers]] is equivalent to the WLPO. 

* The [[untruncated LLPO]] for the [[natural numbers]] is equivalent to the WLPO. 

### Truncated and untruncated versions in dependent type theory

In the context of [[dependent type theory]], the weak limited principle of omniscience can be translated in two ways, by interpreting "or" as [[propositional truncation|propositionally truncated]] ("merely or") or untruncated ("purely or"). Truncated WLPO and untruncated WLPO are equivalent to each other.

## Related statements

* $WLPO$ follows from [[LPO]], but not conversely. If $P(x)$ is a decidable proposition, then so is $\neg{P(x)}$, and so $LPO$ gives
$$(\exists x \in \mathbb{N}, \neg{P(x)}) \vee (\forall x \in \mathbb{N}, \neg{\neg{P(x)}}), $$
which implies
$$\neg(\forall x \in \mathbb{N}, P(x)) \vee (\forall x \in \mathbb{N}, P(x))$$
as $P$ is decidable.

* The [[LLPO]] follows from [[WLPO]], since [[WLPO]] is equivalent to untruncated LLPO, which implies truncated LLPO. However, the converse does not necessarily hold, since in <http://www1.maths.leeds.ac.uk/~rathjen/Lifschitz.pdf> is a model by Michael Rathjen that separates WLPO from LLPO. Similarly, [Grossack 24](#Grossack24) shows that Johnstone's topological topos separates WLPO from LLPO. 

* The WLPO implies the [[stable fan theorem]]. 

## Generalizations

### Choiceless weak limited principle of omniscience

There is a generalization of the weak limited principle of omniscience defined in [King 2024](#King24), which was suggested to be called the **choiceless weak limited principle of omniscience**. The choiceless weak limited principle of omniscience states that given a pair of [[predicates]] $P$ and $Q$ on the [[natural numbers]] $\mathbb{N}$ such that $P(x) \vee Q(x)$ holds for all $x \in \mathbb{N}$, then either for all $x \in \mathbb{N}$, $Q(x)$, or it is not true that for all $x \in \mathbb{N}$, $\neg P(x)$. 
$$(\forall x \in \mathbb{N}.P(x) \vee Q(x)) \Rightarrow ((\forall x \in \mathbb{N}.Q(x)) \vee \neg (\forall x \in \mathbb{N}.\neg P(x)))$$
The idea behind the term "choiceless" is that one isn't forced to choose between $P(x)$ or $Q(x)$ in this version of the weak limited principle of omniscience. One gets back the usual weak limited principle of omniscience if $P(x)$ and $Q(x)$ are [[mutually exclusive propositions]] for all $x \in \mathbb{N}$, from which $Q(x)$ [[if and only if]] $\neg P(x)$ for all $x \in \mathbb{N}$. 

We can also state the principle set-theoretically. The __choiceless weak limited principle of omniscience__ states that given [[subsets]] $P, Q \in \mathcal{P}(\mathbb{N})$, if $P \cup Q = \mathbb{N}$, then either $Q = \mathbb{N}$ or $\neg (P = \emptyset)$. One gets back the usual limited principle of omniscience if $P$ and $Q$ are [[disjoint subsets]] $P \cap Q = \emptyset$, from which $Q = \bar{P}$, where $\bar{P}$ is the [[complement]] of $P$. 

The choiceless weak limited principle of omniscience for the natural numbers $\mathbb{N}$ implies the [[analytic weak limited principle of omniscience]] for all sets of [[real numbers]], as shown in [King 2024](#King24). 

### Generalizing from the natural numbers to an arbitrary set

One can generalize from the [[natural numbers]] to arbitrary sets $A$. Given a set $A$, the **weak limited principle of omniscience for $A$** ($WLPO_A$) for the set $A$ states that the [[universal quantification]] of any [[decidable proposition]] on $A$ is again decidable. That is,
$$(\forall x \in A, P(x) \vee \neg{P(x)}) \Rightarrow (\forall x \in A, P(x)) \vee \neg(\forall x \in A, P(x)).$$
Equivalently, that the negation of the existential quantifier of any decidable proposition is decidable: 
$$(\forall x \in A, P(x) \vee \neg{P(x)}) \Rightarrow (\neg \exists x \in A, P(x)) \vee \neg(\neg \exists x \in A, P(x)).$$

We can also state the principle set-theoretically. Given a [[set]] $A$, the __weak limited principle of omniscience for $A$__ ($WLPO_A$) states that given a [[subset]] $P \in \mathcal{P}(A)$, if $P$ is a [[decidable subset]] of $A$ ($P \cup \bar{P} = A$), then either $\bar{P} = A$ or $\neg (P = \emptyset)$, where $\bar{P}$ is the [[complement]] of $P$. 

If one takes the domains of quantification to be subsingletons, one gets [[weak excluded middle]] $\neg p \vee \neg \neg p$ ($WEM$), which is weaker than $EM$; conversely, $WEM$ implies $WLPO$ (over any domain). Again, Bishop\'s $WLPO$ takes the domain to be $\mathbb{N}$, giving a principle weaker than $WEM$ (and also weaker than $LPO_{\mathbb{N}}$). 

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

* {#Diener18} [[Hannes Diener]], *Constructive reverse mathematics*, Habilitationsschrift Fakultät IV - Naturwissenschaftlich-Technische Fakultät, 2018. ([arXiv:1804.05495](https://arxiv.org/abs/1804.05495), [dspace:ubsi/1306](https://dspace.ub.uni-siegen.de/handle/ubsi/1306))

* {#Booij20} [[Auke Booij]], *Analysis in univalent type theory* (2020) &lbrack;[etheses:10411]( 	http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)&rbrack;

* {#BirchfieldSwan24} Madeleine Birchfield, Andrew Swan (2024) on Category Theory Zulip, [LPO and sigma-frame structure on booleans](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/LPO.20and.20sigma-frame.20structure.20on.20booleans)

* {#Grossack24} [[Chris Grossack]], *Life in Johnstone's Topological Topos 3 -- Bonus Axioms* ([web](https://grossack.site/2024/07/03/topological-topos-3-bonus-axioms))

* {#CCGM24} [[Felix Cherubini]], [[Thierry Coquand]], [[Freek Geerligs]], [[Hugo Moeneclaey]], *A Foundation for Synthetic Stone Duality* ([arXiv:2412.03203](https://arxiv.org/abs/2412.03203))

* {#King24} Christopher King, *What are these generalizations of the principles of omniscience called?*, MathOverflow, 15 February 2024. ([web](https://mathoverflow.net/questions/464247/what-are-these-generalizations-of-the-principles-of-omniscience-called))

[[!redirects WLPO]]
[[!redirects weak limited principle of omniscience]]
[[!redirects weak limited principles of omniscience]]

[[!redirects internal WLPO]]
[[!redirects internal weak limited principle of omniscience]]
[[!redirects internal weak limited principles of omniscience]]

[[!redirects choiceless WLPO]]
[[!redirects choiceless weak limited principle of omniscience]]
[[!redirects choiceless weak limited principles of omniscience]]