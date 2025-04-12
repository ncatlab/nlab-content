+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition ##

In [[dependent type theory]], given a [[Russell universe]] $U$, a [[type]] $A$ is **purely essentially $U$-small** if the universe has an element $B:U$ and an equivalence $p:A \simeq B$. 

A [[type]] $A$ is **merely essentially $U$-small** if [[existential quantifier|there merely exists]] an element $B:U$ such that $A \simeq B$: 
$$\mathrm{isEssentiallySmall}_U(A) \coloneqq \exists B:U.A \simeq B$$

Similarly, given a [[Tarski universe]] $(U, T)$, a [[type]] $A$ is **purely essentially $U$-small** if the universe has an element $B:U$ and an equivalence $p:A \simeq T(B)$.

A [[type]] $A$ is **merely essentially $U$-small** if [[existential quantifier|there merely exists]] an element $B:U$ such that $A \simeq T(B)$: 
$$\mathrm{isEssentiallySmall}_U(A) \coloneqq \exists B:U.A \simeq T(B)$$

More generally, given a type $A$ and a type family $x:A \vdash B(x)$, a type $C$ is **purely essentially $(A, B)$-small** if one can construct an element $z:A$ and an equivalene $p:C \simeq B(z)$. 

A [[type]] $C$ is **merely essentially $(A, B)$-small** if [[existential quantifier|there merely exists]] an element $z:C$ such that $C \simeq B(z)$: 
$$\mathrm{isEssentiallySmall}_{A, B(-)}(C) \coloneqq \exists z:A.C \simeq B(z)$$

## Examples

For a single universe $U$, [[propositional resizing]] states that the type of all [[h-propositions]] in a universe is essentially $U$-small. 

## Making all essentially small types small

Given a [[Russell universe]] $U$, one could make all essentially $U$-small types actually small types by the following [[inference rules]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \mathrm{witnSmall}_A:\exists B:U.A \simeq B}{\Gamma \vdash A:U}$$

## See also ##

* [[type universe]]
* [[locally small type]]
* [[propositional resizing]]
* [[type theoretic axiom of replacement]]

## References ##

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]]: Section 2.19 of: *[[Symmetry]]* (2021) $[$[pdf](https://unimath.github.io/SymmetryBook/book.pdf)$]$

[[!redirects essentially small type]]
[[!redirects essentially small types]]

[[!redirects purely essentially small type]]
[[!redirects purely essentially small types]]

[[!redirects merely essentially small type]]
[[!redirects merely essentially small types]]