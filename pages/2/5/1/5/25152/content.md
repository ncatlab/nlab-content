
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

### In first order logic with equality

#### Uniqueness up to equality

In [[first order logic with equality]], given a predicate $P$ on a type $T$ with equality, the __uniqueness quantifier__ of $P$, denoted $\exists!\, x\colon T, P(x)$, is defined in terms of the universal and existential quantifiers as

$$ \exists!\, x\colon T, P(x) \;\equiv\; \exists\, x\colon T, P(x) \wedge \forall\, y\colon T, P(y) \Rightarrow (x = y) .$$

The intended interpretation is that $\exists!\, x\colon T, P(x)$ is true iff $P(a)$ is true for *exactly* one element $a$ of $T$.

#### Uniqueness up to isomorphism

Sometimes, we want to use a weaker notion of [[equivalence]] than strict [[equality]], such as [[isomorphism]] $x \cong y$. The __uniqueness up to isomorphism quantifier__ of $P$, denoted $\exists!_\cong\, x\colon T, P(x)$, is defined in terms of the universal and existential quantifiers as

$$ \exists!_\cong\, x\colon T, P(x) \;\equiv\; \exists\, x\colon T, P(x) \wedge \forall\, y\colon T, P(y) \Rightarrow (x \cong y).$$

The intended interpretation is that $\exists!_\cong\, x\colon T, P(x)$ is true iff $P(a)$ is true for *exactly* one element $a$ of $T$ up to isomorphism.

Uniqueness up to isomorphism quantifiers are important in [[category theory]], where the relevant notion of sameness is isomorphism rather than strict equality. It is also important in [[foundations|foundational]] [[set theories]] where the type of sets does not have equality, such as some presentations of [[SEAR]] and [[ETCS]]. 

### In dependent type theory

In [[dependent type theory]], given a type $T$ and a type family $x:T \vdash P(x)$, the uniqueness quantifier is a type defined as 

$$\exists!\, x\colon T. P(x) \coloneqq \mathrm{isContr}\left(\sum_{x:T} P(x)\right)$$

which indicates that the [[dependent sum type]] $\sum_{x:T} P(x)$ is a [[contractible type]], which is only the case for a family of type if every dependent type is a mere proposition and, for exactly one element $x:T$ up to identity, the type $P(x)$ is inhabited. 

## Usages

### Defining exclusive disjunction

In [[dependent type theory]], given two [[mere propositions]] $P$ and $Q$, by [[descent]] or [[large elimination]] of the [[type of booleans]], one can construct a boolean-indexed family of propositions 

$$x:\mathrm{bool} \vdash \mathrm{rec}_\mathrm{bool}^{P, Q}(x)$$

with [[equivalences of types]]

$$\beta_\mathrm{bool}^{P, Q}(0):\mathrm{rec}_\mathrm{bool}^{P, Q}(0) \simeq P \quad \beta_\mathrm{bool}^{P, Q}(1):\mathrm{rec}_\mathrm{bool}^{P, Q}(1) \simeq Q$$

in the case for descent for booleans, or with [[judgmental equality]] of types

$$\mathrm{rec}_\mathrm{bool}^{P, Q}(0) \equiv P \quad \mathrm{rec}_\mathrm{bool}^{P, Q}(1) \equiv P$$

in the case for large elimination for booleans. 

The uniqueness quantifier of the above family of propositions is the [[exclusive disjunction]] of $P$ and $Q$:

$$P \underline{\vee} Q \coloneqq \exists!x:\mathbb{2}.\mathrm{rec}_\mathrm{bool}^{P, Q}(x)$$

### Bijections and equivalences

The uniqueness quantifier is used in the definition of a [[bijection]] in [[set theory]] and an [[equivalence in type theory]], where one defines a [[function]] $f:A \to B$ to be a bijection or equivalence if for all $y:B$ the there is a unique $x:A$ such that $f(x) =_B y$

$$\mathrm{isEquiv}(f) \coloneqq \forall y:B.\exists! x:A.f(x) =_B y$$ 

In [[dependent type theory]], this is the same as defining a family of elements $x:A \vdash f(x):B$ to be an equivalence if it comes with a family of elements
$$y:B \vdash \epsilon(f)(y):\exists! x:A.f(x) =_B y$$
The [[inverse]] of an equivalence is given by the family of elements $y:B \vdash \epsilon_A(\epsilon(f)(y)):A$, where $\epsilon_A$ is defined in the [[elimination rules]] for [[uniqueness quantifiers]] in [[dependent type theory]]. 

### Anafunctions

Similarly, uniqueness quantifications is used in the definition of an [[anafunction]], where one defines a [[relation]] or [[correspondence]] $x:A, y:B \vdash R(x, y)$ to be an anafunction if for all $x:A$ there is a unique $y:B$ such that $R(x, y)$

$$\mathrm{isAnafunc}(R) \coloneqq \forall x:A.\exists! y:B.R(x, y)$$ 

### Univalent universes

Uniqueness quantifiers are also used to define [[univalent universes]]. A [[Russell universe]] $U$ is a [[univalent universe]] if for all elements $A:U$ there is a unique $B:U$ such that $A \simeq B$:

$$\mathrm{isUnivalent}(U) \coloneqq \forall A:U.\exists! B:U.A \simeq B$$

Similarly, a [[Tarski universe]] $(U, T)$ is a [[univalent universe]] if for all elements $A:U$ there is a unique $B:U$ such that $T(A) \simeq T(B)$:

$$\mathrm{isUnivalent}(U, T) \coloneqq \forall A:U.\exists! B:U.T(A) \simeq T(B)$$

## Related concepts

* [[quantification]]

* [[existential quantifier]]

* [[universal quantifier]]

* [[definite description]]

* [[generalized the]]

* [[exclusive disjunction]]

## References

* [Uniqueness quantification](https://en.wikipedia.org/wiki/Uniqueness_quantification)

[[!redirects uniquely quantified]]

[[!redirects uniqueness quantifier]]
[[!redirects uniqueness quantifiers]]
[[!redirects uniqueness quantification]]
[[!redirects uniqueness quantifications]]
[[!redirects unicity quantifier]]
[[!redirects unicity quantifiers]]
[[!redirects unicity quantification]]
[[!redirects unicity quantifications]]

[[!redirects there exists a unique]]
[[!redirects there is a unique]]