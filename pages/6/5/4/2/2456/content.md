
# Choice operators
* table of contents
{: toc}

## Definitions

A **(global) choice operator** is structure included in some [[foundations]] of [[mathematics]] which provides a uniform way to choose an element of every [[inhabited set|inhabited]] [[set]] or [[class]].

In [[David Hilbert|Hilbert]]'s original formulation, for any property $P(x)$ we can form a term $\varepsilon x.P(x)$ such that
$$\exists x.P(x) \;\Rightarrow\; P\big(\varepsilon x.P(x)\big).$$
In other words, if $P$ holds of anything at all, then it holds of the particular term $\varepsilon x.P(x)$.  A similar operator was used by [[Bourbaki]] and appears in [[FMathL]].

### In dependent type theory

In dependent type theory with [[propositional truncations]], the naive translation of the global choice operator results in the following rule:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:[A] \vdash \varepsilon_A(x):A}$$

The above rule could be simplified to the following rule using [[function types]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \varepsilon_A:[A] \to A}$$

This rule is an [[axiom of set truncation]], because given type $A$ and elements $x:A$ and $y:A$, one has a function $\varepsilon_{x =_A y}:[x =_A y] \to x =_A y$. Since $[x =_A y]$ is an [[equivalence relation]], the fact that there is a function from $[x =_A y]$ to $x =_A y$ implies that $A$ is a [[set]]. 

One could try to set-truncate the target, or restrict the global choice operator to inhabited [[h-sets]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:[A] \vdash \varepsilon_A(x):[A]_0} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\mathrm{isSet}(A), x:[A] \vdash \varepsilon_A(p, x):A}$$

However, this inference rule implies the untruncated [[axiom of choice]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A, y:B(x) \vdash P(x, y) \; \mathrm{type}}{\Gamma \vdash \mathrm{ac}_{A, B, P}:\Pi x:A.\exists y:B(x).[P(x, y)] \to \exists g:(\Pi x:A.B(x)).\Pi x:A.[P(x, g(x))]}$$

which is inconsistent with a univalent Tarski universe with [[h-proposition|non-propositional]] [[h-sets]]. (See the [[HoTT book]], section 3.8). 

There is also a version of the type-theoretic choice operator local to a [[Tarski universe]] $(U, T)$, given by:

$$\frac{\Gamma \vdash U \; \mathrm{type} \quad \Gamma, X:U \vdash T \; \mathrm{type}}{\Gamma, A:U, x:[T(A)] \vdash \varepsilon_U(A, x):T(A)}$$

$U$ having a choice operator implies that $U$ satisfies [[axiom K]] or [[UIP]]. If $U$ is also univalent, then it is an [[h-groupoid]]. 

### Relation to double negation

The existence of a choice operator implies [[excluded middle]] and the [[double negation law]], and in particular, means that in [[dependent type theory]] the [[propositional truncation]] of a type is given by the [[double negation]] [[modality]]:

$$[A] \coloneqq \neg \neg A$$

This means that the rules for choice operators can be rewritten using double negation rather than propositional truncations:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:\neg \neg A \vdash \varepsilon_A(x):A}$$

equivalently, that 

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \varepsilon_A:\neg \neg A \to A}$$

It then becomes clear that the [[law of double negation]] is simply the choice operator only for [[h-propositions]]. Thus, choice operators could be called the **type-theoretic law of double negation** under the [[propositions as types]] interpretation of [[dependent type theory]]. 

One could equivalently define the set-theoretic choice operator using double negations, by one of these inference rules:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \varepsilon_A:\neg \neg A \to [A]_0} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \varepsilon_A:\mathrm{isSet}(A) \times \neg \neg A \to A}$$

By [[currying]] the conclusion of the second rule, one gets 

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \varepsilon_A:\mathrm{isSet}(A) \to (\neg \neg A \to A)}$$

which is a version of the [[law of double negation]] for [[h-sets]]. 

### Relation to the axiom of choice

The usual [[axiom of choice]] is the choice operator rule limited to [[fiber types]] of [[surjections]] between [[sets]] at elements of the [[codomain]]. 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isSet}(A) \quad \Gamma \vdash q:\mathrm{isSet}(B) \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash r:\mathrm{isSurjection}(f) \quad \Gamma \vdash b:B}{\Gamma \vdash \varepsilon_{\mathrm{fiber}_{A, B}(f, b)}:|\mathrm{fiber}_{A, B}(f, b)| \to \mathrm{fiber}_{A, B}(f, b)}$$

where 

$$\mathrm{fiber}_{A, B}(f, b) \equiv \sum_{x:A} f(x) =_B b$$

If we remove the requirement that the domain is a set, we get the [[axiom of infinity-choice]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash q:\mathrm{isSet}(B) \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash r:\mathrm{isSurjection}(f) \quad \Gamma \vdash b:B}{\Gamma \vdash \varepsilon_{\mathrm{fiber}_{A, B}(f, b)}:|\mathrm{fiber}_{A, B}(f, b)| \to \mathrm{fiber}_{A, B}(f, b)}$$

Similarly, the [[axiom of countable choice]] is the the choice operator rule limited to [[fiber types]] of [[surjections]] from [[sets]] to the [[natural numbers type]] at natural numbers. 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isSet}(A) \quad \Gamma \vdash f:A \to \mathbb{N} \quad \Gamma \vdash r:\mathrm{isSurjection}(f) \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \varepsilon_{\mathrm{fiber}_{A, \mathbb{N}}(f, n)}:|\mathrm{fiber}_{A, \mathbb{N}}(f, n)| \to \mathrm{fiber}_{A, \mathbb{N}}(f, n)}$$

If we remove the requirement that the domain is a set, we get the [[axiom of countable infinity-choice]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:A \to \mathbb{N} \quad \Gamma \vdash r:\mathrm{isSurjection}(f) \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \varepsilon_{\mathrm{fiber}_{A, \mathbb{N}}(f, n)}:|\mathrm{fiber}_{A, \mathbb{N}}(f, n)| \to \mathrm{fiber}_{A, \mathbb{N}}(f, n)}$$

## Foundational status

It should be noted that Hilbert and Bourbaki take the $\varepsilon$-operator, called $\tau$ in "Theory of Sets" to be a primitive symbol in a mathematical theory.  This has the advantage of also allowing the existential and universal [[quantifiers]] to be constructed explicitly, since $\exists x$ translates to $P(\varepsilon_x(P(x)))$.  The intuitive meaning behind the operator is that it returns a distinguished object for which the proposition is true, or if no such object exists, it returns any object for which it is not true.  Of course, the intuitive meaning can be misleading since the properties of the epsilon operator are governed by the axiom schema of existence and $\varepsilon$-extensionality, without which, the symbol has no meaning.  The __axiom scheme of existence__ is a statement of Hilbert's axiom that avoids mention of the existential quantifier.

A wonderful usage of the global choice operator in Bourbaki is that we can easily show that paradoxical sets  do not exist, since the definition of a set is given in terms of whether or not the relation defining the set is collectivizing.  The example of [[Russell's paradox]] is computed in (Theory of Sets, Chapter II, &#167;1, no.4).  A consequence of this formulation is that the epsilon calculus is quantifier-free, since $\varepsilon$ subsumes their roles from the predicate calculus.  If we adjoin $\varepsilon$ to intuitionistic logic with the axiom scheme of existence, we obtain a non-conservative extension of intuitionistic logic in which the law of excluded middle still does not hold.  However, the assumption of the axiom scheme of $\varepsilon$-extensionality implies the axiom of global choice and therefore the law of excluded middle.  

One use of the choice operator is to eliminate undesirable details of implementation.  For example, if $P(x)$ is "$x$ is a Dedekind-complete totally ordered field," then we can define "the real numbers" to be $\varepsilon x.P(x)$.  Any of the numerous constructions of the [[real numbers]] can then be used to show that there exists an $x$ such that $P(x)$, after which point we can discard whichever explicit construction and work only with $\mathbb{R}=\varepsilon x.P(x)$.  This way we can no longer assert that real numbers (elements of $\mathbb{R}$) *are* Dedekind cuts, or equivalence classes of Cauchy sequences, or anything in particular, since the axioms provide no rules about how $\varepsilon x.P(x)$ must be chosen other than that it must satisfy $P$.  So $\mathbb{R}$ *might* consist of Cauchy sequences, or Dedekind cuts, or any other way to construct the reals, but we have no way of knowing, and thus we cannot make use of any such definition in a proof about $\mathbb{R}$; we are forced to use only its formal properties. (For a type-theoretic treatment of this situation, see [generalized the](generalized+the#formalization)).

In many cases, the assumption of a global choice operator implies the [[axiom of choice]], since for any family $(A_u)$ of inhabited sets, a choice function is given by $u\mapsto (\varepsilon x.x\in A_u)$.  In fact, in the form given above it often implies the stronger *global* axiom of choice, which applies to proper classes as well as sets.

> "Here, moreover, we come upon a very remarkable circumstance, namely, that all of these transfinite axioms are derivable from a single axiom, one that also contains the core of one of the most attacked axioms in the literature of mathematics, namely, the axiom of choice: $A(a) \rightarrow A(\varepsilon(A))$, where $\varepsilon$ is the transfinite logical choice function."

> ---Hilbert (1925), "On the Infinite", excerpted in Jean van Heijenoort, _From Frege to G&#246;del_, p. 382.

However, in some [[foundations]] it seems to be possible to avoid this conclusion (if it is unwanted) by not requiring the choice operator to be extensional, i.e. it may not be the case that $A = B$ implies $\varepsilon x.A = \varepsilon x.B$.

Like the [[axiom of choice]], the existence of a global choice operator is consistent with the other axioms of most foundations.  For example, in ZF, the [[constructible universe]] (which models $ZF + (V=L)$, the [[axiom of constructibility]]) admits a natural classical [[well-ordering]] of the entire universe, giving rise to a naturally defined global choice operator (namely, $\varepsilon x.P$ = the smallest $x$ such that $P$ in the global well-ordering).

On the other hand, a type-theoretic global choice operator is inconsistent with the [[univalence axiom]] of [[homotopy type theory]]. For univalence requires that all operations on the [[type of types]] must be natural with respect to equivalences, which no global choice operator can be.

## Related concepts

* [[split support]]
* [[law of double negation]]
* [[propositions as types]]
* [[axiom of choice]]

## Readings

* [Hilbert's $\varepsilon$-Operator](https://planetmath.org/hilbertsvarepsilonoperator), _PlanetMath_.

* Stanford Encyclopedia of Philosophy article on [The Epsilon Calculus](http://plato.stanford.edu/entries/epsilon-calculus/).

* See also Hilbert (1927), "The Foundations of Mathematics", pp. 464&#8211;479 in JvH.


category: foundational axiom

[[!redirects choice operator]]
[[!redirects choice operators]]
[[!redirects global choice operator]]
[[!redirects global choice operators]]

[[!redirects type-theoretic choice operator]]
[[!redirects type-theoretic choice operators]]
[[!redirects type-theoretic global choice operator]]
[[!redirects type-theoretic global choice operators]]

[[!redirects set-theoretic choice operator]]
[[!redirects set-theoretic choice operators]]
[[!redirects set-theoretic global choice operator]]
[[!redirects set-theoretic global choice operators]]

[[!redirects axiom of existence]]
[[!redirects type-theoretic axiom of existence]]
[[!redirects set-theoretic axiom of existence]]

[[!redirects axiom scheme of existence]]
[[!redirects axiom schema of existence]]
[[!redirects axiom schemas of existence]]
[[!redirects axiom schemata of existence]]

[[!redirects typal double negation law]]
[[!redirects typal law of double negation]]
[[!redirects typal double negation principle]]
[[!redirects typal principle of double negation]]
[[!redirects typal double negation axiom]]
[[!redirects typal axiom of double negation]]

[[!redirects type-theoretic double negation law]]
[[!redirects type-theoretic law of double negation]]
[[!redirects type-theoretic double negation principle]]
[[!redirects type-theoretic principle of double negation]]
[[!redirects type-theoretic double negation axiom]]
[[!redirects type-theoretic axiom of double negation]]