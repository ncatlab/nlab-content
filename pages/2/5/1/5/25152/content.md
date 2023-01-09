
\tableofcontents

## Definition

### In first order logic with equality

In [[first order logic with equality]], given a predicate $P$ on a type $T$ with equality, the __uniqueness quantifier__ of $P$, denoted $\exists!\, x\colon T, P(x)$, is defined in terms of the universal and existential quantifiers as

$$ \exists!\, x\colon T, P(x) \;\equiv\; \exists\, x\colon T, P(x) \wedge \forall\, y\colon T, P(y) \Rightarrow (x = y) .$$

The intended interpretation is that $\exists!\, x\colon T, P(x)$ is true iff $P(a)$ is true for *exactly* one element $a$ of $T$.

### In dependent type theory

In [[dependent type theory]], given a type $T$ and a type family $x:T \vdash P(x)$, the uniqueness quantifier is a type defined as 

$$\exists!\, x\colon T. P(x) \equiv \mathrm{isContr}\left(\sum_{x:T} P(x)\right)$$

which indicates that the [[dependent sum type]] $\sum_{x:T} P(x)$ is a [[contractible type]], which is only the case for a family of type if every dependent type is a mere proposition and, for exactly one element $x:T$ up to identity, the type $P(x)$ is inhabited. 

The uniqueness quantifier is used in the definition of an [[equivalence in type theory]], where one defines a function $f:A \to B$ to be an equivalence if for all $y:B$ the there is a unique $x:A$ such that $f(x) =_B y$

$$\mathrm{isEquiv}(f) \coloneqq \prod_{y:B} \exists! x:A.f(x) =_B y$$ 

Similarly, it is used in the definition of an [[anafunction]], where one defines a [[correspondence]] $x:A, y:B \vdash R(x, y)$ to be an anafunction if for all $x:A$ there is a unique $y:B$ such that $R(x, y)$

$$\mathrm{isAnafunc}(R) \coloneqq \prod_{x:A} \exists! y:B.R(x, y)$$ 

## See also

* [[existential quantifier]]

* [[universal quantifier]]

[[!redirects uniquely quantified]]

[[!redirects uniqueness quantifier]]
[[!redirects uniqueness quantifiers]]
[[!redirects uniqueness quantification]]
[[!redirects uniqueness quantifications]]
[[!redirects unicity quantifier]]
[[!redirects unicity quantifiers]]
[[!redirects unicity quantification]]
[[!redirects unicity quantifications]]