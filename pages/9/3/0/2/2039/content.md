
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

What is called _Bredon cohomology_ after ([Bredon 67a](#Bredon67a), [Bredon 67a](#Bredon67a)) is the flavor of [[ordinary cohomology|ordinary]] $G$-[[equivariant cohomology]] which uses the "fine" [[equivariant homotopy theory]] of [[topological G-spaces]] that by [[Elmendorf's theorem]] is equivalent to the [[homotopy theory]] of [[(∞,1)-presheaves]] over $G$-[[orbit category]], instead of  the "coarse" [[Borel model structure|Borel homotopy theory]]. See at _[Equivariant cohomology -- Idea](equivariant+cohomology#Idea)_ for more motivation.

For more technical details see there _[equivariant cohomology -- Bredon equivariant cohomology](equivariant+cohomology#Bredon)_.

## Definition
 {#Definition}

Let $G$ be a [[compact Lie group]], write $Orb_G$ for its [[orbit category]] and write $PSh_\infty(Orb_G)$ for the [[(∞,1)-category of (∞,1)-presheaves]] over $Orb_G$. By [[Elmendorf's theorem]] this is [[equivalence of (∞,1)-categories|equivalent]] to the [[homotopy theory]] of [[topological G-spaces]] with weak equivalences the $H$-[[fixed point]]-wise [[weak homotopy equivalences]] for all closed subgroups $H$ ("the [[equivariant homotopy theory]]"):

$$
  \mathbf{H}^{Orb_G^{op}} \coloneqq  L_{fpwe} G Top \simeq PSh_\infty(Orb_G)
  \,.
$$

A [[spectrum object]] $E \in Stab(\mathbf{H}^{Orb_G^{op}})$ in the [[(∞,1)-topos]] $\mathbf{H}^{Orb_G^{op}}$ is what is called a [[spectrum with G-action]] or, for better or worse, a "[[naive G-spectrum]]".

For $X$ a [[G-space]], then its [[cohomology]] in $\mathbf{H}^{Orb_G^{op}}$ with [[coefficients]] in such $A$ might be called _generalized Bredon cohomology_ (in the "generalized" sense of [[generalized (Eilenberg-Steenrod) cohomology]]).

Specifically for $n \in \mathbb{N}$ and $A \in Ab(Sh(Orb_G))$ an [[abelian sheaf]] then there is an [[Eilenberg-MacLane object]]

$$
  K(n,A) \in \mathbf{H}^{Orb_G^{op}}
$$

whose [[categorical homotopy groups in an (infinity,1)-topos|categorical homotopy groups]] are concentrated in degree $n$ on $A$.

Then _ordinary Bredon cohomology_ (in the "ordinary" sense of [[ordinary cohomology]]) in degree $n$ with [[coefficients]] in $A$ is cohomology in $\mathbf{H}^{Orb_G^{op}}$ with coefficients in $K(n,A)$:

$$
  H_G^n(X,A) \simeq \pi_0 \mathbf{H}^{Orb_G^{op}}(X,A)
$$

(see the general discussion at _[[cohomology]]_).

If here $X$ is presented by a [[G-CW complex]] and hence is cofibrant in the [[model category]] structure that presents the [[equivariant homotopy theory]] (see at _[[Elmendorf's theorem]]_ for details), then the [[derived hom space]] on the right above is equivalently given by the ordinary $G$-[[fixed points]] of the ordinary [[mapping space]] of the [[topological space]] underlying the [[G-spaces]].

$$
  H_G^n(X,A) \simeq \pi_0 [X,A]_G
  \,.
$$

In this form ordinary Bredon cohomology is expressed in ([Bredon 67a, p. 3](#Bredon67a), [Bredon 67b, Theorem (2.11), (6.1)](#Bredon67b)), review in in ([Greenlees-May, p. 10](#GreenleesMay)).

The definition of Bredon cohomology which is more popular ([Bredon 67a, p. 2](#Bredon67a), [Bredon 67b, I.6](#Bredon67b)) is a [[chain complex]]-model for this: regarding $X$ again as a presheaf on the [[orbit category]], define a presheaf of chain complexes

$$
  C_\bullet(X) \;\colon\; Orb_G^{op}\longrightarrow Ch_\bullet 
$$

by 

$$
  C_n(X)(G/H) \coloneqq H_n((X^n)^H, (X^{n-1})^H, \mathbb{Z})
  \,,
$$

where on the right we have the [[relative homology]] of the [[CW complex]] decomposition underlying the [[G-CW complex]] $X$ in degrees as indicated. The [[differential]] on these chain complexes is defined in the obvious way (...).

Then one has an expression for _ordinary Bredon cohomology_  similar to that of [[singular cohomology]] as follows:

$$
  H_G^n(X,A) \simeq H_n(Hom_{Orb_G}(C_\bullet(X,)A))
  \,.
$$

(due to [Bredon 67](#Bredon67), see e.g. ([Greenlees-May, p. 9](#GreenleesMay))).

More generally there is $RO(G)$-graded [[equivariant cohomology]] with [[coefficients]] in [[genuine G-spectra]]. This is _also_ sometimes still referred to as "Bredon cohomology". For more on this see at _[equivariant cohomology -- Bredon cohonology](equivariant%20cohomology#Bredon)_.


## Examples

### With coefficients in representation ring

[[!include incarnations of rational equivariant topological K-theory -- table ]]

## Related concepts

* [[equivariant cohomology]], [[equivariant homotopy theory]]

* [[Elmendorf's theorem]]

* [[twisted Bredon cohomology]]

* [[global equivariant homotopy theory]]

* [[global equivariant stable homotopy theory]]

* [[orbifold cohomology]]

[[!include equivariant cohomology -- table]]

## References

The original text is

* {#Bredon67b} [[Glen Bredon]], _[[Equivariant cohomology theories]]_, Springer Lecture Notes in Mathematics Vol. 34. 1967 ([doi:10.1007/BFb0082690](https://link.springer.com/book/10.1007/BFb0082690))

announced in

* {#Bredon67a} [[Glen Bredon]], _Equivariant cohomology theories_, Bull. Amer. Math. Soc. Volume 73, Number 2 (1967), 266-268. ([educlid:1183528794](https://projecteuclid.org/euclid.bams/1183528794))

Also

* [[Sören Illman]], _Equivariant singular homology and cohomology_, Bull. Amer. Math. Soc. Volume 79, Number 1 (1973), 188-192 ([euclid:bams/1183534324](https://projecteuclid.org/euclid.bams/1183534324))



Reviews include



* {#Blumberg17} [[Andrew Blumberg]], section 1.4 of _Equivariant homotopy theory_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))

* {#tomDieck87} [[Tammo tom Dieck]], Section II.9 of: _[[Transformation Groups]]_, de Gruyter 1987  ([doi:10.1515/9783110858372]( https://doi.org/10.1515/9783110858372))


* {#GreenleesMay} [[John Greenlees]], [[Peter May]], pages 9-10 of _[[Equivariant stable homotopy theory]]_, chapter 8, pages 277-323 in: [[Ioan James]] (ed.), _[[Handbook of Algebraic Topology]]_, North-Holland, Amsterdam, 1995. ([doi:10.1016/B978-0-444-81779-2.X5000-7](https://doi.org/10.1016/B978-0-444-81779-2.X5000-7), [pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

* {#May96} [[Peter May]], section I.4 of _Equivariant homotopy and cohomology theory_ CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996. With contributions by M. Cole, G. Comezana, S. Costenoble, A. D. Elmenddorf, J. P. C. Greenlees, L. G. Lewis, Jr., R. J. Piacenza, G. Triantafillou, and S. Waner. ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/alaska1.pdf), [[MayEtAlEquivariant96.pdf:file]])

* Paolo Masulli, section 2 of _Equivariant homotopy: $KR$-theory_, Master thesis (2011) ([pdf](http://www.math.ku.dk/~jg/students/masulli.msthesis.2011.pdf))

The [[Eilenberg-MacLane objects]] over the [[orbit category]] are discussed in detail in 

* {#Lewis92} [[L. Gaunce Lewis, Jr.]], _Equivariant Eilenberg-MacLane spaces and the equivariant Seifert-van Kampen suspension theorems_, Topology Appl., 48 (1992), no. 1, pp. 25&#8211;61 (<a href="https://doi.org/10.1016/0166-8641(92)90120-O">doi:10.1016/0166-8641(92)90120-O</a>)

Equivalence of Bredon cohomology of [[topological G-spaces]] $X$ to [[abelian sheaf cohomology]] of the [[topological quotient space]] $X/G$ with [[coefficients]] a "[[locally constant sheaf]] except for dependence on [[isotropy groups]]":

* {#Honkasalo88} [[Hannu Honkasalo]], _Equivariant Alexander-Spanier cohomology_,  Mathematica Scandinavia,  63, 179-195, 1988 ([doi:10.7146/math.scand.a-12232](https://doi.org/10.7146/math.scand.a-12232))

  (for [[finite groups]])

* {#Honkasalu90} [[Hannu Honkasalo]], _Equivariant Alexander-Spanier cohomology for actions of compact Lie groups_, Mathematica Scandinavica Vol. 67, No. 1 (1990), pp. 23-34 ([jstor:24492569](https://www.jstor.org/stable/24492569))
 
  (for [[compact Lie groups]])

* {#Honkasalo96} [[Hannu Honkasalo]], _Sheaves on fixed point sets and equivariant cohomology_, Math. Scand. __78__ (1996), 37--55 ([jstor:](https://www.jstor.org/stable/24492815))

  (reformulation in [[topos theory]])

See also at _[[orbifold cohomology]]_.


Equivalent formulation using the [[Grothendieck construction]] for a certain [[Cat]]-valued [[presheaf]] on the [[orbit category]]"

* [[Ieke Moerdijk|I. Moerdijk]], J-A. Svensson, _The equivariant Serre spectral sequence_, Proc. Amer. Math. Soc. __118__ (1993), no. 1, 263--278 [doi:10.2307/2160037](http://dx.doi.org/10.2307/2160037)

Further remarks on this and on the [[twisted cohomology]]-version is in

* Goutam Mukherjee, N. Pandey, _Equivariant cohomology with local coefficients_ ([pdf](http://www.ams.org/proc/2002-130-01/S0002-9939-01-06377-8/S0002-9939-01-06377-8.pdf))

* Amiya Mukherjee, Goutam Mukherjee, _Bredon-Illman cohomology with local coefficients_, The Quarterly Journal of Mathematics, Volume 47, Issue 2, June 1996, Pages 199–219 ([doi:10.1093/qmath/47.2.199](https://doi.org/10.1093/qmath/47.2.199))


* {#Honkasalo97} [[Hannu Honkasalo]], _A sheaf-theoretic approach to the equivariant Serre spectral sequence_, J. Math. Sci. Univ. Tokyo 4 (1997), 53--65 ([pdf](http://journal.ms.u-tokyo.ac.jp/pdf/jms040103.pdf))

* Samik Basua, Debasis Sen, _Representing Bredon cohomology with local coefficients_, Journal of Pure and Applied Algebra Volume 219, Issue 9, September 2015, Pages 3992-4015 ([doi:10.1016/j.jpaa.2015.02.001](https://doi.org/10.1016/j.jpaa.2015.02.001))

See also at _[[orbifold cohomology]]_.

[[!redirects Bredon-Illman cohomology]]

[[!redirects Bredon equivariant cohomology]]
