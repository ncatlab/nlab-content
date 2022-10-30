
# Dream mathematics
* table of contents
{: toc}

## Idea

Dream mathematics is an alternative [[foundation of mathematics]] first studied (as a piece of [[metamathematics]]) by [[Robert Solovay]].  Several 'ill-behaved' counterexamples in [[analysis]] fail to exist in it.


## Definition

__Dream mathematics__ is [[mathematics]] founded on [[ZF]] (or an equivalent [[structural set theory]] such as [[SEAR]]) with [[dependent choice]] and the following axioms (any of which contradict [[full choice]]) required of every [[subset]] $A$ of the [[real line]]:

*  [[Lebesgue-measurable set|Lebesgue measurability]]: $A$ is the [[union]] of a [[Borel set]] and a [[null set]];
*  The [[perfect set property]]: $A$ has an [[inhabited set|inhabited]] [[perfect subset|perfect]] subset if it is [[uncountable set|uncountable]];
*  The [[Baire property]]: $A$ is the [[union]] of an [[open set]] and a [[meager set|meagre set]].

A __dream universe__ is any [[model]] of dream mathematics.  The most well known (and the first known) is the _Solovay model_.


## Consistency

Solovay proved that dream mathematics is [[consistent theory|consistent]] if the existence of an [[inaccessible cardinal]] is consistent with [[ZFC]].  More precisely, Solovay showed how to construct a [[model]] of dream mathematics (now called the _Solovay model_) from any model of $ZFC$ with an inaccessible cardinal.

[[Saharon Shelah]] later showed that one could start with *any* model of $ZFC$ and construct a model of $ZF + DC$ in which every set of reals has the Baire property; on the other hand, [[Ernst Specker]] had already shown that an inaccessible cardinal must be consistent if the perfect set property is. Various intermediate consistency results for Lebesgue measurability are also known, but a complete characterisation is still elusive.


## Properties

Besides the axioms themselves, other nice properties hold in dream mathematics.  Examples include:

*  Every (total) [[linear function]] from a [[Fréchet space]] to any [[topological vector space]] is [[continuous map|continuous]] (so every linear mapping between [[Banach spaces]] is [[bounded map|bounded]]).

*  On a [[localizable measure|localisable measure space]], the [[dual vector space|dual]] of the [[Lebesgue space]] $L^\infty$ is $L^1$ (so these two spaces are [[reflexive Banach space|reflexive]]).

*  Any two [[complete space|complete]] [[norms]] (or even [[F-norms]]) on a given [[vector space]] over the [[real numbers]] must be [[topological equivalence|topologically equivalent]], which nicely explains why you have never seen two *specific* inequivalent complete norms on a given real vector space.


## References

* Wikipedia (English); [Solovay model](https://en.wikipedia.org/wiki/Solovay_model).

* _[[HAF]]_; end of Chapter 27.


[[!redirects dream mathematics]]
[[!redirects dream analysis]]
[[!redirects dream universe]]
[[!redirects dream universes]]

[[!redirects Solovay model]]
[[!redirects Solovay universe]]
