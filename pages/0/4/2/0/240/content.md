A [[topos]] $E$ is **well-pointed** if

1. the [[terminal object]] 1 is a [[generator]], i.e., if $f, g: a \rightarrow b$ are morphisms such that $f x = g x$ for all [[global element]]s $x: 1 \to a$, then $f = g$, and
1. $E$ is nondegenerate, i.e., 1 is not an [[initial object]].

# Boolean properties

Assuming that one accepts [[excluded middle]] in one\'s metalogic, a well-pointed topos is also [[Boolean topos|Boolean]].  Similarly, a well-pointed topos is _two-valued_; that is, the only [[global element|global elements]] of the [[subobject classifier]] are $\top$ and $\bot$ (and these are distinct, by nondegeneracy).

# Logical properties

The main point of a well-pointed topos in logic is the equivalence of *external* and *internal* properties. In particular, a statement in the [[internal logic]] of the topos will be satisfied if and only if it holds for all global terms. (For the 'only if' part, it is necessary that the topos be nondegenerate.)

# In constructive mathematics

To maintain this logical result in [[constructive mathematics]] (that is, without excluded middle in the metalogic), one must add  the following requirements:

1. the terminal object is [[indecomposable object|indecomposable]], and
1. the terminal object is [[projective object|projective]].

These are analogues, for [[disjunction]] and [[existential quantification]], of the nondegeneracy requirement (which is about [[falsehood]]).  Classically, they follow from the two conditions given above.

Incidentally, a well-pointed topos in a constructive metalogic is still "two-valued" in the sense that a global element of the subobject classifier is false if and only if it is not true.  However, it is not two-valued in the (classically equivalent) sense that every global element of the subobject classifier is either true or false.

# In a pretopos

If $E$ is only a [[pretopos]], we have to strengthen the condition that 1 is a generator to the condition that 1 is a [[strong generator]], i.e. for any monomorphism $m:A\to B$, if every global element $1\to B$ factors through $m$, then $m$ is an isomorphism.  In a category with a subobject classifier (such as a topos), any generator is a strong generator.

This is important in [[predicative mathematics]], where the category of sets (and in general, a [[Grothendieck topos|category of sheaves]]) is a pretopos but need not be a topos. But of course it applies whenever one is studying a pretopos.

# In more general categories

Do we know what these should be in any more general situations?

[[Mike Shulman]]: Well, the pretopos version makes sense in any [[coherent category]], and I would bet that it's the right notion in that generality.  In a [[regular category]] one might just want to assert that $1$ is a (regular-)projective strong generator, which would probably be enough for regular logic.  And in a category with mere finite limits, being a strong generator is all one could ask for, and that'd probably be enough for finite-limit logic.


[[!redirects well-pointed pretopos]]
[[!redirects well-pointed category]]
[[!redirects well-pointed toposes]]
[[!redirects well-pointed topoi]]
