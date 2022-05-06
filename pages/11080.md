

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


> This entry one chapter of _[[geometry of physics]]_.

> previous chapters: _[[geometry of physics -- categories and toposes|categories and toposes]]_

> next chapters: _[[geometry of physics -- supergeometry|supergeometry]]_, _[[geometry of physics -- smooth homotopy types|smooth homotopy types]]_


$\,$

$\,$

This chapter introduces a generalized kind of [[sets]] equipped with [[smooth structure]], to be called _[[smooth sets]]_ or, with an eye towards their generalization to _[[geometry of physics -- smooth homotopy types|smooth homotopy types]]_, _smooth [[h-sets]]_ or _smooth [[homotopy 0-types|0-types]]_[^terminology].

The definition (Def. \ref{SmoothSpace} below) subsumes that of [[smooth manifolds]], [[Fréchet manifolds]] and [[diffeological spaces]] but is both simpler and more powerful: smooth sets are simply [[sheaves]] on the [[gros site]] of [[Cartesian Spaces]] (Prop. \ref{CartSpCategory} below) and as such form a nice [[category]] -- a [[topos]] -- and this contains as [[full subcategories]] the more "tame" objects such as [[smooth manifolds]] (Prop. \ref{InclusionOfSmoothManifoldsIntoSmoothSets} below) and [[diffeological spaces]] (Prop. \ref{DiffeologicalSpacesAreTheConcreteSmoothSets} below).

In fact smooth sets are an early stage in a long sequence of generalized smooth spaces appearing in [[higher differential geometry]]:

$\,$
<br/>$\;\;\;\;$ $\{$[[coordinate systems]]$\}$
<br/>$\hookrightarrow$ $\{$[[smooth manifolds]]$\}$ $\phantom{AA}$ (Prop. \ref{InclusionOfSmoothManifoldsIntoSmoothSets} below)
<br/>$\hookrightarrow$ $\{$[[Hilbert manifolds]]$\}$
<br/>$\hookrightarrow$ $\{$[[Banach manifolds]]$\}$
<br/>$\hookrightarrow$ $\{$[[Fréchet manifolds]]$\}$ $\phantom{AA}$ (Prop. \ref{FrechetManifoldsFullyFaithfulInSmoothSets} below)
<br/>$\hookrightarrow$ $\{$[[diffeological spaces]]$\}$ $\phantom{AA}$ (Prop. \ref{ReflectiveInclusionOfDiffeologicalSpacesinSmoothSets} below)
<br/>$\hookrightarrow$ $\{$[[smooth sets]]$\}$ $\hookrightarrow$ $\{$[[formal smooth sets]]$\}$ $\hookrightarrow$ $\{$[[super formal smooth sets]]$\}$ $\phantom{AA}$ (chapter [[geometry of physics -- supergeometry|on supergeometry]])
<br/>
<br/>$\hookrightarrow$ $\{$[[orbifold|smooth orbifolds]]$\}$
<br/>$\hookrightarrow$ $\{$[[smooth groupoids]]$\}$
<br/>$\hookrightarrow $ $\{$[[smooth 2-groupoids]]$\}$
<br/>$\hookrightarrow $ $\cdots$
<br/>$\hookrightarrow $ $\{$[[smooth ∞-groupoids]]$\}$ $\phantom{AA}$ (chapter [[geometry of physics -- smooth homotopy types|on smooth ∞-groupoids]])
<br/>$\hookrightarrow $ $\{$[[formal smooth ∞-groupoids]]$\}$
<br/>$\hookrightarrow $ $\{$[[super formal smooth ∞-groupoids]]$\}$



[^terminology]: In view of the _[[smooth homotopy types]]_ to be discussed in _[[geometry of physics -- smooth homotopy types]]_, the structures discussed now are properly called _smooth [[0-types]]_ or maybe _smooth [[h-sets]]_ or just _smooth sets_. While this subsumes [[smooth manifolds]] which are indeed sets equipped with (particularly nice) [[smooth structure]], it is common in practice to speak of manifolds as "spaces" (indeed as [[topological spaces]] equipped with smooth structure). Historically the _[[Cartesian space]]_ and _[[Euclidean space]]_ of [[Newtonian physics]] are the archetypical examples of smooth manifolds and modern [[differential geometry]] developed very much via motivation by the study of the _spaces_ in [[general relativity]], namely _[[spacetimes]]_. Unfortunately, in a parallel development the word "space" has evolved in [[homotopy theory]] to mean (just) the [[homotopy types]] _represented_ by an actual [[topological space]] (their [[fundamental infinity-groupoids]]). Ironically, with this meaning of the word "space" the original [[Euclidean spaces]] become equivalent to the point, signifying that the modern meaning of "space" in [[homotopy theory]] is quite orthogonal to the original meaning, and that in homotopy theory therefore one should better stick to "[[homotopy types]]". Since historically grown terminology will never be fully logically consistent, and since often the less well motivated terminology is more widely understood, we will follow tradition here and take the liberty to use "smooth sets" and "smooth spaces" synonymously, the former when we feel more formalistic, the latter when we feel more relaxed.

$\,$


#Contents#
* table of contents
{:toc}



## Abstract coordinate systems
 {#CoordinateSystemsLayerMod}


As discussed in the chapter _[[geometry of physics -- categories and toposes|categories and toposes]]_, every kind of _[[geometry]]_ is modeled on a collection of [[generator|archetypical]] basic [[spaces]] and geometric [[homomorphisms]] between them. In [[differential geometry]] the archetypical spaces are the abstract standard [[Cartesian space|Cartesian coordinate systems]], denoted $\mathbb{R}^n$ (in every [[dimension]] $n \in \mathbb{N}$). The geometric homomorphism between them are [[smooth functions]] $\mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$, hence smooth (and possibly degenerate) [[coordinate transformations]].

Here we introduce the basic concept, organizing them in the [[category]] [[CartSp]] of [[Cartesian spaces]] (Prop. \ref{CartSpCategory} below.) We highlight three classical theorems about [[smooth functions]] in Prop. \ref{AlgebraicFactsOfDifferentialGeometry} below, which look innocent but play a decisive role in setting up [[synthetic differential geometry|synthetic differential]] [[supergeometry]] based on the concept of abstract smooth coordinate systems.

At this point these are not yet coordinate systems _on_ some other space. But by applying the general machine of [[geometry of physics -- categories and toposes|categories and toposes]] to these, a concept of [[generalized spaces]] modeled on these abstract coordinate systems is induced. These are the _[[smooth sets]]_ discussed in the next chapter  _[[geometry of physics -- smooth sets]]_.


### The continuum real line
 {#TheContinuumRealWorldLine}

The fundamental premise of [[differential geometry]] as a model of [[geometry]] in [[physics]] is the following.

**Premise.** _The abstract [[worldline]] of any [[particle]] is modeled by the [[continuum]] [[real line]] $\mathbb{R}$._

This comes down to the following sequence of premises.

1. There is a [[linear ordering]] of the [[points]] on a [[worldline]]: in particular if we pick points at some intervals on the worldline we may label these in an order-preserving way by [[integers]]

   $\mathbb{Z}$.

1. These intervals may each be subdivided into $n$ smaller intervals, for each natural number $n$. Hence we may label points on the [[worldline]] in an order-preserving way by the [[rational numbers]]

   $\mathbb{Q}$.

1. This labeling is dense: every point on the worldline is the [[supremum]] of an [[inhabited set|inhabited]] [[bounded subset]] of such labels. This means that a [[worldline]] [[equivalence|is]] the _[[real line]]_, the [[continuum]] of [[real numbers]]

   $\mathbb{R}$.
  
The adjective "real" in "[[real number]]" is a historical shadow of the old idea that real numbers are related to _observed reality_, hence to [[physics]] in this way. The experimental success of this assumption shows that it is valid at least to very good approximation. 


### Cartesian spaces and smooth functions
 {#CartesianSpaces}



+-- {: .num_defn #SmoothFunctions}
###### Definition
**([[smooth function]])**

A [[function]] of [[sets]] $f : \mathbb{R} \to \mathbb{R}$ is called 
a **[[smooth function]]** if, [[coinduction|coinductively]]:

1. the [[derivative]] $\frac{d f}{d x} : \mathbb{R} \to \mathbb{R}$ exists;

1. and is itself a smooth function.

We write $C^\infty(\mathbb{R}) \in Set$ for the [[set]] of all smooth functions on $\mathbb{R}$.

=--

+-- {: .num_remark}
###### Remark

The superscript "${}^\infty$" in "$C^\infty(\mathbb{R})$" refers to the order of the [[derivatives]] that exist for smooth functions. More generally for $k \in \mathbb{N}$ one writes $C^k(\mathbb{R})$ for the set of $k$-fold [[differentiable functions]] on $\mathbb{R}$. These will however not play much of a role for our discussion here. 

=--


+-- {: .num_defn #CartesianSpaceAndHomomorphism}
###### Definition
**([[Cartesian spaces]] and [[smooth functions]])**

For $n \in \mathbb{N}$, the **[[Cartesian space]]** $\mathbb{R}^n$ is the set

$$
  \mathbb{R}^n = \{ (x^1 , \cdots, x^{n}) | x^i \in \mathbb{R} \}
$$

of $n$-[[tuples]] of [[real numbers]]. For $1 \leq k \leq n$ write

$$
  i^k : \mathbb{R} \to \mathbb{R}^n
$$

for the [[function]] such that $i^k(x) = (0, \cdots, 0,x,0,\cdots,0)$ is the [[tuple]] whose $k$th entry is $x$ and all whose other entries are $0 \in \mathbb{R}$; and write

$$
  \mathbb{p}^k : \mathbb{R}^n \to \mathbb{R}
$$

for the function such that $p^k(x^1, \cdots, x^n) = x^k$.

A **[[homomorphism]]** of Cartesian spaces is a _[[smooth function]]_

$$
  f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}
  \,,
$$

hence a [[function]] $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ such that all [[partial derivatives]] exist and are [[continuous map|continuous]].

=--

+-- {: .num_example}
###### Example

Regarding $\mathbb{R}^n$ as an $\mathbb{R}$-[[vector space]], 
every [[linear function]] $\mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$
is in particular a [[smooth function]].

=--

+-- {: .num_remark}
###### Remark

But a homomorphism of Cartesian spaces in def. \ref{CartesianSpaceAndHomomorphism} is _not_ required to be a [[linear map]]. We do _not_ regard the Cartesian spaces here as [[vector spaces]]. 

=--

+-- {: .num_defn}
###### Definition

A [[smooth function]] $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ is called a **[[diffeomorphism]]** if there exists another smooth function 
$\mathbb{R}^{n_2} \to \mathbb{R}^{n_1}$ such that the underlying functions of sets are [[inverse]] to each other

$$
  f \circ g = id
$$

and

$$
  g \circ f = id
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

There exists a [[diffeomorphism]] $\mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ precisely if $n_1 = n_2$.

=--

+-- {: .num_defn #CartesianSpacesAndSmoothFunctions}
###### Definition

We will also say equivalently that

1. a [[Cartesian space]] $\mathbb{R}^n$ is an **[[coordinate system|abstract coordinate system]]**;

1. a [[smooth function]] $\mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ is an **[[coordinate transformation|abstract coordinate transformation]]**;

1. the [[function]] $p^k : \mathbb{R}^{n} \to \mathbb{R}$ is the $k$th **[[coordinate]]** of the coordinate system $\mathbb{R}^n$. We will also write this function as $x^k : \mathbb{R}^{n} \to \mathbb{R}$.

1. for $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ a [[smooth function]], and $1 \leq k \leq n_2$ we write

   1. $f^k \coloneqq p^k\circ f$

   1. $(f^1, \cdots, f^n) \coloneqq f$.

=--

+-- {: .num_remark }
###### Remark

It follows with this notation that

$$
  id_{\mathbb{R}^n} = (x^1, \cdots, x^n) : \mathbb{R}^n \to \mathbb{R}^n
  \,.
$$

Hence an abstract coordinate transformation 

$$ 
  f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}
$$

may equivalently be written as the tuple

$$
  \left(
    f^1 \left( x^1, \cdots, x^{n_1} \right)
    ,
    \cdots,
    f^{n_2}\left( x^1, \cdots, x^{n_1} \right)
  \right)
  \,.
$$

=--



### The magic properties of smooth functions
 {#PropertiesOfSmoothFunctions}

Below we encounter generalizations of ordinary [[differential geometry]] that include explicit "[[infinitesimals]]" in the guise of _[[infinitesimally thickened points]]_, as well as "super-graded infinitesimals", in the guise of _[[superpoints]]_ (necessary for the
description of [[fermion fields]] such as the [[Dirac field]]). As we discuss [below](#FieldBundles), these structures are
naturally incorporated into [[differential geometry]] in just the same way as [[Grothendieck]]
introduced them into [[algebraic geometry]] (in the guise of "[[formal schemes]]"),
namely in terms of [[formal dual|formally dual]] [[rings of functions]] with [[nilpotent ideals]].
That this also works well for [[differential geometry]] rests on the following three
basic but important properties, which say that [[smooth functions]] behave "more algebraically"
than their definition might superficially suggest:


+-- {: .num_prop #AlgebraicFactsOfDifferentialGeometry}
###### Proposition
**(the three magic algebraic properties of [[differential geometry]])**

1. **[[embedding of smooth manifolds into formal duals of R-algebras|embedding of Cartesian spaces into formal duals of R-algebras]]**

   For $X$ and $Y$ two [[Cartesian spaces]], the [[smooth functions]] $f \colon X \longrightarrow Y$
   between them (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}) are in [[natural bijection]] with their
   induced algebra [[homomorphisms]] $C^\infty(X) \overset{f^\ast}{\longrightarrow} C^\infty(Y)$ (example \ref{AlgebraOfSmoothFunctionsOnCartesianSpaces}), so that
   one may equivalently handle [[Cartesian spaces]] entirely via their $\mathbb{R}$-algebras of smooth functions.

   Stated more [[category theory|abstractly]], this means equivalently that the [[functor]] $C^\infty(-)$ that
   sends a [[smooth manifold]] $X$ to its $\mathbb{R}$-[[associative algebra|algebra]]
   $C^\infty(X)$ of [[smooth functions]] (example \ref{AlgebraOfSmoothFunctionsOnCartesianSpaces}) is a _[[fully faithful functor]]_:

   $$
     C^\infty(-)
     \;\colon\;
     SmthMfd \overset{\phantom{AAAA}}{\hookrightarrow} \mathbb{R} Alg^{op}
     \,.
   $$

   ([Kolar-Slovak-Michor 93, lemma 35.8, corollaries 35.9, 35.10](embedding+of+smooth+manifolds+into+formal+duals+of+R-algebras#KolarSlovakMichor93))


1. **[[smooth Serre-Swan theorem|embedding of smooth vector bundles into formal duals of R-algebra modules]]**

   For $E_1 \overset{vb_1}{\to} X$ and $E_2 \overset{vb_2}{\to} X$ two [[vector bundle]] there is then a [[natural bijection]] between vector bundle [[homomorphisms]] $f \colon E_1 \to E_2$ and the [[homomorphisms]] of [[modules]] $f_\ast \;\colon\; \Gamma_X(E_1) \to \Gamma_X(E_2)$ that these induces between the [[spaces of sections]].

   More [[category theory|abstractly]] this means that the [[functor]] $\Gamma_X(-)$ is a [[fully faithful functor]]

   $$
     \Gamma_X(-) \;\colon\; VectBund_X \overset{\phantom{AAAA}}{\hookrightarrow} C^\infty(X) Mod
   $$

   ([Nestruev 03, theorem 11.29](smooth+Serre-Swan+theorem#Nestruev03))

   Moreover, the [[modules]] over the $\mathbb{R}$-algebra $C^\infty(X)$
   of [[smooth functions]] on $X$ which arise this way as [[sections]] of [[smooth vector bundles]] over
   a [[Cartesian space]] $X$
   are precisely the [[finitely generated module|finitely generated]] [[free modules]] over $C^\infty(X)$.

   ([Nestruev 03, theorem 11.32](smooth+Serre-Swan+theorem#Nestruev03))


1. **[[derivations of smooth functions are vector fields|vector fields are derivations of smooth functions]]**.

   For $X$ a [[Cartesian space]] (Def. \ref{CartesianSpaceAndHomomorphism}),
   then any [[derivation]] $D \colon  C^\infty(X) \to C^\infty(X)$ on
   the $\mathbb{R}$-[[associative algebra|algebra]]
   $C^\infty(X)$ of [[smooth functions]] is given by [[differentiation]] with respect to a uniquely defined smooth [[tangent vector field]]: The function that regards [[tangent vector fields]] as [[derivations]]

   $$
     \array{
       \Gamma_X(T X)
         &\overset{\phantom{A}\simeq\phantom{A}}{\longrightarrow}&
       Der(C^\infty(X))
       \\
       v &\mapsto& D_v
     }
   $$

   is in fact an [[isomorphism]].

   (This follows directly from the _[[Hadamard lemma]]_.)

=--

Actually all three statements in prop. \ref{AlgebraicFactsOfDifferentialGeometry}
hold not just for [[Cartesian spaces]], but generally for [[smooth manifolds]] (def./prop. \ref{SmoothManifoldInsideDiffeologicalSpaces} below; if only we generalize in the second statement from [[free modules]] to [[projective modules]].
However for our development here it is useful to first focus on just [[Cartesian spaces]] and then bootstrap
the theory of [[smooth  manifolds]] and much more from that, which we do [below](#FieldBundles).

$\,$

### The site of abstract coordinate systems
 {#CoordinateSystemsLayerSem}

Much of the above disucssion is usefully summarized by saying that abstract coordinate systems with smooth functions between them form a _[[category]]_ (Prop. \ref{CartSpCategory} below). Equipped with the information of how one abstract coordinate system may be _covered_ by other coordinate systems (Def. \ref{DifferentiallyGoodOpenCover} below), this becomes a _[[site]]_ (Prop. \ref{TheDifferentiallyGoodOpenCoverCoverage}) below.

$\,$

+-- {: .num_prop #CartSpCategory}
###### Propositions
**(the [[category]] [[CartSp]] of abstract [[coordinate systems]]/[[Cartesian spaces]])**

Abstract coordinate systems according to prop. \ref{CartesianSpacesAndSmoothFunctions} form a _[[category]]_ ([this def.](geometry+of+physics+--+Categories+and+Toposes#Categories))
-- to be denoted _[[CartSp]]_ -- whose

* [[objects]] are the abstract coordinate systems $\mathbb{R}^{n}$ (the [[class]] of objects is the [[set]] $\mathbb{N}$ of [[natural numbers]] $n$);

* [[morphisms]] $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ are the abstract [[coordinate transformations]] = [[smooth functions]].

Composition of morphisms is given by [[composition]] of [[functions]].

Under this identification

1. The [[identity morphisms]] are precisely the [[identity functions]].

1. The [[isomorphisms]] are precisely the [[diffeomorphisms]].

=--


We discuss a standard structure of a _[[site]]_ on the category [[CartSp]]. Following _[[Sketches of an Elephant|Johnstone -- Sketches of an Elephant]]_, it will be useful and convenient to regard a site as a ([[small site|small]]) category equipped with a _[[coverage]]_. This generates a genuine [[Grothendieck topology]], but need not itself already be one.

+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}$ the standard [[open ball|open n-ball]] is the subset

$$
  D^n = \{ (x_i)_{i =1}^n \in \mathbb{R}^n | \sum_{i = 1}^n (x_i)^2 \lt 1 \}  \hookrightarrow \mathbb{R}^n
  \,.
$$


=--

+-- {: .num_prop}
###### Proposition

There is a [[diffeomorphism]]

$$
  \mathbb{R}^n \stackrel{\simeq}{\to} D^n
  \,.
$$

=--


+-- {: .num_defn #DifferentiallyGoodOpenCover}
###### Definition
**(differentially [[good open covers]])**

A **differentially [[good open cover]]** of a [[Cartesian space]] $\mathbb{R}^n$ is a set $\{U_i \hookrightarrow \mathbb{R}^n\}$ of [[open subset]] inclusions of Cartesian spaces such that these [[open cover|cover]] $\mathbb{R}^n$
and such for each non-empty finite [[intersection]] there exists a [[diffeomorphism]] 

$$
  \mathbb{R}^n \stackrel{\simeq}{\to} U_{i_1} \cap \cdots \cap U_{i_k}
$$

that identifies the $k$-fold intersection with a Cartesian space itself.

=--

+-- {: .num_remark}
###### Remark

Differentiably good covers are useful for computations. Their full impact is however on the [[homotopy theory]] of [[simplicial presheaves]] over [[CartSp]]. This we discuss in the chapter on [[geometry of physics -- smooth homotopy types|smooth homotopy types]], around [this prop.](geometry+of+physics+--+smooth homotopy types#DifferentiablyGoodCoverGivesSPlitHyperCoverOverCartSp).

=--



+-- {: .num_lemma #DiffGoodOpenCoversRefineOpenCovers}
###### Lemma
**(every [[open cover]] has refinement by a differentially [[good open cover]])**

Every [[open cover]] of a [[smooth manifold]] has a refinement by a differentially good open cover, according to Def. \ref{DifferentiallyGoodOpenCover}. 

=--

For proof see [FSS10, Prop. A1](https://ncatlab.org/schreiber/show/Cech+Cocycles+for+Differential+characteristic+Classes), or see at _[[good open cover]]_. 

+-- {: .num_remark}
###### Remark

Lemma \ref{DiffGoodOpenCoversRefineOpenCovers} is not quite a classical statement. The classical statement is only that every open cover is refined by a _topologically_ [[good open cover]]. See the comments _[here in the references-section](ball#References)_ at _[[open ball]]_ for the situation concerning this statement in the literature.

=--

+-- {: .num_remark}
###### Remark

The _good_ open covers do not yet form a [[Grothendieck topology]] on [[CartSp]]. One of the axioms of a Grothendieck topology is that for every [[covering]] family also its [[pullback]] along any morphism in the category is a covering family. But while the pullback of every [[open cover]] is again an open cover, and hence open covers form a Grothendieck topology on [[CartSp]], not every pullback of a _[[good open cover|good]]_ open cover is again _good_.

=--

+-- {: .num_example #ExampleThatGoodOpenCoversAreNotPullbackStable}
###### Example

Let $\{\mathbb{R}^2\stackrel{\phi_{i}}{\hookrightarrow}\mathbb{R}^2\}_{i \in \{1,2\}}$ be the [[open cover]] of the [[plane]] by an open left half space

$$
   \mathbb{R}^2 \simeq \{ (x_1,x_2) \in \mathbb{R}^2 | x_1 \lt 1 \} \stackrel{\phi_1}{\hookrightarrow} \mathbb{R}^2
$$

and a right open half space

$$
   \mathbb{R}^2 \simeq \{ (x_1,x_2) \in \mathbb{R}^2 | x_1 \gt -1 \} \stackrel{\phi_2}{\hookrightarrow} \mathbb{R}^2
  \,.
$$

The intersection of the two is the open strip

$$
  \mathbb{R}^2 \simeq \{ (x_1, x_2) \in \mathbb{R}^2 | -1 \lt x_1 \lt 1 \}
  \hookrightarrow 
  \mathbb{R}^2
  \,.
$$

So this is a [[good open cover]] of $\mathbb{R}^2$. 

But consider then the smooth function 

$$
  2(\cos(2 \pi (-)), \sin(2 \pi (-))) \colon \mathbb{R}^1 \to \mathbb{R}^2 
$$

which sends the line to a curve in the plane that periodically goes around the [[circle]] of radius 2 in the plane. 

Then the pullback of the above good open cover on $\mathbb{R}^2$ to $\mathbb{R}^1$ along this function is an [[open cover]] of $\mathbb{R}$ by two open subsets, each being a disjoint union of countably many open [[intervals]] in $\mathbb{R}$. 
Each of these open intervals is an open 1-ball hence diffeomorphic to $\mathbb{R}^1$, but their _[[disjoint union]]_ is not [[contractible topological space|contractible]] (it does not contract to the point, but to many points!). 

So the pullback of the good open cover that we started with is an open cover which is not _good_ anymore. But it has an evident _refinement_ by a good open cover. 

=--

This is a special case of what the following statement says in generality.

+-- {: .num_prop #TheDifferentiallyGoodOpenCoverCoverage}
###### Proposition
**(the [[site]] of [[Cartesian spaces]] with differentially [[good open covers]])**

The differentially [[good open covers]], Def. \ref{DifferentiallyGoodOpenCover}, constitute a [[coverage]] ([this Def.](geometry+of+physics+--+categories+and+toposes#Coverage)) on the [[category]] [[CartSp]] (from Prop. \ref{CartSpCategory}). 

Hence [[CartSp]] equipped with this coverage is a [[site]] ([this def.](geometry+of+physics+--+categories+and+toposes#Coverage)).

=--

+-- {: .proof}
###### Proof

By definition of [[coverage]] we need to check that for $\{U_i \hookrightarrow \mathbb{R}^n\}_{i \in I}$ any [[good open cover]] and $f \colon \mathbb{R}^k \to \mathbb{R}^n$ any smooth function, we can find a good open cover $\{K_j \to \mathbb{R}^k\}_{j \in J}$ and a [[function]] $J \to I$ such that for each $j \in J$ there is a smooth function $\phi \colon K_j \to U_{\rho(j)}$ that makes this [[diagram]] 
[[commuting diagram|commute]]:

$$
  \array{

    K_j &\stackrel{\phi}{\to}& U_{i(j)}
    \\
    \downarrow && \downarrow
    \\
    \mathbb{R}^k &\stackrel{f}{\to}& \mathbb{R}^n
  }
  \,.
$$

To obtain this, let $\{f^* U_i \to \mathbb{R}^k\}$ be the pullback of the original covering family, in that 

$$
  f^* U_i \coloneqq \{ x \in \mathbb{R}^k | f(x) \in U_i \}
  \hookrightarrow \mathbb{R}^k
  \,.
$$

This is evidently an [[open cover]], albeit not necessarily a _[[good open cover]]_. But by Lemma \ref{DiffGoodOpenCoversRefineOpenCovers} there does exist a good open cover $\{\tilde K_{\tilde j} \hookrightarrow \mathbb{R}^k\}_{\tilde j \in \tilde J}$ _refining_ it, which in turn means that for all $\tilde j$ there is  

$$
  \array{
    \tilde K_{\tilde j} &\to& K_{j(\tilde j)}
    \\
    \downarrow && \downarrow 
    \\
    \mathbb{R}^k &\stackrel{=}{\to}& \mathbb{R}^k
  }
  \,.
$$

Therefore then the [[pasting]] composite of these commuting squares 

$$
  \array{
    \tilde K_{\tilde j} &\to& K_{j(\tilde j)} &\to& U_{i(j(\tilde j))}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \mathbb{R}^k &\stackrel{=}{\to}& \mathbb{R}^k
   &\stackrel{f}{\to}& \mathbb{R}^n
  }
$$

solves the condition required in the definition of [[coverage]].

=--

By example \ref{ExampleThatGoodOpenCoversAreNotPullbackStable} this [[good open cover]] [[coverage]] is not a [[Grothendieck topology]]. But as any coverage, it uniquely completes to one which has the same [[sheaves]]:

+-- {: .num_prop #CompletingGoodOpenCoversToAllOpenCovers}
###### Proposition
**(completing [[good open covers]] to all [[open covers]])**

The [[Grothendieck topology]] induced on [[CartSp]] by the differentially good open cover coverage of def. \ref{TheDifferentiallyGoodOpenCoverCoverage} has as covering families the ordinary [[open covers]]. 

Hence if we explicitly write $CartSp_{good}$ and $CartSp_{Groth}$ for $CartSp$ equipped with the coverage of differentially good open covers as and that of all open covers, respectively, then there is an [[equivalence of categories]] ([this Def.](geometry+of+physics+--+categories+and+toposes#EquivalenceOfCategories)) between their [[categories of sheaves]] ([this Def.](geometry+of+physics+--+categories+and+toposes#Sheaf))

\[
  \label{SheavesOnGoodOpenCoversCoincideWithThosOnALlOpenCovers}
  Sh(CartSp_{\text{good open cov}})
  \;\simeq\;
  Sh(CartSp_{\text{all open cov}})
  \.
\]

=--

+-- {: .num_remark}
###### Remark

Prop. \ref{CompletingGoodOpenCoversToAllOpenCovers} means that for every sheaf-theoretic construction to follow we may just as well consider the Grothendieck topology of open covers on $CartSp$, and hence we may and will suppress the subscripts in (eq:SheavesOnGoodOpenCoversCoincideWithThosOnALlOpenCovers).  

While the sheaves of the open cover topology are the same as those of the good open cover coverage. But the latter is (more) useful for several computational purposes in the following. It is the _good_ open cover coverage that makes manifest, below, that sheaves on $CartSp$ form a [[locally connected topos]] and in consequence then a [[cohesive topos]]. This kind of argument becomes all the more pronounced as we pass [further below](#SmoothnGroupoids) to [[(∞,1)-sheaves]] on [[CartSp]]. This will be discussed in _[Smooth n-groupoids -- Semantic Layer -- Local Infinity-Connectedness](#InfinityConnectednessOfSmoothInfinityGrpd) below.

=--

There are further [[sites]] in use, which induce the same categories of sheaves:

+-- {: .num_defn #SiteOfSmoothManifolds}
###### Definition
**([[sites]] of [[smooth manifolds]] and [[open subsets]] of [[Euclidean spaces]])**

We write

* _[[SmthMfd]]_ for the [[category]] of [[smooth manifolds]] of any finite [[dimension]], with [[smooth functions]] between them;

* $EuclOp$ for the [[category]] of [[open subsets]] of [[Euclidean spaces]] of any finite [[dimension]], with [[smooth functions]] between them.

Both of these carry the respective [[coverage]] of [[good open covers]] and as such become [[sites]] ([this Def.](geometry+of+physics+--+categories+and+toposes#Coverage))

=--



## Smooth sets
 {#SmoothSpacesLayerMod}

In the section _[Coordinate systems](#CoordinateSystems)_ we have set up the archetypical [[spaces]] of [[differential geometry]]. Here we now define in terms of these the most general _[[smooth sets]]_ that differential geometry can deal with. 


### Plots of smooth sets and their gluing
 {#PlotsOfSmoothSpacesAndTheirGluing}

The general kind of "[[smooth space]]" that we want to consider is a [[type|something]] that can be _probed_ by laying out [[coordinate systems]]   inside it, as in [this definition](geometry+of+physics+--+coordinate+systems#CartesianSpaces), and which may be reconstructed by _gluing_ all the possible coordinate systems in it together.

At this point we want to impose no further conditions on a "space" than this. In particular we do not assume that we know beforehand a [[set]] of [[points]] underlying $X$. Instead, we define [[smooth sets]] $X$ (Def. \ref{SmoothSpace}, below) entirely _operationally_ as something about which we may ask "Which ways are there to lay out $\mathbb{R}^n$ inside $X$?" and such that there is a self-consistent answer to this question. 

By the discussion in the chapter _[[geometry of physics -- categories and toposes|categories and toposes]]_, this means that we should define a _[[smooth set]]_ to be a [[sheaf]] on a [[site]] of [[Cartesian spaces]].
The following definitions spell this out.  

The idea of the following definitions may be summarized like this:

1. a generalized _smooth set_ is something that may be probed by laying out coordinate systems into it, in a way that respects transformation of coordinate patches and gluing of coordinate patches;

1. the [[Yoneda lemma]] ([this prop](geometry+of+physics+--+categories+and+toposes#YonedaLemma)) says that this is consistent in that coordinate systems themselves as well as [[smooth manifolds]] may naturally be regarded as generalized smooth sets themselves and that under this identification "laying out a coordinate system" in a smooth set means having a map of smooth sets from the coordinate system to the smooth set.


The first set of consistency conditions on plots of a space is that they respect _coordinate transformations_. This is what the following definition formalises.

+-- {: .num_defn #SmoothPreSpace}
###### Definition
**(pre-smooth set)**

A **pre-smooth set** $X$ is

1. a collection of sets: for each [[Cartesian space]] $\mathbb{R}^n$ (hence for each [[natural number]] $n$) a [[set]]

   $$
     X(\mathbb{R}^n) \in Set
   $$

   -- to be thought of as the _set of ways of laying out $\mathbb{R}^n$ inside $X$_, also called the set of _plots_ of $X$, for short;

1. for each [[smooth function]] $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ (to be thought of as an abstract coordinate transformation) a [[function]] between the corresponding sets of plots

   $$
     X(f) \;\colon\; X(\mathbb{R}^{n_2}) \longrightarrow X(\mathbb{R}^{n_1})
   $$

   -- to be thought of as the function that sends a _plot_ of $X$ by $\mathbb{R}^{n_2}$ to the correspondingly transformed plot by $\mathbb{R}^{n_1}$ induced by laying out $\mathbb{R}^{n_1}$ inside $\mathbb{R}^{n_2}$.

such that this is compatible with coordinate transformations:

1. the [[identity]] coordinate transformation does not change the plots:

   $$
     X(id_{\mathbb{R}^n}) = id_{X(\mathbb{R}^n)}
     \,,
   $$

1. changing plots along two consecutive coordinate transformations $f_1 \colon \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ and $f_2 \colon \mathbb{R}^{n_2} \to \mathbb{R}^{n_3}$ is the same as changing them along the [[composition|composite]] coordinate transformation $f_2 \circ f_1$:


   $$
     X(f_1) \circ X(f_2)  = X(f_2 \circ f_1)
     \,.
   $$

=--

But there is one more consistency condition for a collection of plots to really be probes of some space: it must be true that if we glue small coordinate systems to larger ones, then the plots by the larger ones are the same as the plots by the collection of smaller ones that agree where they overlap. We first formalize this idea of "plots that agree where their coordinate systems overlap."

+-- {: .num_prop #DifferentiallyGoodOpenCover}
###### Definition
**(differentially [[good open cover]])**

For $\mathbb{R}^n$ a [[Cartesian space]], then 

1. an [[open cover]] 

   $$
     \{U_i \hookrightarrow X\}_{i \in I}
   $$ 
   
   is a set of [[open subsets]] of $X$, such that their [[union]] is $X$; hence $\underset{i \in I}{\cup} U_i = X$; 
   
1. this is a _[[good open cover]]_ if all the $U_i$ as well as all their [[inhabited set|non-empty]] finite [[intersections]]
   are [[homeomorphism|homeomorphic]] to [[open balls]], hence to $\mathbb{R}^n$ itself;
   
1. this is a _differentially good open cover_ if all the $U_i$ as well as all their [[inhabited set|non-empty]] finite [[intersections]]
   are [[diffeomorphism|diffeomorphic]] to [[open balls]], hence to $\mathbb{R}^n$ itself.
   

=--

+-- {: .num_defn #MatchingFamiliesOfPlots}
###### Definition
**(glued plots)**

Let $X$ be a pre-smooth set, def. \ref{SmoothPreSpace}.
For $\{U_i \to \mathbb{R}^n\}_{i \in I}$ a differentially [[good open cover]] (def. \ref{DifferentiallyGoodOpenCover}) let

$$
  GluedPlots(\{U_i \to \mathbb{R}^n\}, X) \in Set
$$

be the set of $I$-[[tuples]] of $U_i$-plots of $X$ which coincide on all double [[intersections]]

$$
  \array{
    && U_i \cap U_j
    \\
    & {}^{\mathllap{\iota_i}}\swarrow && \searrow^{\mathrlap{\iota_j}}
    \\
    U_i &&&& U_j
    \\
    & \searrow && \swarrow
    \\
    && \mathbb{R}^n
  }
$$

(also called the _[[matching families]]_ of $X$ over the given cover):

$$
  GluedPlots(\{U_i \to \mathbb{R}^n\}, X)
  \;\;\coloneqq\;\;
  \left\{
    \;
    \left(p_i \in X(U_i)\right)_{i \in I}
    \;|\;\;
    \forall_{i,j \in I} \;:\; X(\iota_i)(p_i) = X(\iota_j)(p_j)
    \;
  \right\}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark
**(interpretation of the gluing condition)**

In def. \ref{MatchingFamiliesOfPlots} the [[equation]]

$$
  X(\iota_i)(p_i) = X(\iota_j)(p_j)
$$

says in words:

> The plot $p_i$ of $X$ by the coordinate system $U_i$ inside the bigger coordinate system $\mathbb{R}^n$ coincides with the plot $p_j$ of $X$ by the other coordinate system $U_j$ inside $X$ when both are restricted to the [[intersection]] $U_i \cap U_j$ of $U_i$ with $U_j$ inside $\mathbb{R}^n$.

=--

+-- {: .num_remark #NaiveDescentMorphism}
###### Remark
**(comparing global plots to glued plots)**

For each differentially good open cover $\{U_i \to \mathbb{R}^n\}_{i \in I}$ (def. \ref{DifferentiallyGoodOpenCover}) and each pre-smooth set $X$, def. \ref{SmoothPreSpace}, there is a canonical [[function]]

$$
  X(\mathbb{R}^n) 
    \longrightarrow 
  GluedPlots(\{U_i \to \mathbb{R}^n\}, X)
$$

from the set of $\mathbb{R}^n$-plots of $X$ to the set of tuples of glued plots, which sends a plot $p \in X(\mathbb{R}^n)$ to its restriction to all the $\phi_i \colon U_i \hookrightarrow \mathbb{R}^n$:

$$
  p \mapsto (X(\phi_i)(p))_{i \in I}
  \,.
$$

=--

If $X$ is supposed to be consistently probable by coordinate systems, then it must be true that the set of ways of laying out a coordinate system $\mathbb{R}^n$ inside it coincides with the set of ways of laying out tuples of glued coordinate systems inside it, for each good cover $\{U_i \to \mathbb{R}^n\}$ as above. Therefore:

+-- {: .num_defn #SmoothSpace}
###### Definition
**([[smooth set]])**

A pre-smooth set $X$, def. \ref{SmoothPreSpace} is a **[[smooth set]]** if for all differentially good open covers $\{U_i \to \mathbb{R}^n\}$ 
(def. \ref{DifferentiallyGoodOpenCover}) the canonical comparison function of remark \ref{NaiveDescentMorphism} from plots to glued plots is a [[bijection]]

\[
  \label{ConditionSmoothSet}
  X(\mathbb{R}^n) \stackrel{\simeq}{\longrightarrow} GluedPlots(\{U_i \to \mathbb{R}^n\}, X)
  \,.
\]

=--

+-- {: .num_remark #OnTheNotionOfSmoothSpaces}
###### Remark

We may think of a [[smooth set]] as being a kind of [[space]] whose _local models_ (in the general sense discussed at _[[geometry]]_) are [[Cartesian spaces]]:

while definition \ref{SmoothSpace} explicitly says that a smooth set is something that is _consistently probeable_ by such local models; by a [[category theory|general abstract]] fact -- which we discuss in more detail below in _[smooth sets - Semantic Layer](#SmoothSpacesLayerSem)_  -- that is sometimes called the [[co-Yoneda lemma]] it follows in fact that smooth sets are precisely the objects that are obtained by
_gluing coordinate systems_ together.

For instance we will see that two open 2-balls $\mathbb{R}^2 \simeq D^2$ along a common rim yields the smooth set version of the [[sphere]] $S^2$, a basic example of a [[smooth manifold]]. But before we examine such explicit constructions, we discuss here for the moment more general properties of smooth sets. The reader instead wishing to see more of these concrete examples at this point should jump ahead to _[smooth sets - Outlook](#SmoothSpacesOutlook)_.

=--

But the following most basic example we consider right now:

+-- {: .num_example #CartesianSpaceAsSmoothSpace}
###### Example
**([[Cartesian spaces]] and [[smooth manifold]] as [[smooth sets]])**

For $n \in \mathbb{R}^n$, there is a [[smooth set]], def. \ref{SmoothSpace}, whose set of plots over the abstract coordinate systems $\mathbb{R}^k$ is the set

$$
  CartSp(\mathbb{R}^k, \mathbb{R}^n) \in Set
$$

of [[smooth functions]] from $\mathbb{R}^k$ to $\mathbb{R}^n$.

Clearly this is the rule for plots that characterize $\mathbb{R}^n$ itself as a smooth set, and so we will just denote this smooth set by the same symbols "$\mathbb{R}^n$":

$$
  \mathbb{R}^n \colon \mathbb{R}^k \mapsto CartSp(\mathbb{R}^k, \mathbb{R}^n)
  \,.
$$

In particular the [[real line]] $\mathbb{R}$ is this way itself a [[smooth set]].

More generally, if the reader already knows what a [[smooth manifold]] $X$ is; these become smooth sets 
by taking their plots to be the ordinary [[smooth functions]] between smooth manifolds, from Cartesian spaces:

$$
  X(\mathbb{R}^n) \coloneqq Hom_{SmthMfd}(\mathbb{R}^n, X)
  \,.
$$

=--

Some smooth sets are far from being like smooth manifolds:

+-- {: .num_example #SmoothSetOfDifferentialForms}
###### Example
**(smooth [[moduli space]] of [[differential forms]])**

Let $k \in \mathbb{N}$. Then there is a [[smooth set]] (def. \ref{CartesianSpaceAsSmoothSpace}) to be denoted
$\mathbf{\Omega}^k$ given as follows:

1. The set $\mathbf{\Omega}^k(\mathbb{R}^n)$ of plots from $\mathbb{R}^n$ is the set of smooth [[differential n-form|differential k-forms]]
   on $\mathbb{R}^n$

   $$
     \mathbf{\Omega}^k(\mathbb{R}^n) \coloneqq \Omega^k(\mathbb{R}^n)
   $$
   
1. for $f \colon \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ a smooth function, then the corresponding change-of-plots function
   is the operation of [[pullback of differential forms]] along $f$:
   
   $$
     \Omega^{k}(\mathbb{R}^{n_2}) \overset{f^\ast}{\longrightarrow} \Omega^k(\mathbb{R}^{n_1})
     \,.
   $$

We introduce and discuss this example in detail in more detail [below](#DifferentialForms)

=--


A [[smooth set]] (def. \ref{SmoothSpace}) need not have an _underlying set_, for instance 
the smooth set $\mathbf{\Omega}^k$ from example \ref{SmoothSetOfDifferentialForms} for $k \geq 1$
has only a single plot from the point (corresponding to the zero differential form on the point), and yet it is
far from being the point. If a smooth set does have an underlying set, then it is called a  _[[diffeological space]]_, see around Prop. \ref{DiffeologicalSpacesAreTheConcreteSmoothSets} below.


+-- {: .num_example #DiscreteSmoothSpace}
###### Example
**([[discrete object|discrete]] [[smooth set]])

For $S \in $ [[Set]] a set, write

$$
  Disc S \in SmoothSet
$$

for the smooth set whose set of $U$-plots for every $U \in CartSp$ is always $S$.

$$
  Disc S \colon U \mapsto S
$$


and which sends every coordinate transformation $f \colon \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ to the identity function on $S$.

A smooth set of this form we call a **[[discrete object|discrete smooth set]]**.

=--



More examples of smooth sets can be built notably by [[intersection|intersecting]] [[images]] of two smooth sets inside a bigger one. In order to say this we first need a formalization of [[homomorphism]] of smooth sets. This we turn to now.


### Homomorphisms of smooth sets
 {#HomomorphismsOfSmoothSpaces}

We discuss "functions" or "maps" between [[smooth sets]], def. \ref{SmoothSpace}, which preserve the smooth set [[structure]] in a suitable sense. As with any notion of function that preserves structure, we refer to them as _[[homomorphisms]]_.

The idea of the following definition is to say that whatever a [[homomorphism]] $f : X \to Y$ between two smooth sets is, it has to take the plots of $X$ by $\mathbb{R}^n$ to a corresponding plot of $Y$, such that this respects coordinate transformations.

+-- {: .num_defn #HomomorphismOfSmoothSpaces}
###### Definition
**([[homomorphisms]] of [[smooth sets]] -- smooth functions)**

Let $X$ and $Y$ be two [[smooth sets]], def. \ref{SmoothSpace}. Then a [[homomorphism]] of _[[smooth function]]_ $f \colon X \to Y$ between them is

* for each abstract coordinate system $\mathbb{R}^n$ (hence for each $n \in \mathbb{N}$) a [[function]]

  $f_{\mathbb{R}^n} : X(\mathbb{R}^n) \to Y(\mathbb{R}^n)$

  that sends $\mathbb{R}^n$-plots of $X$ to $\mathbb{R}^n$-plots of $Y$

such that

* for each [[smooth function]] $\phi : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ we have

  $$
    Y(\phi) \circ f_{\mathbb{R}^{n_1}} = f_{\mathbb{R}^{n_2}} \circ X(\phi)
  $$

  hence a [[commuting diagram]]

  $$
    \array{
      X(\mathbb{R}^{n_1}) &\stackrel{f_{\mathbb{R}^{n_1}}}{\to}& Y(\mathbb{R}^{n_1})
      \\
      \downarrow^{\mathrlap{X(\phi)}} && \downarrow^{\mathrlap{Y(\phi)}}
      \\
      X(\mathbb{R}^{n_2}) &\stackrel{f_{\mathbb{R}^{n_2}}}{\to}& Y(\mathbb{R}^{n_1})
    }
    \,.
  $$

For $f_1 : X \to Y$ and $f_2 : X \to Y$ two homomorphisms of smooth sets, their [[composition]] $f_2 \circ f_1 \colon X \to Y$ is defined to be the homomorphism whose component over $\mathbb{R}^n$ is the composite of functions of the components of $f_1$ and $f_2$:

$$
  (f_2\circ f_1)_{\mathbb{R}^n} \coloneqq {f_2}_{\mathbb{R}^n} \circ {f_1}_{\mathbb{R}^n}
  \,.
$$


=--

+-- {: .num_defn #CategoryOfSmoothSets}
###### Definition
**(the [[category]] _[[SmoothSet]]_ of [[smooth sets]] with [[smooth functions]])**

Write [[SmoothSet]] or $SmoothSet$ for the [[category]] ([this def.](geometry+of+physics+--+Categories+and+Toposes#Categories)) whose [[objects]] are [[smooth sets]], def. \ref{SmoothSpace}, and whose [[morphisms]] are homomorphisms of smooth sets according to def. \ref{HomomorphismOfSmoothSpaces}.

=--

At this point it may seem that we have now _two different_ notions for how to lay out a coordinate system in a smooth set $X$: on the hand, $X$ comes by definition with a rule for what the set $X(\mathbb{R}^n)$ of its $\mathbb{R}^n$-plots is. On the other hand, we can now regard the abstract coordinate system $\mathbb{R}^n$ itself as a smooth set, by example \ref{CartesianSpaceAsSmoothSpace}, and then say that an  $\mathbb{R}^n$-plot of $X$ should be a homomorphism of smooth sets of the form $\mathbb{R}^n \to X$.

The following proposition says that these two superficially different notions actually naturally coincide.

+-- {: .num_prop #YonedaForSmoothSpaces}
###### Proposition

Let $X$ be any [[smooth set]], def. \ref{SmoothSpace}, and regard the abstract coordinate system $\mathbb{R}^n$ as a smooth set, by example \ref{CartesianSpaceAsSmoothSpace}. There is a [[natural bijection]]

$$
  X(\mathbb{R}^n) \simeq Hom_{SmoothSet}(\mathbb{R}^n, X)
$$

between the _postulated_ $\mathbb{R}^n$-plots of $X$ and the _actual_ $\mathbb{R}^n$-plots given by homomorphism of smooth sets $\mathbb{R}^n \to X$.

=--

+-- {: .proof}
###### Proof

This is a special case of the _[[Yoneda lemma]]_ ([this prop.](geometry+of+physics+--+categories+and+toposes#YonedaLemma)), as will be made more explicit below in _[The topos of smooth sets](#ToposOfSmoothSpaces)_.
The reader unfamiliar with this should write out the simple proof explicitly: use the defining [[commuting diagrams]] in def. \ref{HomomorphismOfSmoothSpaces} to deduce that a homomorphism $f : \mathbb{R}^n \to X$ is uniquely fixed by the image of the [[identity]] element in  $\mathbb{R}^n(\mathbb{R}^n) \coloneqq CartSp(\mathbb{R}^n, \mathbb{R}^n)$ under the component function $f_{\mathbb{R}^n} : \mathbb{R}^n(\mathbb{R}^n) \to X(\mathbb{R}^n)$.

=--

+-- {: .num_example #SmoothFunctionOnSmoothSpace}
###### Example

Let $\mathbb{R} \in SmoothSet$ denote the [[real line]], regarded as a [[smooth set]] by example \ref{CartesianSpaceAsSmoothSpace}. Then for $X \in SmoothSet$ any smooth set, a homomorphism of smooth sets

$$
  f \colon X \to \mathbb{R}
$$

is a _[[smooth function]] on $X$_. Prop. \ref{YonedaForSmoothSpaces} says here that when $X$ happens to be an abstract coordinate system regarded as a smooth set by def. \ref{CartesianSpaceAsSmoothSpace}, then this general notion of smooth functions between smooth sets reproduces the basic notion of [this def.](geometry+of+physics+--+coordinate systems#CartesianSpaceAndHomomorphism)

=--

+-- {: .num_defn #PointsOfASmoothSpace}
###### Definition

The 0-[[dimension|dimensional]] abstract coordinate system $\mathbb{R}^0$ we also call the **[[point]]** and regarded as a smooth set we will often write it as

$$
  * \in SmoothSet
  \,.
$$

For any $X \in SmoothSet$, we say that a homomorphism

$$
  x \colon * \to X
$$

is a **point of $X$**.

=--

+-- {: .num_remark}
###### Remark

By prop. \ref{YonedaForSmoothSpaces} the points of a smooth set $X$ are naturally identified with its 0-dimensional plots, hence with the "ways of laying out a 0-dimensional coordinate system" in $X$:

$$
  Hom(*, X) \simeq X(\mathbb{R}^0)
  \,.
$$

=--


### Products and fiber products of smooth sets
 {#ProductsAndFiberProductsOfSmoothSpaces}

+-- {: .num_defn #ProductOfSmoothSpaces}
###### Definition

Let $X, Y \in SmoothSet$ by two smooth sets. Their **[[product]]** is the smooth set $X \times Y \in SmoothSet$ whose plots are pairs of plots of $X$ and $Y$:

$$
  X\times Y (\mathbb{R}^n) \coloneqq X(\mathbb{R}^n) \times Y(\mathbb{R}^n)
  \;\;
  \in Set
  \,.
$$

The **projection on the first factor** is the homomorphism

$$
   p_1 \colon X \times Y \to X
$$

which sends $\mathbb{R}^n$-plots of $X \times Y$ to those of $X$ by forming the projection of the [[cartesian product]] of sets:

$$
  {p_1}_{\mathbb{R}^n} \colon X(\mathbb{R}^n) \times Y(\mathbb{R}^n) \stackrel{p_1}{\to} X(\mathbb{R}^n)
  \,.
$$

Analogously for the **projection to the second factor**

$$
  p_2 \colon X \times Y \to Y
  \,.
$$

=--

+-- {: .num_prop #ProductOfSmoothSpaceWithThePoint}
###### Proposition

Let $* = \mathbb{R}^0$ be the [[point]], regarded as a smooth set, def. \ref{PointsOfASmoothSpace}. Then for $X \in SmoothSet$ any smooth set the canonical projection homomorphism

$$
  X \times * \to X
$$

is an [[isomorphism]].

=--

+-- {: .num_defn}
###### Definition

Let $f \colon X \to Z$ and $g \colon Y \to Z$ be two [[homomorphisms]] of smooth sets, def. \ref{HomomorphismOfSmoothSpaces}. There is then a new smooth set to be denoted

$$
  X \times_Z Y \in SmoothSet
$$

(with $f$ and $g$ understood), called the [[fiber product]] of $X$ and $Y$ along $f$ and $g$, and defined as follows:

the set of $\mathbb{R}^n$-plots of $X \times_Z Y$ is the set of pairs of plots of $X$ and $Y$ which become the same plot of $Z$ under $f$ and $g$, respectively:

$$
  (X \times_Z Y)(\mathbb{R}^n)
  =
  \left\{
    (p_X \in X(\mathbb{R}^n), p_Y \in Y(\mathbb{R}^n))
    \; |\;
    f_{\mathbb{R}^n}(p_X) = g_{\mathbb{R}^n}(p_Y)
  \right\}
  \,.
$$

=--



### Smooth mapping spaces and smooth moduli spaces
 {#SmoothMappingSpaces}


+-- {: .num_defn #SmoothFunctionSpace}
###### Definition
**([[smooth set|smooth]] [[mapping space]])**

Let $\Sigma, X \in SmoothSet$ be two [[smooth sets]], def. \ref{SmoothSpace}. Then the **smooth [[mapping space]]**

$$
  [\Sigma,X] \in SmoothSet
$$

is the [[smooth set]] defined by saying that its set of $\mathbb{R}^n$-plots is

$$
  [\Sigma, X](\mathbb{R}^n)
   \coloneqq
  Hom(\Sigma \times \mathbb{R}^n, X)
  \,.
$$

=--

Here in $\Sigma \times \mathbb{R}^n$ we first regard the abstract coordinate system $\mathbb{R}^n$ as a smooth set by example \ref{CartesianSpaceAsSmoothSpace} and then we form the [[product]] smooth set by def. \ref{ProductOfSmoothSpaces}.

+-- {: .num_remark #NatureOfPlotsOfMappingSpace}
###### Remark

This means in words that a $\mathbb{R}^n$-plot of the [[mapping space]] $[\Sigma,X]$ is a smooth $\mathbb{R}^n$-parameterized _family_ of homomorphisms $\Sigma \to X$.

=--


+-- {: .num_prop #UniversalPropertyOfMappingSpace}
###### Proposition

There is a [[natural bijection]]

$$
  Hom(K, [\Sigma, X])
  \simeq
  Hom(K \times \Sigma, X)
$$

for every smooth set $K$.

=--

+-- {: .proof}
###### Proof

With a bit of work this is straightforward to check explicitly by unwinding the definitions. It follows however from [[category theory|general abstract]] results once we realize that $[-,-]$ is of course the _[[internal hom]]_ of smooth sets. This we come to below in _[Smooth sets - Semantic Layer](#SmoothSpacesLayerSem)_.

=--


+-- {: .num_remark #MappingSpaceAsModuliSpace}
###### Remark

This says in words that a smooth function from any $K$ into the mapping space $[\Sigma,X]$ is equivalently a smooth function from $K \times \Sigma$ to $X$. The latter we may regard as a _$K$-parameterized smooth family_ of smooth functions $\Sigma \to X$. Therefore in view of the previous remark \ref{NatureOfPlotsOfMappingSpace} this says that smooth mapping spaces have a [[universal property]] not just over abstract coordinate systems, but over all smooth sets.

We will therefore also say that $[\Sigma,X]$ is the **smooth [[moduli space]]** of smooth functions from $\Sigma \to X$, because it is such that smooth maps $K \to [\Sigma,X]$ into it _modulate_, as we move around on $K$, a family of smooth functions $\Sigma\to X$, depending on $K$.

=--

First interesting examples of such smooth moduli spaces are discussed in _[Differential forms -- Model Layer](#DifferentialFormsLayerMod)_ below. Many more interesting examples follow once we pass from smooth 0-types to smooth $n$-types below in _[Smooth n-groupoids](#SmoothnGroupoids)_.

We will see many more examples of smooth moduli spaces, starting below in _[Differential forms - Model Layer](#DifferentialFormsLayerMod)_.

+-- {: .num_prop #UnderlyingSetOfSmoothMappingSpace}
###### Proposition


The set of points, def. \ref{PointsOfASmoothSpace}, of a smooth mapping space $[\Sigma,X]$ is the bare set of homomorphism $\Sigma \to X$: there is a [[natural isomorphism]]

$$
  Hom(*, [\Sigma, X]) \simeq Hom(\Sigma, X)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Combine prop. \ref{UniversalPropertyOfMappingSpace} with prop. \ref{ProductOfSmoothSpaceWithThePoint}.

=--


+-- {: .num_example #SmoothPathSpace}
###### Example

Given a [[smooth set]] $X \in SmoothSet$, its smooth **[[path space]]** is the smooth mapping space

$$
  \mathbf{P}X \coloneqq [\mathbb{R}^1, X]
  \,.
$$

By prop. \ref{UnderlyingSetOfSmoothMappingSpace} the points of $P X$ are indeed precisely the smooth trajectories $\mathbb{R}^1 \to X$. But $P X$ also knows how to _smoothly vary_ such smooth trajectories.

This is central for [[variational calculus]] which determines [[equations of motion]] in [[physics]]. This we turn to below in _[Variational calculus](#VariationalCalculus)_.

=--

+-- {: .num_remark}
###### Remark

In [[physics]], if $X$ is a model for [[spacetime]], then $P X$ may notably be interpreted as the smooth set of [[worldlines]] _in_ $X$, hence the smooth set of paths or _trajectories_ of a [[particle]] in $X$.

=--

+-- {: .num_example #SmoothLoopSpace}
###### Example

If in the above example \ref{SmoothPathSpace} the path is
constraind to be a [[loop]] in $X$, one obtains the _[[smooth loop space]]_

$$
  \mathbf{L}X \coloneqq [S^1, X]
  \,.
$$

=--


In example \ref{SmoothFunctionOnSmoothSpace} we saw that a smooth function on a general [[smooth set]] $X$ is a homomorphism of smooth sets, def. \ref{HomomorphismOfSmoothSpaces}

$$
  f \colon X \to \mathbb{R}
  \,.
$$

The collection of these forms the [[hom-set]] $Hom_{SmoothSet}(X, \mathbb{R})$. But by the discussion in _[Smooth mapping spaces](#SmoothMappingSpaces)_ such hom-sets are naturally refined to smooth sets themselves.

+-- {: .num_defn #SmoothSpaceOfSmoothFunctions}
###### Definition

For $X \in SmoothSet$ a [[smooth set]], we say that the **moduli space of smooth functions** on $X$ is the smooth mapping space (def. \ref{SmoothFunctionSpace}), from $X$ into the standard [[real line]] $\mathbb{R}$

$$
  [X, \mathbb{R}] \in SmoothSet
  \,.
$$

We will also denote this by

$$
  \mathbf{C}^\infty(X) \coloneqq [X, \mathbb{R}]
  \,,

$$

since in the special case that $X$ is a [[Cartesian space]] this is the smooth refinement of the set $C^\infty(X)$ of [[smooth functions]] on $X$.

=--

+-- {: .num_remark}
###### Remark

We call this a _[[moduli space]]_ because by prop. \ref{UniversalPropertyOfMappingSpace} above and in the sense of remark \ref{MappingSpaceAsModuliSpace} it is such that smooth functions into it _modulate_ smooth functions $X \to \mathbb{R}$.

By prop. \ref{UnderlyingSetOfSmoothMappingSpace} a point $* \to [X,\mathbb{R}^1]$ of the moduli space is equivalently a smooth function $X \to \mathbb{R}^1$.

=--

### The cohesive topos of smooth sets
 {#SmoothSpacesLayerSem}
 {#ToposOfSmoothSpaces}


In the language of [[geometry of physics -- categories and toposes|categories and toposes]], we may summarize the concept of [[smooth sets]] by saying that they form the _[[sheaf topos]]_ over the _[[site]]_ of [[Cartesian spaces]] (Prop. \ref{SmoothSetsAreSheavesOnCartSp} below).

This perspective allows to see good abstract properties enjoyed by the [[smooth sets]]. The key such property is that the [[topos]] which they form is a _[[cohesive topos]]_ (Prop. \ref{SmoothSetsFormACohesiveTopos} below).


$\,$

+-- {: .num_prop #SmoothSetsAreSheavesOnCartSp}
###### Proposition
**([[equivalence of categories]] between [[smooth sets]] and [[sheaves]] on [[CartSp]])**

There is a canonical [[equivalence of categories]] ([this def.](geometry+of+physics+--+Categories+and+Toposes#EquivalenceOfCategories)) between the [[category]] _[[SmoothSet]]_ of [[smooth sets]] from def. \ref{CategoryOfSmoothSets}, and the [[category of sheaves]] ([this def.](geometry+of+physics+--+Categories+and+Toposes#Sheaf)) on the [[category]] [[CartSp]] ([this def.](geometry+of+physics+--+coordinate+systems#CartSpCategory)) equipped with the [[coverage]] ([this def.](geometry+of+physics+--+Categories+and+Toposes#Coverage)) of differentiably [[good open covers]] (def. \ref{DifferentiallyGoodOpenCover})

$$
  SmoothSet
  \;\simeq\;
  Sh(CartSp)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is a straightforward matter of matching definitions. We spell it out:

* A _pre-smooth set_, def. \ref{SmoothPreSpace} is equivalently a [[presheaf]] ([this Example](geometry+of+physics+--+Categories+and+Toposes#CategoryOfPresheaves)) on [[CartSp]] ([this prop.](geometry+of+physics+--+coordinate+systems#CartSpCategory)), hence a [[functor]] ([this def.](geometry+of+physics+--+Categories+and+Toposes#Functors)) $X : CartSp^{op} \to Set$ from the [[category]] [[CartSp]] to the [[category of sets]] ([this Example](geometry+of+physics+--+Categories+and+Toposes#CategoryOfSets));

* a _[[smooth set]]_, def. \ref{SmoothSpace}, is equivalently a presheaf on [[CartSp]] ([this prop.](geometry+of+physics+--+coordinate+systems#CartSpCategory)) which is a [[sheaf]] ([this def.](geometry+of+physics+--+Categories+and+Toposes#Sheaf)) with respect to the [[coverage]] ([this def.](geometry+of+physics+--+Categories+and+Toposes#Coverage)) of differentially [[good open cover]] (def. \ref{DifferentiallyGoodOpenCover}):

  * the set of "glued plots" (def. \ref{MatchingFamiliesOfPlots}) is the set of [[matching families]] ([this def.](geometry+of+physics+--+Categories+and+Toposes#CompatibleElements))

  * the comparison morphism from global plots  to glued plots of remark \ref{NaiveDescentMorphism} is the comparison map from to [[matching families]] ([here](geometry+of+physics+--+categories+and+toposes#eq:SheafComparison));

  * the condition (eq:ConditionSmoothSet) that this be a [[bijection]] is the _[[sheaf|sheaf condition]]_  ([here](geometry+of+physics+--+Categories+and+Toposes#eq:SheafCondition)).

=--

+-- {: .num_prop #EquivalentSitesForCartSp}
###### Proposition
**(equivalent [[sites]] for [[CartSp]])**

Consider the canonical [[full subcategory]]-inclusion [[functors]]

$$
  CartSp
    \overset{\phantom{AAA}}{\hookrightarrow}
  EuclOp
    \overset{\phantom{AAA}}{\hookrightarrow}
  SmthMfd
$$

which regard, in turn, a [[Cartesian space]] (Def. \ref{CartSpCategory}) as an [[open subset]] of itself, and regard every [[open subset]] of [[Euclidean space]] (Def. \ref{SiteOfSmoothManifolds}) as a [[smooth manifold]] ([this Example](differentiable+manifold#DifferentiableManifoldCartesianSpace)[this Example] and (differentiable+manifold#OpenSubsetsOfDifferentiableManifoldsAreDifferentiableManifolds)).

Then the induced pre-composition functors induce [[equivalences of categories]] ([this Def.](geometry+of+physics+--+categories+and+toposes#EquivalenceOfCategories)) between the corresponding [[categories of sheaves]]:

$$
  SmoothSet
    \;\simeq\;
  Sh(CartSp)
    \;\simeq\;
  Sh(EuclOp)
    \;\simeq\;
  Sh(SmthMfd)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By Prop. \ref{CompletingGoodOpenCoversToAllOpenCovers} we may identify $Sh(CartSp) = Sh(CartSp_{\text{good open cov}})$. With that, 
both inclusions are evidently [[dense subsite]]-inclusions ([this Def.](geometry+of+physics+--+categories+and+toposes#DenseSubsite)). Therefore the statement follows by the [[comparison lemma]] ([this prop.](geometry+of+physics+--+categories+and+toposes#ComparisonLemma)).

=--

As a corollary we obtain:

+-- {: .num_prop #InclusionOfSmoothManifoldsIntoSmoothSets}
###### Proposition
**([[smooth manifolds]] [[fully faithful functor|fully faithful]] inside [[smooth sets]])**

Regarding [[smooth manifolds]] as [[smooth sets]] via Example \ref{CartesianSpaceAsSmoothSpace} yields a [[full subcategory]]-inclusion

$$
  SmoothManifold 
    \overset{\phantom{AA}\iota\phantom{AA}}{\hookrightarrow}
  SmoothSet
  \,,
$$

meaning that for $X, Y \in SmoothManifold$ any two [[smooth manifolds]], this  functor induces a [[bijection]] between the [[smooth functions]] $X \to Y$ regarded in the sense of smooth manifolds, and regarded in the sense of [[smooth sets]] (Def. \ref{HomomorphismOfSmoothSpaces}):

$$
  Hom_{SmoothManifold}(X,Y)
  \;\simeq\;
  Hom_{SmoothSet}(\iota(X), \iota(Y))
  \,.
$$

=--

+-- {: .proof}
###### Proof

By Prop. \ref{EquivalentSitesForCartSp} we have an [[equivalence of categories]]

$$
  SmoothSet
  \;\simeq\;
  Sh(SmoothManifold)
  \,.
$$

With this the statement is given by the [[Yoneda lemma]] ([this prop.](geometry+of+physics+--+categories+and+toposes#YonedaLemma)).

=--


$\,$


+-- {: .num_prop #SmoothSetsFormACohesiveTopos}
###### Proposition
**([[smooth sets]] form a [[cohesive topos]])**

The [[site]] [[CartSp]] (Prop. \ref{TheDifferentiallyGoodOpenCoverCoverage}) is a [[cohesive site]] ([this Def.](geometry+of+physics+--+categories+and+toposes#OneCohesiveSite)), hence its [[sheaf topos]] is a [[cohesive topos]] (by [this Prop. (broken link)](CategoriesOfSheavesOnCohesiveSiteIsCohesive)). Under the identification of Prop. \ref{SmoothSetsAreSheavesOnCartSp}, this means that:

The [[category]] [[SmoothSet]] of [[smooth sets]] (Def. \ref{CategoryOfSmoothSets}) is a [[cohesive topos]] ([this Def.](geometry+of+physics+--+categories+and+toposes#CohesiveTopos)):

\[
  \label{SheafToposAdjointQuadruple}
  SmoothSet
    \array{
      \overset{\phantom{AAA} \Pi_0 \phantom{AAA}}{\longrightarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\longleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\longleftarrow}
    }
  Set
\]

Moreover, this cohesive topos satisfies the following equivalent conditions (from [this Prop.](geometry+of+physics+-+cohesive+toposes#PiecesHavePoints)):

1. _[[pieces have points]]_,

1. _[[discrete objects are concrete]]_.

=--

+-- {: .proof}
###### Proof


The category $CartSp$ clearly has [[finite products]]: The [[terminal object]] is the [[point]], given by the 0-[[dimension|dimensional]] [[Cartesian space]]

$$
  \ast = \mathbb{R}^0
$$

and the [[Cartesian product]] of two [[Cartesian spaces]] is the Cartesian space whose [[dimension]] is the [[sum]] of the two separate dimensions:

$$
  \mathbb{R}^{n_1} \times \mathbb{R}^{n_2}
  \;\simeq\;
  \mathbb{R}^{ n_1 + n_2 }
  \,.
$$

This establishes the first clause in the definition of [[cohesive site]] ([this def.](geometry+of+physics+--+categories+and+toposes#OneCohesiveSite))

For the second clause, consider a differentiably-[[good open cover]] $\{U_i \overset{}{\to} \mathbb{R}^n\}$ (Def. \ref{DifferentiallyGoodOpenCover}). This being a [[good cover]] implies that its [[Cech groupoid]] is, as an [[internal groupoid]] (via [this remark](geometry+of+physics+--+categories+and+toposes#PresheavesOfGroupoidsAsInternalGroupoidsInPresheaves)), of the form

\[
  \label{CechGroupoidForCartSp}
  C(\{U_i\}_i)
  \;\simeq\;
  \left( 
    \array{
       \underset{i,j}{\coprod} y(U_i \underset{\mathbb{R}^n}{\cap} U_j)
       \\
       \big\downarrow \big\uparrow \big\downarrow
       \\
       \underset{i}{\coprod} y(U_i)
    }
  \right)
  \,.
\]

where we used the defining property of [[good open covers]] to identify $y(U_i) \times_X y(U_j) \simeq y( U_i \cap_X U_j )$. 

The [[colimit]] of (eq:CechGroupoidForCartSp), regarded just as a [[presheaf]] of [[reflexive graph|reflexive]] [[directed graph|directed]] [[graphs]] (hence ignoring [[composition]] for the moment), is readily seen to be the [[graph]] of the [[colimit]] of the components (the [[universal property]] follows immediately from that of the component colimits):


\[
  \label{ColimitOfCechGroupoidOverCartSp}
  \begin{aligned}
    \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
    C(\{U_i\}_i)
    & \simeq
    \left( 
      \array{
        \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
         \underset{i,j}{\coprod} y(U_i \underset{\mathbb{R}^n}{\cap} U_j)
         \\
         \big\downarrow \big\uparrow \big\downarrow
         \\
         \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
         \underset{i}{\coprod} y(U_i)
      }
    \right)
    \\
    & \simeq
    \left( 
      \array{
         \underset{i,j}{\coprod} 
         \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
         y(U_i \underset{\mathbb{R}^n}{\cap} U_j)
         \\
         \big\downarrow \big\uparrow \big\downarrow
         \\
         \underset{i}{\coprod} 
         \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
         y(U_i)
      }
    \right)
    \\
    & \simeq
    \left( 
      \array{
         \underset{i,j}{\coprod} \ast
          \\
         \big\downarrow \big\uparrow \big\downarrow
         \\
         \underset{i}{\coprod} \ast
      }
    \right)
  \end{aligned}
  \,.
\]

Here we first used that [[colimits commute with colimits]], hence in particular with [[coproducts]] ([this prop.](geometry+of+physics+--+categories+and+toposes#LimitsCommuteWithLimits)) and then that the colimit of a [[representable presheaf]] is [[generalized the|the]] [[singleton]] set ([this Lemma](geometry+of+physics+--+categories+and+toposes#ColimitOfRepresentableIsSingleton)).

This colimiting [[graph]] carries a unique [[composition]] structure making it a [[groupoid]], since there is at most one morphism between any two objects, and every object carries a morphism from itself to itself. This implies that this groupoid is actually the colimiting groupoid of the Cech groupoid: hence the groupoid obtained from replacing each representable summand in the Cech groupoid by a point.

Precisely this operation on [[Cech groupoids]] of [[good open covers]] of [[topological spaces]] is what _[[Borsuk's nerve theorem]]_ is about, a classical result in [[topology]]/[[homotopy theory]]. This theorem implies directly that the set of [[connected components]] of the groupoid (eq:ColimitOfCechGroupoidOverCartSp) is in [[bijection]] with the set of [[connected components]] of the [[Cartesian space]] $\mathbb{R}^n$, regarded as a [[topological space]]. But this is evidently a [[connected topological space]], which finally shows that, indeed

$$
  \pi_0
  \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
    C(\{U_i\}_i)
  \;\simeq\;
  \ast
  \,.
$$

The second item of the second clause in Def. \ref{OneCohesiveSite} follows similarly, but more easily: The [[limit]] of the [[Cech groupoid]] is readily seen to be, as before, the unique groupoid structure on the limiting underlying graph of presheaves. Since $CartSp$ has a [[terminal object]] $\ast = \mathbb{R}^0$, which is hence an [[initial object]] in the [[opposite category]] $CartSp^{op}$, limits over $CartSp^{op}$ yield simply the evaluation on that object:

\[
  \label{ColimitOfCechGroupoidOverCartSp}
  \begin{aligned}
    \underset{\underset{CartSp^{op}}{\longleftarrow}}{\lim}
    C(\{U_i\}_i)
    & \simeq
    \left( 
      \array{
        \underset{\underset{CartSp^{op}}{\longleftarrow}}{\lim}
         \underset{i,j}{\coprod} y(U_i \underset{\mathbb{R}^n}{\cap} U_j)
         \\
         \big\downarrow \big\uparrow \big\downarrow
         \\
         \underset{\underset{CartSp^{op}}{\longleftarrow}}{\lim}
         \underset{i}{\coprod} y(U_i)
      }
      \phantom{A}
    \right)
    \\
    & \simeq
    \left( 
      \array{
         \underset{i,j}{\coprod} 
         Hom_{CartSp}\left( \ast,  U_i \underset{\mathbb{R}^n}{\cap} U_j \right)
         \\
         \big\downarrow \big\uparrow \big\downarrow
         \\
         \underset{i}{\coprod} 
         Hom_{CartSp}( \ast, U_i )
      }
    \right)
  \end{aligned}
  \,.
\]

Here we used that [[colimits]] (here [[coproducts]]) of [[presheaves]] are computed objectwise, and then the definition of the [[Yoneda embedding]] $y$.

But the [[equivalence relation]] induced by this graph on its set of objects $\underset{i}{\coprod}  Hom_{CartSp}( \ast, U_i )$ precisely identifies pairs of points, one in $U_i$ the other in $U_j$, that are actually the same point of the $\mathbb{R}^n$ being covered. Hence the set of [[equivalence classes]] is the set of points of $\mathbb{R}^n$, which is just what remained to be shown:

$$
  \pi_0
  \underset{\underset{CartSp^{op}}{\longleftarrow}}{\lim}
    C(\{U_i\}_i)
  \;\simeq\;
  Hom_{CartSp}(\ast, \mathbb{R}^n)
  \,.
$$

Finally to see that _[[pieces have points]]_ and _[[discrete objects are concrete]]_ is satisfied, it is sufficient to observe, by [this prop.](geometry+of+physics+-+cohesive+toposes#CohesiveSiteSuchThatDiscreteObjectsAreConcrete) that for each $n \in \mathbb{N}$, the [[hom set]] $Hom_{CartSp}(\ast, \mathbb{R}^n)$ is [[inhabited set|non-empty]]. 

=--

The following statement is a [[0-truncated object|0-truncated]] shadow of the [[differential geometry|differential geometric]] analog of the concept of _[[A1-homotopy theory|A1-localization]]_:

+-- {: .num_prop #ShapeModalityOnSmoothSetsIsR1Localization}
###### Proposition
**([[shape modality]] on [[smooth sets]] is $\mathbb{R}^1$-[[reflective localization|localization]])**

The [[reflective subcategory]]-inclusion from Prop. \ref{SmoothSetsFormACohesiveTopos}

$$
  Set 
    \underoverset
      {\underset{ \phantom{A}Disc\phantom{A} }{\hookrightarrow}}
      {\overset{\Pi}{\longleftarrow}}
      {\bot}
  SmoothSet
$$

of [[sets]] as the [[discrete objects|discrete]] [[smooth sets]], exhibits the _[[reflective subcategory|reflection]] on $\mathbb{R}^1$-[[local objects]]_ ([this Def.](geometry+of+physics+--+categories+and+toposes#LocalizationAtACollectionOfMorphisms)) for $\mathbb{R}^1$ the [[real line]], in the sense of [[localization at an object]]:

$$
  \Pi \;\simeq\; L_{\mathbb{R}^1}
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since we already know that the [[left adjoint]] $\Pi$ exists, we need to show that the [[full subcategory]] of [[discrete object|discrete]] [[smooth sets]] $Set \overset{Disc}{\hookrightarrow} SmoothSet$ is equivalently that of [[local objects]] ([this Def.](geometry+of+physics+–+basic+notions+of+category+theory#LocalObjects)) with respect to the class of morphisms of the form

$$
  X \times \mathbb{R}^1 \overset{ p_1 }{\longrightarrow} X
$$

for $X$ any [[object]] of $SmoothSet$.

We claim that a [[smooth set]] $A$ is a [[local object]] with respect to this class, already if it is a local object with respect to just the [[small set]]

\[
  \label{RnTimesR1Projections}
  \left\{
     \mathbb{R}^n \times \mathbb{R}^1 
     \overset{p_1}{\longrightarrow}
     \mathbb{R}^n
  \right\}_{n \in \mathbb{N}}
\]

for $X = \mathbb{R}^n$ a [[Cartesian space]].

To see this, we identify $SmoothSet \simeq Sh(CartSp)$ via Prop. \ref{EquivalentSitesForCartSp}, and then use the [[co-Yoneda lemma]] ([this Prop.](geometry+of+physics+--+categories+and+toposes#TopologicalCoYonedaLemma)) to express any $X \in SmoothSet$ as a [[colimit]] of [[Cartesian spaces]]: $X \simeq \int^{\mathbb{R}^n \in Cartsp} \mathbb{R}^n \cdot X(\mathbb{R}^n)$. 

Assuming then that $A$ is local with respect to the [[small set]] (eq:RnTimesR1Projections) we obtain

$$
  \begin{aligned}
    Hom_{SmoothSet}\big(
      X \times \mathbb{R}^1 \overset{p_1}{\to} X
      \;\,,\;
      A
    \big)
    & \simeq
    \int_{\mathbb{R}^n \in CartSp}
    Hom_{Set}\left( X(\mathbb{R}^n),
    \,
    \underset{\text{bijection}}{
    \underbrace{
    Hom_{SmoothSet}\big(
      \mathbb{R}^n \times \mathbb{R}^1 \overset{p_1}{\to} \mathbb{R}^n
      \;\,,\;
      A
    \big)
    }}
    \right)
  \end{aligned}
$$

where we used that

1. the [[Cartesian product]] $(-) \times \mathbb{R}^1$ preserves [[colimits]], since it is a [[left adjoint]] ([this Prop.](geometry+of+physics+--+categories+and+toposes#PropertiesOfSheafToposes)) and since [[left adjoints preserve colimits]] ([this Prop.](geometry+of+physics+--+categories+and+toposes#AdjointsPreserveCoLimits)),

1. the [[hom-functor preserves limits]] ([this Prop.](geometry+of+physics+--+categories+and+toposes#HomFunctorPreservesLimits)), hence sends colimits in the first argument to limits.

But on the right this is now a morphisms of [[limits]] induced by morphism of [[diagrams]] which is objectwise an [[bijection]], as shown, and hence is a [[bijection]]) itself.

Hence we are reduced to showing that the [[local objects]] with respect to (eq:RnTimesR1Projections) are the discrete smooth sets. But by [[induction]] over $n \in \mathbb{N}$, locality with respect to (eq:RnTimesR1Projections) means equivalently locality with respect to 

$$
  \left\{ 
    \mathbb{R}^n \overset{\exists !}{\to} \mathbb{R}^0 = \ast
  \right\}
$$

The [[local objects]] with respect to this set are manifestly exactly the [[constant presheaves]]. But by the proof of Prop. \ref{SmoothSetsFormACohesiveTopos} (proceeding via the proof of [this Prop.](geometry+of+physics+--+categories+and+toposes#CategoriesOfSheavesOnCohesiveSiteIsCohesive)) these are indeed exactly the objects in the image of $Set \overset{Disc}{\hookrightarrow} SmoothSet$.

=--



$\,$

### Concrete smooth sets: Diffeological spaces

The cohesiveness of smooth sets (Prop. \ref{SmoothSetsFormACohesiveTopos}) implies in particular that there is a concept of _[[concrete objects]]_ among the smooth sets ([this Def.](geometry+of+physics+--+categories+and+toposes#CohesiveModalities)). We show here (Prop. \ref{DiffeologicalSpacesAreTheConcreteSmoothSets} below) that these concrete smooth sets are [[equivalence of categories|equivalent]] to a kind of [[generalized smooth spaces]] that are known as _[[Chen smooth spaces]]_ ([Chen 77](diffeological+space#Chen77)) or _[[diffeological spaces]]_ ([Souriau 79](diffeological+space#Souriau79), [Iglesias-Zemmour 85](diffeological+space#IglesiasZemmour85)), which we recall as Def. \ref{DiffeologicalSpace} below. 

A comprehensive development of [[differential geometry]] in terms of [[diffeological spaces]] is spelled out in ([Iglesias-Zemmour 13](diffeological+space#PIZ)). 

Since the [[concrete objects]] in any [[cohesive topos]], and hence the [[diffeological spaces]] among all [[smooth sets]], form a [[reflective subcategory]] ([This prop.](geometry+of+physics+--+categories+and+toposes#QuasitoposOfConcreteObjects)), every smooth set has a _[[concretification]]_ to a concrete smooth set, hence to a diffeological space. An important example of this construction are [[moduli spaces]] of [[differential forms]], this we turn to in Def. \ref{SmoothSpaceOfFormsOnSmoothSpace} below.

$\,$


+-- {: .num_defn #DiffeologicalSpace}
###### Definition
**([[diffeological space]] (e.g. [Iglesias Zemmour 18, def. 2 and 5](diffeological+space#IglesiasZemmour18)))**

A _[[diffeological space]]_ $\mathbf{X}$ is 

1. a [[set]] $X \in Set$, called the _underlying set_ of the diffeological space;

1. for each [[open subset]] $U \subset E^n$ of some [[Euclidean space]] $E^n$, for any $n \in \mathbb{N}$, a [[subset]]

   $$
     \mathbf{X}(U) \subset Hom_{Set}(U, X)
   $$ 

   of the [[function set]] of [[functions]] of [[sets]] from $U$ to $X$, called the set of _plots_ of $\mathbf{X}$ by $U$;

such that for every open subset $U$ as above the following conditions hold:

1. the set of plots $\mathbf{X}(U)$ contains all the [[constant functions]]

   $$
     X 
       \overset{const_U}{\hookrightarrow} 
     \mathbf{X}(U) 
       \hookrightarrow 
     Hom_{Set}(U,X)
     \,,
   $$

1. for every [[function]] $\phi \;\colon\; U \to X$ and for every [[open cover]] $\{U_i \overset{\iota_i}{\to} U\}$, if each [[restriction]] is a plot, $\phi\vert_{U_i} \in \mathbf{X}(U_i)$, then $\phi$ itself is a plot: $\phi \in \mathbf{X}(U)$;

1. for all plots $\phi \in \mathbf{X}(U)$, all open subsets $V$ of any [[Euclidean space]], and all [[smooth functions]] $V \overset{f}{\to} U$, we have, the composition is again a plot

   $$
     \phi \circ f   \;\in\; \mathbf{X}(V)
     \,.
   $$

Moreover, for  $\mathbf{X}$ and $\mathbf{Y}$ two [[diffeological spaces]], as above,  then a _smooth map_ between them 

$$
  \mathbf{X} \overset{f}{\longrightarrow} \mathbf{Y}
$$

is a [[function]] of underlying sets

$$
  X \overset{\phantom{A} f \phantom{A}}{\longrightarrow} Y
  \;\;\in\;\;
  Set
$$

such that for each plot $\phi \in \mathbf{X}(U)$ of $\mathbf{X}$ the [[composition]] with that function is a plot of $\mathbf{Y}$:

$$
  f \circ \phi \;\in\; \mathbf{X}(U)
  \,.
$$

This defines a [[category]] $DiffeologicalSpace$ ([this def.](geometry+of+physics+--+categories+and+toposes#Categories)) whose [[objects]] are the diffeological spaces, whose [[morphisms]] are the smooth maps between them, with [[composition]] of morphisms the ordinary composition of functions of underlying sets.

=--

+-- {: .num_prop #DiffeologicalSpacesAreTheConcreteSmoothSets}
###### Proposition
**([[diffeological spaces]] are the [[concrete object|concret]] [[smooth sets]])**

The category of [[diffeological spaces]] (Def. \ref{DiffeologicalSpace}) is a [[full subcategory]] of the category of [[smooth sets]] (Def. \ref{CategoryOfSmoothSets}).

Moreover, in terms of the [[cohesive topos|cohesive]] structure on the category of smooth sets from Prop. \ref{SmoothSetsFormACohesiveTopos}, the diffeological spaces are precisely the _[[concrete objects]]_ ([this def.](geometry+of+physics+--+categories+and+toposes#CohesiveModalities)) among the [[smooth sets]]:

$$
  DiffeologicalSpace
  \;\simeq\;
  SmoothSet_{conc}
  \overset{\phantom{AAAA}}{\hookrightarrow}
  SmoothSet
  \,.
$$

=--


+-- {: .proof}
###### Proof

First observe that the assignment of sets of plots 

$$
  U \mapsto \mathbf{X}(U)
$$

of a diffeological space $\mathbf{X}$, according to Def. \ref{DiffeologicalSpace} constitutes a [[sheaf]] ([this Def.](geometry+of+physics+--+categories+and+toposes#Sheaf)) on the [[site]] $EuclOp$ of [[open subsets]] of [[Euclidean spaces]], 
by the same unwinding of Definitions as in Prop. \ref{SmoothSetsAreSheavesOnCartSp}:

* the third clause in the list of properties in Def. \ref{DiffeologicalSpace} says that the assignment of sets of plots is a [[presheaf]],

* the second clause in the list of properties says that this presheaf satisfies the [[sheaf|sheaf condition]],

* while the first clause in the list of properties is an extra condition, singling out diffeological spaces among all sheaves. 

Under this identification, the definition of a smooth map of diffeological spaces in Def. \ref{DiffeologicalSpace} says that it is equivalently a morphism of presheaves of sets of plots between sheaves of sets of plots, and hence a morphism of sheaves. This establishe a [[full subcategory]]-inclusion

$$
  DiffeologicalSpace
    \hookrightarrow
  Sh(EuclOp)
  \,.
$$

But by Prop. \ref{EquivalentSitesForCartSp} the restriction from the site $EuclOp$ of all open subsets of Euclidean spaces to that of just the site [[CartSp]] of [[Cartesian spaces]] is an [[equivalence of categories]] between the corresponding [[sheaf toposes]]. This yields the full subcategory inclusion

$$
  DiffeologicalSpace
   \hookrightarrow
  Sh(EuclOp)
    \simeq
  Sh(CartSp)
    \simeq
  SmoothSet
  \,,
$$

where the last equivalence is Prop. \ref{SmoothSetsAreSheavesOnCartSp}.

It remains to see that under this inclusion, the diffeological spaces are identified with the [[concrete objects]] among the smooth set.

By definition ([this Def.](geometry+of+physics+--+categories+and+toposes#CohesiveModalities)), a smooth set $\mathbf{X} \in SmoothSet$ is [[concrete object|concrete]], precisely if its [[sharp modality|sharp]]-unit is a [[monomorphism]]

$$
  \mathbf{X}  
    \overset{\phantom{A} \eta_X^\sharp \phantom{A}}{\hookrightarrow}
  \sharp \mathbf{X}
  \,,
$$ 

which is the [[adjunction unit]] ([this Def.](geometry+of+physics+--+categories+and+toposes#AdjunctionUnitFromHomIsomorphism)) of the $(\Gamma \dashv coDisc)$-adjunction

$$
  \mathbf{X}  
    \overset{\phantom{A} \eta_X \phantom{A}}{\hookrightarrow}
  coDisc \Gamma \mathbf{X}
  \,.
$$ 

Now a morphism of sheaves is a monomorphism, precisely if for each object $U \in CartSp$ in the site, its component function

\[
  \label{DecohesAsGammacoDiscUnit}
  \mathbf{X}(U)
    \overset{\phantom{A} \eta_X^\sharp(U) \phantom{A}}{\hookrightarrow}
  (coDisc \Gamma \mathbf{X})(U)
\] 

is an [[injective function]] ([this Prop.](geometry+of+physics+--+categories+and+toposes#RecognitionOfEpimorphisms)). Unde the [[Yoneda lemma]], this function may be re-identified as follows:


\[
  \label{CodiscretePlotIdentidification}
  \array{
    \mathbf{X}(U) &\simeq& Hom_{SmoothSet}(y(U), \mathbf{X})
    \\
    {}^{\mathllap{ \eta_X^\sharp(U) }}\big\downarrow
    &&
    {}^{\mathllap{ Hom_{SmoothSet}(y(U), \eta_X^\sharp ) }}\big\downarrow
    &\searrow^{\mathrlap{ \widetilde{\eta^\sharp_X \circ (-)} }}&
    \\
    (coDisc \Gamma \mathbf{X}(U))
    &\simeq&
    Hom_{SmoothSet}( y(U), coDisc \Gamma \mathbf{X} )
    &\simeq&
    Hom_{Set}( \Gamma y(U), \Gamma \mathbf{X} )
    &\simeq&
    Hom_{Set}( U, X )
    \\
    && \phi &\mapsto& \widetilde \phi
    \,,
  }
\]

where we first used the [[Yoneda lemma]] ([this Prop.](geometry+of+physics+--+categories+and+toposes#YonedaLemma)), then the adjunction isomorphism ([here](geometry+of+physics+--+categories+and+toposes#eq:HomIsomorphismForAdjointFunctors)) of $(\Gamma \dashv coDisc)$. 
In the final step we used that the cohesive structure on $SmoothSet$ comes from $CartSp$ being a [[cohesive site]] (Prop. \ref{SmoothSetsFormACohesiveTopos}) and that in this case $\Gamma$ is given by evaluation on the point ([here](geometry+of+physics+--+categories+and+toposes#CohesiveGlobalSectionsGivenByPointEvaluation)), and we wrote

\[
  \label{UnderlyingSetOfDiffeologicalSpaceAsSmoothSet}
  X \;\coloneqq\; \Gamma \mathbf{X} = \mathbf{X}(\ast)
\]

for the set of points in $\mathbf{X}$. Notice that if $\mathbf{X}$ is indeed a [[diffeological space]], then this set is indeed its underlying set, by the first clause in the list of conditions on a diffeological space in Def. \ref{DiffeologicalSpace}.

This shows that (eq:DecohesAsGammacoDiscUnit) being an injection means equivalently that we have an injection of the form

\[
  \label{RearrangedDecohesAsGammacoDiscUnit}
  \mathbf{X}(U)
    \overset{\phantom{A} \eta_X^\sharp(U) \phantom{A}}{\hookrightarrow}
  Hom_{Set}(U, X)
  \,.
\] 

Hence that $\mathbf{X}(U)$ is always a subset of the [[function set]] from $U$ to the set $X$, as in the second clause in Def. \ref{DiffeologicalSpace}.

This shows that every concrete smooth set is a diffeological space. For the converse, it remains to check that if we start with a diffeological space $\mathbf{X}$ with prescribed inclusion function

\[
  \label{DiffeologicalInclusionFunction}
  \mathbf{X}(U) \hookrightarrow Hom_{Set}(U,X)
\]

then (eq:RearrangedDecohesAsGammacoDiscUnit) indeed reproduces this inclusion. 

To see this, first notice that, by the [[Yoneda lemma]] ([this prop.](geometry+of+physics+--+categories+and+toposes#YonedaLemma)) and the definition of smooth maps between diffeological spaces, the inclusion function (eq:DiffeologicalInclusionFunction) equals the component function of the [[functor]] $\Gamma \;\colon\; SmoothSet \to Set$, that acts by point evaluation:

$$
  \Gamma_{y(U),\mathbf{X}}
  \;\colon\;
  \array{
    Hom_{SmoothSet}( y(U), \mathbf{X} )
    &\hookrightarrow&
    Hom_{Set}( \Gamma y(U), \Gamma \mathbf{X} )
    \\
    f &\mapsto& \Gamma(f)
  }
$$

Hence, by (eq:DecohesAsGammacoDiscUnit), we need to show that

\[
  \label{PostcompositionWithEtaAsGamma}
  \Gamma_{y(U), \mathbf{X}} \;=\;  \widetilde{\eta_{\mathbf{X}} \circ (-)}
  \,.
\]

But this holds as a general fact about [[adjunctions]] (a special case of [this Example](geometry+of+physics+–+basic+notions+of+category+theory#ReExpressingMiddleFunctorInAdjointTriple)).

=--

By [this prop.](geometry+of+physics+--+categories+and+toposes#QuasitoposOfConcreteObjects) it follows that

+-- {: .num_prop #ReflectiveInclusionOfDiffeologicalSpacesinSmoothSets}
###### Proposition
**([[reflective subcategory|reflection]] of [[diffeological spaces]] in [[cohesive topos]] of [[smooth sets]])**

The [[category]] of [[diffeological spaces]] (Def. \ref{DiffeologicalSpace}) is "in between" the [[category of sets]] ([this Example](geometry+of+physics+--+categories+and+toposes#CategoryOfSets)) and the category of [[smooth sets]] (Def. \ref{CategoryOfSmoothSets}) as exhibited by the following system of [[adjoint functors]]:

$$
  \array{
     \\
     \phantom{a}
     \\
     \phantom{A}
     \\
     \Gamma \;\dashv\; coDisc
  }
  \;\;\colon\;\;
  SmoothSet
  \array{
    \phantom{\overset{ \phantom{AA} \Pi_0 \phantom{AA} }{\longrightarrow}}
    \\
    \phantom{\overset{ \phantom{AA} Disc \phantom{AA} }{\hookleftarrow}}
    \\
    \overset{\phantom{AA} conc \phantom{AA}}{\longrightarrow}
    \\
    \overset{\phantom{AA} \iota_{conc} \phantom{AA}}{\hookleftarrow}
  }
  DiffeologicalSpace
  \array{
    \overset{ \phantom{AA} \Pi_0 \phantom{AA} }{\longrightarrow}
    \\
    \overset{ \phantom{AA} Disc \phantom{AA} }{\hookleftarrow}
    \\
    \overset{\phantom{AA}\Gamma \phantom{AA}}{\longrightarrow}
    \\
    \overset{\phantom{AA}coDisc\phantom{AA}}{\hookleftarrow}
  }
  Set
$$

where on the left we have a [[reflective subcategory]] with reflector being _[[concretification]]_ ([this prop.](geometry+of+physics+--+categories+and+toposes#QuasitoposOfConcreteObjects)), and on the right we have the [[corestriction|co]][[restriction]] of the [[adjoint quadruple]] of [[cohesion]] from (eq:SheafToposAdjointQuadruple).

=--


+-- {: .num_prop #FrechetManifoldsFullyFaithfulInSmoothSets}
###### Proposition
**([[Fréchet manifolds]] [[fully faithful functor|fully faithful]] among [[smooth sets]])**


Write $FrechetMfd$ for the [[category]] of [[Fréchet manifolds]] and [[smooth functions]] between these, which generalizes smooth manifolds to possibly [[infinite-dimensional manifold|infinite-dimensional]] smooth manifolds

$$
  CartSp 
   \overset{\phantom{AAAA}}{\hookrightarrow} 
  SmoothMfd 
    \overset{\phantom{AAAA}}{\hookrightarrow} 
  FrechetMfd
  \,.
$$

For $X,Y$ two [[Fréchet manifolds]], write again $C^\infty(X,Y)$ for the set of [[smooth functions]] between them. Then the same kind of construction as for [[smooth manifolds]], sending a Fr&#233;chet manifold to the [[presheaf]]

$$
  \mathbb{R}^n \mapsto C^\infty(\mathbb{R}^n, X)
$$

defines a [[fully faithful functor]] ([this Example](geometry+of+physics+--+categories+and+toposes#FullyFaithfulFunctor))

$$
  FrechetMfd \overset{\phantom{AAAA}}{\hookrightarrow} SmoothSet
  \,,
$$

hence a [[full subcategory]] inclusion.

=--

+-- {: .proof}
###### Proof

The construction clearly factors through [[diffeological spaces]] (Def. \ref{DiffeologicalSpace}), identified as a [[full subcategory]] of [[smooth sets]] via Prop. \ref{ReflectiveInclusionOfDiffeologicalSpacesinSmoothSets}.

With this it is now sufficient to see that [[Fréchet manifolds]] are fully faithful among [[diffeological spaces]]. This is due to ([Losik 94, theorem 3.1.1](diffeological+space#Losik)),

=--

$\,$

### Differential forms
  {#DifferentialForms}

We have seen above in _[The continuum real line](#TheContinuumRealWorldLine)_ that that [[real line]] $\mathbb{R}$ is the basic [[kinematics|kinematical structure]] in the [[differential geometry]] of [[physics]]. Notably the smooth [[path spaces]] $[\mathbb{R}, X]$ from example \ref{SmoothPathSpace} are to be thought of as the smooth spaces of _trajectories_ (for instance of some [[particle]]) in a [[smooth space]] $X$, hence of smooth maps $\mathbb{R} \to X$.

But moreover, _[[dynamics]]_ in [[physics]]  is encoded by _[[linear functionals|functionals]] on such trajectories_: by "[[action functionals]]". In the simplest case these are for instance homomorphisms of smooth spaces

$$
  S \colon \left[I, X\right] \to \mathbb{R}
  \,,
$$

where $I \hookrightarrow \mathbb{R}$ is the standard unit [[interval]].

Such [[action functionals]] we discuss in their own right in _[Variational calculus](#VariationalCalculus)_ below. Here we first examine in detail a fundamental property they all have: they are supposed to be _[[local action functional|local]]_.

Foremost this means that the value associated to a trajectory is _built up incrementally_ from small contributions associated to small sub-trajectories: if a trajectory $\gamma$ is decomposed as a trajectory $\gamma_1$ followed by a trajectory $\gamma_2$, then the action functional is additive

$$
  S(\gamma) = S(\gamma_1) + S(\gamma_2)
  \,.
$$

As one takes this property to the limit of iterative subdivision, one finds that action functionals are entirely determined by their value on _[[infinitesimal space|infinitesimal]] displacements_ along the worldline. If $\gamma \colon \mathbb{R} \to X$ denotes a path and "$\dot \gamma(x)$" denotes the corresponding "infinitesimal path" at worldline parameter $x$, then the value of the action functional on such an infinitesimal path is traditionally written as

$$
  \mathbf{d}S(\dot \gamma)_x  \in \mathbb{R}
  \,,
$$

to be read as "the small change $\mathbf{d}S$ of $S$ along the infinitesimal path $\dot \gamma_x$". 

This function $\mathbf{d}S$ that assigns numbers to infinitesimal paths is called a _[[differential form]]_. Etymologically this originates in the use of "form" as in _[[bilinear form]]_: something that is evaluated. Here it is evaluated on _infinitesimal differences_, referred to as _differentials_.

$\,$

+-- {: .num_defn #Differential1FormsOnCartesianSpaces}
###### Definition

For $n \in \mathbb{N}$ a **[[smooth differential 1-form]]** $\omega$ on a [[Cartesian space]] $\mathbb{R}^n$ is an $n$-[[tuple]] 

$$
  \left(\omega_i \in CartSp\left(\mathbb{R}^n,\mathbb{R}\right)\right)_{i = 1}^n
$$

of [[smooth functions]], which we think of equivalently as the [[coefficients]] of a [[formal linear combination]]

$$
  \omega = \sum_{i = 1}^n f_i \mathbf{d}x^i
$$

on a [[set]] $\{\mathbf{d}x^1, \mathbf{d}x^2, \cdots, \mathbf{d}x^n\}$ of [[cardinality]] $n$.

Write 

$$
  \Omega^1(\mathbb{R}^k) \simeq CartSp(\mathbb{R}^k, \mathbb{R})^{\times k}\in Set
$$

for the set of smooth [[differential 1-forms]] on $\mathbb{R}^k$.

=--

+-- {: .num_remark}
###### Remark

We think of $\mathbf{d} x^i$ as a measure for [[infinitesimal space|infinitesimal]] displacements along the $x^i$-[[coordinate]] of a [[Cartesian space]]. This idea is made precise below in _[Differential 1-forms are smooth increnemental path measures](#1FormsAsSmoothFunctors)_.

=--

If we have a measure of infintesimal displacement on some $\mathbb{R}^n$ and a smooth function $f \colon \mathbb{R}^{\tilde n} \to \mathbb{R}^n$, then this induces a measure for infinitesimal displacement on $\mathbb{R}^{\tilde n}$ by sending whatever happens there first with  $f$ to $\mathbb{R}^n$ and then applying the given measure there. This is captured by the following definition.

+-- {: .num_defn #PullbackOfDifferential1FormsOnCartesianSpaces}
###### Definition

For $\phi \colon \mathbb{R}^{\tilde k} \to \mathbb{R}^k$ a [[smooth function]], the **[[pullback of differential forms|pullback of differential 1-forms]]** along $\phi$ is the [[function]]

$$
  \phi^* \colon \Omega^1(\mathbb{R}^{k}) \to \Omega^1(\mathbb{R}^{\tilde k})
$$

between sets of differential 1-forms, def. \ref{Differential1FormsOnCartesianSpaces}, which is defined on [[basis]]-elements by

$$
  \phi^* \mathbf{d} x^i \coloneqq \sum_{j = 1}^{\tilde k} \frac{\partial \phi^i}{\partial \tilde x^j} \mathbf{d}\tilde x^j
$$

and then extended linearly by

$$
  \begin{aligned}
    \phi^* \omega & = \phi^* \left( \sum_{i} \omega_i \mathbf{d}x^i \right)
    \\
    & \coloneqq
     \sum_{i = 1}^k \left(\phi^* \omega\right)_i \sum_{j = 1}^{\tilde k} \frac{\partial \phi^i }{\partial \tilde x^j}  \mathbf{d} \tilde x^j 
    \\
    & = 
     \sum_{i = 1}^k  \sum_{j = 1}^{\tilde k} (\omega_i \circ \phi) \cdot \frac{\partial \phi^i }{\partial \tilde x^j}  \mathbf{d} \tilde x^j 
  \end{aligned}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The term "pullback" in _[[pullback of differential forms]]_ is not really related, certainly not historically, to the term _[[pullback]]_ in [[category theory]]. One can relate the pullback of differential forms to categorical pullbacks, but this is not really essential here. The most immediate property that both concepts share is that they take a [[morphism]] going in one direction to a map between structures over domain and codomain of that morphism which goes in the other direction, and in this sense one is "pulling back structure along a morphism" in both cases.

=--

Even if in the above definition we speak only about the [[set]] $\Omega^1(\mathbb{R}^k)$ of differential 1-forms, this set naturally carries further [[structure]].

+-- {: .num_defn #ModuleStructureOn1FormsOnRk}
###### Definition

1. The set $\Omega^1(\mathbb{R}^k)$ is naturally an [[abelian group]] with addition given by componentwise addition

   $$
      \begin{aligned}
         \omega + \lambda & =
          \sum_{i = 1}^k \omega_i \mathbf{d}x^i + \sum_{j = 1}^k \lambda_j \mathbf{d}x^j
         \\
         & = \sum_{i = 1}^k(\omega_i + \lambda_i) \mathbf{d}x^i
      \end{aligned}
      \,,
   $$

1. The abelian group $\Omega^1(\mathbb{R}^k)$ is naturally equipped with the structure of a [[module]] over the [[ring]] $C^\infty(\mathbb{R}^k,\mathbb{R}) = CartSp(\mathbb{R}^k, \mathbb{R})$ of [[smooth functions]], where the [[action]] $C^\infty(\mathbb{R}^k,\mathbb{R}) \times\Omega^1(\mathbb{R}^k) \to \Omega^1(\mathbb{R}^k)$ is given by componentwise multiplication

   $$
     f \cdot \omega = \sum_{i = 1}^k( f \cdot \omega_i) \mathbf{d}x^i
     \,.
   $$

=--

+-- {: .num_defn }
###### Remark

More abstractly, this just says that $\Omega^1(\mathbb{R}^k)$ is the [[free module]] over $C^\infty(\mathbb{R}^k)$ on the set $\{\mathbf{d}x^i\}_{i = 1}^k$.

=--

The following definition captures the idea that if $\mathbf{d} x^i$ is a measure for displacement along the $x^i$-[[coordinate]], and $\mathbf{d}x^j$ a measure for displacement along the $x^j$ coordinate, then there should be a way te get a measure, to be called $\mathbf{d}x^i \wedge \mathbf{d} x^j$, for infinitesimal _surfaces_ (squares) in the $x^i$-$x^j$-plane. And this should keep track of the [[orientation]] of these squares, with 

$$
  \mathbf{d}x^j \wedge \mathbf{d}x^i = - \mathbf{d}x^i \wedge \mathbf{d} x^j
$$

being the same infinitesimal measure with orientation reversed.

+-- {: .num_defn #DifferentialnForms}
###### Definition

For $k,n \in \mathbb{N}$, the **smooth [[differential forms]]** on $\mathbb{R}^k$ is the [[exterior algebra]]

$$
  \Omega^\bullet(\mathbb{R}^k) 
   \coloneqq
  \wedge^\bullet_{C^\infty(\mathbb{R}^k)} \Omega^1(\mathbb{R}^k)
$$

over the [[ring]] $C^\infty(\mathbb{R}^k)$ of [[smooth functions]] of the [[module]] $\Omega^1(\mathbb{R}^k)$ of smooth 1-forms, prop. \ref{ModuleStructureOn1FormsOnRk}.

We write $\Omega^n(\mathbb{R}^k)$ for the sub-module of degree $n$ and call its elements the **smooth [[differential n-forms]]**.

=--

+-- {: .num_remark}
###### Remark

Explicitly this means that a [[differential n-form]] $\omega \in \Omega^n(\mathbb{R}^k)$ on $\mathbb{R}^k$ is a [[formal linear combination]] over $C^\infty(\mathbb{R}^k)$ of [[basis]] elements of the form $\mathbf{d} x^{i_1} \wedge \cdots \wedge \mathbf{d}x^{i_n}$ for $i_1 \lt i_2 \lt \cdots \lt i_n$:

$$
  \omega = \sum_{1 \leq i_1 \lt i_2 \lt \cdots \lt i_n \lt k} \omega_{i_1, \cdots, i_n} \mathbf{d}x^{i_1} \wedge \cdots \wedge \mathbf{d}x^{i_n}
  \,.
$$


=--

+-- {: .num_defn #PullbackOfDifferentialForms}
###### Definition

The [[pullback of differential forms|pullback of differential 1-forms]] of def. \ref{Differential1FormsOnCartesianSpaces} extends as an $C^\infty(\mathbb{R}^k)$-[[associative algebra|algebra]] [[homomorphism]] to $\Omega^n(-)$, given for a smooth function $f \colon \mathbb{R}^{\tilde k} \to \mathbb{R}^k$ on basis elements by

$$
  f^* \left(  \mathbf{d}x^{i_1} \wedge \cdots \wedge \mathbf{d}x^{i_n} \right)
  = 
  \left(f^* \mathbf{d}x^{i_1} \wedge \cdots \wedge f^* \mathbf{d}x^{i_n} \right)
  \,. 
$$ 

=--

$\,$

So far we have defined differential $n$-form on abstract coordinate systems. Here we extend this definition to one of differential $n$-forms on arbitrary [[smooth sets]]. We start by observing that the space of _all_ differential $n$-forms on cordinate systems themselves naturally is a smooth set.

+-- {: .num_prop #SmoothModuliSpaceOfnForms}
###### Proposition
**([[smooth set|smooth]] [[moduli space]] of [[differential forms]])**

The assignment of differential $n$-forms

$$
  \Omega^n(-) \colon \mathbb{R}^k \mapsto \Omega^n(\mathbb{R}^k)
$$

of def. \ref{DifferentialnForms} together with the [[pullback of differential forms]]-functions of def. \ref{PullbackOfDifferentialForms}

$$
  \array{
    \mathbb{R}^{k_1} &\mapsto & \Omega^n(\mathbb{R}^{k_1})
    \\
    \uparrow^{\mathrlap{f}} && \downarrow^{\mathrlap{f^*}}
    \\
    \mathbb{R}^{k_2} &\mapsto& \Omega^n(\mathbb{R}^{k_2})
  }
$$

constitutes a [[smooth set]] in the sense of def. \ref{SmoothSpace}, which we denote by

$$
  \mathbf{\Omega}^n(-) \;\in\; SmoothSet
  \,.
$$

We call this  the **universal smooth [[moduli space]]** of differential $n$-forms. 

=--

The reason for this terminology is that homomorphisms of smooth sets into $\Omega^1$ _modulate_ differential $n$-forms on their [[domain]], by prop. \ref{YonedaForSmoothSpaces} (and hence by the [[Yoneda lemma]], [this prop](geometry+of+physics+--+categories+and+toposes#YonedaLemma)):

+-- {: .num_example}
###### Example

For the [[Cartesian space]] $\mathbb{R}^k$ regarded as a [[smooth set]] by example \ref{CartesianSpaceAsSmoothSpace}, there is a [[natural bijection]]

$$
  \Omega^n(\mathbb{R}^k) \simeq Hom(\mathbb{R}^k, \Omega^1)
$$

between the set of smooth $n$-forms on $\mathbb{R}^n$ according to def. \ref{Differential1FormsOnCartesianSpaces} and the set of homomorphism of smooth set, $\mathbb{R}^k \to \Omega^1$, according to def. \ref{HomomorphismOfSmoothSpaces}.

=--

In view of this we have the following elegant definition of smooth $n$-forms on an arbitrary smooth set.

+-- {: .num_defn #DifferentialnFormOnSmoothSpace}
###### Definition

For $X \in SmoothSet$ a [[smooth set]], def. \ref{SmoothSpace}, a **[[differential n-form]]** on $X$ is a [[homomorphism]] of [[smooth sets]] of the form

$$
  \omega \colon X \to \Omega^n(-)
  \,.
$$

Accordingly we write

$$
  \Omega^n(X) \coloneqq SmoothSet(X,\Omega^n)
$$

for the set of smooth $n$-forms on $X$.

=--

We may unwind this definition to a very explicit description of differential forms on smooth sets. This we do in a moment in remark \ref{DifferentialFormOnSmoothSpaceAsSystemOfDiffFormsOnCoordinates}.

Notice that differential 0-forms are equivalently smooth $\mathbb{R}$-valued functions.

+-- {: .num_example #SpaceOf0FormsIsRealLine}
###### Examples

$$
  \Omega^0 \;\simeq\; \mathbb{R}
$$

=--


+-- {: .num_defn #PullbackOfDifferentialFormsOnSmoothSpaces}
###### Definition

For $f \colon X \to Y$ a [[homomorphism]] of [[smooth sets]], def. \ref{HomomorphismOfSmoothSpaces}, the **[[pullback of differential forms]]** along $f$ is the [[function]]

$$
  f^* \colon \Omega^n(Y) \to \Omega^n(X)
$$

given by the [[hom-functor]] into the smooth set $\Omega^n$ of def. \ref{SmoothModuliSpaceOfnForms}:

$$
 f^* \coloneqq Hom(-, \Omega^n)
 \,.
$$

This means that it sends an $n$-form $\omega \in \Omega^n(Y)$ which is modulated by a homomorphism $Y \to \Omega^n$ to the $n$-form $f^* \omega \in \Omega^n(X)$ which is modulated by the [[composition|composite]] $X \stackrel{f}{\to} Y \to \Omega^n$.

=--

+-- {: .num_defn}
###### Proposition

For $X = \mathbb{R}^{\tilde k}$ and $Y = \mathbb{R}^{k}$ definition \ref{PullbackOfDifferentialFormsOnSmoothSpaces} reproduces def. \ref{PullbackOfDifferentialForms}.

=--

+-- {: .proof}
###### Proof

Again by the [[Yoneda lemma]] ([this prop.](geometry+of+physics+--+categories+and+toposes#YonedaLemma))

=--

+-- {: .num_remark #DifferentialFormOnSmoothSpaceAsSystemOfDiffFormsOnCoordinates}
###### Remark

Using def. \ref{PullbackOfDifferentialFormsOnSmoothSpaces}

Unwinding def. \ref{DifferentialnFormOnSmoothSpace} yields the following explicit description:

a differential $n$-form $\omega \in \Omega^n(X)$ on a smooth set $X$ is

1. for each way $\phi \colon \mathbb{R}^k \to X$ of laying out a coordinate system $\mathbb{R}^k$ in $X$ a differential $n$-form

   $$
     \phi^* \omega \in \Omega^n(\mathbb{R}^k)
   $$

   on the abstract coordinate system, as given by def. \ref{DifferentialnForms};

1. for each abstract [[coordinate transformation]] $f \colon \mathbb{R}^{k_2} \to \mathbb{R}^{k_1}$ a corresponding compatibility condition between local differential forms $\phi_1 \colon \mathbb{R}^{k_1} \to X$ and $\phi_2 \colon \mathbb{R}^{k_2} \to X$ of the form

   $$
     f^* \phi_1^* \omega = \phi_2^* \omega
     \,.
   $$

Hence a differential form on a smooth set is simply a collection of differential forms on all its coordinate systems such that these glue along all possible coordinate transformations.

=--


The following adds further explanation to the role of $\Omega^n \in Smooth0Tye$ as a _[[moduli space]]_. Notice that since $\Omega^n$ is itself a [[smooth set]], we may speak about differential $n$-forms on $\Omega^n$ itsefl.

+-- {: .num_defn #UniversalDifferentialnForm}
###### Definition

The **universal differential $n$-form** is the differential $n$-form

$$
  \omega^n_{univ} \in \Omega^n(\Omega^n)
$$

which is modulated by the [[identity]] [[homomorphism]] $id \colon \Omega^n \to \Omega^n$.

=--

With this definition we have:

+-- {: .num_prop}
###### Proposition

For $X \in SmoothSet$ any [[smooth set]], every differential $n$-form on $X$, $\omega \in \Omega^n(X)$ is the pullback of differential forms, def. \ref{PullbackOfDifferentialFormsOnSmoothSpaces}, of the universal differential $n$-form, def. \ref{UniversalDifferentialnForm}, along a homomorphism $f$ from $X$ into the moduli space $\Omega^n$ of differential $n$-forms:

$$
  \omega = f^* \omega^n_{univ}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This statement is of course in a way a big tautology. Nevertheless it is a very useful tautology to make explicit. The whole concept of differential forms on smooth sets here may be thought of as simply a variation of the theme of the [[Yoneda lemma]] ([this prop.](geometry+of+physics+--+categories+and+toposes#YonedaLemma)).

=--

$\,$

We discuss the smooth space of differential forms _on a fixed smooth space_ $X$. 

+-- {: .num_remark}
###### Remark

For $X$ a [[smooth space]], the smooth mapping space $[X, \Omega^n] \in SmoothSet$ is the smooth space whose $\mathbb{R}^k$-plots are differential $n$-forms on the [[product]] $X \times \mathbb{R}^k$

$$
  [X, \Omega^n] \colon \mathbb{R}^k \mapsto \Omega^n(X \times \mathbb{R}^k)
  \,.
$$

This is not _quite_ what one usually wants to regard as an $\mathbb{R}^k$-parameterized of differential forms on $X$. That is instead usually meant to be a differential form $\omega$ on $X \times \mathbb{R}^k$ which has "no leg along $\mathbb{R}^k$". Another way to say this is that the family of forms on $X$ that is represented by some $\omega$ on $X \times \mathbb{R}^k$ is that which over a point $v \colon * \to \mathbb{RR}^k$ has the value $(id_X,v)^* \omega$. Under this [[pullback of differential forms]] any components of $\omega$ with "legs along $\mathbb{R}^k$" are identified with the 0 differential form 

=--

This is captured by the following definition.


+-- {: .num_defn #SmoothSpaceOfFormsOnSmoothSpace}
###### Definition
**([[concrete object|concrete]] [[moduli space]] of [[differential forms]] on a [[smooth set]])** 

For $X \in SmoothSet$ any [[smooth set]] and $n \in \mathbb{N}$, the _smooth space of differential $n$-forms_ $\mathbf{\Omega}^n(X)$ on $X$ is the [[concretification]] (Prop. \ref{ReflectiveInclusionOfDiffeologicalSpacesinSmoothSets}) of the smooth mapping space $[X, \Omega^n]$, def. \ref{SmoothFunctionSpace}, into the smooth moduli space of differential $n$-forms, def. \ref{SmoothModuliSpaceOfnForms}:

$$
  \mathbf{\Omega}^n(X)_{conc} \; \coloneqq \; Conc([X, \Omega^n])
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The $\mathbb{R}^k$-plots of $\mathbf{\Omega}^n(\mathbb{R}^k)$
are indeed smooth differential $n$-forms on $X \times \mathbb{R}^k$ which are such that their evaluation on vector fields tangent to $\mathbb{R}^k$ vanish.

=--

+-- {: .proof}
###### Proof (sketch)

By the proof of [this Prop.](geometry+of+physics+--+categories+and+toposes#QuasitoposOfConcreteObjects) spring the set of plots of $\mathbf{\Omega}^n(X)$ over $\mathbb{R}^k$ is the [[image]] of the [[function]]

$$
  \Omega^n(X \times \mathbb{R}^k)
  \simeq
   Hom_{SmoothSet}(\mathbb{R}^k, [X,\Omega^n])
   \stackrel{\Gamma_{ \mathbb{R}^k, [X,\Omega^n] }}{\to}
   Hom_{Set}(\Gamma(\mathbb{R}^k), \Gamma [X, \Omega^n])
   \simeq
   Hom_{Set}(\mathbb{R}^k_s, \Omega^n(X))
  \,,
$$

where on the right $\mathbb{R}^k_s$ denotes, just for emphasis, the underlying set of $\mathbb{R}^k$. This function manifestly sends a smooth differential form $\omega \in \Omega^n(X \times \mathbb{R}^k)$ to the function from points $v$ of $\mathbb{R}^k$ to differential forms on $X$ given by

$$
  \omega \mapsto \left(v \mapsto  (id_X, v)^* \omega \right)
  \,.
$$

Under this function all components of differential forms with a "leg along" $\mathbb{R}^k$ are sent to the 0-form. Hence the image of this function is the collection of smooth forms on $X \times \mathbb{R}^k$ with "no leg along $\mathbb{R}^k$".

=--

+-- {: .num_remark }
###### Remark

For $n = 0$ we have (for any $X\in SmoothSet$)

$$
  \begin{aligned}
    \mathbf{\Omega}^0(X) 
      & \coloneqq Conc [X, \Omega^0]
    \\
    & \simeq Conc [X, \mathbb{R}]
    \\
    & \simeq [X, \mathbb{R}]
  \end{aligned}
  \,,
$$

by prop. \ref{SpaceOf0FormsIsRealLine}.

=--


$\,$

### Integration and transgression


The traditional concept of [[integration of differential forms]] over a [[compact space|compact]] [[smooth manifold]] $\Sigma$ applies in smooth families of differential forms and hence constitutes in fact a [[smooth function]] from the [[smooth set|smooth]] [[moduli space]] of [[differential forms]] on the given manifold, this is Def. \ref{ParameterizedIntegrationOfDifferentialForms} below.

Using this, [[transgression of differential forms]] may be defines as the application of the [[mapping space]]-[[functor]] out of $\Sigma$ to the [[modulating morphisms]] of [[differential forms]] and applying [[integration of differential forms]] to the result (Def. \ref{TransgressionOfDifferentialFormsToMappingSpaces} below). This simple construction turns out to be equivalent to the traditional definition (Prop. \ref{EquivalenceOfTransgressionOfDifferentialFormsToMappingSpaces} below).


+-- {: .num_defn #ParameterizedIntegrationOfDifferentialForms}
###### Definition
**(parameterized [[integration of differential forms]])

Let 

1. $X$ be a [[smooth set]];

1. $\Sigma_k$ be a [[compact topological space|compact]] [[smooth manifold]] of [[dimension]] $k$, regarded as a [[smooth set]] via Example \ref{CartesianSpaceAsSmoothSpace}.

1. $n \geq k \in \mathbb{N}$ a [[natural number]];

Consider the [[smooth set|smooth]] [[mapping space]] $[\Sigma_k, \mathbf{\Omega}^n]$ (Def. \ref{SmoothFunctionSpace}) out of $\Sigma_k$ into the universal [[smooth set|smooth]] [[moduli space]] $\mathbf{\Omega}^n$ of [[differential n-forms]] (Prop. \ref{SmoothModuliSpaceOfnForms}).

Then we write

$$
  \int_{\Sigma}
    \;\colon\;
  [\Sigma_k, \mathbf{\Omega}^n]
    \longrightarrow
  \mathbf{\Omega}^{n-k}
$$

for the [[smooth function]] (Def. \ref{HomomorphismOfSmoothSpaces}) which takes a plot $\omega_{(-)} \colon U \to [\Sigma, \mathbf{\Omega}^k]$, hence equivalently a differential $n$-form $\omega_{(-)}(-)$ on $U \times \Sigma$, to the result of [[integration of differential forms]] over $\Sigma$:


$$
  \int_{\Sigma} \omega_{(-)}(-) \coloneqq \int_\Sigma \omega_{(-)}
  \,.
$$


=--


+-- {: .num_defn #TransgressionOfDifferentialFormsToMappingSpaces}
###### Definition
**([[transgression of differential forms]] to [[mapping spaces]])

Let 

1. $X$ be a [[smooth set]];

1. $\Sigma_k$ be a [[compact topological space|compact]] [[smooth manifold]] of [[dimension]] $k$, regarded as a [[smooth set]] via Example \ref{CartesianSpaceAsSmoothSpace}.

1. $n \geq k \in \mathbb{N}$ a [[natural number]];

Consider the [[smooth set|smooth]] [[mapping space]] $[\Sigma_k, \mathbf{\Omega}^n]$ (Def. \ref{SmoothFunctionSpace}) out of $\Sigma_k$ into the universal [[smooth set|smooth]] [[moduli space]] $\mathbf{\Omega}^n$ of [[differential n-forms]] (Prop. \ref{SmoothModuliSpaceOfnForms}).


Then the operation of _[[transgression of differential n-forms]]_ on $X$ with respect to $\Sigma_k$ is the [[function]]

$$
  \tau_\Sigma
   \;\coloneqq\;
  \int_\Sigma [\Sigma,-]
   \;\colon\;
  \Omega^n(X) \to \Omega^{n-k}([\Sigma,X])
$$

from [[differential n-forms]] on $X$ to differential $n-k$-forms on the [[smooth set|smooth]] [[mapping space]] $[\Sigma_k,X]$ spring  which takes the differential form corresponding to the smooth function

$$
  (X \stackrel{\omega}{\to} \Omega^n) \in \Omega^n(X)
$$

to the differential form corresponding to the following composite smooth function:

$$
  \tau_\Sigma \omega
   \coloneqq
  \int_{\Sigma} [\Sigma,\omega]
   \;\colon\;
  [\Sigma, X] 
    \stackrel{[\Sigma, \omega]}{\longrightarrow}  
  [\Sigma, \Omega^n]
    \stackrel{\int_{\Sigma}}{\longrightarrow}
  \Omega^{n-k}
  \,,
$$

where $[\Sigma,\omega]$ is the [[mapping space]] [[functor]] on [[morphisms]] and $\int_{\Sigma}$ is the parameterized integration of differential forms from def. \ref{ParameterizedIntegrationOfDifferentialForms}.

More explicitly in terms of plots this means equivalently the following 

A plot of the [[mapping space]]

$$
  \phi_{(-)} \;\colon\; U \to [\Sigma, X] 
$$

is equivalently a [[smooth function]] of the form

$$
  \phi_{(-)}(-) \;\colon\; U \times \Sigma \to X
  \,.
$$

The smooth function $[\Sigma,\omega]$ takes this smooth function to the plot

$$
  U \times \Sigma \to X
   \overset{\phi_{(-)}(-)}{\longrightarrow}
  X 
   \overset{\omega}{\longrightarrow}
  \mathbf{\Omega}^{n}
$$

which is equivalently a differential form

$$
  (\phi_{(-)}(-))^\ast \omega \in \Omega^n(U \times \Sigma)
  \,.
$$

Finally the smooth function $\int_\Sigma$ takes this to the result of [[integration of differential forms]] over $\Sigma$:

$$
  \tau_{\Sigma}\omega\vert_{\phi_{(-)}}
  \;=\;
  \int_\Sigma (\phi_{(-)}(-))^\ast \omega
  \;\in\;
  \Omega^{n-k}(U)
  \,.
$$


=--


+-- {: .num_defn #TransgressionOfDifferentialFormsToMappingSpacesViaEvaluationMap}
###### Definition
**([[transgression of differential forms]] to [[mapping space]] via [[evaluation map]])**

Let 

1. $X$ be a [[smooth set]];

1. $n \geq k \in \mathbb{N}$;

1. $\Sigma_k$ be a [[compact topological space|compact]] [[smooth manifold]] of [[dimension]] $k$.

Then the operation of _transgression of differential $n$-forms_ on $X$ with respect to $\Sigma$ is the [[function]]

$$
  \tau_\Sigma
   \coloneqq
  \int_\Sigma ev^\ast
   \;\colon\;
  \Omega^n(X)
    \overset{ev^\ast}{\longrightarrow} 
  \Omega^n(\Sigma \times [\Sigma, X])
    \overset{\int_\Sigma}{\longrightarrow}
  \Omega^{n-k}([\Sigma,X])
$$

from differential $n$-forms on $X$ to differential $n-k$-forms on the [[mapping space]] $[\Sigma,X]$ (Def. \ref{SmoothFunctionSpace}) which is the [[composition|composite]] of forming the [[pullback of differential forms]] along the [[evaluation map]] $ev \colon  [\Sigma, X] \times \Sigma \to X$ with [[integration of differential forms]] over $\Sigma$.

This construction manifestly extends to the [[smooth set]] of [[differential forms]]

=--



+-- {: .num_prop #EquivalenceOfTransgressionOfDifferentialFormsToMappingSpaces}
###### Proposition

The two definitions of [[transgression of differential forms]] to mapping spaces from def. \ref{TransgressionOfDifferentialFormsToMappingSpaces} and def. \ref{TransgressionOfDifferentialFormsToMappingSpacesViaEvaluationMap} are equivalent.


=--

+-- {: .proof}
###### Proof


We need to check that for all plots $\gamma \colon U \to [\Sigma, X]$
the pullbacks of the two forms to $U$ coincide.

For def. \ref{TransgressionOfDifferentialFormsToMappingSpacesViaEvaluationMap} we get

$$
  \gamma^\ast \int_\Sigma \mathrm{ev}^\ast A
  =
  \int_\Sigma (\gamma,\mathrm{id}_\Sigma)^\ast \mathrm{ev}^\ast A
  \;
  \in \Omega^n(U)
$$

Here we recognize in the integrand the pullback along
the $( (-)\times \Sigma \dashv [\Sigma,-])$-[[adjunct]] $\tilde \gamma : U \times \Sigma \to \Sigma$ of $\gamma$,
which is given by applying the [[left adjoint]] $(-)\times \Sigma$ and then postcomposing with the adjunction counit $\mathrm{ev}$:

$$
  \array{
    U \times \Sigma
    &
     \overset{(\gamma, \mathrm{id}_\Sigma)}{\longrightarrow}
    &
    [\Sigma,X] \times \Sigma
    &
      \overset{\mathrm{ev}}{\longrightarrow}
    &
    X
  }
  \,.
$$
 
Hence the integral is now

$$
  \cdots = \int_{\Sigma} \tilde \gamma^\ast A
  \,.
$$

This is the operation of the top horizontal composite in the following
[[natural transformation|naturality square]] for [[adjuncts]], and so the claim follows by its [[commuting diagram|commutativity]]:

$$
  \array{
    \tilde \gamma \in 
    & 
    Hom(U \times\Sigma, X)
    &
      \overset{Hom(U \times \Sigma,A)}{\longrightarrow}
    &    
    Hom(U \times \Sigma, \mathbf{\Omega}^{n+k})
    &
      \overset{\int_\Sigma(U)}{\longrightarrow}
    &
    \Omega^n(U)
    \\
    &
    {}^{\mathllap{\simeq}}\big\downarrow
      &&
    {}^{\mathllap{\simeq}}\big\downarrow
      &&
    {}^{\mathllap{\simeq}}\big\downarrow
    \\
    \gamma \in 
    & 
    Hom(U,[\Sigma,X])
    &
      \overset{Hom(U,[\Sigma,A])}{\longrightarrow}
    &
    Hom(U,[\Sigma,\mathbf{\Omega}^{n+k}])
    &
      \overset{Hom(U,\int_\Sigma)}{\longrightarrow}
    & 
    Hom(U,\mathbf{\Omega}^n)
  }
$$

(here we write $Hom(-,-) \coloneqq Hom_{SmoothSet}(-,-)$ for the [[hom functor]] of [[smooth sets]]).

=--

+-- {: .num_prop }
###### Proposition
**(relative transgression over [[manifolds with boundary]])**

1. $X$ be a [[smooth set]];

1. $\Sigma_k$ be a [[compact topological space|compact]] [[smooth manifold]] of [[dimension]] $k$ with [[manifold with boundary|boundary]] $\partial \Sigma$

1. $n \geq k \in \mathbb{N}$;

1. $\omega \in \Omega^n_{X}$ a [[closed differential form]].

Write

$$ 
  (-)\vert_{\partial \Sigma}
    \;\coloneqq\;
  [\partial \Sigma \hookrightarrow \Sigma, X]
  \;\colon\;
  [\Sigma, X]
   \longrightarrow
  [\partial \Sigma, X]
$$

for the smooth function that restricts smooth functions on $\Sigma$ to smooth functions on the [[boundary]] $\partial \Sigma$.

Then the operations of transgression of differential forms (def. \ref{TransgressionOfDifferentialFormsToMappingSpaces}) to $\Sigma$ and to $\partial \Sigma$, respectively, are related by


$$
  d \left(
    \tau_{\Sigma}(\omega)
  \right)
  = 
  (-1)^{k+1}
  ((-)\vert_{\partial \Sigma})^\ast \tau_{\partial \Sigma}(\omega)
    \phantom{AAAAAAAA}
  \array{
    [\Sigma, X] 
      &\overset{ \tau_{\Sigma}(\omega) }{\longrightarrow}&
    \mathbf{\Omega}^{n-k}
    \\
    {}^{\mathllap{(-)\vert_{\partial \Sigma} }}\downarrow
      &&
    \downarrow^{\mathrlap{ (-1)^{k+1} d}}
    \\
    [\partial \Sigma, X]
      &\underset{ \tau_{\partial\Sigma}(\omega) }{\longrightarrow}&
    \mathbf{\Omega}^{n-k+1}
  }
  \,.
$$

In particular this means that if the compact manifold $\Sigma$ happens to have no boundary (is a [[closed manifold]]) then transgression over $\Sigma$ takes closed differential forms to closed differential forms.


=--

+-- {: .proof}
###### Proof

Let $\phi_{(-)}(-) \colon U \times \Sigma \to X$ be a plot of the mapping space $[\Sigma, X]$. Notice that the [[de Rham differential]] on the [[Cartesian product]] $U \times \Sigma$ decomposes as

$$
  d = d_U + d_\Sigma
  \,.
$$

Now we compute as follows:


$$
  \begin{aligned}
    d \tau_{\Sigma}\omega\vert_{\phi_(-)}
    & =
    d_U \int_\Sigma (\phi_{(-)}(-))^\ast \omega
    \\
    & =
    (-1)^k \int_\Sigma d_U (\phi_{(-)}(-))^\ast \omega
    \\
    & =
    (-1)^k \int_\Sigma (d - d \Sigma) (\phi_{(-)}(-))^\ast \omega
    \\
    & =
    (-1)^k \int_\Sigma d (\phi_{(-)}(-))^\ast \omega
    -
    (-1)^k \int_\Sigma d_\Sigma (\phi_{(-)}(-))^\ast \omega
    \\
    & =
    (-1)^k \int_\Sigma (\phi_{(-)}(-))^\ast \underset{= 0}{\underbrace{d \omega}}
    -
    (-1)^k \int_\Sigma d_\Sigma (\phi_{(-)}(-))^\ast \omega
    \\
    & =
    -
    (-1)^k \int_\Sigma d_\Sigma (\phi_{(-)}(-))^\ast \omega
    \\
    & =
    -(-1)^k \int_{\partial \Sigma} (\phi_{(-)}(-))^\ast \omega   
    \\
    & = 
    -(-1)^k \tau_{\partial \Sigma} \omega \vert_{\phi_{(-)}}
  \end{aligned}
$$

where in the second but last step we used [[Stokes' theorem]].

=--




(...)


(...)





[[!redirects geometry of physics -- smooth spaces]] 
