## Idea ##

The condition that a [[presheaf]] be a [[sheaf]] may be seen as a condition of unique existence.  A presheaf is separated if it satisfies the uniqueness part.

## Definition ##

A [[presheaf]] $A \in PSh(S)$ with respect to some [[site]] $S$ is **separated** if for all [[local isomorphism]]s $Y \to X$ the induced morphism $Hom(X,A) \to Hom(Y,A)$ is a [[monomorphism]].

## Remarks ##

Recall that a [[sheaf]] on $S$ is a presheaf $A$ such that for all local isomorphisms $Y \to X$ the induced morphism is an *[[isomorphism]]*.  So a separated presheaf is closed to being a sheaf, but not necessarily quite there.

As with sheaves, it is sufficient to check only the [[dense monomorphism]]s instead of all local isomorphisms.  This is equivalent to checking [[cover]]ing [[sieve]]s.