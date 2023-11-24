
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[predicative]] [[constructive mathematics|constructive]] [[set theory]], there is a hierarchy of possible axioms, starting from the existence of [[function sets]] and ending with the existence of [[power sets]] representing impredicativity. Intermediate is the existence of the set of [[entire relations]], which is given by the [[axiom of fullness]] in set theory. 

In [[predicative]] [[constructive mathematics|constructive]] [[dependent type theory]], there is a similar hierarchy of possible axioms, which begins with the existence of [[dependent product types]] (corresponding to function sets in set theory) and ends with the existence of both [[dependent product types]] and the [[type of all propositions]] (corresponding to power sets in set theory), representing impredicativity. Intermediate to both that is the existence of the type of all entire relations between two types $A$ and $B$, which is the type theoretic equivalent of the axiom of fullness. 

Types of entire relations are important in [[dependent type theory]] because, assuming [[propositional truncations]], [[quotient sets]], and [[natural numbers]], they allow the user to define the type of [[multivalued Cauchy real numbers]] - which are equivalent to [[Dedekind real numbers]] - predicatively (i.e. without [[power sets]]). 

## Definition

Recall that an [[entire relation]] between types $A$ and $B$ in type theory is a [[family]] $x:A, y:B \vdash R(x, y)$ such that for all $x:A$

* for all $y:A$, $R(x, y)$ is an [[h-proposition]], and

* there exists an $y:A$ such that $R(x, y)$. 

$$\mathrm{isEntire}(x:A.y:B.R(x, y)) \equiv \prod_{x:A} \left(\prod_{u:A} \mathrm{isProp}(R(x, y))\right) \times \exists y:A.R(x, y)$$

If there exists a [[type of propositions]] $\mathrm{Prop}$, then the type of entire relations is given by the type 

$$\sum_{R:A \times B \to \mathrm{Prop}} \mathrm{isEntire}(R)$$

where 

$$\mathrm{isEntire}(R) \equiv \prod_{x:A} \exists y:B.R(x, y)$$

for Russell types of propositions and 

$$\mathrm{isEntire}(R) \equiv \prod_{x:A} \exists y:B.\mathrm{El}(R(x, y))$$

for Tarski types of propositions. Otherwise, we could use [[inference rules]] to directly define the type of all entire relations between types $A$ and $B$: 

### A la Russell

A la Russell, the type of all entire relations is given by the following rules:

Formation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{EntRel}(A, B) \; \mathrm{type}}$$

Introduction rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash R(x, y)}{\Gamma \vdash \mathrm{toElem}_{A, B, R}:\mathrm{isEntire}(x:A.y:B.R(x, y)) \to \mathrm{EntRel}(A, B)}$$

Elimination rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:\mathrm{EntRel}(A, B)}{\Gamma, x:A, y:B \vdash R(x, y) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:\mathrm{EntRel}(A, B)}{\Gamma \vdash \mathrm{entrelwitn}(R):\mathrm{isEntire}(x:A.y:B.R(x, y))}$$

Computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash R(x, y) \quad \Gamma \vdash p:\mathrm{isEntire}(x:A.y:B.R(x, y))}{\Gamma, x:A, y:B \vdash (\mathrm{toElem}_{A, B, R}(p))(x, y) \equiv R(x, y) \; \mathrm{type}}$$

* Judgmental computation rules

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash R(x, y) \quad \Gamma \vdash p:\mathrm{isEntire}(x:A.y:B.R(x, y))}{\Gamma \vdash \mathrm{entrelwitn}(\mathrm{toElem}_{A, B, R}(p)) \equiv p:\mathrm{isEntire}(x:A.y:B.R(x, y))}$$

* Typal computation rules

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash R(x, y) \quad \Gamma \vdash p:\mathrm{isEntire}(x:A.y:B.R(x, y))}{\Gamma \vdash \beta_{\mathrm{EntRel}(A, B)}^{\mathrm{entrelwitn}, R}:\mathrm{entrelwitn}(\mathrm{toElem}_{A, B, R}(p)) =_{\mathrm{isEntire}(x:A.y:B.R(x, y))} p}$$

Uniqueness rules:

* Judgmental uniqueness rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:\mathrm{EntRel}(A, B)}{\Gamma \vdash \mathrm{toElem}_{A, B, R}(\mathrm{entrelwitn}(R)) \equiv R:\mathrm{EntRel}(A, B)}$$

* Typal uniqueness rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:\mathrm{EntRel}(A, B)}{\Gamma \vdash \eta_{\mathrm{EntRel}(A, B)}(R):\mathrm{toElem}_{A, B, R}(\mathrm{entrelwitn}(R)) =_{\mathrm{EntRel}(A, B)} R}$$

Extensionality rule:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:\mathrm{EntRel}(A, B) \quad \Gamma \vdash S:\mathrm{EntRel}(A, B)}{\Gamma \vdash \mathrm{entrelext}_{A, B}(R, S):(R =_{\mathrm{EntRel}(A, B)} S) \simeq \prod_{x:A} \prod_{y:B} R(x, y) \simeq S(x, y)}$$

### Strictly a la Tarski

Strictly a la Tarski, the type of all entire relations is given by the following rules:

Formation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{EntRel}(A, B) \; \mathrm{type}}$$

Introduction rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash R(x, y)}{\Gamma \vdash \mathrm{toElem}_{A, B, R}:\mathrm{isEntire}(x:A.y:B.R(x, y)) \to \mathrm{EntRel}(A, B)}$$

Elimination rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:\mathrm{EntRel}(A, B)}{\Gamma, x:A, y:B \vdash \mathrm{El}(R, x, y) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:\mathrm{EntRel}(A, B)}{\Gamma \vdash \mathrm{entrelwitn}(R):\mathrm{isEntire}(x:A.y:B.\mathrm{El}(R, x, y))}$$

Computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash R(x, y) \quad \Gamma \vdash p:\mathrm{isEntire}(x:A.y:B.R(x, y))}{\Gamma, x:A, y:B \vdash \mathrm{El}(\mathrm{toElem}_{A, B, R}(p), x, y) \equiv R(x, y) \; \mathrm{type}}$$

* Judgmental computation rules

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash R(x, y) \quad \Gamma \vdash p:\mathrm{isEntire}(x:A.y:B.R(x, y))}{\Gamma \vdash \mathrm{entrelwitn}(\mathrm{toElem}_{A, B, R}(p)) \equiv p:\mathrm{isEntire}(x:A.y:B.R(x, y))}$$

* Typal computation rules

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash R(x, y) \quad \Gamma \vdash p:\mathrm{isEntire}(x:A.y:B.R(x, y))}{\Gamma \vdash \beta_{\mathrm{EntRel}(A, B)}^{\mathrm{entrelwitn}, R}:\mathrm{entrelwitn}(\mathrm{toElem}_{A, B, R}(p)) =_{\mathrm{isEntire}(x:A.y:B.R(x, y))} p}$$

Uniqueness rules:

* Judgmental uniqueness rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:\mathrm{EntRel}(A, B)}{\Gamma \vdash \mathrm{toElem}_{A, B, \mathrm{El}(R)}(\mathrm{entrelwitn}(R)) \equiv R:\mathrm{EntRel}(A, B)}$$

* Typal uniqueness rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:\mathrm{EntRel}(A, B)}{\Gamma \vdash \eta_{\mathrm{EntRel}(A, B)}(R):\mathrm{toElem}_{A, B, \mathrm{El}(R)}(\mathrm{entrelwitn}(R)) =_{\mathrm{EntRel}(A, B)} R}$$

Extensionality rule:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:\mathrm{EntRel}(A, B) \quad \Gamma \vdash S:\mathrm{EntRel}(A, B)}{\Gamma \vdash \mathrm{entrelext}_{A, B}(R, S):(R =_{\mathrm{EntRel}(A, B)} S) \simeq \prod_{x:A} \prod_{y:B} \mathrm{El}(R, x, y) \simeq \mathrm{El}(S, x, y)}$$

### Weakly a la Tarski

Weakly a la Tarski, the type of all entire relations is given by the following rules:

Formation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{EntRel}(A, B) \; \mathrm{type}}$$

Introduction rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash R(x, y)}{\Gamma \vdash \mathrm{toElem}_{A, B, R}:\mathrm{isEntire}(x:A.y:B.R(x, y)) \to \mathrm{EntRel}(A, B)}$$

Elimination rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:\mathrm{EntRel}(A, B)}{\Gamma, x:A, y:B \vdash \mathrm{El}(R, x, y) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:\mathrm{EntRel}(A, B)}{\Gamma \vdash \mathrm{entrelwitn}(R):\mathrm{isEntire}(x:A.y:B.\mathrm{El}(R, x, y))}$$

Computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash R(x, y) \quad \Gamma \vdash p:\mathrm{isEntire}(x:A.y:B.R(x, y))}{\Gamma, x:A, y:B \vdash \beta_{\mathrm{EntRel}(A, B)}^{\mathrm{El}, R}(p, x, y):\mathrm{El}(\mathrm{toElem}_{A, B, R}(p), x, y) \simeq R(x, y)}$$

* Judgmental computation rules

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash R(x, y) \quad \Gamma \vdash p:\mathrm{isEntire}(x:A.y:B.R(x, y))}{\Gamma \vdash (\mathrm{congform}_{\mathrm{isEntire}}(\beta_{\mathrm{EntRel}(A, B)}^{\mathrm{El}, R}(p)))(\mathrm{entrelwitn}(\mathrm{toElem}_{A, B, R}(p))) \equiv p:\mathrm{isEntire}(x:A.y:B.R(x, y))}$$

* Typal computation rules

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash R(x, y) \quad \Gamma \vdash p:\mathrm{isEntire}(x:A.y:B.R(x, y))}{\Gamma \vdash \beta_{\mathrm{EntRel}(A, B)}^{\mathrm{entrelwitn}, R}:(\mathrm{congform}_{\mathrm{isEntire}}(\beta_{\mathrm{EntRel}(A, B)}^{\mathrm{El}, R}(p)))(\mathrm{entrelwitn}(\mathrm{toElem}_{A, B, R}(p))) =_{\mathrm{isEntire}(x:A.y:B.R(x, y))} p}$$

where the equivalence
$$\mathrm{congform}_{\mathrm{isEntire}}(\beta_{\mathrm{EntRel}(A, B)}^{\mathrm{El}, R}(p)):\mathrm{isEntire}(x:A.y:B.\mathrm{El}(R, x, y)) \simeq \mathrm{isEntire}(x:A.y:B.R(x, y))$$
is provided from the typal computation rules for $\mathrm{isEntire}(x:A.y:B.R(x, y))$. 

Uniqueness rules:

* Judgmental uniqueness rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:\mathrm{EntRel}(A, B)}{\Gamma \vdash \mathrm{toElem}_{A, B, \mathrm{El}(R)}(\mathrm{entrelwitn}(R)) \equiv R:\mathrm{EntRel}(A, B)}$$

* Typal uniqueness rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:\mathrm{EntRel}(A, B)}{\Gamma \vdash \eta_{\mathrm{EntRel}(A, B)}(R):\mathrm{toElem}_{A, B, \mathrm{El}(R)}(\mathrm{entrelwitn}(R)) =_{\mathrm{EntRel}(A, B)} R}$$

Extensionality rule:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:\mathrm{EntRel}(A, B) \quad \Gamma \vdash S:\mathrm{EntRel}(A, B)}{\Gamma \vdash \mathrm{entrelext}_{A, B}(R, S):(R =_{\mathrm{EntRel}(A, B)} S) \simeq \prod_{x:A} \prod_{y:B} \mathrm{El}(R, x, y) \simeq \mathrm{El}(S, x, y)}$$

## Related concepts

* [[axiom of fullness]]

* [[type of propositions]]

[[!redirects type of entire relations]]
[[!redirects types of entire relations]]

[[!redirects weak type of entire relations]]
[[!redirects weak types of entire relations]]

[[!redirects strict type of entire relations]]
[[!redirects strict types of entire relations]]

[[!redirects type of all entire relations]]
[[!redirects types of all entire relations]]

[[!redirects weak type of all entire relations]]
[[!redirects weak types of all entire relations]]

[[!redirects strict type of all entire relations]]
[[!redirects strict types of all entire relations]]