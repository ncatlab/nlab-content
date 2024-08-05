
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

A __pretopos__ is a [[category]] which is both (Barr-)[[exact category|exact]] and [[extensive category|extensive]].  (See [[familial regularity and exactness]] for why extensivity and exactness deserve to be considered together.)  This implies that it is a [[coherent category]]. 

Pretoposes are suitable as frameworks for [[finite mathematics|finitist]] [[predicative mathematics]], respectively with [[coherent logic]].

Frequently one is especially interested in pretoposes having additional properties, such as:

* A __Heyting pretopos__ is a pretopos which is also a [[Heyting category]]; a __Boolean pretopos__ is a pretopos which is also a [[Boolean category]].  These are suitable as frameworks for [[finite mathematics|finitist]] [[predicative mathematics]], respectively with [[intuitionistic logic|intuitionistic]] or [[classical logic|classical]] logic.

* A __pretopos with choice__ is a pretopos that satisfies the [[axiom of choice]] (that every [[epimorphism]] is [[split epic|split]]). Every pretopos with choice is automatically boolean. 

* A __[[Π-pretopos]]__ is a pretopos which is also a [[locally cartesian closed category]].  (A $\Pi$-pretopos is automatically a Heyting pretopos.)  These are suitable as frameworks for finitist [[constructive mathematics]] which is 'weakly predicative'.

* An __[[arithmetic pretopos]]__ is a pretopos which has (locally) a parameterised [[natural numbers object]]. Arithmetic pretoposes are suitable as frameworks for non-finitist but strongly predicative mathematics with [[coherent logic]], while Heyting arithmetic pretoposes and Boolean arithmetic pretoposes are suitable as frameworks for non-finitist but strongly predicative mathematics with intuitionistic and classical logic, respectively.

* A __$W$-pretopos__ is a pretopos which has (locally) [[W-types]] ([[initial algebra|initial]] [[algebra for an endofunctor|algebras]] for [[polynomial endofunctors]]), most famously a [[natural numbers object]].  (Here, we take any [[exponentiable morphism]] to define a polynomial endofunctor.  This paragraph is original to this page and not in the literature; it may not be the best definition.) 

* An __arithmetic $\Pi$-pretopos__ is a pretopos that is both a $\Pi$-pretopos and an arithmetic pretopos; it is sufficient that the $\Pi$-pretopos have a [[natural numbers object]], and so could be called __$\Pi$-pretopos with NNO__. These are suitable as frameworks for weakly predicative constructive mathematics that is not finitist.

* A __[[ΠW-pretopos]]__ is a pretopos that is both a $\Pi$-pretopos and a $W$-pretopos.  (Now every morphism defines a polynomial endofunctor, since every morphism is exponentiable.) 

* A __[[predicative topos]]__ is a [[ΠW-pretopos]] that satisfies the [[axiom of multiple choice]].  (This now differs from a $W$-[[topos]] below mainly in still lacking [[power objects]], hence still a context for weakly predicative constructive mathematics.)

* A __[[topos]]__ is a pretopos that has [[power objects]].  A topos is automatically a $\Pi$-pretopos; conversely, a $\Pi$-pretopos is a topos iff it has a [[subobject classifier]], and a Boolean $\Pi$-pretopos is always a topos.  Toposes and [[Boolean toposes]] are suitable as frameworks for finitist (but otherwise impredicative) mathematics, with intuitionistic and classical logic respectively.

* A __$W$-topos__ is of course a topos that is a $W$-pretopos; it is sufficient that the topos have a [[natural numbers object]] (see [van den Berg, Moerdijk 2008](#vdBergMoerdijk2008)), so this is often called a __topos with NNO__.  These are suitable as frameworks for (non-predicative, non-finitist) [[constructive mathematics]], while Boolean $W$-toposes are suitable as a framework for [[classical mathematics]] without the [[axiom of choice]].

* A __topos with choice__ is a topos that satisfies the [[axiom of choice]] (that every [[epimorphism]] is [[split epic|split]]).  Every topos with choice is automatically boolean, so $W$-toposes with choice are suitable as a framework for full classical mathematics.  (In fact, a [[well-pointed category|well-pointed]] $W$-topos with choice is precisely a model of [[ETCS]].)

### Infinitary pretoposes
{#infinitary}

An __infinitary pretopos__ is an [[infinitary coherent category]] which is both [[infinitary extensive category|infinitary extensive]] and [[exact category|exact]].  Giraud\'s theorem says that infinitary pretoposes with small generating sets are the same as [[Grothendieck toposes]], and in particular are [[toposes]] (although this last result is not valid in [[predicative mathematics]]).

An infinitary pretopos (perhaps with [[well-powered category|well-poweredness]] included) is sometimes called an "$\infty$-pretopos" (e.g. in the [[Elephant]]), but we avoid that term because of potential confusion with the notion of [[(∞,1)-pretopos]].

## Examples

* Of course, any [[topos]] is a [[pretopos]], so any example there is an example of a [[pretopos]].

* An example of a pretopos that is not a [[topos]] is the [[category]]
of [[compact Hausdorff spaces]] ([MarraReggio](#MarraReggio)).

* An example of a Boolean pretopos that is not [[cartesian closed category|cartesian closed]] is the category of finite or countably infinite sets (cf. [[Elephant]] p.54).

* The category of [[decidable objects]] of a [[topos]] is a Boolean pretopos. 

* The [[exact completion]] of the category [[Ho(Top)]] of [[topological spaces]] and [[homotopy classes]] of [[continuous maps]] is a pretopos. 

* In [[dependent type theory]], a [[univalent universe]] where every type in the universe satisfies [[axiom K]] and is closed under the [[empty type]], [[unit type]], [[sum types]], [[dependent sum types]], [[product types]], [[propositional truncations]], and [[quotient sets]] is a pretopos. 
  * the universe becomes an [[arithmetic pretopos]] if it is closed under a parameterized [[natural numbers type]]
  * the universe becomes a Heyting pretopos if the universe is closed under [[dependent product types]] for families of [[mere propositions]], or equivalently, if it is closed under types of [[embeddings]]
  * the universe becomes a Boolean pretopos if it is a Heyting pretopos and additionally every proposition satisfies [[excluded middle]]
  * the universe becomes a Π-pretopos if it is closed under all [[dependent product types]], or equivalently, if the universe is closed under [[function types]]
  * the universe becomes an arithmetic Π-pretopos if it is a Π-pretopos and is closed under a [[natural numbers type]]
  * the universe becomes an elementary topos if it is a Π-pretopos and has a [[type of all propositions]]
  * the universe becomes a Boolean topos if it is a Boolean Π-pretopos

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

* {#vdBergMoerdijk2008} [[Benno van den Berg]],  [[Ieke Moerdijk]] (2008-09-25); _$W$-types in sheaves_; [vdBM_Wtypes.ps/pdf](http://www.phil.cmu.edu/projects/ast/Papers/)

* {#MarraReggio} [[Vincenzo Marra]], [[Luca Reggio]], _A characterisation of the category of compact Hausdorff spaces_, Theory Appl. Categ. 35 (2020), Paper No. 51, 1871–1906. [pdf](http://www.tac.mta.ca/tac/volumes/35/51/35-51.pdf), [arXiv:1808.09738](https://arxiv.org/abs/1808.09738).

* {#Taylor} [[Paul Taylor]], [MathOverflow answer](https://mathoverflow.net/questions/382348/subobjects-in-the-category-of-compact-hausdorff-spaces/382351#382351).

* [[Marino Gran]], [[Enrico Vitale]], *On the exact completion of the homotopy category*, Cahiers de Topologie et Géométrie Différentielle Catégoriques **39** 4 (1998)  287-297 &lbrack;[numdam:CTGDC_1998__39_4_287_0](http://www.numdam.org/item/CTGDC_1998__39_4_287_0)&rbrack;

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