
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Set theory
+-- {: .hide}
[[!include set theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

### In set theory

Let $\mathbb{N}$ be the set of natural numbers, let $n:\mathbb{N}$ be an arbitrary natural number, let $\mathrm{Fin}(n)$ be the [[finite set]] with $n$ elements, and let $A$ be an arbitrary set. Then **$n$-tuple extensionality** states that for every [[tuple]] $a:\mathrm{Fin}(n) \to A$ and $b:\mathrm{Fin}(n) \to A$, $a =_{\mathrm{Fin}(n) \to A} b$ if and only if $a(i) =_A b(i)$ for all elements $i \in \mathrm{Fin}(n)$. 

### In dependent type theory

In [[dependent type theory]], **$n$-tuple extensionality** states that given two $n$-tuples $a:\mathrm{Fin}(n) \to A$ and $b:\mathrm{Fin}(n) \to A$ there is an [[equivalence of types]] between the [[identity type]] $a =_{\mathrm{Fin}(n) \to A} b$ and the dependent tuple type $(i:\mathrm{Fin}(n)) \to (a(i) =_{A} b(i))$:
$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A \; \mathrm{type}}{\Gamma,a:\mathrm{Fin}(n) \to A, b:\mathrm{Fin}(n) \to A \vdash \mathrm{tupext}(a, b):(a =_{\mathrm{Fin}(n) \to A} b) \simeq (i:\mathrm{Fin}(n)) \to (a(i) =_{A} b(i))}$$

There is also a version of $n$-tuple extensionality for [[dependent tuple types]] called **dependent $n$-tuple extensionality**, which states that given two dependent $n$-tuples $a:(i:\mathrm{Fin}(n)) \to A(i)$ and $b:(i:\mathrm{Fin}(n)) \to A(i)$ there is an [[equivalence of types]] between the [[identity type]] $a =_{(i:\mathrm{Fin}(n)) \to A(i)} b$ and the dependent tuple type $(i:\mathrm{Fin}(n)) \to (a(i) =_{A(i)} b(i))$:
$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma, i:\mathrm{Fin}(n) \vdash A(i) \; \mathrm{type}}{\Gamma,a:(i:\mathrm{Fin}(n)) \to A(i), b:(i:\mathrm{Fin}(n)) \to A(i) \vdash \mathrm{dtupext}(a, b):(a =_{(i:\mathrm{Fin}(n)) \to A(i)} b) \simeq (i:\mathrm{Fin}(n)) \to (a(i) =_{A(i)} b(i))}$$

## Properties

Tuple extensionality is always true in [[set theory]] and [[dependent type theory]], for the same reason that [[product extensionality]] is true. 

Indeed, one could express tuple extensionality as two separate cases representing nullary tuples and binary tuples:

* Every two elements in a [[singleton]] are equal to each other

* [[product extensionality]]: Given two [[ordered pairs]] in a [[product set]], they are equal if and only if the left product projections are equal to each other and the right product projections are equal to each other. 

In dependent type theory, this becomes:

* Every [[identity type]] of two elements in a [[contractible type]] is a contractible type.

* [[product extensionality]]: Given two [[ordered pairs]] in a [[product set]], the identity type between the two ordered pairs is equivalent to the product type of the identity type of the left product projections and the identity type of the right product projections. 

## See also

* [[extensionality]]
* [[product extensionality]]
* [[sequence extensionality]]
* [[function extensionality]]

[[!redirects tuple extensionality]]
[[!redirects n-tuple extensionality]]

[[!redirects dependent tuple extensionality]]
[[!redirects dependent n-tuple extensionality]]