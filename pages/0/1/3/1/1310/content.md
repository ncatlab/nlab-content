
This entry discusses the conceptual notion of representations 
of Lie-infinity-algebroids and their realization in terms of
**modules for [[differential graded algebra]]s**
and of modules of [[differential graded coalgebra]]s. 
See the remarks at [[rational homotopy theory]] and
[[Lie theory]] for background on the Lie-theoretic interpretation
differential graded (co)algebra.

#Idea#

Recall that an [[Lie infinity-algebroid|L-infinity-algebroid]] is both a
[[horizontal categorification]] as well as a 
[[vertical categorification]] of a Lie algebra: it is
to Lie algebras as [[Lie infinity-groupoid]]s are to Lie groups.

Accordingly, the notion of _representation of a Lie-$\infty$-algebroid_
is a horizontal and vertical categorification of the ordinary notion of
representation of a Lie algebra, which in turn is the linearization of
the notion of representation of a Lie group.

In view of this notice that 
there are essentially two fundamental ways to express the notion of
representation of a [[group]] or [[infinity-groupoid]] $Gr$:

1. as a morphism out of $Gr$: the [[action]];

1. as a fibration over $Gr$: the [[action groupoid]].

While essentially equivalent, it is noteworthy that the first definition
naturally takes place in the context of not-necessarily smooth ($\infty$-)categories, 
while the second one usually remains within the context of smooth ($\infty$)-groupoids: 

namely for $G$ a [[Lie group]], for definiteness and for simplicity, 
with corresponding one-object Lie groupoid
$\mathbf{B}G$, a linear representation in terms of an action morphisms is a [[functor]]

$$
  \rho : \mathbf{B}G \to Vect
$$

from $\mathbf{B}G$ to the category of vector spaces. In fact, there is a
canonical equivalence of the [[functor category]] $[\mathbf{B}G]$ with the
category $Rep(G)$ of linear representations of $G$

$$
  [\mathbf{B}G, Vect] \simeq Rep(G)
  \,.
$$

Every such functor $\rho$ induces a [[fibration]] $V//G \to \mathbf{B}G$ 
over $\mathbf{B}G$, obtained by
the [[pullback]] of the [[universal Vect-bundle|generalized universal bundle]]
$Vect_* \to Vect$ along $\rho$

$$
  \array{
    V//G &\to& Vect_*
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G &\stackrel{\rho}{\to}& Vect
  }
  \,.
$$

Here $V//G$ is the [[action groupoid]] of the [[action]] of $\rho$ on the
representation vector space $V := \rho(\bullet)$, where $\bullet$ is the
single object of $\mathbf{B}G$. This vector space, regarded as a [[discrete category]]
on its underlying set, is the fiber of this fibration, so that the action gives
rise to the fiber sequence

$$
  V \hookrightarrow V//G \to \mathbf{B}G
  \,.
$$

As described at [[generalized universal bundle]], this may be thought of as
(the groupoid incarnation of) the vector bundle which is associated via $\rho$
to the universal $G$-bundle $\mathbf{E}G  \to \mathbf{B}G$, which itself 
is the [[action groupoid]] of the _fundamental representation_ of $G$ on itself,
$$
  \array{
     G &\hookrightarrow& \mathbf{E}G &\to& \mathbf{B}G
     \\
     = && = && =
     G &\hookrightarrow& G//G &\to& \mathbf{B}G
   }
   \,.
$$

From this perspective a representation of a group $G$ is 
nothing but a $G$-equivariant
vector bundle over the point, or equivalently a vector bundle on the
[[orbifold]] $\bullet//G$.
So from this perspective the notion "representation" is not a primitive
notion, but just a particular perspective on [[fibration sequence]]s.

The definition of Lie-infinity algebroid representation below is in this
[[fibration sequence]]/[[fibration]]-theoretic/[[action groupoid]] spirit. 
The expected alternative definition in terms of
action morphisms has been considered (and is well known) apparently only
for special cases.



#Definition#


Recall that we take, by definition, [[Lie infinity-algebroid]]s to be 
[[duality|dual]] to non-negatively-graded,  graded-commutative 
[[differential graded algebra|differential algebra]]s, which are
free as graded-commutative algebras (qDGCAs): we write
$CE_A(g)$ for the qDGCA whose underlying graded-commutative algebra
is the free (over the algebra $A$) graded commutative algebra
$\wegde^\bullet g^*$ for $g$ a non-postively graded cochain complex of
$A$-modules and $g^*$ its degree-wise dual over $A$, to remind us
that this is to be thought of as the Chevalley-Eilenberg algebra
of the Lie-infinity-algebra $g$ whose space of objects is characterized
dually by the algebra $A$.

The category DGCAs is naturally equipped with the 
[[model structure on DGCAs]]. 

**Definition**

A **representation** $\rho$ of a Lie $\infty$-algebroid $(g, A)$ on a 
co-chain complex $V$ is a [[fibration sequence]]

$$
  \wedge^\bullet V \leftarrow CE_\rho(g,V) \leftarrow CE_A(g)
$$

in DGCAs.

A **proper representation** $\rho$ is a strict fiber sequence of morphisms

$$
  \wedge^\bullet V \leftarrow CE_\rho(g,V) \leftarrow CE_A(g)
$$

i.e. such that 

* $CE_\rho(g,V) = CE_A(g) \otimes \wedge^\bullet V$ as GCAs

* $\wedge^\bullet V \leftarrow CE_\rho(g,V)$ is the obvious surjection;

* $CE_\rho(g,V) \leftarrow CE_A(g)$ is the obvious injection;

* the composite of both is the 0-map.

It follows that the differential $d_\rho$ on $CE_\rho(g,V)$ is given by
a "twisting map" $\rho^* : V \to \wedge^\bullet V \wedge g^* \wedge \wedge^\bullet g^*$ as

* $d_\rho|_{g^*} = d_g$

* $d_\rho|_{V} = d_V + \rho^*$

which may be thought of as the representation morphism.

# DG-category of Lie-infinity-algebroid representations #

In 

* Jonathan Block, _Duality and equivalence of module categories in noncommutative geometry I_
([arXiv]())

the [[dg-category]] $Rep(g,A)$ of proper representations of a Lie-infinity-algebroid
$(g,A)$ in the above sense -- called dg-algebra modules there -- is defined.



## relation to coherent complexes of sheaves ##


**Theorem**

For $X$ a smooth complex manifold and $(g,A) = T_{hol} X$ the holomorphic tangent Lie algebroid
of $X$ (so that $CE_A(g) = \Omega^\bullet_{hol}(X)$ the holomorphic deRham complex of $X$), 
the [[homotopy category of an (infinity,1)-category|homotopy category]]
$Ho Rep(T_{hol} X)$ of the [[dg-category]] $Rep(T_{hol} X)$ is [[equivalence of categories|equivalent]]
to the _bounded derived category of complexes of sheaves with coherent cohomology_ on $X$
(see [[coherent sheaf]]).

This is theorem 2.22, p. 17 of Block's article.







## relation to D-modules ##

For $(g,A) = T X$ the tangent Lie algebroid of a smooth manifold $X$, it should be true,
up to technicalities to be spelled out here eventually, that $Ho Rep(T X)$ is equivelent
to the derived category of [[D-module]]s on $X$, or the like.


#Examples#


#References#

The definition of the dg-category of dg-algebra modules and its
equivalence in special cases to derived categories of coherent complexes of sheaves is
in

* Jonathan Block, _Duality and equivalence of module categories in noncommutative geometry I_
([arXiv](http://arxiv.org/abs/math/0509284))

A blog discussion of this is at

* Urs Schreiber,  [Block on L-infinity Module Categories](http://golem.ph.utexas.edu/category/2008/06/block_on_loo_module_categories.html)

Some further discussion and examples of Lie-infinity-algebroid representations is at

* Urs Schreiber, [On Lie-infinity theory](http://golem.ph.utexas.edu/category/2008/05/action_lie_infinityalgebroids.html)

* Hisham Sati, Urs Schreiber, Jim Stasheff, _Twisted differential String- and Fivebrane structures_ ([pdf](http://www.math.uni-hamburg.de/home/schreiber/5twist.pdf))