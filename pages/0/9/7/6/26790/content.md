
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[dependent type theory]], a **record type** is a type which consists of variadic [[tuples]] called *records*, whose individual elements in the tuples are called *fields*. 

Finitary record types can be defined in terms of the [[unit type]] and iterated [[dependent sum types]]. Examples of finitary record types include [[unit types]], [[negative copies]], [[product types]], [[dependent sum types]], etc...

Infinitary record types have an infinite number of fields and require something like [[two-level type theory]] to be implemented. An example of an infinitary record type is any [[semi-simplicial types in homotopy type theory|semi-simplicial type]]. 

## Implementations

Most type-theory based proof assistants include primitive record types, with [[dependent sum types]] defined as a particular case of these, rather than requiring general record types to be defined using dependent sum types.  This includes:

* [[Coq]]
* [[Agda]]
* [[Lean]]
* [[Narya]]

## Record types with type fields

It is also possible to have "record types" whose fields themselves are types. These are typically [[types of types]] with additional structure. 

For example, traditionally we have [[dependent sum types]] involving a type universe field: suppose we have a Russell universe $U$ or a Tarski universe $(U, T)$ and a function $P:U \to U$. Then the type of $U$-small types which have the structure $P$ is given by the [[dependent sum type]] $\sum_{A:U} P(A)$ for Russell universes and $\sum_{A:U} T(P(A))$ for Tarski universes. 

But in a dependent type theory with a separate [[type]] [[judgment]], types are not elements of universes. Instead of the above notion of "type of $U$-small types which have the structure $P$", we have the notion of "type of all types which have the structure $P$". Types $A$, previously elements of the universe $A:U$, are now judged to be types $A \; \mathrm{type}$. The function $P:U \to U$ which takes types to propostions is now an operator on types, which is defined using [[inference rules]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash P(A) \; \mathrm{type}}$$

or in [[dependent type theory with type variables]], as a type family 

$$A \; \mathrm{type} \vdash P(A) \; \mathrm{type}$$

Examples of such $P$ definable from the existing type formers in [[dependent type theory]] include 

* $\mathrm{isProp}$, which results in the [[type of all propositions]], 
* $\mathrm{isFinite}$, which results in the [[type of all finite types]], 
* given a type $T$, $[(-) \simeq T]$, which results in the type of all types merely [[equivalence of types|equivalent]] to $T$. 
* given a type $T$, $[(-) \hookrightarrow T]$, which results in the [[subobject preorder|subtype preorder]] of $T$, the type of all types which merely [[embedding of types|embed into]] $T$. 

The resulting type of all types which have the structure $P$ is denoted in this section by $\mathrm{Type}_P$. 

Care must be taken for which $P$ one could use to define the record type of all types which have the structure $P$. For example, given [[unit type]] $\mathbb{1}$, for $P(A) \equiv A \to \mathbb{1}$ and $P(A) \equiv \mathrm{isSet}(A)$, the resulting $\mathrm{Type}_P$ always contains itself or its [[set truncation]] in addition to the [[empty type]], resulting in [[Girard's paradox]]; thus, one cannot form such record types with type fields in the type theory. 

Now, similar to [[type universes]], $\mathrm{Type}_P$ could be presented either [[a la Russell]] or [[a la Tarski]] in a [[dependent type theory]]. The difference between the two is that in the former, every type which satisfies $P$ in the type theory is literally an element of the type of types which satisfy $P$, while in the latter, elements of $\mathrm{Type}_P$ are only indices of a type family $\mathrm{El}$; every [[finite type]] in the type theory is only [[essentially small type|essentially $\mathrm{Type}_P$-small]] for [[weakly Tarski]] record types or [[judgmentally equal]] to an $P(A)$ for $A:\mathrm{Type}_P$ for [[strictly Tarski]] record types. 

For weak Tarski record types with satisfy $P$, one also needs the typal congruence rules for forming $P(A)$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{congform}_P(e):P(A) \simeq P(B) \; \mathrm{type}}$$

#### Strictly a la Tarski

Presented strictly a la Tarski, the type of all types which have the structure $P$ is given by the following [[natural deduction]] [[inference rules]]:

Formation rules for the type of all types which have the structure $P$:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{Type}_P \; \mathrm{type}}$$

Introduction rules for the type of all types which have the structure $P$:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{toElem}_A:P(A) \to \mathrm{Type}_P}$$

Elimination rules for the type of all types which have the structure $P$:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \mathrm{El}(A) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \mathrm{witn}_P(A):P(\mathrm{El}(A))}$$

Computation rules for the type of all types which have the structure $P$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \mathrm{El}(\mathrm{toElem}_A(p)) \equiv A \; \mathrm{type}}$$

* Judgmental computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \mathrm{witn}_P(\mathrm{toElem}_A(p)) \equiv p:P(A)}$$

* Typal computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \beta_{\mathrm{Type}_P}^{\mathrm{Witn}_P,A}(p):\mathrm{witn}_P(\mathrm{toElem}_A(p)) =_{P(A)} p}$$

Uniqueness rules for the type of all types which have the structure $P$:

* Judgmental computation rules:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \mathrm{toElem}_{\mathrm{El}(A)}(\mathrm{witn}_P(A)) \equiv A:\mathrm{Type}_P}$$

* Typal computation rules:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \eta_{\mathrm{Type}_P}(A):\mathrm{toElem}_{\mathrm{El}(A)}(\mathrm{witn}_P(A)) =_{\mathrm{Type}_P} A}$$

[[univalence axiom|Extensionality principle]] of the type of all types which have the structure $P$:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P \quad \Gamma \vdash B:\mathrm{Type}_P} {\Gamma \vdash \mathrm{ext}_{\mathrm{Type}_P}(A, B):\mathrm{isEquiv}(\mathrm{transport}^\mathrm{El}(A, B))}$$

#### Weakly a la Tarski

Presented [[weakly a la Tarski]], the type of all types which have the structure $P$ is given by the following [[natural deduction]] [[inference rules]]:

Formation rules for the type of all types which have the structure $P$:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{Type}_P \; \mathrm{type}}$$

Introduction rules for the type of all types which have the structure $P$:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{toElem}_A:P(A) \to \mathrm{Type}_P}$$

Elimination rules for the type of all types which have the structure $P$:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \mathrm{El}(A) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \mathrm{witn}_P(A):P(\mathrm{El}(A))}$$

Computation rules for the type of all types which have the structure $P$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \beta_{\mathrm{Type}_P}^{\mathrm{El}, A}(p):\mathrm{El}(\mathrm{toElem}_A(p)) \simeq A \; \mathrm{type}}$$

* Judgmental computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \mathrm{congform}_P(\beta_{\mathrm{Type}_P}^{\mathrm{El}, A}(p))(\mathrm{witn}_P(\mathrm{toElem}_A(p))) \equiv p:P(A)}$$

* Typal computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \beta_{\mathrm{Type}_P}^{\mathrm{witn}_P,A}(p):\mathrm{congform}_P(\beta_{\mathrm{Type}_P}^{\mathrm{El}, A}(p))(\mathrm{witn}_P(\mathrm{toElem}_A(p))) =_{P(A)} p}$$

where the equivalence
$$\mathrm{congform}_P(\beta_{\mathrm{Type}_P}^{\mathrm{El}, A}(p)):P(\mathrm{El}(\mathrm{toElem}_A(p))) \simeq P(A)$$
is provided from the typal computation rules for $P(A)$. 

Uniqueness rules for the type of all types which have the structure $P$:

* Judgmental computation rules:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash A \equiv \mathrm{toElem}_{\mathrm{El}(A)}(\mathrm{witn}_P(A)):\mathrm{Type}_P}$$

* Typal computation rules:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \eta_{\mathrm{Type}_P}(A):A =_{\mathrm{Type}_P} \mathrm{toElem}_{\mathrm{El}(A)}(\mathrm{witn}_P(A))}$$

[[univalence axiom|Extensionality principle]] of the type of all types which have the structure $P$:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P \quad \Gamma \vdash B:\mathrm{Type}_P} {\Gamma \vdash \mathrm{ext}_{\mathrm{Type}_P}(A, B):\mathrm{isEquiv}(\mathrm{transport}^\mathrm{El}(A, B))}$$

#### A la Russell

Presented a la Russell, the type of all types which have the structure $P$ is given by the following [[natural deduction]] [[inference rules]]:

Formation rules for the type of all types which have the structure $P$:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{Type}_P \; \mathrm{type}}$$

Introduction rules for the type of all types which have the structure $P$:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{toElem}_A:P(A) \to \mathrm{Type}_P}$$

Elimination rules for the type of all types which have the structure $P$:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash A \; \mathrm{type}} \qquad \frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \mathrm{witn}_P(A):P(A)}$$

Computation rules for the type of all types which have the structure $P$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \mathrm{toElem}_A(p) \equiv A \; \mathrm{type}}$$

* Judgmental computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \mathrm{witn}_P(\mathrm{toElem}_A(p)) \equiv p:P(A)}$$

* Typal computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \beta_{\mathrm{Type}_P}^{\mathrm{finWitn},A}(p):\mathrm{witn}_P(\mathrm{toElem}_A(p)) =_{P(A)} p}$$

Uniqueness rules for the type of all types which have the structure $P$:

* Judgmental computation rules:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \mathrm{toElem}_{A}(\mathrm{witn}_P(A)) \equiv A:\mathrm{Type}_P}$$

* Typal computation rules:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \eta_{\mathrm{Type}_P}(A):\mathrm{toElem}_{A}(\mathrm{witn}_P(A)) =_{\mathrm{Type}_P} A}$$

[[univalence axiom|Extensionality principle]] of the type of all types which satisfy $P$:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P \quad \Gamma \vdash B:\mathrm{Type}_P} {\Gamma \vdash \mathrm{ext}_{\mathrm{Type}_P}(A, B):\mathrm{isEquiv}(\mathrm{idToEquiv}(A, B))}$$ 

## Related concepts

* [[dependent sum type]]

* [[negative type]]

* [[type of types]]

## References

* Wikipedia, <a href="https://en.wikipedia.org/wiki/Record_(computer_science)">Record (computer science)</a>

[[!redirects record type]]
[[!redirects record types]]

[[!redirects record]]
[[!redirects records]]

[[!redirects record type with type fields]]
[[!redirects record types with type fields]]

[[!redirects Russell record type with type fields]]
[[!redirects Russell record types with type fields]]

[[!redirects Tarski record type with type fields]]
[[!redirects Tarski record types with type fields]]

[[!redirects Russell record type]]
[[!redirects Russell record types]]

[[!redirects record type a la Russell]]
[[!redirects record types a la Russell]]

[[!redirects record type à la Russell]]
[[!redirects record types à la Russell]]

[[!redirects Tarski record type]]
[[!redirects Tarski record types]]

[[!redirects record type a la Tarski]]
[[!redirects records type a la Tarski]]

[[!redirects record type à la Tarski]]
[[!redirects records type à la Tarski]]
