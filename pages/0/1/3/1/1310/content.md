

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Recall that an $L_\infty$-[[Lie infinity-algebroid|algebroid]] is both a
[[horizontal categorification]] as well as a 
[[vertical categorification]] of a Lie algebra: it is
to Lie algebras as [[Lie ∞-groupoids]] are to Lie groups.

Accordingly, the notion of _representation of a Lie-$\infty$-algebroid_
is a horizontal and vertical categorification of the ordinary notion of
representation of a Lie algebra, which in turn is the linearization of
the notion of representation of a Lie group.

In view of this notice that 
there are essentially two fundamental ways to express the notion of
[[representation]] of a [[group]] or [[∞-groupoid]] $Gr$:

1. as a morphism out of $Gr$: the [[action]];

1. as a [[fibration sequence|fibration sequence]] over $Gr$: the [[action groupoid]].

While essentially equivalent, it is noteworthy that the first definition
naturally takes place in the context of not-necessarily smooth ($\infty$-)categories, 
while the second one usually remains within the context of smooth ($\infty$)-groupoids: 

namely for $G$ a Lie group, for definiteness and for simplicity, 
with corresponding one-object [[Lie groupoid]]
$\mathbf{B} G$ -- the [[delooping]] of the [[group]] $G$ --, a linear representation in terms of an action morphisms is a [[functor]]

$$
  \rho : \mathbf{B} G \to Vect
$$

from $\mathbf{B} G$ to the category of vector spaces. In fact, there is a
canonical equivalence of the [[functor category]] $[\mathbf{B}G, Vect]$ with the
category $Rep(G)$ of linear representations of $G$

$$
  [\mathbf{B}G, Vect] \simeq Rep(G)
  \,.
$$

Every such functor $\rho$ induces a [[fibration sequence]] $V//G \to \mathbf{B}G$ 
over $\mathbf{B}G$, obtained as
the [[pullback]] of the [[generalized universal bundle]]
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
rise to the [[fibration sequence|fiber sequence]]

$$
  V \hookrightarrow V//G \to \mathbf{B}G
  \,.
$$

As described at [[generalized universal bundle]], this may be thought of as
(the groupoid incarnation of) the vector bundle which is associated via $\rho$
to the universal $G$-bundle $\mathbf{E}G  \to \mathbf{B}G$, which itself 
is the [[action groupoid]] of the _[[fundamental representation]]_ of $G$ on itself,
$$
  \array{
     G &\hookrightarrow& \mathbf{E}G &\to& \mathbf{B}G
     \\
     = && = && =
     \\
     G &\hookrightarrow& G//G &\to& \mathbf{B}G
   }
   \,.
$$

From this perspective a representation of a group $G$ is 
nothing but a $G$-equivariant
vector bundle over the point, or equivalently a vector bundle on the
[[orbifold]] $\bullet//G$.
So from this perspective the notion "[[representation]]" is not a primitive
notion, but just a particular perspective on [[fibration sequences]].

The definition of Lie-$\infty$ algebroid representation below is in this
[[fibration sequence]]/[[fibration]]-theoretic/[[action groupoid]] spirit. 
The expected alternative definition in terms of
action morphisms has been considered (and is well known) apparently only
for special cases.



## Definition

### Representations

Recall that we take, by definition, [[Lie ∞-algebroids]] to be 
[[duality|dual]] to non-negatively-graded,  graded-commutative 
[[differential graded algebra|differential algebras]], which are
free as graded-commutative algebras (qDGCAs): we write
$CE_A(g)$ for the qDGCA whose underlying graded-commutative algebra
is the free (over the algebra $A$) graded commutative algebra
$\wedge^\bullet g^*$ for $g$ a non-postively graded cochain complex of
$A$-modules and $g^*$ its degree-wise dual over $A$, to remind us
that this is to be thought of as the Chevalley-Eilenberg algebra
of the [[Lie ∞-algebroid]] $g$ whose space of objects is characterized
dually by the algebra $A$.


**Definition**

A **representation** $\rho$ of a Lie $\infty$-algebroid $(g, A)$ on a 
co-chain complex $V$ of $A$-modules is a co[[fibration sequence]]

$$
  \wedge^\bullet V \leftarrow CE_\rho(g,V) \leftarrow CE_A(g)
$$

in DGCAs, i.e. a homotopy pushout

$$
  \array{
    \wedge^\bullet V &\leftarrow& CE_\rho(g)
    \\
    \uparrow && \uparrow
    \\
    0 &\leftarrow & CE_A(g)
  }
  \,.
$$

What has been considered in the literature so far is the more restrictive version, where the pushout is taken to be strict ([[Urs Schreiber|Urs]]: at least I think that this is the right way to say it):

A **proper representation** $\rho$ is a strict cofiber sequence of morphisms of DGCAs

$$
  \wedge^\bullet V \leftarrow CE_\rho(g,V) \leftarrow CE_A(g)
$$

i.e. such that 

* $CE_\rho(g,V) = CE_A(g) \otimes \wedge^\bullet V$ as GCAs

* $\wedge^\bullet V \leftarrow CE_\rho(g,V)$ is the obvious surjection;

* $CE_\rho(g,V) \leftarrow CE_A(g)$ is the obvious injection;

* the composite of both is the 0-map.

It follows that the differential $d_\rho$ on $CE_\rho(g,V)$ is given by
a **twisting map** $\rho^* : V \to (\wedge^\bullet V) \wedge (g^*) \wedge (\wedge^\bullet g^*)$ as

* $d_\rho|_{g^*} = d_g$

* $d_\rho|_{V} = d_V + \rho^*$

which may be thought of as the dual of the representation morphism (see the examples below).

### dg-Category of representations 

In [Block](#Block) the [[dg-category]] $Rep(g,A)$ of proper representations of a Lie-$\infty$-algebroid
$(g,A)$ in the above sense -- called dg-algebra modules there -- is defined.

**Definition**

Given two objects $CE_\rho(g,V)$ and $CE_{\rho'}(g,V')$
in $Rep(g,A)$, the cochain complex 

$Hom( CE_\rho(g,V),  CE_{\rho'}(g,V') )$

consist in degree $k$ of morphisms of degree $k$

$$
  \phi : V \otimes \wedge^\bullet g \to V' \otimes \wedge^\bullet g^*
$$

satisfying $\phi(v t) = (-1)^{k |a|} \phi(v) t$

and the differential $d_{Hom}$ is the usual differential on hom-complexes $d \phi = d_{\rho'} \circ \phi - (-1)^{|\phi|} \phi \circ d_\rho$.

For a fixed Lie $\infty$-algebroid $(g,A)$, the category 

$$
  Rep(g,A)
$$

with Lie representations of $(g,A)$ as objects and chain comoplexes as above as hom-objects is a [[dg-category]].


## Properties

### Relation to coherent complexes of sheaves 

**Theorem**

For $X$ a smooth complex manifold and $(g,A) = T_{hol} X$ the holomorphic tangent Lie algebroid
of $X$ (so that $CE_A(g) = \Omega^\bullet_{hol}(X)$ the holomorphic deRham complex of $X$), and for 
$Rep(T_{hol} X)$ taken to have as objects complexes of _finitely generated_ and _projective_ $C^\infty(X)$-modules (i.e. complexes of smooth vector bundles)
the [[homotopy category of an (infinity,1)-category|homotopy category]]
$Ho Rep(T_{hol} X)$ of the [[dg-category]] $Rep(T_{hol} X)$ is [[equivalence of categories|equivalent]]
to the _bounded derived category of complexes of sheaves with coherent cohomology_ on $X$
(see [[coherent sheaf]]).

This is [Block, theorem 2.22](#Block).

The objects of $Rep(T_{hol} X)$ are literally complexes of smooth vector bundles that are equipped with "half a flat connection", namely with a flat covariant derivative only along holomorphic tangent vectors. It is an old result that holomorphic vector bundles are equivalent to such smooth vector bundles with "half a flat connection". This is what the theorem is based on.





### Relation to D-modules 

For $(g,A) = T X$ the tangent Lie algebroid of a smooth manifold $X$, it should be true,
up to technicalities to be spelled out here eventually, that $Ho Rep(T X)$ is equivelent
to the derived category of [[D-modules]] on $X$, or the like.


## Examples

* ordinary representation of a Lie algebra on a vector space: $CE_\rho(g,V)$ is essentially the Chevalley-Eilenberg complex that computes the cohomology of $g$ with coefficients in $V$.

* flat connections on bundles

* [[adjoint representation]] of $L_\infty$-[[L-∞-algebras|algebras]]


## References

The general definition of representation of $\infty$-Lie algebroids as above appears in

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _Differential twisted string- and fivebrane structures_ (<a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSIII">web</a>)

The definition of the dg-category of representation of a tangent Lie algebroid and its equivalence in special cases to derived categories of complexes of coherent sheaves is in

* [[Jonathan Block]], _Duality and equivalence of module categories in noncommutative geometry I_
([arXiv](http://arxiv.org/abs/math/0509284))
{#Block}

For the case of Lie 1-algebroids essentially the same definition appears also in

* [[Camilo Arias Abad]], [[Marius Crainic]], _Representations up to homotopy of Lie algebroids_ ([arXiv](http://arxiv.org/abs/0901.0319))


The [[Lie integration]] of representations of Lie 1-algebroids $\mathfrak{a} \to end(V)$ to morphisms of [[∞-categories]] $A \to Ch_\bullet^\circ$ is discussed in

* [[Camilo Arias Abad]], [[Florian Schätz]], _The $A_\infty$ de Rham theorem and integration of representations up to homotopy_ ([arXiv:1011.4693](http://arxiv.org/abs/1011.4693))


[[!redirects Lie infinity-algebroid representations]]
[[!redirects Lie ∞-algebroid representation]]
[[!redirects Lie-∞ algebroid representation]]
[[!redirects Lie-∞ algebroid representations]]
[[!redirects Lie ∞-algebroid representations]]

[[!redirects representation up to homotopy]]
[[!redirects representations up to homotopy]]