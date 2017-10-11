
> This entry contains one chapter of the material at _[[geometry of physics]]_.

> previous chapter: _[[ geometry of physics -- coordinate systems|coordinate systems]]_

> next chapters: _[[geometry of physics -- differential forms|differential forms]]_, _[[geometry of physics -- differentiation|differentiation]]_, _[[geometry of physics -- smooth homotopy types|smooth homotopy types]]_

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

#Contents#
* table of contents
{:toc}


## Idea

This chapter introduces a generalized kind of [[sets]] equipped with [[smooth structure]], to be called _smooth sets_ or _smooth spaces_ or _smooth 0-types_. 

The definition subsumes that of [[smooth manifolds]], [[Fréchet manifolds]] and [[diffeological spaces]] but is both simpler and more powerful: smooth sets are simply [[sheaves]] on the [[gros site]] of [[Cartesian Spaces]] and as such form a nice [[category]] -- a [[topos]] -- and this contains as [[full subcategories]] the more "tame" objects such as smooth manifolds and diffeological spaces.

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
$\{$[[smooth spaces]]$\}$ 
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

## **Smooth sets**
 {#SmoothSpaces}

In the section _[Coordinate systems](#CoordinateSystems)_ we have set up the archetypical [[spaces]] of [[differential geometry]]. Here we now define in terms of these the most general _[[smooth spaces]]_ that differential geometry can deal with. We also discuss basic properties of these smooth spaces, all in the [Mod Layer](#SmoothSpacesLayerMod).

In the [Sem Layer](SmoothSpacesLayerSem) we discuss smooth spaces as a _[[topos]]_ and in fact as a _[[cohesive topos]]_. This is essentially the stage on which all of the fellowing developments take place. Or rather, the refinement of this to a _[[(infinity,1)-topos|higher topos]]_ is, which we discuss further below in the chapter _[Smooth ∞-Groupoids](#SmoothnGroupoids)_.


### Model Layer
 {#SmoothSpacesLayerMod}

In this [Model Layer](#LayerMod) we discuss concretely the definition of [[smooth sets]] and of  [[homomorphisms]] between them,  together with basic examples and properties.

#### Plots of smooth spaces and their gluing
 {#PlotsOfSmoothSpacesAndTheirGluing}

The general kind of "[[smooth space]]" that we want to consider is a [[type|something]] that can be _probed_ by laying out coordinate systems as in [this definition](geometry+of+physics+--+coordinate+systems#CartesianSpaces)  inside it, and that can be obtained by _gluing_ all the possible coordinate systems in it together. 

At this point we want to impose no further conditions on a "space" than this. In particular we do not assume that we know beforehand a [[set]] of [[points]] underlying $X$. Instead, we define smooth spaces $X$ entirely _operationally_ as something about which we can ask "Which ways are there to lay out $\mathbb{R}^n$ inside $X$?" and such that there is a self-consistent answer to this question. The following definitions make precise what we mean by this. The reader wishing to see more motivational discussion first might look at _[[motivation for sheaves, cohomology and higher stacks|conceptual exposition]]_.


The idea of the following definitions may be summarized like this:

1. a generalized _smooth space_ is something that may be probed by laying out coordinate systems into it, in a way that respects transformation of coordinate patches and gluing of coordinate patches;

1. the [[Yoneda lemma]] says that this is consistent in that coordinate systems themselves as well as [[smooth manifolds]] may naturally be regarded as generalized smooth spaces themselves and that under this identification "laying out a coordinate system" in a smooth space means having a map of smooth spaces from the coordinate system to the smooth space.

+-- {: .num_defn }
###### Definition (terminology)
**(plots)**

For brevity we will refer to "a way to lay out a coordinate system in $X$" as a _plot_ of $X$. 

=--


The first set of consistency conditions on plots of a space is that they respect _coordinate transformations_. This is what the following definition formalises.

+-- {: .num_defn #SmoothPreSpace}
###### Definition

A **smooth pre-space $X$ is 

1. a collection of sets: for each [[Cartesian space]] $\mathbb{R}^n$ (hence for each [[natural number]] $n$) a [[set]] 

   $$
     X(\mathbb{R}^n) \in Set
   $$  

   -- to be thought of as the _set of ways of laying out $\mathbb{R}^n$ inside $X$_;

1. for each abstract coordinate transformation, hence for each [[smooth function]] $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ a [[function]] between the corresponding sets

   $$
     X(f) : X(\mathbb{R}^{n_2}) \to X(\mathbb{R}^{n_1})
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

+-- {: .num_defn #MatchingFamiliesOfPlots}
###### Definition

Let $X$ be a smooth pre-space, def. \ref{SmoothPreSpace}.
For $\{U_i \to \mathbb{R}^n\}_{i \in I}$ a differentially [[good open cover]], def. \ref{DifferentiallyGoodOpenCover}, let 

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

In def. \ref{MatchingFamiliesOfPlots} the [[equation]]

$$ 
  X(\iota_i)(p_i) = X(\iota_j)(p_j)
$$

says in words:

> The plot $p_i$ of $X$ by the coordinate system $U_i$ inside the bigger coordinate system $\mathbb{R}^n$ coincides with the plot $p_j$ of $X$ by the other coordinate system $U_j$ inside $X$ when both are restricted to the [[intersection]] $U_i \cap U_j$ of $U_i$ with $U_j$ inside $\mathbb{R}^n$.

=--

+-- {: .num_remark #NaiveDescentMorphism}
###### Remark

For each differentially good open cover $\{U_i \to \mathbb{R}^n\}_{i \in I}$ and each smooth pre-space $X$, def. \ref{SmoothPreSpace}, there is a canonical [[function]]

$$
  X(\mathbb{R}^n) \to GluedPlots(\{U_i \to \mathbb{R}^n\}, X)
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

A smooth pre-space $X$, def. \ref{SmoothPreSpace} is a **[[smooth space]]** if for all differentially good open covers $\{U_i \to \mathbb{R}^n\}$, def. \ref{DifferentiallyGoodOpenCover}, the canonical function of remark \ref{NaiveDescentMorphism} from plots to glued plots is a [[bijection]]

$$
  X(\mathbb{R}^n) \stackrel{\simeq}{\to} GluedPlots(\{U_i \to \mathbb{R}^n\}, X)
  \,.
$$

=--

+-- {: .num_remark #OnTheNotionOfSmoothSpaces}
###### Remark

We may think of a [[smooth space]] as being a kind of [[space]] whose _local models_ (in the general sense discussed at _[[geometry]]_) are [[Cartesian spaces]]: 

while definition \ref{SmoothSpace} explicitly says that a smooth space is something that is _consistently probeable_ by such local models; by a [[category theory|general abstract]] fact -- which we discuss in more detail below in _[Smooth Spaces - Semantic Layer](#SmoothSpacesLayerSem)_  -- that is sometimes called the [[co-Yoneda lemma]] it follows in fact that smooth spaces are precisely the objects that are obtained by 
_gluing coordinate systems_ together.

For instance we will see that two open 2-balls $\mathbb{R}^2 \simeq D^2$ along a common rim yields the smooth space version of the [[sphere]] $S^2$, a basic example of a [[smooth manifold]]. But before we examine such explicit constructions, we discuss here for the moment more general properties of smooth spaces. The reader instead wishing to see more of these concrete examples at this point should jump ahead to _[Smooth Spaces - Outlook](#SmoothSpacesOutlook)_.

=--

But the following most basic example we consider right now:

+-- {: .num_example #CartesianSpaceAsSmoothSpace}
###### Example

For $n \in \mathbb{R}^n$, there is a [[smooth space]], def. \ref{SmoothSpace}, whose set of plots over the abstract coordinate systems $\mathbb{R}^k$ is the set

$$
  CartSp(\mathbb{R}^k, \mathbb{R}^n) \in Set
$$ 

of [[smooth functions]] from $\mathbb{R}^k$ to $\mathbb{R}^n$.

Clearly this is the rule for plots that characterize $\mathbb{R}^n$ itself as a smooth space, and so we will just denote this smooth space by the same symbols "$\mathbb{R}^n$":

$$
  \mathbb{R}^n \colon \mathbb{R}^k \mapsto CartSp(\mathbb{R}^k, \mathbb{R}^n)
  \,.
$$

In particular the [[real line]] $\mathbb{R}$ is this way itself a [[smooth space]].

=--


In a moment we find a formal justification for this slight abuse of notation.

Another basic class of examples of smooth spaces are the [[discrete space|discrete]] smooth spaces:

+-- {: .num_defn #DiscreteSmoothSpace}
###### Definition

For $S \in $ [[Set]] a set, write

$$
  Disc S \in Smooth0Type
$$

for the smooth space whose set of $U$-plots for every $U \in CartSp$ is always $S$.

$$
  Disc S \colon U \mapsto S
$$


and which sends every coordinate transformation $f \colon \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ to the identity function on $S$.

A smooth space of this form we call a **[[discrete object|discrete smooth space]]**.

=--



More examples of smooth spaces can be built notably by [[intersection|intersecting]] [[images]] of two smooth spaces inside a bigger one. In order to say this we first need a formalization of [[homomorphism]] of smooth spaces. This we turn to now.


#### Homomorphisms of smooth spaces
 {#HomomorphismsOfSmoothSpaces}

We discuss "functions" or "maps" between [[smooth spaces]], def. \ref{SmoothSpace}, which preserve the smooth space [[structure]] in a suitable sense. As with any notion of function that preserves structure, we refer to them as _[[homomorphisms]]_.

The idea of the following definition is to say that whatever a [[homomorphism]] $f : X \to Y$ between two smooth spaces is, it has to take the plots of $X$ by $\mathbb{R}^n$ to a corresponding plot of $Y$, such that this respects coordinate transformations.

+-- {: .num_defn #HomomorphismOfSmoothSpaces}
###### Definition

Let $X$ and $Y$ be two smooth spaces, def. \ref{SmoothSpace}. Then a [[homomorphism]] $f \colon X \to Y$ is

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

For $f_1 : X \to Y$ and $f_2 : X \to Y$ two homomorphisms of smooth spaces, their [[composition]] $f_2 \circ f_1 \colon X \to Y$ is defined to be the homomorphism whose component over $\mathbb{R}^n$ is the composite of functions of the components of $f_1$ and $f_2$:

$$
  (f_2\circ f_1)_{\mathbb{R}^n} \coloneqq {f_2}_{\mathbb{R}^n} \circ {f_1}_{\mathbb{R}^n}
  \,.
$$


=--

+-- {: .num_defn}
###### Definition

Write $Smooth0Type$ for the [[category]] whose [[objects]] are [[smooth spaces]], def. \ref{SmoothSpace}, and whose [[morphisms]] are homomorphisms of smooth spaces, def. \ref{HomomorphismOfSmoothSpaces}.

=--

At this point it may seem that we have now _two different_ notions for how to lay out a coordinate system in a smooth space $X$: on the hand, $X$ comes by definition with a rule for what the set $X(\mathbb{R}^n)$ of its $\mathbb{R}^n$-plots is. On the other hand, we can now regard the abstract coordinate system $\mathbb{R}^n$ itself as a smooth space, by example \ref{CartesianSpaceAsSmoothSpace}, and then say that an  $\mathbb{R}^n$-plot of $X$ should be a homomorphism of smooth spaces of the form $\mathbb{R}^n \to X$.

The following proposition says that these two superficially different notions actually naturally coincide. 

+-- {: .num_prop #YonedaForSmoothSpaces}
###### Proposition

Let $X$ be any [[smooth space]], def. \ref{SmoothSpace}, and regard the abstract coordinate system $\mathbb{R}^n$ as a smooth space, by example \ref{CartesianSpaceAsSmoothSpace}. There is a [[natural bijection]]

$$
  X(\mathbb{R}^n) \simeq Hom_{Smooth0Type}(\mathbb{R}^n, X)
$$

between the _postulated_ $\mathbb{R}^n$-plots of $X$ and the _actual_ $\mathbb{R}^n$-plots given by homomorphism of smooth spaces $\mathbb{R}^n \to X$.

=--

+-- {: .proof}
###### Proof

This is a special case of the _[[Yoneda lemma]]_, as will be made more explicit below in _[The topos of smooth spaces](#ToposOfSmoothSpaces)_. 
The reader unfamiliar with this should write out the simple proof explicitly: use the defining [[commuting diagrams]] in def. \ref{HomomorphismOfSmoothSpaces} to deduce that a homomorphism $f : \mathbb{R}^n \to X$ is uniquely fixed by the image of the [[identity]] element in  $\mathbb{R}^n(\mathbb{R}^n) \coloneqq CartSp(\mathbb{R}^n, \mathbb{R}^n)$ under the component function $f_{\mathbb{R}^n} : \mathbb{R}^n(\mathbb{R}^n) \to X(\mathbb{R}^n)$.

=--

+-- {: .num_example #SmoothFunctionOnSmoothSpace}
###### Example

Let $\mathbb{R} \in Smooth0Type$ denote the [[real line]], regarded as a [[smooth space]] by def. \ref{CartesianSpaceAsSmoothSpace}. Then for $X \in Smooth0Type$ any smooth space, a homomorphism of smooth spaces

$$
  f \colon X \to \mathbb{R}
$$

is a _[[smooth function]] on $X$_. Prop. \ref{YonedaForSmoothSpaces} says here that when $X$ happens to be an abstract coordinate system regarded as a smooth space by def. \ref{CartesianSpaceAsSmoothSpace}, then this general notion of smooth functions between smooth spaces reproduces the basic notion of def, \ref{CartesianSpaceAndHomomorphism}.

=--

+-- {: .num_defn #PointsOfASmoothSpace}
###### Definition

The 0-[[dimension|dimensional]] abstract coordinate system $\mathbb{R}^0$ we also call the **[[point]]** and regarded as a smooth space we will often write it as

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

By prop. \ref{YonedaForSmoothSpaces} the points of a smooth space $X$ are naturally identified with its 0-dimensional plots, hence with the "ways of laying out a 0-dimensional coordinate system" in $X$:

$$
  Hom(*, X) \simeq X(\mathbb{R}^0)
  \,.
$$

=--


#### Products and fiber products of smooth spaces
 {#ProductsAndFiberProductsOfSmoothSpaces}

+-- {: .num_defn #ProductOfSmoothSpaces}
###### Definition

Let $X, Y \in Smooth0Type$ by two smooth spaces. Their **[[product]]** is the smooth space $X \times Y \in Smooth0Type$ whose plots are pairs of plots of $X$ and $Y$:

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

Let $* = \mathbb{R}^0$ be the [[point]], regarded as a smooth space, def. \ref{PointsOfASmoothSpace}. Then for $X \in Smooth0Type$ any smooth space the canonical projection homomorphism

$$
  X \times * \to X
$$

is an [[isomorphism]].

=--

+-- {: .num_defn}
###### Definition

Let $f \colon X \to Z$ and $g \colon Y \to Z$ be two [[homomorphisms]] of smooth spaces, def. \ref{HomomorphismOfSmoothSpaces}. There is then a new smooth space to be denoted 

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



#### Smooth mapping spaces and smooth moduli spaces
 {#SmoothMappingSpaces}


+-- {: .num_defn #SmoothFunctionSpace}
###### Definition

Let $\Sigma, X \in Smooth0Type$ be two [[smooth spaces]], def. \ref{SmoothSpace}. Then the **smooth [[mapping space]]** 

$$
  [\Sigma,X] \in Smooth0Type
$$ 

is the [[smooth space]] defined by saying that its set of $\mathbb{R}^n$-plots is

$$
  [\Sigma, X](\mathbb{R}^n)
   \coloneqq
  Hom(\Sigma \times \mathbb{R}^n, X)
  \,.
$$

=--

Here in $\Sigma \times \mathbb{R}^n$ we first regard the abstract coordinate system $\mathbb{R}^n$ as a smooth space by example \ref{CartesianSpaceAsSmoothSpace} and then we form the [[product]] smooth space by def. \ref{ProductOfSmoothSpaces}.

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

for every smooth space $K$.

=--

+-- {: .proof}
###### Proof

With a bit of work this is straightforward to check explicitly by unwinding the definitions. It follows however from [[category theory|general abstract]] results once we realize that $[-,-]$ is of course the _[[internal hom]]_ of smooth spaces. This we come to below in _[Smooth spaces - Semantic Layer](#SmoothSpacesLayerSem)_.

=--


+-- {: .num_remark #MappingSpaceAsModuliSpace}
###### Remark

This says in words that a smooth function from any $K$ into the mapping space $[\Sigma,X]$ is equivalently a smooth function from $K \times \Sigma$ to $X$. The latter we may regard as a _$K$-parameterized smooth family_ of smooth functions $\Sigma \to X$. Therefore in view of the previous remark \ref{NatureOfPlotsOfMappingSpace} this says that smooth mapping spaces have a [[universal property]] not just over abstract coordinate systems, but over all smooth spaces.

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

Given a [[smooth space]] $X \in Smooth0Type$, its smooth **[[path space]]** is the smooth mapping space

$$
  \mathbf{P}X \coloneqq [\mathbb{R}^1, X]
  \,.
$$ 

By prop. \ref{UnderlyingSetOfSmoothMappingSpace} the points of $P X$ are indeed precisely the smooth trajectories $\mathbb{R}^1 \to X$. But $P X$ also knows how to _smoothly vary_ such smooth trajectories. 

This is central for [[variational calculus]] which determines [[equations of motion]] in [[physics]]. This we turn to below in _[Variational calculus](#VariationalCalculus)_.

=--

+-- {: .num_remark}
###### Remark

In [[physics]], if $X$ is a model for [[spacetime]], then $P X$ may notably be interpreted as the smooth space of [[worldlines]] _in_ $X$, hence the smooth space of paths or _trajectories_ of a [[particle]] in $X$. 

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


#### The smooth moduli space of smooth functions
 {#SmoothModuliSpaceOfSmoothFunctions}


In example \ref{SmoothFunctionOnSmoothSpace} we saw that a smooth function on a general [[smooth space]] $X$ is a homomorphism of smooth spaces, def. \ref{HomomorphismOfSmoothSpaces}

$$
  f \colon X \to \mathbb{R}
  \,.
$$

The collection of these forms the [[hom-set]] $Hom_{Smooth0Type}(X, \mathbb{R})$. But by the discussion in _[Smooth mapping spaces](#SmoothMappingSpaces)_ such hom-sets are naturally refined to smooth spaces themselves.

+-- {: .num_defn #SmoothSpaceOfSmoothFunctions}
###### Definition

For $X \in Smooth0Type$ a [[smooth space]], we say that the **moduli space of smooth functions** on $X$ is the smooth mapping space (def. \ref{SmoothFunctionSpace}), from $X$ into the standard [[real line]] $\mathbb{R}$

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



#### Outlook
 {#SmoothSpacesOutlook}


+-- {: .num_remark}
###### Remark

Later we define/see the following:

* A _[[smooth manifold]]_  is a [[smooth space]] that is [[covering|locally]] _[[equivalence|equivalent]]_ to a [[coordinate system]];

* A _[[diffeological space]]_ is a [[smooth space]] such that every coordinate labels a [[point]] in the space. In other words, a diffeological space is a smooth space that has an underlying set $X_s \in Set$ of points such that the set of $\mathbb{R}^n$-plots is a subset of the set of all functions:

  $$
    X(\mathbb{R}^n) \hookrightarrow Functions(\mathbb{R}^n, S_s)
    \,.
  $$

  (This need not be the case in a general smooth space, important counterexamples are the _universal smooth moduli spaces of differential forms_ in [Smooth moduli space of differential forms](#SmoothUniversalModuliSpaceOfDifferentialForms)).

 

=--


+-- {: bluebox }
###### 

This ends the Model-layer discussion of smooth spaces. We now pass to a more advanced discussion of this topic in the [Semantics layer below](#SmoothSpacesLayerSem). The reader wishing to stick to more elementary discussion for the time being should skip ahead to the Model-layer discussion of [Differential forms below](#DifferentialForms). 

=--

### Semantic Layer
 {#SmoothSpacesLayerSem}

In this [Semantic Layer]{#LayerSem} we mention some basic definitions of [[topos theory]] and discuss the [[topos]] formed by the [[smooth spaces]] defined in [Smooth Spaces - Mayer Mod](#SmoothSpacesLayerMod).

#### Toposes
 {#Toposes}


+-- {: .num_defn #SheafToposAsSubtopos}
###### Definition

A [[sheaf topos]] is [[subtopos]] of [[presheaf topos]]

$$
  Sh(C) 
    \stackrel{\overset{\overline{(-)}}{\leftarrow}}{\hookrightarrow}
  PSh(C)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Here the [[left adjoint]] $\overline{(-)}$, which is equivalently

* the [[inverse image]] of the [[geometric embedding]] [[geometric morphism]]

* the [[sheafification]] functor

is precisely such that for every [[covering]] $\{U_i \to U\}_{i \in I}$ in the [[site]] $C$ the [[sieve]] inclusion 

$$
  S(\{U_i\}) \hookrightarrow U \;\;\;\; \in PSh(C)
$$

(a [[dense monomorphism]]) is sent to an [[isomorphism]].

Hence the sheaf topos is the left exact [[localization]] at the covering sieve inclusions.

=--

+-- {: .num_remark}
###### Remark

The [[presheaf topos]] $PSh(C)$ is the [[free cocompletion]] of the [[category]] $C$, hence the category obtained from $C$ by [[free construction|freely]] forming [[colimits]] of its objects.

In contrast, the [[localization]] $Sh(C) \hookrightarrow PSh(C)$ enforces _relations_ between these free colimits.

Therefore in total we may think of $Sh(C)$ as obtained by [[generators and relations]] from the [[site]] $C$: 

* the objects of $C$ are the generators;

* the [[coverings]] of $C$ are the relations.

=--

Def. \ref{SheafToposAsSubtopos} is the "external" characterization of sheaf toposes. 

More intrinsically we have _[[Giraud's theorem]]_:

+-- {: .num_theorem}
###### Theorem

A [[sheaf topos]] is equivalently a [[presentable category]] with

1. [[universal colimits]]

1. [[effective quotients]]

1. [[disjoint coproducts]]

=--

This characterization, or rather its refinement to [[(infinity,1)-categories of (infinity,1)-sheaves]], is crucial, below, for the discussion of [[principal bundles]] and their [[associated bundle|associated]] [[fiber bundles]]. 

For other general considerations we need rather that every [[sheaf topos]] is in particular an _[[elementary topos]]_

+-- {: .num_defn}
###### Definition

An [[elementary topos]] is 

* a [[locally cartesian closed category]] 

* with a [[subobject classifier]].

=--

The first of these says that the [[internal language]] is [[dependent type theory]] with [[dependent sum types]] and [[dependent product types]], the second says that its has a [[type of propositions]]. This we turn to in [Smooth Spaces - Syntactic Layer](#SmoothSpacesLayerSyn) below.

#### Subobjects
 {#Subobjects}

* [[subobject]], [[subobject classifier]]

* [[truncated object in an (infinity,1)-topos|(-1)-truncation]]

#### Slice toposes
 {#SliceToposes}

* [[slice topos]]

* [[etale geometric morphism]]

#### Local, connected and cohesive toposes

* [[local topos]]

  * [[concrete object]]

* [[locally connected topos]], [[connected topos]]

  * [[connected object]]

* [[cohesive topos]]


#### The topos of smooth spaces
 {#ToposOfSmoothSpaces}

+-- {: .num_remark}
###### Remark

* A _smooth pre-space_, def. \ref{SmoothPreSpace} is equivalently a [[presheaf]] on [[CartSp]], hence a [[functor]] $X : CartSp^{op} \to Set$;

* a _[[smooth space]]_, def. \ref{SmoothSpace}, is equivalently a presheaf on [[CartSp]] which is a [[sheaf]] with respect to the differentially [[good open cover]]-[[coverage]]:

  * the set of "glued plots", def. \ref{MatchingFamiliesOfPlots} is the [[descent object]];

  * the canonical morphism of remark \ref{NaiveDescentMorphism} is the [[descent morphism]];

  * the condition that it be an isomorphism (for each differentially good open cover) is the [[descent]]- or [[sheaf]] condition.

=--


The [[sheaf topos]], def. \ref{SheafToposAsSubtopos}, of [[smooth spaces]] enjoys a few crucial properties: it is

* a [[locally connected topos|locally connected]] and [[connected topos]]

* a [[local topos]]

* a [[cohesive topos]]. This we discuss in the remainder of this [Semantic Layer](#LayerSem).


##### Connectedness 
 {#ConnectedSmooth0Type}

The full [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is a [[locally connected topos]] in that the terminal [[global section]] [[geometric morphism]] to [[Set]] is an [[essential geometric morphism]]:

$$
  Sh(CartSp)
  \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{L Const}{\leftarrow}}{\underset{\Gamma}{\to}}}
  Set
$$

The extra [[left adjoint]] $\Pi_0 : Sh(CartSp) \to Set$ sends diffeological spaces to the set of path-[[connected]] components of their underlying [[topological space]]s.


+-- {: .num_prop}
###### Proposition

The [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is a [[locally connected topos]].

=--

+-- {: .proof}
###### Proof

The following argument works for every [[site]] $C$ which is such that constant presheaves on $C$ are already sheaves.

Notice that this is the case for $C = CartSp$ because every Cartesian space is connected: for $S \in Set$ a compatible family of elements of $Const S$ on a cover $\{U_i \to \mathbb{R}^n\}$ of some $\mathbb{R}^n$ is an element of $S$ on each patch, such that their restriction maps to intersections of patches coincide. But the restriction maps are all identities, so this says that all these elements coincide. Therefore the set of compatible families is just the set $S$ itself, hence the presheaf $Const S$ is a sheaf.

So with $L : PSh(C) \to Sh(C)$ the [[sheafification]] functor we have that $L Const S \simeq Const S$.

Whenever this is the case the [[left adjoint]] to the constant presheaf functor, which always exists for presheaves and is given by the [[colimit]] functor, is also left adjoint on the level of sheaves, because for each $X \in Sh(C)$ and $S \in Set$ we have natural bijections

$$
  \begin{aligned}
    Hom_{Sh(C)}(X, L Const S)
    & =
    Hom_{PSh(C)}(X, L Const S)
    \\
    & \simeq
    Hom_{PSh(C)}(X, Const S)
    \\
    & \simeq
    Hom_{Set}(\lim_\to X, S)
  \end{aligned}
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

Write $\Pi_0 := \lim_\to : Sh(CartSp) \to Set$
for the [[left adjoint]] to $LConst : Set \stackrel{Const}{\to} PSh(C) \stackrel{L}{\to} Sh(C)$.

=--

+-- {: .num_prop}
###### Proposition

For $X \in Sh(C)$ a diffeological space, $\Pi_0(X)$ is the set of path-connected components of the topological space underlying $X$.

=--

+-- {: .proof}
###### Proof

By the [[co-Yoneda lemma]] we may write 

$$
  X = {\lim_\to}_{(U \to X) \in y/X} U
$$

and since $\Pi_0$ commutes with colimits we have

$$
  \Pi_0(X) \simeq 
  \Pi_0 {\lim_\to}_{(U \to X)} U
  \simeq
  {\lim_\to}_{(U \to X)} \Pi_0(U)
  \,.
$$

But also by the co-Yoneda lemma we have that the [[colimit]] over any [[representable functor|representable]] is the singleton set, hence our expression

$$
  \cdots \simeq 
  {\lim_\to}_{(U \to X)} *
$$

is the colimit over the category of plots of $X$ of the functor that is constant on the point. This colimit is the [[coproduct]] of points over the connected components of the [[diagram]] category.

The connected components of the category of plots $y/X$ are the path-connected (or "plot-connected") components of the underlying topological space of $X$.



=--


+-- {: .num_prop}
###### Proposition

The [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is actually a [[connected topos]].

=--

+-- {: .proof}
###### Proof

Since $CartSp$ is a [[connected category]] it is immediate that $Const \colon Set \to PSh(CartSp)$ is a [[full and faithful functor]]. By the above this equals $L Const$, which is hence also full and faithful.

By the discussion at [[connected topos]] we could equivalently convince ourselves that $\Pi_0$ preserves the terminal object. The terminal object of $Sh(CartSp)$ is $y(\mathbb{R}^0)$, hence representable. By the above, $\Pi_0$ sends all representable objects to the singleton set, which is the terminal object of $Set$. 

=--

##### Locality 
 {#LocalSmooth0Type}


+-- {: .num_prop}
###### Proposition


The [[sheaf topos]] $Sh(CartSp)$ is also a [[local topos]]

$$
  (L Const \dashv \Gamma \dashv CoDisc)
  \colon
  Sh(CartSp) \stackrel{\overset{L Const}{\longleftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{CoDisc}{\longleftarrow}}} 
  Set
$$

=--

+-- {: .proof}
###### Proof


The [[site]] [[CartSp]] is a [[local site]]: it has a [[terminal object]] and the only [[covering]] [[sieve]] of this object is the trivial one. This implies the claim, by the discussion at [[local site]].

Concretely, the extra [[right adjoint]] $CoDisc$ takes a [[set]] $S$ to the presheaf given by the assigmnent

$$
  CoDisc(S) : U \mapsto Hom_{Set}(CartSp(*,U), S)
  \,,
$$

that takes a Cartesian space $U$ to the set of [[function]]s from its underlying set of points to $S$. This is clearly a sheaf (a function of sets from $U$ to $S$ is clearly fixed by all its restrictions to a collections of  subsets of $U$ whose unition is $U$.)

=--

Geometrically, the object $CoDisc S \in Sh(CartSp)$ is the diffeological space [[codiscrete space|codiscrete]] (indiscrte) smooth structure.

+-- {: .num_prop}
###### Proposition

Every [[local topos]] comes with its notion of [[concrete sheaves]] that form a sub-[[quasitopos]]. For the local topos $Sh(CartSp)$ these are precisely the diffeological spaces.

$$

  Set \stackrel{\leftarrow}{\underset{CoDisc}{\hookrightarrow}}
  DiffologicalSp \stackrel{\leftarrow}{\hookrightarrow}
  Sh(CartSp)
$$


=--



+-- {: .proof}
###### Proof


The [[concrete sheaves]] for the [[local topos]] $Sh(CartSp)$ are by definition those objects $X$ for which the 
$(\Gamma \dashv CoDisc)$-[[unit of an adjunction|unit]]

$$
  X \to CoDisc \Gamma X
$$

is a [[monomorphism]]. Monomorphisms of sheaves are tested objectwise, so that means equivalently that for every $U \in CartSp$ we have that 

$$
  X(U) \simeq Hom_{Sh}(U,X) \to Hom_{Sh}(U, Codisc \Gamma X)
  \simeq Hom_{Set}(\Gamma U, \Gamma X)
$$

is a monomorphism. This is precisely the condition on a sheaf to be a diffeological space.

=--



##### Cohesion
 {#CohesionOfTheToposOfSmoothSpaces}


+-- {: .num_prop}
###### Proposition

The [[sheaf topos]] $Sh(CartSp)$ is even a [[cohesive topos]] in which the axiom _[pieces have points](/nlab/show/cohesive+topos#PiecesHavePoints)_ holds.

=--

+-- {: .proof}
###### Proof

The [[site]] [[CartSp]] is a [[cohesive site]] (see there for detail). This implies the statement.

=--

This implies that $Sh(CartSp)$ is a [[locally connected topos]], [[connected topos]], [[local topos]]. It means in addition that it is also a [[strongly connected topos]].

This means that there is a _homotopy category_ or _concordance category_ of [[smooth spaces]], with the same objects as $Sh(CartSp)$, but with hom-sets given by

$$
  Conc(X,Y) := \Pi_0 [X,Y]_{Sh(CartSp)}
 \,,
$$

where $[X,Y]_{Sh(CartSp)}$ is the [[internal hom]] in the [[cartesian closed category]] $Sh(CartSp)$.




### Syntactic Layer
 {#SmoothSpacesLayerSyn}

In this [Syntactic Layer](#LayerSyn) we discuss the two further aspects that the [[internal language]] of a [[topos]] adds to the internal language of a just a category with [[finite products]] (which is the [[dependent type theory|dependent]] [[type theory]] with [[unit type]] and [[product type]] discussed in _[Coordinate systems - Syntactic Layer](#CoordinateSystemsLayerSyn)): [[dependent product types]] and a [[type of propositions]].

[[dependent type theory]] $\leftrightarrow$ [[locally cartesian closed category]]

[[type of propositions]] $\leftrightarrow$ [[subobject classifier]]

(...)


#### Type theory of a topos

##### Natural deduction rules for dependent product types
 {#NaturalDeductionForDependentProduct}

[[!include dependent product natural deduction - table]]

In the special case that $A$ does not actually deopend on $X$:

[[!include function type natural deduction - table]]

##### Internal logic of a topos

What is called _[[logic]]_ is the [[syntax]] for [[n-truncated object in an (infinity,1)-category|(-1)-truncated objects]] in [[slice categories]], hence of [[monomorphisms]] regarded as objects of slice categories.

(...)

* [[propositions as types]], [[programs as proofs]]

* [[computational trinitarianism]]

* [[type of propositions]]

#### Modal type theory

##### Modalities

* [[modal logic]], [[modal type theory]]

* [[monad (in computer science)]]

##### Sharp modality and Codiscrete types
 {#SharpModalityAndCodiscreteTypes}

+-- {: .num_defn #SharpModalityOfLocalTopos}
###### Definition

Let $\mathbf{H}$ be a [[local topos]]

$$
  \mathbf{H}
   \stackrel{\stackrel{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{CoDisc}{\leftarrow}}}
  \,.
$$

Write

$$
  (\flat \dashv \sharp)
  \;
  \colon
  \;
  \mathbf{H}
  \stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\to}}
  \, .
  \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{coDisc}{\to}}
  \, .
$$

for the induced [[adjoint functor|adjoint]] [[monad]] $\sharp$ and [[comonad]] $\flat$. We 

* call $\sharp$ the **sharp modality**;

* call $\flat$ the **flat modality**.

=--

The term _modality_ refers to _[[modal logic]]_. (...)

+-- {: .num_remark}
###### Remark

We refer to $\sharp A$ as the **sharp type** of $A$. 
This may be thought of as referring to the fact that by [[adjunction]] a homomorphism
$X \to \sharp A$ is equivalently a function
$\Gamma X \to \Gamma A$ of the underlying sets. This means that smooth maps $X \to \sharp A$ are like maps into $A$ that do _not_ have to respect the cohesive structure on $A$, but instead 
can be arbitrarily "kinky" ("sharp").

=--

This motivates the following terminology.

+-- {: .num_defn #Decohese}
###### Definition

We write

$$
  DeCoh_X \colon X \to \sharp X
$$

For the [[unit of an adjunction|unit]] of the $(\Gamma \vdash coDisc)$-[[adjunction]].

=--


(...)

[[!redirects geometry of physics -- smooth spaces]]