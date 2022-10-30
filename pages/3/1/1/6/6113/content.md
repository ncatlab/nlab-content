
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Stable Homotopy theory
+-- {: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

For $X$ a [[pointed object|pointed]] [[topological space]], its **suspension spectrum** $\Sigma^\infty X$ is the [[spectrum]] given by the pre-spectrum whose degree-$n$ space is the $n$-fold [[reduced suspension]] of $X$:

$$
  (\Sigma^\infty X)_n = \Sigma^n X
  \,.
$$

(e.g. [Elmendorf-Kriz-May, example 1.1](#ElmendorfKrizMay))

As a [[symmetric spectrum]]: ([Schwede 12, example I.2.6](#Schwede12))

## Properties

### Completion to an $\Omega$-spectrum

See at [Omega spectrum -- Completion of a suspension spectrum](Omega-spectrum#CompletionOfSuspensionSpectra).

### Relation to looping and stabilization

As an [[infinity-functor]] $\Sigma^\infty\colon Top_* \to Spec$ the suspension spectrum functor exhibits the [[stabilization]] of [[Top]].

$$
  (\Sigma^\infty \dashv \Omega^\infty)\colon 
  Top_* \stackrel{\overset{\Omega^\infty}{\leftarrow}}{\underset{\Sigma^\infty}{\to}}
  Spec
$$


### Strong monoidalness
 {#StrongMonoidalness}

The suspension spectrum functor is [[strong monoidal functor|strong monoidal]].

On the one hand, this is the case for its incarnation as a [[1-functor]] with values in [[structured spectra]] ([this Prop.](Introduction+to+Stable+homotopy+theory+--+1-2#SmashProductOfFreeSpectra))
Via the corresponding [[symmetric monoidal smash product of spectra|symmetric monoidal]] [[Model categories of diagram spectra|model structure on structured spectra]] this exhibits strong monoidalness also as an [[(infinity,1)-functor]].

More abstractly this follows from general properties of [[stabilization]] when regarding [[stable homotopy theory]] as the result of inverting [[smash product]] with the [[circle]], via [Robalo 12, last clause of Prop. 4.1 with last clause of Prop. 4.10 (1) ](stabilization#Robalo12). For emphasis see also [Hoyois 15, section 6.1](stabilization#Hoyois15), specifically [Hoyois 15, Def. 6.1](stabilization#Hoyois15).




[[!include smash-monoidal diagonals -- section]]




## Related concepts

* [[free structured spectrum]]

* [[equivariant suspension spectrum]]

## References

* {#Adams74} [[Frank Adams]], part III, section 2 of _[[Stable homotopy and generalised homology]]_, 1974


* {#ElmendorfKrizMay} [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], example 1.1 of _[[Modern foundations for stable homotopy theory]]_, in [[Ioan Mackenzie James]], _[[Handbook of Algebraic Topology]]_, Amsterdam: North-Holland (1995) pp. 213&#8211;253,  ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))


* {#Kuhn84} Nicholas J. Kuhn, _Suspension spectra and homology equivalences_, Trans. Amer.
Math. Soc. 283, 303&#8211;313 (1984) ([JSTOR](http://www.jstor.org/stable/2000005))

* {#Klein02} [[John Klein]], _Moduli of suspension spectra_ ([arXiv:math/0210258](http://arxiv.org/abs/math/0210258), [MO](http://mathoverflow.net/a/84686/381))

* {#Schwede12} [[Stefan Schwede]], Example I.2.6 in _Symmetric spectra_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec.pdf))

Suspension spectra of [[infinite loop spaces]] are discussed (in a context of [[Goodwillie calculus]] and [[chromatic homotopy theory]]) in 

* Nicholas J. Kuhn, section 6.2 of _Goodwillie towers and chromatic homotopy: An overview_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/KuhnKinosaki.pdf))

[[!redirects suspension spectrum]]
[[!redirects suspension spectra]]