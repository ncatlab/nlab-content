
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

The _stable homotopy category_ is the [[homotopy category of an (infinity,1)-category|homotopy category]] of the [[stable (infinity,1)-category of spectra]].

This is the [[category]] studied in [[stable homotopy theory]].

## Definition

### Via left homotopy of spectra

Let $PreSpectra \stackrel{\overset{L}{\longrightarrow}}{\underset{\ell}{\longleftarrow}} Spectra$ be the 1-categorical [[adjunction]] between spectra and prespectra, in the sense defined at [[coordinate-free spectrum]], where $\ell$ is the forgetful functor. For $E$ a spectrum and $X$ a [[pointed topological space]], write

$$
  E \wedge X \coloneqq L(\ell E \wedge X)
$$

for the spectrification of the degreewise [[smash product]] of [[pointed objects]]. Write $I_+$ for the unit [[interval]] with a base point adjoined.

A _[[left homotopy]]_ between maps of spectra $E_1$ and $E_2$ is a morphism of spectra

$$
  E_1\wedge I_+ \longrightarrow E_2
  \,.
$$

Write $[E_1,E_2]$ for the [[homotopy classes]] of maps. The stable homotopy category is equivalently the category of spectra of CW-type with these homotopy classes of maps between them.

([Elmendorf-Kriz-May, p. 8](#ElmendorfKrizMay))

Restricted to [[suspension spectra]] this is equivalently the [[colimit]] over all [[reduced suspensions]] of [[homotopy classes]] of topological spaces:

$$
  [\Sigma^\infty X_1, \Sigma^\infty X_2]
    \simeq
  \underset{\longrightarrow}{\lim}_{n} [\Sigma^n X, \Sigma^n Y]
  \,.
$$ 

For the analogous construction in [[equivariant stable homotopy theory]] see ([Greenlees-May 95, section 2](#GreenleesMay95))

## Related concepts

* [[Whitehead theorem]]

## References

* [[Dieter Puppe]], _On the stable homotopy category_, Topology and its application (1973)  ([[PuppeStableHomotopyCategory.pdf:file]])

* Cary Malkiewich, _The stable homotopy category_ ([pdf](http://math.stanford.edu/~carym/stable.pdf))

* {#ElmendorfKrizMay} [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], _Modern foundations for stable homotopy theory_, in I. M. James (ed.), _Handbook of algebraic topology_, Amsterdam: North-Holland, pp. 213&#8211;253,  ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))

* {#GreenleesMay95} [[John Greenlees]], [[Peter May]], _Equivariant stable homotopy theory_, in I.M. James (ed.), _Handbook of Algebraic Topology_ , pp. 279-325. 1995. ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

