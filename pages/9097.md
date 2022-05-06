
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[(∞,1)-topos]] of _synthetic differential super $\infty$-groupoids_ combines the properties of that of

1. [[smooth super ∞-groupoids]]

1. [[synthetic differential ∞-groupoids]].

## Definition

Let [[CartSp]]$_{supersynth}$ be the [[site]] which is the [[full subcategory]] of that of [[Isbell duality|formal duals]] of [[smooth superalgebras]] on those of the form 

$$
  \mathbb{R}^p \times D \times \mathbb{R}^{0|q}
  \simeq
  \mathbb{R}^{p|q} \times D
$$ 

where

* $\mathbb{R}^p$ is the [[Cartesian space]] of [[dimension]] $p$;

* $\mathbb{R}^{p|q}$ is the [[super vector space]] of dimension $(p|q)$ ($\mathbb{R}^{0|1}$ is the [[odd line]]);

* $D$ is an [[infinitesimally thickened point]].

If $D$ here is the formal dual of the [[Artin algebra]] on $k$ commuting nilpotent elements, then such an object is written $\mathbb{R}^{p \oplus k|q}$ in ([Konechny-Schwarz](#KonechnySchwarz)).

Let then 

$$
  SynthDiffSuper\infty Grpd
  \coloneqq
  Sh_\infty(CartSp_{supersynth})
$$

be the [[(∞,1)-category of (∞,1)-sheaves]] over this site.

## Related concepts

* [[cohesive (∞,1)-topos]]

  * [[discrete ∞-groupoid]]

  * [[Euclidean-topological ∞-groupoid]]

  * [[smooth ∞-groupoid]]

  * [[synthetic differential ∞-groupoid]]

  * [[super ∞-groupoid]]

  * [[smooth super ∞-groupoid]]



## References

* Anatoly Konechny and [[Albert Schwarz]], 

  _On $(k \oplus l|q)$-dimensional supermanifolds_ in _Supersymmetry and Quantum Field Theory_ ([[Dmitry Volkov]] memorial volume) Springer-Verlag (1998) Lecture Notes in Physics, 509 , J. Wess and V. Akulov (editors)([arXiv:hep-th/9706003](http://arxiv.org/abs/hep-th/9706003))

  _Theory of $(k \oplus l|q)$-dimensional supermanifolds_ Sel. math., New ser. 6 (2000) 471 - 486
  {#KonechnySchwarz}

* [[Urs Schreiber]], section 4.5 of: _[[schreiber:differential cohomology in a cohesive topos]]_

* [[Hisham Sati]], [[Urs Schreiber]], Section 3.1.3 of: _[[schreiber:Proper Orbifold Cohomology]]_ ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))

* [[Urs Schreiber]], _[[schreiber:Introduction to Higher Supergeometry]]_, lecture at _[[Higher Structures in M-Theory 2018]]_, [Durham Symposium](http://www.maths.dur.ac.uk/lms/)

  published in parts as: _Higher Structures in M-Theory_ (with [[Branislav Jurčo]], [[Christian Saemann]], [[Martin Wolf]]), Fortschritte der Physik (2019) ([arXiv:1903.02807](https://arxiv.org/abs/1903.02807), [doi:10.1002/prop.201910001]( https://doi.org/10.1002/prop.201910001))



[[!redirects synthetic differential super ∞-groupoid]]

[[!redirects synthetic differential super infinity-groupoids]]
[[!redirects synthetic differential super ∞-groupoids]]
