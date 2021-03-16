
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

The objects of [[equivariant stable homotopy theory]] -- genuine [[G-spectra]] -- are very rich: Already the [[fixed point spectra]] of [[equivariant suspension spectra]] contain considerably more information than just the [[suspension spectra]] of the plain underlying [[fixed point spaces]] -- the latter are just the _[[geometric fixed point spectra]].

The _tom Dieck splitting_  ([tom Dieck 75](#tomDieck75), [Lewis-May-Steinberger 86, V.11](#LewisMaySteinberger86)) gives an explicit description of all the [[wedge sum|wedge summands]] appearing in [[fixed point spectra]] of [[equivariant suspension spectra]]. These wedge sums start out with the [[geometric fixed point spectra]] and then have one summand for each [[conjugacy class]] of [[subgroups]] $H \subset G$, given by the plain [[suspension spectra]] of the [[homotopy quotient]] of the $H$-[[fixed point spaces]] by the corresponding [[Weyl group]]-[[action]].

Induced from this [[wedge sum]] splitting formula for the spectra themselves is a corresponding [[direct sum]]-formula of the [[equivariant stable homotopy groups]] in terms of plain [[stable homotopy groups]].

The richness of this splitting, hence of [[G-spectra]], is witnessed by its simplest non-trivial example, which is the [[equivariant stable homotopy groups]] of the [[equivariant sphere spectrum]]: This yields the [[abelian group]] underlying the [[Burnside ring]], which is [[free abelian group|freely generated]] from the [[conjugacy classes]] of [[subgroups]] of $G$ (see [below](#ForTheEquivariantSphereSpectrum)).

## Statement 

For $H\subset G$ a [[subgroup]], write

* $[H \subset G]$ for its [[conjugacy class]];

* $W_G H \coloneqq (N_G H)/H$ for its [[Weyl group]], the [[quotient group]] of the [[normalizer subgroup]] (of $H$ in $G$) by $H$;

* $E W_G H$ for the [[universal principal bundle]] of the [[Weyl group]].

### Of fixed point spectra of equivariant suspension spectra
 {#OfFixedPointSpectraOfEquivariantSuspensionSpectra}

The [[fixed point spectrum]] of an [[equivariant suspension spectrum]] is given by the [[wedge sum]] formula

$$
  F^G(\Sigma^\infty_G X)
  \simeq
  \underset{[H\subset G]}{\bigvee}
  \Sigma^\infty( E (W_G H)_+ \wedge_{W_G H} X^H )
$$

where $\Sigma^\infty$ is the plain [[suspension spectrum]] construction.

(e.g. [Guillou-May 12, theorem 5.3](#GuillouMay12), [Schwede 15, example 7.7](#Schwede15))

In particular, since $W_G G = 1$ and $W_G 1 = G$, the extremal summands for $H = G$ and $H = 1$ are just the [[suspension spectrum]] of the plain [[fixed point space]] $X^G$ and of the [[homotopy quotient]] $X\sslash G$ (equivalently the  [[Borel construction]] $X \sslash G \simeq E G_+ \times_G X$ ) of the full space, respectively:


$$
  F^G(\Sigma^\infty_G X)
  \simeq
  \Sigma^\infty( X^G )
    \vee
  \left(
    \underset{{[H\subset G]} \atop {1 \neq H \neq G}}{\bigvee}
    \Sigma^\infty( E (W_G H)_+ \wedge_{W_G H} X^H )
  \right)
    \vee
  \Sigma^\infty( E G_+ \wedge_{G} X )
  \,.
$$

Here the first summand is the _[[geometric fixed point spectrum]]_ inside the full [[fixed point spectrum]]

$$
  \Phi^G(\Sigma^\infty_G X) 
  \;\simeq\; 
  \Sigma^\infty( X^G )
  \hookrightarrow
  F^G(\Sigma^\infty_G X)
$$

([Schwede 15, Example 7.7](#Schwede15))


### For equivariant homotopy groups

It follows that for $X$ a pointed [[topological G-space]], its [[equivariant homotopy groups]] are  

$$
  \begin{aligned}
    \pi_\bullet^G(\Sigma^\infty X)
    & 
    \simeq
    \underset{[H \subset G]}{\bigoplus}
    \pi_\bullet^{W_G H}(\Sigma^\infty (E (W_G H)_+ \wedge X^H))
    \\
    &\simeq
    \pi_\bullet(\Sigma^\infty X^G)
    \oplus
    \underset{{[H \subset G]} \atop {1 \neq H \neq G}}{\bigoplus}
    \pi_\bullet^{W_G H}(\Sigma^\infty (E (W_G H)_+ \wedge X^H))
    \oplus
    \pi_\bullet^{G}(\Sigma^\infty (E G_+ \wedge X))
  \end{aligned}
$$

where the [[direct sum]] is over [[conjugacy classes]] of [[subgroups]] $H$ of $G$.

(e.g. [Schwede 15, theorem 6.12](#Schwede15))



### For rational equivariant homotopy theory


For $G$ finite and for [[rational equivariant stable homotopy theory]] this becomes ([Greenlees, 6.2](#Greenlees))

$$
  G RationalSpectra \simeq \underset{[H \subset G] }{\prod} \mathbb{Q}(W_G H) Mod
$$

where the product is over [[conjugacy classes]] of [[subgroups]] $H$ of $G$ and $W_G H$ denotes the [[Weyl group]] of $H$ in $G$

## Examples

### For the equivariant sphere spectrum
 {#ForTheEquivariantSphereSpectrum}

For the [[equivariant sphere spectrum]] $\mathbb{S} = \Sigma^\infty_G S^0$ the tom Dieck splitting says that its 0th [[equivariant homotopy group]]
is the [[free abelian group]] on the set of [[conjugacy classes]] of [[subgroups]] of $G$:

$$
  \pi_0^G(\mathbb{S})
  \simeq
  \underset{[H \subset G]}{\oplus} \pi_0^{W H}(\Sigma_+^\infty E W H)
  \simeq
  \mathbb{Z}\big[\text{conjugacy classes of subgroups}\big]
$$

(e.g. [Schwede 15, p. 64](#Schwede15))

This is the group underlying the [[Burnside ring]].


## Related concepts

* [[equivariant Whitehead theorem]]

* [[Elmendorf's theorem]]

* [[G-CW approximation]]

## References

The theorem at the level of [[stable homotopy groups]] is due to

* {#tomDieck75} [[Tammo tom Dieck]], Satz 2 of _Orbittypen und  &#x00E4;quivariante Homologie. II._, Arch. Math. (Basel) 26 (1975), no. 6, 650–662

The refinement to [[spectra]] is achieved in section V.11 of

* {#LewisMaySteinberger86} [[L. Gaunce Lewis]], [[Peter May]], and Mark Steinberger (with contributions by J.E. McClure), _Equivariant stable homotopy theory_, Springer Lecture Notes in Mathematics Vol.1213. 1986 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/equi.pdf))

An alternative proof is in

* {#GuillouMay12} [[Bert Guillou]], [[Peter May]], section 6.2 of _Permutative $G$-categories in equivariant infinite loop space theory_, Algebr. Geom. Topol. 17 (2017) 3259-3339 ([arXiv:1207.3459](http://arxiv.org/abs/1207.3459))


Detailed lecture notes are in

* {#Schwede15} [[Stefan Schwede]], section 6 of _[[Lectures on Equivariant Stable Homotopy Theory]]_, 2015 ([pdf](http://www.math.uni-bonn.de/people/schwede/equivariant.pdf))

* {#Blumberg17} [[Andrew Blumberg]], section 2.7 of _The Burnside category_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))

A brief mentioning appears in this survey of [[rational equivariant stable homotopy theory]]:

* {#Greenlees} [[John Greenlees]], p. 3 of _Triangulated categories of rational equivariant cohomology theories_ ([pdf](https://pdfs.semanticscholar.org/eda8/ee6effb2ae487085a2e7615a4a7e1964c493.pdf), [[GreenleesRationalEquivariant.pdf:file]])



[[!redirects tom  Dieck splittings]]

[[!redirects tom Dieck splitting theorem]]
[[!redirects tom Dieck splitting theorems]]
