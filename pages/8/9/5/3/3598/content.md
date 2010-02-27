<div class="rightHandSide toc">
[[!include type theory - contents]]
</div>
In [[type theory]], a **display map** is a morphism $p\colon B\to A$ in a [[category]] which represents a [[dependent type]] under some categorical semantics of type theory valued in that category.  That is, $B$ represents a type dependent on a variable of type $A$, usually written syntactically as $x:A \vdash B(x):Type$.  The intended intuition is that $B(x)$ is the [[fiber]] of the map $p$ over $x\in A$.

More specifically, the [[syntactic category]] of a type theory is naturally equipped with a class of maps called "display maps" which come from its type dependencies, while models for such a theory can be studied in any other category equipped with a suitable class of maps called "display maps."  By the usual adjunction, such models are then equivalent to functors out of the syntactic category which preserve the relevant structure, including the display maps.

Since the most common dependent type theories include [[dependent product]] types, and any display map in a category that represents semantics for such a theory must be [[exponentiable morphism|exponentiable]], the term **display map** is sometimes used to mean any exponentiable morphism.

Sometimes all maps are display maps.  This happens particularly in extensional type theory, such as versions of the [[internal logic]] of categories that include dependent types.

[[!redirects display maps]]
[[!redirects display morphism]]
[[!redirects display morphisms]]
