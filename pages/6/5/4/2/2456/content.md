
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Choice operators
* table of contents
{: toc}

## Definitions

A **(global) choice operator** is structure included in some [[foundations]] of [[mathematics]] which provides a uniform way to choose an element of every [[inhabited set|inhabited]] [[set]] or [[class]].

In [[David Hilbert|Hilbert]]'s original formulation, for any property $P(x)$ we can form a term $\varepsilon x.P(x)$ such that
$$\exists x.P(x) \;\Rightarrow\; P\big(\varepsilon x.P(x)\big).$$
In other words, if $P$ holds of anything at all, then it holds of the particular term $\varepsilon x.P(x)$.  A similar operator was used by [[Bourbaki]] and appears in [[FMathL]].

### In category theory

In category theory, there are two different notions of [[logic]], the usual external logic, and the [[internal logic]] of a category. These different notions of logic leads to different notions of a choice operator in category theory, an external choice operator and an internal choice operator

#### External choice operator

Let $\mathcal{E}$ be a [[well-pointed category|well-pointed]] [[Heyting category]]. This allows for the objects of $\mathcal{E}$ to behave as [[sets]] and [[morphisms]] $x:\mathrm{Hom}_\mathcal{E}(1, X)$ from the [[terminal object|terminal]] [[generator]] $1 \in \mathcal{E}$ to any object $X \in \mathcal{E}$ to behave as [[elements]] of $X$. Then Hilbert's formulation of the **external (global) choice operator** is rendered as the following: for any object $X \in \mathcal{E}$ and any property $P(x)$ on the [[hom-set]] $\mathrm{Hom}_\mathcal{E}(1, X)$ we can form a [[morphism]] $\varepsilon_X x.P(x) \in \mathrm{Hom}_\mathcal{E}(1, X)$ such that
$$\exists x \in \mathrm{Hom}_\mathcal{E}(1, X).P(x) \;\Rightarrow\; P\big(\varepsilon_X x.P(x)\big).$$

This is sometimes used in [[categorical set theories]] like [[ETCS plus epsilon]]. 

#### Internal choice operator

Let $C$ be a [[regular category]]. This implies that given an [[object]] $X \in C$, there is a [[support object]] $[X] \in C$, defined as the [[image]] of the [[unique]] [[morphism]] $X \to 1$ into the [[terminal object]] $1 \in C$. 

An **internal (global) choice operator** consists of, for every object $X$, a morphism $\varepsilon_X:[X] \to X$ from the support object of $X$ to the original object $X$. 

Hilbert's original formulation of the choice operator translates over to the [[internal language]] of $C$ into the statement that for every object $X$ and subobject $P \hookrightarrow X$, there is a morphism $\varepsilon_P:[P] \to P$ from the [[support object]] of $P$ to $P$ itself. This implies the formulation above since the object $X$ is always a [[subobject]] of itself; conversely, if there is a morphism $\varepsilon_X:[X] \to X$ for every object $X \in C$, then there is a morphism $\varepsilon_P:[P] \to P$ for subobjects $P \hookrightarrow X$. 

### In allegory theory

Given a [[regular category]] $C$, the [[bicategory of relations]] of $C$ is a [[unitary tabular allegory]]. Conversely, the [[category of maps]] of a unitary tabular allegory is a regular category. Similarly, given a [[Heyting category]] $C$, the [[bicategory of relations]] of $C$ is a [[division allegory]], and conversely, the [[category of maps]] of a division allegory is a Heyting category. This implies that internal global choice operators can be defined in any unitary tabular allegory and external global choice operators can be defined in any (well-pointed) [[division allegory]]. 

This is sometimes used in [[allegorical set theories]] like [[SEAR plus epsilon]]. 

#### External choice operator

Recall that a [[map]] in an [[allegory]] $\mathcal{E}$ is a morphism with a [[right adjoint]], and an [[injective morphism in a dagger 2-poset|injective map]] between objects $X \in \mathcal{E}$ and $Y \in \mathcal{E}$ is a map $f \in \mathrm{Map}_\mathcal{E}(X, Y)$ such that $f^\dagger \circ f \leq \mathrm{id}_X$. For any objects $X \in \mathcal{E}$ and $Y \in \mathcal{E}$, let 
$$\mathrm{Map}_\mathcal{E}(X, Y) \subseteq \mathrm{Hom}_\mathcal{E}(X, Y)$$ 
denote the hom-subset of maps between objects $X$ and $Y$. A [[division allegory]] $\mathcal{E}$ is *[[well-pointed]]* if 

* The allegorical unit $1$ is not a [[zero object]]

* for any objects $X \in \mathcal{E}$ and $Y \in \mathcal{E}$ and injective maps $f \in \mathrm{Map}_\mathcal{E}(X, Y)$, if for all [[maps]] $y \in \mathrm{Map}_\mathcal{E}(1, Y)$ from the allegorical unit $1 \in \mathcal{E}$ to $Y$, there exists a map $x \in \mathrm{Map}_\mathcal{E}(1, X)$ such that $f \circ x = y$, then $f$ is a [[unitary isomorphism]]. 

Then Hilbert's formulation of the **external (global) choice operator** is rendered as the following: for any object $X \in \mathcal{E}$ and any property $P(x)$ on $\mathrm{Map}_\mathcal{E}(1, X)$ we can form a [[map]] $\varepsilon_X x.P(x) \in \mathrm{Map}_\mathcal{E}(1, X)$ such that
$$\exists x \in \mathrm{Map}_\mathcal{E}(1, X).P(x) \;\Rightarrow\; P\big(\varepsilon_X x.P(x)\big).$$

#### Internal choice operator

The [[support object]] $[X]$ of an object $X$ in a [[unitary tabular allegory]] $C$ is the [[tabulation]] of the [[uniqueness quantifier|unique]] [[map]] from $X$ into the [[allegorical unit]] $1$. 

An **internal (global) choice operator** in $C$ consists of, for every object $X$, an [[map]] $\varepsilon_X:\mathrm{Map}_C([X], X)$ from the support object of $X$ to the original object $X$. 

### In dependent type theory

In dependent type theory with [[propositional truncations]], the naive translation of the global choice operator results in the following rule:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:[A] \vdash \varepsilon_A(x):A}$$

The above rule could be simplified to the following rule using [[function types]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \varepsilon_A:[A] \to A}$$

This corresponds to the internal global choice operator in category theory, since the logic is only internal logic in dependent type theory; there is no separate external logic. 

One can also use a Hilbert-style global choice operator which says that choice operators exist for [[dependent sum types]]

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \varepsilon_A x.B(x):\exists x:A.B(x) \to \sum_{x:A} B(x)}$$

where the [[existential quantifier]] is defined as

$$\exists x:A.B(x) \coloneqq \left[\sum_{x:A} B(x)\right]$$

The Hilbert-style global choice operator implies the other version of the global choice operator, because given a type $A$, the dependent sum type $\sum_{x:A} \sum_{y:A} x =_A y$ is [[definitionally isomorphic]] to $A$. Conversely, the other version of the global choice operator implies the Hilbert style choice operator, since having a global choice operator for every type implies having choice operators for dependent sum types. 

## Properties

### Relation to set truncation axioms

This rule is an [[axiom of set truncation]], because given type $A$ and elements $x:A$ and $y:A$, one has a function $\varepsilon_{x =_A y}:[x =_A y] \to x =_A y$. Since $[x =_A y]$ is an [[equivalence relation]], the fact that there is a function from $[x =_A y]$ to $x =_A y$ implies that $A$ is a [[set]]. 

One could try to set-truncate the target, or restrict the global choice operator to inhabited [[h-sets]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:[A] \vdash \varepsilon_A(x):[A]_0} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\mathrm{isSet}(A), x:[A] \vdash \varepsilon_A(p, x):A}$$

However, this inference rule implies the untruncated [[axiom of choice]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A, y:B(x) \vdash P(x, y) \; \mathrm{type}}{\Gamma \vdash \mathrm{ac}_{A, B, P}:\Pi x:A.\exists y:B(x).[P(x, y)] \to \exists g:(\Pi x:A.B(x)).\Pi x:A.[P(x, g(x))]}$$

which is inconsistent with a univalent Tarski universe with [[h-proposition|non-propositional]] [[h-sets]]. (See the [[HoTT book]], section 3.8). 

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

In [[dependent type theory]], the usual [[axiom of choice]] says that the [[dependent product type|dependent product]] of a family of inhabited sets is itself inhabited:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{AC}^{A, B}:\left(\mathrm{isSet}(A) \times \left(\prod_{x:A} \mathrm{isSet}(B(x))\right)\right) \to \left(\prod_{x:A} [B(x)]\right) \to \left[\prod_{x:A} B(x)\right]}$$

If one untruncates the codomain of the function, one gets choice operators for every set-indexed family of sets:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{AGC}^{A, B}:\left(\mathrm{isSet}(A) \times \left(\prod_{x:A} \mathrm{isSet}(B(x))\right)\right) \to \left(\prod_{x:A} [B(x)]\right) \to \prod_{x:A} B(x)}$$

If one removes the requirement that the type family is a family of sets from the axiom of choice, one gets the [[axiom of infinity-choice]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{AC}_\infty^{A, B}:\mathrm{isSet}(A) \to \left(\prod_{x:A} [B(x)]\right) \to \left[\prod_{x:A} B(x)\right]}$$

If one untruncates the codomain of the function, one gets choice operators for every set-indexed family of type:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{AGC}_\infty^{A, B}:\mathrm{isSet}(A) \to \left(\prod_{x:A} [B(x)]\right) \to \prod_{x:A} B(x)}$$

Similarly, the [[axiom of countable choice]] says that the [[dependent product type|dependent product]] of a family of inhabited sets indexed by the natural numbers is itself inhabited:

$$\frac{\Gamma, n:\mathbb{N} \vdash A(n) \; \mathrm{type}}{\Gamma \vdash \mathrm{AC}_\mathbb{N}^A:\left(\prod_{n:\mathbb{N}} \mathrm{isSet}(A(n))\right) \to \left(\prod_{n:\mathbb{N}} [A(n)]\right) \to \left[\prod_{n:\mathbb{N}} A(n)\right]}$$

If one untruncates the codomain of the function, one gets choice operators for every $\mathbb{N}$-indexed family of sets:

$$\frac{\Gamma, n:\mathbb{N} \vdash A(n) \; \mathrm{type}}{\Gamma \vdash \mathrm{AGC}_\mathbb{N}^A:\left(\prod_{n:\mathbb{N}} \mathrm{isSet}(A(n))\right) \to \left(\prod_{n:\mathbb{N}} [A(n)]\right) \to \prod_{n:\mathbb{N}} A(n)}$$

If one removes the requirement that the type family is a family of sets from the axiom of choice, one gets the [[axiom of infinity-choice]]:

$$\frac{\Gamma, n:\mathbb{N} \vdash A(n) \; \mathrm{type}}{\Gamma \vdash \mathrm{AC}_\mathbb{N}^A:\left(\prod_{n:\mathbb{N}} [A(n)]\right) \to \left[\prod_{n:\mathbb{N}} A(n)\right]}$$

If one untruncates the codomain of the function, one gets choice operators for every $\mathbb{N}$-indexed family of types:

$$\frac{\Gamma, n:\mathbb{N} \vdash A(n) \; \mathrm{type}}{\Gamma \vdash \mathrm{AC}_\mathbb{N}^A:\left(\prod_{n:\mathbb{N}} [A(n)]\right) \to \prod_{n:\mathbb{N}} A(n)}$$

The codomain-untruncated versions of these variants of the axiom of choice are all equivalent to the original [[inference rule]] of having global choice operators, which is the special case of either

1. for the codomain-untruncated [[axiom of choice]] the type family being indexed by a [[contractible type]]

2. for the codomain-untruncated [[axiom of countable choice]], the type family being defined by $A(n + 1)$ being a [[contractible type]] for all natural numbers, so that $A(0) \simeq \prod_{n:\mathbb{N}} A(n)$. 

### Sets which constructively have a choice operator

Every [[detachable subset]] of the [[natural numbers]] has a choice operator. This is because, every detachable subset of the natural numbers is in [[bijection]] with the set $\{n \in \mathbb{N} \vert P(n)\}$ for a [[decidable proposition|decidable]] [[predicate]] $P(n)$ on the [[natural numbers]] $n \in \mathbb{N}$. Given a [[decidable proposition|decidable]] [[predicate]] $P(n)$ on the [[natural numbers]] $n \in \mathbb{N}$, if there exists a natural number $n \in \mathbb{N}$ such that $P(n)$ holds, then one can construct a [[minimum|minimal]] [[natural number]] $\min_P$ such that the $P(\min_P)$ holds. See [Rijke 2022](#Rijke22) for a proof of this in [[dependent type theory]], where $\{n \in \mathbb{N} \vert P(n)\}$ is represented by the [[dependent sum type]] $\sum_{n:\mathbb{N}} P(n)$ and the existential quantifier $\exists n:\mathbb{N}.P(n)$ is represented by the [[propositional truncation]] of the dependent sum type. 

Every [[pointed set]] $(X, \mathrm{pt})$ has a choice operator, since its [[support of a set|support]] $[X]$ is a [[singleton]] and thus in bijection with the canonical singleton $\mathcal{P}(\emptyset)$ in [[set theory]], and elements in $X$ are thus in bijection with functions from its support to $X$ itself:

$$i:X \cong X^{\mathcal{P}(\emptyset)} \cong X^{[X]}$$

Thus the choice operator can simply be defined as the evaluation of the [[bijection]] at the given point $\mathrm{pt}$ of the set,

$$\epsilon_X \coloneqq i(\mathrm{pt})$$

This makes sense, since if the pointed set $X$ is already a [[subset]] of another set $Y$, then we know that there is already an element for which the [[predicate]] $P_X$ on $Y$ representing the subset $X$ holds - the given point of the pointed set; i.e. $P_X(\mathrm{pt})$ always holds. 

Constructively, the empty set is always not pointed because the function set $\emptyset^\emptyset$ is a [[singleton]]. However, that every set is either pointed or empty is equivalent to the excluded-middle presentation of the axiom of global choice, which says that one can construct an element of the [[disjoint union]] $X + X^\emptyset$. 

## Foundational status

It should be noted that Hilbert and Bourbaki take the $\varepsilon$-operator, called $\tau$ in "Theory of Sets" to be a primitive symbol in a mathematical theory.  This has the advantage of also allowing the existential and universal [[quantifiers]] to be constructed explicitly, since $\exists x$ translates to $P(\varepsilon_x(P(x)))$.  The intuitive meaning behind the operator is that it returns a distinguished object for which the proposition is true, or if no such object exists, it returns any object for which it is not true.  Of course, the intuitive meaning can be misleading since the properties of the epsilon operator are governed by the axiom schema of existence and $\varepsilon$-extensionality, without which, the symbol has no meaning.  The __axiom scheme of existence__ is a statement of Hilbert's axiom that avoids mention of the existential quantifier.

A wonderful usage of the global choice operator in Bourbaki is that we can easily show that paradoxical sets  do not exist, since the definition of a set is given in terms of whether or not the relation defining the set is collectivizing.  The example of [[Russell's paradox]] is computed in (Theory of Sets, Chapter II, &#167;1, no.4).  A consequence of this formulation is that the epsilon calculus is quantifier-free, since $\varepsilon$ subsumes their roles from the predicate calculus.  If we adjoin $\varepsilon$ to intuitionistic logic with the axiom scheme of existence, we obtain a non-conservative extension of intuitionistic logic in which the law of excluded middle still does not hold.  However, the assumption of the axiom scheme of $\varepsilon$-extensionality implies the axiom of global choice and therefore the law of excluded middle.  

One use of the choice operator is to eliminate undesirable details of implementation.  For example, if $P(x)$ is "$x$ is a Dedekind-complete totally ordered field," then we can define "the real numbers" to be $\varepsilon x.P(x)$.  Any of the numerous constructions of the [[real numbers]] can then be used to show that there exists an $x$ such that $P(x)$, after which point we can discard whichever explicit construction and work only with $\mathbb{R}=\varepsilon x.P(x)$.  This way we can no longer assert that real numbers (elements of $\mathbb{R}$) *are* Dedekind cuts, or equivalence classes of Cauchy sequences, or anything in particular, since the axioms provide no rules about how $\varepsilon x.P(x)$ must be chosen other than that it must satisfy $P$.  So $\mathbb{R}$ *might* consist of Cauchy sequences, or Dedekind cuts, or any other way to construct the reals, but we have no way of knowing, and thus we cannot make use of any such definition in a proof about $\mathbb{R}$; we are forced to use only its formal properties. (For a type-theoretic treatment of this situation, see [generalized the](generalized+the#formalization)).

In many cases, the assumption of a global choice operator implies the [[axiom of choice]], since for any family $(A_u)$ of inhabited sets, a choice function is given by $u\mapsto (\varepsilon x.x\in A_u)$.  In fact, in the form given above it often implies the stronger *global* axiom of choice, which applies to proper classes as well as sets.

> "Here, moreover, we come upon a very remarkable circumstance, namely, that all of these transfinite axioms are derivable from a single axiom, one that also contains the core of one of the most attacked axioms in the literature of mathematics, namely, the axiom of choice: $A(a) \rightarrow A(\varepsilon(A))$, where $\varepsilon$ is the transfinite logical choice function."

> ---Hilbert (1925), "On the Infinite", excerpted in Jean van Heijenoort, _From Frege to G&#246;del_, p. 382.

However, in some [[foundations]] it seems to be possible to avoid this conclusion (if it is unwanted) by not requiring the choice operator to be extensional, i.e. it may not be the case that $A = B$ implies $\varepsilon x.A = \varepsilon x.B$.

Like the [[axiom of choice]], the existence of a global choice operator is consistent with the other axioms of most foundations.  For example, in ZF, the [[constructible universe]] (which models $ZF + (V=L)$, the [[axiom of constructibility]]) admits a natural classical [[well-ordering]] of the entire universe, giving rise to a naturally defined global choice operator (namely, $\varepsilon x.P$ = the smallest $x$ such that $P$ in the global well-ordering).

On the other hand, in [[dependent type theory]] a global choice operator over the entire type theory is inconsistent with a [[univalent universe]]. For univalence requires that all operations on the [[type universe]] must be natural with respect to equivalences, which no global choice operator can be. If one only has a global choice operator over only the types in a given type universe, one can still prove the [[limited principle of omniscience]] for [[natural numbers]] $\mathrm{LPO}_\mathbb{N}$ for the entire type theory: a global choice operator for a universe $U$ implies that the [[axiom of choice]] and [[excluded middle]] holds in $U$, which in turn implies that the [[type of booleans]] is the homotopy-[[initial object|initial]] [[sigma-frame|$\sigma$-frame]], which is equivalent to $\mathrm{LPO}_\mathbb{N}$. 

## Related concepts

* [[split support]]
* [[law of double negation]]
* [[propositions as types]]
* [[axiom of choice]]

## Readings

* [Hilbert's $\varepsilon$-Operator](https://planetmath.org/hilbertsvarepsilonoperator), _PlanetMath_.

* Stanford Encyclopedia of Philosophy article on [The Epsilon Calculus](http://plato.stanford.edu/entries/epsilon-calculus/).

* See also Hilbert (1927), "The Foundations of Mathematics", pp. 464&#8211;479 in JvH.

For the principle of global choice in [[dependent type theory]], see example 14.4.1, remark 14.4.2. and corollary 17.5.3 of 

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

category: foundational axiom

[[!redirects axiom of global choice]]
[[!redirects global axiom of choice]]

[[!redirects principle of global choice]]
[[!redirects principles of global choice]]

[[!redirects choice operator]]
[[!redirects choice operators]]
[[!redirects global choice operator]]
[[!redirects global choice operators]]

[[!redirects internal choice operator]]
[[!redirects internal choice operators]]
[[!redirects internal global choice operator]]
[[!redirects internal global choice operators]]

[[!redirects external choice operator]]
[[!redirects external choice operators]]
[[!redirects external global choice operator]]
[[!redirects external global choice operators]]

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

[[!redirects codomain-untruncated choice]]
[[!redirects codomain-untruncated axiom of choice]]
[[!redirects codomain untruncated choice]]
[[!redirects codomain untruncated axiom of choice]]

[[!redirects codomain-untruncated countable choice]]
[[!redirects codomain-untruncated axiom of countable choice]]
[[!redirects codomain untruncated countable choice]]
[[!redirects codomain untruncated axiom of countable choice]]
