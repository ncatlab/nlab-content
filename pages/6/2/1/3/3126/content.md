[[!redirects tangent (∞,1)-category]]

#Contents#
* automatic table of contents goes here
{:toc}

## Idea


For $C$ an [[(∞,1)-category]], its **tangent $(\infty,1)$-category** $T_C \to C$ is the $(\infty,1)$-category over $C$ obtained from the forming fiberwise the [[stabilization]] of the [[codomain fibration]] $cod : [I,C] \to C$:

an object of $T_C$ over an object $A \in C$ is an object of the [[stable (∞,1)-category]] $Stab(C^{/A})$ that is the [[stabilization]] of the [[overcategory]] of $C$ over $A$.

As described at [[deformation theory]], this may be thought of as generalizing the [[bifibration]] $Mod \to Ring$ of [[module]]s over [[ring]]s. In this sense,one may think of the fibers of of a tangent $(\infty,1)$-category as a generalization of a category of modules.

## Cotangent complex

The projection functor $p : T_C \to C$ has a [[left adjoint]]

$$
  \Omega : C \to T_C
$$

that is also a [[section]]. This is the [[cotangent complex]] functor. It sends each object to the analog of the [[Kähler differential]]s of that object.

## Applications

The tangent $(\infty,1)$-category $T_C \to C$ is a generalization of the [[bifibration]] $Mod \to Ring$ of [[module]]s over [[ring]]s that models the [[stack]] algebraic [[vector bundle]]s (as described in more detail at [[Sweedler coring]]). It is used in [[deformation theory]] for a general definition of [[cotangent complex]] of an [[(∞,1)-category]].

## References

The definition and study of the notion is tangent $(\infty,1)$-categories is from 

* [[Jacob Lurie]], [[Deformation Theory]]