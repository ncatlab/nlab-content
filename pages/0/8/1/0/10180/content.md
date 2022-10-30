
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[presheaf topos]] $[FinSet, Set]$ on the [[opposite category]] of [[FinSet]] is the [[classifying topos]] for the [[theory of objects]], sometimes called the "object classifier" This is not to be confused with the notion of an [[object classifier]] in an [[(∞,1)-topos]]  and maybe better called in full the _classifying topos for the theory of objects_.

For $E$ any [[topos]], a [[geometric morphism]] $E \to [FinSet,Set]$ is equivalently just an [[object]] of $E$.

Similarly, the presheaf topos $[FinSet_*, Set]$ (where $FinSet_*$ is the category of finite [[pointed sets]]) classifies pointed objects; cf. [this question](http://mathoverflow.net/questions/85600/what-do-gamma-sets-classify) and answer.  This is the topos of "$\Gamma$-sets"; see [[Gamma-space]].

## Properties

+-- {: .num_prop}
###### Proposition

The classifying topos $[FinSet, Set]$ is [[equivalence of categories|equivalent]] to the category of finitary [[endofunctors]] on [[Set]] (those that commute with [[filtered colimits]]):

$$
  [FinSet, Set] \simeq End_f(Set)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Because every [[set]] is the [[filtered colimit]] over its finite [[subsets]].

=--

+-- {: .num_remark}
###### Remark

Since the category $End_f(Set) \hookrightarrow End(Set)$ of [[finitary monads]] is naturally a [[monoidal category]] under composition, this induces the structure of a (non-cartesian) [[monoidal category]] also on the [[classifying topos]] $[FinSet, Set]$ and hence makes it a [[monoidal topos]]. A [[monoid]] with respect to this monoidal structure is equivalently a [[finitary monad]].  

=--

## References


* [[Peter Johnstone]], section D3.2 in _[[Sketches of an Elephant]]_

* [[Richard Garner]], _Lawvere theories, finitary monads and Cauchy-completion_ ([arXiv:1307.2963](http://arxiv.org/abs/1307.2963))
 {#Garner13}
