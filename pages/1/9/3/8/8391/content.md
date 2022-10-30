
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

In [[logic]], _decidable_ refers to the question of whether there is an effective method for deciding membership in a set of formulas (or [[judgment]]s in [[type theory]]). Here we take an effective method to be given by any of the equivalent formal characterizations ([[general recursion]], [[Turing machine]]s, [[lambda calculus]]) that according to the [[Church-Turing thesis]] capture the informal notion.

Sometimes _decidable_ is also used in another sense, namely that of [[independent statement]], according to which a logical theory decides a formula if it proves the formula or its [[negation]] (see at _[[decidable proposition]]_), and according to which a formula is undecidable (independent) if the theory in question proves neither the formula nor its negation. This is the sense in which the [[continuum hypothesis]] in undecidable from the axioms of [[ZFC]] and in which the [[consistency statement]] of a sufficiently strong, recursively enumerated theory is undecidable in (independent of) that theory, according to G&#246;del's [[second incompleteness theorem]]. To avoid confusion, the preferred term to use here is [[independent]]. 

## Decidability of a logical system

A logical system is decidable if there is an algorithm deciding whether a given formula is a theorem of the system.

In this sense, [[propositional logic]] and [[monadic predicate logic]] are decidable, whereas [[first-order logic]] and [[higher-order logic]] are undecidable

## Decidability of a theory

A [[theory]] is a set of formulas closed under logical consequence (in some logical system, usually first order logic with a given [[signature]]). A theory is decidable if there is an algorithm (effective method) deciding whether a formula is a member of the theory of not. In the usual case where the theory is presented from a list of [[axiom]]s, the question is whether the formula is deducible from the axioms.

Examples of decidable theories include:

* [[Presburger arithmetic]]
* the first-order theory of [[Boolean algebra]]s
* the first-order theory of [[real closed field]]s
* the monadic second-order theory of the binary tree

Examples of undecidable theories include:

* [[Peano arithmetic]] (considered as either a first-order or a second-order theory)
* the first-order theory of [[groups]]

## In the context of type theory

[[type theory|Type theory]] gives rise a number of decision problems, and it is generally desirable that these are solvable.

### Type checking

[[Type checking]] refers to the problem whether the judgment $\Gamma\vdash a : A$ is derivable in a given type theory. For instance, [[intensional type theory]] has decidable type checking, but [[extensional type theory]], which adds the rule of [[equality reflection]], does not. For an exposition of this result, see the [thesis](#Hofmann) of Hofmann. 

In more expressive type theories, we can also ask whether [[judgmental equality]] (also called _computational_ or _definitional_ equality) is decidable. Since deciding the judgmental equality is often a prerequisite for deciding type checking, systems with decidable type checking often have decidable judgmental equality.

### Typability

[[Typeability]] refers to the problem of deciding for a given term whether it inhabits some type. [[simple type theory|Simple type theory]] has decidable typeability, and the programming language [[ML]], which features a weak form of polymorphism, [[let polymorphism]], also has decidable typeability.
 
[[dependent type theory]] has undecidable typeability.

### Type inhabitation

[[Type inhabitation]] refers to the problem of deciding for a given type whether there is a term that inhabits it. Under the propositions-as-types correspondence, this incorporates the question of the decidability of the corresponding logic since a proposition is provable if and only if the the type of its proofs is inhabited.

For [[simple type theory]], type inhabitation is  decidable, whereas it is undecidable for [[dependent type theory]].

## Related concepts

* **decidability**

  * [[decidable subset]]

  * [[decidable object]]

  * [[decidable equality]]

  * [[decidable proposition]]

* [[definability]]

## References

* Wikipedia, _[Decidablility (logic)](http://en.wikipedia.org/wiki/Decidability_%28logic%29)_ 

* Martin Hofmann, _Extensional concepts in intensional type theory_, Ph.D. dissertation, University of Edinburgh (1995). ([link](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/)) 
 {#Hofmann} 

[[!redirects type checking]]
