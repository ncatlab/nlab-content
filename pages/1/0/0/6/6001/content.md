
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The concept of _$\Omega$-spectra_ is one several [[equivalence of (∞,1)-categories|equivalent]] [[presentable (∞,1)-category|presentation]] of the [[stable (∞,1)-category of spectra]]. 

## Definition


With $\Omega$ the notation for the [[loop space]] construction (whence the name),an $\Omega$-spectrum is a sequence $E_\bullet = (E_n)_{n \in \mathbb{N}}$ of [[pointed object|pointed]] [[∞-groupoids]] ([[homotopy types]]) equipped for each $n \in \mathbb{N}$ with an [[equivalence of ∞-groupoids]]

$$
  E_n \stackrel{\simeq}{\longrightarrow} \Omega E_{n+1}
  \,.
$$ 

Remark: In terms of [[model category]] [[presentable (∞,1)-category|presentation]] one may also consider sequences of [[topological spaces]] equipped with [[homeomorphisms]] $E_n \longrightarrow \Omega E_{n+1}$  See at _[[spectrum]]_ the section <a href="http://nlab.mathforge.org/nlab/show/spectrum#OmegaSpectrum">Omega-spectra</a>.

## Examples

### $\Omega$-spectrum completion of suspension spectra
 {#CompletionOfSuspensionSpectra}

Given a [[pointed topological space]] $X$, its [[suspension spectrum]] $\Sigma^\infty X$ is far from being an $\Omega$-spectrum. The $\Omega$-spectrum that it induces is given by [[free infinite loop space]] constructions:

write

$$
  Q\;\colon\; Top^{\ast/} \longrightarrow Top^{*/}
$$

for the [[free infinite loop space]] [[functor]] given as the [[colimit]]

$$
  Q X \coloneqq \underset{\longrightarrow}{\lim}_k \Omega^k \Sigma^k X
$$

over iterated [[suspension]] and [[loop space]] construction. 

Then $(Q \Sigma^\infty X)_n \coloneqq Q(\Sigma^n X)$ is the $\Omega$-spectrum corresponding to the suspension spectrum of $X$.



## Related concepts

* [[coordinate-free spectrum]]

* [[excisive functor]]

## References

* {#ElmendorfKrizMay95} [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], section 1 of  _[[Modern foundations for stable homotopy theory]]_, in [[Ioan Mackenzie James]], _[[Handbook of Algebraic Topology]]_, Amsterdam: North-Holland (1995) pp. 213&#8211;253,  ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))

* {#Malkiewich14} [[Cary Malkiewich]], section 2.2 of _The stable homotopy category_, 2014 ([pdf](http://math.stanford.edu/~carym/stable.pdf))


[[!redirects Omega-spectra]]

[[!redirects Omega spectrum]]
[[!redirects Omega spectra]]

