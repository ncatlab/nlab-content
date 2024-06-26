
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

A _simplicial ring_ is a [[simplicial object]] in the [[category]] [[Ring]] of [[rings]].

This may be understood conceptually as follows:

* as ordinary rings are algebras over the ordinary [[algebraic theory]] $T$ of rings, if we regard this as an [[(∞,1)-algebraic theory]] then simplicial rings model the $(\infty,1)$-algebras over that;

* the category [[Ring]]${}^{op}$ is naturally equipped with the structure of a [[geometry (for structured (infinity,1)-toposes)|pregeometry]]. The corresponding [[geometry (for structured (∞,1)-toposes)]] is $sRing^{op}$, the opposite of the category of simplicial rings.



## Definition

A **simplicial ring** is a [[simplicial object]] in the [[category]] [[Ring]] of [[rings]].


## Properties

### Connected components

Given a simplicial ring $A = A_{\bullet}$, its [[connected components]] (the 0th "[[homotopy group]]")) is an ordinary [[ring]] 

$$
  \pi_0(A) \in Ring
  \,.
$$

Forming connected components is a [[functor]] from simplicial rings to plain rings, which is [[left adjoint]] to the inclusion of ordinary rings as simplicially constant simplicial rings, exhibiting a [[reflective subcategory]] inclusion

$$
  Ring \stackrel{\stackrel{\pi_0}{\longleftarrow}}{\hookrightarrow} Ring^{\Delta^{op}}
  \,.
$$

([To&#235;n 14, section 2.2](Toen14))

So on [[formal duals]] of [[commutative ring|commutative]] (simplicial) rings this is a [[coreflection]] of [[affine schemes]] in affine [[derived schemes]]

$$
  CRing^{op}
    \stackrel{\hookrightarrow}{\longleftarrow}
  (CRing^{\Delta^{op}})^{op}
  \,.
$$

Notice that coreflective embeddings are also given for instance by the inclusion of [[manifolds]] into [[formal manifolds]]. This is one way in which formal duals of simplicial rings manifest themselves as [[infinitesimal neighbourhoods]] of formal duals of plain rings.


### Higher homotopy groups

The higher [[homotopy groups]] $\pi_n(A)$ of a simplicial ring $A_\bullet$ are naturally [[modules]] over the ring $\pi_0(A)$ of connected components, so $A_\bullet$ is weakly [[contractible]], as a [[simplicial set]], iff $\pi_0(A)=0$.  

(Again this is a manifestation of the simplicial ring being just an infinitesimal thickening of its connected components.)

Notice that $\pi_0(A)$ is equivalently the [[cokernel]] of $d_0-d_1 \colon A_1 \longrightarrow A_0$.  Accordingly, any chain of [[face maps]] $A_n \longrightarrow A_0$ compose with the projection to $\pi_0(A)$ is independent of the choices.  These maps 

$$
  A_n \longrightarrow \pi_0(A)
$$

give a [[surjective]] map from $A_\bullet$ to the constant simplicial ring $\pi_0(A)$.  

(This is just the simplest piece of the [[Postnikov tower]].) If $\pi_0(A)\neq 0$ we can then compose with a surjective map to a constant simplicial field.


### Model category structure

There is a [[model category]] structure on simplicial rings that presents $\infty$-rings. See [[model structure on simplicial T-algebras]] for more.

We describe here the [[model category]] presentation of the [[(∞,1)-category]] of modules over simplicial rings.

Let $A$ be a simplicial commutative algebra. Write $A SMod$ for the [[category]] which, with $A$ regarded as a [[monoid]] in the category $SAb$ of abelian [[simplicial group]]s is just the category of $A$-[[module]]s in $SAb$. This means that


* objects are abelian [[simplicial group]]s $N$ equipped with 
  an [[action]] [[morphism]] $A \otimes N \to N$ of simplicial 
  abelian groups;

Equip $A SMod$ with the structure of a [[model category]] by setting:

* a morphism $N_1\to N_2$ of $A$-[[modules]] is a weak equivalence 
  resp. a fibration precisely if the  underlying morphism of [[simplicial set]]s is a
  weak equivalence, resp. fibration, in the standard 
  [[model structure on simplicial sets]].

**Proposition** This defines a [[model category]] structure which is

* [[cofibrantly generated model category|cofibrantly generated]];

* [[proper model category|proper]];

* [[cellular model category|cellular]].


## Examples

### Simplicial fields

All simplicial [[fields]] are simplicially constant.  This is because the composite $A_0\xrightarrow{s_0^n}A_n\xrightarrow{d_0^n}A_0$ is the identity, so $d_0^n$ is surjective, but all field homomorphisms are injective, so $d_0^n$ is an isomorphism.



## Related concepts

* [[simplicial algebra]]

* [[model structure on simplicial T-algebras]]

## References

Introduction and survey includes 

* [[Bertrand Toën]], chapter 4 of _Simplicial presheaves and derived algebraic geometry_ , lecture at [Simplicial methods in higher categories](http://www.crm.es/HigherCategories/)  ([pdf](http://www.crm.cat/HigherCategories/hc1.pdf))

* {#Toen14} [[Bertrand Toën]], _Derived Algebraic Geometry_ ([arXiv:1401.1044](http://arxiv.org/abs/1401.1044))


See [[model structure on simplicial algebras]] for references on the model structure discussed above.

Some of the above material is taken from <a href="http://mathoverflow.net/questions/45273/what-facts-in-commutative-algebra-fail-miserably-for-simplicial-commutative-rings">this MO entry</a>.

Discussion in the context of [[homotopy theory]], hence for simplicial [[ring spectra]] includes

* {#GoerssHopkins99} [[Paul Goerss]], [[Michael Hopkins]], _Simplicial Structured Ring Spectra_ (1999) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.34.9216))


[[!redirects simplicial rings]]
[[!redirects simplicial commutative ring]]
[[!redirects simplicial commutative rings]]
