
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[spacetime]] geometry of a [[black hole]] or [[black brane]] close to the [[horizon]] is called its _near-horizon geometry_. Accordingly, the geometry far from the horizon might be called its _far-horizon geometry_. One commonly says that the black hole/brane solution _interpolates_ between its near and far horizon geometry.

## Properties

In the following "small" and "large" [[radius]] is in [[units]] of [[Planck length]] $\ell_P$ times a root of the integer charge ("number" $N$) of the branes, i.e. being "near" to the horizon means that 

$$ 
  r/\ell_P N^{1/k} \ll 1 
$$

while "far" from the horizon means that 

$$ 
  r/\ell_P N^{1/k} \gg 1 
$$

(e.g. [AFFHS 98, (2), (7) and below (11)](#AFFHS98)).

This means that the near/far horizon limit may also be thought of as corresponding to large/small $N$, respectively.

Since the [[Planck length]] "is tiny" and due to the higher roots of $N$ appearing here, this means that $N$ must be "huge" for the near horizon limit to be visible at macroscopic scale, while, conversely, any "moderate" value of $N$ means implies that every macroscopic radius is "far" from the horizon. 



### Near-horizon geometry
 {#NearHorizonGeometry}

For [[black brane|black]] [[M-branes]] ([[black branes]] in [[11-dimensional supergravity]]) of [[dimension]] $p+1$ that preserve some [[supersymmetry]], the near horizon geometry is always a [[Cartesian product]] of an [[anti-de Sitter spacetime]] $AdS_{p+2}$ with a [[compact topological space|compact]] [[Einstein manifold]] $X_{11-(p+2)}$; 

$$
  Ads_{p+2} \times X_{d-(p+2)}
  \,;
$$

while for [[black brane|black]] [[D-branes]] and [[NS5-branes]] in [[type II supergravity]] the near horizon geometry is [[conformal transformation|conformal]] to a geometry of this form $AdS_{p+2} \times X_{d-(p+2)}$ (see [AFFHS 98, section 2](#AFFHS98)).

### Far-horizon geometry
 {#FarHorizonGeometry}

In contrast, the "far-horizon geometry" of all those [[black branes]] whose near horizon geometry is $AdS_{p+2} \times X_{d-(p+2)}$ (i.e. actual [[anti-de Sitter spacetime]] without conformal factor) is of the form 

$$
  \mathbb{R}^{p,1} \times C\left(X_{d-(p+2)}\right)
  \,,
$$

where $\mathbb{R}^{p,1}$ is [[Minkowski spacetime]] (the brane [[worldvolume]]) and $C(X_{d-(p+2)})$ is the [[metric cone]] over $X_{d-(p+2)}$, hence an [[orbifold]] (see [AFFHS 98, section 3](#AFFHS98)). Since this "far-horizon limit" is still a solution to the [[supergravity]] [[equations of motion]] away from the tip of the cone, it may in itself be regarded as a "[[cone brane]]"-solution (see [AFFHS 98, section 3.1](#AFFHS98)).

If $X_{d-(p+2)}$ is a smooth [[quotient space]] by the [[action]] of a [[finite subgroup of SU(2)]], then the corresponding [[cone brane]] is a brane "at an [[ADE-singularity]]".


Examples and applications of such cone branes, in the context of [[M-theory on G2-manifolds]], are discussed in [Atiyah-Witten 01](#AtiyahWitten01).

## Examples
 {#Examples}

The near/far horizon limits of the [[black brane|black]] [[M-branes]]:

* _[The black M2-brane](#BlackM2)_

* _[The black M5-brane](#BlackM5Brane)_

* _[The MK6-brane](#MK6Brane)_

### The black M2-brane
 {#BlackM2}

The [[black brane|black]] [[M2-brane]] is given by the [[Riemannian metric]]

\[
  \label{BlackM2BraneMetric}
  g_{M2} \;\coloneqq\;
  H^{- 2/3} g_{(\mathbb{R}^{2,1})}
  +
  H^{1/3} g_{C(X_7)}
\]

and the [[C-field]] [[field strength|strength]]

$$
  F_{M2} \;\coloneqq\; dvol_{\mathbb{R}^{2,1}} \wedge d H^{-1}
$$

where $C(X_7)$ denotes the [[metric cone]] on a [[closed manifold|closed]] 7-[[dimension|dimensional]] [[Einstein manifold]] $X_7$ for [[cosmological constant]] $\Lambda = 5$, whence 

$$
  g_{C(X)}
  \;\coloneqq\;
  (d r)^2 + r^2 g_{X_7}
  \,,
$$

and

$$
  H \;\coloneqq\; 1 + \frac{\ell_{th}^6}{r^6}
  \:,
  \phantom{AAA}
  \ell_{th} \;\coloneqq\; 2^{5/6} \pi^{2/6} N^{1/6} \ell_P
$$

with $N$ the number of [[M2-branes]] and with $\ell_P$ the [[Planck length]] in 11 dimensions.

In the near-horizon/large $N$-limit $\ell_{th} \to \infty$ this becomes

$$
  \begin{aligned}
    g_{M2} 
    \overset{\ell_{th} \gg 1}{\longrightarrow}
    \;\;\;
    & 
    \left(
      r/\ell_{th}
    \right)^{4}
    g_{(\mathbb{R}^{2,1})}
    +
    \left( r/\ell_{th} \right)^{-2} g_{C(X_7)}
    \\
    = & 
    \left(
      r/\ell_{th}
    \right)^{4}
    g_{(\mathbb{R}^{2,1})}
    +
    \left( r/\ell_{th} \right)^{-2} (d r)^2 
    +
    \ell_{th}^{2}
    g_{X_7}
    \\
    = & 
    \underset{
      = g_{AdS}
    }{\underbrace{
    \frac{1}{z^2}
    \left(
      2^4 g_{(\mathbb{R}^{2,1})}
      +
      (d z)^2
    \right)
    }}
    +
    \ell_{th}^{2}
    g_{X_7}    
  \end{aligned}
  \,,
$$

where in the last step we set

$$
  r \;\coloneqq\; 2 \ell_{th} \frac{1}{\sqrt{z}}
$$

This reveals the first summand as being the [[metric tensor]] of [[anti-de Sitter spacetime]] of AdS radius $\ell_{th}$ in [[horospheric coordinates]], and the second summand as that of $X_{7}$ rescaled to radius $\ell_{th}$.

In contrast, in the far-horizon/small $N$-limit $\ell_{th} \to 0$ (eq:BlackM2BraneMetric) becomes

$$
  g_{M2} \;\overset{\ell_{th} \to 0}{\longrightarrow}\;
  g_{\mathbb{R}^{2,1}}
  +
  g_{C(X_7)}
$$

and 

$$
  F_{M2} \;\overset{\ell_{th} \to 0}{\longrightarrow}\; 0
$$

which is the metric on a [[Cartesian product]] of flat [[Minkowski spacetime]] [[worldvolume]] of an M2-brane with the [[metric cone]] on $X_7$.


### The black M5-brane
 {#BlackM5Brane}

The [[black brane|black]] [[M5-brane]] is given by the [[Riemannian metric]]

\[
  \label{BlackM5BraneMetric}
  g_{M5} \;\coloneqq\;
  H^{- 1/3} g_{(\mathbb{R}^{5,1})}
  +
  H^{2/3} g_{C(X_4)}
\]

and the [[C-field]] [[field strength|strength]]

$$
  F_{M2} \;\coloneqq\; \pm 3 \star_5 \wedge d H
$$

where $C(X_4)$ denotes the [[metric cone]] on a [[closed manifold|closed]] 4-[[dimension|dimensional]] [[Einstein manifold]] $X_4$ for [[cosmological constant]] $\Lambda = 3$, whence 

$$
  g_{C(X)}
  \;\coloneqq\;
  (d r)^2 + r^2 g_{X_4}
  \,,
$$

and

$$
  H \;\coloneqq\; 1 + \frac{\ell_{th}^3}{r^3}
  \:,
  \phantom{AAA}
  \ell_{th} \;\coloneqq\; \pi^{1/3} N^{1/3} \ell_P
$$

with $N$ the number of [[M5-branes]] and with $\ell_P$ the [[Planck length]] in 11 dimensions.

In the near-horizon/large $N$-limit $\ell_{th} \to \infty$ this becomes

$$
  \begin{aligned}
    g_{M5} 
    \overset{\ell_{th} \gg 1}{\longrightarrow}
    \;\;\;
    & 
    \left(
      r/\ell_{th}
    \right)^{4}
    g_{(\mathbb{R}^{2,1})}
    +
    \left( r/\ell_{th} \right)^{-2} g_{C(X_7)}
    \\
    = & 
    r/\ell_{th}
    g_{(\mathbb{R}^{2,1})}
    +
    \left( r/\ell_{th} \right)^{-2} (d r)^2 
    +
    \ell_{th}^{2}
    g_{X_7}
    \\
    = & 
    \underset{
      = g_{AdS}
    }{\underbrace{
    \frac{1}{z^2}
    \left(
      2 g_{(\mathbb{R}^{2,1})}
      +
      (d z)^2
    \right)
    }}
    +
    \ell_{th}^{2}
    g_{X_4}    
  \end{aligned}
  \,,
$$

where in the last step we set

$$
  r \;\coloneqq\; \ell_{th}\tfrac{1}{2} \frac{1}{z^2}
$$

This reveals the first summand as being the [[metric tensor]] of [[anti-de Sitter spacetime]] of AdS radius $\ell_{th}$ in [[horospheric coordinates]], and the second summand as that of $X_{4}$ rescaled to radius $\ell_{th}$.


In contrast, in the far-horizon/small $N$-limit $\ell_{th} \to 0$ (eq:BlackM5BraneMetric) becomes

$$
  g_{M5} \;\overset{\ell_{th} \to 0}{\longrightarrow}\;
  g_{\mathbb{R}^{5,1}}
  +
  g_{C(X_4)}
$$

and 

$$
  F_{M2} \;\overset{\ell_{th} \to 0}{\longrightarrow}\; 0
$$

which is the metric on a [[Cartesian product]] of flat [[Minkowski spacetime]] [[worldvolume]] of an M5-brane with the [[metric cone]] on $X_4$.

### The MK6-brane
 {#MK6Brane}

The [[metric tensor]] of $N$ coincident [[KK-monopoles]] in [[11-dimensional supergravity]] in the limit that $\ell_{th} \coloneqq N \ell_P \to 0$ is

\[
  \label{SmallNMK6}
  g_{MK6} 
    \;=\;
  g_{\mathbb{R}^{6,1}}
  +
  (d y)^2
  + 
  y^2
  \big(
    (d \theta)^2
    + 
    (\sin \theta)^2 (d \varphi)^2
    + 
    (\cos \theta)^2 (d \phi)^2
  \big)
\] 

subject to the identification

\[
  \label{OrbifoldIdentificationForKKMonopole}
  (\varphi, \phi)
  \;\sim\;
  (\varphi, \phi) + (2\pi/N ,2\pi/N)
  \,.
\]

This is equation (47) in [IMSY 98](#IMSY98), which applies subject to the condition 

$$
  U/\left(\frac{N}{g^{2/3}_{YM}}\right) 
  \;=\; 
  U/\left(\frac{N}{(2\pi)^{4/3} \ell_P}\right) 
  \;\gg\; 
  1
$$ 

from a few lines above. Inserting this condition into the definition $y^2 \coloneqq 2 N \ell^3_P U $ right above (47) shows that

$$
  \begin{aligned}
  y^2 
  & =
  2 N \ell^3_P U
  \\
  & =
  2(2\pi)^{-4/3} N^2 \ell_P^2 
  \;
  \underset{
    \gg 1
  }{
  \underbrace{
     \left(U/\left(\frac{N}{ (2 \pi)^{4/3} \ell_P}\right)\right)
  }}
  \end{aligned}
$$

hence that the distance $y$ from the locus of the MK6-brane is large in units of

$$
  \ell_{th} \;=\; \sqrt{2} (2\pi)^{-2/3} N \ell_P
  \,.
$$

The identification (eq:OrbifoldIdentificationForKKMonopole) means that this is the [[orbifold]] [[metric cone]] $\mathbb{R}^{6,1} \times \left( \mathbb{R}^4/(\mathbb{Z}_N)\right)$, hence an [[ADE classification|
A-type]] [[ADE-singularity]]. To make this more explicit, introduce the complex coordinates

$$
  v \;\coloneqq\; y \, e^{i \varphi} \sin \theta
  \;\;\;
  w \;\coloneqq\; y \, e^{i \phi} \cos \theta
$$

on $\mathbb{R}^4 \simeq \mathbb{C}^2$, in terms of which (eq:SmallNMK6) becomes

$$
  g_{MK6} 
  \;\coloneqq\;
  d v d \overline v
  + 
  d w d \overline w
$$

and which exhibit the identification (eq:OrbifoldIdentificationForKKMonopole) as indeed that of the [[ADE classification|A-type]] $\mathbb{Z}_N$-action ([Asano 00, around (18)](#Asano00)).

[[!include KK-monopole geometries -- table]]



## Related concepts

* [[piecewise flat spacetime]]

* [[anti-de Sitter spacetime]]

* [[asymptotic boundary]]

## References

### General


See also

* Wikipedia, _[Near-horizon metric](https://en.wikipedia.org/wiki/Near-horizon_metric)_

### For extremal black holes

That the near horizon geometry of the [[extremal black hole|extremal]] [[Reissner-Nordström black hole]] in $\mathcal{N}=2$ [[4d supergravity]] is $AdS_2 \times S^2$ was observed in 

* [[Gary Gibbons]], in F. del Aguila, [[J. de Azcarraga]], [[Luis Ibanez]] (eds.) _Supersymmetry, Supergravity and Related Topics_

Review: 

* Hari K. Kunduri, James Lucietti, _Classification of Near-Horizon Geometries of Extremal Black Holes_ ([web](http://relativity.livingreviews.org/Articles/lrr-2013-8/title.html))

Description of the near-horizon geometry of near-extremal black holes by [[Jackiw-Teitelboim gravity]]:

* {#NSST18} Pranjal Nayak, Ashish Shukla, Ronak M Soni, [[Sandip Trivedi]], V. Vishal, _On the Dynamics of Near-Extremal Black Holes_ ([arXiv:1802.09547](https://arxiv.org/abs/1802.09547))

* {#MTV18} Upamanyu Moitra, [[Sandip Trivedi]], V. Vishal, _Near-Extremal Near-Horizons_ ([arXiv:1808.08239](https://arxiv.org/abs/1808.08239))


### For black branes

That the near horizon geometry of [[black branes]] in [[11-dimensional supergravity]] is (conformal to) [[anti de Sitter spacetime]] times some [[compact space]] is apparently due to 

* {#GibbonsTownsend93} [[Gary Gibbons]], [[Paul Townsend]], _Vacuum interpolation in supergravity via super p-branes_, Phys. Rev. Lett. 71, (1993) 3754 ([arXiv:hep-th/9307049](https://arxiv.org/abs/hep-th/9307049))

* {#DuffGibbonsTownsend94} [[Mike Duff]], [[Gary Gibbons]], [[Paul Townsend]], _Macroscopic superstrings as interpolating solitons_, Phys. Lett. B. 332 (1994) 32 ([arXiv:hep-th/9405124](https://arxiv.org/abs/hep-th/9405124))

* {#GibbonsHorowitzTownend95} [[Gary Gibbons]], [[Gary Horowitz]], [[Paul Townsend]], _Higher-dimensional resolution of dilatonic black hole singularities_, Class. Quant. Grav. 12 (1995) 297 ([arXiv:hep-th/9410073](https://arxiv.org/abs/hep-th/9410073))

* [[Gary Gibbons]], Nucl. Phys. B207, (1982) 337;

* [[Renata Kallosh]], [[Amanda Peet]], Phys. Rev. B46, (1992) 5223;

* [[Sergio Ferrara]], [[Gary Gibbons]], [[Renata Kallosh]], Nucl. Phys. B500, (1997) 75;

* [[Ali Chamseddine]], [[Sergio Ferrara]], [[Gary Gibbons]], [[Renata Kallosh]], Phys. Rev. D55, (1997) 3647

The observation that the resulting [[isometry group]] is the bosonic body of one of the [[orthosymplectic super groups]] is due to

* P. Claus, [[Renata Kallosh]], J. Kumar, [[Paul Townsend]], [[Antoine Van Proeyen]], _Conformal Theory of M2, D3, M5 and D1+D5 Branes_, JHEP 9806 (1998) 004 ([arXiv:hep-th/9801206](https://arxiv.org/abs/hep-th/9801206))

A decent account is in 

* {#AFFHS98} [[Bobby Acharya]], [[Jose Figueroa-O'Farrill]], [[Chris Hull]], B. Spence, _Branes at conical singularities and holography_, Adv. Theor. Math. Phys.2:1249-1286, 1999 ([arXiv:hep-th/9808014](https://arxiv.org/abs/hep-th/9808014))

reviewed in

* {#FigOFar98} [[Jose Figueroa-O'Farrill]], _Near-horizon geometries of supersymmetric branes_, talk at [SUSY 98](http://inspirehep.net/record/971430/) ([arXiv:hep-th/9807149](https://arxiv.org/abs/hep-th/9807149), [talk slides](http://www.maths.ed.ac.uk/~jmf/CV/Seminars/SUSY98.pdf))

The near horizon geometry of coincident [[KK-monopoles]] in [[11-dimensional supergravity]] is discussed in 

* {#IMSY98} Nissan Itzhaki, [[Juan Maldacena]], Jacob Sonnenschein, Shimon Yankielowicz, section 9 of _Supergravity and The Large $N$ Limit of Theories With Sixteen Supercharges_, Phys. Rev. D 58, 046004 1998 ([arXiv:hep-th/9802042](https://arxiv.org/abs/hep-th/9802042))

* {#ItzhakiTseytlinYankielowicz98} Nissan Itzhaki, [[Arkady Tseytlin]], S. Yankielowicz, _Supergravity Solutions for Branes Localized Within Branes_, Phys.Lett.B432:298-304, 1998 ([arXiv:hep-th/9803103](https://arxiv.org/abs/hep-th/9803103))

* {#Hashimoto98} Akikazu Hashimoto, _Supergravity Solutions for Localized Intersections of Branes_, JHEP 9901 (1999) 018 ([arXiv:hep-th/9812159](https://arxiv.org/abs/hep-th/9812159))


* {#Asano00} Masako Asano, section 3 of _Compactification and Identification of Branes in the Kaluza-Klein monopole backgrounds_ ([arXiv:hep-th/0003241](https://arxiv.org/abs/hep-th/0003241))


Examples and applications of cone branes in the context of [[M-theory on G2-manifolds]] are discussed in

* {#AtiyahWitten01} [[Michael Atiyah]], [[Edward Witten]] _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([arXiv:hep-th/0107177](http://arxiv.org/abs/hep-th/0107177))

Conical [[D-branes]] are discussed in 

* [[Koji Hashimoto]], Shunichiro Kinoshita, Keiju Murata, _Conic D-branes_, Progress of Theoretical and Experimental Physics, Volume 2015, Issue 8,  August 2015 ([arXiv:1505.04506](https://arxiv.org/abs/1505.04506), [slides pdf](http://www2.yukawa.kyoto-u.ac.jp/~qft.web/2015/slides/kinoshita.pdf))

Near horizon geometries of [[black branes]] which [[KK-compactification|KK-compactify]] to [[black holes]]:

* [[Mirjam Cvetič]], Paulo J. Porfírio, Alejandro Satz, _Gaussian null coordinates, near-horizon geometry and conserved charges on the horizon of extremal non-dilatonic black p-branes_ ([arXiv:2003.09304](https://arxiv.org/abs/2003.09304))

Further discussion for [[M2-branes]]:

* Harvendra Singh, _M2-branes on a resolved $\mathbb{C}^4/\mathbb{Z}_4$_, 	JHEP 0809:071, 2008 ([arXiv:0807.5016](https://arxiv.org/abs/0807.5016))





[[!redirects near-horizon geometries]]

[[!redirects near horizon geometry]]
[[!redirects near horizon geometries]]

[[!redirects far-horizon geometry]]
[[!redirects far-horizon geometries]]

[[!redirects far horizon geometry]]
[[!redirects far horizon geometries]]


[[!redirects near-horizon limit]]
[[!redirects near-horizon limits]]

[[!redirects near horizon limit]]
[[!redirects near horizon limits]]


[[!redirects near-horizon metric]]
[[!redirects near-horizon metrices]]

[[!redirects far-horizon metric]]
[[!redirects far-horizon metrices]]

[[!redirects far-horizon limit]]
[[!redirects far-horizon limits]]

[[!redirects far horizon limit]]
[[!redirects far horizon limits]]


[[!redirects cone brane]]
[[!redirects cone branes]]

