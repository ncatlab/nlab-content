
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

# Measurable spaces
* table of contents
{: toc}

## Idea

Measurable spaces are the traditional prelude to the general theory of [[measure]] and [[integration]].  Basically, a measure is a recipe for computing the size --- e.g., length, area, volume --- of [[subsets]] of a given [[set]] $X$.  The structure of a 'measurable space' picks out those subsets of $X$ for which the size is well-defined; these subsets are called 'measurable'.  The measure on $X$ is then an operation that assigns a number to each measurable subset saying how big it is.

In short: you get a [[measure space]] by placing a measure on a measurable space.

Ideally, all subsets would be measurable, but this contradicts the [[axiom of choice]] for the basic example of [[Lebesgue measure]] on the [[real line]].  Although it is possible to use nonstandard [[foundations]] of mathematics in which all subsets of the real line are Lebesgue measurable, any general theory that includes that example and is more general than those foundations requires some explicit notion of measurable space (or an alternative such as a [[measurable locale]]).

In any case, measurable spaces are of some interest in their own right, even without a measure on them.


## Definitions

We give first the usual notion, assuming the validity of [[excluded middle]] and [[power sets]]; see below for alternative versions, including the [[constructive mathematics|constructive]] and [[predicative mathematics|predicative]] theories.

Given a [[set]] $X$, a __$\sigma$-[[sigma-algebra|algebra]]__ is a collection of [[subsets]] of $X$ that is closed under [[complement|complementation]], [[countable set|countable]] [[unions]], and countable [[intersections]].  A __measurable space__, by the usual modern definition, is a set $X$ equipped with a $\sigma$-algebra $\Sigma$.  The elements of $\Sigma$ are called the __[[measurable sets]]__ of $X$ (or more properly, the measurable subsets of $(X,\Sigma)$).

Given measurable spaces $X$ and $Y$, a __[[measurable function]]__ from $X$ to $Y$ is a [[function]] $f\colon X \to Y$ such that the [[preimage]] $f^*(T)$ is measurable in $X$ whenever $T$ is measurable in $Y$.  Measurable spaces and measurable functions form a [[category]] [[Meas]], which is [[topological concrete category|topological]] over [[Set]].

In classical measure theory, it is usually assumed that $Y$ is the [[real line]] (or a variation) equipped with the [[Borel sets]] (see the examples below).  Then $f$ is measurable if and only if $f^{-1}(I)$ is measurable whenever $I \subseteq Y$ is an interval.


## Variations

We will briefly examine variations of the notion of measurable space, from those most like the standard to those most unlike it.  Most of these are discussed at articles dedicated to them.

Historically, people have used more general notions that $\sigma$-algebras, such as algebras, $\delta$-rings, and similar concepts whose names you can probably now guess; these are all discussed at [[sigma-algebra]].  These are all more general than $\sigma$-algebras, being possibly not closed under some operations.  When using some of these more general rings of measurable sets, it is necessary to allow [[partial functions]] whose domain is a [[relatively measurable set]] as measurable functions; for details, see [[measurable function]].

It is often convenient if a measurable space has, in addition to the $\sigma$-algebra of measurable sets, a $\sigma$-[[sigma-ideal|ideal]] of __measurable [[null sets]]__.  That is, besides the set $X$ and the $\sigma$-alebra $\Sigma$, we have a collection $N \subseteq \Sigma$ that is closed under [[countable set|countable]] unions and taking subsets (within $\Sigma$).  (The elements of $N$ are the *measurable* null sets; a __[[null set]]__ is *any* subset of a measurable null set.)  One can equivalently specify a $\delta$-[[delta-filter|filter]] of __measurable [[full sets]]__; the full sets are the [[complements]] of the null sets.  Either way, this allows us to use almost measurable [[almost functions]] up to [[almost equality]], as described at [[measurable function]].

In [[constructive mathematics]], because [[complement|complementation]] doesn\'t behave nicely, the concept of $\sigma$-algebra is not so useful.  It\'s also essential to use [[almost functions]] to avoid a paucity of measurable functions.  One solution, due to [[Henry Cheng]], may be found at [[Cheng measurable space]]; briefly, we use [[disjoint pairs]] $(A,B)$ of sets instead of individual measurable sets and use formal complements in the algebra, as well as a notion of [[full sets]].  Assuming [[excluded middle]], a Cheng measurable space is actually equivalent to a measurable space equipped with null (or full) sets, as in the previous paragraph.

In order to have the most important theorems of [[measure theory]], it is necessary and sufficient to restrict to [[localizable measures]].  Since localizability refers only to the null (or full) sets, we can actually speak of a __[[localizable measurable space]]__: a measurable space equipped with null (or full) sets as above, with the property that the [[boolean algebra]] of measurable sets [[quotient algebra|modulo]] the null sets is [[complete lattice|complete]].

Another approach to measure theory, more abstract, is to ignore the set $X$ and use *only* the $\sigma$-algebra $\Sigma$, as an abstract [[boolean algebra]] equipped with [[countable set|countable]] [[suprema]]; this is called a __[[measurable algebra]]__ (or a [[measure algebra]] when equipped with a [[measure]]).  A measurable algebra might also can be equipped with a $\sigma$-ideal of null sets (or a $\delta$-filter of full sets), but really it is simpler to take the [[quotient algebra]], which is itself a perfectly good measurable algebra.  Even if a measurable algebra is a [[complete lattice]], it can still be pathological; but if it has enough [[normal measure]]s, then we have a __[[measurable locale]]__; the [[category]] of measurable locales is [[equivalence of categories|equivalent]] to that of [[localizable measurable spaces]] (from the previous paragraph).

Yet another category equivalent to localizable measurable spaces and measurable locales is the [[opposite category]] of the category of [[commutative ring|commutative]] [[von Neumann algebras]]; this is really a version of the [[Gelfand–Neumark theorem]].  Then a *[[noncommutative geometry|noncommutative]]* (localizable) measurable space is (the formal dual of) *any* von Neumann algebra.  In this way, measure theory may be seen as a branch of [[operator algebra]] theory (at least if one assumes that only localizable measurable spaces are well enough behaved to be worthy of study).


## Examples

*  Of course, the [[power set]] of $X$ is closed under all operations, so it is a $\sigma$-algebra.  Thus every set becomes a __[[discrete space|discrete]] measurable space__.


*  If $X$ is a [[topological space]], then the $\sigma$-algebra generated by the open sets (or equivalently, by the closed sets) in $X$ is the __Borel $\sigma$-algebra__; its elements are called the __[[Borel sets]]__ of $X$. In particular, the Borel sets of [[real number]]s are the Borel sets in the [[real line]] with its usual topology.


*  If a measurable space $(X,\Sigma)$ is equipped with a measure $\mu$, making it into a [[measure space]], then the sets of measure zero form a $\sigma$-[[sigma-ideal|ideal]] of $\Sigma$ (that is an [[ideal]] that is also a sub-$\sigma$-ring).  Let a __[[null subset|null set]]__ be *any* set (measurable or not) contained in a set of measure zero; then the null sets form a $\sigma$-ideal in the [[power set]] of $X$.  Call a set __$\mu$-measurable__ if it is the union of a measurable set and a null set; then the $\mu$-measurable sets form a $\sigma$-algebra $\Sigma_\mu$ called the __completion__ of $\Sigma$ under $\mu$, and the measurable space $(X,\Sigma_\mu)$ is the __completion__ of $(X,\Sigma)$.

*  In particular, the __Lebesgue-measurable__ sets in the real line are the elements of the completion of the Borel $\sigma$-algebra under [[Lebesgue measure]].


## Properties

### Relation to von Neumann algebras
 {#RelationToVonNeumannAlgebras}

One version of the [[Gelfand-Naimark theorem|Gel'fand–Naimark theorem]] states that the category of [[commutative algebra|commutative]] $W^*$-[[W*-algebra|algebras]] is [[dual equivalence|dual]] to the category of *localizable* measurable spaces.  (As such, arbitrary $W^*$-algebras may be interpreted as 'noncommutative' measurable spaces in a sense analogous to [[noncommutative geometry]].)  See the [references below](#ReferencesRelationToVonNeumannAlgebras).

To make this work correctly, we cannot simply define localizability as a [[property]] of measurable spaces; instead, a __[[localizable measurable space]]__ is a measurable space (a set $X$ with a $\sigma$-algebra $\Sigma$) with a $\sigma$-[[sigma-ideal|ideal]] $\mathcal{N}$ of $\Sigma$ and $\mathcal{P}X$ simultaneously (called the ideal of __[[null sets]]__) such that $\Sigma/\mathcal{N}$ is a [[complete lattice]]; and a [[morphism]] of localizable measurable spaces is a measurable function, with the property that the [[preimage]] of any null set is null, up to an [[equivalence relation]] where $f \cong g$ if $\{ x \;|\; f(x) \neq g(x) \}$ is a null set.

The requirement that $\Sigma/\mathcal{N}$ be complete is the real localizability condition here; the trick of equipping a measurable space with a $\sigma$-ideal of null sets (or equivalently a $\sigma$-[[filter]] of [[full sets]]) and taking measurable functions only up to equivalence is a common one in other situations.

Localizable measurable spaces can also be studied via the lattice $\Sigma/\mathcal{N}$, which is a [[frame]]; the morphisms correspond to certain [[continuous maps]] between [[locales]], and thus we are studying locales with [[extra structure]], called __[[measurable locales]]__.


### Relation to Boolean toposes

In terms of [[topos theory]], measured spaces are closely related to [[Boolean toposes]] (e.g. [Jackson 06](#Jackson06), [Henry 14](#Henry14)).

## In alternative foundations

While Lebesgue measure on $\mathbb{R}^n$ can be done in very weak [[foundations]], a general theory of measure and measurable spaces seems to require powerful [[set theory|set-theoretic]] machinery.  Indeed, not much seems to be possible in [[predicative mathematics|predicative]] contexts, and the (nonpredicative) [[constructive mathematics|constructive]] theory is noticeably more complicated than the classical theory.  On the other hand, the classical theory has its own complications, with nonmeasurable sets and functions that can be proved to exist but which seem to never arise in practice.  Instead, there are classically false but apparently consistent foundations in which measure theory is extremely simple.


### Predicative theory
{#Predicative}

The main problem for measure theory in [[predicative mathematics]] is getting your hands on a $\sigma$-algebra.  Once you\'ve got that, you\'ve got a measurable space (obviously) and go on to [[measure space]], where there are no new difficulties.  However, what is (say) a Borel set in the real line?  This is difficult, if not impossible, to explain predicatively.  (In the case of [[Lebesgue measure]], there *are* ways to describe the Lebesgue-measurable sets predicatively, but these do not seem to generalise to a broader theory.)

Note that there is no real problem in describing what, say, an open set is.  Not only can this be done for the real line in the usual $\epsilon$-$\delta$ way, but it is easy to take *any* collection of subsets of any set $X$, call that collection a [[subbase]], and describe which sets are the open sets in the [[topological space|topology]] generated by that subbase.  The reason is that there are only two steps in moving from a subbase to a topology, and while the latter step is too impredicative to allow one to speak of the *set* of all open sets, it\'s OK if you only want to talk about *individual* open sets.  (To be explicit: given a collection $B$ to be used as subbase, a set $G$ is _open_ if, for every point $x$, if $x \in G$, then there exist a [[natural number]] $n$ and elements $A_1, \ldots, A_n$ of $B$ such that $x \in A_i$ for each $i$ and, for every point $y$, if $y \in A_i$ for each $i$, then $y \in G$.  Since we quantify only over points and natural numbers, not over sets or functions, this is a predicative definition, and it\'s easy to prove that the open sets satisfy the axioms of a topology.)

This cannot be done with $\sigma$-algebras, since we need uncountably many sets.  To be sure, each individual step is predicative, and we can freely talk about $G_\delta$ sets and the like, but to define a Borel set we need to quantify over all countable ordinals.  While it is possible to hypothesise the existence of an uncountable ordinal $\omega_1$ and be predicative 'over' $\omega_1$ (and after all, everything else in this section is only predicative over the first infinite ordinal $\omega_0$, which we only have if we accept an [[axiom of infinity]]), this cannot be constructed predicatively.  (The immediate definition of $\omega_1$ as the [[Hartog's number]] of $\omega_0$ uses [[power set]]s; while the construction of an uncountable ordinal by applying the [[well-ordering theorem]] to the [[function set]] $\mathbf{N}^{\mathbf{N}}$ doesn\'t seem to use reasoning that requires the existence of power sets as long as you don\'t also throw in [[excluded middle]], it does use reasoning that is not accepted by any predicative school that I know.)

So as far as I ([[Toby Bartels]]) can tell, there is no general predicative theory of measurable spaces, only an ad hoc theory of Lebsegue measurability.  I would be delighted to learn otherwise!


### Constructive theory

From a constructive perspective, there are a couple of related problems with the classical theory.  One is that the notion of $\sigma$-algebra is highly suspicious, because it relies on an operation, [[complement]]ation, that behaves very differently in the [[intuitionistic logic]] that [[constructive mathematics]] uses.  The other is that, even you acept the definition of $\sigma$-algebra anyway (after all, the Lebesgue-measurable sets on the real line do still form one), there may be very few measurable functions.

Indeed, if we set aside the general theory of measurable spaces and simply do Lebesgue measure ad hoc in a constructive (even predicative) way, we find that instead of measurable [[functions]] we really want measurable [[partial functions]] whose domain of definition is a [[full set]].  This suggests that if we want to define the concept of measurable function, then we have to know what the full sets are.

There is a way out, due to [[Henry Cheng]], for both of these problems at once.  Instead of dealing with individual sets, we will deal with pairs of [[disjoint sets]].  The intuition is that we use disjoint pairs $(A,B)$ such that $A \cup B$ is full ---with $(A,\neg{A})$ being the motivating example in the classical theory---, but we let the $\sigma$-algebra itself tell us which pairs those are.  Once we fix a particular measure, we may find additional pairs whose union is full, somewhat like finding additional measurable sets when taking the completion in the classical theory (although taking the completion is a separate phenomenon here), but that\'s all right; the important thing is that each pair chosen really is full in any measure used (much as each set in a classical $\sigma$-algebra must actually be measurable by any measure used).

See details at [[Cheng space]].


### In dream mathematics

While measure theory only gets more complicated in constructive mathematics, it becomes much easier in [[dream mathematics]].

... more coming ...


## Related concepts

* [[measurable locale]]

* [[noncommutative measurable space]]

## References

### General

For Cheng\'s theory of measure spaces, see the 1985 edition of Bishop & Bridges, _Constructive Analysis_.  (And the references therein, obviously, but I haven\'t read those.)

### Relation to von Neumann algebra
 {#ReferencesRelationToVonNeumannAlgebras}

A discussion of the abstract properties of the category of localizable measurable spaces and its relation to [[von Neumann algebras]] is in 

* Alain Guichardet, _Sur la cat&#233;gorie des alg&#232;bres de von Neumann_  (French) Bull. Sci. Math. (2) 90 1966 41&#8211;64. ([MSN](http://ams.org/mathscinet-getitem?mr=201989)) ([scan](http://dmitripavlov.org/scans/guichardet.pdf))

A useful series of expositions along these lines is in

* [[Dmitri Pavlov]], _On measurable spaces_

  * [MO comment 1](http://mathoverflow.net/questions/20740/is-there-an-introduction-to-probability-theory-from-a-structuralist-categorical-p/20820#20820)

  * [MO comment 2](http://mathoverflow.net/questions/49426/is-there-a-category-structure-one-can-place-on-measure-spaces-so-that-category-th/49542#49542)

See also 

* Ryszard Pawe&#322; Kostecki, _$W^\ast$-algebras and noncommutative integration_ ([pdf](http://www.fuw.edu.pl/~kostecki/wstarint.pdf))

### Relation to Boolean toposes

* {#Jackson06} Matthew Jackson, _A sheaf-theoretic approach to measure theory_, 2006 ([pdf](http://www.andrew.cmu.edu/~awodey/students/jackson.pdf))

* {#Henry14} [[Simon Henry]], _From toposes to non-commutative geometry through the study of internal Hilbert spaces_, 2014  ([pdf](http://www.math.jussieu.fr/~henrys/Thesis.pdf))


+-- {: .query}

**Revision plan**

1.  Describe several variations of definition:
    *  with a filter of full sets,
    *  localizable,
    *  Cheng,
    *  from a delta-ring etc,
    *  localic,
    *  finitary,
    *  noncommutative.

2.  Do measurable functions only afterwards, stressing almost-everywhere equality.  Describe the relevant categories.

3.  Mention measure spaces and anything else.

=--


[[!redirects measurable space]]
[[!redirects measurable spaces]]

[[!redirects complete measurable space]]
[[!redirects complete measurable spaces]]
[[!redirects completion of a measurable space]]
[[!redirects completions of a measurable space]]
[[!redirects completions of measurable spaces]]