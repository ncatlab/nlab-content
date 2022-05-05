
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

In the context of [[equivariant stable homotopy theory]] and $G$ one distinguishes, for a [[G-spectrum]] $E$, between the plain  _[[fixed point spectrum]]_ $F^G(E)$ and its _geometric fixed point spectrum_ $\Phi^G(E)$. 

Here the terminology "geometric" is in the sense of _[[point-set topology]]_, as opposed to [[homotopy theory]]: If $X$ is a ([[pointed topological space|pointed]]) [[topological space]] equipped with a [[continuous function]] $G$-[[action]] (a [[topological G-space]]), so that one may consider its $G$-[[equivariant suspension spectrum]] $\Sigma^\infty_G X \in G Spectra$, then the _geometric fixed point spectrum_ $\Phi^G(\Sigma^\infty_G X)$ of the latter is equivalent to the plain [[suspension spectrum]] of the plain [[fixed point]]-space $X^G$:

$$
  \Phi^G\big(  \Sigma^\infty_G X \big) 
     \;\simeq\;   
  \Sigma^\infty\big( X^G \big)
  \,,
$$

see the characterization in Prop. \ref{AbstractCharacterizationOfGeometricFixedPointSpectra}, below.

In general this is different from (not [[equivalence in an (infinity,1)-category|equivalent]] to) both of the following other notions of fixed point spectra:

1. the plain (really: [[homotopy theory|homotopy theoretic]]) [[fixed point spectrum]] $F^G(\Sigma^\infty_G X)$, which is instead the [[derived functor]] of forming topological fixed points $X \mapsto X^G$, hence which applies this construction only after [[fibrant resolution]]; the difference between the two is described by the _[[tom Dieck splitting theorem]]_, see Prop. \ref{AsWedgeSummandInTomDieckSplitting} below.

1. the [[categorical fixed point spectrum]]...


## Definition

A concrete definition of geometric fixed points of an equivariant spectrum is in ([Schwede 15, 7.3](#Schwede15)). A conceptual characterization in terms of [[localization of spectra]] is in ([Mathew-Naumann-Noel 15, def. 6.12](#MathewNaumannNoel15)).

## Properties

### For equivariant suspension spectra
 {#ForEquivariantSuspensionSpectra}


+-- {: .num_prop #AsWedgeSummandInTomDieckSplitting}
###### Proposition
**(as a [[wedge sum|wedge summand]] in the [[tom Dieck splitting]])** 

For $X$ a [[topological G-space]] and $\Sigma^\infty_G X$ its [[equivariant suspension spectrum]], there is a canonical comparison morphism (...) 

$$
  \Phi^G(\Sigma^\infty_G X) 
  \;\simeq\; 
  \Sigma^\infty( X^G )
  \hookrightarrow
  F^G(\Sigma^\infty_G X)
$$

which exhibits its geometric fixed point spectrum as precisely the first summand in the [[tom Dieck splitting]] of the plain [[fixed point spectrum]]

$$
  F^G(\Sigma^\infty_G X)
  \simeq
  \Sigma^\infty( X^G )
    \vee
  \left(
    \underset{{[H\subset G]} \atop {1 \neq H \neq G}}{\vee}
    \Sigma^\infty( E (W_G H)_+ \wedge_{W_G H} X^H )
  \right)
    \vee
  \Sigma^\infty( E G_+ \wedge_{G} X )
  \,.
$$

=--

([Schwede 15, Example 7.7](#Schwede15))

In fact:

+-- {: .num_prop #AbstractCharacterizationOfGeometricFixedPointSpectra}
###### Proposition

The construction of geometric fixed point spectra is essentially uniquely characterized by the  property 

$$
  \Phi^G\big(  \Sigma^\infty_G X \big) 
     \;\simeq\;   
  \Sigma^\infty\big( X^G \big)
$$

and the property of being [[left derived functor|left derived]] [[strong monoidal functor|strong monoidal]] and preserving [[homotopy colimits]].

=--

([Schwede 15, remark 7.15](#Schwede15), [Blumberg 17, around Def. 2.5.16](#Blumberg17))

{#PartialGeometricFixedPoint} This generalizes to a "partial" geometric fixed point functor, which for a given [[subgroup]] $H \subset G$ sends

$$
  \Phi^H \;\colon\; G Spectra \longrightarrow W_G H Spectra
$$

(for $W_G/H$ the [[Weyl group]], which is the [[quotient group]] $G/H$ in the case that $H$ is a [[normal subgroup]]) and satisfies

$$
  \Phi^N \big(  \Sigma^\infty_G X \big) 
  \;\simeq\;
  \Sigma^\infty_{W_G H} X^H
  \,.
$$

([Lewis-May-Steinberger 86, II.9, cor. 9.9](#LewisMaySteinberger86), [Lewis 00, Scholium 10.2](#Lewis00))


## Related concepts

* [[fixed point space]]

* [[fixed point spectrum]]

* [[categorical fixed point spectrum]]

* [[homotopy fixed points]]

## References

* {#LewisMaySteinberger86} [[L. Gaunce Lewis]], [[Peter May]], and Mark Steinberger (with contributions by J.E. McClure), _Equivariant stable homotopy theory_, Springer Lecture Notes in Mathematics Vol.1213. 1986 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/equi.pdf))


* {#Lewis00} [[L. Gaunce Lewis, Jr.]], section 10 of _Splitting theorems for certain equivariant spectra_, Memoirs of the AMS, number 686, March 2000, Volume 144 ([pdf](http://hopf.math.purdue.edu/LewisG/spltspec.pdf))

* {#Schwede15} [[Stefan Schwede]], section 7.3 of _[[Lectures on Equivariant Stable Homotopy Theory]]_, 2015 ([pdf](http://www.math.uni-bonn.de/people/schwede/equivariant.pdf))

* {#Schwede18} [[Stefan Schwede]], section 3.3. of _[[Global homotopy theory]]_ ([arXiv:1802.09382](https://arxiv.org/abs/1802.09382))

* {#Blumberg17} [[Andrew Blumberg]], Def. 2.5.16 in _Equivariant homotopy theory_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))


* {#MathewNaumannNoel15} [[Akhil Mathew]], [[Niko Naumann]], [[Justin Noel]], _Nilpotence and descent in equivariant stable homotopy theory_ ([arXiv:1507.06869](http://arxiv.org/abs/1507.06869))



[[!redirects geometric fixed point spectra]]

[[!redirects geometric fixed point]]
[[!redirects geometric fixed points]]


