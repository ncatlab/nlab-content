+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
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
 {#Idea}

### Plain cobordism hypothesis

What is known as the *Cobordism Hypothesis* is, in its most basic form, the [[conjecture]] that, roughly, the [[(∞,n)-category of cobordisms]] $Bord_n^{fr}$ with [[framed manifold|framing]] is [[equivalence|equivalently]] the  [[free construction|free]] [[symmetric monoidal (∞,n)-category]] [[(∞,n)-category with duals|with duals]] on a single [[object]].

The idea is due to [Baez & Dolan (1995)](#BaezDolan95), who stated it in the further generality of [[k-tuply monoidal n-category|$k$-tuply monoidal $n$-categories]] (i.e. for $k \leq \infty$) under the name *[[Tangle Hypothesis]]* ([p. 23](https://arxiv.org/pdf/q-alg/9503002.pdf#page=23)), before definitions of these [[higher category theory|higher category theoretical]] notions were available. The term "cobordism hypothesis" is used by Baez and Dolan only in passing and without definition ([p. 25](https://arxiv.org/pdf/q-alg/9503002.pdf#page=25)) but was popularized by [Lurie (2009)](#Lurie09) who gave a detailed though still incomplete sketch of a [[proof]] by appeal to the notion of [[n-fold complete Segal space|$n$-fold complete Segal spaces]] as a [[geometric definition of higher categories]], thereby breaking the impasse caused by previous attempts (e.g. [tac:18-10](http://www.tac.mta.ca/tac/volumes/18/10/18-10abs.html)) which instead tried [[algebraic definitions of higher categories]].

Since a (framed) fully [[extended topological quantum field theory]] (TQFT) may be identified with a symmetric [[monoidal (∞,n)-functor|monoidal]] [[(∞,n)-functor|$(\infty,n)$-functor]] $Z \colon Bord^{fr}_n \to \mathcal{C}^\otimes$, the cobordism hypothesis implies (and should be implied by, via a higher [[Yoneda lemma]]) that [[fully extended TQFTs]] are entirely determined by their value on the point (the "[[n-vector space]] of [[states]]" of the theory), and conversely that [[fully dualizable objects]] in $\mathcal{C}^{\otimes}$ [[equivalence|equivalently]] encode such fully extended TQFTs. As such the hypothesis is actually called the "*Extended TQFT Hypothesis*" by [Baez & Dolan (1995)](#BaezDolan95) ([p. 28](https://arxiv.org/pdf/q-alg/9503002.pdf#page=28)).

From the cobordism hypothesis for [[framed manifold|framing]] structure it follows fairly readily that the [[infinity-groupoid|$\infty$-groupoid]] of [[fully dualizable objects]] in a symmetric monoidal $(\infty,n)$-category carries an [[group action|action]] of the [[orthogonal group]] $O(n)$ and that cobordisms with [[tangential structure|tangential]] [[G-structure]] for $G \hookrightarrow O(n)$ are similarly classified by the [[homotopy fixed points|homopy fixed loci]] of the [[restricted action|corresponding]] $G$-action &lbrack;[Lurie (2009, Thm. 2.4.26)](#Lurie09)&rbrack;. This yields the statement of the hypothesis for common notions of cobordisms, such as with [[orientation]] ([[SO(n)]][[G-structure|-structure]]), [[spin structure]] ([[Spin(n)]][[G-structure|-structure]]), etc.

The idea of the cobordism hypothesis is that:

1. [[cylinders]] count as trivial ([[identity morphism|identity]]) [[cobordisms]] between their [[boundary]] components, corresponding to how local [[spacetime]]-evolution in a [[topological quantum field theory]] is trivial (corresponding to the physics jargon that "their [[Hamiltonian]] vanishes"),

1. so that all the non-trivial information in [[cobordism]] and in [[TQFT]]-propagation is in the structure of [[handle body]]-attachments (in physics known as: "topology change") which obey the [[triangle identity|zig-zag rules]] [known from](adjunction#InTermsOfStringDiagrams) [[adjunctions]], [[2-adjunctions]] and their further higher dimensional analogs,

1. which means that the point -- regarded as a 0-dimensional element of an $n$-dimensional [[cobordism]] -- is equipped with the [[structure]] of, first of all, a [[dualizable object]] under the relevant [[tensor product]] of cobordisms (which is [[disjoint union]]), and next that of a $k$-dualizable object for all $k \leq n$.

### Geometric cobordism hypothesis
 {#GeometricCobordismHypothesis}

More generally, the *geometric* cobordism hypothesis &lbrack;[Grady & Pavlov (2021)](#GradyPavlov21)&rbrack; asserts that general non-topological *geometric* [[functorial field theory|extended functorial field theories]] (such as [[conformal field theory]] as well as the usual [[relativistic quantum field theory|relativistic]] [[AQFT on curved spacetimes|QFT on curved spacetimes]]) are similarly encoded by (1.) local data depending only on the notion of geometry and (2.)  global topological data encoded only in higher dualizability structure.

For example, the [[FRS-theorem on rational 2d CFT]] is, at least in spirit, a realization of this idea: It states that [[rational CFT|rational]] [[2d conformal field theories]], when defined on all possible [[worldsheet]] [[surfaces]], are fully encoded (1.) by local geometric data encoded in [[vertex operator algebras]] or [[conformal nets]] or similar and (2.) global purely topological data (a suitable [[Frobenius algebra|Frobenius]] [[algebra object]] [[internalization|internal to]] the [[modular tensor category]] [[representation category|of representations]] of that [[vertex operator algebra]]/[[conformal net]]).

Conversely, the plain (topological) cobordism hypothesis is the special case of the geometric cobordism hypothesis of no geometric structure and in this sense very much captures the idea which in physics is known as "TQFTs are those QFTS without local degrees of freedom".

In general, where the notion of extended (geometric) [[functorial field theory]] is one candidate for a definition of (non-topological) [[non-perturbative quantum field theory]], the (geometric) cobordism hypothesis may be regarded as the first step in establishing the construction of such theories, reducing the problem entirely to the local behaviour of the theory. 

Notice that the local behaviour of [[quantum field theory]] is still immensely rich: It keeps busy quantum field theorists most of whom never encounter a topological effect in their life. For example the original statement of the [[Wightman axioms]]/[[Haag-Kastler axioms]] are entirely concerned only with the local behaviour of Lorentzian QFTs (namely on [[Minkowski spacetime]]) and yet the construction of any non-trivial examples in dimensions $d \geq 4$ remains wide open.

In this vein, much in the spirit of [Freyd's dictum](category+theory#WhatIsTriviallyTrivial) on the role of [[categorical algebra]] in general, one may read the (geometric) cobordism hypothesis as trivializing the trivial part of [[non-perturbative quantum field theory]]. 

A proof of the geometric cobordism hypothesis is thus the important first step towards the [currently wide-open and yet crucial problem](mass+gap#ReferencesMassGapProblem) of mathematically constructing [[non-perturbative quantum field theories]].




## Formalization 

In &lbrack;[Lurie 2009](#Lurie09)&rbrack; a sketch of an approach to the formalization and proof of the cobordism hypothesis is described.

### For framed cobordisms
 {#ForFramed}

#### Statement

For $\mathcal{C}$ a [[symmetric monoidal (∞,n)-category with duals]] write $Core(\mathcal{C})$ for its [[core]] (the maximal [[∞-groupoid]] in $\mathcal{C}$).

For $\mathcal{C}$, $\mathcal{D}$ two [[symmetric monoidal (∞,n)-categories]], write   $Fun^\otimes(\mathcal{D}, \mathcal{C} )$ for  the [[(∞,n)-category]] of symmetric monoidal [[(∞,n)-functors]] between them.


+-- {: .num_defn #FramedCobordismsNCat}
###### Definition


Let $Bord_n^{fr}$ be the [[symmetric monoidal (∞,n)-category|symmetric monoidal]] [[(∞,n)-category of cobordisms]] with [[framed manifold|n-framing]].


=--


+-- {: .num_theorem #CobordismHypothesisFramedVersion}
###### Theorem (cobordism hypothesis, framed version)

Evaluation of any such functor $F$ on the [[point]] ${*}$

$$
  F \mapsto F({*})
$$

induces an [[(∞,n)-functor]]

$$
  pt^* : Fun^\otimes(Bord_n^{fr} , \mathcal{C} ) \to \mathcal{C} .
$$


such that

* this factors through the [[core]] of $\mathcal{C}$;

* the map 

  $$
    pt^* \;\colon\; Fun^\otimes(Bord_n^{fr} , \mathcal{C} ) \to Core(\mathcal{C})
  $$

  is an [[equivalence in an (∞,1)-category|equivalence]] of [[(∞,n)-categories]].


=--

This is ([Lurie 2009, theorem 2.4.6](#Lurie09)).


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

* for $n = 1$: the $O(1) = \mathbb{Z}/2\mathbb{Z}$ action given by passing to [[dual objects]];

* for $n = 2$: the $O(2)$-action of the _[[Serre automorphism]]_.

* for $n = \infty$: the $O(n)$-action on [[n-fold loop spaces]] (see e.g. [Gaudens-Menichi 07, section 5](#GaudensMenichi07)) (see also at _[[orthogonal spectra]]_).

=--

([Lurie, examples 2.4.12, 2.4.14. 2.4.15](#Lurie))

+-- {: .num_prop #CanonicalSOActionOnBnZ}
###### Proposition

For all $n \in \mathbb{N}$, the canonical $SO$-[[∞-action]] on 

$$
  B^n \mathbb{Z} \in Ab_\infty(\infty Grpd) \hookrightarrow (\infty,n)CatWithDuals
$$

is trivial.

=--

+-- {: .proof }
###### Proof

The action on a [[connective spectrum]] $\Omega^\infty X$ factors through the [[J-homomorphism]]

$$
  SO \times \Omega^\infty X
  \stackrel{(J,id)}{\longrightarrow}
  \Omega^\infty S^\infty \times \Omega^\infty X
  \stackrel{precomp}{\longrightarrow}
  \Omega^\infty X
  \,.
$$

But on [[homotopy groups]] the [[image of J]] is pure [[torsion]] which means that for $\Omega^\infty X = B^n \mathbb{Z}$ the induced actions on homotopy groups are all trivial. From this and using the [[long exact sequence of homotopy groups]] it follows that the $\infty$-action itself is trivial.

=--


### For cobordisms with extra topological structure
 {#CobsWithExtraTopStructure}

We discuss the cobordism hypothesis for cobordisms that are equipped with the extra [[structure]] of maps into some [[topological space]] equipped with a [[vector bundle]]. This is the case for which an [[extended TQFT]] is (the local refinement of) what has also been called an _[[HQFT]]_.

#### For cobordisms with any structure ("$(X,\xi)$-structure")
 {#ForCobordismsWithXXiStructure}

+-- {: .num_defn #XXiStructure}
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

The two extreme cases of def. \ref{XXiStructure} are the following

+-- {: .num_example #FramingAsXXiStructur}
###### Example

For $X = \ast$ the point and $\xi = \mathbb{R}^n$, then an $(X,\xi)$-structure is the same as an $n$-[[framing]], hence

$$
  (Bord_n^{(\ast, \mathbb{R}^n)})
  \simeq
  Bord_n^{fr}
$$ 

reproduces the $(\infty,n)$-category of framed cobordisms of def. \ref{FramedCobordismsNCat}.

=--

+-- {: .num_example #UnorientedAsXXiStructur}
###### Example

For $X = $[[BO(n)|$B O(n)$]] the [[classifying space]] of real [[vector bundles]] of [[rank]] $n$ (the [[delooping]] of the [[∞-group]] $O(n)$ underlying the [[orthogonal group]]) and for $\xi = E O(n) \underset{O(n)}{\times} \mathbb{R}^n$ the vector bundle [[associated bundle|associated]] to the $O(n)$-[[universal bundle]], then $(X,\xi)$-structure on $n$-dimensional manifolds is essentially _no_-structure (the [[maximal compact subgroup]]-inclusion $O(n)\to GL(n)$ is a [[weak homotopy equivalence]]). Cobordisms with this structure will also be called _unoriented cobordisms_

$$
  Bord_n^{un} \coloneqq Bord_n^{(B O(n), E O(n)\underset{O(n)}{\times} \mathbb{R}^n)}
  \,.
$$

Accordingly, for $X = B SO(n)$ the [[delooping]] of the [[special orthogonal group]], the corresponding $(X,\xi)$-structure makes _oriented manifolds_

$$
  Bord_n^{or} \coloneqq Bord_n^{(B SO(n), E SO(n)\underset{SO(n)}{\times} \mathbb{R}^n)}
  \,.
$$

=--

Generally: 

+-- {: .num_example #GStructureAsXXiStructure}
###### Example

For $\chi \colon G \to O(n)$ a [[topological group]] mapping via a [[homomorphism]] to $O(n)$, then $X = B G$ and $\xi = \chi^\ast (E O(n)\underset{O(n)}{\times} \mathbb{R}^n)$, the $(X,\xi)$-structure is [[G-structure]].

This we get to [below](#CobordismsWithGStructure).

=--


+-- {: .num_defn #CatOfCobordismsWithXIStructure}
###### Definition

Let $X$ be a [[topological space]] and $\xi \to X$ an $n$-[[dimensional]] [[vector bundle]]. The [[(∞,n)-category]] $Bord_n^{(X, \xi)}$ is defined analogously to $Bord_n$ but with all manifolds equipped with $(X,\xi)$-structure, def. \ref{XXiStructure}.

=--

This is ([Lurie, def. 2.4.17](#Lurie)).

+-- {: .num_theorem #CobHypTheoremForTargetSpaceAndVectorBundle}
###### Theorem

Let $\mathcal{C}$ be a [[symmetric monoidal (∞,n)-category]] with duals, let $X$ be a [[CW-complex]], let $\xi \to X$ be an $n$-[[dimensional]] [[vector bundle]] over $X$ equipped with an inner product, and let $\tilde X \to X$ be the [[associated bundle|associated]] [[orthogonal group|O(n)]]-[[principal bundle]] of orthonormal [[frames]] in $\xi$. 

There is an [[equivalence in an (∞,1)-category|equivalence]] in [[∞Grpd]]

$$
  Fun^\otimes(Bord_n^{(X,\xi)}, \mathcal{C})
  \simeq
  Top_{O(n)}(\tilde X, \tilde \mathcal{C})
  \,,
$$ 

where on the right we regard $\tilde C$ as a [[topological space]] carrying the canonical $O(n)$-[[action]] discussed [above](#TheCanonicalOnAction).

=--

This is ([Lurie, theorem. 2.4.18](#Lurie)). The following is some aspects of the idea of the proof in ([Lurie, p. 57](#Lurie)).

+-- {: .num_remark #ActionHomomorphismsAsInfinityActionHomomorphisms}
###### Remark

In the language of [[∞-actions]] (as discussed there), the space $Top_{O(n)}(\tilde X, \tilde \mathcal{C})$ is that of horizontal maps fitting into

$$
  \array{
     X && \longrightarrow && \tilde X//O(n)
     \\
     & \searrow && \swarrow
     \\
     && B SO(n)
  }
$$

where the left map is the classifying map for $\xi$ and the right one is the canonical one out of the [[homotopy quotient]].

=--

+-- {: .proof #ProofOf2.4.18}
###### Idea of Proof of theorem \ref{CobHypTheoremForTargetSpaceAndVectorBundle}.

Notice that for each point $x \colon \ast \to X$ there is an induced inclusion

$$
  Bord_n^{fr} \stackrel{x}{\longrightarrow} Bord_n^{(X,\xi)}
$$

of the framed cobordisms, def. \ref{FramedCobordismsNCat}, into those of $(X,\xi)$-structure, def. \ref{CatOfCobordismsWithXIStructure}, including those cobordisms whose map to $X$ is constant on $X$, and observing that for these an $(X,\xi)$-structure is equivalently an $n$-[[framing]]. Moreover, by corollary \ref{CanonicalOnAction} the induced point evaluation is $O(n)$-equivariant, hence yielding a morphism of [[∞-groupoids]]

$$
  \alpha
  \;\colon\;
  Func^\otimes(Bord_n^{(X,\xi)}, \mathcal{C})
  \longrightarrow
  Maps_{O(n)}(\tilde X, \tilde \mathcal{C})
  \,,
$$

where $\tilde X$ denotes the $O(n)$-[[principal bundle]] to which $\xi$ is [[associated bundle|associated]].

More generally, this is true for the pullback structure of $\xi$ along along any map $Y \to X$, yielding

$$
  \alpha_Y
  \;\colon\;
  Func^\otimes(Bord_n^{(Y,\xi|Y)}, \mathcal{C})
  \longrightarrow
  Maps_{O(n)}(\tilde X\underset{X}{\times} Y, \tilde \mathcal{C})
  \,.
$$

By the previous comment, observe that $\alpha_Y$ is an equivalence for $Y = \ast$.

Now the [[codomain]] of this [[natural transformation]] sends [[(∞,1)-colimits]] in $Y$ over $X$ to [[(∞,1)-limits]]. ([Lurie, theorem 3.1.8](#Lurie)) shows that the same is true for the domain. Hence $\alpha_Y$ is an equivalence for all $Y$ that appear as [[(∞,1)-colimits]] of the point. But this is the case for all [[∞-groupoids]] $Y$, by [this proposition](limit+in+a+quasi-category#EveryInfinityGroupoidIsHomotopyColimitOfConstantFunctorOverItself).


=--



We consider now some special cases of the general definition of local structure-topological field theory


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

We discuss the special case of the cobordism hypothesis for $(X,\xi)$-bundles (def. \ref{CatOfCobordismsWithXIStructure}) for the special case of [[G-structure]] (example \ref{GStructureAsXXiStructure}), hence for the case that $X$ is the [[classifying space]] of a [[topological group]].

Let $G$ be a [[topological group]] equipped with a [[homomorphism]] $\chi : G \to O(n)$ to the [[orthogonal group]]. Notice that via the canonical linear [[representation]] $\mathbf{B}O(n) \to$ [[Vect]] of $O(n)$ on $\mathbb{R}^n$, this induces accordingly a representation of $G$ on $\mathbb{R}^n$..

Let then 

* $X := B G$ be the [[classifying space]] for $G$;

* $\xi_\chi := \mathbb{R}^n \times_G E G $ be the corresponding [[associated bundle|associated vector bundle]] to the [[universal principal bundle]] $E G \to B G$.

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

+-- {: .num_cor #GEquivariantVersion}
###### Corollary

For $G$ an [[∞-group]] equipped with a homomorphism $G \to O(n)$ to the [[orthogonal group]] (regarded as an [[∞-group]] in [[∞Grpd]]), then evaluation on the point induces an equivalence

$$
  Fun^\otimes( Bord_n^{G}, \mathcal{C} )
  \simeq
  (\tilde {\mathcal{C}})^{G}
$$

between extended TQFTs on $n$-dimensional manifolds with [[G-structure]] and the [[∞-groupoid]] [homotopy invariants](invariant#ForInfinityGroupActions) of the [[infinity-action]] of $G$ on $\tilde \mathcal{C}$ (which is induced by the evaluation on the point).

=--

This is ([Lurie, theorem 2.4.26](#Lurie)).

+-- {: .proof #ProofOf2.4.26}
###### Proof

Theorem \ref{CobHypTheoremForTargetSpaceAndVectorBundle} asserts that

$$
  Fun^\otimes( Bord_n^{G}, \mathcal{C} )
  \simeq
  Maps_{G}(E G , \tilde C)
 \,.
$$

Hence it remains to see that the right hand side are equivalently the [[homotopy invariants]] of the $G$-[[∞-action]]. This follows for instance with the discussion at [[∞-action]], by which 

$$
  Maps_G(V,W)\simeq \infty Grpd_{/B G}(V/\!/G, W/\!/G)
  \,.
$$

This yields

$$
   Maps_{G}(E G , \tilde C)
   \simeq
   \infty Grpd_{/ B G}( B G, \tilde C /\!/B G )
   \,.
$$

By the discussion at [[dependent product]]

$$
  \infty Grpd_{/ B G}( B G, \tilde C /\!/B G )
  \simeq
  \underset{B G}{\prod} (\tilde C /\!/B G)
$$

which are the [[homotopy invariants]].

=--

#### For (un-)oriented cobordisms
 {#ForUnorientedCobordisms}

The case that $\chi \colon G \longrightarrow O(n)$ is the identity
is at the other extreme of the framed case, and turns out to be similarly fundamental.


For $\mathbf{H}$ an [[(∞,1)-topos]], write $Corr_n(\mathbf{H})^\otimes$ for the [[(∞,n)-category of correspondences]] in $\mathbf{H}$. For $Phases \in DCat_n(\mathbf{H})$ an [[(∞,n)-category with duals]] [[internal (∞,n)-category|internal]] to $\mathbf{H}$, write $Corr_n(\mathbf{H}_/{Phases})^{\otimes_{phases}}$ for the [[(∞,n)-category of correspondences]] over $Phases$ and equipped with the [[phased tensor product]]. There is the [[forgetful functor|forgetful]] [[monoidal (∞,n)-functor]]

$$
  Corr_n(\mathbf{H}_{/Phases})^{\otimes_{phased}}
  \longrightarrow
  Corr_n(\mathbf{H})^\otimes
$$

By the discussion at _[[(∞,n)-category of correspondences]]_ these are [[(∞,n)-categories with duals]] and the canonical $O(n)$-[[∞-action]] on them, corollary \ref{CanonicalOnAction}, is trivial for $Corr_n(\mathbf{H})$. This means that an $O(n)$-[[homotopy fixed point]] in $Corr_n(\mathbf{H})$ is just an object of $\mathbf{H}$ equipped in turn with an $O(n)$-[[∞-action]].  Therefore

+-- {: .num_prop #UnorientedBulkFieldTheories}
###### Proposition

Local unoriented-topological field theory

$$
  Bord_n^\sqcup \longrightarrow Corr_n(\mathbf{H})^\otimes
$$

are equivalent to objects $X \in \mathbf{H}$ equipped with an $O(n)$-[[∞-action]].

At least for $\mathbf{H} = $ [[∞Grpd]], then given such, the corresponding field theory $Z_{X/\!/O(n)}$ sends a cobordism $\Sigma$ to the space of maps

$$
  \array{
     \Pi(\Sigma) && \longrightarrow && X//O(n)
     \\
     & {}_{\mathllap{T \Sigma \oplus \mathbb{R}^{n-dim(\Sigma)}}}\searrow
     && \swarrow
     \\
     && B O(n)
  }
$$ 

hence

$$
  Z_{X//O(n)} \colon \Sigma \mapsto [\Pi(\Sigma),X]^{O(n)}
  \,.
$$

In particular this means that the assignment to the point is again $X$ itself.

=--

This is a slight rephrasing of the paragraph pp 58-59 in ([Lurie](#LurieTFT)).



+-- {: .num_prop #ExchangingFieldsForStructures}
###### Proposition

At least for $\mathbf{H} = $ [[∞Grpd]], with $X \in \mathbf{H}$ an object equipped with an $O(n)$-[[∞-action]], then horizontal lifts in

$$
  \array{
     && Corr_n(\mathbf{H}_{/Phases})^{\otimes_{phased}}
     \\
     & \nearrow & \downarrow
     \\
     Bord_n^\sqcup
     &\underset{X//O(n)}{\longrightarrow}&
     Corr_n(\mathbf{H})^\otimes
  }
$$

are equivalent to 

$$
  (Bord_n^{(X//O(n), X \underset{O(n)}{\times}\mathbb{R}^n)})^{\sqcup}
  \longrightarrow
  Phases^\otimes
  \,.
$$

=--

This is ([Lurie, prop. 3.2.8](#Lurie)).

+-- {: .num_remark}
###### Remark

Via the interpretation of local field theories with coefficients in 
$Corr_n(\mathbf{H}_{/Phases})^{\otimes_{phased}}$ as [[schreiber:Local prequantum field theory]], the statement of prop. \ref{ExchangingFieldsForStructures} translates in quantum field theory jargon to the statement that "All background structures are fields." This is essentially the slogan of [[general covariance]].

=--


+-- {: .num_cor #UnorientedLocalPrequantumFieldTheory}
###### Corollary

Let $Phases^\otimes \in Ab_\infty(\mathbf{H})$ be an [[abelian ∞-group]] object, regarded as a [[(∞,n)-category with duals]] [[internal (∞,n)-category|internal]] to $\mathbf{H}$.

At least if $\mathbf{H} = $ [[∞Grpd]], then local unoriented-topological field theories of the form

$$
  Bord_n^\sqcup \longrightarrow Corr_n(\mathbf{H}_{/Phases})^{\otimes_{phased}}
$$

are equivalent to a choice

1. of $X \in \mathbf{H}$ equipped with an $O(n)$-[[∞-action]]

1. a homomorphism of $O(n)$-[[∞-actions]] $L \colon X \to Phases$ (where $Phases^\otimes$ is equipped with the canonical $\infty$-action induced from the framed cobordism hypothesis), hence (by the discussion at _[[∞-action]]_) to a horizontal morphism in $\mathbf{H}$ fitting into the diagram

$$
  \array{
      X//O(n) && \stackrel{L//O(n)}{\longrightarrow} && Phases//O(n)
      \\
      & \searrow &\swArrow_\simeq& \swarrow
      \\
      && B O(n)
  }
  \,.
$$

=--

+-- {: .proof }
###### Proof

By prop. \ref{UnorientedBulkFieldTheories}
the co-restriction

$$
  Bord_n^\sqcup \stackrel{Z}{\longrightarrow} Corr_n(\mathbf{H}_{/Phases})^{\otimes_{phased}}
  \longrightarrow Corr_n(\mathbf{H})^\otimes
$$

is equivalent to an [[∞-action]]

$$
  \array{
     X &\longrightarrow& X//O(n)
     \\
     && \downarrow
     \\
     && B O(n)
  }
$$

Therefore by prop. \ref{ExchangingFieldsForStructures} $Z$ is equivalent to

$$
  (Bord_n^{(X//O(n), X \underset{O(n)}{\times} \mathbb{R}^n)  })^\sqcup
  \longrightarrow
  Phases^\otimes
  \,.
$$

Finally, by theorem \ref{CobHypTheoremForTargetSpaceAndVectorBundle} and in view of remark \ref{ActionHomomorphismsAsInfinityActionHomomorphisms}, this is equivalent to maps of the form

$$
  \array{
      X//O(n) && \stackrel{L//O(n)}{\longrightarrow} && Phases//O(n)
      \\
      & \searrow && \swarrow
      \\
      && B O(n)
  }
  \,.
$$


=--

By the discussion at _[[schreiber:Local prequantum field theory]]_, these statements hold also for fields with moduli spaces in more general $(\infty,1)$-toposes $\mathbf{H}$ (one sufficient condition is that $\mathbf{H}$ has an [[(infinity,1)-site]] of definition all whose objects are [[etale homotopy theory|etale contractible]]).

Some examples are discussed at _[[prequantum field theory]]_ in the section _[Higher Chern-Simons field theory -- Levels](prequantum+field+theory#HigherChern-SimonsLocalPrequantumFieldTheoryLevels)_.

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

One important variant of the category of cobordisms is obtained by discarding all those morphisms which have non-empty incoming (say, dually one could use outgoing) boundary component. Then a representation of this category imposes on its values "cups but no caps", hence only half of the data of a [[dualizable object]] in the given degree. 

Accordingly, in this case the cobordism hypothesis says that such a functor is given not quite by a [[fully dualizable object]], but by a weaker structure called a _[[Calabi-Yau object]]_ (see there for more).

([Lurie, section 4.2](#Lurie))

2-dimensional TQFT of this form is known as _[[TCFT]]_, see there for more



### For cobordisms with geometric structure

A non-topological [[quantum field theory]] is a representation of a [[cobordism category]] for cobordisms equipped with extra [[stuff, structure, property]] that is "not just topological", meaning roughly not of the form of def. \ref{CatOfCobordismsWithXIStructure}. 

The theory for this more general case is not as far developed yet. 

* steps towards classification of quantum field theories with _super-Euclidean structure_ are discussed at

  * [[(1,1)-dimensional Euclidean field theories and K-theory]]

  * [[(2,1)-dimensional Euclidean field theories and tmf]]

* a general definition of a [[cobordism category]] of cobordisms equipped with **geometric structure** given by a morphism into, roughly, a [[smooth infinity-groupoid]] of structure is discussed in  ([Ayala](#Ayala)).

A full-blown geometric cobordism statement is due to [Grady & Pavlov 2021](#GradyPavlov21).

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

* [[opetopic type theory]]

[[!include Isbell duality - table]]


## References 

### Topological cobordisms

The original hypothesis is formulated in 

*  {#BaezDolan95} [[John Baez]], [[James Dolan]], _Higher dimensional algebra and Topological Quantum Field Theory_ J. Math. Phys. **36** (1995) 6073-6105 &lbrack;[arXiv:q-alg/9503002](http://arxiv.org/abs/q-alg/9503002)&rbrack;

A sketch of an approach to the formalization and proof of the cobordism hypothesis is described in:

* {#Lurie09} [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_, Current Developments in Mathematics **2008** (2009) 129-280 &lbrack;[arXiv:0905.0465](http://arxiv.org/abs/0905.0465)&rbrack;


The comparatively simple case of $n = 1$ is spelled out in detail in 

* [[Yonatan Harpaz]], _The Cobordism Hypothesis in Dimension 1_ ([arXiv:1210.0229](http://arxiv.org/abs/1210.0229))

and aspects of the case $n = 2$ (see also at _[[2d TQFT]]_) are further discussed in 

* {#SchommerPries11} [[Chris Schommer-Pries]], _The Classification of Two-Dimensional Extended Topological Field Theories_ ([arXiv:1112.1000](http://arxiv.org/abs/1112.1000))

Lecture notes and reviews on the topic of the cobordisms hypothesis:

* [[Jacob Lurie]], _TQFT and the Cobordism Hypothesis_ ([video](http://www.ma.utexas.edu/video/dafr/lurie/), [notes](http://www.ma.utexas.edu/users/plowrey/dev/rtg/notes/perspectives_TQFT_notes.html))

* [[Jacob Lurie]], _The Classification of Extended Topological Field Theories_ ([video](https://www.youtube.com/watch?v=svsidHyNk1k))

* [[Julie Bergner]], _[[UC Riverside Seminar on Cobordism and Topological Field Theories]]_  (2009).  

* [[Julie Bergner]], _Models for $(\infty,n)$-Categories and the Cobordism Hypothesis_ , in [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_, AMS 2011

* [[Daniel Freed]], _The cobordism hypothesis_, Bulletin of the American Mathematical Society 50 (2013), pp. 57-92, ([arXiv:1210.5100](http://arxiv.org/abs/1210.5100), [doi:10.1090/S0273-0979-2012-01393-9](https://doi.org/10.1090/S0273-0979-2012-01393-9))

* {#SchommerPries13} [[Chris Schommer-Pries]], _Dualizability in Low-Dimensional Higher Category Theory_ ([arXiv:1308.3574](http://arxiv.org/abs/1308.3574))

* {#Teleman14} [[Constantin Teleman]], _Five lectures on topological field theory_, 2014 ([pdf](http://math.berkeley.edu/~teleman/math/barclect.pdf))

An approach to the proof of the cobordism hypothesis via [[factorization homology]] is in

* [[David Ayala]], [[John Francis]], _The cobordism hypothesis_, ([arXiv:1705.02240](https://arxiv.org/abs/1705.02240))

Discussion of the canonical $O(n)$-action on [[n-fold loop spaces]] (which may be thought of as a special case of the cobordism hypothesis) includes

* {#GaudensMenichi07} Gerald Gaudens, [[Luc Menichi]],  section 5 of _Batalin-Vilkovisky algebras and the $J$-homomorphism_, Topology and its Applications Volume 156, Issue 2, 1 December 2008, Pages 365&#8211;374 ([arXiv:0707.3103](http://arxiv.org/abs/0707.3103))


### Geometric cobordisms
 {#ReferencesGeometricCobordisms}

Higher cobordisms with geometric [[structure]] (i.e. for non-topological [[extended quantum field theory]]) are discussed in

* {#Ayala} [[David Ayala]], _Geometric cobordism categories_ ([arXiv:0811.2280](https://arxiv.org/abs/0811.2280))

* {#GradyPavlov20} [[Daniel Grady]], [[Dmitri Pavlov]], *Extended field theories are local and have classifying spaces* &lbrack;[arXiv:2011.01208](https://arxiv.org/abs/2011.01208)&rbrack;

and full proof of the cobordism hypothesis in this geometric generality (hence for non-topological [[extended quantum field theory|extended]] [[FQFT]] such as [[conformal field theory]]) is claimed in:

* {#GradyPavlov21} [[Daniel Grady]], [[Dmitri Pavlov]], *The geometric cobordism hypothesis* &lbrack;[arXiv:2111.01095](https://arxiv.org/abs/2111.01095)&rbrack;

based on [Grady & Pavlov 2020](#GradyPavlov20).

Review:

* [[Dmitri Pavlov]], *The geometric cobordism hypothesis*, talk at *[QFT and Cobordism](https://nyuad.nyu.edu/en/events/2023/march/quantum-field-theories-and-cobordisms.html)*, [[CQTS]] (Mar 2023) &lbrack;[pdf](https://dmitripavlov.org/nyuad.pdf), [[Pavlov-GCHatCQTS.pdf:file]], [web](Center+for+Quantum+and+Topological+Systems#PavlovMar2023), video: [YT](https://www.youtube.com/watch?v=n6Eog_z82eA)&rbrack;




[[!redirects cobordism hypotheses]]


[[!redirects cobordism theorem]]


[[!redirects geometric cobordism hypothesis]]


