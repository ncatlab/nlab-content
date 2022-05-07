
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
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
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


## The De Morgan laws

The __De Morgan laws__ are the statements, valid in various forms of logic, that De Morgan duality is mediated by [[negation]].  For example, using the second line of the first table, we have
$$ \array {
   \neg(p \wedge q) \equiv \neg{p} \vee \neg{q} ,\\
   \neg(p \vee q) \equiv \neg{p} \wedge \neg{q} .
} $$
Traditionally, the term is reserved for this line.

In the [[foundations]] of [[constructive mathematics]], __De Morgan\'s Law__ usually means the statement
$$ \neg(p \wedge q) \vdash \neg{p} \vee \neg{q} ,$$
since every other aspect of the first two lines is already constructively valid, the claim that negation mediates the De Morgan self-duality already has a name (the [[double negation]] law, equivalent to the principle of [[excluded middle]]), and no other line involves only operators that appear in intuitionstic [[propositional calculus]].  This de Morgan's law is equivalent to the law of [[weak excluded middle]].


## Related concepts

* [[De Morgan Heyting algebra]]

* [[De Morgan algebra]]

* [[excluded middle]]


[[!redirects De Morgan duality]]
[[!redirects De Morgan dualities]]
[[!redirects de Morgan duality]]
[[!redirects de Morgan dualities]]

[[!redirects De Morgan dual]]
[[!redirects De Morgan duals]]
[[!redirects de Morgan dual]]
[[!redirects de Morgan duals]]

[[!redirects De Morgan law]]
[[!redirects De Morgan laws]]
[[!redirects de Morgan law]]
[[!redirects de Morgan laws]]
[[!redirects De Morgan's law]]
[[!redirects De Morgan's laws]]
[[!redirects de Morgan's law]]
[[!redirects de Morgan's laws]]
[[!redirects De Morgan's law]]
[[!redirects De Morgan's laws]]
