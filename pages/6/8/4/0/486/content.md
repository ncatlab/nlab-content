
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Regular and Exact categories
+-- {: .hide}
[[!include regular and exact categories - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Pretopos
* table of contents
{: toc}

## Definitions

### General

A __pretopos__ is a [[category]] which is both [[exact category|exact]] and [[extensive category|extensive]].  (See [[familial regularity and exactness]] for why extensivity and exactness deserve to be considered together.)  This implies that it is a [[coherent category]].

Frequently one is especially interested in pretoposes having additional properties, such as:

* A __Heyting pretopos__ is a pretopos which is also a [[Heyting category]]; a __Boolean pretopos__ is a pretopos which is also a [[Boolean category]].  These are suitable as frameworks for [[finite mathematics|finitist]] [[predicative mathematics]], respectively with [[intuitionistic logic|intuitionistic]] or [[classical logic|classical]] logic.

* A __[[Π-pretopos]]__ is a pretopos which is also a [[locally cartesian closed category]].  (A $\Pi$-pretopos is automatically a Heyting pretopos.)  These are suitable as frameworks for finitist [[constructive mathematics]] which is 'weakly predicative'.

* A __$W$-pretopos__ is a pretopos which has (locally) [[W-types]] ([[initial algebra|initial]] [[algebra for an endofunctor|algebras]] for [[polynomial endofunctors]]), most famously a [[natural numbers object]].  (Here, we take any [[exponentiable morphism]] to define a polynomial endofunctor.  This paragraph is original to this page and not in the literature; it may not be the best definition.)  Heyting $W$-pretoposes and Boolean $W$-pretoposes are suitable as frameworks for non-finitist but strongly predicative mathematics (with intuitionistic and classical logic, respectively).

* A __[[ΠW-pretopos]]__ is a topos that is both a $\Pi$-pretopos and a $W$-pretopos.  (Now every morphism defines a polynomial endofunctor, since every morphism is exponentiable.)  These are suitable as frameworks for weakly predicative constructive mathematics that is not finitist.

* A __[[predicative topos]]__ is a [[ΠW-pretopos]] that satisfies the [[axiom of multiple choice]].  (This now differs from a $W$-[[topos]] below mainly in still lacking [[power objects]], hence still a context for weakly predicative constructive mathematics.)

* A __[[topos]]__ is a pretopos that has [[power objects]].  A topos is automatically a $\Pi$-pretopos; conversely, a $\Pi$-pretopos is a topos iff it has a [[subobject classifier]], and a Boolean $\Pi$-pretopos is always a topos.  Toposes and [[Boolean toposes]] are suitable as frameworks for finitist (but otherwise impredicative) mathematics, with intuitionistic and classical logic respectively.

* A __$W$-topos__ is of course a topos that is a $W$-pretopos; it is sufficient that the topos have a [[natural numbers object]] (see van den Berg & Moerdijk), so this is often called a __topos with NNO__.  These are suitable as frameworks for (non-predicative, non-finitist) [[constructive mathematics]], while Boolean $W$-toposes are suitable as a framework for [[classical mathematics]] without the [[axiom of choice]].

* A __topos with choice__ is a topos that satisfies the [[axiom of choice]] (that every [[epimorphism]] is [[split epic|split]]).  Every topos with choice is automatically boolean, so $W$-toposes with choice are suitable as a framework for full classical mathematics.  (In fact, a [[well-pointed category|well-pointed]] $W$-topos with choice is precisely a model of [[ETCS]].)


### Infinitary pretoposes
{#infinitary}

An __infinitary pretopos__ is an [[infinitary coherent category]] which is both [[infinitary extensive category|infinitary extensive]] and [[exact category|exact]].  Giraud\'s theorem says that infinitary pretoposes with small generating sets are the same as [[Grothendieck toposes]], and in particular are [[toposes]] (although this last result is not valid in [[predicative mathematics]]).

An infinitary pretopos (perhaps with [[well-powered category|well-poweredness]] included) is sometimes called an "$\infty$-pretopos" (e.g. in the [[Elephant]]), but we avoid that term because of potential confusion with the notion of [[(∞,1)-pretopos]].

## Examples

Of course, any [[topos]] is a [[pretopos]], so any example there is an example of a [[pretopos]].

An example of a pretopos that is not a [[topos]] is the [[category]]
of [[compact Hausdorff spaces]] \cite{MarraReggio}.

## Properties

### Internal logic and mathematics in pretopoi

Like any coherent (or Heyting) category, a (Heyting) pretopos has an [[internal logic]].  Extensivity and exactness make a Heyting pretopos a very set-like category.  One can say imprecisely that it has "all the good first-order properties of a [[topos]]", meaning not that it has those properties that can be expressed in elementary terms (which is false) but that it has those properties that (unlike exponential and power objects) correspond to first-order reasoning in ordinary mathematics.  Therefore, pretoposes (especially Heyting, $\Pi$, and/or $W$ ones) are related to predicative constructive mathematics in a way similar to how toposes are related to non-predicative constructive mathematics.


### Colimits

A pretopos is necessarily [[balanced category|balanced]], but while it has coproducts and coequalizers of equivalence relations, it need not have all finite colimits.  However, if it has countable pullback-stable unions of subobjects (what the [[Elephant]] calls a _$\sigma$-pretopos_; see [[infinitary coherent category]]), then any internal binary relation generates an equivalence relation and therefore has a quotient, so we can construct arbitrary coequalizers and thus arbitrary finite colimits.  And we can perform an "internal" version of this argument in a $\Pi$-pretopos with a [[natural numbers object|NNO]], such as a $\Pi$-$W$-pretopos.


### The precanonical topology

A pretopos, being a [[coherent category]], admits a [[subcanonical site|subcanonical]] [[Grothendieck topology]] called the [[coherent topology]].  In a pretopos, this topology is generated by finite jointly epimorphic families.  Since the [[canonical topology]] on a [[Grothendieck topos]] consists of all jointly epimorphic families, the coherent topology on a pretopos is sometimes called the __precanonical topology__.

The [[codomain fibration]] of a pretopos is always a [[stack]] for its precanonical topology.  Being a pretopos is stronger than necessary for this condition to hold in a coherent category, however; see [[coherent category]] for the necessary and sufficient conditions.

## Related concepts

* [[Π-pretopos]], [[ΠW-pretopos]], [[list-arithmetic pretopos]]

* [[2-pretopos]]

* [[(∞,1)-pretopos]]

* [[conceptual completeness]]

## References

*  [[Benno van den Berg]],  [[Ieke Moerdijk]] (2008-09-25); _$W$-types in sheaves_; [vdBM_Wtypes.ps/pdf](http://www.phil.cmu.edu/projects/ast/Papers/)

* {#MarraReggio} [[Vincenzo Marra]], [[Luca Reggio]], _A characterisation of the category of compact Hausdorff spaces_, Theory Appl. Categ. 35 (2020), Paper No. 51, 1871–1906. [pdf](http://www.tac.mta.ca/tac/volumes/35/51/35-51.pdf), [arXiv:1808.09738](https://arxiv.org/abs/1808.09738).

* {#Taylor} [[Paul Taylor]], [MathOverflow answer](https://mathoverflow.net/questions/382348/subobjects-in-the-category-of-compact-hausdorff-spaces/382351#382351).

[[!redirects pretopos]]
[[!redirects pretoposes]]
[[!redirects pretopoi]]

[[!redirects Heyting pretopos]]
[[!redirects Heyting pretoposes]]
[[!redirects Heyting pretopoi]]

[[!redirects Boolean pretopos]]
[[!redirects Boolean pretoposes]]
[[!redirects Boolean pretopoi]]

[[!redirects W-pretopos]]
[[!redirects W-pretoposes]]
[[!redirects W-pretopoi]]

[[!redirects infinitary pretopos]]
[[!redirects infinitary pretoposes]]
[[!redirects infinitary pretopoi]]

[[!redirects precanonical topology]]
[[!redirects precanonical topologies]]