[[!redirects tangent (∞,1)-category]]

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For $C$ a [[locally presentable (∞,1)-category]] whose objects one thinks of as function algebras on certain test spaces, the **tangent $(\infty,1)$-category** $T_C \to C$ of $C$ is the fiberwise [[stabilization]] of the [[codomain fibration]] $[\Delta[1], C] \to C$. 

As discussed at [[deformation theory]],  this generalizes the classical [[bifibration]] $Mod \to CRing$ of the category of all [[module]]s over the cateory [[CRing]] of all commutative rings: the fiber of the tangent $(\infty,1)$-category $T_C$ over an object $A \in C$ may be thought of as the $(\infty,1)$-category of _modules_ over $A$, or more geometrically as the $(\infty,1)$-category of [[vector bundle]]s or rather [[quasicoherent sheaves]] over whatever [[space]] $A$ is regarded to be the algebra of functions on.
 
A remarkable amount of information about the geometry of these spaces is encoded in the fiber of the tangent $(\infty,1)$-category over them. Notably the [[left adjoint|left]] [[adjoint (∞,1)-functor]] 

$$
  \Omega : C \to T_C
$$

to the domain projection $dom : T_C \to C$ turns out to send each $A$ to its [[cotangent complex]] $\Omega(A)$, to be thought of as the module of [[Kähler differential]]s on the space that $A$ is functions on.



## References

The definition and study of the notion is tangent $(\infty,1)$-categories is from 

* [[Jacob Lurie]], _[[Deformation Theory]]_