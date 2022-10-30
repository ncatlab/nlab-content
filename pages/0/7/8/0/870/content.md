
# De Morgan duality
* table of contents
{: toc}

## Idea

In [[logic]], de Morgan duality is a [[duality]] between [[intuitionistic logic]] and dual-intuitionistic [[paraconsistent logic]].  In [[classical logic]] and [[linear logic]], it is a self-duality mediated by [[negation]].  Although it goes back to [[Aristotle]] (at least), its discovery is generally attributed to [[Augustus de Morgan]].


## The dualities

More explicitly, __de Morgan duality__ is the duality between logical operators as shown in the table below:

| Intuitionistic operator                  |   | Dual-intuitionistic operator               |
| ---------------------------------------- | - | ------------------------------------------ |
| $\top$ ([[truth]])                       |   | $\bot$ ([[falsehood]])                     |
| $\wedge$ ([[conjunction]])               |   | $\vee$ ([[disjunction]])                   |
| $\Rightarrow$ ([[conditional]])          |   | $\setminus$ ([[without]])                  |
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

As with classical negation, linear [[negation]] is self-dual.

The first two rows of the intuitionistic/dual-intuitionistic/classical duality generalise to arbitrary [[lattices]], including [[subobject]] lattices in [[coherent category|coherent categories]], and from there to the duality between [[limits]] and [[colimits]] in category theory:

| Limit               |   | Colimit            |
| ------------------- | - | ------------------ |
| [[top]]             |   | [[bottom]]         |
| [[meet]]            |   | [[join]]           |
| [[intersection]]    |   | [[union]]          |
| [[terminal object]] |   | [[initial object]] |
| &#8942;                   |   | &#8942;                  |

So in a way, all [[duality]] in category theory is a generalisation of de Morgan duality.


## The de Morgan laws

The __de Morgan laws__ are the statements, valid in various forms of logic, that de Morgan duality is mediated by [[negation]].  For example, using the second line of the first table, we have
$$ \array {
   \neg(p \wedge q) \equiv \neg{p} \vee \neg{q} ,\\
   \neg(p \vee q) \equiv \neg{p} \wedge \neg{q} .
} $$
Traditionally, the term is reserved for this line.

In the [[foundations]] of [[constructive mathematics]], __de Morgan\'s Law__ usually means the statement
$$ \neg(p \wedge q) \vdash \neg{p} \vee \neg{q} ,$$
since every other aspect of the first two lines is already constructively valid, the claim that negation mediates the de Morgan self-duality of negation already has a name (the [[double negation]] law, equivalent to the principle of [[excluded middle]]), and no other line involves only operators that appear in intuitionstic [[propositional calculus]].


[[!redirects de Morgan duality]]
[[!redirects de Morgan dualities]]
[[!redirects de Morgan dual]]
[[!redirects de Morgan duals]]

[[!redirects de Morgan law]]
[[!redirects de Morgan laws]]
[[!redirects de Morgan's law]]
[[!redirects de Morgan's laws]]
[[!redirects de Morgan's law]]
[[!redirects de Morgan's laws]]
