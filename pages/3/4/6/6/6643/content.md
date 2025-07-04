
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### 2-Category theory
+-- {: .hide}
[[!include 2-category theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A **flexible limit** is a [[strict 2-limit]] whose [[weighted limit|weight]] is [[cofibrant object|cofibrant]].  This implies that flexible limits are also [[2-limits]] (in the non-strict sense, which for us is the default -- recall that these are traditionally called [[bilimits]]).

Furthermore, all [[PIE-limits]] and therefore all [[strict pseudo-limits]] are flexible; thus any [[strict 2-category]] which admits all flexible limits also admits all $2$-limits.  A number of [[strict 2-categories]] admit all flexible limits, but not all strict $2$-limits, and this is a convenient way to show that they admit all $2$-limits.


## Definition

Let $D$ be a small [[strict 2-category]].  Write $[D,Cat]$ for the strict 2-category of [[strict 2-functors]], [[strict 2-natural transformation|strict 2-natural transformations]], and [[modifications]], and $Ps(D,Cat)$ for the strict 2-category of strict 2-functors, [[pseudonatural transformations]], and modifications.  The inclusion
$$ [D,Cat] \to Ps(D,Cat) $$
(as a [[wide subcategory]]) has a strict [[left adjoint]] $Q$, which is the [[pseudo morphism classifier]] for an appropriate [[strict 2-monad]].  Therefore, for any functor $\Phi \colon D\to Cat$, we have $Q\Phi \colon D\to Cat$ such that pseudonatural transformations $\Phi \to \Psi$ are in natural bijection with strict 2-natural transformations $Q\Phi \to \Psi$.

The [[counit of an adjunction|counit]] of this adjunction is a canonical strict 2-natural transformation $q\colon Q\Phi \to \Phi$.  We say that $\Phi$ is **flexible** if this transformation has a [[section]] in $[D,Cat]$.


## Examples

All [[PIE-limits]] are flexible.  This includes [[products]], [[inserters]], [[equifiers]] by definition, and also [[descent object|descent objects]], [[iso-inserters]], [[comma objects]], [[Eilenberg–Moore objects]], and so on.  In fact, PIE-limits have a characterization similar to the definition above of flexible limits: they are the coalgebras for $Q$ regarded as a 2-[[comonad]].

The [[split idempotent|splitting of idempotents]] is flexible, but not PIE.  Moreover, in a certain sense it is the "only" such.  Precisely, flexible limits are the [[saturated class of limits|saturation]] of each of the following classes of limits:

* PIE-limits together with splitting of idempotents
* PIE-limits together with splitting of idempotent equivalences
* strict pseudo-limits together with splitting of idempotents
* strict pseudo-limits together with splitting of idempotent equivalences
* [[products]], [[iso-inserters]], [[powers]], splitting of idempotents
* [[products]], [[powers]], splitting of idempotents, [[pullbacks]] of [[normal isofibrations]]
* [[products]], [[powers]], splitting of idempotents, [[pullbacks]] of [[amnestic isofibrations]]

## Related pages

* Flexible limits may be characterised as the **persistent** [[double limits]].
* [[semiflexible limit]]
* [[PIE-limit]]
* [[coherence theorem for bicategories with finite limits]]


## References

* {#BirdKellyPowerStreet89} [[Greg J. Bird]], [[Max Kelly]], [[John Power]], [[Ross Street]], _Flexible limits for 2-categories_, Journal of Pure and Applied Algebra **61** 1 (1989) 1-27 \[<a href="https://doi.org/10.1016/0022-4049(89)90065-0">doi:10.1016/0022-4049(89)90065-0</a>\]

* [[John Bourke]]. _Accessible aspects of 2-category theory_. Journal of Pure and Applied Algebra 225.3 (2021): 106519.


[[!redirects flexible limit]]
[[!redirects flexible limits]]

[[!redirects flexible 2-limit]]
[[!redirects flexible 2-limits]]

