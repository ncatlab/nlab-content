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

More concretely, the tangent $(\infty,1)$-category $T_C \to C$ for $C = K^{op}$ is the fiberwise [[stabilization]] of the [[codomain fibration]] $Func(\Delta[1], C) \to C$.  

This generalizes -- as discussed at [[deformation theory]] -- the classical example of the [[bifibration]] [[Mod]] $\to$ [[CRing]] of the category of all [[module]]s over the cateory [[CRing]] of all commutative rings: 

the fiber of the tangent $(\infty,1)$-category $T_C$ over an object $A \in C$ may be thought of as the $(\infty,1)$-category of **square-0-extensions** $A \oplus N$ of $A$, for $N$ a [[module]] over $A$. Dually, in $K = C^{op}$ we may think of these as being infinitesimal neighbourhoods of 0-sections of [[vector bundle]]s -- or rather of [[quasicoherent sheaves]] -- over whatever [[space]] $A$ is regarded to be the algebra of functions on.
 
A remarkable amount of information about the geometry of these spaces/objects in $K$ is encoded in the fiber of the tangent $(\infty,1)$-category over them. Notably the [[left adjoint|left]] [[adjoint (∞,1)-functor]] 

$$
  \Omega : C \to T_C
$$

to the domain projection $dom : T_C \to C$ turns out to send each $A$ to its [[cotangent complex]] $\Omega(A)$, to be thought of as the module of [[Kähler differential]]s on the space that $A$ is functions on.


## Definition

Let $C$ be a [[locally presentable (∞,1)-category]].

+-- {: .un_def}
###### Definition
**(fiberwise stabilization)**

For $C' \to C$ a [[model structure for quasi-categories|categorical fibration]], [[generalized the|the]] **fiberwise stabilization** $Stab(C' \to C)$ is -- roughly -- the fibration universal with the property that for each $A \in C$ its [[fiber]] over $A$ is the [[stabilization]] $Stab(C'_A)$ of the fiber $C'_A$ over $A$.


=--

This is [[Deformation Theory|DT, section 1.1]] formulated in view of [[Deformation Theory|DT, remark 1.1.8]]. There $Stab(C' \to C)$ is called the _stable envelope_ .

+-- {: .un_def}
###### Definition
**(tangent $(\infty,1)$-category)**

[[generalized the|The]] **tangent $(\infty,1)$-category** $T_C \to C$ [[generalized the|the]] _fiberwise stabilization_ of the [[codomain fibration]]  $cod : Func(\Delta[1], C) \to C$:

$$
  (T_C \stackrel{p}{\to} C) := Stab(Func(\Delta[1], C) \stackrel{cod}{\to} C  )
  \,.
$$

=--

This is [[Deformation Theory|DT, def 1.1.12]].

## Properties

+-- {: .un_prop}
###### Proposition

The tangent $(\infty,1)$-category $T_C$ of the [[locally presentable (∞,1)-category]] $C$ is itself a locally presentable $(\infty,1)$-category.

In particular, it admits all [[limit]]s and [[colimit]]s.

=--

+-- {: .proof}
###### Proof

This is [[Deformation Theory|DT, prop. 1.1.13]].

=--

## Cotangent complex

From its definition as the fiberwise stabilization of the [[codomain fibration]] $cod : Func(\Delta[1], C) \to C$ the tangent $(\infty,1)$-category $p : T_C \to C$ inherits a second $(\infty,1)$-functor to $C$, coming from the _domain_ evaluation

$$
  dom : T_C \to C
  \,.
$$ 

+-- {: .un_prop}
###### Definition/Proposition
**(cotangent complex)**

The domain evaluation $dom : T_C \to C$ admits a [[left adjoint|left]] [[adjoint (∞,1)-functor]]

$$
  (\Omega \dashv dom) : T_C \stackrel{\overset{\Omega}{\leftarrow}}{\underset{dom}{\to}}
  C
$$

that is also a [[section]] of $p : T_C \to C$ in that 

$$
  (C \stackrel{\Omega}{\to} T_C \stackrel{p}{\to} C) \simeq Id_C
$$ 

and hence that $C$ is a [[retract]] of $T_C$.

This $\Omega$ is the **cotangent complex $(\infty,1)$-functor** : for $A \in C$ the object $\Omega(A)$ is the [[cotangent complex]] of $A$.

=--

+-- {: .proof}
###### Proof

This is [[Deformation Theory|DT, def. 1.1.2, remark 1.2.3]].

=--


## References

The definition and study of the notion is tangent $(\infty,1)$-categories is from 

* [[Jacob Lurie]], _[[Deformation Theory]]_

[[!redirects tangent (infinity,1)-categories]]
[[!redirects tangent (∞,1)-category]]
[[!redirects tangent (∞,1)-categories]]
