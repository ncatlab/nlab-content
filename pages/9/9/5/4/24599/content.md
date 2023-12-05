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

A [[type theory]] where types behave like [[sets]], i.e. in which all types are [[h-sets]].  Thus, it is a form of [[set-level foundations]]. This includes:

* Any (definitionally) [[extensional type theory]], where there is an equality reflection rule for [[identity types]] or [[path types]] which turns their inhabitants into judgmental equalities. This includes [[Martin-Löf type theory]] with equality reflection and [[cubical type theory]] with equality reflection. 

* Any [[intensional type theory]] with an axiom like [[UIP]] or [[axiom K]], or rules which prove said axioms such as strong [[pattern matching]] or [[boundary separation]], which makes all [[identity types]] or [[path types]] valued in [[propositions]]/[[subsingletons]]. Examples of the latter include [[MLTT]] with [[UIP]], [[Lean]], the default type theory of [[Agda]], [[observational type theory]], and [[XTT]].

Set-level type theory contrasts with higher-level type theory such as [[homotopy type theory]] or plain [[intensional type theory]], where types behave (at least potentially) like [[n-groupoids]] or even [[infinity-groupoids]].  In the [[negative thinking|other direction]], it contrasts with type theories where types behave like [[propositions]] (type theories of this sort are often called [[logics]]).

## Set-level intensional type theories

In a set-level but intensional type theory, we distinguish [[definitional equality|definitional]] and [[propositional equality]] (unlike in [[extensional type theory]]), but no two terms can be propositionally equal in more than one way (up to propositional equality).  In the language of [[homotopy type theory]], this means that all types are [[h-sets]].  There are a number of equivalent ways to force this to be true by adding [[axioms]] to type theory.

1. We can add as an axiom the "uniqueness of identity proofs" ([[axiom UIP]]) property that any two inhabitants of the same identity type $Id_A(x,y)$ are themselves equal (in the corresponding higher identity type).

1. We can add Streicher's *[[axiom K]]* which says that any inhabitant of a self-equality type $Id_A(x,x)$ is (propositionally) equal to the identity/reflexivity equality $1_x$.  (Axiom K is so named because $K$ comes after $J$, and $J$ usually denotes the [[elimination rule|eliminator]] for [[identity types]].)

1. In the presence of [[dependent sum types]], we can add an axiom saying that if $(a,b_1)$ and $(a,b_2)$ are pairs in a dependent sum $\sum_{x\colon A} B(x)$ with the same first component, and the identity type $Id_{\sum_{x\colon A} B(x)}((a,b_1), (a,b_2))$ is inhabited, then so is $Id_{B(a)}(b_1,b_2)$.

1. Given the [[circle type]] $S^1$, we can add any of the equivalent axioms which state respectively that $S^1$ is a [[set]] $\mathrm{isSet}(S^1)$; $S^1$ is a [[proposition]] $\mathrm{isProp}(S^1)$ or a [[contractible type]] $\mathrm{isContr}(S^1)$, which are the same condition as $S^1$ being a [[set]] because $S^1$ is provably a [[pointed connected groupoid]]; and there is an [[identification]] $K:\mathrm{refl}_{S^1}(\mathrm{base}) =_{S^1} \mathrm{loop}$. 

1. We can allow definition of functions by a strong form of *pattern matching*, as in unmodified [[Agda]].  The relevant "extra strength" is to allow output *types* of a pattern match which are only well-defined *after* the pattern has been matched.

1. In [[cubical type theory]] (with [[glue types]] removed, since univalence is incompatible with set-level-ness), we can add a [[boundary separation]] rule, leading to [[XTT]].


## See also

* [[set-level foundations]]

[[!redirects set-level type theories]]
