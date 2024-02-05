
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


## Idea

The **propositional axiom of choice** is simply another name for the usual [[axiom of choice]] in [[dependent type theory]], to distinguish with the untruncated version of the axiom of choice called the *[[type theoretic axiom of choice]]*. 

It corresponds to the *[[internal axiom of choice]]* in [[categorical semantics]] and in [[set theory]]. 

## Statement

The propositional axiom of choice is the statement that given types $A$ and $B$ and type family $x:A, y:B \vdash R(x, y)$, one can construct

$$\mathrm{ac}_R:\left(\prod_{x:A} \exists y:B.R(x, y)\right) \to \left(\exists f:A \to B.\prod_{x:A} R(x, f(x))\right)$$

The [[propositions as subsingletons]] interprets [[disjunction]] and [[existential quantification]] as the [[bracket type]] of the [[sum type]] and [[dependent sum type]] respectively, and leads to the usual statement of the axiom of choice translated to [[dependent type theory]]. 

The equivalent form of the axiom of choice involving a unary type family $x:A \vdash P(x)$ instead of a binary type family $x:A, y:B \vdash R(x, y)$ states that one can construct

$$\mathrm{ac}_R:\left(\prod_{x:A} [P(x)]\right) \to \left[\prod_{x:A} P(x)\right]$$

This is the statement that any [[dependent product]] of any [[family]] of [[inhabited]] [[h-sets]] is [[inhabited]]. 

## Related concepts

* [[propositional truncation]]

* [[inhabited set]], [[inhabited object]]

* [[dominance]]

* [[type theoretic axiom of choice]]

* [[internal axiom of choice]]. 

## References

* [[Martin Hyland]], p. 1 of: _Variations on realizability: realizing the propositional axiom of choice_,  Mathematical Structures in Computer Science, Volume 12, Issue 3, June 2002, pp. 295 - 317  ([doi:10.1017/S0960129502003651](https://doi.org/10.1017/S0960129502003651), [pdf](https://www.dpmms.cam.ac.uk/~martin/Research/Publications/2002/vor02.pdf))

[[!redirects PAC]]
