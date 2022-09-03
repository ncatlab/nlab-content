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

A [[type theory]] where types behave like [[sets]]. This includes:

* Any (definitionally) [[extensional type theory]], where there is an equality reflection rule for [[identity types]] or [[path types]] which turns their inhabitants into judgmental equalities. This includes [[Martin-Löf type theory]] with equality reflection and [[cubical type theory]] with equality reflection. 

* Any [[intensional type theory]] with an axiom like [[UIP]] or [[axiom K]], or rules which prove said axioms such as strong [[pattern matching]] or [[boundary separation]], which makes all [[identity types]] or [[path types]] valued in [[propositions]]/[[subsingletons]]. Examples of the latter include [[MLTT]] with [[UIP]], [[Lean]], the default type theory of [[Agda]], [[observational type theory]], and [[XTT]].

Set-level type theory contrasts with higher-level type theory such as [[homotopy type theory]] or plain [[intensional type theory]], where types behave (at least potentially) like [[n-groupoids]] or even [[infinity-groupoids]].  In the [[negative thinking|other direction]], it contrasts with type theories where types behave like [[propositions]] (type theories of this sort are often called [[logics]]).

## See also

* [[set-level foundations]]
