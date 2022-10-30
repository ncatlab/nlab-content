
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

Given a [[spectrum]] $X$, and a [[ring spectrum]] $E$, then the _$E$-nilpotent completion_ of $X$ at $E$ is, for any choice $X_\bullet \to X$ of $E$-[[Adams tower]], the [[homotopy limit]] $\underset{\longleftarrow}{\lim} X_\bullet$ over that tower ([Ravenel 84, def. 1.13](#Ravenel84)).

Under certain finiteness conditions (see [below](#RelationToELocalization)), but not generally, this is equivalent to the $E$-[[Bousfield localization of spectra|Bousfield localization]] $L_E X$ (which, in turn, is in special cases given by [[formal completion]], see at _[[fracture theorem]]_).

The $E$-[[Adams spectral sequence]] induced by the given [[Adams tower]] [[conditionally converges]] to the $E$-nilpotent completion.

## Properties

### Relation to $E$-localization
 {#RelationToELocalization}

+-- {: .num_remark #CanonicalMapFromELocalizationToTotalization}
###### Remark

There is a canonical map

$$
  L_E X \stackrel{}{\longrightarrow} \underset{\leftarrow}{\lim}_n (E^{\wedge^{n+1}_S}\wedge_S X)
$$

from the $E$-[[Bousfield localization of spectra]] of $X$ into the [[totalization]].


=--

We consider now conditions for this morphism to be an [[equivalence]].

+-- {: .num_defn #CoreOfARing}
###### Definition

For $R$ a [[ring]], its _core_ $c R$ is the [[equalizer]] in

$$
  c R 
    \longrightarrow 
  R 
    \stackrel{\longrightarrow}{\longrightarrow}
  R \otimes R
  \,.
$$

=--

+-- {: .num_prop #SufficientConditionsForTotalizationToBeELocalization}
###### Proposition

Let $E$ be a [[connective spectrum|connective]] [[E-∞ ring]] such that the core of $\pi_0(E)$, def. \ref{CoreOfARing}, is either of

* the [[localization of a ring|localization]] of the [[integers]] at a set $J$ of [[primes]], $c \pi_0(E) \simeq \mathbb{Z}[J^{-1}]$;

* $\mathbb{Z}_n$ for $n \geq 2$.

Then the map in remark \ref{CanonicalMapFromELocalizationToTotalization} is an equivalence

$$
  L_E X \stackrel{\simeq}{\longrightarrow} 
  \underset{\leftarrow}{\lim}_n (E^{\wedge^{n+1}_S}\wedge_S X)
  \,.
$$

=--

([Bousfield 79](#Bousfield79)).



## Examples

* The nilpotent completion of a [[connective spectrum]] at the [[Eilenberg-MacLane spectrum]] $H \mathbb{Z}$, happens to be the spectrum itself (by a [[Postnikov tower]] argument).

## Related concepts

* [[formal completion]]

## References

Original references include

* {#Ravenel84} [[Douglas Ravenel]], _Localization with respect to certain periodic homology theories_, American Journal of Mathematics, Vol. 106, No. 2, (Apr., 1984), pp. 351-414 ([pdf](https://www.math.rochester.edu/people/faculty/doug/mypapers/loc.pdf))

Lecture notes include

* {#Hopkins99} [[Mike Hopkins]], section 4 of _Complex oriented cohomology theories and the language of stacks_, course notes 1999 ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/coctalos.pdf))

Discussion of the conditions under which $E$-nilpotent completion gives $E$-localization is due to

* {#Bousfield79} [[Aldridge Bousfield]], _The localization of spectra with respect to homology_, Topology 18 (1979), no. 4, 257--281. ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))

* {#Ravenel84} [[Douglas Ravenel]], _Localization with respect to certain periodic homology theories_, American Journal of Mathematics, Vol. 106, No. 2, (Apr., 1984), pp. 351-414 ([pdf](https://www.math.rochester.edu/people/faculty/doug/mypapers/loc.pdf))

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_ (2010) lecture 30: _Localizations and the Adams-Novikov Spectral Sequence_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture30.pdf))


See also

* {#Carlsson07} [[Gunnar Carlsson]], _Derived completions in stable homotopy theory_ ([arXiv:0707.2585](http://arxiv.org/abs/0707.2585))


[[!redirects E-nilpotent completions]]

[[!redirects nilpotent completion]]
[[!redirects nilpotent completions]]
