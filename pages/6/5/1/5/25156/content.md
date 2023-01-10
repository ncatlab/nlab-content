\tableofcontents

## Idea

In [[dependent type theory]], given a natural number $n:\mathbb{N}$, an $n$-[[tuple]] in a type $A$ is a family of elements $i:\mathrm{Fin}(n) \vdash x(i):A$, or equivalently, a function $x:\mathrm{Fin}(n) \to A$ with domain of the [[finite set]] with $n$ elements. A dependent sequence is like a sequence but in which we allow $A$ to depend on the finite set. 

## Definition

Given a natural number $n:\mathbb{N}$ and a family of types indexed by the [[finite set]] with $n$ elements $i:\mathrm{Fin}(n) \vdash A(i)$, a **dependent $n$-tuple** can be defined as 

* a family of elements $i:\mathrm{Fin}(n) \vdash x(i):A(i)$

* an element of the [[dependent function type]] $x:(i:\mathrm{Fin}(n)) \to A(i)$

## Dependent n-tuple types

A dependent $n$-tuple type is simply the [[dependent function type]] $(i:\mathrm{Fin}(n)) \to A(i)$, and thus comes with the following rules:

Formation rules for dependent tuple types:
$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma, i:\mathrm{Fin}(n) \vdash A(i) \; \mathrm{type}}{\Gamma \vdash (i:\mathrm{Fin}(n)) \to A(i) \; \mathrm{type}}$$

Introduction rules for dependent tuple types:
$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma, i:\mathrm{Fin}(n) \vdash A(i) \; \mathrm{type} \quad \Gamma, i:\mathrm{Fin}(n) \vdash a(i):A(i)}{\Gamma \vdash \lambda(n:\mathbb{N}).a(n):(i:\mathrm{Fin}(n)) \to A(i)}$$

Elimination rules for dependent tuple types:
$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma, i:\mathrm{Fin}(n) \vdash A(i) \; \mathrm{type}}{\Gamma, a:(i:\mathrm{Fin}(n)) \to A(i), i:\mathrm{Fin}(n) \vdash \mathrm{ev}(a, j):A(j)}$$

Computation rules for dependent tuple types:
$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma, i:\mathrm{Fin}(n) \vdash A(i) \; \mathrm{type} \quad \Gamma, i:\mathrm{Fin}(n) \vdash a(i):A(i)}{\Gamma, j:\mathrm{Fin}(n) \vdash \beta_\Pi(j):\mathrm{ev}(\lambda(i:\mathrm{Fin}(n)).a(i), j) =_{A(j)} a(j)}$$

Uniqueness rules for dependent tuple types:
$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma, i:\mathrm{Fin}(n) \vdash A(i) \; \mathrm{type}}{\Gamma, a:(i:\mathrm{Fin}(n)) \to A(i) \vdash \eta_\Pi(a):a =_{(i:\mathrm{Fin}(n)) \to A(i)} \lambda(i:\mathrm{Fin}(n)).a(i)}$$

## Properties

Dependent $n$-tuple types also have their own extensionality principle, called **dependent $n$-tuple extensionality**. This states that given two dependent $n$-tuples $a:(i:\mathrm{Fin}(n)) \to A(i)$ and $b:(i:\mathrm{Fin}(n)) \to A(i)$ there is an [[equivalence of types]] between the [[identity type]] $a =_{(i:\mathrm{Fin}(n)) \to A(i)} b$ and the dependent tuple type $(i:\mathrm{Fin}(n)) \to (a(i) =_{A(i)} b(i))$:
$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma, i:\mathrm{Fin}(n) \vdash A(i) \; \mathrm{type}}{\Gamma,a:(i:\mathrm{Fin}(n)) \to A(i), b:(i:\mathrm{Fin}(n)) \to A(i) \vdash \mathrm{dtupext}(a, b):(a =_{(i:\mathrm{Fin}(n)) \to A(i)} b) \simeq (i:\mathrm{Fin}(n)) \to (a(i) =_{A(i)} b(i))}$$

Dependent $n$-tuple extensionality is provable in any dependent type theory with [[dependent sum types]] and [[identity types]]; it follows from the same principles as [[product extensionality]] does. 

Dependent tuple types are also used in defining [[finite choice]] in [[dependent type theory]]:

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma, i:\mathrm{Fin}(n) \vdash A(i) \; \mathrm{type}}{\Gamma, a:(i:\mathrm{Fin}(n)) \to \left[A(i)\right] \vdash \mathrm{finitechoice}(a):\left[(i:\mathrm{Fin}(n)) \to A(i)\right]}$$

Similarly to dependent tuple extensionality, finite choice is provable in dependent type theory. 

## See also

* [[tuple]], [[sequence]], [[function]]

* **dependent tuple**, [[dependent sequence]], [[dependent function]]

* [[finite choice]]

[[!redirects dependent tuple]]
[[!redirects dependent tuples]]
[[!redirects dependent n-tuple]]
[[!redirects dependent n-tuples]]

[[!redirects dependent tuple type]]
[[!redirects dependent tuple types]]
[[!redirects dependent n-tuple type]]
[[!redirects dependent n-tuple types]]