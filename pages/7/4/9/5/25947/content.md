+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Definition

### Judgmental congruence rules

In [[dependent type theory]] with [[judgmental equality]], a **(judgmental) congruence rule** is an [[inference rule]] which states that [[judgmental equality]] is respected. 

For example, there is a congruence rule for element conversion, which states that given judgmentally equal types $A$ and $B$ and judgmentally equal elements $a$ and $b$ of $A$, $a$ and $b$ are judgmentally equal elements of $B$:

$$\frac{\Gamma \vdash A \equiv B \; \mathrm{type} \quad \Gamma \vdash a \equiv b:A}{\Gamma \vdash a \equiv b:B}$$

There are many other different judgmental congruence rules, one for every term or type that is formed in the [[natural deduction]] [[inference rules]] in the type theory:

#### Congruence rules for dependent function types

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \equiv B'(x) \; \mathrm{type}
\end{array}
}{\Gamma \vdash \prod_{x:A} B(x) \equiv \prod_{x:A'} B'(x)\; \mathrm{type}}$$

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x) \quad \Gamma, x:A \vdash b'(x):B(x) \\ 
	\Gamma, x:A \vdash b(x) \equiv b'(x):B(x)
\end{array}
}{\Gamma \vdash \lambda x:A.b(x) \equiv \lambda x:A.b'(x):\prod_{x:A}.B(x)}$$

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash f:\prod_{x:A} B(x) \quad f':\prod_{x:A} B(x) \\
	\Gamma \vdash f \equiv f':\prod_{x:A} B(x)
\end{array}
}{\Gamma, x:A \vdash f(x) \equiv f'(x):B(x)}$$

If the dependent function type is weak, then there are also the following congruence rules for the computation and uniqueness rules of dependent function types:

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x) \quad \Gamma, x:A \vdash b'(x):B(x) \\ 
	\Gamma, x:A \vdash b(x) \equiv b'(x):B(x)
\end{array}
}{\Gamma \vdash \beta_{\prod}^{A, B} x:A.b(x) \equiv \beta_{\prod}^{A, B} x:A.b'(x):\prod_{x:A} b(x) =_{B(x)} (\lambda x:A.b(x))(x)}$$

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash B'(x) \; \mathrm{type} \\
	\Gamma, x:A \vdash B(x) \equiv B'(x) \; \mathrm{type}
\end{array}
}{\Gamma \vdash \eta_{\prod}^{A, B} \equiv \eta_{\prod}^{A, B'}:\prod_{f:\prod_{x:A} B(x)} f =_{\prod_{x:A} B(x)} \lambda x:A.f(x)}$$

#### Congruence rules for dependent pair types:

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \equiv B'(x) \; \mathrm{type}
\end{array}
}{\Gamma \vdash \sum_{x:A} B(x) \equiv \sum_{x:A'} B'(x)\; \mathrm{type}}$$

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \equiv B'(x) \; \mathrm{type}
\end{array}
}{\Gamma, x:A, y:B(x) \vdash \mathrm{pair}_{\sum}^{A, B} \equiv \mathrm{pair}_{\sum}^{A', B'}:\sum_{x:A} B(x)}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \equiv B'(x) \; \mathrm{type} \quad \Gamma, z:\sum_{x:A} B(x) \vdash C(z) \equiv C'(z) \; \mathrm{type}
\end{array}
}{\Gamma \vdash \mathrm{ind}_{\sum}^{A, B, C} \equiv \mathrm{ind}_{\sum}^{A', B', C'}:\prod_{g:\prod_{x:A} \prod_{y:B(x)} C(\mathrm{pair}_{\sum}^{A, B}(x, y))} \prod_{z:\sum_{x:A} B(x)} C(z)}$$

If the dependent pair type is weak, then there is also the following congruence rule for the computation rule of dependent pair types:

$$\frac{
\begin{array}{c}
\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \equiv B'(x) \; \mathrm{type} \quad \Gamma, z:\sum_{x:A} B(x) \vdash C(z) \equiv C'(z) \; \mathrm{type}
\end{array}
}{\Gamma \vdash \beta_{\sum}^{A, B, C} \equiv \beta_{\sum}^{A', B', C'}:\prod_{g:\prod_{x:A} \prod_{y:B(x)} C(\mathrm{pair}_{\sum}^{A, B}(x, y))} \prod_{x:A} \prod_{y:B(x)} \mathrm{ind}_{\sum}^{A, B, C}(g, \mathrm{pair}_{\sum}^{A, B}(x, y)) =_{C(\mathrm{pair}_{\sum}^{A, B}(x, y))} g(x, y)}$$

#### Congruence rules for identity types:

$$\frac{\Gamma \vdash A \equiv A' \; \mathrm{type}}{\Gamma, x:A, y:A \vdash x =_A y \equiv x =_{A'} y}$$

$$\frac{\Gamma \vdash A \equiv A' \; \mathrm{type}}{\Gamma \vdash \mathrm{refl}_A \equiv \mathrm{refl}_{A'}:\prod_{x:A} x =_A x}$$

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A, y:A, p:x =_A y \vdash C(x, y, p) \equiv C'(x, y, p) \; \mathrm{type}
\end{array}
}{\Gamma \vdash \mathrm{ind}_{=}^{A, C} \equiv \mathrm{ind}_{=}^{A', C'}:\prod_{t:\prod_{x:A} C(x, x, \mathrm{refl}_A(x))} \prod_{x:A} \prod_{y:A} \prod_{p:x =_A y} C(x, y, p)}$$

If the identity types are weak, then there is also the following congruence rule for the computation rule of identity types:

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A, y:A, p:x =_A y \vdash C(x, y, p) \equiv C'(x, y, p) \; \mathrm{type}
\end{array}
}{\Gamma \vdash \beta_{ \mathrm{ind}_=}^{A, C} \equiv \beta_{\mathrm{ind}_=}^{A', C'}:\prod_{t:\prod_{x:A} C(x, x, \mathrm{refl}_A(x))} \prod_{x:A} \mathrm{ind}_{=}^{A, C}(t, x, x, \mathrm{refl}_A(x)) =_{C(x, x, \mathrm{refl}_A(x))} t(x)}$$

#### Congruence rules for the empty type:

$$\frac{\Gamma, x:\emptyset \vdash C(x) \equiv C'(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{ind}_\emptyset^C \equiv \mathrm{ind}_\emptyset^{C'}:\prod_{x:\emptyset} C(x) \; \mathrm{type}}$$

#### Congruence rules for the type of booleans:

$$\frac{\Gamma, x:\mathbb{2} \vdash C(x) \equiv C'(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{ind}_\mathbb{2}^C \equiv \mathrm{ind}_\mathbb{2}^{C'}:\prod_{a:C(0)} \prod_{b:C(1)} \prod_{x:\mathbb{2}} C(x)}$$

If the type of booleans is weak, then there are also the following congruence rules for the computation rules of the type of booleans:

$$\frac{\Gamma, x:\mathbb{2} \vdash C(x) \equiv C'(x) \; \mathrm{type}}{\Gamma \vdash \beta_\mathbb{2}^{0, C} \equiv \beta_\mathbb{2}^{0, C'}:\prod_{a:C(0)} \prod_{b:C(1)} \mathrm{ind}_\mathbb{2}^C(a, b, 0) =_{C(0)} a}$$

$$\frac{\Gamma, x:\mathbb{2} \vdash C(x) \equiv C'(x) \; \mathrm{type}}{\Gamma \vdash \beta_\mathbb{2}^{1, C} \equiv \beta_\mathbb{2}^{1, C'}:\prod_{a:C(0)} \prod_{b:C(1)} \mathrm{ind}_\mathbb{2}^C(a, b, 1) =_{C(1)} b}$$

#### Congruence rules for the natural numbers type:

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \equiv C'(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^C \equiv \mathrm{ind}_\mathbb{N}^{C'}:\prod_{c_0:C(0)} \prod_{c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x))} \prod_{x:\mathbb{N} C(x)}}$$

If the natural numbers type is weak, then there are also the following congruence rules for the computation rules of the natural numbers type:

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \equiv C'(x) \; \mathrm{type}}{\Gamma \vdash \beta_\mathbb{N}^{0, C} \equiv \beta_\mathbb{N}^{0, C'}:\prod_{c_0:C(0)} \prod_{c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x))} \mathrm{ind}_\mathbb{N}^C(c_0, c_s, 0) =_{C(0)} c_0}$$

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \equiv C'(x) \; \mathrm{type}}{\Gamma \vdash \beta_\mathbb{N}^{s, C} \equiv \beta_\mathbb{N}^{s, C'}:\prod_{c_0:C(0)} \prod_{c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x))} \prod_{x:\mathbb{N}} \mathrm{ind}_\mathbb{N}^C(c_0, c_s, s(x)) =_{C(s(x))} c_s(x)(\mathrm{ind}_\mathbb{N}^C(c_0, c_s, x))}$$

#### Congruence rules for axioms

Similarly, we have congruence rules for every [[axiom]] in the dependent type theory, such as 

* congruence rule for [[function extensionality]]:

$$\frac{\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \equiv B'(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{funext}_{A, B} \equiv \mathrm{funext}_{A', B'}:\prod_{f;\prod_{x:A} B(x)} \prod_{g:\prod_{x:A} B(x)} (f =_{\prod_{x:A} B(x)} g) \simeq \prod_{x:A} f(x) =_{B(x)} g(x)}$$

* congruence rule for the [[axiom of choice]]:

$$\frac{\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \equiv B'(x) \; \mathrm{type} \quad \Gamma, x:A, y:B(x) \vdash C(x, y) \equiv C'(x, y) \; \mathrm{type}}{\Gamma \vdash \mathrm{choice}_{A, B, C} \equiv \mathrm{choice}_{A', B', C'}:\left(\mathrm{isSet}(A) \times \prod_{x:A} \mathrm{isSet}(B(x))\right) \to \forall x:A.\exists y:B(x).C(x, y) \to \exists g:\prod_{x:A} B(x).\forall x:A.C(x, g(x))}$$

### Typal congruence rules

In [[dependent type theory]], a **typal congruence rule** is an derivable [[inference rule]] which states that given [[identifications]] of the component terms and [[equivalences]] of the component types in the hypotheses of the [[natural deduction]] [[inference rules]], one could derive the corresponding identification and equivalences of the derived terms and types in the conclusion of the inference rules. 

For example, the typal congruence rule for element conversion states that given equivalent types $A$ and $B$ with equivalence $e:A \simeq B$ and typally equal elements $a$ and $b$ of $A$ with identification $p:a =_A b$, $e(a)$ and $e(b)$ are typally elements of $B$, and is given by [[function application to identifications|application]] of $e$ to $p$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b}{\Gamma \vdash \mathrm{ap}_e(a, b, p):e(a) =_B e(b)}$$

There are many other different typal congruence rules which are derivable, one for every term or type that is formed in the [[natural deduction]] [[inference rules]] in the type theory:

#### Congruence rules for dependent function types

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash A' \; \mathrm{type} \quad \Gamma \vdash e_A:A \simeq A' \\
        \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash B'(x) \; \mathrm{type} \quad \Gamma, x:A \vdash e_B(x):B(x) \simeq B'(x)
\end{array}
}{\Gamma \vdash \mathrm{congform}_{\prod_{x:A} B(x)}:\left(\prod_{x:A} B(x)\right) \simeq \left(\prod_{x:A'} B'(x)\right)}$$

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x) \quad \Gamma, x:A \vdash b'(x):B(x) \\ 
	\Gamma, x:A \vdash p(x):b(x) =_{B(x)} b'(x)
\end{array}
}{\Gamma \vdash \mathrm{congIntro}_{\prod_{x:A} B(x)}^{x:A.b(x), x:A.b'(x), x:A.p(x)}:\lambda x:A.b(x) =_{\prod_{x:A}.B(x)} \lambda x:A.b'(x)}$$

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash f:\prod_{x:A} B(x) \quad f':\prod_{x:A} B(x) \\
	\Gamma \vdash p:f =_{\prod_{x:A} B(x)} f'
\end{array}
}{\Gamma, x:A \vdash \mathrm{congElim}_{\prod_{x:A} B(x)}(p, x):f(x) =_{B(x)} f'(x)}$$

#### Congruence rules for identity types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash A' \; \mathrm{type} \quad \Gamma \vdash e_A:A \simeq A'}{\Gamma, x:A, y:A \vdash \mathrm{congform}_{=_A}(e_A, x, y):(x =_A y) \simeq (e(x) =_{A'} e(y))}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash A' \; \mathrm{type} \quad \Gamma \vdash e_A:A \simeq A'}{\Gamma \vdash \mathrm{congIntro}_{=_A}(e_A):\mathrm{congForm}_{\prod_{x:A} x =_A x}(\mathrm{refl}_A) =_{\prod_{x:A'} x =_A x} \mathrm{refl}_{A'}}$$

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \; \mathrm{type} \quad \Gamma, z:\sum_{x:A} \sum_{y:A} x =_A y \vdash C(z) \; \mathrm{type} \quad \Gamma, z:\sum_{x:A} \sum_{y:A} x =_A y \vdash C'(z) \; \mathrm{type} \\
	\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash e_C:\prod_{z:\sum_{x:A} \sum_{y:A} x =_A y} C(z) \simeq C'(z) \\
\end{array}
}{\Gamma \vdash \mathrm{congElim}_{=_A}(e_C):\mathrm{congForm}_{\prod_{t:\prod_{x:A} C'(\Delta_A(x))} \prod_{z:\sum_{x:A} \sum_{y:A} x =_A y} C'(z)}(\mathrm{congForm}_{\prod_{z:\sum_{x:A} \sum_{y:A} x =_A y} C'(z)}(\mathrm{ind}_{=}^{A, C})) =_{\prod_{t:\prod_{x:A} C'(\Delta_A(x))} \prod_{z:\sum_{x:A} \sum_{y:A} x =_A y} C'(z)} \mathrm{ind}_{=}^{A, C'}}$$

where $\Delta_A(x) \coloneqq (x, x, \mathrm{refl}_A(x)):\sum_{x:A} \sum_{y:A} x =_A y$ is the [[diagonal function]] of $A$. 

## See also

* [[inference rule]]

* [[structural rule]]

## References

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

[[!redirects congruence rule]]
[[!redirects congruence rules]]

[[!redirects judgmental congruence rule]]
[[!redirects judgmental congruence rules]]

[[!redirects typal congruence rule]]
[[!redirects typal congruence rules]]