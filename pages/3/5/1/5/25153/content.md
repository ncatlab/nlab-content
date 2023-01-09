\tableofcontents

## Idea

In [[dependent type theory]], a [[sequence]] in a type $A$ is a family of elements $n:\mathbb{N} \vdash x(n):A$, or equivalently, a function $x:\mathbb{N} \to A$ with domain of the natural numbers. A dependent sequence is like a sequence but in which we allow $A$ to depend on the natural numbers. 

## Definition

Given a family of types indexed by the natural numbers $n:\mathbb{N} \vdash A(x)$, a **dependent sequence** can be defined as 

* a family of elements $n:\mathbb{N} \vdash x(n):A(x)$

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

Dependent sequence types are used in [[strongly predicative mathematics]], where one does not have [[dependent function types]], to construct the [[real numbers]]. 

## See also

* [[sequence]]

* [[dependent function]]

* [[dependent choice]]

[[!redirects dependent sequence]]
[[!redirects dependent sequences]]

[[!redirects dependent sequence type]]
[[!redirects dependent sequence types]]