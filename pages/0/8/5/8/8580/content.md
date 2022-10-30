

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


## About this page

This page is going to contain an introduction to aspects of [[differential geometry]] and their application in fundamental [[physics]]: the [[gauge theory]] appearing in the [[standard model of particle physics]] and the [[Riemannian geometry]] appearing in the [[standard model of cosmology]], as well as the [[symplectic geometry]] appearing in the [[quantization]] of both.

### Scope and perspective

The intended topic scope and readership of the first layer of this page -- the _[Mod Layer](#LayerMod)_ --  is much like that of the book ([Frankel](#Frankel)), only that here we make use of a more modern and more transparent conceptual toolbox and discuss in two other layers, the _[Sem Layer](#LayerSem)_ and the _[Syn Layer](#LayerSyn)_ the deeper mechanisms at work in the background.

For instance where traditionally expositions of [[differential geometry]] proceed by generalizing the [[geometry]] of abstract [[coordinate|coordinate systems]] $\mathbb{R}^n$ to _[[smooth manifolds]]_, here we instead begin by generalizing, in the _[Mod layer](#LayerMod)_, coordinate systems right away to _[[smooth spaces]]_, which happens to be both more expressive as well as actually much easier. In parallel (and to be read independently or not at all) we discuss in the  [Sem layer](#LayerSem) how this means that we are working in the _[[sheaf topos]]_ over abstract coordinate systems.  Smooth manifolds are then introduced later as an intermediate notion, together with that of _[[diffeological spaces]]_. (Many of the constructions in [[differential geometry]] applied in [[physics]] do not actually need the notion of a smooth manifold, and, more importantly, for many notions in modern theoretical physics smooth manifolds are not actually sufficiently general.) 

In fact we introduce smooth manifolds only after we introduce _[[smooth groupoids]]_, which are differential geometric structures that are _still_ simpler than smooth manifolds, and of course even more expressive than smooth spaces. In fact, smooth groupoids are the very heart of the geometry of physics. Modern fundamental physics is all based on the "[[gauge symmetry|gauge principle]]" and in the [Mod Layer](#LayerMod) we explain how, mathematically, this is essentially nothing but the theory of smooth groupoids. As further background information we discuss in the [Sem Layer](#LayerSem) how this means that we are working in a [[(infinity,1)-topos|higher topos]] over abstract coordinate systems, and in the [Syn Layer](#LayerSyn) how this means that we are reasoning about physics using the _[[natural deduction]]_ rules of _[[homotopy type theory]]_.

### Layers of exposition
 {#Layers}

We discuss each topic below in three stages, in three _layers_. 

1. The first layer, called **Layer Mod**, deals with concrete explicit  constructions as familiar from traditional textbooks on differential geometry and physics. This layer is supposed to be readable and useful all in itself and the reader who feels that this is all he or she wants to see can stick to this and ignore the other layers. In particular, while _Layer Mod_ does invoke the basic notion of a _[[category]]_ and of a _[[functor]]_ -- which are as simple as the notions of [[group]] or [[associative algebra|algebra]] --, it does not use any actual _[[category theory]]_. 
 {#LayerMod}

1. The second layer, called **Layer Sem**, makes explicit the ([[(infinity,1)-category theory|higher]]) [[category theory]] and ([[(infinity,1)-topos theory|higher]]) [[topos theory]] at work in the background. This puts the concrete constructions of _Layer Mod_ into a more general context and helps to see certain organizational patterns that underly the seemingly different phenomena. It provides some powerful theorems which _Layer Mod_ is secretly benefitting from. For instance this layer gives a systematic rule for generalizing everything at the beginning in _Layer Mod_ from ordinary [[differential geometry]] to what is called  _[[supergeometry]]_, which is the context in which [[fermion|fermionic]] [[particles]] are formalized: the [[matter]] constituents of the [[observable universe]].
 {#LayerSem}

1. The third layer, called **Layer Syn**, makes explict the expression of these phenomena in the [[logical framework|formal]] [[internal language]] of the [[topos]] of [[smooth spaces]] -- which is _[[dependent type theory|dependent]] [[type theory]]_ -- and of the [[(infinity,1)-topos|higher topos]] of [[smooth infinity-groupoid|smooth higher groupoids]] -- which is _[[homotopy type theory]]_. This makes more transparent various constructions in ([[(infinity,1)-topos theory|higher]]) [[topos theory]] used in _Layer Sem_, and in fact it provides 
a [[categorical semantics|natural construction principle]] for objects in a (higher) topos that model some intended _meaning_, which is precisely what [[mathematical physics]] is about.
This is meant for readers who enjoy seeing fundamental physics _naturally_ rooted in genuinely fundamental mathematics, in _[[natural deduction]]_, as it were. Everybody else should ignore this.
 {#LayerSyn}
 
**The three layers**

* **Layer Mod** -- [[concrete particular]]: [[models]]

* **Layer Sem** -- [[concrete general]]: [[categorical semantics]] in [[(infinity,1)-topos theory|higher]] [[topos theory]]

* **Layer Syn** -- [[abstract general]]: [[syntax]] in [[homotopy type theory|homotopy]]-[[type theory]]

## Coordinate systems
 {#CoordinateSystems}

Every kind of _[[geometry]]_ is modeled on a collection of [[generator|archetypical]] basic [[spaces]] and geometric [[homomorphisms]] between them. In [[differential geometry]] the archtypical spaces are the abstract standard [[Cartesian space|Cartesian coordinate systems]], denoted $\mathbb{R}^n$, in every [[dimension]] $n \in \mathbb{N}$, and the geometric homomorphism between them are [[smooth functions]] $\mathbb{R}^{n_1} \to \mathbb{R}^{n_1}$, hence smooth (and possiby degenerate) [[coordinate transformations]].

Here we discuss the central aspects of the nature of such abstract coordinate systems in themselves. At this point these are not yet coordinate systems _on_ some other space. That is instead the topic of the next section _[Smooth spaces](#SmoothSpaces)_.

### Layer Mod
 {#CoordinateSystemsLayerMod}

In this [Mod Layer ](#LayerMod) we discuss the [[concrete particulars]] of _[[coordinate systems]]_: the [[continuum]] [[real line]] $\mathbb{R}$, the [[Cartesian spaces]] $\mathbb{R}^n$ formed from it and the [[smooth functions]] between these.

#### The continuum real (world-)line
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

Speculations are common that in a fully exact theory of [[quantum gravity]], currently unavailable, this assumption needs to be refined. 
For instance in _[[p-adic physics]]_ one explores the hypothesis that the relevant [[complete field|completion]] of the rational numbers as above is not the reals, but [[p-adic numbers]] $\mathbb{Q}_p$ for some [[prime number]] $p \in \mathbb{N}$. Or for example in the study of [[QFT on non-commutative spacetime]] one explore the idea that at small scales the smooth [[continuum]] is to be replaced by an object in [[noncommutative geometry]]. Combining these two ideas leads to the notion of [[non-commutative analytic space]] as a potential model for _[[space]]_ in [[physics]]. And so forth.

For the time being all this remains speculation and differential geometry based on the [[continuum]] [[real line]] remains the context of all fundamental [[model (in theoretical physics)|model building]] in physics related to observed [[phenomenology]]. Often it is argued that these speculations are necessitated by the very nature of [[quantum theory]] applied to [[gravity]]. But, at least so far, such statements are not actually supported by the standard theory of [[quantization]]:
we discuss below in _[Geometric quantization](GeometricQuantization)_ how not just [[classical physics]] but also [[quantum theory]], in the best modern version available, is entirely rooted in differential geometry based on the [[continuum]] [[real line]].

This is the motivation for studying models of physics in geometry modeled on the [[continuum]] [[real line]]. On the other hand, in all of what follows our discussion is set up such as to be _maximally independent_ of this specific choice (this is what _[[topos theory]]_ accomplishes for us, discussed below _[Smooth spaces -- Layer Sem](#SmoothSpacesLayerSem)_). If we do desire to consider another choice of archetypical spaces for the geometry of physics we can simply "change the [[site]]", as discussed [below](#SmoothSpacesLayerSem) and many of the constructions, propositions and theorems in the following will continue to hold. This is notably what we do below in _[Supergeometric coordinate systems](#SupergeometricCoordinateSystems)_ when we generalize the present discussion to a flavor of differential geometry that also formalizes the notion of [[fermion]] [[particles]]: "differential [[supergeometry]]."


#### Cartesian spaces and smooth functions
 {#CartesianSpaces}



+-- {: .num_defn}
###### Definition

A [[function]] of [[sets]] $f : \mathbb{R} \to \mathbb{R}$ is called 
a **[[smooth function]]** if, [[coinduction|coinductively]]:

1. the [[derivative]] $\frac{d f}{d x} : \mathbb{R} \to \mathbb{R}$ exists;

1. and is itself a smooth function.

=--

+-- {: .num_defn #CartesianSpaceAndHomomorphism}
###### Definition

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

A **[[homomorphism]]** of Cartesian spaces is a [[smooth function]]

$$
  f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}
  \,,
$$

hence a [[function]] $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ such that all [[partial derivatives]] exist and are [[continuous map|continuous]] (...).

=--

+-- {: .num_example}
###### Example

Regarding $\mathbb{R}^n$ as an $\mathbb{R}$-[[vector space]], 
every [[linear function]] $\mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$
is in particular a [[smooth function]].

=--

+-- {: .num_remark}
###### Remark

But a homomorphism of Cartesian spaces in def. \ref{CartesianSpaceAndHomomorphism} is *not* required to be a [[linear map]]. We do *not* regard the Cartesian spaces here as [[vector spaces]]. 

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

+-- {: .num_prop #CartSpCategory}
###### Propositions

Abstract coordinate systems according to prop. \ref{CartesianSpacesAndSmoothFunctions} form a _[[category]]_ 
-- to be denoted _[[CartSp]]_ -- whose

* [[objects]] are the abstract coordinate systems $\mathbb{R}^{n}$ (the [[class]] of objects is the [[set]] $\mathbb{N}$ of [[natural numbers]] $n$);

* [[morphisms]] $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ are the abstract [[coordinate transformations]] = [[smooth functions]].

Composition of morphisms is given by [[composition]] of [[functions]].

We have that

1. The [[identity]] morphisms are precisely the identity functions.

1. The [[isomorphisms]] are precisely the [[diffeomorphisms]].

=--

+-- {: .num_defn}
###### Definition

Write [[CartSp]]${}^{op}$ for the [[opposite category]] of [[CartSp]].

This is the category with the same objects as $CartSp$, but where a morphism $\mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ in $CartSp^{op}$ is given by a morphism $\mathbb{R}^{n_1} \leftarrow \mathbb{R}^{n_2}$ in $CartSp$.

=--

We will be discussing below the idea of exploring smooth spaces by laying out abstract coordinate systems in them in all possible ways. The reader should begin to think of the sets that appear in the following definition as the _set of ways_ of laying out a given abstract coordinate systems in a given space. This is discussed in more detail below in _[Smooth spaces](#SmoothSpaces)_.

+-- {: .num_defn}
###### Definition

A [[functor]]  $X : CartSp^{op} \to Set$ (a "[[presheaf]]") is

1. for each abstract coordinate system $U$ a [[set]] $X(U)$

1. for each [[coordinate transformation]] $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ a [[function]] $X(f) : X(\mathbb{R}^{n_2}) \to X(\mathbb{R}^{n_2})$

such that 

1. [[identity]] is respected $X(id_{\mathbb{R}^n}) = id_{X(\mathbb{R}^n)}$;

1. [[composition]] is respected $X(f_2)\circ X(f_1) = X(f_2 \circ f_1)$

=--


#### The fundamental theorems about smooth functions
 {#PropertiesOfSmoothFunctions}

The special properties [[smooth functions]] that make them play an important role different from other classes of functions are the following.

1. existence of [[bump functions]] and [[partitions of unity]]

1. the [[Hadamard lemma]] and [[Borel's theorem]]

Or maybe better put: what makes smooth functions special is that the first of these properties holds, while the second is still retained.

(...)


### Layer Sem
 {#CoordinateSystemsLayerSem}

In this [Sem Layer](#LayerSem) we discuss the [[concrete general]] aspects of _abstract [[coordinate systems]]_, def. \ref{CartesianSpacesAndSmoothFunctions}: the fact that they naturally form: 

1. an _[[algebraic theory]]_, 

1. a _[[site]]_.

#### The algebraic theory of smooth algebras
 {#TheAlgebraicTheoryOfSmoothAlgebras}

+-- {: .num_prop}
###### Propositions

* The [[category]] [[CartSp]] has all [[finite limit|finite]]
[[products]]. 

* Every object is a finite [[product]] of the object $\mathbb{R}$ (the [[real line]] itself).

* The [[terminal object]] is $\mathbb{R}^0$, the [[point]].

=--

Hence [[CartSp]] is (the [[syntactic category]]) of an [[algebraic theory]] ([[Lawvere theory]]). 

+-- {: .num_defn}
###### Definition

This is called the [[theory]] of _[[smooth algebras]]_.

A [[product]]-preserving [[functor]] 

$$
  A : CartSp \to Set
$$

is a _[[smooth algebra]]_.

=--

+-- {: .num_example}
###### Example

* The [[smooth algebra]] $C^\infty(\mathbb{R}^n)$ of [[smooth functions]] on the [[Cartesian space]] $\mathbb{R}^n$ is the [[representable functor|functor corepresented]] by $\mathbb{R}^n$.

* The [[ring of dual numbers|algebra of dual numbers]] $C^\infty(\mathbf{D})$ is the smooth algebra which assigns...

* (...)

=--

(...)

#### The coverage of differentially good open covers
 {#CoverageOfDifferentiallyGoodOpenCovers}

+-- {: .num_defn}
###### Definition

The [[open ball]] is

$$
  D^n \hookrightarrow \mathbb{R}^n
$$

(...)

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

A **differentially [[good open cover]]** of a [[Cartesian space]] $\mathbb{R}^n$ is a set $\{U_i \hookrightarrow \mathbb{R}^n\}$ of [[open subset]] inclusions of Cartesian spaces such that these [[open cover|cover]] $\mathbb{R}^n$
and such for each non-empty finite [[intersection]] there exists a [[diffeomorphism]] 

$$
  \mathbb{R}^n \stackrel{\simeq}{\to} U_{i_1} \cap \cdots \cap U_{i_k}
$$

that identifies the $k$-fold intersection with a Cartesian space itself.

=--

+-- {: .num_theorem}
###### Theorem

Every [[open cover]] refines to a differentially good open cover, def. \ref{DifferentiallyGoodOpenCover}. 

=--

A proof is at _[[good open cover]]_. 

+-- {: .num_remark}
###### Remark

Despite its appearance, this is not quite a classical statement. The classical statement is only that every open cover is refined by a _topologically_ [[good open cover]]. See the comments _[here in the references-section](http://ncatlab.org/nlab/show/ball#References)_ at _[[open ball]]_ for the situation concerning this statement in the literature.

=--

+-- {: .num_prop}
###### Proposition

The differentially good open covers, def. \ref{DifferentiallyGoodOpenCover}, constitute a [[coverage]] on [[CartSp]]. 

Hence [[CartSp]] equipped with that coverage is a [[site]].

=--


### Layer Syn
 {#CoordinateSystemsLayerSyn}

In this [Syn Layer](#LayerSyn) we discuss the [[abstract generals]] of _abstract [[coordinate systems]]_, def. \ref{CartesianSpacesAndSmoothFunctions}: the [[internal language]] of a category with [[products]], which is _[[type theory]]_ with _[[product types]]_.

#### Judgments about types and terms
 {#Judgments}

We now introduce a different _notation_ for [[objects]] and [[morphisms]] in a [[category]] (such as the category [[CartSp]] of def. \ref{CartSpCategory}). This notation is designed to, eventually, make more transparent what exactly it is that happens when we [[deductive reasoning|reason deductively]] about [[objects]] and [[morphisms]] of a [[category]]. 

But before we begin to make any actual [[deductions]] about [[objects]] and [[morphisms]] in a category [below](#NaturalDeductionRulesForProductTypes), in this section here we express the given objects and morphsims at hand in the first place. Such basic statements of the form "There is an object called $A$." are to be called _[[judgments]]_, in order not to confuse these with genuined _[[propositions]]_ that we eventually formalize _within_ this [[metalanguage]].

To express that there is an [[object]] 

$$
  X \in \mathcal{C}
$$ 

in a [[category]] $\mathcal{C}$, we write now equivalently the string of symbols (called a _[[sequent]]_)

$$
  \vdash \; X \colon Type
  \,.
$$

We say that these symbols express the _[[judgement]]_ that $X$ is a _[[type]]_. We also say that $\vdash \; X \colon Type$ is the _[[syntax]]_ of which $X \in \mathcal{C}$ is the _[[categorical semantics]]_.

For instance the [[terminal object]] $* \in \mathcal{C}$ we call the [[categorical semantics]] of the _[[unit type]]_ and write [[syntax|syntactically]] as

$$
  \vdash \; Unit \colon Type
  \,.
$$

If we want to express that we do assume that a terminal object indeed exists, hence that we want to be able to _[[deduction|deduce]]_ the existence of a terminal object from no hypothesis, then we write this [[judgment]] below a horizontal line

$$
  \frac{}{\vdash \; Unit \colon Type}
  \,.
$$

We will see more interesting such horizontal-line statements [below](#NaturalDeductionRulesForProductTypes).

Next, to express an [[element]] of the object $X$ in $\mathcal{C}$, hence a [[morphism]] 

$$
  * \stackrel{x}{\to} X
$$ 

in $\mathcal{C}$ we write equivalenly the [[sequent]]

$$
  \vdash \; x \colon X
$$

and call this the [[judgment]] that $x$ is a _[[term]]_ of [[type]] $X$.

Notice that every object $X \in \mathcal{C}$ becomes the [[terminal object]] in the _[[slice category]]_ $\mathcal{C}_{/X}$.
Let $A \to X$ be any morphism in $\mathcal{C}$, regarded as an object in the [[slice category]]

$$
  A \in \mathcal{C}_{/X}
  \,.
$$

We declare that the [[syntax]] of which this is the [[categorical semantics]] is given by the [[sequent]]

$$
  x \colon X \;\vdash \;  A(x) \colon Type
  \,.
$$

We say that this expresses the [[judgement]] that $A$ is an  _$X$-[[dependent type]]_; or a type in the _[[context]] of a [[free variable]]_ $x$ of [[type]] $X$.

Notice that an [[element]] of $A \in \mathcal{C}_{/X}$ is a [[generalized element]] of $A$ in $\mathcal{C}$, namely a morphism $X \to A$ which fits into a [[commuting diagram]]

$$
  \array{
    X &&\stackrel{a}{\to}&& A
    \\
    & {}_{\mathllap{id_X}}\searrow && \swarrow_{}
    \\
    && X
  }
$$

in $\mathcal{C}$.

We declare that the [[syntax]] of which such

$$
  a \in A  \;\;\;\; (in \mathcal{C}_{/X})
$$

is this the [[categorical semantics]] is the [[sequent]]

$$
  x\colon X \;\vdash\; a(x) : A(x)
  \,.
$$

We say that this expresses the [[judgment]] that $a(x)$ is a [[term in context|term depending on]] the [[free variable]] $x$ of [[type]] $X$.

This completes the list of _[[judgment]]_ [[syntax]] to be considered. Notice that if the category $\mathcal{C}$ has [[products]] then, even though it does not explicitly appear above, this is sufficient to express any morphism $X \stackrel{f}{\to} Y$ in $\mathcal{C}$ as the [[semantics]] of a [[term]]: we regard this morphism naturally as being the corresponding morphism in the [[slice category]] $\mathcal{C}_{/X}$ which as a [[commuting diagram]] in $\mathcal{C}$ itself is

$$
  \array{
     X && \stackrel{(f,id_X)}{\to} &&  Y\times X
     \\
     & {}_{\mathllap{id_X}}\searrow && \swarrow_{\mathrlap{p_2}}
     \\
     && X
  }
  \,.
$$ 

This is the [[categorical semantics]] for which the [[syntax]] is simply

$$
  x \colon X \;\vdash\; y(x) \colon Y
  \,,
$$

being the [[judgment]] which expresses that $y(x)$ is a [[term in context]] of an $X$-[[dependent type]] $Y$ in the special degenerate case that $Y$ does not actually vary with $x \colon X$.



#### Natural deduction rules for product types
 {#NaturalDeductionRulesForProductTypes}

With the [above symbolic notation](#Judgments) for making [[judgments]] about the presence of [[objects]] and [[morphisms]] in a [[category]] $\mathcal{C}$, we now consider a system of rule of [[deduction]]  that tells us how we may _process_ these symbols (how to do _[[computations]]_) such that the new symbols we obtain in turn express new objects and new morphisms in $\mathcal{C}$ that we can build out of the given ones by _[[universal constructions]]_ in the sense of [[category theory]]. 

This way of _deducing_ new expressions from given ones is very basic as well as very natural and hence goes by the technical term _[[natural deduction]]_. For every kind of [[type]] (every [[universal construction]] in [[category theory]]) there is, in [[natural deduction]], one set of rules for how to [[deductive reasoning|deductively reason]] about it. This set of rules, in turn, always consists of four kinds of rules, called the

1. [[type formation rule]]

1. [[term introduction rule]]

1. [[term elimination rule]]

1. [[computation rule]].

These are going to be the [[syntax]] in _[[type theory]]_ of which [[universal constructions]] in [[category theory]] is the [[categorical semantics]].

In our running example where $\mathcal{C} = $ [[CartSp]], the only [[universal construction]] available is that of forming [[products]]. We therefore introduce now the [[natural deduction]] rules by way of example of the special case of [[product types]].

**1. [[type formation rule]]** Let 

$$
  A , B \in \mathcal{C}
$$ 

be two [[objects]] in a [[category]] with [[products]]. Then there exists [[generalized the|the]] [[product]] [[object]]

$$
  A \times B \in \mathcal{C}
  \,.
$$

We now declare that the [[syntax]] of which this state of affairs is the [[categorical semantics]] is the collection of symbols of the form

$$
  \frac{A \colon Type \;\;\;\;\; B \colon Type}{ A \times B \colon Type}
  \,.
$$

Here on top of the horizontal line we have the two [[judgments]] which express that, [[syntax|syntactically]], $A$ is a [[type]] and $B$ is a [[type]], and [[semantics|semantically]]  that $A \in \mathcal{C}$ and $B \in \mathcal{C}$. Below the horizontal line is, in turn, the [[judgment]] which expresses that there is, syntactically,  a [[product type]], which semantically is the [[product]] $A \times B \in \mathcal{C}$. The horizontal line itself is to indicate that if we are given the (symbols of) the collection of judgments on top, then we are entitled to also obtain the judgment on the bottom.

**Remark (Computation)** All this may seem, on first sight, like being a lot of fuss about something of grandiose banality. To see what is gradually being accomplished here despite of this appearance, as we proceed in this discussion, the reader can and should think of this as the first steps in the definition of a [[programming language]]: the notiuon of judgment is a syntactic rules for strings of symbols that a computer is to read in, and a [[natural deduction]]-step as the [[type formation rule]] above is an operation that this computer validates as being an allowed step of transforming a memory state with a given collection of such strings into a new memory state to which the string below the horizontal line is added. As we add the remaining rules below, what looks like a grandiose banality so far will remain grandiose, but no longer be a banality. The reader feeling in need of more motativational remarks along these lines might want to take a break here and have a look at the entry _[[computational trinitarianism]]_ first, that provides more pointers to the grandiose picture which we are approaching here.

Next, the second [[natural deduction]] rule for [[product types]] is the

**2. [[term elimination rule]]**. The fact that $A \times B \in \mathcal{C}$ is equipped with two [[projection]] [[morphisms]] 

$$
  \array{
    A \stackrel{p_1}{\leftarrow} A \times B \stackrel{p_2}{\to} B
  }
$$ 

means that from every [[element]] $t$ of $A \times B$ we may deduce the existence of [[elements]] $p_1(t)$ and $p_2(t)$ of $A$ and $B$, respectively. We declare now that this is the [[categorical semantics]] of which the [[natural deduction]] [[syntax]] is:

$$
  \frac{\vdash \; t \colon A \times B}{\vdash \; p_1(t) \colon A}
  \;\;\;\;\;\;\;\;\;
  \frac{\vdash \; t \colon A \times B}{\vdash \; p_2(t) \colon B}
  \,.
$$

As before, this is to say that if syntactically we are given strings of symbols expressing [[judgments]] as on the top of these horizontal lines, then we may "[[natural deduction|naturally deduce]]" also the judgment of the string of symbols on the bottom of this line.

**3. [[term introduction rule]]**. The first part of the [[universal property]] of the [[product]] in [[category theory]] is that for  $Q \in \mathcal{C}$ any other [[object]] equipped with morphisms 

$$
  \array{
    && Q
    \\
    & {}^{\mathllap{a}}\swarrow && \searrow^{\mathrlap{b}}
    \\
    A  && &&  B
  }
$$ 

in $\mathcal{C}$, we obtain a canonical morphism 

$$
  Q \to A \times B
$$ 

in $\mathcal{C}$. This is now declared to be the [[categorical semantics]] of which the [[natural deduction]] [[syntax]] is

$$
  \frac{
    \vdash\; a \colon A \;\;\;\;\;\; \vdash\; b \colon B
  }{
   \vdash (a,b) \colon A \times B
  }
  \,.
$$

With the [[elements]] that are the [[semantics]] of the terms appearing here made explicit, this is the syntax for a [[diagram]]

$$
  \array{
     && Q
     \\
     & {}^{\mathllap{a}}\swarrow &\downarrow^{\mathrlap{(a,b)}}& \searrow^{\mathrlap{b}}
     \\
     A && A \times B && B
  }
  \,.
$$


**4. [[computation rule]]**. The next part of the [[universal property]] of the [[product]] in [[category theory]] is that the resulting [[diagram]]

$$
  \array{
    && Q
    \\ 
    & {}^{\mathllap{a}}\swarrow &\downarrow& \searrow^{\mathrlap{b}}
    \\
    A &\stackrel{p_1}{\leftarrow}& A \times B & \stackrel{p_2}{\to} & B
  }
$$

is in fact a _[[commuting diagram]]_. Syntactically this is, clearly, the rule that the following identifications of strings of symbols are to be enforced

$$
  p_1(a,b) = a \;\;\;\;\;\; p_2(a,b) = b
  \,. 
$$

This concluces the description of the [[natural deduction]] about [[objects]], [[morphisms]] and [[products]] in a [[category]] using its [[type theory]] [[syntax]]. In the [next section](#SmoothSpaces) we promote our running example category $\mathcal{C}$, which admits only very few [[universal constructions]] (just [[products]]), to a richer category, the [[sheaf topos]] over it. That richer category then accordingly comes with a richer [[syntax]] of [[natural deduction]] inside it, namely with full [[dependent type theory]]. This we discuss in the [Syn Layer below](#SmoothSpacesLayerSyn).


## Smooth spaces
 {#SmoothSpaces}

### Layer Mod

* [[smooth space]] = [[type|thing]] into which we can throw [[coordinate systems]] ([[motivation for sheaves, cohomology and higher stacks|conceptual exposition]])

  [[functor]] $X : CartSp^{op} \to Set$ such that coordinate patches glue

* [[smooth manifold]] = [[smooth space]] that is [[covering|locally]] _[[equivalence|equivalent]]_ to a [[coordinate system]]

* [[diffeological space]] = [[smooth space]] such that every coordinate labels a [[point]] in the space (which need not be in a general smooth space)

$\{$[[coordinate systems]]$\}$ 
 $\hookrightarrow$
$\{$[[smooth manifolds]]$\}$ 
 $\hookrightarrow$
$\{$[[diffeological spaces]]$\}$ 
 $\hookrightarrow$
$\{$[[smooth spaces]]$\}$ 
 $\hookrightarrow$
$\{$[[smooth groupoids]]$\}$ 
 $\hookrightarrow \cdots $

[[mapping spaces]]: for $\Sigma, X$ [[smooth spaces]], the [[mapping space]] $[\Sigma,X]$ is defined as the [[smooth space]] whose $U$-[[coordinate charts]] are $\mathbf{H}(\Sigma \times U ,X)$.


Example: [[smooth loop space]] $L X = [S^1, X]$ (on the horizon: [[path integral]])

### Layer Sem
 {#SmoothSpacesLayerSem}

[[sheaf topos]]

[[slice topos]]

[[subobject classifier]]

### Layer Syn
 {#SmoothSpacesLayerSyn}

[[dependent type theory]] $\leftrightarrow$ [[locally cartesian closed category]]

[[type of propositions]] $\leftrightarrow$ [[subobject classifier]]

## Differential forms

* [[smooth function]] on [[coordinate system]] = [[smooth function]] $\mathbb{R}^n \to \mathbb{R}$

* [[smooth function]] on [[smooth space]] $X$ = one smooth function $f|_U$ on each [[coordinate chart]] $U \to X$ such that they fit together under [[coordinate transformation|change of coordinates]]

then

* [[differential form|differential 1-form]] on [[coordinate system]] $\mathbb{R}^n$ = $n$ smooth functions $\{f_i\}_{i = 1}^n$, written $\omega = f_1 \mathbf{d}x^1 + f_2 \mathbf{d}x^2 + \cdots + f_n \mathbf{d}x^n$

  ([[infinitesimal space|infinitsimal]] [[measure]] of [[length]])

* [[differential form|differential 1-form]] on [[smooth space]] $X$ = one $\omega|_U$ for each [[coordinate chart]] $U \to X$ such that these fit together under [[coordinate transformation|change of coordinates]]. 

then

* [[differential form]] on [[coordinate system]] $\mathbb{R}^n$ = element of [[exterior algebra]]...

the smooth space of differential $n$-forms is $\Omega^n(-)$


the [[Yoneda lemma]]: $\Omega^n(\mathbb{R}^n) = \{\mathbb{R}^n \to \Omega^n(-)\}$

observe: $\Omega^0(-) = \mathbb{R}$


## Differentiation

* [[derivative]]

* [[de Rham differential]]: map of smooth spaces $\mathbf{d} : \Omega^n(-) \to \Omega^{n+1}(-)$

for instance [[electromagnetic potential]]

$$
  A = \phi \mathbf{d}t + A_1 \mathbf{d}x^1 + A_2 \mathbf{d}x^2 + A_3 \mathbf{d}x^3
$$

then [[field strength]] is

$$
  F 
    \coloneqq
  \mathbf{d}A 
    = 
   E_1 \mathbf{d}t \wedge \mathbf{d}x^1 
    + 
   E_2 \mathbf{d}t \wedge \mathbf{d}x^2 
    + 
   E_3 \mathbf{d}t \wedge \mathbf{d}x^3
    + 
    B_1 \mathbf{d}x^2 \wedge \mathbf{d}x^3 
    + 
    B_2 \mathbf{d}x^3 \wedge \mathbf{d}x^1 
    + 
    B_3 \mathbf{d}x^1 \wedge \mathbf{d}x^2 
$$

with 

$$
  E_i = \frac{\partial \phi}{\partial x^i}
$$

and

$$
  B_1 = \frac{\partial A_2}{\partial x^3} - \frac{\partial A_3}{\partial x^2}
$$

etc

for

$$
  A,A' : X \to \Omega^1(-)
$$

a [[gauge transformation]] $A \to A'$
is $\lambda : X \to \mathbb{R}$ with

$$
  A' = A + \mathbf{d} \lambda
$$




first 2 of 4 [[Maxwell equations]]: $\mathbf{d} F = 0$

(the other 2 below in Riemannian geometry)

## Variational calculus

for instance [[variational calculus]]

[[action functional]] for [[particle]] on [[spacetime]] $X$ ("[[sigma-model]]")

$$
  S : [S^1, X] \to \mathbb{R}
$$

variation is

$$
  \mathbf{d}S : [S^1, X] \stackrel{S}{\to} \mathbb{R}
  \stackrel{\mathbf{d}}{\to}
  \Omega^1(-)
$$

* [[Euler-Lagrange equations]]

## Smooth groupoids

$$
  X_1 \stackrel{\overset{d_1}{\to}}{\stackrel{\overset{s_0}{\leftarrow}}{\underset{d_0}{\to}}}
  X_0
$$

$$
  \array{
    && X^{\Delta^2}
    \\
    &{}^{\mathllap{\exists}}\nearrow & \downarrow
    \\
    U &\stackrel{}{\to}& X^{\Lambda^2_i}
  }
$$

Example: $X$ a [[smooth space]] and $G$ a [[smooth group]] and 

$\rho : X \times G \to X$ an [[action]] then

[[action groupoid]]

$$
  X \sslash G = 
  \left(
    X \times G \stackrel{\overset{\rho}{\to}}{\underset{p_1}{\to}}
    X
  \right)
$$

## Principal bundles

any [[Lie group]] $G$ induces its [[delooping]] [[Lie groupoid]] 
  
$$
  \mathbf{B}G
  =
  * \sslash G
  = 
  \left(
     G \stackrel{\to}{\to} * 
  \right)
  \,.
$$

also

$$
  \mathbf{E}G
  =
  G \sslash G
  = 
  \left(
     G\times G \stackrel{\overset{\cdot}{\to}}{\underset{p_1}{\to}} G 
  \right)
  \,.
$$

canonical map

$$
  \array{
    \mathbf{E}G
    \\
    \downarrow
    \\
    \mathbf{B}G
  }
$$

[[universal principal bundle]]

for $X$ a [[smooth space]] a $G$-[[principal bundle]] over $X$ is a smooth space $P$ with map $P \to X$ such that there is a diagram 

$$
  \array{ 
     P &\stackrel{\simeq}{\leftarrow}& \tilde P &\to& \mathbf{E}G
     \\
     \downarrow && \downarrow &pb& \downarrow
     \\
     X &\stackrel{\simeq}{\leftarrow}& \tilde X &\underset{g}{\to}& \mathbf{B}G
  }
$$

where the left horizontal morphisms are [[weak equivalences]]
and the right square is a [[pullback]]

## Smooth manifolds


A [[smooth manifold]] of [[dimension]] $n$ 

a [[smooth space]] with an [[atlas]] 

$$
  \{ \mathbb{R}^n \underoverset{\simeq}{\phi_i^{-1}}{\to} U_i \hookrightarrow X\}
$$ 

of [[coordinate charts]]. On each overlap $U_i \cap U_j$ of two charts, the [[partial derivatives]] of the corresponding [[coordinate transformations]]

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

* $X$ itself is a [[Lie groupoid]] $(X \stackrel{\to}{\to} X)$ with trivial morphism structure;

* from the atlas $\{U_i \to X\}$ we get the corresponding [[Cech groupoid]] 
  $$
    C(\{U_i\}) = 
    (\coprod_{i, j} U_i \cap U_j \stackrel{\to}{\to} \coprod_i U_i)
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



## Tangent bundle


The above situation is neatly encoded in the existence of a [[diagram]] of Lie groupoids of the form

$$
  \array{
     C(\{U_i\}) &\stackrel{\lambda}{\to}& \mathbf{B} GL(n).
     \\
     {}^{\mathllap{\simeq}}\downarrow
     \\
     X
  }
  \,,
$$

where

* the left morphism is [[stalk]]-wise (around small enough [[neighbourhoods]] of each point) an [[equivalence of groupoids]] (we make this more precise in a moment);

* the horizontal functor has as components the functions $\lambda_{i j}$ and its functoriality is the cocycle condition $\lambda_{i j} \cdot \lambda_{j k} = \lambda_{i k}$.


A [[natural transformation|transformation]] of smooth functors $\lambda_1 \Rightarrow \lambda_2 : C(\{U_i\}) \to \mathbf{B} GL(n)$ is precisely a [[coboundary]] between two such cocycles.

## $G$-Structure

$$
  \mathbf{B}G \to \mathbf{B}K
$$

given a $K$-[[principal bundle]]

$$
  \array{
    \tilde X &\to &\mathbf{B}K
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

a [[reduction of the structure group]] along $G \to K$ is

$$
  \array{
    \tilde X &&\to&& \mathbf{B}G
    \\
    & \searrow &\swArrow_{e}& \swarrow
    \\
    && \mathbf{B}K
  }
$$


## Riemannian geometry

[[reduction of the structure group]] along

$\mathbf{B}O(n) \to \mathbf{B}GL(n)$

$$
  \array{
    \tilde X &&\to&& \mathbf{B}O(n)
    \\
    & {}_{\mathllap{\vdash T \Sigma}}\searrow &\swArrow_{e}& \swarrow
    \\
    && \mathbf{B}GL(n)
  }
$$

$e$ is [[vielbein]]: definition of an [[orthonormal frame]]
at each point

example: the other 2 [[Maxwell equations]]: $\mathbf{d} \star F = j_{el}$.

[[Einstein-Maxwell theory]]

## Integration 

$\Sigma$ [[compact topological space|compact]] [[orientation|oriented]] [[smooth manifold]] of [[dimension]] $k$

[[integration of differential forms]] is map of smooth spaces

$$
  \int_{\Sigma} : [\Sigma, \Omega^n(-)] \to \Omega^{n-k}(-)
$$

over a [[coordinate chart]] $U$ this sends

$$
  \int_{\Sigma, U} : \Omega^n(\Sigma\times U) \to \Omega^{n-k}(U)
  \,.
$$

## Transgression

[[transgression]] of [[differential forms]] to [[mapping space]] is the composite

$$
  \int_\Sigma [\Sigma,-]
  : 
  \Omega^n(X) \to \Omega^{n-k}([\Sigma,X])
$$

$$
  (X \stackrel{\omega}{\to} \Omega^n(-)) \in \Omega^n(X)
$$

to

$$
  \int_{\Sigma} [\Sigma,\omega]
   :
  [\Sigma, X] \stackrel{[\Sigma, \omega]}{\to}  \Omega^{n-k}(-)
$$

for instance [[action functional]] for [[electron]] in [[electromagnetic field]] $A$ is $S_{em} = \int_{S^1} [S^1, A]$

$$
  \int_{S^1} [S^1, A]
  : 
  [S^1, X]
    \stackrel{[S^1, A]}{\to}
  [S^1 , \Omega^1]
    \stackrel{\int_{S^1}}{\to}
  \Omega^0(-)
  = 
  \mathbb{R}
$$

variation gives [[Lorentz force]]


* [[Stokes theorem]]




## Circle-principal connections

[[Dirac charge quantization]] says that the
[[electromagnetic field]] is only locally in general a map

$$
  \array{
    && \Omega^1(-)
    \\
    & {}^{\mathllap{A}}\nearrow & \downarrow^{\mathrlap{\mathbf{d}}}
    \\
    X &\stackrel{\omega}{\to}& \Omega^2_{cl}
  }
$$

globally it is instead a map

$$
  \array{
    && \mathbf{B}U(1)_{conn}
    \\
    & {}^{\nabla}\nearrow & \downarrow^{F_{(-)}}
    \\
    X &\stackrel{\omega}{\to}& \Omega^2_{cl}
  }
$$

where

$$
  \array{  
    \mathbf{B}U(1)_{conn} &\stackrel{F_{(-)}}{\to}& \Omega^2_{cl}
    \\
    \downarrow &pb& \downarrow
    \\
    \mathbf{B}U(1)_{diff} &\to& \Omega^{1 \leq \bullet \leq 2}_{cl}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}U(1)
  }
$$

[[circle bundle with connection]]

the [[smooth groupoid]] is

$$
  \mathbf{B}U(1)_{conn}
  =
  \Omega^1(-) \sslash U(1)
$$

quotient of $\Omega^1(-)$ by $U(1)$-[[gauge transformations]]

for

$$
  A,A' : X \to \Omega^1(-)
$$

a [[gauge transformation]] $A \to A'$
is $\lambda : X \to U(1)$ with

$$
  A' = A + \mathbf{d} log \lambda
$$

## Smooth $n$-groupoids

* [[groupoid]]

[[smooth infinity-groupoid|smooth n-groupoid]]

* [[Dold-Kan correspondence]]


## First Chern class

* [[magnetic charge]], [[first Chern class]]

$$
  \array{
    && && \mathbf{B}(\mathbb{R}\sslash \mathbb{Z})
    &\to& \mathbf{B}^2 \mathbb{Z}
    \\
    && && \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}\mathbb{Z} 
      &\to&  
    \mathbf{B}\mathbb{R} 
      &\to&  
    \mathbf{B}U(1)
  }
$$

$$
  \mathbf{c}_1
   :
  \pi_0\mathbf{H}(X,\mathbf{B}U(1))
  \to 
  \pi_0 \mathbf{H}(X, \mathbf{B}^2 \mathbb{Z})
  \simeq
  H^2(X, \mathbb{Z})
$$

## Circle-principal $n$-connection

* [[Deligne complex]]

* [[circle n-bundle with connection]] $\mathbf{B}^n U(1)_{conn}$

* [[fiber integration in ordinary differential cohomology]]

  $$
    \exp(2 \pi i \int_\Sigma(-)) 
     :
    [\Sigma, \mathbf{B}^n U(1)_{conn}]
    \to 
    \mathbf{B}^{n-k}U(1)_{conn}
  $$

## Abelian Chern-Simons theory

* [[higher dimensional Chern-Simons theory]]

* [[cup-product in ordinary differential cohomology]]

$$
  \cup_{conn}
  :
  \mathbf{B}U(1)_{conn}
  \to 
  \mathbf{B}^3 U(1)_{conn}
$$

$$
  \exp(2 \pi i \int_{\Sigma}[\Sigma, \cup_\conn])
   : 
  [\Sigma, \mathbf{B}U(1)_{conn}]
   \stackrel{[\Sigma, \cup_{conn}]}{\to}
  [\Sigma, \mathbf{B}^3 U(1)_{conn}]
   \stackrel{\exp(2 \pi i \int_\Sigma (-))}{\to}
  U(1)
$$

## Principal connections

* [[connection on a bundle]] $\mathbf{B}G_{conn}$

* [[Yang-Mills theory]]

## Associated bundle

* [[action]]

  $$
    \array{
      V &\to& V\sslash G
      \\
      && \downarrow
      \\
      && \mathbf{B}G
    }
  $$

* [[associated bundle]]

$$
  \array{
    E &\to& V\sslash G
    \\
    \downarrow &pb& \downarrow
    \\
    \tilde X &\to& \mathbf{B}G
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

* [[section]]

$$
  \array{
    X &&\stackrel{\sigma}{\to}&& V \sslash G
    \\
    & \searrow &\swArrow_{\simeq}& \swarrow
    \\
    && \mathbf{B}G
  }
$$

## Spin geometry

* [[spin group]]

* [[spin representation]]

$$
  \array{
    V &\to& V \sslash Spin
    \\
    && \downarrow
    \\
    && \mathbf{B}Spin
  }
$$

* [[spinor bundle]]

* [[spinor]]

$$
  \array{
    X &&\stackrel{\psi}{\to}&& V \sslash Spin
    \\
    & \searrow &\swArrow& \swarrow
    \\
    && \mathbf{B}Spin
  }
$$

## Covariant derivative

* [[covariant derivative]]

$$
  \array{
     (V\sslash G)_{conn}
     \\
     \downarrow
     \\
     \mathbf{B}G_{conn}
  }
$$

$$
  \array{
    \tilde X &&\stackrel{(\sigma, \nabla \sigma)}{\to}&& (V \sslash G)_{conn}
    \\
    & \searrow &\swArrow& \swarrow
    \\
    && \mathbf{B}G_{conn}
  }
$$

## Einstein-Yang-Mills theory

* [[Einstein-Yang-Mills theory]]

* [[standard model of particle physics]]

* [[standard model of cosmology]]

## Symplectic geometry

* [[symplectic geometry]]

## Geometric quantization
 {#GeometricQuantization}

* [[geometric quantization]]

## Supergeometric coordinate systems
 {#SupergeometricCoordinateSystems}

### Layer Mod

The premise in [The continuum real world line](#TheContinuumRealWorldLine) is now refined to

**Premise.** The abstract worldline of a [[fermionic particle]] is a $\mathbb{Z}_2$-[[odd line|graded]] [[formal manifold|formal neighbourhood]] $\mathbb{R}^{1|n}$ of the [[real line]], for some $n \in \mathbb{N}$.

For $n = 0$ this is again the real line $\mathbb{R}^{1|0} = \mathbb{R}$.


* [[fermion]]

* [[supermanifold]]

### Layer Sem

* [[super infinity-groupoid]]

* [[smooth super infinity-groupoid]]

### Layer Syn

## References

A textbooks with basic introductions to [[differential geometry]] and [[physics]] is

* [[Theodore Frankel]], _[[The Geometry of Physics - An Introduction]]_
 {#Frankel}

A discussion with emphasis on the kind of tools that we are using here is in 

* [[Frédéric Paugam]], _Towards the mathematics of quantum field theory_ ([pdf](http://people.math.jussieu.fr/~fpaugam/documents/enseignement/master-mathematical-physics.pdf))

An introductory discussion with much overlap with the above discussion is in section "1.3 Introduction -- Models and applications" of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

Another introductory discussion along the above lines of aspects in [[gravity]] and [[higher gauge theory]] motivated from [[string theory]] is in 

* [[Urs Schreiber]], _[[twisted smooth cohomology in string theory]]_, ESI (2012)

