A [[topos]] $E$ is __well-pointed__ if the [[terminal object]] 1 is a [[generator]], i.e., if $f, g: a \rightarrow b$ are morphisms such that $f x = g x$ for all [[global element]]s $x: 1 \to a$, then $f = g$. It is usually also required that $E$ be nondegenerate, i.e., 1 is not an [[initial object]].

# Boolean properties

Assuming that one accepts [[excluded middle]] in one\'s metalogic, a well-pointed topos is also a [[boolean topos]]. Similarly, a well-pointed topos is _two-valued_; that is, the only [[global element|global elements]] of the [[subobject classifier]] are $\top$ and $\bot$ (and these are distinct, by nondegeneracy).

# Logical properties

The main point of a well-pointed topos in logic is the equivalence of *external* and *internal* properties. In particular, a statement in the [[internal logic]] of the topos will be satisfied if and only if it holds for all global terms. (For the 'only if' part, it is necessary that the topos be nondegenerate.)

# In constructive mathematics

To maintain this logical result in constructive mathematics (that is, without excluded middle in the metalogic), one must add to the nondegeneracy requirement that the terminal object be [[indecomposable object|indecomposable]] and [[projective object|projective]]. These are analogues, for [[disjunction]] and [[existential quantification]], of the nondegeneracy requirement (which is about [[falsehood]]).

Incidentally, a well-pointed topos is still two-valued in the sense that a global element of the subobject classifier is false if (and only if, given nondegeneracy) it is not true.  However, it is not two-valued in the (classically equivalent) sense that every global element of the subobject classifier is either true or false.
