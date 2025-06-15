
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

There is a lot of interesting stuff to be said about _equality_ in [[logic]], [[higher category theory]], and the [[foundations]] of mathematics, but it hasn\'t all been said here yet.

## Different kinds of equality
   {#DifferentKinds}

Here is a list of distinctions between different notions of _equality_, in different contexts, where possibly all the following pairs of notions are, in turn, "the same", just expressed in terms of different terminologies:

* the difference between [[axiom|axiomatic]] and [[definition|defined]] equality;
* the difference between identity and equality,
* the difference between intensional and extensional equality,
* the difference between the notions of equality: equality [[judgements]], equality [[propositions]], and equality [[types]]; see [[equality in type theory]] for more details,
* the difference between equality and [[isomorphism]],
* the difference between equality and [[equivalence]],
* the possibility of operations that might not preserve equality.

## Equality in constructive and classical mathematics

Constructive mathematics is mathematics in which the law of excluded middle does not necessarily hold for [[propositions]], [[subsingletons]], or [[h-propositions]]. Classical mathematics is mathematics in which the law of excluded middle does hold for [[propositions]], [[subsingletons]], or [[h-propositions]]. Here, we take equality to mean either typal or propositional equality, so that equality is a relation or a type family on a type or set. 

In classical mathematics, equality of sets is a [[stable relation|stable]] [[equivalence relation]], and [[denial inequality]] of sets is a [[tight apartness relation]]. However, in constructive mathematics, equality cannot be proven to be stable for all sets, and denial inequality cannot be proven to be a tight apartness relation for all sets. Instead, one could distinguish between 4 different notions of equality and [[inequality]]:

* [[tight apartness relations]]. However, not all sets have tight apartness relations. 

* equality, which is an [[equivalence relation]]; set with [[tight apartness relations]] have [[stable equality]]. 

* [[denial inequality]], which can only be proven to be a [[weakly tight]] [[irreflexive symmetric relation]]. However, all statements in classical mathematics involving only denial inequalities hold in constructive mathematics, by the [[double negation translation]] and the property that for any proposition $P$, $\neg \neg \neg P$ if and only if $\neg P$. 

* the [[double negation]] of equality, which can only be proven to be a [[stable relation|stable]] [[reflexive symmetric relation]]. However, all statements in classical mathematics involving only equality hold in constructive mathematics with the equality replaced by its double negation, by the [[double negation translation]]. 

The sets in which equality and inequality behaves as it does in [[classical mathematics]] are the sets with [[decidable equality]]. 

As a result, in constructive mathematics, sometimes one takes sets with [[tight apartness relations]] instead of general [[sets]] to be the foundational primitive concept. In classical mathematics, this is unnecessary, because every [[set]] has a [[tight apartness relation]]. 

## Related concepts

* **equality**, [[equation]]

* [[definition]], [[assignment]], [[equality]]

* [[inequality]]

  * [[denial inequality]] 
  
  * [[apartness relation]]

  * [[antithesis interpretation]]

* [[isomorphism]]

* [[equivalence]]

* [[weak equivalence]]

* [[homotopy equivalence]], [[weak homotopy equivalence]]

* [[equivalence in an (∞,1)-category]]

* [[equivalence of (∞,1)-categories]]

[[!include logic symbols -- table]]

## References

* [[Kevin Buzzard]], *Grothendieck's use of equality* ([arXiv:2405.10387](https://arxiv.org/abs/2405.10387))

[[!redirects equal]]
[[!redirects equals]]
[[!redirects equality]]
[[!redirects equalities]]