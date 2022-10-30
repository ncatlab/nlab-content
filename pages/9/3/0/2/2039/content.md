
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

What is called _Bredon cohomology_ after ([Bredon 67](#Bredon67)) is the flavor of $G$-[[equivariant cohomology]] which uses the "fine" [[equivariant homotopy theory]] of [[topological G-spaces]] that by [[Elmendorf's theorem]] is equivalent to the [[homotopy theory]] of [[(∞,1)-presheaves]] over $G$-[[orbit category]], instead of  the "coarse" [[Borel model structure|Borel homotopy theory]]. See at _[Equivariant cohomology -- Idea](equivariant+cohomology#Idea)_ for more motivation.

For more technical details see there _[equivariant cohomology -- Bredon equivariant cohomology](equivariant+cohomology#Bredon)_.

## Definition
 {#Definition}

Let $G$ be a [[compact Lie group]], write $orb_G$ for its [[orbit category]] and write $PSh_\infty(Orb_G)$ for the [[(∞,1)-category of (∞,1)-presheaves]] over $Orb_G$. By [[Elmendorf's theorem]] this is [[equivalence of (∞,1)-categories|equivalent]] to the [[homotopy theory]] of [[topological G-spaces]] with weak equivalences the $H$-[[fixed point]]-wise [[weak homotopy equivalences]] for all closed subgroups $H$ ("the [[equivariant homotopy theory]]"):

$$
  \mathbf{H}_{/\mathbf{B}G} \coloneqq  L_{fpwe} G Top \simeq PSh_\infty(Orb_G)
  \,.
$$

A [[spectrum object]] $E \in Stab(\mathbf{H}_{/\mathbf{B}G})$ in the [[(∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}G}$ is what is called a [[spectrum with G-action]] or, for better or worse, a "[[naive G-spectrum]]".

For $X$ a [[G-space]], then its [[cohomology]] in $\mathbf{H}_{/\mathbf{B}G}$with [[coefficients]] in such $A$ might be called _generalized Bredon cohomology_ (in the "generalized" sense of [[generalized (Eilenberg-Steenrod) cohomology]]).

Specifically for $n \in \mathbb{N}$ and $A \in Ab(Sh(Orb_G))$ an [[abelian sheaf]] then there is an [[Eilenberg-MacLane object]]

$$
  K(n,A) \in \mathbf{H}_{\mathbf{B}G}
$$

whose [[categorical homotopy groups in an (infinity,1)-topos|categorical homotopy groups]] are concentrated in degree $n$ on $A$.

Then _ordinary Bredon cohomology_ (in the "ordinary" sense of [[ordinary cohomology]]) in degree $n$ with [[coefficients]] in $A$ is cohomology in $\mathbf{H}_{/\mathbf{B}G}$ with coefficients in $K(n,A)$:

$$
  H_G^n(X,A) \simeq \pi_0 \mathbf{H}_{/\mathbf{B}G}(X,A)
$$

(see the general discussion at _[[cohomology]]_).

If here $X$ is presented by a [[G-CW complex]] and hence is cofibrant in the [[model category]] structure that presents the [[equivariant homotopy theory]] (see at _[[Elmendorf's theorem]]_ for details), then the [[derived hom space]] on the right above is equivalently given by the ordinary $G$-[[fixed points]] of the ordinary [[mapping space]] of the [[topological space]] underlying the [[G-spaces]].

$$
  H_G^n(X,A) \simeq \pi_0 [X,A]_G
  \,.
$$

In this form ordinary Bredon cohomology appears for instance in ([Greenlees-May, p. 10](#GreenleesMay)).

But what ([Bredon 67](#Bredon67)) _really_ wrote down is a [[chain complex]]-model for this: regarding $X$ again as a presheaf on the [[orbit category]], define a presheaf of chain complexes

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


## Related concepts

* [[equivariant cohomology]], [[equivariant homotopy theory]]

* [[Elmendorf's theorem]]

* [[global equivariant homotopy theory]]

* [[global equivariant stable homotopy theory]]

[[!include equivariant cohomology -- table]]

## References

The original text is

* {#Bredon67} [[Glen Bredon]], _Equivariant cohomology theories_, Springer Lecture Notes in Mathematics Vol. 34. 1967.

Reviews include

* {#GreenleesMay} [[John Greenlees]], [[Peter May]], pages 9-10 of _Equivariant stable homotopy theory_ ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

* {#May96} [[Peter May]], section I.4 of _Equivariant homotopy and cohomology theory_ CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996. With contributions by M. Cole, G. Comezana, S. Costenoble, A. D. Elmenddorf, J. P. C. Greenlees, L. G. Lewis, Jr., R. J. Piacenza, G. Triantafillou, and S. Waner. ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/alaska1.pdf))
* Paolo Masulli, section 2 of _Equivariant homotopy: $KR$-theory_, Master thesis (2011) ([pdf](http://www.math.ku.dk/~jg/students/masulli.msthesis.2011.pdf))

The [[Eilenberg-MacLane objects]] over the orbit category are discussed in detail in 

* {#Lewis92} L. G. Lewis, _Equivariant Eilenberg-MacLane spaces and the equivariant Seifert-van Kampen suspension theorems_, Topology Appl., 48 (1992), no. 1, pp. 25&#8211;61.


There is an interesting (nontrivially) equivalent definition by Moerdijk and Svensson, using the [[Grothendieck construction]] for a certain $Cat$-valued presheaf on the orbit category. 

* [[Ieke Moerdijk|I. Moerdijk]], J-A. Svensson, _The equivariant Serre spectral sequence_, Proc. Amer. Math. Soc. __118__ (1993), no. 1, 263--278 [doi:10.2307/2160037](http://dx.doi.org/10.2307/2160037)

Further remarks on this and on the [[twisted cohomology]]-version is in

* G. Mukherjee, N. Pandey, _Equivariant cohomology with local coefficients_ ([pdf](http://www.ams.org/proc/2002-130-01/S0002-9939-01-06377-8/S0002-9939-01-06377-8.pdf))

* H. Honkasalo, _Sheaves on fixed point sets and equivariant cohomology_, Math. Scand. __78__ (1996), 37--55 ([pdf](http://www.mscand.dk/article.php?id=1099))

* H. Honkasalo, _A sheaf-theoretic approach to the equivariant Serre spectral sequence_, J. Math. Sci. Univ. Tokyo
4 (1997), 53--65 ([pdf](http://journal.ms.u-tokyo.ac.jp/pdf/jms040103.pdf))

For [[orbifolds]] there is a generalization of $K$-theory which is closely related to the Bredon cohomology (rather than usual equivariant cohomology):

* Alejandro Adem, Yongbin Ruan, _Twisted Orbifold K-Theory_, Commun.Math.Phys. 237 (2003) 533-556, [doi:10.1007/s00220-003-0849-x](http://dx.doi.org/10.1007/s00220-003-0849-x) ([arXiv:0107.5168](http://front.math.ucdavis.edu/0107.5168))


