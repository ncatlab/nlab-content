
> this entry contains one chapter of _[[geometry of physics]]_. 

> previous chapters: _[[geometry of physics -- smooth sets|smooth sets]]_, _[[geometry of physics -- smooth homotopy types|smooth homotopy types]]_

> next chapters: _[[geometry of physics -- G-structure and Cartan geometry|G-structure and Cartan geometry]]_, _[[geometry of physics -- supergeometry|supergeometry]]_

#Contents#
* table of contents
{:toc}

## **Manifolds and orbifolds**
 {#ManifoldsAndOrdbifolds}

In the discussion at _[[geometry of physics -- smooth sets]]_ we have started with very simple model spaces for [[differential geometry]], namely just the [[Cartesian spaces]], and have obtained from these, by passing to the [[sheaf topos]] over the [[site]] that they form, very general [[smooth spaces]]. We remarked that _[[smooth manifolds]]_ form a [[full subcategory]] for these general [[smooth sets]] and hence sit in between the very simple model spaces and the very general smooth sets.

$$
  CartSp \hookrightarrow SmoothMfd \hookrightarrow Smooth0Type
$$

In making this statement, we assumed that we already know what smooth manifolds are. Here now we consider the question of _characterizing_ smooth manifolds as special smooth sets, hence (re-)defining them, but in a way that is slightly (though not much) different from the traditional textbook description, a way that is true to the spirit of regarding smooth sets as the good ambient context for doing differential geometry.

Or rather, as throughout these notes, by characterizing smooth manifolds among smooth sets in a neat general abstract way, we may carry this characterization verbatim from [[smooth sets]] to the more general context of [[smooth homotopy types]], where its interpretation becomes something that goes beyond what traditional textbook methods allow to cover: the concept of smooth manifold thus embedded into [[smooth groupoids]] comes out as the concept of _[[étale groupoid]]_ ([[differentiable stack|differentiable]] [[étale stack]]). A traditionally fairly familiar special class of these are _[[orbifolds]]_ the direct analog in [[differential geometry]] of what in [[algebraic geometry]] is famous as [[Deligne-Mumford stacks]].

Fully generally, the interpretation of the abstract concept of manifold in [[smooth homotopy types]] is a concept of _smooth [[étale ∞-groupoids]]_. 


In fact more is true. The terminology _smooth [[étale groupoid]]_ without further qualification refers to [[smooth groupoids]] that are _locally diffeomorphic_ to a [[Cartesian space]] $\mathbb{R}^n$, in a suitable way. But more generall one may replace $\mathbb{R}^n$ here with any other [[group object]] $V$ in [[smooth sets]], hence with any [[smooth group]], and in fact with any [[∞-group]] object in [[smooth homotopy types]], hence with any [[smooth ∞-group]]: given any such, then a _$V$-manifold_ is a smooth homotopy type $X$ which is locally diffeomorphic to $V$ in a suitable sense. One may say that $X$ is _&#233;tal&#233;_ (spread out), but over $V$.

For instance in [[higher Cartan geometry|higher]] [[super Cartan geometry]] $V$ is typically an [[extended super Minkowski spacetime]] (some super [[n-group]]) and $X$ is a [[superspacetime]] locally diffeomorphic to that.

A key aspect featured by $V$-manifolds, in this general sense, but not necessarily by more general smooth homotopy types, is that they carry a _[[frame bundle]]_, a [[principal bundle]] for the [[general linear group]] $GL(V)$ -- which in the generality of higher differential geometry we define to be the [[automorphism ∞-group]] of the [[infinitesimal neighbourhood]] of the neutral element in $V$. The class of this frame bundle characterizes how the local diffeomorphic identifications of $X$ with $V$ are twisted with respect to each other as one moves around on $X$. 

This is the key to formulating genuine geometric structure on smooth spaces: following an insight that goes back to [[Élie Cartan]], most every sort of geometric structure on a smooth space $X$ is a ([[integrable G-structure|infinitesimally integrable]]) _[[G-structure]]_, hence a [[reduction of the structure group]] of the [[frame bundle]] of $X$, subject to some local rigidity constraint. This subsumes notably ([[pseudo-Riemannian geometry|pseudo]]-)[[Riemannian geometry|Riemannian geometric structure]], [[complex structure]], [[symplectic structure]], [[conformal structure]] and much more. These geometric structures on higher manifolds are the topic of the chapter _[[geometry of physics -- G-structure and Cartan geometry]]_.


### Model Layer
 {#ModelLayer}


#### Manifolds

We give first an account of the traditional definition of smooth manifolds, but (re-)phrasing it equivalently in category-theoretic terms that lend themselves to generalization. 


##### Formal smooth Cartesian spaces
 {#FormalSmoothCartesianSpaces}
1. 

In order to speak about [[tangent vectors]] and [[local diffeomorphisms]] in a way that generalizes to [[higher differential geometry]], it is useful to introduce structure that allows to _co-represent_ tangent vectors: where a smooth path in a Cartesian space $X$ is a smooth function out of the [[real line]] $\mathbb{R}$ into $X$, a [[tangent vector]] as traditionally defined is intuitively the restriction of such a map to the first order [[infinitesimal neighbourhood]] of the origin in $\mathbb{R}$: an "infinitesimal path". 

The idea now (which is the idea of [[synthetic differential geometry]]) is to make that intuition into a mathematical fact by passing to a context of slightly generalized Cartesian spaces where that [[infinitesimal neighbourhood]] exists _literally_ as a [[subobject]] $\mathbb{D} \hookrightarrow \mathbb{R}$, such that the a tangent vector is _literally_ a morphism $\mathbb{D} \to X$.

In order to see what these generalized Cartesian spaces might be, recall a basic fact about [[smooth functions]]:

Write $CAlg_{\mathbb{R}}$ for the [[category]] of [[commutative algebras]] over the [[field]] of [[real numbers]]. Write [[SmoothCartSp]] for the [[category]] of [[Cartesian spaces]] and [[smooth functions]] between them.

+-- {: .num_prop #EmbeddingOfSmoothManifoldsIntoFormalDualsOfRAlgebras}
###### Proposition

The [[functor]]

$$
  C^\infty(-) \colon SmoothCartSp \longrightarrow CAlg_{\mathbb{R}}^{op}
$$

which sends a [[Cartesian space]] to (the [[formal dual]] of) its $\mathbb{R}$-[[commutative algebra|algebra]] of [[smooth functions]] is a [[full and faithful functor]].


In other words, for two [[Cartesian spaces]] $X,Y$ there is a [[natural bijection]] between the [[smooth functions]] $X \to Y$ and the algebra homomorphisms $C^\infty(X)\leftarrow C^\infty(Y)$.

=--

See at _[[embedding of smooth manifolds into formal duals of R-algebras]]_ for more on this.

+-- {: .num_remark #CarefulWithSmoothAlgebras}
###### Remark

One has to be careful that prop. \ref{EmbeddingOfSmoothManifoldsIntoFormalDualsOfRAlgebras} might seem to imply more than it does. In order that all constructions on all commutative algebras have the desired dual effect on formally dual smooth spaces (e.g. construction of [[products]]/[[coproducts]], or construction of [[Kähler differentials]]) one needs to refine plain commutative algebras over $\mathbb{R}$ to _[[smooth algebras]]_. See there for more on this point, which however for our purposes here is not of further concern. 

=--

With Cartesian spaces embedded into the larger context of formal duals of commutative algebras by prop. \ref{EmbeddingOfSmoothManifoldsIntoFormalDualsOfRAlgebras}, we may pass to a larger subcategory of the latter to obtain a notion of generalized smooth spaces. Since we are after [[infinitesimal spaces]] of sorts, and since, via the embedding of prop. \ref{EmbeddingOfSmoothManifoldsIntoFormalDualsOfRAlgebras}, a space is equivalently encoded in the [[algebra of functions]] it carries, we need to specify those commutative algebras that behave like algebras of functions on infinitesimal Cartesian spaces. The intuition is that these spaces are so small, that the canonical coordinate functions $x^i$ on them take values which are so very small $\llt 1$ that when taken to some power they vanish not only approximately, but identically. But this intuition is easily formalized:

+-- {: .num_defn #FormalSmoothCartesianSpaces}
###### Definition

Write 

$$
  InfPoint \hookrightarrow CAlg_{\mathbb{R}}^{op}
$$ 

for the [[full subcategory]] of the [[opposite category]] of [[commutative algebras]] over $\mathbb{R}$ on [[formal duals]] of [[commutative algebras]] over the [[real numbers]] of the form $\mathbb{R}\oplus V$ with $V$ a finite-dimensional  [[nilpotent ideal]] ([[local Artin algebras]] over the real numbers). We call this the category of _[[infinitesimally thickened points]]_.

Write moreover

$$
  FormalSmoothCartSp
  \coloneqq
  CartSp \rtimes InfPoint \hookrightarrow CAlg_{\mathbb{R}}^{op}
$$

for the [[full subcategory]] on [[formal duals]] of those algebras which are [[tensor products]] of commutative $\mathbb{R}$-algebras of the form

$$
  C^\infty(\mathbb{R}^n) \otimes C^\infty(D)
$$

of algebras $C^\infty(\mathbb{R}^p)$ of [[smooth functions]] $\mathbb{R}^n$ as in def. \ref{EmbeddingOfSmoothManifoldsIntoFormalDualsOfRAlgebras} with algebras corresponding to infinitesimally thickened points $D$ as above.

=--

+-- {: .num_remark}
###### Remark

The basic idea of prop. \ref{FormalSmoothCartesianSpaces} is familiar in [[algebraic geometry]], going back to [[Alexander Grothendieck]]'s work in the 1950s, related to [[crystalline cohomology]]. Traditionally the idea is often embodied in the concept of [[formal schemes]], which is however considerably more involved ([[locally ringed spaces]], [[ind-objects]]) than necessary for capturing the basic phenomenon. The point that the simple idea of modelling infinitesimals by nilpotent element in functions rings is not at all restricted to [[algebraic geometry]] but also works in [[differential geometry]] has been highlighted by [[William Lawvere]] in the 1960s, who phrased it in terms of what is now known as the [[Kock-Lawvere axioms]] of [[synthetic differential geometry]]. In this context textbooks tend to amplify the usefulness of [[smooth algebras]] with infinitesimals, but as long as one does not insist on all geometric operations to have algebraic duals, see remark \ref{CarefulWithSmoothAlgebras} above, then using just plain real algebras with nilpotent elements as done here is sufficient. 

=--


+-- {: .num_prop #SmoothCartSpCoreflectiveInFormalSmoothCartSp}
###### Proposition

The evident [[full subcategory]] inclusion 
 of [[smooth Cartesian spaces]] into [[formal smooth manifold|formal smooth Cartesian spaces]], def. \ref{FormalSmoothCartesianSpaces} is [[coreflective 
subcategory|coreflective]], hence has a [[right adjoint]] $p$

$$
  (i \dashv p)
  \;\colon\;
  SmoothCartSp 
   \stackrel{\overset{i}{\hookrightarrow}}{\underset{p}{\longleftarrow}}
  FormalSmoothCartSp
  \,.
$$

On formal dual algebras, $p$ is given by quotienting out the [[nilpotent ideal]].

=--

+-- {: .proof}
###### Proof

We need to check that for all $n_1, n_2 \in \mathbb{N}$ and for all $D \in InfPoint$, there is a [[natural bijection]] between the set of morphisms

$$
  \mathbb{R}^{n_1} \longrightarrow \mathbb{R}^{n_2}\times D
$$

in $FormalSmoothCartSp$, and the set of morphisms

$$
  \mathbb{R}^{n_1} \longrightarrow \mathbb{R}^{n_2}
$$

in $SmoothCartSp$. By definition, the former set is equivalently that of $\mathbb{R}$-algebra homomorphisms $\phi$ of the form

$$
  C^\infty(\mathbb{R}^{n_1})
   \longleftarrow
  C^\infty(\mathbb{R}^{n_2})\otimes_{\mathbb{R}} V
  \,,
$$

where $V$ is the [[nilpotent ideal]] of the formal dual algebra of functions on $D$.

Now for $v$ an element in the algebra on the right which is nilpotent, hence for which there is $p \in \mathbb{N}$ such that $v^p = 0$, then any algebra homomorphism $\phi$ needs to preserve this condition, hence also $\phi(v)^p = 0$ and hence also $\phi(v)$ is nilpotent. But the only nilpotent element in $C^\infty(\mathbb{R}^{n_1})$ is zero. Therefore every algebra homomorphism $\phi$ as above has to have $V$ in its [[kernel]], hence it has to factor through the quotient projection $C^\infty(\mathbb{R}^{n_2})\otimes_{\mathbb{R}} V \to C^\infty(\mathbb{R}^{n_2})$. 

With this the statement follows by prop. \ref{EmbeddingOfSmoothManifoldsIntoFormalDualsOfRAlgebras}.

(A similar argument gives that $p$ is a functor in the first place.)

=--


##### Formal smooth sets
 {#FormalSmoothSets}

Following closely the theory at _[[geometry of physics -- smooth sets]]_, we are now to pass to the [[generalized smooth spaces]] which are _locally probe-able_ by the formal smooth Cartesian spaces of def. \ref{FormalSmoothCartesianSpaces}, and these are the [[sheaves]] on the [[site]] $FormalSmoothCartSp$ that the latter form.

+-- {: .num_defn #FormalSmoothCartesianSpacesSite}
###### Definition

Regard the category $FormalSmoothCartSp$ of def. \ref{FormalSmoothCartesianSpaces} as a [[site]] by equipping it with the [[coverage]] whose covering families are of the form


$$
  \left\{
    U_i \times D \stackrel{(\phi_i,id_D)}{\longrightarrow} U \times D
  \right\}
$$

for $U, U_i \in SmoothCartSp \hookrightarrow FormalSmoothCartSp$, $D \in InfPoint \hookrightarrow FormalSmoothCartSp$, and $\{U_i \stackrel{\phi_i}{\to} U\}$ a covering family in $SmoothCartSp$, hence a traditional [[open cover]].

=--



+-- {: .num_defn #ToposOfFormalSmoothSets}
###### Definition

A _formal smooth set_ is a [[sheaf]] on the site $FormalSmoothCartSp$ of def. \ref{FormalSmoothCartesianSpacesSite}. Write

$$
  FormalSmooth0Type \coloneqq Sh(FormalSmoothCartSp)
$$

for the [[category of sheaves]] on that site.

=--

+-- {: .num_remark }
###### Remark

The category of def. \ref{ToposOfFormalSmoothSets}
is traditionally known as the _[[Cahiers topos]]_.

=--

+-- {: .num_prop #AdjointQuadrupleOnFormalSmoothSets}
###### Proposition

The co-reflective inclusion of sites of prop. \ref{SmoothCartSpCoreflectiveInFormalSmoothCartSp}

$$
  SmoothCartSp \stackrel{\overset{i}{\hookrightarrow}}{\underset{p}{\longleftarrow}} FormalSmoothCartSp
$$

extends via [[Kan extension]] to an [[adjoint quadruple]] of functors

$$
  Smooth0Type
   \stackrel{\overset{i_!}{\hookrightarrow}}{\stackrel{\overset{i^\ast}{\longleftarrow}}{\stackrel{\overset{i_\ast}{\hookrightarrow}}{\underset{i^!}{\longrightarrow}}}}
  FormalSmooth0Type
$$

between [[smooth sets]] and [[formal smooth sets]].

=--

We agree that when in the following we write an unlabeled inclusion

$$
  Smooth0Type \hookrightarrow FormalSmooth0Type
$$

then we always mean inclusion by $i_!$ in the above, not by $i_\ast$. On representables this is the inclusion $i$ of smooth Cartesian spaces into Cartesian spaces.


+-- {: .num_defn #AdjointTripleOnFormalSmoothSets}
###### Definition

We write

$$
  (\Re \dashv \Im \dashv \&)
  \;\colon\;
  FormalSmooth0Type
   \stackrel{\overset{i^\ast}{\longrightarrow}}{\stackrel{\overset{i_\ast}{\longleftarrow}}{\underset{i^!}{\longrightarrow}}}
   Smooth0Type
   \stackrel{\overset{i_!}{\longrightarrow}}{\stackrel{\overset{i^\ast}{\longleftarrow}}{\underset{i_\ast}{\longrightarrow}}}
  FormalSmooth0Type
$$

for the [[adjoint triple]] of ([[comonad|co]]-)[[monads]] induced from the functors in prop. \ref{AdjointQuadrupleOnFormalSmoothSets}. At times we call these, respectively


* $\Re$ -- [[reduction modality]];

* $\Im$ -- [[infinitesimal shape modality]];

* $\&$ -- [[infinitesimal flat modality]].

=--

+-- {: .num_example #NatureOfTheModalitiesOnCahiersTopos}
###### Example

The single key fact to understand the operations in def. \ref{AdjointTripleOnFormalSmoothSets} is the [[left Kan extension]] of presheaves along a functor between sites restricts to that functor on representables. (See at _[Kan extension -- Left Kan extension on representables](Kan+extension#LeftKanOnRepresentables)_). 

This means that for $U \in SmoothCartSp \hookrightarrow FormalSmoothCartSp$ and $D \in InfPoint \hookrightarrow FormalSmoothCartSp$ then 

* $\Re( U \times D) \simeq D$;

* $Hom(U \times D, \Im(X)) \simeq Hom(U, X)$.

=--


##### Tangent vectors 
 {#TangentVectors}

The following is the key observation regarding generally the role of nilpotent elements in function algebras and specifically as to the nature of formal Cartesian spaces.

+-- {: .num_example #TangentVectorsByAlgebra}
###### Example

Write $\mathbb{D}$ for the [[formal dual]] of the [[algebra of dual numbers]] $(\mathbb{R}[\epsilon])/(\epsilon^2)$. Then morphisms


$$
  \mathbb{R}^n \times \mathbb{D}\longrightarrow \mathbb{R}^n
$$

which are the identity after restriction along $\mathbb{R}^n \to \mathbb{R}^n \times \mathbb{D}$, are equivalently algebra homomorphisms of the form


$$
  (C^\infty(\mathbb{R}^n)\otimes_{\mathbb{R}} \wedge^\bullet \langle \epsilon\rangle
  \longleftarrow
  C^\infty(\mathbb{R}^n)
$$

which are the identity modulo $\epsilon$. Such a morphism has to take any function $f \in C^\infty(\mathbb{R}^n)$ to 

$$
  f + (\partial f) \epsilon
$$

for some smooth function $(\partial f) \in C^\infty(\mathbb{R}^n)$. The condition that this assignment makes an algebra homomorphism is equivalent to the statement that for all $f_1,f_2 \in C^\infty(\mathbb{R}^n)$


$$
  (f_1 f_2 + (\partial (f_1 f_2))\epsilon )
  =
  (f_1 + (\partial f_1) \epsilon)
  (f_2 + (\partial f_2) \epsilon)
  \,.
$$

Multiplying this out and using that $\epsilon^2 = 0$ this in turn is equivalent to

$$
  \partial(f_1 f_2) = (\partial f_1) f_2 + f_1 (\partial f_2)
  \,.
$$

This in turn means equivalently that $\partial\colon C^\infty(\mathbb{R}^n)\to C^\infty(\mathbb{R}^n)$ is a [[derivation]]. But derivations of algebras of [[smooth functions]] are equivalent to [[vector fields]]. (See at _[[derivations of smooth functions are vector fields]]_).

In particular one finds that maps

$$
  \mathbb{D} \longrightarrow \mathbb{R}^n
$$

are equivalently single [[tangent vectors]].

=--


Based on this, the following is a classical fact of [[synthetic differential geometry]].

+-- {: .num_prop #TangentBundlesAsInternalHoms}
###### Proposition

For $X \in SmoothMfd \hookrightarrow Smooth0Type \hookrightarrow FormalSmooth0Type$ a [[smooth manifold]], then the [[internal hom]] $[\mathbb{D},X]$ out of the [[infinitesimal interval]] is equivalent to the total space manifold of the [[tangent bundle]] of $X$.

=--

+-- {: .proof}
###### Proof

By definition of [[internal hom]], for every object $U$ then morphisms

$$
  U \longrightarrow [\mathbb{D},X]
$$

are in [[natural bijection]] with morphisms

$$
  U \times \mathbb{D}\longrightarrow X
  \,.
$$

By example \ref{TangentVectorsByAlgebra} these are smoothly $U$-parameterized tangent vectors in $X$, hence are naturally isomorphism to morphisms

$$
  U \longrightarrow T X
  \,.
$$

Hence $[\mathbb{D},X]$ and $T X$ represent isomorphic [[representable functors]]. Then the [[Yoneda lemma]] implies that they are themselves [[isomorphism|isomorphic]].

=--

##### Local diffeomorphisms

The traditional definition of [[local diffeomorphisms]] says

+-- {: .num_defn #LocalDiffeomorphismTraditional}
###### Definition

A [[smooth function]] $f \colon X \longrightarrow Y$
between [[smooth manifolds]] is a _local diffeomorphism_ if for all points $x\in X$ its [[derivatives]] at that point induce an [[isomorphism]] of [[tangent bundle|tangent]] [[vector spaces]]

$$
  \underset{x \in X}{\forall}  d f \;\colon\; T_x X \stackrel{\simeq}{\longrightarrow} T_{f(x)}Y
  \,.
$$

=--

A more [[category theory|category theoretic]] way to say this, which may still be found in some traditional textbooks, is this

+-- {: .num_prop #LocalDiffeosDetectedByPullbackOfTangentBundle}
###### Proposition

A [[smooth function]] $f \colon X \longrightarrow Y$
between [[smooth manifolds]] is a _local diffeomorphism_, def. \ref{LocalDiffeomorphismTraditional}, equivalently if the [[diagram]] of [[tangent bundles]] that it induces

$$
  \array{
    T X &\stackrel{}{\longrightarrow}& X
    \\
    \downarrow^{\mathrlap{d f}} && \downarrow
    \\
    T Y &\stackrel{}{\longrightarrow}& Y
  }
$$

is a [[pullback]] diagram.

=--

Now this in turn we may further reformulate as follows:



+-- {: .num_prop #TraditionalLocalDiffeosByModality}
###### Proposition

A [[smooth function]] $f \colon X \longrightarrow Y$
between [[smooth manifolds]] is a _local diffeomorphism_, def. \ref{LocalDiffeomorphismTraditional}, equivalently if after regarding in under the embedding $Smooth0Type \hookrightarrow FormalSmooth0Type$, the [[unit of a monad|unit]] [[natural transformation|naturality square]] of the [[infinitesimal shape modality]], def. \ref{AdjointTripleOnFormalSmoothSets},

$$
  \array{
    X &\stackrel{}{\longrightarrow}& \Im X
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{\Im f}}
    \\
    Y &\stackrel{}{\longrightarrow}& \Im Y
  }
$$

is a [[pullback]]

=--

+-- {: .proof}
###### Proof

Pullbacks of sheaves are detected by giving pullbacks of sets after evaluating on all possible objects of the [[site]]. 

Consider first those objects of the form $U \in SmoothCartSp \hookrightarrow FormalSmoothCartSp \hookrightarrow FormalSmooth0Type$. By example \ref{NatureOfTheModalitiesOnCahiersTopos} for these the diagram in question becomes

$$
  \array{
    Hom(U,X) &\stackrel{id}{\longrightarrow}& Hom(U,X)
    \\
    \downarrow^{\mathrlap{Hom(U,f)}} && \downarrow^{\mathrlap{Hom(U,f)}}
    \\
    Hom(U,Y) &\stackrel{id}{\longrightarrow}& Hom(U,Y)
  }
  \,,
$$

which is trivially a pullback. Consider then objects of the form $U \times \mathbb{D}$ for $\mathbb{D}$ the [[infinitesimal interval]]. By example \ref{NatureOfTheModalitiesOnCahiersTopos} and by prop. \ref{TangentBundlesAsInternalHoms} they all giving pullbacks is equivalent to the diagram

$$
  \array{
    T X &\stackrel{}{\longrightarrow}& X
    \\
    \downarrow^{\mathrlap{d f}} && \downarrow
    \\
    T Y &\stackrel{}{\longrightarrow}& Y
  }
$$

being a pullback. By prop. \ref{LocalDiffeosDetectedByPullbackOfTangentBundle} this is already equivalent to $f$ being a local diffeomorphism.

But local diffeomorphisms of [[smooth manifolds]] (as opposed to [[formally étale morphisms]] of [[schemes]]!) are already necessarily [[étale morphisms]], i.e. they diffeomorphically identify not just an [[infinitesimal neighbourhood]] around each point, but the whole [[germ]]. This implies that for $D \in InfPoint \hookrightarrow FormalSmoothCartSp \hookrightarrow FormalSmooth0Type$ any object, also the image of the diagram under $Hom(U \times D,-)$ gives a pullback. 


=--

Given prop. \ref{TraditionalLocalDiffeosByModality} it makes sense to say

+-- {: .num_defn #LocalDiffeosGenerallyInCahiersTopos}
###### Definition

A morphism $f \colon X\to Y$ in $FormalSmooth0Type$ is a _[[local diffeomorphism]]_ (or [[formally étale morphism]]) if the [[natural transformation|naturality sqare]] of the [[unit of a monad|unit]] of its [[infinitesimal shape modality]]

$$
  \array{
    X &\stackrel{}{\longrightarrow}& \Im X
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{\Im f}}
    \\
    Y &\stackrel{}{\longrightarrow}& \Im Y
  }
$$

is a [[pullback]] diagram.

=--


##### Smooth manifolds
  {#Manifolds}
  {#SmoothManifold}

With the (re-)formulation of local diffeomorphisms between smooth manifolds and their generalization to maps of smooth sets by prop. \ref{LocalDiffeosGenerallyInCahiersTopos}, we now have the following neat way to characterize smooth manifolds among [[smooth sets]].

+-- {: .num_defn #ManifoldsAsEtaleGroupoids}
###### Definition/Proposition

For $n\in \mathbb{N}$, a [[smooth manifold]] of [[dimension]] $n$ is an object $X \in FormalSmooth0Type$ such that there exists a morphisms of the form

$$
  \underset{i }{\coprod} U_i
  \stackrel{=}{\to}
  \underset{i }{\coprod} \mathbb{R}^n 
  \longrightarrow
  X
$$

which is

1. an [[epimorphism]],

1. a [[local diffeomorphism]], def. \ref{LocalDiffeosGenerallyInCahiersTopos};

=--

+-- {: .proof}
###### Proof

A quick abstract way to prove this, for which however at this point we have not provided all the ingredients yet, is to observe that the map being an [[1-epimorphism]] makes it equivalent to its [[Cech nerve]] [[groupoid object in an (infinity,1)-category|groupoid object]], and it being a local diffeomorphism makes that an [[étale groupoid]]. This being 0-truncated, its underlying object (stack) is equivalent to a smooth manifold, in fact as a groupoid object it is the [[Cech groupoid]] of that smooth manifold 

$$
  \underset{i,j}{\coprod}  U_i \underset{X}{\times} U_j
  \stackrel{\longrightarrow}{\longrightarrow}
  \underset{i}{\coprod} U_i
$$

with respect to the cover that we started with above.

=--


##### Frame bundles
 {#FrameBundleTraditional}

> the following is some semi-traditional basic discussion. Need to see what to do with this here.

On each overlap $U_i \cap U_j$ of two charts, the [[partial derivatives]] of the corresponding [[coordinate transformations]]

$$
  \phi_j\circ \phi_i^{-1}
  : 
  U_i \cap U_j \subset \mathbb{R}^n \to \mathbb{R}^n
$$

form the [[Jacobian matrix]] of [[smooth functions]]

$$
  ((\lambda_{i j})^{\mu}{}_{\mu})
  \coloneqq
  \left[\frac{d}{d x^\nu} \phi_j \circ \phi_i^{-1} (x^\mu)
  \right]
  :
  U_i \cap U_j 
  \to 
  GL_n
$$

with values in invertible [[matrices]], hence in the
[[general linear group]] $GL(n)$. By construction (by the [[chain rule]]), these functions satisfy on triple overlaps of coordinate charts the [[matrix product]] equations

$$
  (\lambda_{i j})^\mu{}_\lambda (\lambda_{j k})^\lambda{}_{\nu} 
  = 
  (\lambda_{i k})^\mu{}_{\nu}
  \,,
$$

(here and in the following sums over an index appearing upstairs and downstairs are explicit)

hence the equation

$$
  \lambda_{i j} \cdot \lambda_{j k} = \lambda_{i k}
$$

in the [[group]] $C^\infty(U_i \cap U_j \cap U_k, GL(n))$ of smooth $GL(n)$-valued functions on the chart overlaps.

This is the _[[cocycle]] condition_ for a smooth [[Cech cohomology|Cech cocycle]] in degree 1 with coefficients in $GL(n)$ (precisely: with coefficients in the [[sheaf]] of [[smooth functions]] with values in $GL(n)$ ). We write

$$
  [(\lambda_{i j})] \in H^1_{smooth}(X, GL_n)
  \,.
$$

Formulated as [[smooth groupoids]]

* $X$ itself is a [[Lie groupoid]] $(X \stackrel{\longrightarrow}{\longrightarrow} X)$ with trivial morphism structure;

* from the atlas $\{U_i \to X\}$ we get the corresponding [[Cech groupoid]] 
  $$
    C(\{U_i\}) = 
    (\coprod_{i, j} U_i \cap U_j \stackrel{\longrightarrow}{\longrightarrow} \coprod_i U_i)
    = 
    \left\{
      \array{
         && (x,j)
         \\
         & \nearrow &=& \searrow
         \\
        (x,i) &&\to&& (x,k)
      }
      \;\;\;
      for\, x \in U_i \cap U_j \cap U_k
    \right\}
    \,,
  $$

  whose objects are the points in the atlas, with morphisms identifying lifts of a point in $X$ to different charts of the atlas;

The above situation is neatly encoded in the existence of a [[diagram]] of Lie groupoids of the form

$$
  \array{
     C(\{U_i\}) &\stackrel{\tau_X}{\longrightarrow}& \mathbf{B} GL(n).
     \\
     {}^{\mathllap{\simeq}}\downarrow
     \\
     X
  }
  \,,
$$

where

* the left morphism is [[stalk]]-wise (around small enough [[neighbourhoods]] of each point) an [[equivalence of groupoids]] (we make this more precise in a moment);

* the horizontal functor $\tau_X$ has as components the functions $\lambda_{i j}$ and its functoriality is the cocycle condition $\lambda_{i j} \cdot \lambda_{j k} = \lambda_{i k}$.


A [[natural transformation|transformation]] of smooth functors $\lambda_1 \Rightarrow \lambda_2 : C(\{U_i\}) \to \mathbf{B} GL(n)$ is precisely a [[coboundary]] between two such cocycles.

This defines a morphism of [[smooth groupoids]]

$$
  \tau_X \;\colon\; X \to \mathbf{B}GL(n)
  \,.
$$

The [[homotopy fiber]] of this map is a $GL(n)$-[[principal bundle]] called the [[frame bundle]] of $X$, while  the canonically [[associated bundle]] via the canonical [[representation]] of $GL(n)$ on $\mathbb{R}^n$ is the [[tangent bundle]]

$$
  T X \to X
  \,.
$$


#### &#201;tale groupoids

##### Formal smooth groupoids

In view of the refinement of [[smooth sets]] on the one hand to [[formal smooth sets]] and on the other hand to [[smooth groupoid]], we now consider the joint refinement to [[formal smooth groupoids]].

This proceeds essentially verbatim to the previous definitions

+-- {: .num_defn #FormalSmoothGroupoids}
###### Definition

A _pre-formal smooth groupoid_ is a [[presheaf]] of [[groupoids]] on $FormalSmoothCartSp$.

Write

$$
  FormalSmooth1Type \coloneqq L_{lwhe} PreFormalSmooth1Type
$$

for the [[(2,1)-category]] which is the [[simplicial localization]] at the local weak equivalences.

=--

(...)



$$
  \array{
    Smooth1Type &
      \stackrel{\hookrightarrow}{\stackrel{\longleftarrow}{\stackrel{\hookrightarrow}{\longleftarrow}}}
    & FormalSmooth1Type
    \\
    \downarrow && \downarrow
    \\
    Smooth0Type
    &
      \stackrel{\hookrightarrow}{\stackrel{\longleftarrow}{\stackrel{\hookrightarrow}{\longleftarrow}}}
    &
    FormalSmooth0Type
  }
$$


We may now directy adapt the definition of local diffeos as in def. \ref{LocalDiffeosGenerallyInCahiersTopos} simply by generalizing [[0-types]] to [[1-types]] and [[pullbacks]] to [[homotopy pullbacks]]:

+-- {: .num_defn #LocalDiffeosGenerallyInFormalSmooth1Types}
###### Definition

A morphism $f \colon X\to Y$ in $FormalSmooth1Type$, def. \ref{FormalSmoothGroupoids}, is a _[[local diffeomorphism]]_ (or [[formally étale morphism]]) if the [[natural transformation|naturality sqare]] of the [[unit of a monad|unit]] of its [[infinitesimal shape modality]]

$$
  \array{
    X &\stackrel{}{\longrightarrow}& \Im X
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{\Im f}}
    \\
    Y &\stackrel{}{\longrightarrow}& \Im Y
  }
$$

is a [[homotopy pullback]] diagram.

=--

##### &#201;tale Lie groupoids
 {#EtaleLieGroupoids}

The traditional definition of smooth [[étale groupoids]] is the following:

+-- {: .num_defn #EtaleGroupoidTraditional}
###### Definition

A [[Lie groupoid]] $\mathcal{G}_\bullet$ is _[[étale groupoid|étale]]_ if its target map

$$
  t \colon \mathcal{G}_1 \longrightarrow \mathcal{G}_0
$$

is a [[local diffeomorphism]].

=--

+-- {: .num_remark #ImplicitConditionsInEtaleGroupoidDef}
###### Remark

The condition in def. \ref{EtaleGroupoidTraditional} implies that all the other structure maps are local diffeomorphisms, too:

Inversion $(-)^{-1}\colon \mathcal{G}_1\stackrel{\simeq}{\to} \mathcal{G}_1$ is even a global [[diffeomorphism]]. Hence if the target map is a local diffeomorphism then the source map $s = t \circ (-)^{-1}$ is the composite of two local diffeos and as such itself a local diffeo.

The identity-assigning map $i \colon \mathcal{G}_0 \to \mathcal{G}_1$ is a [[section]] of a local diffeo (either $s$ or $t$) and hence itself a local diffeo. 

The two projections out of $\mathcal{G}_1 \underset{\mathcal{G}_0}{\times} \mathcal{G}_1$ are pullbacks of local diffeos, and hence themselves local diffeos. 

=--


Given a [[Lie groupoid]] 
we write
$\mathcal{G}_0 \longrightarrow \mathcal{G}$ for the corresponding [[differentiable stack]] with [[atlas]].


+-- {: .num_prop #EtaleGroupoidByInfinitesimalShape}
###### Proposition

A [[Lie groupoid]] $\mathcal{G}_\bullet$ is an [[étale groupoid]], def. \ref{EtaleGroupoidTraditional}, precisely if $\mathbb{G}_0 \to \mathcal{G}$ is a [[local diffeomorphism]] of smooth groupoids, def. \ref{} in that

$$
  \array{
    \mathcal{G}_0 &\longrightarrow& \Im \mathcal{G}_0
    \\
    \downarrow && \downarrow
    \\
    \mathcal{G} &\longrightarrow& \Im \mathcal{G}
  }
$$

is a [[homotopy pullback]] diagram of [[formal smooth groupoids]]

=--

+-- {: .proof}
###### Proof

We compute the homotopy pulback by fibrant presentation of the morphism on the right, via the [[factorization lemma]].

$$
  \array{
    \mathcal{G}_0 \underset{\mathcal{G}_\bullet}{\times} \mathcal{G}^I_\bullet  &\longrightarrow& \Im \mathcal{G}_0 \underset{\Im\mathcal{G}_\bullet}{\times} \Im\mathcal{G}^I_\bullet
    \\
    \downarrow && \downarrow
    \\
    \mathcal{G}_\bullet &\longrightarrow& \Im \mathcal{G}_\bullet
  }
$$

Inspection shows that in degree 0 this diagram is just the naturality square of the $\Im$-unit on the target map $t\colon \mathcal{G}_1 \to \mathcal{G}_0$. Hence by prop. \ref{TraditionalLocalDiffeosByModality} this is a pullback in degree-0 precisely already if $\mathcal{G}_\bullet$ is &#233;tale. By remark \ref{ImplicitConditionsInEtaleGroupoidDef} this implies that the projection $p_2 \colon \mathcal{G}_1\underset{\mathcal{G}_0}{\times}\mathcal{G}_1 \to \mathcal{G}_1$ is a local diffeo, and that is equivalent to the above diagram being a pullback in degree 1.

=--

+-- {: .num_remark}
###### Remark

In view of def./prop. \ref{ManifoldsAsEtaleGroupoids}, 
prop. \ref{EtaleGroupoidByInfinitesimalShape} gives that [[étale groupoids]] are precisely the "1-higher manifolds". For historical reasons this kind of statement is more prominent in the context of [[algebraic geometry]], where it essentially corresponds to regarding [[Artin stacks]] (in particular [[Deligne-Mumford stacks]]) as higher or [[derived schemes]].



=--

### Semantics Layer

#### Differential cohesion

[[differential cohesion]]


#### $V$-Manifolds
 {#Manifolds}


+-- {: .num_defn #LocalDiffeomorphisms}
###### Definition

Given $X,Y\in \mathbf{H}$ then a morphism $f \;\colon\; X\longrightarrow Y$ is a _[[local diffeomorphism]]_ if its naturality square of the [[infinitesimal shape modality]]

$$
  \array{
    X &\longrightarrow& \Im X
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{\Im f}}
    \\
    Y &\longrightarrow& \Im Y
  }
$$

is a [[pullback]] square. 

=--

+-- {: .num_remark}
###### Remark

The abstract definition \ref{LocalDiffeomorphisms} comes down to being the appropriate [[synthetic differential supergeometry]]-version  of the traditional statement that $f$ is a [[local diffeomorphism]] if the diagram of [[tangent bundles]]

$$
  \array{
    T X &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{T f}} && \downarrow^{\mathrlap{f}}
    \\
    T Y &\longrightarrow& Y
  }
$$

To see this, notice by the discussion at _[[synthetic differential geometry]]_ that for $D$ an [[infinitesimally thickened point]], then for any $X \in \mathbf{H}$ the [[mapping space]] $[D,X]$ is the [[jet bundle]] of $X$ with jets of order as encoded by the infinitesimal order of $D$. In particular if $\mathbb{D}^1(1)$ is the first order infinitesimal interval defined by the fact that its [[algebra of functions]] is the [[algebra of dual numbers]] $C^\infty(\mathbb{D}^1(1)) = (\mathbb{R} \oplus \epsilon \mathbb{R})/(\epsilon^2)$, and $X$ is a [[smooth manifold]], then 

$$
  [\mathbb{D}^1(1), X]\simeq T X
$$

is the ordinary [[tangent bundle]] of $X$. Now use that the [[internal hom]] $[D,-]$ preserves [[limits]] in its second argument, and that, by the hom-adjunction, $\mathbf{H}(U, [D,X]) \simeq \mathbf{H}(U \times D, X)$ and finally use that $\mathbf{H}(U \times D, \Im X)\simeq \mathbf{H}(\Re(U \times D), X)\simeq \mathbf{H}(U,X)$.


=--

Let now $V \in \mathbf{H}$ be given, equipped with the structure of a [[group]] ([[infinity-group]]).

+-- {: .num_defn #VManifold}
###### Definition

A _$V$-[[manifold]]_ is an $X \in \mathbf{H}$ such that there exists a _$V$-[[atlas]]_, namely a [[correspondence]] of the form

$$
  \array{
    && U
    \\
    & \swarrow && \searrow
    \\
    V && && X
  }
$$

with both morphisms being [[local diffeomorphisms]], def. \ref{LocalDiffeomorphisms}, and the right one in addition being an [[epimorphism]], hence an [[atlas]].

=--


+-- {: .num_prop}
###### Proposition

If $f \;\colon\; X \longrightarrow Y$ is a [[local diffeomorphism]],
def. \ref{LocalDiffeomorphisms}, then so is image
$\stackrel{\rightsquigarrow}{f}\colon \stackrel{\rightsquigarrow}{X} \longrightarrow \stackrel{\rightsquigarrow}{Y}$ under the [[bosonic modality]].

=--

+-- {: .proof}
###### Proof

Since the [[bosonic modality]] provides [[Aufhebung]] for $\Re\dashv \Im$ by prop. \ref{Sublations} we have $\rightsquigarrow \Im \simeq \Im$. Moreover $\Im \rightsquigarrow \simeq \Im$ anyway. Finally $\rightsquigarrow$ preserves [[pullbacks]] (being in particular a [[right adjoint]]). Hence hitting a pullback diagram

$$
  \array{
    X &\longrightarrow& \Im X
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{\Im f}}
    \\
    Y &\longrightarrow& \Im Y
  }
$$

with $\rightsquigarrow\;\;$ yields a pullback diagram

$$
  \array{
    \stackrel{\rightsquigarrow}{X} &\longrightarrow& \Im \stackrel{\rightsquigarrow}{X}
    \\
    \downarrow^{\mathrlap{\stackrel{\rightsquigarrow}{f}}} && \downarrow^{\mathrlap{\Im \stackrel{\rightsquigarrow}{f}}}
    \\
    \stackrel{\rightsquigarrow}{Y} &\longrightarrow& \Im \stackrel{\rightsquigarrow}{Y}
  }
$$

=--

+-- {: .num_cor }
###### Corollary

The bosonic space $\stackrel{\rightsquigarrow}{X}$ underlying 
a $V$-manifold $X$, def. \ref{VManifold}, is a $\stackrel{\rightsquigarrow}{V}$-manifold

=--

#### Frame bundles
 {#FrameBundles}

+-- {: .num_defn #GeneralLinearGroup}
###### Definition

The _[[general linear group]]_ $GL(V)$ is the [[automorphism infinity-group]] of the [[infinitesimal neighbourhood]] $\mathbb{D}^V_e$, def. \ref{InfinitesimalDiskBundle}, of the neutral element $e \colon \ast \to \mathbb{D}^V_e \to V$:

$$
  GL(V) \coloneqq \mathbf{Aut}(\mathbb{D}^V_e)
  \,.
$$

=--

+-- {: .num_prop #FrameBundle}
###### Proposition

For $X$ a $V$-manifold, def. \ref{VManifold}, then its infinitesimal disk bundle $T_{inf} X \to X$,
def. \ref{InfinitesimalDiskBundle}, is [[associated infinity-bundle|associated]]
to a $GL(V)$-[[principal infinity-bundle|principal]] $Fr(X) \to X$ -- to be called the _[[frame bundle]]_, [[modulating morphism|modulated]] by a map to be called $\tau_X$, producing [[homotopy pullbacks]] of the form

$$
  \array{
     T_{inf} X &\longrightarrow& V/GL(V)
     \\
     \downarrow && \downarrow
     \\
     X &\stackrel{\tau_X}{\longrightarrow}& \mathbf{B} GL(V)
  }
  \;\;\;
  \array{
     Fr(X) &\longrightarrow& \ast
     \\
     \downarrow && \downarrow
     \\
     X &\stackrel{\tau_X}{\longrightarrow}& \mathbf{B} GL(V)
  }
  \,.
$$

=--

+-- {: .num_defn #Framing}
###### Definition

A [[framing]] of a $V$-manifold is a trivialization of its [[frame bundle]], prop. \ref{FrameBundle}, hence a diagram in $\mathbf{H}$ of the fomr

$$
  \array{
    X && \longrightarrow && \ast
    \\
    & \searrow &\swArrow& \swarrow
    \\
    && \mathbf{B}GL(V)
  }
$$


=--

+-- {: .num_remark #ModuliForFramings}
###### Remark

It is useful to express def. \ref{Framing} in terms of the [[slice topos]] $\mathbf{H}_{/\mathbf{B}GL(V)}$. Write $V\mathbf{Frame}\in \mathbf{H}_{/\mathbf{B}GL(V)}$ for the canonical morphism $\ast \to \mathbf{B}GL(V)$ regarded as an object in the slice. Then a framing as in def. \ref{Framing} is equivalently a morphism

$$
  \phi \colon \tau_X \longrightarrow V\mathbf{Frame}
$$

in $\mathbf{H}_{/\mathbf{B}GL(V)}$.

=--

+-- {: .num_prop #LeftTranslationFraming}
###### Proposition

The[[group object]] $V$, canonically regarded as a $V$-manifold, carries a canonical framing, def. \ref{Framing}, $\phi_{li}$, induced by left translation. 

=--


### Syntax Layer 

(...)

[[!redirects formal smooth set]]
[[!redirects formal smooth sets]]