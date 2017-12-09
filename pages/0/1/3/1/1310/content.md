

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

This entry discusses [[∞-actions]]/[[∞-representations]] of [[Lie-infinity algebroids]] (generalizing [[Lie algebra actions]]), hence the [[infinitesimal object|infinitesimal]] version of [[∞-actions]] of [[smooth ∞-groupoids]].

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


+-- {: .num_defn}
###### Definition

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

=--

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

In ([Block 05](#Block05)) the [[dg-category]] $Rep(g,A)$ of proper representations of a Lie-$\infty$-algebroid
$(g,A)$ in the above sense -- called _dg-algebra modules_ there -- is defined.

+-- {: .num_defn}
###### Definition

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

=--

## Examples

### Basic

+-- {: .num_example}
###### Example

For an n ordinary [[Lie algebra representation]] $\rho$ on a vector space $V$ consider the [[Chevalley-Eilenberg algebra]] $CE_\rho(g,V)$ that computes the [[Lie algebra cohomology]] of $\mathfrak{g}$ with [[coefficients]] in $V$. This exhibits the action in the above sense.

=--

+-- {: .num_example #ActionOfTangentLieAlgebroid}
###### Example

A [[flat connections]] on a [[vector bundle]] exhibits a representation of the [[tangent Lie algebroid]] of the base manifold.

=--

A holomorphic variant of this is [below](#ActionOfHolomorphicTangentAlgebroid).

* (...) [[adjoint representation]] of $L_\infty$-[[L-∞-algebras|algebras]]


### Action of holomorphic tangent Lie algebroid on chain complexes of complex vector bundles
  {#ActionOfHolomorphicTangentAlgebroid}

The following variant of example \ref{ActionOfTangentLieAlgebroid} is a [[homotopy theory|homotopy-theoretic]]-refinement of the classical [[Koszul-Malgrange theorem]].

+-- {: .num_theorem}
###### Theorem

For $X$ a [[smooth manifold|smooth]] [[complex manifold]] and $(g,A) = T_{hol} X$ the holomorphic [[tangent Lie algebroid]]
of $X$ (so that $CE_A(g) = \Omega^\bullet_{hol}(X) = \Omega^{\bullet,0}(X)$ the holomorphic part of the [[Dolbeault complex]] of $X$), and for 
$Rep(T_{hol} X)$ taken to have as objects complexes of _finitely generated_ and _projective_ $C^\infty(X)$-modules (i.e. complexes of smooth [[vector bundles]]) 
the [[homotopy category of an (infinity,1)-category|homotopy category]]
$Ho Rep(T_{hol} X)$ of the [[dg-category]] $Rep(T_{hol} X)$ is [[equivalence of categories|equivalent]]
to the _bounded [[derived category]] of [[chain complexes]] of [[abelian sheaves]] with [[coherent cohomology]]_ on $X$
(see at _[[coherent sheaf]]_).

=--

This is ([Block 05, theorem 2.22](#Block05) (in the counting of version 1 on the arXiv!)).

The objects of $Rep(T_{hol} X)$ are literally complexes of smooth vector bundles that are equipped with "half a flat connection", namely with a flat covariant derivative only along holomorphic tangent vectors. It is an old result that [[holomorphic vector bundles]] (see there) are equivalent to such smooth vector bundles with "half a flat connection". This is what the theorem is based on.


### Extensions of $L_\infty$-algebras
 {#Extensions}

+-- {: .num_example}
###### Example

For $\mathfrak{g}$ any [[L-∞ algebra]], and $\mathfrak{a}$ any other,then an [L-∞ extension](infinity-Lie+algebra+cohomology#Extensions) (see there) $\hat {\mathfrak{g}}$ of $\mathfrak{g}$ by $\mathfrak{a}$ is a [[homotopy fiber sequence]]

$$
  \mathfrak{a} \to \hat {\mathfrak{g}} \to \mathfrak{g}
$$

of [[L-∞ algebras]] (see at _[[model structure for L-∞ algebras]]_). Regarding this as sequence of [[L-∞ algebroids]] over the point

$$
  \mathbf{B}\mathfrak{a} \to \mathbf{B}\hat {\mathfrak{g}} \to \mathbf{B}\mathfrak{g}
$$

and then passing to [[Chevalley-Eilenberg algebras]], this exhibits an action/representation of the $L_\infty$-algebra $\mathfrak{g}$ on the $L_\infty$-algebroid $\mathbf{B}\mathfrak{a}$.

=--

For instance the [[string Lie 2-algebra]] is the $\mathbf{B} \mathbb{R}$-extension of a semisimple [[Lie algebra]] $\mathfrak{g}$ with bilinear [[invariant polynomial]] $\langle -,-\rangle$ corresponding to the 3-cocycle $\langle -,[-,-]\rangle \in CE(\mathfrak{g})$, hence exhibits an action/representation of $\mathfrak{g}$ on $\mathbf{B}\mathbb{R}$. This is the infinitesimal version of the [[∞-action]] of a simply connected compact simple [[Lie group]] $G$ on the [[circle 2-group]] $\mathbf{B}U(1)$ which exhibits the [[String 2-group]] extension.

Analogous statements in various degrees hold for the $L_\infty$-algebra [[Fivebrane 6-group]]

$$
  \mathbf{B}^6 \mathbb{R} \to \mathfrak{fivebrane}\to \mathfrak{string}
$$

exhibiting an $\infty$-action of the [[string Lie 2-algebra]] on $\mathbf{B}^7 \mathbb{R}$, and analogously for the [[supergravity Lie 3-algebra]], the [[supergravity Lie 6-algebra]] and for all the other extensions in [[schreiber:The brane bouquet]].


## Relations to (co-)modules over the CE (co-)algebra

Under identifying [[L-infinity algebras]] with graded (co-)commutative [[dg-coalgebras]]/[[dg-algebras]] (their [[Chevalley-Eilenberg algebras]]) then their representations correspond to dg-(co-)modules whose underlying graded (co-)algebras are (co-)free. See at

* [[model structure on dg-comodules]]

* [[model structure on dg-modules]]



## References
 {#References}

The definition of representation of $L_\infty$-algebras is discussed in section 5 of

* [[Tom Lada]], [[Martin Markl]], _Strongly homotopy Lie algebras_ ([arXiv:9406095](http://arxiv.org/abs/hep-th/9406095))


The general definition of representation of $\infty$-Lie algebroids (of [[finite type]]) as above appears as def. 4.9 in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _Differential twisted string- and fivebrane structures_ ([arXiv:0910.4001 version 1](http://arxiv.org/abs/0910.4001v1))

(this discussion is not in the published version [arXiv:0910.4001v2](http://arxiv.org/abs/0910.4001v2), for size reasons)

modeled after the geneal abstract definition of [[∞-actions]] in 

* [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications]]_, Journal of Homotopy and Related Structures, 2014 ([arXiv:1207.0248](http://arxiv.org/abs/1207.0248))

The definition of the dg-category of representation of a tangent Lie algebroid and its equivalence in special cases to derived categories of complexes of coherent sheaves is in

* {#Block05} [[Jonathan Block]], _Duality and equivalence of module categories in noncommutative geometry I_ ([arXiv:0509284](http://arxiv.org/abs/math/0509284))

Application of this to the description of [[B-branes]] is in 

* {#Bergman08} [[Aaron Bergman]], _Topological D-branes from Descent_ ([arXiv:0808.0168](http://arxiv.org/abs/0808.0168))


For the case of Lie 1-algebroids essentially the same definition appears also in

* [[Camilo Arias Abad]], [[Marius Crainic]], _Representations up to homotopy of Lie algebroids_ ([arXiv](http://arxiv.org/abs/0901.0319))


The [[Lie integration]] of representations of Lie 1-algebroids $\mathfrak{a} \to end(V)$ to morphisms of [[∞-categories]] $A \to Ch_\bullet^\circ$ is discussed in

* [[Camilo Arias Abad]], [[Florian Schätz]], _The $A_\infty$ de Rham theorem and integration of representations up to homotopy_ ([arXiv:1011.4693](http://arxiv.org/abs/1011.4693))


[[!redirects representation of an ∞-Lie algebroid]]
[[!redirects representations of ∞-Lie algebroids]]

[[!redirects L-∞ algebroid representation]]
[[!redirects L-∞ algebroid representations]]
[[!redirects L-infinity algebroid representation]]
[[!redirects L-infinity algebroid representations]]


[[!redirects Lie infinity-algebroid representations]]
[[!redirects Lie ∞-algebroid representation]]
[[!redirects Lie-∞ algebroid representation]]
[[!redirects Lie-∞ algebroid representations]]
[[!redirects Lie ∞-algebroid representations]]

[[!redirects representation up to homotopy]]
[[!redirects representations up to homotopy]]

[[!redirects ∞-Lie algebroid representation]]
[[!redirects ∞-Lie algebroid representations]]

[[!redirects L-∞ algebra action]]
[[!redirects L-∞ algebra actions]]

[[!redirects L-infinity algebra action]]
[[!redirects L-infinity algebra actions]]

