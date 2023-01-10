
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

#### Rules for uniqueness quantifiers

If the [[dependent type theory]] has [[identity types]] and [[dependent identity types]], one could directly form the uniqueness quantifier via its [[natural deduction]] rules:

Formation rules for uniqueness quantifier types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \exists!x:A.B(x) \; \mathrm{type}}$$

Introduction rules for uniqueness quantifier types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:B(a) \quad \Gamma, x:A, y:B(x) \vdash \tau_A(x, y):a =_A x \quad \Gamma, x:A, y:B(x) \vdash \tau_B(x, y):b =_B^{\tau_A(x, y)} y}{\Gamma \vdash w(a, b, \tau_A, \tau_B):\exists!x:A.B(x)}$$

Elimination rules for uniqueness quantifier types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash p:\exists!x:A.B(x)}{\Gamma \vdash \epsilon_A(p):A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash p:\exists!x:A.B(x)}{\Gamma \vdash \epsilon_B(p):B(\epsilon_A(p))}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash p:\exists!x:A.B(x)}{\Gamma, x:A, y:B(x) \vdash c_A(p, x, y):\epsilon_A(p) =_A x}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash p:\exists!x:A.B(x)}{\Gamma, x:A, y:B(x) \vdash c_B(p, x, y):\epsilon_B(p) =_B^{c_A(p, x, y)} y}$$

Computation rules for uniqueness quantifier types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:B(a) \quad \Gamma, x:A, y:B(x) \vdash \tau_A(x, y):a =_A x \quad \Gamma, x:A, y:B(x) \vdash \tau_B(x, y):b =_B^{\tau_A(x, y)} y}{\Gamma \vdash \beta_{\exists!x:A.B(x)}^{\epsilon_A}(a, b):\epsilon_A(w(a, b, \tau_A, \tau_B)) =_A a}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:B(a) \quad \Gamma, x:A, y:B(x) \vdash \tau_A(x, y):a =_A x \quad \Gamma, x:A, y:B(x) \vdash \tau_B(x, y):b =_B^{\tau_A(x, y)} y}{\Gamma \vdash \beta_{\exists!x:A.B(x)}^{\epsilon_B}(a, b):\epsilon_B(w(a, b, \tau_A, \tau_B))) =_B^{\beta_{\exists!x:A.B(x)}^{\epsilon_A}(a, b)} b}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:B(a) \quad \Gamma, x:A, y:B(x) \vdash \tau_A(x, y):a =_A x \quad \Gamma, x:A, y:B(x) \vdash \tau_B(x, y):b =_B^{\tau_A(x, y)} y}{\Gamma, x:A, y:B(x) \vdash \beta_{\exists!x:A.B(x)}^{c_A}(a, b, x, y):c_A(w(a, b, \tau_A, \tau_B), x, y) =_{p:(-) =_A x}^{\beta_{\exists!x:A.B(x)}^{\epsilon_A}} \tau_A(x, y)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:B(a) \quad \Gamma, x:A, y:B(x) \vdash \tau_A(x, y):a =_A x \quad \Gamma, x:A, y:B(x) \vdash \tau_B(x, y):b =_B^{\tau_A(x, y)} y}{\Gamma, x:A, y:B(x) \vdash \beta_{\exists!x:A.B(x)}^{c_B}(a, b, x, y):c_B(w(a, b, \tau_A, \tau_B), x, y) =_{(-) =_B^{\beta_{\exists!x:A.B(x)}^{c_A}(a, b, x, y)} y}^{\beta_{\exists!x:A.B(x)}^{\epsilon_B}} \tau_B(x, y)}$$

Uniqueness rules for uniqueness quantifier types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash p:\exists!x:A.B(x)}{\Gamma \vdash \eta_{\exists!x:A.B(x)}(p):w(\epsilon_A(p), \epsilon_B(p), c_A(p), c_B(p)) =_{\exists!x:A.B(x)} p}$$

#### Usage

The uniqueness quantifier is used in the definition of an [[equivalence in type theory]], where one defines a function $f:A \to B$ to be an equivalence if for all $y:B$ the there is a unique $x:A$ such that $f(x) =_B y$

$$\mathrm{isEquiv}(f) \coloneqq \prod_{y:B} \exists! x:A.f(x) =_B y$$ 

This is the same as defining a family of elements $x:A \vdash f(x):B$ to be an equivalence if it comes with a family of elements
$$y:B \vdash \epsilon(f)(y):\exists! x:A.f(x) =_B y$$

Similarly, it is used in the definition of an [[anafunction]], where one defines a [[correspondence]] $x:A, y:B \vdash R(x, y)$ to be an anafunction if for all $x:A$ there is a unique $y:B$ such that $R(x, y)$

$$\mathrm{isAnafunc}(R) \coloneqq \prod_{x:A} \exists! y:B.R(x, y)$$ 

## See also

* [[quantification]]

* [[existential quantifier]]

* [[universal quantifier]]

* [[definite description]]

* [[generalized the]]

[[!redirects uniquely quantified]]

[[!redirects uniqueness quantifier]]
[[!redirects uniqueness quantifiers]]
[[!redirects uniqueness quantification]]
[[!redirects uniqueness quantifications]]
[[!redirects unicity quantifier]]
[[!redirects unicity quantifiers]]
[[!redirects unicity quantification]]
[[!redirects unicity quantifications]]