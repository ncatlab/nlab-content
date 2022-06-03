+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

When attempting to define [[coinductive types]], there is an obstacle to the complete [[dualization]] of the usual rules for [[inductive types]] in [[dependent type theory]], including dualizing the [[induction principle]] to a “coinduction principle”. For this some form of “codependent types” would be needed. In the context of [[homotopy type theory]], Ahrens, Capriotti, and Spadotti write:

> The universal property defining (internal) coinductive types in HoTT is dual to the one defining (internal) inductive types.  One might hence assume that their existence is equivalent to a set of type-theoretic rules dual (in a suitable sense) to those given for external W-types...  However, the rules for external W-types cannot be dualized in a naïve way, due to some asymmetry of HoTT related to dependent types as maps into a “type of types” (a universe) ([ACS15](#ACS15))

Codependent type theory is a hypothetical type theory where one should be able to define codependent types, and coinductive types with a coinduction principle. 
 
## Related concepts

* [[coinductive type]]

* [[locally cocartesian coclosed category]]

## References

* {#ACS15} Benedikt Ahrens, Paolo Capriotti, Régis Spadotti, _Non-wellfounded trees in Homotopy Type Theory_, ([arXiv:1504.02949](https://arxiv.org/abs/1504.02949))