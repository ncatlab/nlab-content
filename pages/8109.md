
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea


By the construction of [[complex oriented cohomology theories]] from [[formal groups]] (via the [[Landweber exact functor theorem]]), the [[height of a formal group|height filtration]] of formal groups induces a "[[chromatic filtration|chromatic]]" [[filtration]] on [[complex oriented cohomology theories]]. 
_Chromatic homotopy theory_ is the study of [[stable homotopy theory]] and specifically of [[complex oriented cohomology theories]] by means of and along this [[chromatic filtration]].

More abstractly, this filtering is induced by the [[prime spectrum of a symmetric monoidal stable (∞,1)-category]] of the [[(∞,1)-category of spectra]] for [[p-localization|p-local]] [[finite spectra]], which is labeled by the [[Morava K-theories]].

More in detail, for each [[prime]] $p \in \mathbb{N}$ and for each  $n \in \mathbb{N}$ there is a [[Bousfield localization of spectra]]

$$
  L_n \coloneqq L_{K(0)\vee \cdots \vee K(n)}
  \,,
$$

where $K(n)$ is the $n$th [[Morava K-theory]] (for the given [[prime]] $p$). These arrange into the [[chromatic tower]] which for each spectrum $X$ is of the form

$$  
  X \to \cdots \to L_n X \to L_{n-1} X \to \cdots \to L_0 X
  \,.
$$

The [[chromatic convergence theorem]] states mild conditions under which the [[homotopy limit]] over this tower is the $p$-[[Bousfield localization of spectra|localization]] 

$$
  X \to X_{(p)}
$$

of $X$. 

Since moreover $L_n X$ is the [[homotopy fiber product]] (see at _[[smash product theorem]]_ and see [this remark](fracture+theorem#ExampleOfChromaticFracturing) at _[[fracture square]]_ )

$$
  L_n X \simeq L_{K(n)}X \underset{L_{n-1}L_{K(n)}X}{\times} L_{n-1}X
$$

it follows that in principle one may study a spectrum $X$ by understanding all its "chromatic pieces" $L_{K(n)} X$. 


## Examples

[[!include chromatic tower examples - table]]

## Related concepts

* motivation: [[J-homomorphism and chromatic homotopy]]

* [[stable homotopy theory]]

* [[stable homotopy groups of spheres]], [[J-homomorphism]]

* [[complex oriented cohomology theory]]

* [[complex cobordism cohomology theory]], [[MU]]

  * [[Lazard's theorem]]

  * [[Quillen's theorem on MU]]

  * [[Landweber exact functor theorem]]

  * [[Landweber-Novikov theorem]]

  * [[Brown-Peterson spectrum]]

* [[formal group law]]

  * [[moduli stack of formal groups]]

  * [[height of a formal group]]

  * [[Morava stabilizer group]]

* [[Morava K-theory]]

  * [[∞-field]]

  * [[integral Morava K-theory]]

  * [[K(n)-local stable homotopy theory]]

  * [[Bousfield-Kuhn functor]]

* [[Morava E-theory]]

  * [[Lubin-Tate theory]]

* [[chromatic filtration]]

  * [[chromatic localization]]

  * [[chromatic tower]]

  * [[monochromatic layer]]

  * [[periodicity theorem]]

  * [[chromatic convergence theorem]]

* [[telescopic complexity]], [[telescopic localization]]

* [[Adams spectral sequence]]

  * [[Steenrod algebra]], [[Adams operation]]

  * [[chromatic spectral sequence]], [[May spectral sequence]]

* [[algebraic K-theory]], [[red-shift conjecture]]

* [[transchromatic character]]

* [[motivic chromatic homotopy theory]]



## References 
 {#References}

### Stable case

Original articles include

* {#Ravenel84} [[Douglas Ravenel]], _Localization with Respect to Certain Periodic Homology Theories_, American Journal of Mathematics Vol. 106, No. 2 (Apr., 1984), pp. 351-414 ([doi:10.2307/2374308](https://doi.org/10.2307/2374308), [jstor:2374308](https://www.jstor.org/stable/2374308))


A quick idea is given in section 6 of 

* [[Mark Mahowald]], [[Doug Ravenel]], _Towards  a Global Understanding of the Homotopy Groups of Spheres_, pages 57-74 in Part II of: _The Lefschetz Centennial Conference -- Proceedings on Algebraic Topology_, Proceedings of the Lefschetz Centennial Conference held December 10-14, 1984, Contemporary Mathematics 58, American Mathematical Society, 1987.  ([ISBN:978-0-8218-5063-3](https://bookstore.ams.org/conm-58-2), [pdf](http://www.math.rochester.edu/people/faculty/doug/mypapers/global.pdf), [[MahowaldRavenelHomotopyGroupsOfSpheres.pdf:file]])

A good historical introduction is in 

* [[Jack Morava]], _Complex cobordism and algebraic topology_ ([arXiv:0707.3216](http://arxiv.org/abs/0707.3216))


Comprehensive lecture notes are in

* {#LurieLectures} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010 ([lecture notes](http://www.math.harvard.edu/~lurie/252x.html))
 

* [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_

Brief surveys include

* [[Haynes Miller]], _"Chromatic" homotopy theory_ May 2011 ([pdf](http://www-math.mit.edu/~hrm/papers/chromatic.pdf))

A lightning review of results by Henn with Goerss, Mahowald, Rezk, and Karamanov is in 

* Hans-Werner Henn, _Recent developments in stable homotopy theory_ ([pdf](https://etale.site/livetex/saft/henn.pdf),)

A collection of various lecture notes and other material is kept at

* [Talbot 2013: Chromatic Homotopy Theory](http://math.mit.edu/conferences/talbot/index.php?year=2013), _[2013 Pre-Talbot Seminar Chromatic homotopy theoy](https://www.hiroleetanaka.com/pretalbot2013/index.php)_

See also:

* Glossary for stable and chromatic honotopy theory ([[StableChromaticGlossary.pdf:file]])


Discussion of generalization of [[elliptic cohomology]] to higher chromatic homotopy theory is discussed in

* [[Doug Ravenel]], _Toward higher chromatic analogs of elliptic cohomology_ [pdf](http://www.math.rochester.edu/people/faculty/doug/mypapers/high1.pdf)

* [[Doug Ravenel]], _Toward higher chromatic analogs of elliptic cohomology II_, Homology, Homotopy and Applications, vol. 10(1), 2008, pp.1-36 ([pdf](http://www.math.rochester.edu/people/faculty/doug/mypapers/high2.pdf), [pdf slides](http://www.math.rochester.edu/people/faculty/doug/mypapers/halifax.pdf))

Relation of chromatic homotopy theory to [[Goodwillie calculus]] is discussed in

* [[Greg Arone]], [[Mark Mahowald]], _The Goodwillie tower of the identity functor and the unstable periodic homotopy of spheres_, Inventiones mathematicae, February 1999, Volume 135, Issue 3, pp 743-788 ([pdf](http://hopf.math.purdue.edu/Arone-Mahowald/ArMahowald.pdf), [doi:10.1007/s002220050300](https://doi.org/10.1007/s002220050300))

* [[Nicholas Kuhn]], _Goodwillie towers and chromatic homotopy: an overview_,   Proceedings of the Nishida Fest (Kinosaki 2003),  245--279, Geom. Topol. Monogr., 10, Geom. Topol. Publ., Coventry, 2007 ([arXiv:math/0410342](https://arxiv.org/abs/math/0410342), [doi:10.2140/gtm.2007.10.245](http://dx.doi.org/10.2140/gtm.2007.10.245))

Categorical [[ultraproducts]] are used to provide asymptotic approximations in

* [[Tobias Barthel]], [[Tomer Schlank]], [[Nathaniel Stapleton]], _Chromatic homotopy theory is asymptotically algebraic_, ([arXiv:1711.00844](https://arxiv.org/abs/1711.00844))

### Unstable case

There are also chromatic approximations in ordinary (not [[stabilization|stabilized]]) [[homotopy theory]]:

* [[Aldridge Bousfield]], _Localization and periodicity in unstable homotopy theory_, J. Amer. Math. Soc. 7 (1994), 831-873 ([doi:10.1090/S0894-0347-1994-1257059-7](https://doi.org/10.1090/S0894-0347-1994-1257059-7), [jstor:2152734](https://www.jstor.org/stable/2152734))

* {#Heuts18} [[Gijs Heuts]], _Lie algebras and $v_n$-periodic spaces_ ([arXiv:1803.06325](https://arxiv.org/abs/1803.06325))

* {#LurieHopkins18} [[Jacob Lurie]], [[Michael Hopkins]], _Unstable Chromatic Homotopy Theory_, lecture notes 2018 ([web](http://math.harvard.edu/~lurie/Thursday2017.html))

[[!redirects chromatic level]]
[[!redirects chromatic filtration]]
[[!redirects chromatic levels]]
[[!redirects chromatic stable homotopy theory]]