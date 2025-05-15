
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

Let $A$ be a type and let $x:A \vdash B(x)$ be a type family. 

Traditionally a record type with type fields is a [[dependent sum types]] involving a type universe field: suppose we have a Russell universe $U$ or a Tarski universe $(U, T)$ and a function $P:(A \to U) \to U$ representing the non-type fields of the record type. Then the type of record types with type fields is given by the [[dependent sum type]] 
$$\sum_{A:U} \sum_{B:A \to U} P(A, B) \qquad \sum_{A:U} \sum_{B:T(A) \to U} T(P(A, B)$$ 
for Russell universes and Tarski universes respectively, where $A$ is the index type of the family $B$ of type fields. 

But in a dependent type theory with a separate [[type]] [[judgment]], types are not elements of universes. Instead of the above notion of "record type with $U$-small types fields", we have the notion of "record types with type fields". Type families $(B(x))_{x:A}$, previously functions $B:A \to U$, are now judged to be types in [[context]] $x:A \vdash B(x) \; \mathrm{type}$. The function $P:(A \to U) \to U$ which takes types to propostions is now an operator on types and type families, which is defined using [[inference rules]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x)}{\Gamma \vdash P(\underline{ }x.B(x)) \; \mathrm{type}}$$

Examples of such $P$ definable from the existing type formers in [[dependent type theory]], include

* $\mathrm{isProp}$, which results in the [[type of propositions]], 
* $\mathrm{isMutuallyExclusive}$, which results in the [[type of mutually exclusive propositions]], 
* $\mathrm{isFinite}$, which results in the [[type of finite types]], 
* given a type $T$, $[(-) \simeq T]$, which results in the type of all types merely [[equivalence of types|equivalent]] to $T$. 
* given a type $T$, $[(-) \hookrightarrow T]$, which results in the [[subobject preorder|subtype preorder]] of $T$, the type of all types which merely [[embedding of types|embed into]] $T$. 

The resulting record type with type fields $(B(x))_{x:A}$ and non-type fields $P$ is denoted in this section by $\mathrm{Type}_P$. 

Care must be taken for which $P$ one could use to define the record type with type fields. For example, given [[unit type]] $\mathbb{1}$ and the type family $(B(x))_{x:\mathbb{1}}$, for $P(\underline{ }x.B(x)) \equiv B(\mathrm{pt}) \to \mathbb{1}$ and $P(\underline{ }x.B(x)) \equiv \mathrm{isSet}(B(\mathrm{pt}))$, the resulting $\mathrm{Type}_P$ always contains itself or its [[set truncation]] in addition to the [[empty type]], resulting in [[Girard's paradox]]; thus, one cannot form such record types with type fields in the type theory. 

## Related concepts

* [[dependent sum type]]

* [[negative type]]

* [[type of types]]

## References

* Wikipedia, <a href="https://en.wikipedia.org/wiki/Record_(computer_science)">Record (computer science)</a>

[[!redirects record]]
[[!redirects records]]

[[!redirects record type]]
[[!redirects record types]]

[[!redirects finitary record type]]
[[!redirects finitary record types]]

[[!redirects infinitary record type]]
[[!redirects infinitary record types]]

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
