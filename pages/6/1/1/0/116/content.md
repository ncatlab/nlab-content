# Definition #

A _group_ is a [[groupoid]] with one object.

Don't worry: this definition is equivalent to [the definition you're used to](http://en.wikipedia.org/wiki/Group_%28mathematics%29#Definition).

# Internalization #

A **group object** [[internalization|in]] a [[category]] $C$ with finite [[product|products]] is an object $G$ together with maps $mult:G\times G\to G$, $id:1\to G$, and $inv:G\to G$ such that various diagrams expressing associativity, unitality, and inverses commute.

Equivalently, it is a functor $C^{op}\to Grp$ whose underlying functor $C^{op} \to Set$ is [[representable functor|representable]].

For example, a group object in [[Diff]] is a [[Lie group]].  A group object in [[Top]] is a [[topological group]].  And a group object in $Alg^{op}$, where $Alg$ is the category of commutative algebras, is a (commutative) [[Hopf algebra]].

+--{.query}
I'm a little confused by this last example. I can believe that a group object in the opposite $CAlg^{op}$ of the category of commutative algebras is a commutative Hopf algebra, because the product there is given by coproduct in $CAlg$ which is tensor product on the underlying vector spaces. But the coproduct in $Alg$ is something more complicated, so I don't see how you get comultiplication $H \to H \otimes H$ this way. 

Added later: I see the same point was made by the same author (Mike) over at [[Hopf algebra]], so I'm going to go ahead and insert the correction here too. 
=--