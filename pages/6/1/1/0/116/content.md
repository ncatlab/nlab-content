# Definition #

A **group** is a [[groupoid]] with one object.

Don't worry: this definition is equivalent to [the definition you're used to](http://en.wikipedia.org/wiki/Group_%28mathematics%29#Definition).

# Internalization #

A **group object** [[internalization|in]] a [[category]] $C$ with finite [[product|products]] is an object $G$ together with maps $mult:G\times G\to G$, $id:1\to G$, and $inv:G\to G$ such that various diagrams expressing associativity, unitality, and inverses commute.

Equivalently, it is a functor $C^{op}\to Grp$ whose underlying functor $C^{op} \to Set$ is [[representable functor|representable]].

For example, a group object in [[Diff]] is a [[Lie group]].  A group object in [[Top]] is a [[topological group]].  And a group object in $CAlg^{op}$, where $CAlg$ is the category of commutative algebras, is a (commutative) [[Hopf algebra]].

A group object in [[Grp]] is the same thing as an abelian group (see [[Eckmann-Hilton lemma]]), and a group object in [[Cat]] is the same thing as an [[internal category]] in [[Grp]], both being equivalent to the notion of [[crossed module]]. 
