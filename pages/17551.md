
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

In the context of [[equivariant stable homotopy theory]] one distinguishes, for a [[G-spectrum]] $E$, between the plain  _[[fixed point spectrum]]_ $F^G(X)$ and its _geometric fixed point spectrum_ $\Phi^G(X)$.

A concrete definition of geometric fixed points of an equivariant spectrum is in ([Schwede 15, 7.3](#Schwede15)). A conceptual characterization in terms of [[localization of spectra]] is in ([Mathew-Naumann-Noel 15, def. 6.12](#MathewNaumannNoel15)).

## Properties

### For equivariant suspension spectra
 {#ForEquivariantSuspensionSpectra}

For $X$ a [[topological G-space]] and $\Sigma^\infty_G X$ its [[equivariant suspension spectrum]], its geometric fixed point spectrum is precisely the first summand in 

$$
  \Phi^G(\Sigma^\infty_G X) 
  \;\simeq\; 
  \Sigma^\infty( X^G )
  \hookrightarrow
  F^G(\Sigma^\infty_G X)
$$

the [[tom Dieck splitting]] of the plain [[fixed point spectrum]]

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

([Schwede 15, Example 7.7](#Schwede15))

In fact, the construction of geometric fixed point spectra is uniquely characterized by this property and the property of being [[left derived functor|left derived]] [[strong monoidal functor|strong monoidal]] and preserving [[homotopy colimits]].

([Blumberg 17, around Def. 2.5.16](#Blumberg17))

## Related concepts

* [[fixed point spectrum]]

* [[homotopy fixed points]]

## References

* {#Schwede15} [[Stefan Schwede]], section 7.3 of _[[Lectures on Equivariant Stable Homotopy Theory]]_, 2015 ([pdf](http://www.math.uni-bonn.de/people/schwede/equivariant.pdf))

* {#Schwede18} [[Stefan Schwede]], section 3.3. of _[[Global homotopy theory]]_ ([arXiv:1802.09382](https://arxiv.org/abs/1802.09382))

* {#Blumberg17} [[Andrew Blumberg]], Def. 2.5.16 in _Equivariant homotopy theory_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))


* {#MathewNaumannNoel15} [[Akhil Mathew]], [[Niko Naumann]], [[Justin Noel]], _Nilpotence and descent in equivariant stable homotopy theory_ ([arXiv:1507.06869](http://arxiv.org/abs/1507.06869))



[[!redirects geometrix fixed point spectra]]

[[!redirects geometric fixed point]]
[[!redirects geometric fixed points]]


