
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[type II string theory]] on [[orientifolds]] ([Dai-Lin-Polchinski 89](#DaiLinPolchinski89)), one says _O-plane_ for the [[fixed point]] locus of the $\mathbb{Z}_2$-[[involution]] (see at _[[real space]]_).

O-planes carry [[D-brane charges]] in [[KR-theory]] ([Witten 98](#Witten98)), see ([DMR 13](#DMR13)) for a mathematical account. They serve [[RR-field tadpole cancellation]] and as such play a key role in the construction of [[intersecting D-brane models]] for [[string phenomenology]].

## Properties


### T-Duality with type I string theory
 {#TDualityWithTypeIStringTheory}

Under [[T-duality]], [[type I string theory]] is [[duality in string theory|dual]] to [[type II string theory]] with orientifold planes (reviewed e.g. in [Ibanez-Uranga 12, section 5.3.2 - 5.3.4](#IbanezUranga12)):

<img src="https://ncatlab.org/nlab/files/TDualityOrientifold.jpg" width="700">



### O-Plane charge
 {#OPlaneCharge}

O-planes carry effective negative [[RR-charge]] which may (must) cancel against the actual [[RR-charge|RR-]] [[D-brane charge]] via [[RR-field tadpole cancellation]].

#### For flat orientifolds
 {#OPlaneChargeForFlatOrientifolds}

The charge of the [[spacetime]]-filling $O9$-plane of plain [[type I string theory]] ([[type II string theory]] on the [[orientifold]] $\mathbb{R}^{9,1}\sslash \mathbb{Z}_2$ with [[trivial action|trival]] spacetime $\mathbb{Z}_2$-[[action]]) is found by [[worldsheet]]-computation to be $-32$ in [[physical unit|units]] of [[D9]]-[[D-brane charge|brane charge]]:

\[
  \label{O9PlaneCharge}
  q_{O9^-}
  \;=\;
  -32
  \,
  q_{D9}
\]


(e.g. [Blumenhagen-Lüst-Theisen 13 (9.83)](#BlumenhagenLustTheisen13)).

+-- {: .num_remark #ContingOfDBranesOnOrientifolds}
###### Remark
**counting of D-branes on orientifolds**

Beware that there is some convention involved in assigning an absolute value of unit D-brane charge $q_{D9}$. A common choice in the literature is to mean by "one D-brane" one of the two pre-images on the [[covering space]], in which case its obsolute charge is to be 



\[
  \label{DBraneChargeOnOrbifold}
  q_{Dp}
  \;=\;
   1/2
\]

(e.g. [BDHKMMS 01, p. 46-47](#BDHKMMS01)). From [BLT 13, p. 318](#BlumenhagenLustTheisen13):

<img src="https://ncatlab.org/nlab/files/DBraneCountingOnOrientifoldsI.jpg" width="500"/>


=--

This means that [[RR-field tadpole cancellation]] here requires the presence of 32 [[D-branes]] (or rather, by Remark \ref{ContingOfDBranesOnOrientifolds}: 16 and their $\mathbb{Z}_2$-mirror images), hence a space-filling [[D9-brane]] with [[Chan-Paton bundle]] of [[rank of a vector bundle|rank]] $32$, corresponding to a [[gauge group]] [[SO(32)]]. For more on this see at _[[type I string theory]] -- [Tadpole cancellation and SO(32)-GUT](type+I+string+theory#TadpoleCancellationAndSO32GUT)_.


From this the O$p^-$-brane charge for $p \leq n$ follows from [[T-duality]] (as [above](#TDualityWithTypeIStringTheory))
with respect to [[KK-compactification]] on a [[n-torus|d-torus]] $\mathbb{T}^d$ with $\mathbb{Z}_2$-[[action]] given by canonical [[coordinate function|coordinate]] [[reflection]]

$$
  \array{
    \mathbb{Z}_2 \times \mathbb{R}^{10-d-1,1} \times \mathbb{T}^d
    &\longrightarrow&
    \mathbb{R}^{10-d-1,1}
      \times
    \mathbb{T}^d
    \\
    (\sigma, (\vec x, \vec y))
    &\mapsto&
     (\vec x, - \vec y)
  }
  \,.
$$

This results in $O(9-d)^-$-planes with [[worldvolume]] $\mathbb{R}^{10-d-1,1}$. But since the [[orbifold]] $\mathbb{T}^d\sslash \mathbb{Z}_2$ now has $2^d$ [[singularities]] /[[fixed points]] ([this Example](Riemannian+orbifold#CoordinateReflectionOnNTorus)) there are now $2^d$ such $O(9-d)^-$-planes.

Since the number of [[D-branes]] does not change under [[T-duality]], the total O-plane charge should be the same as before

$$
  2^d \cdot q_{O(9-d)}
  \;=\;
  1 \cdot q_{O9}
  \;=\;
  -32 \cdot q_{D9}
  \;=\;
  - 2^5 \cdot q_{D9}
$$

which means that the $O(9-d)^-$-plane charge is

$$
  q_{O(9-d)^-}
  \;=\;
  - 2^{5-d} \cdot q_{D(p-d)}
$$

or equivalently

\[
  \label{OpPlaneCharge}
  q_{O p^-}
  \;=\;
  - 2^{ p - 4 } \cdot q_{D p}
\]

(e.g. [Ibáñez-Uranga 12 (5.52)](#IbanezUranga12), [Blumenhagen-Lüst-Theisen 13 (10.212)](#BlumenhagenLustTheisen13))

{#TableOfOPlaneCharges} In summary, we have the following table of O-plane charges on [[flat orbifolds]]:

| [[O-plane]] <br/> species | charge <br/> $q_{O p^-}/q_{D p}$| transverse <br/> [[n-torus|d-torus]] | [[fixed points]] <br/> $\left\vert\left( \mathbb{T}^d\right)^{\mathbb{Z}_2}\right\vert$ |
|------------|--------|-------|----| 
| $O9^-$ | $-32$ | $\mathbb{T}^0$  | $\phantom{1}1$ |
| $O8^-$ | $-16$ | $\mathbb{T}^1$  | $\phantom{1}2$ |
| $O7^-$ | $-\phantom{1}8$ | $\mathbb{T}^2$  | $\phantom{1}4$ |
| $O6^-$ | $-\phantom{1}4$ | $\mathbb{T}^3$  |  $\phantom{1}8$ | 
| $O5^-$ | $-\phantom{1}2$ | $\mathbb{T}^4$  |  $16$ | 
| $O4^-$ | $-\phantom{1}1$ | $\mathbb{T}^5$  |  $32$ |

In particular the [[O4-plane]] has negative unit charge (in [[physical unit|units]] of [[D4]]-[[D-brane charge|brane charge]] $q_{D4}$), so that the total charge of $-32$ here comes entirely from the [[number]] $32 = 2^5$ of [[fixed points]] of the $\mathbb{Z}_2$-[[action]] on $\mathbb{T}^5$.

O-plane charges of different dimension may be present

\begin{center}
<img src="https://ncatlab.org/nlab/files/O8IntersectingO4.jpg" width="600"/>
\end{center}


>  graphics grabbed from [Johnson 97](#Johnson97)


#### In the presence of discrete torsion
{#WithDiscreteTorsion} 

In the presence of [[discrete torsion]] in the [[B-field]] and/or the [[RR-fields]], this charge structure of orientifold planes on [[flat orbifolds]] gets further modified ([Hanany-Kol 00, Sec. 2.1](#HananyKol00), see [Bergman-Gimon-Sugimoto 01, Sec. 1](#BergmanGimonSugimoto01)):


\begin{center}
\begin{imagefromfile}
  "file_name": "OPlaneChargeWithDiscreteTorsion.jpg",
  "width": 470
\end{imagefromfile}
\end{center}

> graphics grabbed from [Bergman-Gimon-Sugimoto 01](#BergmanGimonSugimoto01)

(In comparing this last table with the [above table](#TableOfOPlaneCharges),
notice that this shows the Op-plane charge in [[physical unit|units]] of $q_{Dq} \coloneqq 1/2$ as in (eq:DBraneChargeOnOrbifold).)

#### In differential equivariant KR-theory

A proposal for a formalization of a much more general formula for O-plane charge, regarded in [[differential K-theory|differential]] [[equivariant K-theory|equivariant]] [[KR-theory]] is briefly in [Distler-Freed-Moore 09, p. 6](#DistlerFreedMoore09).



### Duality with M-Theory
 {#DualityWithMTheory}

The possible O-planes in [[M-theory]] are $MO1$ ($\leftrightarrow$[[M-wave]]), [[MO5]] ($\leftrightarrow$[[M5-brane]]) and [[MO9]] ([Hanany-Kol 00 around (3.2)](#HananyKol00), [HSS 18, Prop. 4.7](#HSS18)).

Under the [[duality between M-theory and type IIA string theory]] the O8-plane is identified with the [[MO9]] of [[Horava-Witten theory]]:

\begin{center}
<img src="https://ncatlab.org/nlab/files/O8DualToM9.jpg" width="600"/>
\end{center}

> graphics grabbed from [GKSTY 02, section 3](#GKSTY02)

while the [[O4-plane]] is [[duality between M-theory and type IIA string theory|dual]] to the [[MO5]] ([Hori 98](#Hori98), [Gimon 98, Sec. III](#Gimon98), [AKY 98, Sec. II B](#AKY98), [Hanany-Kol 00, 3.1.1](#HananyKol00)) 

\begin{center}
<img src="https://ncatlab.org/nlab/files/O4PlanesFromMO5.jpg" width="500"/>
\end{center}

> graphics grabbed from [Gimon 98](#Gimon98)


and the $O0$ to the MO1 ([Hanany-Kol 00 3.3](#HananyKol00))
 
### Fractional branes at O-planes


By the discussion at _[D-branes ending on NS5 branes](NS5-brane#D6BranesEndingOnNS5Branes)__, a [[black brane|black]] [[D6-brane]] may end on a [[black brane|black]] [[NS5-brane]], and in fact a priori each [[black brane|brane]] [[NS5-brane]] has to be the junction of two [[black brane|black]] [[D6-branes]]. 

<img src="https://ncatlab.org/nlab/files/HalfNS5.jpg" width="650"/>

> from [GKSTY 02](#GKSTY02)

If in addition the [[black brane|black]] [[NS5-brane]] sits at an [[O8-plane]], hence at the [[orientifold]] [[fixed point]]-locus, then in the ordinary $\mathbb{Z}/2$-[[quotient]] it appears as a "[[half-brane]]" with only one copy of [[D6-branes]] ending on it:


<img src="https://ncatlab.org/nlab/files/HalfNS5II.jpg" width="400"/>

> from [GKSTY 02](#GKSTY02)

(In [Hanany-Zaffaroni 99](#HananyZaffaroni99) this is interpreted in terms of the [['t Hooft-Polyakov monopole]].)

{#LiftToMTheortyOfNS5Halfbrane} The lift to [[M-theory]] of this situation is an [[M5-brane]] intersecting an [[M9-brane]]:

<img src="https://ncatlab.org/nlab/files/M9KK6Intersection.jpg" width="650"/>

> from [GKSTY 02](#GKSTY02)

Alternatively the [[O8-plane]] may intersect the [[black brane|black]] [[D6-branes]] away from the [[black brane|black]] [[NS5-brane]]:

<img src="https://ncatlab.org/nlab/files/D6D8Intersection.jpg" width="650"/>

> from [HKLY 15](#HKLY15)

In general, some of the NS5 sit away from the [[O8-plane]], while some sit on top of it:


<img src="https://ncatlab.org/nlab/files/NS5D6O8.jpg" width="500"/>

> from [Hanany-Zaffaroni 98](#HananyZaffaroni98)


See also at _[[intersecting D-brane models]]_ the section _[Intersection of D6s with O8s](intersecting+D-brane+model#IntersectionOfD6WithO8)_.


## Related concepts

* [[D-brane]]

* [[M-theory lift of gauge enhancement on D6-branes]]

* [NS5 half-branes](NS5-brane#NSHalfBranes)


## References

### General

The term "orientifold" originates around 

* {#DaiLinPolchinski89} Jin Dai, R.G. Leigh, [[Joseph Polchinski]], p. 12 of _New Connections Between String Theories_, Mod.Phys.Lett. A4 (1989) 2073-2083 ([spire:25758](http://inspirehep.net/record/25758))

Other early accounts include

* {#Johnson97} [[Clifford Johnson]], _Anatomy of a Duality_, Nucl.Phys. B521 (1998) 71-116 ([arXiv:hep-th/9711082](https://arxiv.org/abs/hep-th/9711082))

* {#HananyZaffaroni98} [[Amihay Hanany]], [[Alberto Zaffaroni]], _Branes and Six Dimensional Supersymmetric Theories_, Nucl.Phys. B529 (1998) 180-206 ([arXiv:hep-th/9712145](https://arxiv.org/abs/hep-th/9712145))

* {#Witten98} [[Edward Witten]], section 5 of _D-branes and K-theory_, J. High Energy Phys., 1998(12):019, 1998 ([arXiv:hep-th/9810188](http://arxiv.org/abs/hep-th/9810188)) 

* [[Sunil Mukhi]], Nemani V. Suryanarayana, _Gravitational Couplings, Orientifolds and M-Planes_, JHEP 9909 (1999) 017 ([arXiv:hep-th/9907215](https://arxiv.org/abs/hep-th/9907215))

* Yoshifumi Hyakutake, Yosuke Imamura, [[Shigeki Sugimoto]], _Orientifold Planes, Type I Wilson Lines and Non-BPS D-branes_, JHEP 0008 (2000) 043 ([arXiv:hep-th/0007012](https://arxiv.org/abs/hep-th/0007012))

* {#BDHKMMS01} [[Jan de Boer]], [[Robbert Dijkgraaf]], [[Kentaro Hori]], [[Arjan Keurentjes]], [[John Morgan]], [[David Morrison]], [[Savdeep Sethi]], section 3 of _Triples, Fluxes, and Strings_, Adv.Theor.Math.Phys. 4 (2002) 995-1186 ([arXiv:hep-th/0103170](https://arxiv.org/abs/hep-th/0103170))

Textbook accounts:

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], section 10 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge 2012

* {#BlumenhagenLustTheisen13} [[Ralph Blumenhagen]], [[Dieter Lüst]], [[Stefan Theisen]], Section 9.4 and 10.6 of _Basic Concepts of String Theory_ Part of the series Theoretical and Mathematical Physics, Springer 2013

See also 

* Wikipedia, _[Orientifold](https://en.wikipedia.org/wiki/Orientifold)_

### With discrete torsion

O-Plane charge in the presence of [[discrete torsion]]:

* [Hanany-Kol 00](#HananyKol00)

* {#BergmanGimonSugimoto01} [[Oren Bergman]], [[Eric Gimon]], [[Shigeki Sugimoto]], _Orientifolds, RR Torsion, and K-theory_, JHEP 0105:047, 2001 ([arXiv:hep-th/0103183](https://arxiv.org/abs/hep-th/0103183))

* [[Atish Dabholkar]], [[Jaemo Park]], _Strings on Orientifolds_, Nucl. Phys. B477 (1996) 701-714 ([arXiv:hep-th/9604178](https://arxiv.org/abs/hep-th/9604178))

### In terms of KO-theory

O-Plane charge in [[differential K-theory|differential]] [[equivariant K-theory|equivariant]] [[KR-theory]]:

* {#DMR13} [[Charles Doran]], Stefan Mendez-Diez, [[Jonathan Rosenberg]], _T-duality For Orientifolds and Twisted KR-theory_ ([arXiv:1306.1779](http://arxiv.org/abs/1306.1779))


* {#DistlerFreedMoore09} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv:0906.0795](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))

* {#DistlerFreedMooreII} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Spin structures and superstrings_ ([arXiv:1007.4581](http://arxiv.org/abs/1007.4581))
 
reviewed/surveyed in

* [[Daniel Freed]], _Dirac charge quantiation, K-theory, and orientifolds_, talk at a workshop _Mathematical methods in general relativity and quantum field theories_, Paris, November 2009 ([pdf](http://www.ma.utexas.edu/users/dafr/paris_nt.pdf), [[FreedK09.pdf:file]])

* {#Moore10} [[Greg Moore]], _The RR-charge of an orientifold_, Oberwolfach talk 2010 ([pdf](https://www.physics.rutgers.edu/~gmoore/Oberwolfach_June2010_FINAL.pdf), [[MooreOrientifold2010.pdf:file]], [ppt](http://www.physics.rutgers.edu/~gmoore/AnnArbor_Feb2010_FINAL.ppt))

* {#Freed} [[Daniel Freed]], _Lectures on twisted K-theory and orientifolds_, lecures at _[K-Theory and Quantum Fields](http://www.esi.ac.at/activities/events/2012/k-theory-and-quantum-fields)_, ESI 2012 ([[FreedESI2012.pdf:file]])

Actual construction of [[twisted K-theory|twisted]] [[differential K-theory|differential]] [[KO-theory|orthogonal]] [[topological K-theory|K-theory]] and its relation to [[D-brane charge]] in [[type I string theory]] (on [[orientifolds]]):

* {#GradySati19b} [[Daniel Grady]], [[Hisham Sati]], _Twisted differential KO-theory_ ([arXiv:1905.09085](https://arxiv.org/abs/1905.09085))

### Examples / Models

The [[Witten-Sakai-Sugimoto model]] for [[QCD]] on O-planes:

* {#ImotoSakaiSugimoto09} Toshiya Imoto, [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], _$O(N)$ and $USp(N)$ QCD from String Theory_, Prog.Theor.Phys.122:1433-1453, 2010 ([arXiv:0907.2968](https://arxiv.org/abs/0907.2968))


### Lift to M-theory

Lift to [[M-theory]] ([[MO5]], [[MO9]]):

* {#Hori98} [[Kentaro Hori]], _Consistency Conditions for Fivebrane in M Theory on $\mathbb{R}^5/\mathbb{Z}_2$ Orbifold_, Nucl.Phys.B539:35-78, 1999 ([arXiv:hep-th/9805141](https://arxiv.org/abs/hep-th/9805141))

* {#Gimon98} [[Eric Gimon]], _On the M-theory Interpretation of Orientifold Planes_ ([arXiv:hep-th/9806226](https://arxiv.org/abs/hep-th/9806226), [spire:472499](http://inspirehep.net/record/472499))

* {#AKY98} Changhyun Ahn, Hoil Kim, Hyun Seok Yang, _$SO(2N)$ $(0,2)$ SCFT and M Theory on $AdS_7 \times \mathbb{R}P^4$_, Phys.Rev. D59 (1999) 106002 ([arXiv:hep-th/9808182](https://arxiv.org/abs/hep-th/9808182))

* {#GKSTY02} E. Gorbatov, V.S. Kaplunovsky, J. Sonnenschein, [[Stefan Theisen]], S. Yankielowicz, section 3 of _On Heterotic Orbifolds, M Theory and Type I' Brane Engineering_, JHEP 0205:015, 2002 ([arXiv:hep-th/0108135](https://arxiv.org/abs/hep-th/0108135))

* {#HananyKol00} [[Amihay Hanany]], [[Barak Kol]], _On Orientifolds, Discrete Torsion, Branes and M Theory_, JHEP 0006 (2000) 013 ([arXiv:hep-th/0003025](https://arxiv.org/abs/hep-th/0003025))

* {#HKLY15} Hirotaka Hayashi, Sung-Soo Kim, Kimyeong Lee, Futoshi Yagi, _6d SCFTs, 5d Dualities and Tao Web Diagrams_ ([arXiv:1509.03300](https://arxiv.org/abs/1509.03300))

* {#HSS18} [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]_ ([arXiv:1805.05987](https://arxiv.org/abs/1805.05987))

The [[brane intersection|intersection]] with [[(p,q)5-brane webs]]:

* Hirotaka Hayashi, Sung-Soo Kim, Kimyeong Lee, Masato Taki, Futoshi Yagi, _More on 5d descriptions of 6d SCFTs_, JHEP10 (2016) 126 ([arXiv:1512.08239](https://arxiv.org/abs/1512.08239))

* [[Amihay Hanany]], [[Alberto Zaffaroni]], _Issues on Orientifolds: On the brane construction of gauge theories with $SO(2n)$ global symmetry_, JHEP 9907 (1999) 009 ([arXiv:hep-th/9903242](https://arxiv.org/abs/hep-th/9903242))

* Gabi Zafrir, _Brane webs in the presence of an $O5^-$-plane and 4d class S theories of type D_, JHEP07 (2016) 035 ([arXiv:1602.00130](https://arxiv.org/abs/1602.00130))




[[!redirects orientifold planes]]

[[!redirects O-plane]]
[[!redirects O-planes]]


[[!redirects O6-plane]]
[[!redirects O6-planes]]

[[!redirects O7-plane]]
[[!redirects O7-planes]]

[[!redirects O8-plane]]
[[!redirects O8-planes]]

[[!redirects Op-plane]]
[[!redirects Op-planes]]


[[!redirects O-plane charge]]
[[!redirects O-plane charges]]



