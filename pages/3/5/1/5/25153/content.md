\tableofcontents

## Idea

In [[dependent type theory]], a [[sequence]] in a type $A$ is a family of elements $n:\mathbb{N} \vdash x(n):A$, or equivalently, a function $x:\mathbb{N} \to A$ with domain of the natural numbers. A dependent sequence is like a sequence but in which we allow $A$ to depend on the natural numbers. 

## Definition

Given a family of types indexed by the natural numbers $n:\mathbb{N} \vdash A(n)$, a **dependent sequence** can be defined as 

* a family of elements $n:\mathbb{N} \vdash x(n):A(n)$

* a [[dependent sequential net]] $(x:\mathbb{N} \vdash P(x); x:\mathbb{N}, p:P(x) \vdash f(x, p):B(x), x:\mathbb{N} \vdash \mathrm{isInhab}(x):\left[P(x)\right])$ for which the dependent type $P(x)$ is a [[contractible type]] for all natural numbers $x:\mathbb{N}$

* a [[dependent correspondence]] $x:\mathbb{N}, y:B(x) \vdash R(x, y)$ for which the dependent type $\sum_{y:B(x)} R(x, y)$ is a [[contractible type]] for all natural numbers $x:\mathbb{N}$. 

* an element of the [[dependent function type]] $x:(n:\mathbb{N}) \to A(n)$

## Dependent sequence types

A dependent sequence type is simply the [[dependent function type]] $(n:\mathbb{N}) \to A(n)$, and thus comes with the following rules:

Formation rules for dependent sequence types:
$$\frac{\Gamma, n:\mathbb{N} \vdash A(n) \; \mathrm{type}}{\Gamma \vdash (n:\mathbb{N}) \to A(n) \; \mathrm{type}}$$

Introduction rules for dependent sequence types:
$$\frac{\Gamma, n:\mathbb{N} \vdash A(n) \; \mathrm{type} \quad \Gamma, n:\mathbb{N} \vdash a(n):A(n)}{\Gamma \vdash \lambda(n:\mathbb{N}).a(n):(n:\mathbb{N}) \to A(n)}$$

Elimination rules for dependent sequence types:
$$\frac{\Gamma, n:\mathbb{N} \vdash A(n) \; \mathrm{type}}{\Gamma, a:(n:\mathbb{N}) \to A(n), n:\mathbb{N} \vdash \mathrm{ev}(a, n):A(n)}$$

Computation rules for dependent sequence types:
$$\frac{\Gamma, n:\mathbb{N} \vdash A(n) \; \mathrm{type} \quad \Gamma, n:\mathbb{N} \vdash a(n):A(n)}{\Gamma, m:\mathbb{N} \vdash \beta_\Pi(m):\mathrm{ev}(\lambda(n:\mathbb{N}).a(n), m) =_{A(m)} a(m)}$$

Uniqueness rules for dependent sequence types:
$$\frac{\Gamma, n:\mathbb{N} \vdash A(n) \; \mathrm{type}}{\Gamma, a:(n:\mathbb{N}) \to A(n) \vdash \eta_\Pi(a):a =_{(n:\mathbb{N}) \to A(n)} \lambda(n:\mathbb{N}).a(n)}$$

Dependent sequence types also have their own extensionality principle, called [[dependent sequence extensionality]]. This states that given two dependent sequences $a:(n:\mathbb{N}) \to A(n)$ and $b:(n:\mathbb{N}) \to A(n)$ there is an [[equivalence of types]] between the [[identity type]] $a =_{(n:\mathbb{N}) \to A(n)} b$ and the dependent sequence type $(n:\mathbb{N}) \to (a(n) =_{A(n)} b(n))$:
$$\frac{\Gamma, n:\mathbb{N} \vdash A(n) \; \mathrm{type}}{\Gamma,a:(n:\mathbb{N}) \to A(n), b:(n:\mathbb{N}) \to A(n) \vdash \mathrm{dseqext}(a, b):(a =_{(n:\mathbb{N}) \to A(n)} b) \simeq (n:\mathbb{N}) \to (a(n) =_{A(n)} b(n))}$$

Dependent sequence types are used in [[strongly predicative mathematics]], where one does not have [[dependent function types]], to construct the [[natural numbers type]], as dependent sequence types are used in the [[elimination rules]], [[computation rules]], and [[uniqueness rules]] of the natural numbers type:

Elimination rules for the natural numbers type:

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x)) \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^C(c_0, c_s, n):C(n)}$$

Computation rules for the natural numbers type:

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x))}{\Gamma \vdash \beta_\mathbb{N}^0(c_0, c_s):\mathrm{Id}_{C(0)}\mathrm{ind}_\mathbb{N}^C(c_0, c_s, 0), c_0)}$$

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x)) \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \beta_\mathbb{N}^s(c_0, c_s, n):\mathrm{Id}_{C(s(n))}(\mathrm{ind}_\mathbb{N}^C(c_0, c_s, s(n)), c_s(n)(\mathrm{ind}_\mathbb{N}^C(c_0, c_s, n)))}$$

Uniqueness rules for the natural numbers type:

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c:\prod_{x:\mathbb{N}} C(x) \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \eta_\mathbb{N}(c, n):\mathrm{Id}_{C(n)}(\mathrm{ind}_\mathbb{N}^C(c(0), \lambda x:\mathbb{N}.c(s(x)), n), c(n))}$$ 

It is also used in defining the [[axiom of countable choice]] in [[dependent type theory]]:

$$\frac{\Gamma, n:\mathbb{N} \vdash A(n) \; \mathrm{type}}{\Gamma, a:(n:\mathbb{N}) \to \left[A(n)\right] \vdash \mathrm{countablechoice}(a):\left[(n:\mathbb{N}) \to A(n)\right]}$$

## See also

* [[tuple]], [[sequence]], [[function]]

* [[dependent tuple]], **dependent sequence**, [[dependent function]]

* [[countable choice]]

* [[ascending chain condition]], [[Noetherian ring]], [[Noetherian module]], [[Noetherian bimodule]]

* [[descending chain condition]], [[Artinian ring]], [[Artinian module]], [[Artinian bimodule]]

* [[sequential spectrum]], [[sequential spectrum type]]

[[!redirects dependent sequence]]
[[!redirects dependent sequences]]

[[!redirects dependent sequence type]]
[[!redirects dependent sequence types]]