+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
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

\tableofcontents

## Definition 

In [[dependent type theory]], the __axiom of replacement__ states that given a [[type universe]] $U$, for every [[essentially small type|essentially $U$-small]] type $A$, every [[locally small type|locally $U$-small]] type $B$, and every function $f:A \to B$, the [[image]] $\mathrm{im}(f)$ is essentially $U$-small. 

Equivalently, given types $A$ and $B$ and [[Tarski universe]] $(U, T)$, there is a function

$$\mathrm{axrepl}_U^{A, B}:\left(\sum_{C:U} T(C) \simeq A\right) \times \left(\sum_{R:B \times B \to U} \prod_{a:B} \prod_{b:B} T(R(a, b)) \simeq (a =_B b)\right) \to \left(\sum_{I:(A \to B) \to U} \prod_{f:A \to B} T(I(f)) \simeq \mathrm{im}(f)\right)$$

If the dependent type theory has [[type variables]] and [[impredicative polymorphism]], the axiom of replacement can be expressed as an actual [[axiom]] rather than an [[axiom schema]]:

$$\mathrm{axrepl}_U:\Pi A.\Pi B.\left(\sum_{C:U} T(C) \simeq A\right) \times \left(\sum_{R:B \times B \to U} \prod_{a:B} \prod_{b:B} T(R(a, b)) \simeq (a =_B b)\right) \to \left(\sum_{I:(A \to B) \to U} \prod_{f:A \to B} T(I(f)) \simeq \mathrm{im}(f)\right)$$

## Set replacement

There is a variant of the axiom of replacement in [[dependent type theory]] called the **axiom of set replacement**, which restricts the type $B$ in the above statement of the axiom of replacement to be a [[set]]. The axiom of set replacement is equivalent to the existence of [[quotient sets]] in the [[type universe]] $U$. 

## Related concepts

* [[resizing axiom]]

* [[type universe]]

* [[essentially small type]]

* [[locally small type]]

* [[axiom of replacement]]

* [[quotient set]]

## References ##

* [[Egbert Rijke]], *The join construction*, 26 Jan 2017, ([arXiv:1701.07538](https://arxiv.org/abs/1701.07538))

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]], Section 2.19 in: *[[Symmetry]]* (2021) $[$[pdf](https://unimath.github.io/SymmetryBook/book.pdf)$]$ 

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

* [[Ayberk Tosun]], *Constructive and Predicative Locale Theory in Univalent Foundations* ([arXiv:2603.01308](https://arxiv.org/abs/2603.01308))

[[!redirects type-theoretic axiom of replacement]]

[[!redirects set replacement]]
[[!redirects axiom of set replacement]]
[[!redirects axioms of set replacement]]