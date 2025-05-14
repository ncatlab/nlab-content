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

The notion of _coinductive types_ is [[duality|dual]] to that of _[[inductive types]]_.

## Examples

Examples of coinductive types include:

* streams (infinite sequences);
* [[trees]] with infinite branches;
* [[conatural numbers]].

## Properties

### Categorical semantics

Where the [[categorical semantics]] of an [[inductive type]] is an [[initial algebra for an endofunctor]], the semantics of a coinductive type is a [[terminal coalgebra of an endofunctor]].

### Coinductive type formation in homotopy type theory

There is an obstacle to the complete [[dualization]] of the usual rules for [[inductive types]] in [[homotopy type theory]], including dualizing the [[induction principle]] to a “coinduction principle”. For this some form of “codependent types” would be needed.

> The universal property defining (internal) coinductive types in HoTT is dual to the one defining (internal) inductive types.  One might hence assume that their existence is equivalent to a set of type-theoretic rules dual (in a suitable sense) to those given for external W-types...  However, the rules for external W-types cannot be dualized in a naïve way, due to some asymmetry of HoTT related to dependent types as maps into a “type of types” (a universe) ([ACS15](#ACS15))

However, it is possible instead to dualize the alternative characterization of inductive types as [[initial algebra for an endofunctor|initial algebras]] for a notion of coinductive types as [[terminal coalgebra of an endofunctor|terminal coalgebras]], and that can be formulated (and often constructed) in ordinary HoTT. In ([ACS15](#ACS15)) the authors proceed to construct coinductive types from indexed inductive types.
 
## Related concepts

* [[coinduction]], [[corecursion]]

* [[coinductive definition]]

* [[inductive type]]

* [[higher coinductive type]]

* [[displayed coinductive type]]

* [[codependent type theory]]

[[!redirects coinductive types]]
[[!redirects codata]]

## References

* {#ACS15} [[Benedikt Ahrens]], [[Paolo Capriotti]], [[Régis Spadotti]], *Non-wellfounded trees in Homotopy Type Theory*, in 13th International Conference on Typed Lambda Calculi and Applications (TLCA 2015). Leibniz International Proceedings in Informatics (LIPIcs), Volume 38, pp. 17-30, Schloss Dagstuhl - Leibniz-Zentrum für Informatik (2015) ([doi:10.4230/LIPIcs.TLCA.2015.17](https://doi.org/10.4230/LIPIcs.TLCA.2015.17), [arXiv:1504.02949](https://arxiv.org/abs/1504.02949))

* _coinductives_, [discussion](https://groups.google.com/forum/#!msg/homotopytypetheory/tYRTcI2Opyo/PIrI6t5me-oJ) on Homotopy Type Theory group.