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

In [[dependent type theory]], the __axiom of replacement__ states that given a [[type universe]] $U$, for every [[essentially small type|essentially $U$-small]] type $A$, every [[locally small type|locally $U$-small]] type $B$, and every function $f:A \to B$, the [[image]] $\mathrm{im}(f)$ is essentially $U$-small. 

Equivalently, given types $A$ and $B$ and [[Tarski universe]] $(U, T)$, there is a function

$$\mathrm{axrepl}_U^{A, B}:\left(\sum_{C:U} T(C) \simeq A\right) \times \left(\sum_{R:B \times B \to U} \prod_{a:B} \prod_{b:B} T(R(a, b)) \simeq (a =_B b)\right) \to \left(\sum_{I:(A \to B) \to U} \prod_{f:A \to B} T(I(f)) \simeq \mathrm{im}(f)\right)$$

If the dependent type theory has [[type variables]] and [[impredicative polymorphism]], the axiom of replacement can be expressed as an actual [[axiom]] rather than an [[axiom schema]]:

$$\mathrm{axrepl}_U:\Pi A.\Pi B.\left(\sum_{C:U} T(C) \simeq A\right) \times \left(\sum_{R:B \times B \to U} \prod_{a:B} \prod_{b:B} T(R(a, b)) \simeq (a =_B b)\right) \to \left(\sum_{I:(A \to B) \to U} \prod_{f:A \to B} T(I(f)) \simeq \mathrm{im}(f)\right)$$

## See also ##

* [[type universe]]

* [[essentially small type]]

* [[locally small type]]

* [[axiom of replacement]]

## References ##

* [[Egbert Rijke]], *The join construction*, 26 Jan 2017, ([arXiv:1701.07538](https://arxiv.org/abs/1701.07538))

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]], Section 2.19 in: *[[Symmetry]]* (2021) $[$[pdf](https://unimath.github.io/SymmetryBook/book.pdf)$]$ 

[[!redirects type-theoretic axiom of replacement]]