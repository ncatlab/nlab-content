
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* automatic table of contents
{:toc}

## Idea

A _simplicial ring_ is a [[simplicial object]] in the [[category]] [[Ring]] or [[ring]]s.

It may be understood conceptually as follows:

* as ordinary rings are algebras over the orrdinary [[algebraic theory]] $T$ of rings, if we regard this as an [[(?1)-algebraic theory]] then simplicial rings model the $(\infty,1)$-algebras over that;

* the category [[Ring]]${}^{op}$ is naturally equipped with the structure of a [[geometry (for structured (infinity,1)-toposes)|pregeometry]]. The corresponding [[geometry (for structured (∞,1)-toposes)]] is $sRing^{op}$, the opposite of the category of simplicial rings.



## Definition

A **simplicial ring** is a [[simplicial object]] in the [[category]] [[Ring]] of [[ring]]s.

## Modules over simplicial rings

There is an evident notion of [[(∞,1)-category]] of [[module]]s over a simplicial ring. The corresponding [[bifibration]] $SMod \to SRing$ of modules over simplicial ring has the remarkable property that it is equivalently to that [[tangent (∞,1)-category]] of the [[(∞,1)-category]] of simplicial rings.

### Model category presentation {#ModelCatOnSimplicialModules}

We describe the [[model category]] presentation of the [[(∞,1)-category]] of modules over simplicial rings.

Let $A$ be a simplicial commutative algebra. Write $A SMod$ for the [[category]] which, with $A$ regarded as a [[monoid]] in the category $SAb$ of abelian [[simplicial group]]s is just the category of $A$-[[module]]s in $SAb$. This means that


* objects are abelian [[simplicial group]]s $N$ equipped with 
  an [[action]] [[morphism]] $A \otimes N \to N$ of simplicial 
  abelian groups;

Equip $A SMod$ with the structure of a [[model category]] by setting:

* a morphism $N_1\to N_2$ of $A$-[[module]]s is a weak equivalence 
  resp. a fibration
  precisely if the  underlying morphism of [[simplicial set]]s is a
  weak equivalence, resp. fibration, in the standard 
  [[model structure on simplicial sets]].

**Proposition** This defines a [[model category]] structure which is

* [[cofibrantly generated model category|cofibrantly generated]];

* [[proper model category|proper]];

* [[cellular model category|cellular]].


## In higher geometry

Simplicial rings are one notion of [[vertical categorification]] of [[rings]], another generalization is [[E-infinity-ring]]s. As such, simplicial rings come with their notion of [[higher geometry]], in particular their notion of [[derived scheme]]s, [[derived stack]]s and [[quasicoherent sheaf|quasicoherent sheaves]]. An application of this appears for instance in [[geometric infinity-function theory]].

## References

For instance chapter 4 of

* [[Bertrand Toen]], _Simplicial presheaves and derived algebraic geometry_ , lecture at [Simplicial methods in higher categories](http://www.crm.es/HigherCategories/)  ([pdf](http://www.crm.cat/HigherCategories/hc1.pdf))

[[!redirects simplicial algebra]]