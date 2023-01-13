
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

## Idea

In [[dependent type theory]], given a type $A$, one could define a type $\mathrm{Copy}(A)$ called a **copy** of $A$, which is [[equivalence in type theory|equivalent]] to $A$.

## Definitions

There are two ways to define the copy $\mathrm{Copy}(A)$ of a type $A$, as a [[positive type]] or as a [[negative type]]

### Copies as a positive type

Copies as positive types are also called **unary sum types** or **positive unary product types**

The rules for positive copies are given as follows:

Formation rules for copies:
$$\frac{\Gamma A \; \mathrm{type}}{\Gamma \vdash \mathrm{Copy}(A) \; \mathrm{type}}$$

Introduction rules for copies:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{copy}(a):\mathrm{Copy}(A)}$$

Elimination rules for copies:
$$\frac{\Gamma, z:\mathrm{Copy}(A) \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:\mathrm{Copy}(A)}{\Gamma \vdash \mathrm{ind}_{\mathrm{Copy}(A)}^C(c, e):C[e/z]}$$

Computation rules for copies:
$$\frac{\Gamma, z:\mathrm{Copy}(A) \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_B:\mathrm{ind}_{\mathrm{Copy}(A)}^C(c, \mathrm{copy}(a)) =_{C[\mathrm{copy}(a)/z]} c[a/x]}$$

Uniqueness rules for copies:
$$\frac{\Gamma, z:\mathrm{Copy}(A) \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:\mathrm{Copy}(A) \quad \Gamma, y:\mathrm{Copy}(A) \vdash u:C \quad \Gamma, a:A \vdash i_\mathrm{copy}(u):u[\mathrm{copy}(a)/y] =_{C[\mathrm{copy}(a)/y]} c[a/x]}{\Gamma \vdash \eta_{\mathrm{Copy}(A)}:u[e/z] =_{C[e/z]} \mathrm{ind}_{\mathrm{Copy}(A)}^C(c, e)}$$

\begin{theorem}
$\mathrm{copy}$ is an [[equivalence of types]] between $A$ and $\mathrm{Copy}(A)$. 
\end{theorem}

\begin{proof}
Suppose one takes the type family $C$ in the elimination, computation, and uniqueness rules to be the type family $\sum_{x:A} \mathrm{copy}(x) =_{\mathrm{Copy}(A)} (-)$. Then the elimination rule states that $\sum_{x:A} \mathrm{copy}(x) =_{\mathrm{Copy}(A)} b$ has an element for all elements $b:\mathrm{Copy}(A)$, the computation rule states that given all elements $a:A$ the type $\sum_{x:A} \mathrm{copy}(x) =_{\mathrm{Copy}(A)} \mathrm{copy}(a)$ is contractible, and the uniqueness rule states that if the type $\sum_{x:A} \mathrm{copy}(x) =_{\mathrm{Copy}(A)} \mathrm{copy}(a)$ is contractible for all elements $a:A$, then the type $\sum_{x:A} \mathrm{copy}(x) =_B b$ is contractible for all elements $b:B$. Thus, $\mathrm{copy}$ is an [[equivalence of types]], since the type $\sum_{x:A} \mathrm{copy}(x) =_{\mathrm{Copy}(A)} b$ is contractible for all elements $b:\mathrm{Copy}(A)$. 
\end{proof}

### Copies as a negative type

Copies as negative types are also called **negative unary product types**

The rules for negative copies are given as follows:

Formation rules for copies:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{Copy}(A) \; \mathrm{type}}$$

Introduction rules for copies:
$$\frac{\Gamma \vdash a:A}{\Gamma \vdash \mathrm{copy}(a):\mathrm{Copy}(A)}$$

Elimination rules for copies:
$$\frac{\Gamma \vdash b:\mathrm{Copy}(A)}{\Gamma \vdash \mathrm{original}(b):A}$$

Computation rules for copies:
$$\frac{\Gamma \vdash a:A}{\Gamma \vdash \mathrm{original}(\mathrm{copy}(a)) \equiv a:A} \qquad \frac{\Gamma \vdash a:A}{\Gamma \vdash \mathrm{original}(\mathrm{copy}(a)) \equiv_A a \; \mathrm{true}} \qquad \frac{\Gamma \vdash a:A}{\Gamma \vdash \beta_{\mathrm{Copy}(A)}(a):\mathrm{original}(\mathrm{copy}(a)) =_A a}$$

Uniqueness rules for copies:
$$\frac{\Gamma \vdash b:\mathrm{Copy}(A)}{\Gamma \vdash b \equiv \mathrm{copy}(\mathrm{original}(b)):\mathrm{Copy}(A)} \qquad \frac{\Gamma \vdash b:B}{\Gamma \vdash b \equiv_{\mathrm{Copy}(A)} \mathrm{copy}(\mathrm{original}(b)) \; \mathrm{true}} \qquad \frac{\Gamma \vdash b:\mathrm{Copy}(A)}{\Gamma \vdash \eta_{\mathrm{Copy}(A)}(b):b =_{\mathrm{Copy}(A)} \mathrm{copy}(\mathrm{original}(b))}$$

Unary products with judgmental or propositional [[conversion rules]] turn $\mathrm{copy}$ into a [[judgmentally strict equivalence]] and a [[propositionally strict equivalence]] respectively. Unary products with only typal [[conversion rules]] turn $\mathrm{copy}$ and $\mathrm{original}$ into [[quasi-inverse functions]] of each other. One could then define a function $f:\mathrm{QInv}(\mathrm{copy}) \to \mathrm{isEquiv}(\mathrm{copy})$ which takes the quasi-inverse function $(\mathrm{original}, \beta_{\mathrm{Copy}(A)}, \eta_{\mathrm{Copy}(A)})$ to a witness that $\mathrm{copy}$ has [[contractible type|contractible]] [[fiber type|fibers]] and is thus an [[equivalence of types]]. 

## Extensionality principle for copies

The extensionality princple for copies says that for each element $x:A$ and $y:A$ the [[action on identities]] for the copy function $\mathrm{copy}$ is an [[equivalence of types]]

$$x:A, y:A \vdash \mathrm{copyext}(x, y):\mathrm{isEquiv}(\mathrm{ap}_{\mathrm{copy}}(x, y))$$

In [[Mike Shulman]]'s model of [[higher observational type theory]], this would be promoted to a [[judgmental equality]]:

$$x:A, y:A \vdash (x =_A y) \equiv (\mathrm{copy}(x) =_{\mathrm{Copy}(A)} \mathrm{copy}(y))$$

## Relation to equivalences

Given types $A$ and $B$ and $f:A \to B$, $f$ is an [[equivalence of types]] if $B$ satisfies the [[universal property]] of a positive copy type of $A$ with copy function $f:A \to B$. Indeed, one could define the [[isEquiv]] type family $f:A \to B \vdash \mathrm{isEquiv}(f)$ by very similar rules to the rules for positive copy types:

Formation rules for isEquiv:
$$\frac{\Gamma A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B}{\Gamma \vdash \mathrm{isEquiv}(f) \; \mathrm{type}}$$

Introduction rules for isEquiv:
$$\frac{\Gamma A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash a:A \quad \Gamma, y:B \vdash b(y):f(a) =_B y \quad \Gamma, x:A, y:B, z:f(x) =_B y \vdash \tau_A(x, y, z):a =_A x \quad \Gamma, x:A, y:B, z:f(x) =_B y \vdash \tau_B(x, y, z):b(y) =_B^{\tau_A(x, y, z)} z}{\Gamma \vdash w(a, b, \tau_A, \tau_B):\mathrm{isEquiv}(f)}$$

Elimination rules for isEquiv:
$$\frac{\Gamma A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash p:\mathrm{isEquiv}(f) \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[f(x)/z] \quad \Gamma \vdash e:B}{\Gamma \vdash \mathrm{ind}_{\mathrm{isEquiv}(f)}^C(c, e):C[e/z]}$$

Computation rules for isEquiv:
$$\frac{\Gamma A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash p:\mathrm{isEquiv}(f) \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[f(x)/z] \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_B:\mathrm{ind}_{\mathrm{isEquiv}(f)}^C(c, f(a)) =_{C[f(a)/z]} c[a/x]}$$

Uniqueness rules for isEquiv:
$$\frac{\Gamma A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B \quad \Gamma \vdash p:\mathrm{isEquiv}(f) \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[f(x)/z] \quad \Gamma \vdash e:\mathrm{isEquiv}(f) \quad \Gamma, y:B \vdash u:C \quad \Gamma, a:A \vdash i_f(u):u[f(a)/y] =_{C[f(a)/y]} c[a/x]}{\Gamma \vdash \eta_{\mathrm{isEquiv}(f)}:u[e/z] =_{C[e/z]} \mathrm{ind}_{\mathrm{isEquiv}(f)}^C(c, e)}$$

## See also

* [[equivalence in type theory]]
* [[unit type]]
* [[dependent sum type]]
* [[sum type]]
* [[definition]]

## References

Copying types could be found in 

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]], *[[Symmetry]]* (2021) $[$[pdf](https://unimath.github.io/SymmetryBook/book.pdf)$]$ 

[[!redirects copy]]
[[!redirects copies]]
[[!redirects copying]]

[[!redirects copy type]]
[[!redirects copy types]]

[[!redirects copying types]]

[[!redirects unary sum]]
[[!redirects unary sums]]

[[!redirects unary sum type]]
[[!redirects unary sum types]]

[[!redirects unary product]]
[[!redirects unary products]] 

[[!redirects unary product type]]
[[!redirects unary product types]] 

[[!redirects copy induction]] 