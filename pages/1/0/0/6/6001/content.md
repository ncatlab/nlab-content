
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

Among [[sequential spectrum|sequential]] [[pre-spectra]] $X$, the $\Omega$-spectra are those for which the structure maps $X_n \to \Omega X_{n+1}$ (from each component space to the [[based loop space]] of the next component space) are a [[weak homotopy equivalence]].  

(Beware that some authors require a [[homeomorphism]] instead and say "weak $\Omega$-spectrum", for the more general case).

Omega-spectra are particularly good representatives among [[pre-spectra]] of the objects of the [[stable (∞,1)-category of spectra]], hence of the [[stable homotopy category]]. For instance they are (after [[geometric realization]]) the [[fibrant objects]] of the [[Bousfield-Friedlander model structure]].

## Definition


With $\Omega$ the notation for the [[loop space]] construction (whence the name),an $\Omega$-spectrum is a sequence $E_\bullet = (E_n)_{n \in \mathbb{N}}$ of [[pointed object|pointed]] [[∞-groupoids]] ([[homotopy types]]) equipped for each $n \in \mathbb{N}$ with an [[equivalence of ∞-groupoids]]

$$
  E_n \stackrel{\simeq}{\longrightarrow} \Omega E_{n+1}
  \,.
$$ 

Remark: In terms of [[model category]] [[presentable (∞,1)-category|presentation]] one may also consider sequences of [[topological spaces]] equipped with _[[homeomorphisms]]_ $E_n \longrightarrow \Omega E_{n+1}$  See at _[[spectrum]]_ the section _[Omega-spectra](spectrum#OmegaSpectrum)_.

## Properties

### $\Omega$-spectrification

The inclusion of $\Omega$-spectra into all sequential pre-spectra has a [[left adjoint]], [[spectrification]]. See there for more.

## Examples

### $\Omega$-spectrification of suspension spectra
 {#CompletionOfSuspensionSpectra}

Given a [[pointed topological space]] $X$, its [[suspension spectrum]] $\Sigma^\infty X$ is far from being an $\Omega$-spectrum. The $\Omega$-spectrum that it induces (its [[spectrification]]) is given by [[free infinite loop space]] constructions:

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

### K-theory spectrum

The standard incarnation of the spectrum [[Brown representability theorem|representing]] complex and real [[topological K-theory]] $K U$ and $K O$ is already an $\Omega$-spectrum, due to [[Bott periodicity]]

$$
  \Omega^2(B U \times \mathbb{Z}) \simeq B U \times \mathbb{Z}
$$

and

$$
  \Omega^8 B O \simeq B O \times \mathbb{Z}
  \,.
$$


## Related concepts

* [[coordinate-free spectrum]]

* [[excisive functor]]

## References

* {#Adams74} [[Frank Adams]], part III, section 2 of _[[Stable homotopy and generalised homology]]_, 1974

* {#ElmendorfKrizMay95} [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], section 1 of  _[[Modern foundations for stable homotopy theory]]_, in [[Ioan Mackenzie James]], _[[Handbook of Algebraic Topology]]_, Amsterdam: North-Holland (1995) pp. 213&#8211;253,  ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))

* {#Kochmann96} [[Stanley Kochmann]], section 3.3 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Malkiewich14} [[Cary Malkiewich]], section 2.2 of _The stable homotopy category_, 2014 ([pdf](http://math.stanford.edu/~carym/stable.pdf))


[[!redirects Omega-spectra]]

[[!redirects Omega spectrum]]
[[!redirects Omega spectra]]

