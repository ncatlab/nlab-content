Informally, a **free functor** is a [[left adjoint]] to a [[forgetful functor]]. (This is informal because the concept of forgetful functor is informal; *any* functor might be viewed as forgetful, so *any* left adjoint might be viewed as free, while in practice only some are.)

One formal sort of free functor is the left adjoint $C\to C^T$, where $T$ is a [[monad]] on the category $C$ and $C^T$ is its [[Eilenberg-Moore category]] (the category of $T$-algebras).  This includes:

* The "free group" functor $Set \to Grp$

* The "free abelian group" functor $Set \to Ab$

* The "free category" functor $DiGraph \to Cat$

and many others.

In general, if $U: C \to D$ is thought of as a forgetful functor and $F: D \to C$ is its left adjoint, then $F(x)$ is the __free $C$-object__ on an object $x$ of $D$.


[[!redirects free object]]
[[!redirects free objects]]