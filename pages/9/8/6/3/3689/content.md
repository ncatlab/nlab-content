
# Contents
* automatic table of contents goes here
{:toc}

## Idea

That [[category]] $Mod$ is the category of all [[module]]s over all commutative [[ring]]s.


## Definition

* An [[object]] is a pair $(R,N)$ consisting of a commutative [[ring]] $R$ and an $R$-[[module]] $N$. 

* A [[morphism]]

  $$
   (\phi,\kappa) :  (R,N) \to (R',N')
  $$

  is a pair consisting of a ring homomorphism $\phi : R \to R'$ and a morphism $\kappa : N \to \phi^* N'$ of $R$-modules, where $\phi^* N'$ is the [[tensor product]] $\phi^* N' := R \otimes_{\phi} N$.


## As a bifibration

Projecting out the first items in these pairs yields a canonical functor

$$
  p :Mod \to CRing
$$

$$
  (R,N) \mapsto R
  \,.
$$

that exhibits $Mod$ as a [[bifibration]] over $R$.

The fiber of this projection over a ring $R$ is $Mod_R$, the category of $R$-modules.

In particular the fiber over the initial commutative ring $R = \mathbb{Z}$ is

$$
  Mod_{\mathbb{Z}} = Ab
$$

the category [[Ab]] of abelian groups.


## Tangents and deformation theory

By an old observation of Quillen -- reviewed at [[module]] -- the bifibration $Mod \to CRing$ this is [[equivalence of categories|equivalent]] to the category of fiberwise abelian [[group object]] in the [[codomain fibration]] $[I,CRing] \to CRing$:

$$
  (Mod \to CRing) \simeq Ab([I,CRing]] \to CRing)
  \,.
$$

For a fixed ring $R$, the category $Mod_R$ of $R$-modules is canonically equivalent to $Ab(CRing/R)$, the category of abelian [[group object]]s in the [[overcategory]] $CRing/R$:

$$
  Mod_R \simeq Ab(CRing/R)
  \,.
$$

This says that $Mod \to Ring$ is the [[tangent category]] of $CRing$: the above equivalence regards an $R$-module $N$ equivalently as the square-0-extension ring $R \oplus N$ (with producte $(r_1,n_1) \cdots (r_2,n_2) = (r_1 r_2, r_1 n_2 + r_2 n_1)$), which may be thought of as the ring of functions on the infinitesimal neighbourhood of the 0-section of the [[vector bundle]] (or rather [[quasicoherent sheaf]]) over $Spec R$ that is given by $N$.

There is thus another natural projection from $Mod$ to rings, namely the functor that remembers these square-0-extensions

$$
  f : Mod \to CRing
$$

$$
  (R,N) \mapsto R \oplus N
  \,.
$$

This functor has a [[left adjoint]] $\Omega : CRing \to Mod$ which is also a [[section]]: this is the functor that sends a ring to its module of [[Kähler differential]]s.

$$
  (\Omega \dashv f) :  Mod \stackrel{\overset{\Omega}{\leftarrow}}{\underset{f}{\to}}
  CRing
  \,.
$$


## References

A summary of these classical facts together with their embedding into the bigger picture of [[tangent (∞,1)-category|tangent (∞,1)-categories]] is in

* [[Jacob Lurie]], _[[Deformation Theory]]_


category: category

[[!redirects Mod]]

[[!redirects RMod]]
[[!redirects R Mod]]
[[!redirects R-Mod]]
[[!redirects KMod]]
[[!redirects K Mod]]
[[!redirects K-Mod]]
[[!redirects kMod]]
[[!redirects k Mod]]
[[!redirects k-Mod]]

[[!redirects category of modules]]
[[!redirects categories of modules]]
