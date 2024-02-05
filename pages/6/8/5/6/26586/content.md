
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
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

## Idea

In [[dependent type theory]], the **type theoretic axiom of choice** is a version of [[axiom of choice]] which does not use any [[bracket types]] in the theorem, as it uses the [[propositions as types]] interpretation of dependent type theory. Despite its name, the type theoretic axiom of choice is provable in dependent type theory from the [[inference rules]] of dependent product types, dependent sum types, and [[identity types]], and so really deserves to be called the **type theoretic principle of choice**. This is in contrast to what is referred to as the *[[propositional axiom of choice]]* or simply *[[axiom of choice]]* which does use [[bracket types]] via the [[propositions as subsingletons]] interpretation of dependent type theory and is just the usual [[axiom of choice]] expressed in dependent type theory. 

## Statement

The type theoretic axiom of choice is the statement that given types $A$ and $B$ and type family $x:A, y:B \vdash R(x, y)$, one can construct

$$\mathrm{ac}_R \coloneqq \lambda g.(\lambda x.\pi_1(g(x)), \lambda x.\pi_2(g(x))):\left(\prod_{x:A} \sum_{y:B} R(x, y)\right) \to \left(\sum_{f:A \to B} \prod_{x:A} R(x, f(x))\right)$$

The [[propositions as types]] interprets [[disjunction]] and [[existential quantification]] directly as the [[sum type]] and [[dependent sum type]] respectively, and the statement of the axiom of choice comes out as simply the statement that products distribute over coproducts. (See [[distributivity pullback]] for a discussion in terms of the internal type theory of a locally cartesian closed category.) 

The equivalent form of the axiom of choice involving cartesian products of inhabited types then becomes in type theory the statement that "any [[dependent product]] of any [[family]] of [[pointed types]] is [[pointed]]". and is just the [[identity function]] on the dependent product type. 

## Related concepts

* [[axiom of choice]]

* [[propositional axiom of choice]]

## References

The type theoretic axiom of choice is found in:

* {#HoTTBook} [[Univalent Foundations Project]], section 1.6, of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

[[!redirects type-theoretic axiom of choice]]
[[!redirects type theoretic axiom of choice]]

[[!redirects type-theoretic principle of choice]]
[[!redirects type theoretic principle of choice]]