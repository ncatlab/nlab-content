
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# De Morgan duality
* table of contents
{: toc}

## Idea

In [[logic]], De Morgan duality is a [[duality]] between [[intuitionistic logic]] and dual-intuitionistic [[paraconsistent logic]].  In [[classical logic]] and [[linear logic]], it is a [[self-duality]] mediated by [[negation]].  Although it goes back to [[Aristotle]] (at least), its discovery is generally attributed to [[Augustus De Morgan]].


## The dualities

More explicitly, __De Morgan duality__ is the duality between logical operators as shown in the table below:

| Intuitionistic operator                  |   | Dual-intuitionistic operator               |
| ---------------------------------------- | - | ------------------------------------------ |
| $\top$ ([[truth]])                       |   | $\bot$ ([[falsehood]])                     |
| $\wedge$ ([[conjunction]])               |   | $\vee$ ([[disjunction]])                   |
| $\Rightarrow$ ([[conditional]])          |   | $\setminus$ ([[co-Heyting algebra|subtraction]])                  |
| $\Leftrightarrow$ ([[biconditional]])    |   | $+$ ([[exclusive disjunction]])            |
| $\neg$ ($p \Rightarrow \bot$)            |   | $-$ ($\top \setminus p$)                   |
| $\forall$ ([[universal quantification]]) |   | $\exists$ ([[existential quantification]]) |
| $\Box$ ([[necessity]])                   |   | $\lozenge$ ([[possibility]])               |

The first two operators in each column exist in both intuitionistic and dual-intuitionistic [[propositional logic]] and the last two in each column exist in both forms of [[predicate logic]] and [[modal logic]] (respectively), but they are still dual as shown.  All of these exist in [[classical logic]] (although some of the paraconsistent operators are not widely used), and the two forms of negation ($\neg$ and $-$) are the same there.

In [[linear logic]], this extends to a duality between conjunctive and disjunctive operators:

| Conjunctive operator |   | Disjunctive operator |
| -------------------- | - | -------------------- |
| $\top$               |   | $0$                  |
| $1$                  |   | $\bot$               |
| $\&$                 |   | $\oplus$             |
| $\otimes$            |   | $\parr$              |
| $^\bot$              |   | $^\bot$              |
| $\bigwedge$          |   | $\bigvee$            |
| $!$                  |   | $?$                  |

As with classical negation, linear [[negation]] is self-dual. (For the [[categorical semantics]] of this see at [[dualizing object]] and at _[Wirthm&#252;ller context -- Comparison of push-forwards](Wirthm&#252;ller+context#PushforwardsIntertwinedByDuality)_.)

The first two rows of the intuitionistic/dual-intuitionistic/classical duality generalise to arbitrary [[lattices]], including [[subobject]] lattices in [[coherent category|coherent categories]], and from there to the duality between [[limits]] and [[colimits]] in category theory:

| Limit               |   | Colimit            |
| ------------------- | - | ------------------ |
| [[top]]             |   | [[bottom]]         |
| [[meet]]            |   | [[join]]           |
| [[intersection]]    |   | [[union]]          |
| [[terminal object]] |   | [[initial object]] |
| &#8942;                   |   | &#8942;                  |

So in a way, all [[duality]] in category theory is a generalisation of De Morgan duality.

## Related concepts

* [[De Morgan laws]]

[[!redirects De Morgan duality]]
[[!redirects De Morgan dualities]]
[[!redirects de Morgan duality]]
[[!redirects de Morgan dualities]]

[[!redirects De Morgan dual]]
[[!redirects De Morgan duals]]
[[!redirects de Morgan dual]]
[[!redirects de Morgan duals]]
