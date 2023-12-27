
#Contents#
* table of contents
{:toc}

## Definition

Given two sets $S$ and $T$, there is a function $c:T \to (S \to T)$ such that for every element $x:T$ there is a function $c(x):S \to T$ such that for every element $a:S$, $c(x)(a) = x$. For every element $x:T$, the function $c(x)$ is called the __constant function__ from $S$ to $T$ with value $x$. 

Given two [[sets]] $S$ and $T$ and an element $x$ of $T$, the __constant function__ from $S$ to $T$ with value $x$ is the [[function]] $f$ defined by
$$ f(a) = x $$
for every element $a$ of $S$.

More generally, any function $f: S \to T$ is a __constant function__ if
$$ f(a) = f(b) $$
for every element $a$ and element $b$ of $S$.  Note that every constant function with particular value (as defined earlier) is constant (as defined here).

The converse is a little more complicated.  If $S$ is [[inhabited set|inhabited]], then every constant function from $S$ to $T$ is the constant function from $S$ to $T$ with some particular value, which is unique.  If $S$ is [[empty set|empty]] but $T$ is inhabited, then the unique function from $S$ to $T$ is constant with any particular value in $T$.  If $S$ and $T$ are both empty, then the unique function from $S$ to $T$ is constant, but not constant at any particular value.

Using [[excluded middle]], we can say that, if $T$ is inhabited, then any constant function from $S$ to $T$ is constant at some (possibly not unique) value, but this theorem fails in [[constructive mathematics]].

See also [[constant morphism]].

### In dependent type theory

In [[dependent type theory]], a **propositionally constant function** or **typally constant function** from type $A$ to $B$ at an element $b:B$ is a function $f:A \to B$ such that $f(x) =_B b$ for all $x:A$. Equivalently, it is an element of the dependent sum type

$$\sum_{b:B} \sum_{f:A \to B} \prod_{x:A} f(x) =_B b$$

For all $b:B$, there is always a propositionally constant function given by $\lambda x:A.b:A \to B$ with $\beta_{A, B}^{x:A.b}:\prod_{x:A} (\lambda x:A.b)(x) =_B b$ from the typal [[computation rules]] for [[function types]], or 

$$(b, \lambda x:A.b, \beta_{A, B}^{x:A.b}):\sum_{b:B} \sum_{f:A \to B} \prod_{x:A} f(x) =_B b$$

When function types have judgmental computation rules than one has $\beta_{A, B}^{x:A.b} \equiv \lambda x:A.\mathrm{refl}_B(b)$. 

Alternatively, a propositionally constant function $f:A \to B$ is a function which factors through the base generator $\mathrm{base}:A \to \mathrm{Cone}(A)$ of the [[cone type]] of $A$; there exists a function $b:\mathrm{Cone}(A) \to B$ such that for all $x:A$, $b(\mathrm{base}(x)) \equiv f(x)$. Since the [[cone type]] of $A$ is always a [[contractible type]], it is a [[terminal object]] in types. 

Given a propositionally constant function $f:A \to B$ with $p:\prod_{x:A} f(x) =_B b$, by the recursion principle of the cone type, one has 

$$\mathrm{rec}_{\mathrm{Cone}(A)}^B(b, f, p):\mathrm{Cone}(A) \to B$$

such that 

$$\mathrm{rec}_{\mathrm{Cone}(A)}^B(b, f, p)(\mathrm{vertex}) \equiv b:B$$

$$\mathrm{rec}_{\mathrm{Cone}(A)}^B(b, f, p)(\mathrm{base}(x)) \equiv f(x):B$$

$$\mathrm{ap}_{\mathrm{rec}_{\mathrm{Cone}(A)}^B(b, f, p)}(\mathrm{edge}(x)) \equiv p:f(x) =_B b$$

## Related concepts

* [[constant of a theory]]

* **constant function** /  [[locally constant function]] 

* [[constant sheaf]] / [[locally constant sheaf]]

* [[constant stack]] / [[locally constant stack]]

* [[constant ∞-stack]] / [[locally constant ∞-stack]]

* [[local system]]

* [[weakly constant function]]

* [[deterministic random variable]], [[almost surely]]

* [[cone type]]

[[!redirects constant function]]
[[!redirects constant functions]]
[[!redirects constant map]]
[[!redirects constant maps]]

[[!redirects propositionally constant function]]
[[!redirects propositionally constant functions]]
[[!redirects propositionally constant map]]
[[!redirects propositionally constant maps]]

[[!redirects typally constant function]]
[[!redirects typally constant functions]]
[[!redirects typally constant map]]
[[!redirects typally constant maps]]
