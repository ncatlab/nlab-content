
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

A _partial order_ on a set is a way of ordering its elements to say that some elements precede others, but allowing for the possibility that two elements may be incomparable without being the same.  This is the fundamental notion in [[order theory]].

By regarding the ordering $\leq$ as the existence of a unique [[morphism]], preorders may be regarded as certain [[categories]] (namely, [[thin categories]]).  This category is sometimes called the _order category_ associated to a partial order; see [below](#AsACategoryWithExtraProperties) for details.


## Definitions

### As a set with extra structure

A poset may be understood as a [[set]] with [[extra structure]].

Given a [[set]] $S$, a __partial order__ on $S$ is a (binary) [[relation]] $\leq$ with the following properties:

* [[reflexive relation|reflexivity]]: $x \leq x$ always;

* [[transitive relation|transitivity]]: if $x \leq y \leq z$, then $x \leq z$;

* [[antisymmetric relation|antisymmetry]]: if $x \leq y \leq x$, then $x = y$.

A __poset__ is a set equipped with a partial order.


### As a preorder with antisymmetry

A poset is precisely a [[proset]] satisfying the extra condition that 
$x \leq y \leq x$ implies that $x = y$. 

#### In dependent type theory

In [[dependent type theory]], the identity type $x = y$ representing equality is not necessarily valued in [[h-propositions]]. As a result, a naive translation of the set theoretic definition of a partial order from a preorder above doesn't work. Instead, one has to postulate an [[equivalence of types]] between the identity type $x = y$ and the condition $x \leq y \leq x$: 

A **partial order** is a preorder $X$ with an [[equivalence of types]] $\mathrm{antisym}(x, y):(x =_X y) \simeq (x \lt y) \times (y \lt x)$ for all $x:X$ and $y:X$. 

Equivalently, one could [[inductively define]] a function 

$$x:X, y:X \vdash \mathrm{idToOrd}(x, y):(x =_X y) \to (x \lt y) \times (y \lt x)$$

on reflexivity of the [[identity type]] by reflexivity of the preorder

$$\mathrm{idToSymCon}(x, x)(\mathrm{id}_X(x)) \coloneqq \mathrm{refl}_{\leq}(x)$$

Then, a partial order is a preorder such that the defined function $\mathrm{idToOrd}(x, y)$ is an [[equivalence of types]] for all $x:X$ and $y:X$.

$$\mathrm{antisym}:\prod_{x:X} \prod_{y:X} \mathrm{isEquiv}(\mathrm{idToOrd}(x, y))$$

In either case, since the preorder is valued in propositions, the antisymmetry axiom ensures that the partial order is an [[h-set]]. 

### As a category with extra properties 
 {#AsACategoryWithExtraProperties}

A poset [[relation between preorders and (0,1)-categories|may be understood]] as a [[category]] with [[extra property]], sometimes called its _order category_.

A __poset__ [[relation between preorders and (0,1)-categories|is]] a [[category]] such that:

* for any [[pair]] of [[objects]] $x, y$, there is at most one morphism from $x$ to $y$

* if there is a morphism from $x$ to $y$ and a morphism from $y$ to $x$ (which by the above implies that $x$ and $y$ are [[isomorphic]]), then $x = y$.

[[relation between preorders and (0,1)-categories|Equivalently]], this says that a poset is a [[skeletal category|skeletal]] [[thin category|thin]] category, or equivalently a skeletal [[category enriched]] over the [[cartesian monoidal category]] of [[truth values]] or equivalently a skeletal [[(0,1)-category]]. (See also at *[[enriched poset]]*).

When we do this, we are soon [[relation between preorders and (0,1)-categories|led to contemplate]] a slight generalization of partial orders: namely [[preorder|preorders]]. The reason is that the antisymmetry law, saying that $x \le y$ and $y \le x$ imply $x = y$, violates the [[principle of equivalence]] in a certain sense.  (On the other hand, it does not violate it if taken as a *definition* of [[equality]].)


### Monotone functions 

The morphisms of partially ordered sets are [[monotone functions]]; a __monotone function__ $f$ from a poset $S$ to a poset $T$ is a [[function]] from $S$ to $T$ (seen as [[structured sets]]) that preserves $\leq$:
$$ x \leq y \;\Rightarrow\; f(x) \leq f(y) .$$
Equivalently, it is a [[functor]] from $S$ to $T$ (seen as certain categories).

In this way, posets form a [[category]] [[Pos]].


### Intervals 

A (closed bounded) **[[interval]]** in a poset $C$ is a set of the form
$$[x,y] = \{r\in C|x\le r\le y\}.$$

A poset is **[[locally finite poset|locally finite]]** if every closed bounded interval is finite.


### Kinds of posets 

A poset with a [[top element]] and [[bottom element]] is called __bounded__.  (But note that a *[[subset]]* of a poset may be bounded without being a bounded as a poset in its own right.)  More generally, it is __bounded above__ if it is has a top element and __bounded below__ if it has a bottom element.

A poset with all finite [[meets]] and [[joins]] is called a __[[lattice]]__; if it has only one or the other, it is still a __[[semilattice]]__.

A poset in which every finite set has an upper bound (but perhaps not a *least* upper bound, that is a join) is a __[[directed set]]__.

As remarked above, a poset in which each interval $[x,y]$ is a [[finite set]] is called __locally finite__ or a __[[causet]]__.

A poset with a bounding [[countable set|countable subset]] is called __$\sigma$-bounded__.  That is, the poset is $\sigma$-bounded above if there exists a sequence $(x_n)_{n=1}^{N}$ (where $N$ is a natural number or infinity) such that for every $y$ in the poset there is an $x_m$ with $y \leq x_m$.  (The poset is $\sigma$-bounded below if we have $x_m \leq y$ instead.)  Note that every bounded poset is $\sigma$-bounded, but not conversely.  Note that some authorities require $N = \infty$; this makes a difference only for the empty poset (we say it is $\sigma$-bounded, they say it is not).


### In higher category theory 

A poset can be understood as a [[(0,1)-category]]. This suggests an obvious [[vertical categorification]] of the notion of poset to that of [[n-poset]].


## Properties

### Extension to linear order
 {#ExtensionToLinearOrder}

+-- {: .num_prop #LinearExtension}
###### Proposition

On a [[finite set]], every [[partial order]] may be 
[[linear extension of a partial order|extended]] to a [[linear order]].

For non-finite sets this still holds with the [[axiom of choice]].

=--

See at _[[linear extension of a partial order]]_ [this Prop.](linear+extension+of+a+partial+order#LinearExtensionOfAPartialOrder).


### Locales from posets -- Alexandroff topology
{#LocalesFromPosets}

+-- {: .num_defn }
###### Definition

For $P$ a poset, write $Up(P)$ for the [[topological space]] whose underlying [[set]] is the underlying set of $P$ and whose [[open subset]]s are the _upward closed subsets_ of $P$: those subsets $U \subset P$ with the property that 

$$
  ((x \in U) and (x \leq y)) \Rightarrow (y \in U)
  \,.
$$ 

This is called the **[[Alexandroff topology]]** on $P$.

=--

+-- {: .num_prop #UpIfFFAndPreservesLimits}
###### Proposition

This construction naturally extends to a 
[[full and faithful functor]].

$Up : $ [[Poset]] $\to$ [[Top]] $\to$ [[Locale]].


=--

+-- {: .num_prop }
###### Proposition

For $P$ a poset, there is a [[natural equivalence]]

$$
  Sh(Up(P)) \simeq [P,Set]
$$

between the [[category of sheaves]] on the [[locale]] $Up(P)$ and the 
category of [[copresheaves]] on $P$.

=--

For more see [[Alexandroff topology]].


### Cauchy completion

Every poset is a [[Cauchy complete category]]. Posets are the Cauchy completions of [[prosets]]. ([Rosolini](#Rosolini))

### In univalent universes

In [[homotopy type theory]], every [[type]] with a partial order in a [[univalent universe]] is a poset. ([Tosun](#Tosun), [Ahrens, North, Shulman, Tsementzis](#ANST))

### Finite posets and Birkhoff duality
 {#OppositeCategory}

Let $FinPoset$ be the category of finite posets and order-preserving functions, and let $FinDistLat$ be the category of finite [[distributive lattices]] and lattice homomorphisms.  These are contravariantly equivalent, thanks to the presence of an [[ambimorphic object]]:

**Proposition.** The [[opposite category]] of $FinPoset$ is [[equivalence of categories|equivalent]] to $FinDistLat$:

$$
  FinPoset^{op} \simeq FinDistLat.
$$

One direction of this equivalence is given by the hom-functor

$$
  [-,2] \;\colon\; FinPoset^{op} \stackrel{\simeq}{\to} FinDistLat
$$

where $2 = \{0,1\}$ is the 2-element poset with $0 \lt 1$ and for any $Y \in \FinPoset$, $[Y,2]$ is the distributive lattice of poset morphisms from $Y$ to $2$. The other direction is given by 

$$
  [-,2] \;\colon\; FinDistLat^{op} \stackrel{\simeq}{\to} FinPoset
$$

where $2$ is the 2-element distributive lattice and for any $X \in  FinDistLat$, $[X,2]$ is the poset of distributive lattice morphisms from $X$ to $2$. 

This __Birkhoff duality__ is (in one form or another) mentioned in many places; the formulation in terms of hom-functors may be found in 

* [[Gavin C. Wraith]], _Using the generic interval_, Cah. Top. G&#233;om. Diff. Cat. **XXXIV** 4 (1993) pp.259-266. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1993__34_4/CTGDC_1993__34_4_259_0/CTGDC_1993__34_4_259_0.pdf))

The functorial nature of the correspondence means that morphisms of finite posets (i.e. order-preserving maps) naturally correspond to morphisms of finite distributive lattices (i.e. order-preserving maps that also respect meet and join).

It follows from Birkhoff's representation theorem that every finite distributive lattice can be seen as a lattice of sets (i.e. sets with join and meet given by union and intersection) -- in particular, sets whose elements are the join-irreducible elements of the lattice. Furthermore, a good intuition for why this duality holds is that either an element is generated as the join of existing elements, or it is join-irreducible. Hence given any existing poset, we can simply add all missing joins, and also a bottom (i.e. the nullary join). By general results (the adjoint functor theorem for posets) this suffices to ensure that all meets exist as well. This is analogous to the free colimit completion of a category, and indeed Birkhoff representation can be seen as a very special case of the Yoneda lemma as applied to (0,1)-category theory (i.e., order theory), since (0,1)-presheaves are functors into Bool rather than Set and hence correspond to [[lower set]]s.

Birkhoff duality does not hold for infinite posets. 

## Examples

* The [[function algebra]] of [[rational number|rational]]-valued [[functions]] on any [[set]] $X$ is a partial order. 

* The [[function algebra]] of [[Cauchy real number|Cauchy real]]-valued functions on $X$ is a partial order. In fact, it is the [[Cauchy completion]] of the function algebra of [[rational number|rational]]-valued [[functions]] on $X$. 

* More generally, if $A$ is a [[vector space]] on the [[rational numbers]] with a [[quadratic form]], then $A$ is a partial order, and its Cauchy completion is a vector space of same dimension on the [[Cauchy real numbers]] with a quadratic form. In particular, the Cauchy [[complex numbers]] and the [[Gaussian rationals]] are partial orders. 

* In a logic with implications, the set of propositions is partially ordered with respect to the implication as a relation.


## Related concepts

* [[relation between preorders and (0,1)-categories]]

* [[preorder]]

* [[continuous poset]]

* [[Noetherian poset]]

* [[enriched poset]]

* [[specialization topology]]

* [[prefix order]]

* [[partially ordered object]]

* [[Thomason model structure]]

* [[antithesis partial order]]

* [[involutive poset]]

## References

* Richard P. Stanley, Enumerative [[combinatorics]], vol I [pdf](http://www-math.mit.edu/~rstan/ec/ec1.pdf)

[[Cauchy completion]] of prosets and posets is discussed in 

* G. Rosolini, _A note on Cauchy completeness for preorders_ ([pdf](http://rivista.math.unipr.it/fulltext/1999-2s/06.pdf))
 {#Rosolini}

Here are some references on [[directed homotopy theory]]:

* [[Marco Grandis]], _Directed homotopy theory, I. The fundamental category_ ([arXiv](http://arxiv.org/abs/math.AT/0111048))

* [[Tim Porter]], _Enriched categories and models for spaces of evolving states_, Theoretical Computer Science, 405, (2008), pp. 88--100.

* [[Tim Porter]], _Enriched categories and models for spaces of dipaths. A discussion document and overview of some techniques_ ([pdf](http://drops.dagstuhl.de/opus/volltexte/2007/898/pdf/06341.PorterTimothy.Paper.898.pdf))

Posets in [[univalent universes]] in [[homotopy type theory]] are discussed in

* {#Tosun} Ayberk Tosun, Formal Topology in Univalent Foundations [pdf](https://odr.chalmers.se/handle/20.500.12380/301098)

* {#ANST} Benedikt Ahrens, Paige Randall North, Michael Shulman, Dimitris Tsementzis, The Univalence Principle ([abs:2102.06275](https://arxiv.org/abs/2102.06275))

On posets that are [[cofibrant objects]] in the Thomason model structure:

* [[Roman Bruckner]], [[Christoph Pegel]], _Cofibrant objects in the Thomason Model Structure_, &lbrack;[arXiv:0808.4108](http://arxiv.org/abs/1603.05448)&rbrack;

* [[Roman Bruckner]], *Abstract Homotopy Theory and the Thomason Model Structure*, PhD thesis, Bremen 2016 &lbrack;[gbv:46-00105527-15](http://nbn-resolving.de/urn:nbn:de:gbv:46-00105527-15), [pdf](https://media.suub.uni-bremen.de/bitstream/elib/1120/1/00105527-1.pdf)&rbrack;

On the [[Birkhoff duality]] between finite posets and finite [[distributive lattices]]

* {#Birkhoff37} [[Garrett Birkhoff]], *Rings of sets*. Duke Mathematical Journal, 3(3):443–454, 1937.

* {#Spitters16} [[Bas Spitters]], *Cubical sets and the topological topos* ([arXiv:1610.05270](https://arxiv.org/abs/1610.05270))

[[!redirects poset]]
[[!redirects posets]]
[[!redirects partial orders]]
[[!redirects partial ordering]]
[[!redirects partial orderings]]
[[!redirects partially ordered]]
[[!redirects partially ordered set]]
[[!redirects partially ordered sets]]
[[!redirects partially-ordered]]
[[!redirects partially-ordered set]]
[[!redirects partially-ordered sets]]

[[!redirects bounded poset]]
[[!redirects bounded posets]]

[[!redirects order category]]
[[!redirects order categories]]
[[!redirects poset category]]
[[!redirects poset categories]]