
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A __hereditarily finite set__ is a [[finite set]] of hereditarily finite sets; this circular definition is usually interpreted [[recursion|recursively]], although you can also interpret it [[corecursion|corecursively]] to get _ill-founded_ hereditarily finite sets.  The set of all (well-founded) hereditarily finite sets (which is infinite, and not hereditarily finite itself) is written $V_\omega$ to show its place in the [[von Neumann hierarchy]] of pure sets.

As a property of a [[set]], being hereditarily finite is equivalent (up to [[isomorphism]] of sets) to simply being finite.  So the 'hereditary' part is meaningful only in  [[material set theory]], not [[structural set theory|structurally]], unless you see it as a property of a [[pure set]] represented structurally as a membership tree.


## Properties

There are countably many hereditarily finite sets, up to [[equality]] (in material set theory), and in fact they can be neatly enumerated as follows:  Given a [[natural number]] $n \geq 0$, write $n$ in base $2$; the $i$th hereditarily finite set is a member of the $n$th one if the $i$th bit of $n$ is $1$.  (This definition is well-founded, because the highest non-zero bit of $n$ must have position at most $\log_2 n$, which is less than $n$.)

So the hereditarily finite sets are as follows:

| number |   | in base $2$ |   | set                                  |
| ------ | - | ----------- | - | ------------------------------------ |
| $0$    |   | (empty)     |   | $\empty = \{\}$                      |
| $1$    |   | $1$         |   | $\star = \{\empty\}$                 |
| $2$    |   | $10$        |   | $2_Z = \{\star\}$                    |
| $3$    |   | $11$        |   | $2_{vN} = \{\empty, \star\}$         |
| $4$    |   | $100$       |   | $3_Z = \{2_Z\}$                      |
| $5$    |   | $101$       |   | $\{\empty, 2_Z\}$                    |
| $6$    |   | $110$       |   | $\{\star, 2_Z\}$                     |
| $7$    |   | $111$       |   | $\{\empty, \star, 2_Z\}$             |
| $8$    |   | $1000$      |   | $\{2_{vN}\}$                         |
| $9$    |   | $1001$      |   | $\{\empty, 2_{vN}\}$                 |
| $10$   |   | $1010$      |   | $\{\star, 2_{vN}\}$                  |
| $11$   |   | $1011$      |   | $3_{vN} = \{\empty, \star, 2_{vN}\}$ |
| $12$   |   | $1100$      |   | $\{2_Z, 2_{vN}\}$                    |
| $13$   |   | $1101$      |   | $\{\empty, 2_Z, 2_{vN}\}$            |
| $14$   |   | $1110$      |   | $\{\star, 2_Z, 2_{vN}\}$             |
| $15$   |   | $1111$      |   | $\{\empty, \star, 2_Z, 2_{vN}\}$     |
| &#8942;      |   | &#8942;           |   | &#8942;                                    |

In this table, we\'ve indicated the representations of $2$ and $3$ in the most common models of natural numbers as pure sets, those of **Z**ermelo (where $n + 1 = \{n\}$) and of **v**on **N**eumann (where $n + 1 = n \cup \{n\}$); these both begin with $0 = \empty$ and $1 = \star$ but diverge thereafter.  (Von Neumann\'s representation is favoured now, as it allows each natural number to have itself as its [[cardinal number]], a situation that generalises to infinite limit [[ordinal numbers]].)  However, the existence of this enumeration shows that another representation of natural numbers as pure sets is to use *all* hereditarily finite sets.

The set $V_\omega$ of hereditarily finite sets is a [[Grothendieck universe]] (unless you phrase the definition specifically to rule this out).  Thus the [[axiom of infinity]] (which guarantees the existence of some model of the set $\mathbf{N}$ of natural numbers) can be seen as following from a very simple universe axiom: that some [[Grothendieck universe]] exists.  Conversely, if any [[natural numbers object]] $\mathbf{N}$ exists in the category of sets, then you can form the universe $V_\omega$ (using the [[axiom of replacement]]) by performing the above enumeration.

In [[constructive mathematics]], one gets different notions of hereditarily finite set depending on exactly how one defines _[[finite set]]_.  The enumeration above works if you use the strictest sense, but you need to close under taking [[subsets]] (or use subfinite sets to start with) to get a Grothendieck universe in [[material set theory]].


[[!redirects hereditarily finite set]]
[[!redirects hereditarily finite sets]]
