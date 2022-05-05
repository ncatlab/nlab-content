

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

> previous chapters: _[[ geometry of physics -- coordinate systems|coordinate systems]]_, _[[geometry of physics -- categories and toposes|categories and toposes]]_

> next chapters: _[[geometry of physics -- differential forms|differential forms]]_, _[[geometry of physics -- differentiation|differentiation]]_, _[[geometry of physics -- smooth homotopy types|smooth homotopy types]]_


$\,$

$\,$

This chapter introduces a generalized kind of [[sets]] equipped with [[smooth structure]], to be called _[[smooth sets]]_ or _smooth [[homotopy 0-types|0-types]]_.

The definition (Def. \ref{SmoothSpace} below) subsumes that of [[smooth manifolds]], [[Fréchet manifolds]] and [[diffeological spaces]] but is both simpler and more powerful: smooth sets are simply [[sheaves]] on the [[gros site]] of [[Cartesian Spaces]] spring and as such form a nice [[category]] -- a [[topos]] -- and this contains as [[full subcategories]] the more "tame" objects such as smooth manifolds and diffeological spaces.

In fact smooth sets are an early stage in a long sequence of generalized smooth spaces used in [[higher differential geometry]]:

$\{$[[coordinate systems]]$\}$
 $\hookrightarrow$
$\{$[[smooth manifolds]]$\}$
 $\hookrightarrow$
$\{$[[Hilbert manifolds]]$\}$
 $\hookrightarrow$
$\{$[[Banach manifolds]]$\}$
 $\hookrightarrow$
$\{$[[Fréchet manifolds]]$\}$
 $\hookrightarrow$
$\{$[[diffeological spaces]]$\}$
 $\hookrightarrow$
$\{$[[smooth sets]]$\}$
 $\hookrightarrow$
$\{$[[orbifold|smooth orbifolds]]$\}$
 $\hookrightarrow$
$\{$[[smooth groupoids]]$\}$
 $\hookrightarrow $
$\{$[[smooth 2-groupoids]]$\}$
 $\hookrightarrow
 \cdots
 \hookrightarrow $
$\{$[[smooth ∞-groupoids]]$\}$



+-- {: .num_remark}
###### Remark
**Note on terminology.**

In view of the _[[smooth homotopy types]]_ to be discussed in _[[geometry of physics -- smooth homotopy types]]_, the structures discussed now are properly called _smooth [[0-types]]_ or maybe _smooth [[h-sets]]_ or just _smooth sets_. While this subsumes [[smooth manifolds]] which are indeed sets equipped with (particularly nice) [[smooth structure]], it is common in practice to speak of manifolds as "spaces" (indeed as [[topological spaces]] equipped with smooth structure). Historically the _[[Cartesian space]]_ and _[[Euclidean space]]_ of [[Newtonian physics]] are the archetypical examples of smooth manifolds and modern [[differential geometry]] developed very much via motivation by the study of the _spaces_ in [[general relativity]], namely _[[spacetimes]]_. Unfortunately, in a parallel development the word "space" has evolved in [[homotopy theory]] to mean (just) the [[homotopy types]] _represented_ by an actual [[topological space]] (their [[fundamental infinity-groupoids]]). Ironically, with this meaning of the word "space" the original [[Euclidean spaces]] become equivalent to the point, signifying that the modern meaning of "space" in [[homotopy theory]] is quite orthogonal to the original meaning, and that in homotopy theory therefore one should better stick to "[[homotopy types]]".

Since historically grown terminology will never be fully logically consistent, and since often the less well motivated terminology is more widely understood, we will follow tradition here and take the liberty to use "smooth sets" and "smooth spaces" synonymously, the former when we feel more formalistic, the latter when we feel more relaxed.

=--



#Contents#
* table of contents
{:toc}




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

1. the [[Yoneda lemma]] says that this is consistent in that coordinate systems themselves as well as [[smooth manifolds]] may naturally be regarded as generalized smooth sets themselves and that under this identification "laying out a coordinate system" in a smooth set means having a map of smooth sets from the coordinate system to the smooth set.


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

We introduce and discuss this example in detail in the chapter _[[geometry of physics -- differential forms]]_.

=--


A [[smooth set]] (def. \ref{SmoothSpace}) need not have an _underlying set_, for instance 
the smooth set $\mathbf{\Omega}^k$ from example \ref{SmoothSetOfDifferentialForms} for $k \geq 1$
has only a single plot from the point (corresponding to the zero differential form on the point), and yet it is
far from being the point. If a smooth set does have an underlying set, then it is called a 
_[[diffeological space]]_:

+-- {: .num_example }
###### Example
**([[diffeological spaces]])**

A [[smooth set]] $X$ (def. \ref{SmoothSpace}) is called a _[[concrete sheaf|concrete]] smooth set_ or 
a _[[diffeological space]]_ if there exists

1. a [[set]] $X_s \in Set$;

1. for each $n \in \mathbb{N}$ a natural identification of the set of plots $X(\mathbb{R}^n)$
   with a [[subset]] of the set of [[functions]] $\mathbb{R}^n_s \to X_s$ from the underlying set $\mathbb{R}^n_s$ of
   $\mathbb{R}^n$ (forgetting all [[smooth structure]]) to that set $X_s$:
   
   $$
     X(\mathbb{R}^n) \hookrightarrow Hom_{Set}(\mathbb{R}^n_s, X_s)
     \,.
   $$ 

Key examples of diffeological spaces are [[mapping spaces]] between smooth manifolds, which we turn to below
(def. \ref{SmoothFunctionSpace}).

=--

+-- {: .num_example #DiscreteSmoothSpace}
###### Example
**([[discrete object|discrete]] [[smooth set]])

For $S \in $ [[Set]] a set, write

$$
  Disc S \in Smooth0Type
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

Let $X$ and $Y$ be two smooth sets, def. \ref{SmoothSpace}. Then a [[homomorphism]] $f \colon X \to Y$ is

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

Write [[SmoothSet]] or $Smooth0Type$ for the [[category]] ([this def.](geometry+of+physics+--+Categories+and+Toposes#Categories)) whose [[objects]] are [[smooth sets]], def. \ref{SmoothSpace}, and whose [[morphisms]] are homomorphisms of smooth sets according to def. \ref{HomomorphismOfSmoothSpaces}.

=--

At this point it may seem that we have now _two different_ notions for how to lay out a coordinate system in a smooth set $X$: on the hand, $X$ comes by definition with a rule for what the set $X(\mathbb{R}^n)$ of its $\mathbb{R}^n$-plots is. On the other hand, we can now regard the abstract coordinate system $\mathbb{R}^n$ itself as a smooth set, by example \ref{CartesianSpaceAsSmoothSpace}, and then say that an  $\mathbb{R}^n$-plot of $X$ should be a homomorphism of smooth sets of the form $\mathbb{R}^n \to X$.

The following proposition says that these two superficially different notions actually naturally coincide.

+-- {: .num_prop #YonedaForSmoothSpaces}
###### Proposition

Let $X$ be any [[smooth set]], def. \ref{SmoothSpace}, and regard the abstract coordinate system $\mathbb{R}^n$ as a smooth set, by example \ref{CartesianSpaceAsSmoothSpace}. There is a [[natural bijection]]

$$
  X(\mathbb{R}^n) \simeq Hom_{Smooth0Type}(\mathbb{R}^n, X)
$$

between the _postulated_ $\mathbb{R}^n$-plots of $X$ and the _actual_ $\mathbb{R}^n$-plots given by homomorphism of smooth sets $\mathbb{R}^n \to X$.

=--

+-- {: .proof}
###### Proof

This is a special case of the _[[Yoneda lemma]]_, as will be made more explicit below in _[The topos of smooth sets](#ToposOfSmoothSpaces)_.
The reader unfamiliar with this should write out the simple proof explicitly: use the defining [[commuting diagrams]] in def. \ref{HomomorphismOfSmoothSpaces} to deduce that a homomorphism $f : \mathbb{R}^n \to X$ is uniquely fixed by the image of the [[identity]] element in  $\mathbb{R}^n(\mathbb{R}^n) \coloneqq CartSp(\mathbb{R}^n, \mathbb{R}^n)$ under the component function $f_{\mathbb{R}^n} : \mathbb{R}^n(\mathbb{R}^n) \to X(\mathbb{R}^n)$.

=--

+-- {: .num_example #SmoothFunctionOnSmoothSpace}
###### Example

Let $\mathbb{R} \in Smooth0Type$ denote the [[real line]], regarded as a [[smooth set]] by example \ref{CartesianSpaceAsSmoothSpace}. Then for $X \in Smooth0Type$ any smooth set, a homomorphism of smooth sets

$$
  f \colon X \to \mathbb{R}
$$

is a _[[smooth function]] on $X$_. Prop. \ref{YonedaForSmoothSpaces} says here that when $X$ happens to be an abstract coordinate system regarded as a smooth set by def. \ref{CartesianSpaceAsSmoothSpace}, then this general notion of smooth functions between smooth sets reproduces the basic notion of def, \ref{CartesianSpaceAndHomomorphism}.

=--

+-- {: .num_defn #PointsOfASmoothSpace}
###### Definition

The 0-[[dimension|dimensional]] abstract coordinate system $\mathbb{R}^0$ we also call the **[[point]]** and regarded as a smooth set we will often write it as

$$
  * \in Smooth0Type
  \,.
$$

For any $X \in Smooth0Type$, we say that a homomorphism

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

Let $X, Y \in Smooth0Type$ by two smooth sets. Their **[[product]]** is the smooth set $X \times Y \in Smooth0Type$ whose plots are pairs of plots of $X$ and $Y$:

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

Let $* = \mathbb{R}^0$ be the [[point]], regarded as a smooth set, def. \ref{PointsOfASmoothSpace}. Then for $X \in Smooth0Type$ any smooth set the canonical projection homomorphism

$$
  X \times * \to X
$$

is an [[isomorphism]].

=--

+-- {: .num_defn}
###### Definition

Let $f \colon X \to Z$ and $g \colon Y \to Z$ be two [[homomorphisms]] of smooth sets, def. \ref{HomomorphismOfSmoothSpaces}. There is then a new smooth set to be denoted

$$
  X \times_Z Y \in Smooth0Type
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

Let $\Sigma, X \in Smooth0Type$ be two [[smooth sets]], def. \ref{SmoothSpace}. Then the **smooth [[mapping space]]**

$$
  [\Sigma,X] \in Smooth0Type
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

Given a [[smooth set]] $X \in Smooth0Type$, its smooth **[[path space]]** is the smooth mapping space

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


### The smooth moduli space of smooth functions
 {#SmoothModuliSpaceOfSmoothFunctions}


In example \ref{SmoothFunctionOnSmoothSpace} we saw that a smooth function on a general [[smooth set]] $X$ is a homomorphism of smooth sets, def. \ref{HomomorphismOfSmoothSpaces}

$$
  f \colon X \to \mathbb{R}
  \,.
$$

The collection of these forms the [[hom-set]] $Hom_{Smooth0Type}(X, \mathbb{R})$. But by the discussion in _[Smooth mapping spaces](#SmoothMappingSpaces)_ such hom-sets are naturally refined to smooth sets themselves.

+-- {: .num_defn #SmoothSpaceOfSmoothFunctions}
###### Definition

For $X \in Smooth0Type$ a [[smooth set]], we say that the **moduli space of smooth functions** on $X$ is the smooth mapping space (def. \ref{SmoothFunctionSpace}), from $X$ into the standard [[real line]] $\mathbb{R}$

$$
  [X, \mathbb{R}] \in Smooth0Type
  \,.
$$

We will also denote this by

$$
  \mathbf{C}^\infty(X) \coloneqq [X, \mathbb{R}]
  \,,

$$

since in the special case that $X$ is a [[Cartesian space]] this is the smooth refinement of the set $C^\infty(X)$ of [[smooth functions]], def. \ref{SmoothFunctions}, on $X$.

=--

+-- {: .num_remark}
###### Remark

We call this a _[[moduli space]]_ because by prop. \ref{UniversalPropertyOfMappingSpace} above and in the sense of remark \ref{MappingSpaceAsModuliSpace} it is such that smooth functions into it _modulate_ smooth functions $X \to \mathbb{R}$.

By prop. \ref{UnderlyingSetOfSmoothMappingSpace} a point $* \to [X,\mathbb{R}^1]$ of the moduli space is equivalently a smooth function $X \to \mathbb{R}^1$.

=--



### Outlook
 {#SmoothSpacesOutlook}


+-- {: .num_remark}
###### Remark

Later we define/see the following:

* A _[[smooth manifold]]_  is a [[smooth set]] that is [[covering|locally]] _[[equivalence|equivalent]]_ to a [[coordinate system]];

* A _[[diffeological space]]_ is a [[smooth set]] such that every coordinate labels a [[point]] in the space. In other words, a diffeological space is a smooth set that has an underlying set $X_s \in Set$ of points such that the set of $\mathbb{R}^n$-plots is a subset of the set of all functions:

  $$
    X(\mathbb{R}^n) \hookrightarrow Functions(\mathbb{R}^n, S_s)
    \,.
  $$

  (This need not be the case in a general smooth set, important counterexamples are the _universal smooth moduli spaces of differential forms_ in [Smooth moduli space of differential forms](#SmoothUniversalModuliSpaceOfDifferentialForms)).



=--


+-- {: bluebox }
######

This ends the Model-layer discussion of smooth sets. We now pass to a more advanced discussion of this topic in the [Semantics layer below](#SmoothSpacesLayerSem). The reader wishing to stick to more elementary discussion for the time being should skip ahead to the Model-layer discussion of [Differential forms below](#DifferentialForms).

=--

## The topos of smooth sets
 {#SmoothSpacesLayerSem}
 {#ToposOfSmoothSpaces}


In the language of [[geometry of physics -- categories and toposes|categories and toposes]], we may summarize the concept of [[smooth sets]] by saying that they form the _[[sheaf topos]]_ over the _[[site]]_ of [[Cartesian spaces]] (Prop. \ref{SmoothSetsAreSheavesOnCartSp} below).

This perspective allows to see good abstract properties enjoyed by the [[smooth sets]]. The key such property is that the [[topos]] which they form is a _[[cohesive topos]]_ (Def. \ref{CohesiveTopos} below). We prove this below in Example \ref{SmoothSetsFormACohesiveTopos}, and then discuss applications.

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

$\,$




$\,$

### Cohesion on smooth sets
  {#CohesionOnSmoothSets}

+-- {: .num_example #SmoothSetsFormACohesiveTopos}
###### Example
**([[smooth sets]] form a [[cohesive topos]])**

The [[category]] $SmoothSet$ of [[smooth sets]] (Def. \ref{CategoryOfSmoothSets}) is a [[cohesive topos]] (Def. \ref{CohesiveTopos})

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


=--

+-- {: .proof}
###### Proof

First of all, by Prop. \ref{SmoothSetsAreSheavesOnCartSp}, smooth sets indeed form a [[sheaf topos]], over the [[site]] [[CartSp]]

$$
  SmoothSet \simeq Sh(CartSp)
  \,.
$$

Hence, by Prop. \ref{CategoriesOfSheavesOnCohesiveSiteIsCohesive}, it is now sufficient to see that [[CartSp]] is a [[cohesive site]] (Def. \ref{OneCohesiveSite}).

It clearly has [[finite products]]: The [[terminal object]] is the [[point]], given by the 0-[[dimension|dimensional]] [[Cartesian space]]

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

This establishes the first clause in Def. \ref{OneCohesiveSite}. 

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



=--




(...)


(...)




[[!redirects geometry of physics -- smooth spaces]] 
