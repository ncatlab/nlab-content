
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

# Measurable locales
* table of contents
{: toc}

## Idea

Measurable locales are certain [[locales]], which may serve as a basis for [[measure theory]] much as general locales serve as a basis for [[topology]] (especially in [[constructive mathematics]]).  Specifically, a measurable locale is equivalent to a compact strictly [[localizable measurable space]] (or [[dual equivalence|dual]] to a commutative [[von Neumann algebra]]).

Ironically, in [[constructive mathematics]], measurable locales are *not* locales (except for the [[empty space]]), on pain of [[excluded middle]].

The concept is due to [[Dmitri Pavlov]].


## Definitions

At present, there is no purely [[order theory|order-theoretic]] definition of measurable locales.  However, there are a few other ways of defining them.


### In classical mathematics

First we give definitions appropriate for [[classical mathematics]].

As a preliminary step, consider the [[category]] $Comp Bool Alg_{sup}$ of [[complete boolean algebras]] and [[supremum]]-preserving [[homomorphisms]] of boolean algebras.  This is a [[full subcategory]] of the category $Frm$ of [[frames]] and so its [[opposite category]] $Comp Bool Alg_{sup}^{op}$ is a full subcategory of the category [[Loc]] of locales.  The category $Meas Loc$ of measurable locales is yet further a full subcategory of $Comp Bool Alg_{sup}^{op}$, so our job is simply to specify *which* complete boolean algebras are the [[objects]] of this category.  There are at least three equivalent ways of doing so.

1. By one definition, a complete boolean algebra $L$ is a __measurable locale__ if there is a (complete) compact strictly [[localizable measure space]] $X$ such that $L$ is [[isomorphic]] (as a boolean algebra) to the boolean algebra $\mathcal{M}/\mathcal{N}$ of [[measurable subsets]] of $X$ modulo [[null subsets]].  Note that the measure on $X$ is irrelevant except to specify the null subsets.  In this way, $Meas Loc$ becomes [[equivalence of categories|equivalent]] to the category $CSLEMS$ of (complete) compact strictly localizable [[enhanced measurable spaces]].  (Not every measure space has a *complete* boolean algebra as $\mathcal{M}/\mathcal{N}$; those which do are called *localizable*, and an enhanced measurable space is a structure with both $\mathcal{M}$ and $\mathcal{N}$ specified.)

2. By another definition, a complete boolean algebra $L$ is a __measurable locale__ if for every element $x \neq 0$ of $L$ there is a [[continuous valuation]] (see [below](#normalmeasures)) $\mu$ on $L$ valued in $[0,\infty]$ such that $\mu(x) = 1$.  (It would be enough to demand that $0 \lt \mu(x) \lt \infty$, since we can rescale the valuation.)

3. By yet another definition, a complete boolean algebra $L$ is a __measurable locale__ if there is a commutative $W^*$-[[W-star-algebra|algebra]] $A$ such that $L$ is [[isomorphic]] (as a boolean algebra) to the boolean algebra $Proj(A)$ of [[projection operators]] in $A$; (see [[idempotent operator]] for a construction of $Proj(A)$).  In this way, $Meas Loc$ becomes [[dual equivalence|dual]] to the category $Comm W^* Alg$ of commutative $W^*$-algebras.  For this definition, we need not require that $L \cong Proj(A)$ be complete (or even a boolean algebra); this can be proved.

Whichever of these equivalent definitions is adopted, a __measurable function__ between measurable locales is simply a [[continuous map]] between them as locales; these are the [[morphisms]] of $Meas Loc$.  In more elementary terms, a measurable function from $L$ to $M$ (thought of as measurable locales) is a function from $M$ to $L$ (thought of as Boolean algebras) that preserves all [[joins]] (and then it also preserves finite [[meets]] and so is a [[frame]] [[homomorphism]]).  Or we can think of this function's [[right adjoint]], a function from $L$ to $M$ that preserves all [[meets]].


### In constructive mathematics

(This section is not due to Pavlov.)

For purposes of [[constructive mathematics]], [[Toby Bartels]] suspects that it is appropriate to use the definition from $W^\star$-algebras, so long as we allow norms to be [[lower real numbers]].  (If they are all [[located real number|located]], then $Proj(A)$ has [[decidable equality]], which we don\'t want to require.)  The other definitions seem more difficult to work with (primarily because they require completeness explicitly).

For this definition (as was remarked above), we need not require that $L \cong Proj(A)$ be complete.  Constructively, we *cannot* require this; $Proj(A)$ need not be complete (although it is still a boolean algebra).  Indeed, consider the point (see [the examples](#examples)), based on $A \coloneqq \mathbb{C}$, which is *not* the complete [[Heyting algebra]] of *all* [[truth values]] but only the (possibly incomplete) boolean algebra $\{\bot, \top\}$ of *classical* truth values (corresponding to the self-adjoint idempotent complex numbers $0$ and $1$).

It seems that there is some notion of completeness that applies here; $L$ should in some sense be 'measurably complete'.  In the point, for example, the [[subsingleton]] $\{* \;|\; P\}$, where $P$ is a truth value, is measurable iff $P$ is true or false, so the supremum of $\{\top \;|\; P\}$ exists in $L$ under the same circumstances.  Figuring this out could allow the definitions through measurable spaces or continuous valuations to work.

Simpson's theory of [[sigma-locale]]s, see below, is developed in classical framework, but could be a good starting point for a constructive theory, as it avoids the focus on complements.  (But the main problem is completeness, not complements.)


## Examples {#examples}

The [[empty space]], which is [[initial object|initial]] in $Meas Loc$, is the [[terminal object|terminal]] boolean algebra with one element.

The [[point]], which is [[terminal object|terminal]] in $Meas Loc$, is the [[initial object|initial]] boolean algebra $\{\bot, \top\}$ of (classical) [[truth values]].

The [[real line]] is the boolean algebra of Lebesgue-[[measurable sets]] of [[real numbers]] modulo the [[null sets]].  This is complete as a boolean algebra because ... \[argument needed\] (and even constructively, it is still a boolean algebra).

Applying the classification of $W^*$-algebras, we find that (up to [[isomorphism]]), every measurable locale is a [[disjoint union]] (dually a [[direct product]] of boolean algebras) of $\{\bot, \top\}^I$ for a set $I$ of arbitrary cardinality.  If $I$ is finite, we get discrete spaces; if $I$ is countable, we get the real line.  Note that a single real line is already isomorphic to the union of countably infinitely many real lines.  (Of course, we can\'t expect this [[classification theorem]] to hold constructively.)


### Borel measurable spaces

To do [[measure theory]], it\'s important to know how to interpret the [[real line]] with the [[Borel sets]] (rather than Lebesgue sets) as a measurable space.  This is actually a little tricky, because [[Lebesgue measure]] is not complete on the Borel sets, and passing to the Lebesgue sets gives a different measurable space.  We might simply take the Borel sets as they are (so that only the empty set is null), but then this is not complete as a boolean algebra.

One might suspect that there is no Borel real line in $Meas Loc$, which would cast serious doubts on that as a category for measure theory.  But we can argue by [[abstract nonsense]] that it must exist, and more generally that any [[locale]] (including the [[locale of opens]] of any [[topological space]]) has a __Borel measurable locale__, as follows:

... <http://mathoverflow.net/questions/31603/why-do-probabilists-take-random-variables-to-be-borel-and-not-lebesgue-measurab/31724#31724> ... [[representable functor theorem]] ...

In the case of the real line, the resulting measurable locale is actually rather complicated: something like an uncountable disjoint union of points and lines.

This process is a [[functor]] $B\colon Loc \to Meas Loc$, which we can also extend to $Top \to Loc \to Meas Loc$.


### Lebesgue measurable spaces

Similarly, [[smooth manifolds]] give rise to (much simpler!) measurable locales by taking the Lebesgue sets (possible since we know which sets are null sets on a smooth manifold).  This process is a [[functor]] $L\colon SmoothMan_subm \to MeasLoc$, where the [[morphisms]] in $SmoothMan_subm$ are the [[smooth map|smooth]] [[submersions]].

In the case of the [[real line]], we get the usual line described under the basic examples above.  In fact, *any* [[second-countable space|second-countable]] smooth manifold with positive dimension gives rise to this measurable locale; the really interesting thing about $L$ is what it does to the morphisms.


## Measures {#normalmeasures}

On *any* complete boolean algebra $L$, given any [[abelian monoid]] $R$ equipped with a [[convergence space|convergence structure]] (such as $[0,\infty]$), a __[[normal measure]]__ on $L$ valued in $R$ is a [[function]] $\mu\colon L \to R$ such that:

*  _[[inclusion-exclusion|additivity]]_: $\mu(\bot) = 0$ and $\mu(x \wedge y) + \mu(x \vee y) = \mu(x) + \mu(y)$;

*  _[[Scott continuity|continuity]]_: if $S$ is a downward-[[codirected set|directed]] [[subset]] of $L$ whose [[infimum]] is the [[bottom element]], then the [[net]] $(\mu(x))_{x\colon S}$ converges to $0$.

One could, of course, define a garden-variety [[measure]] by requiring continuity only when $S$ is the image of a decreasing [[sequence]], but apparently normal measures are what we want for measurable locales.  Normal measures are also known as [[continuous valuations]].

Absolutely continuous measures on, say, Lebesgue space correspond to normal measures on the real line as a measurable locale.  ([[Lebesgue measure]] is not normal on the $\sigma$-algebra of measurable sets, but it is normal on the boolean algebra of measurable sets modulo null sets, which is what we want.)

This should work in constructive mathematics, with $[0,\infty]$ (for a positive measure) being be the space of nonnegative [[lower reals]].


## Related work

This is related to $\sigma$-[[sigma-locale|locales]].

* Alex Simpson, _Measure, randomness and sublocales_ [link](http://www.sciencedirect.com/science/article/pii/S0168007211001874)

which is part of his work to develop [[synthetic probability theory]].


## References

The basic definition and some elementary properties are given in

* [[Dmitri Pavlov]], _Gelfand-type duality for commutative von Neumann algebras_,
[arXiv:2005.05284](https://arxiv.org/abs/2005.05284).

This paper also establishes  [[Gelfand-type duality for commutative von Neumann algebras]].

The theory of measurable locales originated on [[MathOverflow]], in various questions and answers by [[Dmitri Pavlov]].  Here is an index:

* [[Dmitri Pavlov]], [answer](http://mathoverflow.net/questions/49426/is-there-a-category-structure-one-can-place-on-measure-spaces-so-that-category-th/49542#49542) to _Is there a category structure one can place on measure spaces so that category-theoretic products exist?_ (version: 2011-01-08)


[[!redirects measurable locale]]
[[!redirects measurable locales]]
[[!redirects MeasLoc]]
[[!redirects Meas Loc]]
