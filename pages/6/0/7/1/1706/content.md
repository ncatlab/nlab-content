+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea 

The **Cobordism Hypothesis** states, roughly, that the [[(∞,n)-category of cobordisms]] $Bord_n$ is the 
[[free functor|free]] [[symmetric monoidal (∞,n)-category]] [[(∞,n)-category with duals|with duals]] on a single object.

Since a fully [[extended topological quantum field theory]] may be identified with an [[monoidal (∞,n)-functor|monoidal]] [[(∞,n)-functor]] $Z : Bord_n \to C$, this implies that all these [[TQFT]]s are entirely determined by their value on the point: "the [[n-vector space]] of [[state]]s" of the theory.



As motivation, notice that by [Galatius-Tillmann-Madsen- 09Weiss](cobordism+category#GMWT) we have that the [[loop space]] of the [[geometric realization]] of the [[framed manifold|framed]] [[cobordism category]] is equivalent to the [[sphere spectrum]]

$$
  \Omega \Vert Cob_d^{fr} \Vert
  \simeq
  \lim_{\to_{n \to \infty}} Maps_*(S^n, S^n)
  \simeq
  \Omega^\infty S^\infty
$$

which can be understood as the free [[infinite loop space]] on the point.



## Formalization 

In ([Lurie](#Lurie)) a formalization and proof of the cobordism hypothesis is described.

### For framed cobordisms
 {#ForFramed}

#### Statement

+-- {: .num_defn #FramedCobordismsNCat}
###### Definition

Let $C$ by a [[symmetric monoidal (∞,n)-category]] [[(∞,n)-category with duals|with duals]] and $Core(C)$ its [[core]] (the maximal [[∞-groupoid]] in $C$).

Let $Bord_n^{fr}$ be the [[symmetric monoidal (∞,n)-category|symmetric monoidal]] [[(∞,n)-category of cobordisms]] with [[framed manifold|n-framing]].

Finally let $Fun^\otimes(Bord_n^{fr} , C )$ be the [[(∞,n)-category]] of symmetric monoidal [[(∞,n)-functor]]s from bordisms to $C$.

=--


+-- {: .num_theorem #CobordismHypothesisFramedVersion}
###### Theorem (cobordism hypothesis, framed version)

Evaluation of any such functor $F$ on the [[point]] ${*}$

$$
  F \mapsto F({*})
$$

induces an [[(∞,n)-functor]]

$$
  pt^* : Fun^\otimes(Bord_n^{fr} , C ) \to C .
$$


such that

* this factors through the [[core]] of $C$;

* the map 

  $$
    pt^* : Fun^\otimes(Bord_n^{fr} , C ) \to Core(C)
  $$

  is an [[equivalence in an (∞,1)-category|equivalence]] of [[(∞,n)-categories]].


=--

This is ([Lurie, theorem 2.4.6](#Lurie)).


+-- {: .proof}
###### Proof

The proof is based on

1. the [[Galatius-Madsen-Tillmann-Weiss theorem]],  which characterizes the [[geometric realization]] $|Bord_n^{or}|$ in terms of the [[suspension]] of the [[Thom spectrum]];

1. Igusa's connectivity result which he uses to show that putting "framed [[Morse function]]s" on cobordisms doesn't change their [[homotopy type]] (theorem 3.4.7, page 73)

In fact, the Galatius-Madsen-Weiss theorem is now supposed to be a corollary of Lurie's result.

=--

#### Implications -- The canonical $O(n)$-∞-action
 {#TheCanonicalOnAction}

One of the striking consequences of theorem \ref{CobordismHypothesisFramedVersion} is that it implies that 

+-- {: .num_cor #CanonicalOnAction}
###### Corollary

Every [[∞-groupoid]] 

$$
  \mathcal{C}^{fd} \hookrightarrow \mathcal{C}
$$ 

of [[fully dualizable objects]] in a [[symmetric monoidal (∞,n)-category]] $\mathcal{C}$ carries a canonical [[∞-action]] of (the [[∞-group]] structure on the [[homotopy type]] of) the [[orthogonal group]] $O(n)$, induced by the action of $O(n)$ on the [[framed manifold|n-framing]] of the point in $Bord_n^{fr}$.

=--

([Lurie, corollary 2.4.10](#Lurie))

+-- {: .num_example #ExamplesOfTheCanonicalOnActions}
###### Example

The action in corollary \ref{CanonicalOnAction} is

* for $n = 1$: the $O(1) = \mathbb{Z}/2\mathbb{Z}$ action action given by passing to [[dual objects]];

* for $n = 2$ the $O(2)$-action the _[[Serre automorphism]]_.

* for $n = \infty$ the $O(n)$-action on [[n-fold loop spaces]] (see e.g. [Gaudens-Menichi 07, section 5](#GaudensMenichi07)) (see also at _[[orthogonal spectra]]_).

=--

([Lurie, examples 2.4.12, 2.4.14. 2.4.15](#Lurie))


### For cobordisms with extra topological structure
 {#CobsWithExtraTopStructure}

We discuss the cobordism hypothesis for cobordisms that are equipped with the extra [[structure]] of maps into some [[topological space]] equipped with a [[vector bundle]]. This is the case for which an [[extended TQFT]] is (the local refinement of) what has also been called an _[[HQFT]]_.

+-- {: .num_defn }
###### Definition

Let $X$ be a [[topological space]] and $\xi \to X$ a [[real number|real]] [[vector bundle]] on $X$ of [[rank]] $n$. Let $N$ be a [[smooth manifold]] of [[dimension]] $m \leq n$. An **$(X,\xi)$-structure** on $N$ consists of the following data

* A [[continuous function]] $f : N \to X$;

* An [[isomorphism]] of [[vector bundle]]s

  $$
    T N \oplus \mathbb{R}^{n-m} \simeq f^* \xi
  $$

  between the [[fiber]]wise [[direct sum]] of the [[tangent bundle]] $T N$ with the trivial rank $(n-m)$ bundle and the [[pullback]] of $\xi$ along $f$. 


=--

This is ([Lurie, notation 2.4.16](#Lurie)).

+-- {: .num_defn #CatOfCobordismsWithXIStructure}
###### Definition

Let $X$ be a [[topological space]] and $\xi \to X$ an $n$-[[dimensional]] [[vector bundle]]. The [[(∞,n)-category]] $Bord_n(X, \xi)$ is defined analogously to $Bord_n$ but with all manifolds equipped with $(X,\xi)$-structure.

=--

This is ([Lurie, def. 2.4.17](#Lurie)).

+-- {: .num_theorem #CobHypTheoremForTargetSpaceAndVectorBundle}
###### Theorem

Let $C$ be a [[symmetric monoidal (∞,n)-category]] with duals, let $X$ be a [[CW-complex]], let $\xi \to X$ be an $n$-[[dimensional]] [[vector bundle]] over $X$ equipped with an inner product, and let $\tilde X \to X$ be the [[associated bundle|associated]] [[orthogonal group|O(n)]]-[[principal bundle]] of orthonormal [[frame]]s in $\xi$. 

There is an [[equivalence in an (∞,1)-category|equivalence]] in [[∞Grpd]]

$$
  Fun^\otimes(Bord_n^{(X,\xi)}, C)
  \simeq
  Top_{O(n)}(\tilde X, \tilde C)
  \,,
$$ 

where on the right we regard $\tilde C$ as a [[topological space]] carrying the canonical $O(n)$-[[action]] discussed [above](#TheCanonicalOnAction).

=--

This is ([Lurie, theorem. 2.4.18](#Lurie)).


We consider some special cases of this general definition


#### For framed cobordisms in a topological space 
  {#StatementForCobordismsInAManifold}

We discuss the special case of the cobordism hypothesis for $(X,\xi)$-cobordisms (def. \ref{CatOfCobordismsWithXIStructure}) for the case that the vector bundle $\xi$ is the trivial vector bundle $\xi = \mathbb{R}^n \otimes X$. 


In this case $\tilde X = O(n) \times X$.  Write

$$
  Bord_n^{fr}(X) := Bord_n^{(X,X \times \mathbb{R}^n)}
  \,.
$$


Write $\Pi(X) \in $ [[∞Grpd]] for the [[fundamental ∞-groupoid]] of $X$.

+-- {: .num_prop }
###### Corollary

There is an [[equivalence in an (∞,1)-category|equivalence]] in [[∞Grpd]]

$$
  Fun^\otimes(Bord^{fr}_n(X), C)
  \simeq
  (\infty,n)Cat(\Pi(X), \tilde C)
  \simeq
   \infty Grpd(\Pi(X), Core(\tilde C))
  \,,
$$ 

=--

This is a special case of the [above theorem](#CobHypTheoremForTargetSpaceAndVectorBundle).

Notice that one can read this as saying that $Cob_n(X)$ is roughly like the [[free functor|free]] [[symmetric monoidal (∞,n)-category]] on the [[fundamental ∞-groupoid]] of $X$ (relative to $\infty$-categories of fully dualizable objects at least).



#### For cobordisms with $G$-structure
 {#CobordismsWithGStructure}

We discuss the special case of the cobordism hypothesis for $(X,\xi)$-bundles (def. \ref{CatOfCobordismsWithXIStructure}) for the special case that $X$ is the [[classifying space]] of a [[topological group]].

Let $G$ be a [[topological group]] equipped with a [[homomorphism]] $\chi : G \to O(n)$ to the [[orthogonal group]]. Notice that via the canonical linear [[representation]] $\mathbf{B}O(n) \to$ [[Vect]] of $O(n)$ on $\mathbb{R}^n$, this induces accordingly a representation of $G$ on $\mathbb{R}^n$..

Let then 

* $X := B G$ be the [[classifying space]] for $G$;

* $\xi_\chi := (\mathbb{R}^n \times_G E G $ be the corresponding [[associated bundle|associated vector bundle]] to the [[universal principal bundle]] $E G \to B G$.

+-- {: .num_defn }
###### Definition

We say

$$
  Bord^G_n := Bord_n^{(B G, \xi_\chi)}
  \,.
$$

is the $(\infty,n)$-category of **cobordisms with $G$-structure**.

=--

See ([Lurie, notation 2.4.21](#Lurie))

+-- {: .num_defn }
###### Definition

We have

* For $G = 1$ the trivial group, a $G$-structure is just a framing and so

  $$
    Bord_n^{(1,\xi)} \simeq Bord_n^{fr}
  $$

  reproduces the $(\infty,n)$-category of [[framed cobordisms]], def. \ref{FramedCobordismsNCat}.

* For $G = SO(n)$ the [[special orthogonal group]] equipped with the canonical embedding $\chi : SO(n) \to O(n)$ a $G$-structure is an [[orientation]]

  $$
    Bord_n^{(SO(n))} \simeq Bord_n^{or}
    \,.
  $$

* For $G = O(n)$ the [[orthogonal group]] itself equipped with the identity map $\chi : O(n) \to O(n)$ a $G$-structure is no structure at all,

  $$
    Bord_n^{O(n)} \simeq Bord_n
    \,.
  $$

=--

See ([Lurie, example 2.4.22](#Lurie)).

Then we have the following version of the cobordism hypothesis for manifolds with $G$-structure.

+-- {: .num_theorem #GEquivariantVersion}
###### Theorem

For $G$ an [[∞-group]] equipped with a homomorphism $G \to O(n)$ to the [[orthogonal group]] (regarded as an [[∞-group]] in [[∞Grpd]]), then evaluation on the point induces an equivalence

$$
  Fun^\otimes( Bord_n^{G}, \mathcal{C} )
  \simeq
  (\tilde {\mathcal{C}})^{G}
$$

between extended TQFTs on $n$-dimensional manifolds with [[G-structure]] and the [[∞-groupoid]] [homotopy invariants](invariant#ForInfinityGroupActions) of the [[infinity-action]] of $G$ on $\tilde \mathcal{C}$ (which is induced by the evaluation on the point).

=--

This is ([Lurie, theorem 2.4.26](#Lurie)).


#### For HQFTs
  {#ForHQFTs}

If in  def. \ref{CatOfCobordismsWithXIStructure} one chooses $X = B SO(n) \times Y$ for any topological space $Y$, and $\xi$ the [[pullback]] of the canonical vector bundle bundle on $B SO$ to $B SO \times Y$, then an $(\infty,n)$-functor $Bord^{X}_n \to C$ is similar to what Turaev calls an [[HQFT]] over $Y$.



### For cobordisms with singularities (boundaries/branes and defects/domain walls)
 {#ForCobordismsWithSingularities}

There is a vast generalization of the plain $(\infty,n)$-category of cobordisms (with topological structure) considered above given by allowing the [[cobordisms]] to be equipped with various types of [[singularities]] ([Lurie 09, Definition Sketch 4.3.2](#Lurie)).

Each type of singularity in dimension $k$ now corresponds to a new generator [[k-morphisms]], and the (framed) $(\infty,n)$-category of cobordisms with singularities is now no longer the free symmetric monoidal $(\infty,n)$-category freely generated from just a point (a 0-morphisms), but freely generated from these chosen generators. This general version is ([Lurie 09, Theorem 4.3.11](#Lurie)).

For instance if the generator on top of the point $\ast$ is a [[1-morphism]] of the form $\emptyset \to \ast$, then this defines a type of [[codimension]] $(n-1)$-[[boundary]]; and hence extended TQFTs with such boundary data and with coefficients in some symmetric monoidal $(\infty,n)$-category $\mathcal{C}$ with all dual are equivalent to choices of morphisms $1 \to A$, where $A \in \mathcal{C}$ is the fully dualizable object assigned to the point, as before, and now equipped with a morphism from the tensor unit into it.
Indeed, this is the usual datum that describes [[branes]] in QFT (see for instance at [[FRS formalism]]).

For more on this see at _[[QFT with defects]]_.

### For noncompact cobordisms
 {#ForNoncompactCobordisms}

One important variant of the category of cobordisms is obtained by discarding all those morphisms which have non-empty incoming (say, dually one could use outgoing) bounrary component. Then a representation of this category imposes on its values "cups but no caps", hence only half of the data of a [[dualizable object]] in the given degree. 

Accordingly, in this case the cobordism hypothesis says that such a functor is given not quite by a [[fully dualizable object]], but by a weaker structure called a _[[Calabi-Yau object]]_ (see there for more).

2-dimensional TQFT of this form is known as _[[TCFT]]_, see there for more



### For cobordisms with geometric structure

A non-topological [[quantum field theory]] is a representation of a [[cobordism category]] for cobordisms equipped with extra [[stuff, structure, property]] that is "not just topological", meaning roughly not of the form of def. \ref{CatOfCobordismsWithXIStructure}. 

The theory for this more general case is not as far developed yet. 

* steps towards classification of quantum field theories with _super-Euclidean structure_ are discussed at

  * [[(1,1)-dimensional Euclidean field theories and K-theory]]

  * [[(2,1)-dimensional Euclidean field theories and tmf]]

* a general definition of a [[cobordism category]] of cobordisms equipped with **geometric structure** given by a morphism into, roughly, a [[smooth infinity-groupoid]] of structure is discussed in  ([Ayala](#Ayala)).

## Remarks ##

### Morphisms of TQFTs

In particular this means that $Fun^\otimes(Bord_n^{fr} , C )$ is itself an $(\infinity,0)$-category, i.e. an [[∞-groupoid]].

When interpreting symmetric monoidal functors from bordisms to $C$ as [[TQFT]]s this means that TQFTs with given codomain $C$ form a [[topological space|space]], an [[∞-groupoid]]. In particular, any two of them are either equivalent or have no morphism between them.

According to [[Chris Schommer-Pries]] interesting morphisms of [[TQFT]]s arise when looking at transformations only on sub-categories on all of $Bord_n$. This is described at [[QFT with defects]] .


### Invariants determined from the point ###

The theorem does say that the invariant attached by an extended TQFT to the point determines all the higher invariants &#8211; however it is important to notice that there are strong constraints on what is assigned to the point. For an $n$-dimensional _framed_ theory one needs to assign a [[fully dualizable object]], and the meaning of the term "fully dualizable" depends on $n$, and gets increasingly hard to satisfy as n grows..

For an $n$-dimensional unoriented theory, the object assigned to the point has to be a fixed point for the $O(n)$- action on fully dualizable objects that is obtained from the framed case of the theorem. 

In the 1d case, this $O(1)$ action on dualizable objects takes every object to its dual, and an $O(1)$ fixed point is indeed a vector space with a nondegenerate symmetric inner product. 


For an _oriented_ theory $n$-dimensional theory need an $SO(n)$-fixed point, which for $n=1$ is nothing but for $n=2$ ends up meaning a [[Calabi-Yau category]] (in the case the target 2-category is that of categories).

In fact something more general is true: if one wants a theory that takes values on manifolds equipped with a $G$-structure, for $G$ any group mapping to $O(n)$ (such as for instance [[orientation]] already discussed or its higher versions [[Spin structure]] or [[String structure]] or [[Fivebrane structure]] or ...) one needs to assign to the point a $G$-fixed point in dualizable objects in your category (with $G$ acting through $O(n)$). 

This beautifully includes all the above plus for example [[manifold]]s with maps (up to [[homotopy]]) to some auxiliary (connected) space $X$ &#8211; here we take $G$ to be the [[loop space]] $\Omega X$  of $X$ (mapping trivially to $O(n)$), so that a reduction of the structure group of the manifold to $G$ involves a map to the [[delooping]] $\mathcal{B}G \simeq X$. 

Such theories are classified by $X$-families of fully dualizable objects. 

Notice that there is an important subtlety of Lurie's theorem in the case of manifolds with $G$-structure which is easy to confuse. The general version of the theorem about TFTs does not say that they are the $G$-fixed points for the $G$-action on fully dualizable objects, but rather they are the _homotopy_ fixed points. This is very important because a homotopy fixed point is not just a property. It is additional structure. Depending on $G$, this additional structure is often encoded in the higher dimensional portion of the field theory.

 One can see this in the 1 dimensional case: there is no property of vector spaces which automatically endows them with an inner product, but it is [[stuff, structure, property|extra structure]].

## Related concepts

* [[generalized tangle hypothesis]]

* [[conformal cobordism category]]

[[!include Isbell duality - table]]


## References 



The original hypothesis is formulated in 

*  [[John Baez]], [[James Dolan]], _Higher dimensional algebra and Topological Quantum Field Theory_ J.Math.Phys. 36 (1995) 6073-6105 ([arXiv:q-alg/9503002](http://arxiv.org/abs/q-alg/9503002))

The formalization and proof is described in 

* {#Lurie} [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_, Current Developments in Mathematics Volume 2008 (2009), 129-280 ([arXiv:0905.0465](http://arxiv.org/abs/0905.0465))


This is almost complete, except for one step that is not discussed in detail. But a new (unpublished) result by [[Søren Galatius]] bridges that step in particular and drastically simplifies the whole proof in general. 

The comparatively simple case of $n = 1$ is spelled out in detail in 

* [[Yonatan Harpaz]], _The Cobordism Hypothesis in Dimension 1_ ([arXiv:1210.0229](http://arxiv.org/abs/1210.0229))

Lecture notes and reviews on the topic of the cobordisms hypothesis include

* [[Jacob Lurie]], _TQFT and the Cobordism Hypothesis_ ([video](http://www.ma.utexas.edu/video/dafr/lurie/), [notes](http://www.ma.utexas.edu/users/plowrey/dev/rtg/notes/perspectives_TQFT_notes.html))

* [[Julie Bergner]], _[[UC Riverside Seminar on Cobordism and Topological Field Theories]]_  (2009).  

* [[Julie Bergner]], _Models for $(\infty,n)$-Categories and the Cobordism Hypothesis_ , in [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_, AMS 2011

* [[Daniel Freed]], _The cobordism hypothesis_ ([arXiv:1210.5100](http://arxiv.org/abs/1210.5100))

* {#Teleman14} [[Constantin Teleman]], _Five lectures on topological field theory_, 2014 ([pdf](http://math.berkeley.edu/~teleman/math/barclect.pdf))


Discussion of the canonical $O(n)$-action on [[n-fold loop spaces]] (which may be thought of as a special case of the cobordism hypothesis) includes

* {#GaudensMenichi07} Gerald Gaudens, Luc Menichi,  section 5 of _Batalin-Vilkovisky algebras and the $J$-homomorphism_, Topology and its Applications Volume 156, Issue 2, 1 December 2008, Pages 365&#8211;374 ([arXiv:0707.3103](http://arxiv.org/abs/0707.3103))


Cobordisms with geometric structure are discussed in

* [[David Ayala]], _Geometric cobordism categories_ ([pdf](http://www.math.ku.dk/~ayala/geombord.pdf))
{#Ayala}



[[!redirects cobordism theorem]]