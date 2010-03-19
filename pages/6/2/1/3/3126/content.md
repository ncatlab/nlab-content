[[!redirects tangent (∞,1)-category]]

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For $K$ a [[locally presentable (∞,1)-category]] whose objects we think of as [[space]]s of sorts, its **tangent $(\infty,1)$-category**

$$
  (T_{K^{op}})^{op} \to K
$$

is an [[(∞,1)-category]] over $K$, whose objects may be thought of as spaces that are **[[infinitesimal space|infinitesimal]] thickenings** of those of $K$.

More concretely, the tangent $(\infty,1)$-category $T_C \to C$ for $C = K^{op}$ is the fiberwise [[stabilization]] of the [[codomain fibration]] $[\Delta[1], C] \to C$.  

This generalizes -- as discussed at [[deformation theory]] -- the classical example of the [[bifibration]] [[Mod]] $\to$ [[CRing]] of the category of all [[module]]s over the cateory [[CRing]] of all commutative rings: 

the fiber of the tangent $(\infty,1)$-category $T_C$ over an object $A \in C$ may be thought of as the $(\infty,1)$-category of **square-0-extensions** $A \oplus N$ of $A$, for $N$ a [[module]] over $A$. Dually, in $K = C^{op}$ we may think of these as being infinitesimal neighbourhoods of 0-sections of [[vector bundle]]s or rather [[quasicoherent sheaves]] over whatever [[space]] $A$ is regarded to be the algebra of functions on.
 
A remarkable amount of information about the geometry of these spaces/objects in $K$ is encoded in the fiber of the tangent $(\infty,1)$-category over them. Notably the [[left adjoint|left]] [[adjoint (∞,1)-functor]] 

$$
  \Omega : C \to T_C
$$

to the domain projection $dom : T_C \to C$ turns out to send each $A$ to its [[cotangent complex]] $\Omega(A)$, to be thought of as the module of [[Kähler differential]]s on the space that $A$ is functions on.



## References

The definition and study of the notion is tangent $(\infty,1)$-categories is from 

* [[Jacob Lurie]], _[[Deformation Theory]]_

[[!redirects tangent (infinity,1)-categories]]
[[!redirects tangent (∞,1)-category]]
[[!redirects tangent (∞,1)-categories]]
