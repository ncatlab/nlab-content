
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _complete Segal space_ is a model for an [[internal category in an (∞,1)-category]] in [[∞Grpd]], with the latter [[presentable (∞,1)-category|presented]] by [[sSet]]/[[Top]]. So complete Segal spaces present [[(∞,1)-categories]].  They are also called _Rezk categories_ after [[Charles Rezk]].

More in detail, a complete Segal space $X$ is

* for each $n \in \mathbb{N}$ a [[Kan complex]] $X_n$, thought of as the _space of composable sequences of $n$-morphisms and their composites_;

* forming a [[simplicial object]] $X_\bullet$ in [[sSet]] (a [[bisimplicial set]]);

such that

1. there is a [[composition]] operation well defined up to [[coherence|coherent]] [[homotopy]]: exibited by the [[Segal maps]]

   $$
     X_k \to X_1 \times_{X_0} \cdots \times_{X_0} X_1
   $$

   (into the iterated [[homotopy pullback]] of the [[∞-groupoid]] of 1-morphisms over the $\infty$-groupoid of objects) being [[homotopy equivalences]]

   (so far this defines a _[[Segal space]]_);

1. the notion of [[equivalence]] in $X_\bullet$ is compatible with that in the ambient [[∞Grpd]] ("completeness"): the sub-simplicial object $Core(X_\bullet)$ on the invertible morphisms in each degree is homotopy constant: it has all face and degeneracy maps being [[homotopy equivalences]].

   (this says that if a morphism is an equivalence under the explicit composition operation then it is already a morphism in $X_0$ ).

## Definition
 {#Definition}

We first discuss

* [Complete Segal spaces](#CompleteSegalSpaces)

as such, and then the more general notion of

* [Complete Segal space objects](#CompleteSegalSpaceObjects)

internal to a suitable model category/$(\infty,1)$-category $\mathcal{C}$ -- this reduces to the previous notion for $\mathcal{C} = sSet_{Quillen}$.

### Complete Segal spaces
 {#CompleteSegalSpaces}

+-- {: .num_defn}
###### Definition

A **[[Segal space]]** is a [[simplicial object]] in [[simplicial sets]]

$$
  X \in [\Delta^{op}, sSet]
$$

such that

* it is fibrant in the [[Reedy model structure]] $[\Delta^{op}, sSet_{Quillen}]_{Reedy}$;

* it is a [[local object]] with respect to the [[spine]] inclusions $\{Sp[n] \hookrightarrow \Delta[n]\}_{n \in \mathbb{N}}$;

  equivalently: for all $n \in \mathbb{N}$ the [[Segal map]]

  $$
    X_n \to X_1 \times_{X_0} \cdots \times_{X_0} X_1 
  $$

  is a [[weak homotopy equivalence]] (of [[Kan complexes]], in fact).

=--

([Rezk, 4.1](#Rezk)).

+-- {: .num_defn #HomotopyCategory}
###### Definition

For $X$ a Segal space, its **[[homotopy category]]** $Ho(X)$ is the
[[Ho(Top)]]-[[enriched category]] whose [[objects]] are the vertices of $X_0$ 

$$
  Obj(X) = (X_0)_0
$$

and for $x,y \in Obj(X)$ the [[hom object]] is the [[homotopy type]] of the [[homotopy fiber product]]

$$
  Ho(X)(x,y) := \pi_0 \Big(\{x\} \times_{X_0} X_1 \times_{X_0} \{y\}\Big)
  \,.
$$

The [[composition]]

$$
  Ho_X(x,y) \times Ho_X(y,z) \to Ho_X(x,z)
$$

is the (uniquely defined) action of the [[infinity-anafunctor]]

$$
  X_1 \times_{X_0} X_1
  \underoverset{\simeq}{(d_2, d_0)}{\leftarrow}
  X_2
  \stackrel{d_1}{\to}
  X_1
$$

on these connected components.

=--

([Rezk, 5.3](#Rezk))

+-- {: .num_defn}
###### Definition

For $X$ a Segal space, write

$$
  X_{hoequ} \hookrightarrow X_1
$$

for the inclusion of the connected components of those vertices that become [[isomorphisms]] in the homotopy category, def. \ref{HomotopyCategory}.

=--

([Rezk, 5.7](#Rezk))

+-- {: .num_defn}
###### Definition

A Segal space $X$ is called a **complete Segal space** if 

$$
  s_0 : X_0 \to X_{hoequ}
$$

is a weak equivalence. 

=--

([Rezk, 6.](#Rezk))

+-- {: .num_remark}
###### Remark

This condition is equivalent to $X$ being a [[local object]] with respect to the morphism $N(\{0 \stackrel{\simeq}{\to} 1\}) \to *$. This is discussed [below](#CharacterizationOfCompleteness).

=--

+-- {: .num_remark}
###### Remark

The completeness condition may also be thought of as _[[univalence]]_. See there for more.

=--

+-- {: .num_remark}
###### Remark

There is a Segal completion functor given in ([Rezk, 14.](#Rezk)).

=--

### Complete Segal space objects
 {#CompleteSegalSpaceObjects}

See [[category object in an (infinity,1)-category]] for more information.

(...)

## Properties

### Characterization of Completeness
 {#CharacterizationOfCompleteness}

+-- {: .num_theorem}
###### Theorem

A Segal space $X$ is a complete Segal space precisely if it is a [[local object]] with respect to the morphism $N(0 \stackrel{\simeq}{\to} 1) \to *$, hence precisely if with respect to the canonical [[sSet]]-[[enriched category|enriched]] [[hom objects]] we have that

$$
  X_0 
   \simeq 
  [\Delta^{op}, sSet](*, X) 
    \to 
  [\Delta^{op}, sSet](N(0 \stackrel{\simeq}{\to} 1), X)
$$

is a weak equivalence.

=--

([Rezk, theorem 6.2](#Rezk))

### Model category structure
 {#ModelCategoryStructure}

The category $[\Delta^{op}, sSet]$ of [[simplicial presheaves]] on the [[simplex category]] ([[bisimplicial sets]]) supports a [[model category]] structure whose fibrant objects are precisely the complete Segal spaces: the _[[model structure for complete Segal spaces]]_. This presents the [[(∞,1)-category of (∞,1)-categories]].

### Relation to simplicial localization
 {#RelationToSimplicialLocalization}

Given $\mathcal{C}$ a [[category with weak equivalences]] $\mathcal{W} \subset Mor(\mathcal{C})$ or more generally a "[[relative category]]", then there is canonically a complete Segal space associated with it by the "relative nerve" construction, def. \ref{RelativeNerve} followed by fibrant replacement, and hence by the [model structure](#ModelCategoryStructure) this determines an [[(∞,1)-category]] $N_{Rezk}(\mathcal{C},\mathcal{W})$ . 

On the other hand classical [[simplicial localization]]-theory provides several ways (e.g. [[hammock localization]]) to turn $(\mathcal{C}, \mathcal{W})$ into an [[(∞,1)-category]] $\mathcal{C}[\mathcal{W}]^{-1}$ which universally turns the elements in $\mathcal{W}$ into [[homotopy equivalences]].

+-- {: .num_theorem}
###### Theorem

These constructions are compatible in that there is an [[equivalence of (∞,1)-categories]]

$$
  N_{Rezk}(\mathcal{C},\mathcal{W})
  \simeq
  \mathcal{C}[\mathcal{W}^{-1}]
  \,.
$$

=--

For [[simplicial model categories]] this is ([Rezk, theorem 8.3](#Rezk). For general [[model categories]] this is ([Bergner 07, theorem 6.2](#Bergner07)). For the fully general case this follows from results by [[Clark Barwick]], [[Daniel Kan]] and [[Bertrand Toën]] as pointed out by [[Chris Schommer-Pries]] [here on MathOverflow](http://mathoverflow.net/a/93139/381).

In fact, the construction $(\mathcal{C},\mathcal{W})\mapsto N_{Rezk}(\mathcal{C},\mathcal{W})$ admits a direct generalization in the case where $\mathcal{C}$ is a [[quasicategory]], and $N_{Rezk}(\mathcal{C},\mathcal{W})$ still presents the localization $\mathcal{C}[\mathcal{W}^{-1}]$. This is ([Mazel-Gee19, Theorem 3.8](#MazelGee19)). A generalization can be found in ([Arakawa23, Theorem 1.7](#Arakawa23)).

### Model categories for presheaves

There is a notion of [[right/left fibration of complete Segal spaces]] analogous to [[right/left Kan fibrations]] for [[quasi-categories]].


## Examples
 {#Examples}

We discuss some examples. For more and more basic examples see also at _[Segal space -- Examples](Segal+space#Examples)_.

### Ordinary categories as complete Segal spaces
 {#OrdinaryCategoriesAsCompleteSegalSpaces}

We discuss how an ordinary [[small category]] is naturally regarded as a complete Segal space.
([Rezk, 3.5](#Rezk))

#### Preliminaries

We need the following basic ingredients.

Write $(-)^{(-)} : Cat^{op} \times Cat \to Cat$ for the [[internal hom]] in [[Cat]], sending two categories $A$, $X$ to the [[functor category]] $X^A = Func(A,X)$.

By the discussion at [[nerve]] we have a canonical functor

$$
  \Delta \hookrightarrow Cat
$$

including the [[simplex category]] into [[Cat]] by regarding the [[simplex]] $\Delta[n]$ as the category generated from $n$ consecutive morphisms.

The [[nerve]] itself is then then functor

$$
  N : Cat \to sSet
$$

to [[sSet]] sending a category $C$ to 

$$
  N(C) : k \mapsto C^{\Delta[k]}
  \,.
$$

Its restriction along $Grpd \hookrightarrow Cat$ to [[groupoids]] lands in [[Kan complexes]] $KanCplx \hookrightarrow $ [[sSet]].

The [[core]] operation is the functor

$$
  Core : Cat \to Grpd
$$

[[right adjoint]] to the inclusion of [[Grpd]] into [[Cat]]. It sends a category to the groupoid obtained by discarding all non-invertible morphisms.

#### The construction

Let $C$ be a [[small category]]. Define 

$$
  \mathbf{C} \in [\Delta^{op}, sSet]
$$

by

$$
  \mathbf{C}_k := N(Core(C^{\Delta[k]}))  
  \,.
$$

In degree 0 this is the the [[core]] of $C$ itself. In degree 1 it is the groupoid $\mathbf{C}_1$ underlying the [[arrow category]] of $C$. 

One sees that the [[source]] and [[target]] functors $s, t : C^{\Delta[1]} \to C$ are [[isofibrations]] and hence their image under [[core]] and [[nerve]] are [[Kan fibrations]]. Therefore it follows that the [[homotopy pullback]] (see there) $\mathbf{C}_1 \times_{\mathbf{C}_0} \cdots \times_{\mathbf{C}_0} \mathbf{C}_1$ is given already be the ordinary [[pullback]] in the [[1-category]] [[Grpd]]. Using this, it is immediate that for all $k$ the functors

$$
  Core(C^{\Delta[k]}) \to Core(C^{\Delta[1]}) \times_{Core(C)} \cdots \times_{Core(C)} Core(C^{\Delta[1]}) 
$$

are [[isomorphisms]], and so in particular 

$$
  \mathbf{C}_k 
   \to 
  \mathbf{C}_1 \times_{\mathbf{C}_0} \cdots \times_{\mathbf{C}_0} \mathbf{C}_1
$$

is an equivalence. 

It is clear that the [[composition]] operation in the complete Segal space defined this way "is" the composition in $C$. In particular the morphisms that are invertible under this composition are precisely those that are already invertible in $C$. Therefore we have the core simplicial object

$$
  Core(\mathbf{C}) : k \mapsto N(Core(C)^{\Delta[k]})
   = N(Core(C))^{\Delta[k]}
  \,,
$$

where, note, now we _first_ take the core of $C$ and then form morphism categories. 

This simplicial Kan complex has in each positive degree a [[path space object]] for the [[Kan complex]] $N(Core(C))$.

Notably (since $\Delta[k]$ is [[weak homotopy equivalence|weak homotopy equivalent]] to the point) it follows that indeed all the face and degeneracy maps are weak homotopy equivalences.

So for every category $C$, the simplicial object $\mathbf{C}$ constructed as above is a complete Segal space. This construction extends to a functor $Cat \to completeSegalSpace$ and this is homotopy full and faithful.

#### Properties of the inclusion
 {#PropertiesOfTheInclusionOfCategories}
 

Write

$$
 Sing_J : Cat \to [\Delta^{op}, sSet]
$$

for the functor just defined

+-- {: .num_prop}
###### Proposition

For $C$ and $D$ two categories, there are [[natural isomorphisms]]

$$
  Sing_J(C \times D)
  \simeq
  Sing_J(C) \times Sing_J(D)
$$

and

$$
  Sing_J(D^C) \simeq (Sing_J D)^{Sing_J C}
  \,.
$$

A functor $f : C \to D$ is an [[equivalence of categories]] precisely if $Sing_J(f)$ is an equivalence in the [[Reedy model structure]] $[\Delta^{op}, sSet]_{Reedy}$ (hence is degreewise a [[weak homotopy equivalence]] of Kan complexes).

=--

This appears as ([Rezk, theorem 3.7](#Rezk)).

### Relative and Model categories as complete Segal spaces
 {#RelativeCategoryAsCompleteSegalSpace}

Let $C$ be a category with a class $W \subset Mor(C)$ of [[category with weak equivalences|weak equivalences]].  For instance, $C$ could be a [[model category]] or (much) more generally a "[[relative category]]".  Then the [above](#OrdinaryCategoriesAsCompleteSegalSpaces) construction has the following evident variant.

+-- {: .num_prop #RelativeNerve}
###### Definition

Let $N(C,W) \in [\Delta^{op}, sSet]$ be given by
$$ N(C,W) : n \mapsto N(Core_W(C^{\Delta[n]})) \,, $$ 
where now $Core_W(-)$ denotes the [[subcategory]] on those [[natural transformations]] whose components are [[weak equivalences]] in $C$.

=--

+-- {: .num_remark}
###### Remark

The typical [[model category]] is not a [[small category]] with respect to the base choice of [[universe]]. In this case $N(C,W)$ will be a "[[large set|large]]" bisimplicial set. In other words, one needs to employ some [[universe enlargement]] to interpret this definition.

=--

+-- {: .num_remark}
###### Remark

If $C$ is a model category, then $Core_W(C^{\Delta[n]})$ is the subcategory of weak equivalences in any of the standard [[model structures on functors]] on $C^{\Delta[n]}$. By a [classical fact](/nlab/show/%28infinity%2C1%29-categorical+hom-space#SpacesOfEquivalences) discssed at _[[(∞,1)-categorical hom-space]]_, its [[nerve]] is a model for the [[core]] of the corresponding [[(∞,1)-category of (∞,1)-functors]].

=--

The bisimplicial set $N(C,W)$ is not, in general, a complete Segal space.  It does, however, represent the same [[(∞,1)-category]] as the [[simplicial localization]] of $C$ at $W$; see [this MO question](http://mathoverflow.net/questions/92916/does-the-classification-diagram-localize-a-category-with-weak-equivalences/93139).

We can, of course, always reflect $N(C,W)$ into a complete Segal space by passing to a [[fibrant replacement]] in the [[model structure for complete Segal spaces]].  But something better is true here: it suffices to make a _[[Reedy model structure|Reedy]] fibrant_ replacement (which does not change the [[homotopy type]] of the simplicial sets $N(Core_W(C^{\Delta[n]}))$, but only "arranges them more nicely").

+-- {: .num_prop}
###### Proposition
Any [[Reedy model structure|Reedy fibrant replacement]] of $N(C,W)$ is a complete Segal space.
=--

This is ([Rezk, theorem 8.3](#Rezk)).

### Quasi-categories as complete Segal spaces
 {#QuasiCategoriesAsCompleteSegal}

The formula $\mathcal{C} \mapsto k \mapsto Core(\mathcal{C}^{\Delta[k]})$ also defines a relative functor from quasi-categories to complete segal spaces,
which has a one-sided inverse $X \mapsto X_{\bullet,0}$. This is the $\Gamma$ appearing in [Joyal & Tierney (2007), proposition 4.10](#JoyalTierney07).

However, to get a right Quillen functor, we need to use a different model of Core.

+-- {: .num_defn}
###### Definition

Write 

$$
  \Delta_J : \Delta \to sSet
$$

for the [[cosimplicial object|cosimplicial]] [[simplicial set]] that sends $[n]$ to the [[nerve]] of the [[codiscrete groupoid]] on $n+1$ objects

$$
  \Delta_J[n] = N(0 \stackrel{\simeq}{\to} \cdots \stackrel{\simeq}{\to} n)
  \,.
$$

Write

$$
 Sing_J : sSet \to [\Delta^{op}, sSet]
$$

for the functor given by


$$
  Sing_J(X)_n = Hom_{sSet}(\Delta[n] \times \Delta_J[\bullet], X)
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

For $X \in sSet$ a [[quasi-category]]/[[inner Kan complex]], $Sing_J(X)$ is a complete Segal space. 

=--

See at _[[model structure for dendroidal complete Segal spaces]]_ the section _[Quasi-operads to dendroidal complete Segal spaces](model+structure+for+dendroidal+complete+Segal+spaces#QuasiOperadsToDendroidalCompleteSegal)_

## Related concepts

* [[semi-Segal space]], [[Segal space]]

* [[model structure for complete Segal spaces]]

* [[higher complete Segal space]], [[dendroidal complete Segal space]]

* [[Rezk completion]]

* [[directed homotopy type theory]]

* [[table - models for (infinity,1)-operads]]



## References

### General

Complete Segal spaces were originally defined in 

* {#Rezk} [[Charles Rezk]], _A model for the homotopy theory of homotopy theory_ , Trans. Amer. Math. Soc., 353(3), 973-1007 ([arXiv:math/9811037](https://arxiv.org/abs/math/9811037))
 

The relation to [[quasi-categories]] is discussed in 

* {#JoyalTierney07} [[Andre Joyal]], [[Myles Tierney]], _Quasi-categories vs. Segal spaces_, in *Categories in Algebra, Geometry and Mathematical Physics*, Contemporary Mathematics **431** (2007) &lbrack;[arXiv:math/0607820](http://arxiv.org/abs/math/0607820), [doi:10.1090/conm/431](https://doi.org/10.1090/conm/431)&rbrack;


Further discussion of the relation to [[simplicial localization]] is in 

* {#Bergner07} [[Julia Bergner]], _Complete Segal spaces arising from simplicial categories_ ([arXiv:0704.1624](http://arxiv.org/abs/0704.1624))

* {#MazelGee19}[[Aaron Mazel-Gee]], _The universality of the Rezk nerve_, Algebr. Geom. Topol., 19(7), 2019, 3217--3260 ([arXiv:math/1510.03150](https://arxiv.org/abs/1510.03150), [doi:10.2140/agt.2019.19.3217](https://doi.org/10.2140/agt.2019.19.3217))

* {#Arakawa23}[[Kensuke Arakawa]], _Classification Diagrams of Marked Simplicial Sets_ ([arXiv:math/2311.01101](https://arxiv.org/abs/2311.01101)).

A survey of the definition and its relation to equivalent definitions is in section 4 of 

* [[Julia Bergner]], _A survey of $(\infty, 1)$-categories_ ([arXiv](http://arxiv.org/abs/math.AT/0610239)).

See also pages 29 to 31 of

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_

For literature on the variants and refinements see at _[[Theta space]]_ and _[[n-fold complete Segal space]]_.

Related MathOverflow discussion includes

* [Does the classification diagram localize a category with weak equivalences?](http://mathoverflow.net/q/92916/381)


[[!redirects complete Segal spaces]]
[[!redirects Rezk category]]
[[!redirects Rezk categories]]

[[!redirects Segal completeness]]

[[!redirects Segal completion]]
[[!redirects Segal completions]]
