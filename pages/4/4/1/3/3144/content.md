
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

A _simplicial ring_ is a [[simplicial object]] in the [[category]] [[Ring]] of [[ring]]s.

It may be understood conceptually as follows:

* as ordinary rings are algebras over the ordinary [[algebraic theory]] $T$ of rings, if we regard this as an [[(∞,1)-algebraic theory]] then simplicial rings model the $(\infty,1)$-algebras over that;

* the category [[Ring]]${}^{op}$ is naturally equipped with the structure of a [[geometry (for structured (infinity,1)-toposes)|pregeometry]]. The corresponding [[geometry (for structured (∞,1)-toposes)]] is $sRing^{op}$, the opposite of the category of simplicial rings.



## Definition

A **simplicial ring** is a [[simplicial object]] in the [[category]] [[Ring]] of [[ring]]s.

There is an evident notion of [[(∞,1)-category]] of [[module]]s over a simplicial ring. The corresponding [[bifibration]] $sMod \to sRing$ of modules over simplicial ring is equivalently to the [[tangent (∞,1)-category]] of the [[(∞,1)-category]] of simplicial rings.

## Properties

### Homotopy groups

Given a simplicial ring $A_\bullet$, it is standard that its connected components (the 0th "[[homotopy group]]") $\pi_0(A)$ is an ordinary ring and $\pi_n(A)$ is a module over it, so $A_\bullet$ is weakly [[contractible]] iff $\pi_0(A)=0$.  

Also, $\pi_0(A)$ is just the [[cokernel]] of $d_0-d_1:A_1\to A_0$.  We can take any chain of face maps $A_n\to A_0$ and compose with the projection to $\pi_0(A)$, and this will be independent of which chain we chose.  These maps $A_n\to\pi_0(A)$ give a [[surjective]] map from $A_\bullet$ to the constant simplicial ring $\pi_0(A)$.  

(This is just the simplest piece of the [[Postnikov tower]].) If $\pi_0(A)\neq 0$ we can then compose with a surjective map to a constant simplicial field.

All simplicial [[field]]s are constant.  This is just because the composite $A_0\xrightarrow{s_0^n}A_n\xrightarrow{d_0^n}A_0$ is the identity, so $d_0^n$ is surjective, but all field homomorphisms are injective, so $d_0^n$ is an isomorphism.

### Model category structure

There is a [[model category]] structure on simplicial rings that presents $\infty$-rings. See [[model structure on simplicial T-algebras]] for more.

We describe here the [[model category]] presentation of the [[(∞,1)-category]] of modules over simplicial rings.

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

## Related concepts

* [[simplicial algebra]]

* [[model structure on simplicial T-algebras]]

## References

An introduction is in chapter 4 of

* [[Bertrand Toën]], _Simplicial presheaves and derived algebraic geometry_ , lecture at [Simplicial methods in higher categories](http://www.crm.es/HigherCategories/)  ([pdf](http://www.crm.cat/HigherCategories/hc1.pdf))

Some of the above material is taken from <a href="http://mathoverflow.net/questions/45273/what-facts-in-commutative-algebra-fail-miserably-for-simplicial-commutative-rings">this MO entry</a>.

[[!redirects simplicial rings]]
