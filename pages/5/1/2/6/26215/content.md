
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[type theory]], there are many ways to represent the notion of conversion of [[terms]] from one to another in the syntax. Usually, this is represented by untyped or typed [[judgmental equality]] as a [[judgment]] $a \equiv b$ or $a \equiv b:A$ respectively. **Explicit conversion** is the representation of conversion as [[terms]] of a [[type]] $p:a \equiv b$. 

In [[objective type theory]] and other dependent type theories which don't have a judgmental equality as a judgment, explicit conversion is used for [[definitions]] and for [[beta-conversion]] and [[eta-conversion]], and is represented by [[identifications]] $p:a =_A b$ for [[elements]] and by [[equivalence of types|equivalences]] $e:A \simeq B$ for [[types]]. If the weak type theory has [[dependent type theory with type variables|type variables]] and [[identity type#IdentityTypesbetweenTypes|identity types between types]] $A = B$, one can use [[identifications]] $p:A = B$ instead of equivalences $e:A \simeq B$ for representing conversions between types. 

## Related concepts

* [[judgmental equality]]

* [[identity type]]

* [[dependent type theory with explicit conversions]]

## References

* [[Floris van Doorn]], [[Herman Geuvers]], and [[Freek Wiedijk]], *Explicit convertibility proofs in pure type systems*. Proceedings of the Eighth ACM SIGPLAN international workshop on Logical frameworks & meta-languages: theory & practice, ACM. 2013, pp. 25–36 ([pdf](https://www.cs.ru.nl/~herman/PUBS/ExplicitPTS.pdf))

* [[Theo Winterhalter]], *Formalisation and Meta-Theory of Type Theory* ([github](https://github.com/TheoWinterhalter/phd-thesis/releases/tag/v1.2.1))

The use of the [[identity type]] for [[explicit conversions]] in [[objective type theory]] is discussed in:

* {#BB21} [[Benno van den Berg]], [[Martijn den Besten]], *Quadratic type checking for objective type theory* ([arXiv:2102.00905](https://arxiv.org/abs/2102.00905))

[[!redirects explicit conversion]]
[[!redirects explicit conversions]]