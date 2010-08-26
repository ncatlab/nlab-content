In [[logic]], de Morgan duality is a [[duality]] between [[intuitionistic logic]] and [[paraconsistent logic]] (in its dual-intuitionistic form).  In [[classical logic]] and [[linear logic]], it is a self-duality mediated by [[negation]].  Although it goes back to Aristotle (at least), its discovery is generally attributed to Augustus de Morgan.

More explicitly, this is the duality between logical constants and operators as shown in the table below:

| Intuitionistic operator                  |   | Dual-intuitionistic operator               |
| ---------------------------------------- | - | ------------------------------------------ |
| $\top$ ([[truth]])                       |   | $\bot$ ([[falsehood]])                     |
| $\wedge$ ([[conjunction]])               |   | $\vee$ ([[disjunction]])                   |
| $\Rightarrow$ ([[conditional]])          |   | $\setminus$ ([[without]])                  |
| $\Leftrightarrow$ ([[biconditional]])    |   | $+$ ([[exclusive disjunction]])            |
| $\neg$ ($p \Rightarrow \bot$)            |   | $-$ ($\top \setminus p$)                   |
| $\forall$ ([[universal quantification]]) |   | $\exists$ ([[existential quantification]]) |
| $\Box$ ([[necessity]])                   |   | $\lozenge$ ([[possibility]])               |

Note that the first two operators in each column exist in both intuitionistic and dual-intuitionistic [[propositional logic]] and the last two in each column exist in both forms of [[predicate logic]] and [[modal logic]] (respectively), but they are still dual as shown.  All of these exist in classical logic (although some of the paraconsistent operators are not widely used), and the two forms of negation ($\neg$ and $-$) are the same there.

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

As with classical negation, linear negation is self dual.

The first two rows of the intuitionistic/paraconsistent/classical duality generalise to arbitrary [[lattice]]s, including [[subobject]] lattices in [[coherent category|coherent categories]], and from there to the duality between [[limit]]s and [[colimit]]s in category theory:

| Limit               |   | Colimit            |
| ------------------- | - | ------------------ |
| [[top]]             |   | [[bottom]]         |
| [[meet]]            |   | [[join]]           |
| [[intersection]]    |   | [[union]]          |
| [[terminal object]] |   | [[initial object]] |
| &#8942;                   |   | &#8942;                  |

So in a way, all duality in category theory is a generalisation of de Morgan duality.

The __de Morgan laws__ are the statements, valid in various forms of logic, that de Morgan duality holds.  In the [[foundations]] of [[constructive mathematics]], __de Morgan\'s Law__ usually means the statement $\neg(p \wedge q) \vdash \neg{p} \vee \neg{q}$, since the other de Morgan laws of intuitionistic propositional logic (the converse of this one, as well as $\neg(p \vee q) \equiv \neg{p} \wedge \neg{q}$ and the nullary versions $\neg{\top} \equiv \bot$ and $\neg{\bot} \equiv \top$) are already constructively valid.


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
