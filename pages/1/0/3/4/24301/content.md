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

Assuming [[function extensionality]], the axiom of replacement holds for any [[univalent universe]] $U$ that is closed under [[pushout types]] and contains a [[natural numbers type]] ([Rijke 17, Theorem 4.6](#Rijke17)).

## Set replacement

There is a variant of the axiom of replacement in [[dependent type theory]] called the **axiom of set replacement**, which restricts the type $B$ in the above statement of the axiom of replacement to be a [[set]]. 

Assuming [[propositional extensionality]] and [[function extensionality]], the axiom of set replacement is equivalent to the existence of [[quotient sets]] in the [[type universe]] $U$ ([De Jong and Escardó 23, Theorem 3.29](#DeJongEscardo23)) and is derivable from [[propositional resizing]] ([Rijke and Spitters 15, Lemma 3.28](#RijkeSpitters15)).


## Related concepts

* [[resizing axiom]]

* [[type universe]]

* [[essentially small type]]

* [[locally small type]]

* [[axiom of replacement]]

* [[quotient set]]

## References ##

* {#Rijke17} [[Egbert Rijke]], _The join construction_, 26 Jan 2017, ([arXiv:1701.07538](https://arxiv.org/abs/1701.07538))

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]], Section 2.19 in: _[[Symmetry]]_ (2021) $[$[pdf](https://unimath.github.io/SymmetryBook/book.pdf)$]$

* [[Egbert Rijke]], Section 18.1 of: _[[Introduction to Homotopy Type Theory]]_, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

* [[Evan Cavallo]], [[Thierry Coquand]], _Type-theoretic replacement and univalent completion: applications and interpretations_, 31st International Conference on Types for Proofs and Programs (TYPES 2025), Leibniz International Proceedings in Informatics (LIPIcs) **384** (2026) 10:1--10:27 &lbrack;[doi:10.4230/LIPIcs.TYPES.2025.10](https://doi.org/10.4230/LIPIcs.TYPES.2025.10)&rbrack;

Regarding set replacement:

* {#RijkeSpitters15} [[Egbert Rijke]], [[Bas Spitters]], Section 3.4 of: _Sets in homotopy type theory_, Mathematical Structures in Computer Science **25** Special Issue 5: From type theory and homotopy theory to Univalent Foundations of Mathematics (2015) 1172 - 1202 &lbrack;[arXiv:1305.3835](https://arxiv.org/abs/1305.3835), [doi:10.1017/S0960129514000553](https://doi.org/10.1017/S0960129514000553)&rbrack;

* {#DeJongEscardo23} [[Tom de Jong]], [[Martín Hötzel Escardó]], Section 3.4 of: _On Small Types in Univalent Foundations_, Logical Methods in Computer Science **19** 2 (2023) &lbrack;[arXiv:2111.00482](https://arxiv.org/abs/2111.00482), [doi:10.46298/lmcs-19(2:8)2023](https://doi.org/10.46298/lmcs-19%282:8%292023)&rbrack;

* [[Tom de Jong]], Section 2.11.4 of: _Domain Theory in Constructive and Predicative Univalent Foundations_, PhD thesis, University of Birmingham (2023) &lbrack;[url](https://etheses.bham.ac.uk/id/eprint/13401), [arXiv:2301.12405](https://arxiv.org/abs/2301.12405)&rbrack;

* [[Ayberk Tosun]], Section 2.15 of: _Constructive and Predicative Locale Theory in Univalent Foundations_, PhD thesis, University of Birmingham (2025) &lbrack;[url](http://etheses.bham.ac.uk/id/eprint/16416), [arXiv:2603.01308](https://arxiv.org/abs/2603.01308)&rbrack;

[[!redirects type-theoretic axiom of replacement]]

[[!redirects set replacement]]
[[!redirects axiom of set replacement]]
[[!redirects axioms of set replacement]]