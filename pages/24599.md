+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A [[type theory]] where types behaves like [[sets]]. This includes:

* Any definitional [[extensional type theory]], where there is an equality reflection rule for [[identity types]] or [[path types]] which turns them into judgmental equalities. This includes [[Martin-Löf type theory]] with equality reflection and [[cubical type theory]] with equality reflection. 

* Any definitionally [[intensional type theory]] with an axiom like [[UIP]] or [[axiom K]] or rules which prove said axioms like [[boundary separation]], which makes all [[identity types]] or [[path types]] valued in [[propositions]]/[[subsingletons]]. Examples of the latter include [[MLTT]] with [[UIP]], [[Lean]], the default type theory of [[Agda]], [[observational type theory]], and [[XTT]]

Contrast with higher-level type theory, where types behave like [[n-groupoids]] or even [[infinity-groupoids]], and type theories where types behave like [[propositions]]. 

## See also

* [[set-level foundations]]