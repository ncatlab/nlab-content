

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea 

[[Mike Shulman]] ([Shulman 2022](#Shulman2022)) has proposed an interpretation of [[affine logic]] for use in [[constructive mathematics]], called the _antithesis interpretation_.

The motivation here is that in much of constructive mathematics, especially (but not only) in [[constructive analysis]], statements of interest seem to come in pairs, a statement $P^+$ that amounts to a constructive version of a well-known statement $P^{\mathrm{C}}$ from [[classical mathematics]], and a statement $P^-$ that amounts to a constructive version of $\neg{P^{\mathrm{C}}}$, and which is equivalent to $\neg{P^+}$ in [[classical logic]], but which is not the same as $\neg{P^+}$ in [[intuitionistic logic]] (being sometimes stronger, sometimes weaker, sometimes neither, and similarly for $P^+$ vis-a-vis $\neg{P^-}$).  For example, if $P^{\mathrm{C}}$ is the claim that some [[real number]] $x$ is [[rational number|rational]], then $P^+$ is

$$ \exists\, q \in \mathbb{Q},\; x = q $$

(the conventional meaning of &lsquo;$x$ is rational&rsquo; in constructive analysis), while $P^-$ is

$$ \forall\, q \in \mathbb{Q},\; x \# q $$

(the conventional meaning of &lsquo;$x$ is [[irrational number|irrational]]&rsquo; in constructive analysis); here, $\#$ is the standard [[apartness relation]] between real numbers, whose [[negation]] is the [[equality relation]] $=$.  As you can see, the two statements are [[de Morgan duality|de Morgan dual]] to one another, and so are negations of each other in classical logic, but neither is the negation of the other in intuitionistic logic.

That such pairs of statements commonly arise is a truism in constructive mathematics.  The point of the antithesis interpretation is that the pair $(P^+, P^-)$ may be derived systematically from a single statement $P^{\mathrm{L}}$ in affine logic.  And this is a [[sound interpretation]], in that any reasoning valid in affine logic (or even [[linear logic]]) will be constructively valid for both statements; that is, if $P^{\mathrm{L}} \vdash Q^{\mathrm{L}}$ in affine (or even linear) logic, then $P^+ \vdash Q^+$ and $Q^- \vdash P^-$ in intuitionistic logic.  Therefore, as long as the reasoning is affine (or even linear), one can prove intuitionistic theorems about both at once.

The antithesis interpretation also explains why there are often both weak and strong versions of $P^-$ (or even $P^+$ sometimes), having especially to do with the interpretation of [[disjunction]].  This comes up already in defining what a [[set]] is, because of the nature of the [[equality relation]] on a set $S$.  As in the example about about rational and irrational real numbers, every set should also be equipped with an antithesis [[inequality relation]] $\#$, and the axioms for this may be derived from the axioms for an equality relation.  The [[transitive relation|transitivity]] axiom for equality has two obvious interpretations in affine logic, which lead to two different interpretations in intuitionistic logic as axioms for $\#$: a weak version (intepreting $\parr$) stating (for elements $x, y, z$ of $S$) that if $x \# z$, then $y \# z$ if $x = y$, and $x \# y$ if $y = z$; and a strong version (interpreting $\oplus$) stating that if $x \# z$, then $x \# y$ or $y \# z$.  (The weak version really does follow from the strong version because we also automatically have that $x = y$ and $x \# y$ can never both be true.)  Ultimately, the weak version says only that $\#$ is an [[inequality relation]] on the set $S$, while the strong version says that $\#$ is an [[apartness relation]].

Since every proposition comes with an antithesis proposition in the antithesis interpretation, the natural notion of a [[subset]] is actually a pair of [[disjoint subsets]], leading to a potentially far-reaching reinterpretation of the role of [[higher-order logic]] in constructive mathematics, with concepts like a family of collections of subsets becoming a disjoint pair of families of disjoint pairs of collections of disjoint pairs of subsets.

## Affine logical operations
{#AffineLogicalOperations}

An affine proposition $P$ is interpreted as a pair $(P^+, P^-)$ of propositions in intuitionistic logic which are mutually exclusive in that $\neg (P^+ \wedge P^-)$ holds. As a result, the propositional affine logical operations are intuitionistically operations on the [[type]] 
$$\Omega_\pm = \sum_{P^+:\Omega} \sum_{P^-:\Omega} \neg (P^+ \wedge P^-)$$ 

Similarly, an affine predicate $P$ on a type $A$ is interpreted as a pair $(P^+, P^-)$ of predicates on $A$ in intuitionistic logic which are pointwise mutually exclusive in that $\neg (P^+(x) \wedge P^-(x))$ holds for all $x:A$. This is equivalently a function $P:A \to \Omega_\pm$. 

We have the following propositional and predicate affine logical operations:

* [[truth]] is an element of $\Omega_\pm$ defined as

$$1 \coloneqq (\top, \bot)$$

* [[falsehood]] is an element of $\Omega_\pm$ defined a

$$0 \coloneqq (\bot, \top)$$

* [[additive conjunction]] is a function from $\Omega_\pm \times \Omega_\pm$ to $\Omega_\pm$ defined as

$$(P^+, P^-) \sqcap (Q^+, Q^-) \coloneqq (P^+ \wedge Q^+, P^- \vee Q^-)$$

* [[additive disjunction]] is a function from $\Omega_\pm \times \Omega_\pm$ to $\Omega_\pm$ defined as

$$(P^+, P^-) \sqcup (Q^+, Q^-) \coloneqq (P^+ \vee Q^+, P^- \wedge Q^-)$$

* [[multiplicative conjunction]] is a function from $\Omega_\pm \times \Omega_\pm$ to $\Omega_\pm$ defined as

$$(P^+, P^-) \boxtimes (Q^+, Q^-) \coloneqq (P^+ \wedge Q^+, (P^+ \Rightarrow Q^-) \wedge (Q^+ \Rightarrow P^-))$$

* [[multiplicative disjunction]] is a function from $\Omega_\pm \times \Omega_\pm$ to $\Omega_\pm$ defined as

$$(P^+, P^-) \boxplus (Q^+, Q^-) \coloneqq ((P^- \Rightarrow Q^+) \wedge (Q^- \Rightarrow P^+), P^- \wedge Q^-)$$

* [[linear implication]] is a function from $\Omega_\pm \times \Omega_\pm$ to $\Omega_\pm$ defined as

$$(P^+, P^-) \multimap (Q^+, Q^-) \coloneqq ((P^+ \Rightarrow Q^+) \wedge (Q^- \Rightarrow P^-), P^+ \wedge Q^-)$$

* [[linear negation]] is a function from $\Omega_\pm$ to $\Omega_\pm$ defined as

$$(P^+, P^-)^\bot \coloneqq (P^-, P^+)$$

* [[exponential conjunction]] is a function from $\Omega_\pm$ to $\Omega_\pm$ defined as

$$!(P^+, P^-) \coloneqq (P^+, P^+ \Rightarrow P^-)$$

* [[exponential disjunction]] is a function from $\Omega_\pm$ to $\Omega_\pm$ defined as

$$?(P^+, P^-) \coloneqq (P^- \Rightarrow P^+, P^-)$$

* the linear [[existential quantifier]] for a type $A$ is a function from $A \to \Omega_\pm$ to $\Omega_\pm$ defined as

$$\bigsqcup_{x:A} (P^+(x), P^-(x)) \coloneqq (\exists x:A.P^+(x), \forall x:A.P^-(x))$$

* the linear [[universal quantifier]] for a type $A$ is a function from $A \to \Omega_\pm$ to $\Omega_\pm$ defined as

$$\bigsqcap_{x:A} (P^+(x), P^-(x)) \coloneqq (\forall x:A.P^+(x), \exists x:A.P^-(x))$$

### Properties

The [[exponential conjunction]] and [[exponential disjunction]] can be defined entirely in terms of the [[multiplicative disjunction]] and [[multiplicative conjunction]] respectively:

$$!P \coloneqq P \boxtimes P \quad ?P \coloneqq P \boxplus P$$

### Excluded middle

Suppose that the [[law of excluded middle]] holds in the [[intuitionistic logic]], so that the logic becomes [[classical logic]]. Then $\Omega$ is equivalent to the [[boolean domain]] $\mathbb{2}$, and $\Omega_\pm$ is equivalent to the three-element set $\{(\top, \bot), (\bot, \bot), (\bot, \top)\}$ representing the propositions in [[Łukasiewicz logic]]. As a result, the affine predicate logic in the antithesis interpretation becomes predicate Łukasiewicz logic. 

## Concepts in the antithesis interpretation

* [[antithesis partial order]]

* [[unified topological space]]

## From a philosophical perspective

Philosophically the antithesis translation positions itself at the crossroad of several approaches to "logicist metaphysics" that usually are thought to be incompatible:

On the one hand, the British philosopher [[Michael Dummett]] has argued for [[intuitionistic logic]] as the _constructivist_ "logical basis of metaphysics". But if the suggestions in the concluding section of [Shulman (2022)](#Shulman2022}) are borne out and affine logic turns out as a/the viable approach to constructivist _mathematics_ this might call for a revision of constructivist _metaphysics_ as well which in the aftermath could find itself in rapprochement to _classical_ metaphysics since affine logic has an involutive negation.

On the other hand, the construction of the antithesis model by forming pairs $(P^+,P^-)$ such that $P^+\wedge P^-\simeq 0$ looks a like a neat illustration of "speculative thinking" as suggested by [[Georg Hegel|Hegel]] who writes in the lectures on the philosophy of religion (A II):

> Spekulativ denken heißt, ein Wirkliches auflösen und dieses sich so entgegensetzen, daß die Unterschiede nach Denkbestimmungen entgegengesetzt sind und der Gegenstand als Einheit beider gefaßt wird.[^HG]

The German philosopher [[Uwe Petersen]] has indeed argued that a contraction-free logic with abstraction and unrestricted [[comprehension scheme|comprehension]] (plus a [[Lawvere's fixed point theorem|general fixed point property]]) serves as the natural habitat for a formal approach to _speculative_ metaphysics of the Hegelian ilk.

To pun: the _affine metaphysics_ suggested by the antithesis interpretation promises to bring out the affinities between classical, constructivist and speculative metaphysics!

## Related concepts

* [[constructive mathematics]]

* [[affine logic]], [[linear logic]]

* [[Chu construction]]

* [[Dialectica construction]]

* [[double negation translation]]

## References

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518))

Some discussion about the antithesis interpretation occurred in:

* *One universe as a foundation & friends*, Category Theory Zulip ([web](https://categorytheory.zulipchat.com/#narrow/channel/229136-theory.3A-category-theory/topic/One.20universe.20as.20a.20foundation.20.26.20friends))

[^HG]: "Thinking speculatively means to dissolve a real and to oppose it with itself in such a manner that the differences are opposed according to their thought determinations and the object is conceived as the unity of both of them."
 Hegel, _Vorlesungen über die Philosophie der Religion I - Werke 16_, Suhrkamp Frankfurt 1986. (p.30)

[[!redirects antithesis translation]]

[[!redirects Antithesis translation]]

[[!redirects Antithesis interpretation]]

[[!redirects antithetical translation]]