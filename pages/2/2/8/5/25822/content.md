
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

In [[string theory]], what has come to be known as the *Hanany-Witten-effect* (or *-process*, *-tansition*, or *-move*) is an expected phenomenon exhibited by branes in [[type II string theory]] which is roughly described as follows:

"*Moving an [[NS5-brane]] across a [[D-brane|$D (2p+\sigma)$-brane]] creates a [[D-brane|$D (2p-2 + \sigma)$-brane]] [[intersecting branes|stretching between]] the two*".

> (Here $\sigma = 0$ in [[type IIA string theory]] and $\sigma=1$ in [[type IIB string theory]].)

Something like this was informally argued in [Hanany & Witten (1997)](#HananyWitten97). Later authors have
tried to offer explanation and illustration of what is meant to be happening here, as follows:


[Nakatsu et al (1998)](#NakatsuEtAl98):

<center>
<div style="margin:-40px 10px 10px 0;">
<img src="/nlab/files/NakatsuEtAl-HananyWittenEffect.jpg" width="680"></img>
</div>
</center>


[Marolf (2001)](#Marolf01):

<center>
<div style="margin:-40px 10px 10px 0;">
<img src="/nlab/files/Marolf-HananyWittenEffect.jpg" width="440"></img>
</div>
</center>

[Eto et al (2005)](#EtoEtAl05):

<center>
<div style="margin:-40px 10px 10px 0;">
<img src="/nlab/files/EtoEtAl-HananyWittenEffect.jpg" width="720"></img>
</div>
</center>

[Pelc (2008)](#Pelc08):

<center>
<div style="margin:-40px 10px 10px 0;">
<img src="/nlab/files/Pelc-HananyWittenEffect.jpg" width="480"></img>
</div>
</center>

[Gang et al (2011)](#GangEtAl11):

<center>
<div style="margin:-40px 10px 10px 0;">
<img src="/nlab/files/GangEtAl-HananyWittenEffect.jpg" width="600"></img>
</div>
</center>



\linebreak

[Marolf (2001)](#Marolf01) suggested that the Hanany-Witten effect may be understood entirely as a consequence of the famous ([[pregeometric RR-field|pregeometric]]) [[Bianchi identity]] for the [[RR-field]]-[[fluxes]] $F_{8-2p-\sigma}$ sourced by the [[D-branes]], which is [[twisted de Rham cohomology|twisted]] by the [[B-field]]-[[flux]] $H_3$ sourced by [[NS5-branes]]:

\[
  \label{GeneralBianchiIdentity}
  \mathrm{d}
  F_{8-2p-\sigma}
  \;=\;
  H_3 \wedge F_{8-(2p+2)-\sigma}
\]

and offered an argument in prose &lbrack;[Marolf (2001) pp. 3](#Marolf01)&rbrack;. 

[Below](#Examples) we spell out this approach in more detail.



## Examples
 {#Examples}

### D6 stretching between D8 and NS5
 {#D6StretchingBetweenNS5AndD8}

(cf. *[[D6-D8 brane bound state]]* and [Bergshoeff, Lozano & Ortin (1998)](#BergshoeffLozanoOrtin98))

We explain the "Hanany-Witten effect" in detail for the case of "flat" [[NS5-brane|NS5]]--[[D6-brane|D6]]--[[D8-brane|D8]]-configurations, as a consequence of the [[pregeometric RR-field|pregeometric]] [[Bianchi identities]] (eq:GeneralBianchiIdentity) satisfied by the [[flux densities]] sourced by these branes.

In this case  we are dealing with

* [[Minkowski spacetimes]]$\;$ $\mathbb{R}^{1,p}$ which we may identify with their canonical [[coordinate charts]] $(x^0, \vec x) \,\coloneqq\, (x^0, x^1, \cdots, x^p)$.

* A closed [[differential 3-form]] 

  $$
    H_3 
      \,\coloneqq\,
    k vol_{S^3}
    \,\in\,
    \Omega^3_{dR}\big(
      S^3
    \big)_{cl}
    \xrightarrow{(pr_{S^3})^\ast}
    \Omega^3_{dR}
    \big(
      \mathbb{R}^{1,5}
      \times
      \mathbb{R}_{+}
      \times
      S^3
    \big)_{cl}
    \,\simeq\,
    \Omega^3_{dR}
    \big(
      \mathbb{R}^{1,9}
      \setminus
      \mathbb{R}^{1,5}
    \big)_{cl}
  $$

  being the [[B-field]] [[flux density]] sourced by an [[NS5-brane]] with worldvolume 

  $$
    \mathbb{R}^{5,1} 
      \xhookrightarrow{
        \vec x \,\mapsto\, (\vec x, \vec 0)
      }
    \mathbb{R}^{9,1}
    \,.
  $$

* A closed [[differential 0-form]]  (the "[[massive type IIA supergravity|Romans mass]]")

  $$
    F_0
      \,\in\,
    \Omega^0_{dR}
    \Big(
      \mathbb{R}^{9,1}
      \setminus
      \mathbb{R}^{8,1}
    \Big)
  $$

  being the [[RR-field]] [[flux density]] sourced by a [[D8-brane]] whose worldvolume 

  $$
    \mathbb{R}^{1,8} 
      \overset{
       \vec x \,\mapsto\, (\vec x, d)
      }{
        \hookrightarrow 
      }
    \mathbb{R}^{1,9}
  $$

  we take to be located at $x^9=d$ for some $d \in \mathbb{R}_+$.


* A [[differential 2-form]] 

  $$
    F_2
      \,\in\,
    \Omega^3_{dR}
    \Big(
      \mathbb{R}^{9,1}
      \setminus
      \big(
        \mathbb{R}^{5,1}
        \cup
        \mathbb{R}^{6,1}
      \big)
    \Big)
  $$

  being the [[RR-field]] [[flux density]] sourced by a [[D6-brane]] with *potential worldvolume* ("potential" because the D6 may have $\sim$ vanishing charge carried by parts of its worldvolume, hence may "disappear" from its would-be worldvolume locus in parts, as we will see): 

  \[
    \label{D6BraneWorldvolume}
    \mathbb{R}^{6,1} 
      \xhookrightarrow{
        (x^0, \vec x)
        \,\mapsto\,
        \big(x^0, \vec 0, \vec x\big)
      }
    \mathbb{R}^{9,1}
  \] 

  transverse to that of both the NS5-brane and the D8-brane and satisying the equation 

  \[
    \label{BianchiIdentityForD6BraneFlux}
    \mathrm{d}
    F_{2}
    \;=\;
    H_3 \wedge F_{0}
    \;\;\;\;\;
    \in
    \;
    \Omega^3_{dR}
    \Big(
      \mathbb{R}^{9,1}
      \setminus
      \big(
        \mathbb{R}^{5,1}
        \cup
        \mathbb{R}^{8,1}
        \cup
        \mathbb{R}^{6,1}
      \big)
    \Big)
    \,,
  \]

  where now $H_3$ and $F_0$ are understood of the [[pullback of differential forms|pullback]] (restriction) of the above [[differential forms]] of these names to the [[complement]] of the [[D6-brane]] [[worldvolume]] (eq:D6BraneWorldvolume).

  Notice that even if/though the original forms $H_3$ is *not [[exact differential form|exact]]*, after this pullback/restriction to this it does become exact, so that the equation (eq:BianchiIdentityForD6BraneFlux) is meaningful.

In order to model the Hanany-Witten effect proper as considered by previous authors, we declare the following boundary conditions:

* The [[massive type IIA supergravity|Romans vacuum]] is to the "right" of the [[D8-brane]]

  \[
    \label{RomansVacuum}
    x^9 \gt d 
    \;\;\;\;\;\;\;
    \Rightarrow
    \;\;\;\;\;\;\;
    F_0(x^9) = 0
    \,.
  \]

  Notice that the [[Bianchi identity]] for $F_0$ is $\mathrm{d} F_0 = 0$, which means that it is a [[locally constant function]] whose jump across the [[D8-brane]] worldvolume measures the charge/number $N$ of these D8-branes (cf. eg. [Fazzi (2017) p. 40](NS5-brane#Fazzi17)). Hence

  \[
    \label{RomansVacuum}
    x^9 \lt d 
    \;\;\;\;\;\;\;
    \Rightarrow
    \;\;\;\;\;\;\;
    F_0(x^9) = N
    \,.
  \]
  
  
* There is no D6-brane to the far "left" of the NS5/D8, 

  \[
    \label{ND6BesidesThoseCreated}
    \underset{\underset{x^9 \to -\infty}{\longrightarrow}}{\lim}
    F_2(x^9)
    \;\;
    =
    \;\;
    0
    \,,
  \]

  which just means to disregard D6-brane whose presence is not due to the Hanany-Witten effect.

With these boundary conditions set, the differential equation (eq:BianchiIdentityForD6BraneFlux) may be solved for $F_2$, and hence for the density of D6-brane charge/number which is "created" by the Hanany-Witten effect: At given $x^9$ the number/charge of D6-branes seen is the integral of $F^2$ around the 2-sphere in 

$$
  \mathbb{R}^{9,1}
  \setminus
  \mathbb{R}^{6,1}
  \;\simeq\;
  \mathbb{R}^{6,1} 
    \times
  \mathbb{R}_+
    \times 
  S^2 
$$

over $(\vec 0, x^9) \,\in\, \mathbb{R}^{6,1}$.  Now there are two cases:

\linebreak

\linebreak

\linebreak

\linebreak

\linebreak


\[
  \label{IllustrationFluxDensitityofD6OnD8}
\]
<center>
<div style="margin:-200px 10px 10px 0;">
<img src="/nlab/files/FluxesOfD6BetweenNS5AndD8-230618b.jpg" width="650"></img>
</div>
</center>



1. **$d \lt 0$ -- indicated in the top part of figure (eq:IllustrationFluxDensitityofD6OnD8)**

   In this case the NS5-brane is to the "right" of the D8-brane and hence in the Romans vacuum where $F_0 = 0$. Here the differential equation (eq:BianchiIdentityForD6BraneFlux) becomes

   $$
     \begin{array}{c}
      \mathrm{d} F_2 &=& F_0 \wedge H_3
      \\
      &=& 0
     \end{array}
   $$

   This means that $F_2$ does not change in the Romans vacuum, and hence if it vanishes to the left, as the boundary condition assumes, then it vanishes throughout.

   Since the integral of $F_2$ counts the number/charge of D6-brane, the conclsusion is that *no D6-branes are created* in this situation.

1. **$d \gt 0$ -- indicated in the bottom part of figure (eq:IllustrationFluxDensitityofD6OnD8)**

   In this case the NS5-brane is to the "left" of the D8-brane and hence in the region where $F_0 = N$ equals the number of D8-branes. Here the differential equation (eq:BianchiIdentityForD6BraneFlux) becomes

   $$
     \begin{array}{c}
      \mathrm{d} F_2 &=& F_0 \wedge H_3
      \\
      &=& N \, H_3
     \end{array}
   $$

   This means now that as approach the NS5/D8-branes from the "left", $F_2$ is continuously increasing by a rate measured by the density $H_3$ of NS5-brane flux. While this is everywhere non-vanishing, it is concentrated around the NS5-brane worldvolume locus (falling off by a power law from there). Therefore once we have "crossed the NS5-brane" and thus picked up most of its flux, $\int_{S^2} F_2$ will have increased from its asympotically vanishing value to $N \int_{S^2} \int_{-\infty}^d H_3 \,\sim\, N \int_{S^3} H_3 \,\sim\, N k$, the product of the number of NS5-branes and D8-branes. This is hence the number of D6-branes "created" by the Hanany-Witten effect.


### D3 stretching between D5 and NS5
 {#D2StretchingBetweenNS5AndD5}

(cf. *[[D3-D5 brane bound state]]*)

We discuss the "creation" of [[D3-brane]] [[flux]] "in between" a [[background field|background]] of [[D5-brane]]- and [[NS5-brane]] flux as seen from (just) the [[pregeometric RR-field|pregeometric flux]]-equations.

If we assume that there are no [[D7-branes]] present in that the [[RR-field]] [[flux density]] which they source vanishes, $F_1 = 0$, then the [[Bianchi identity]] for the [[D5-brane]]-flux is just

$$
  \begin{array}{rcl}
  \mathrm{d} \, F_3
  &=&
  H_3 \wedge F_1
  \\
  &=& 0
  \end{array}
$$

just as for the [[B-field]] [[flux density]]

$$
  \mathrm{d}\, H_3 \;=\; 0
  \,.
$$

Hence assume that there is a pair of flat parallel [[D5-branes]] and [[NS5-branes]] at a [[positive number|positive]] distance $2 d \in \mathbb{R}_+$ from each other 

$$
  \array{
    \mathbb{R}^{5,1}_{NS5}
    &\xhookrightarrow{\phantom{--}}&
    \mathbb{R}^{10,1}
    \\
    (t,\vec x) &\mapsto& (t,\vec x, -d , \vec 0)
  }
  \;\;\;\;\;\;\;\;\;\;\;
  \;\;\;\;\;\;\;\;\;\;\;
  \;\;\;\;\;\;\;\;\;\;\;
  \array{
    \mathbb{R}^{5,1}_{D5}
    &\xhookrightarrow{\phantom{--}}&
    \mathbb{R}^{10,1}
    \\
    (t,\vec x) &\mapsto& (t,\vec x, +d , \vec 0)
  }
$$

in that the respective [[flux densities]] are 
$$
  H_3 
    \;\coloneqq\;
  vol_{S^3}
  \;\in\;
  \Omega^3_{dR}(S^3)
  \xrightarrow{ pr_{S^3}^\ast }
  \Omega^3_{dR}\big(
    \mathbb{R}^{5,1}_{NS5}
    \times 
    \mathbb{R}_+
    \times
    S^3
  \big)
  \;\simeq\;
  \Omega^3_{dR}\big(
    \mathbb{R}^{9,1}
    \setminus
    \mathbb{R}^{5,1}_{D5}
  \big)
$$

and

$$
  F_3 
    \;\coloneqq\;
  vol_{S^3}
  \;\in\;
  \Omega^3_{dR}(S^3)
  \xrightarrow{ pr_{S^3}^\ast }
  \Omega^3_{dR}\big(
    \mathbb{R}^{5,1}_{D5}
    \times 
    \mathbb{R}_+
    \times
    S^3
  \big)
  \;\simeq\;
  \Omega^3_{dR}\big(
    \mathbb{R}^{9,1}
    \setminus
    \mathbb{R}^{5,1}_{D5}
  \big)
$$

In the following we regard both of these as further [[pullback of differential forms|pulled back]]/restricted to the joint [[complement]] $\mathbb{R}^{9,1} \setminus \big( \mathbb{R}^{5,1}_{NS5} \cup \mathbb{R}^{5,1}_{D5} \cup \mathbb{R}^{3,1}_{D3}\big)$.
Notice that as such they differ, one being the translate of the other by $2d$ along one of the axes.

Now the [[Bianchi identity]] for the [[RR-field]] [[flux density]] $F_5$ sourced by any [[D3-branes]] is

\[
  \label{BianchiIdentityForD3InBetweenNS5AndD5}
  \mathrm{d} \, F_{5}
  \;=\;
  H_3 \wedge F_3
  \,,
\]

Imposing the [[boundary condition]] that $F_5$ [[vanishing at infinity|vanishes at infinity]],  the differential equation will imply the presence of non-vanishing $F_5$-flux and hence of $D3$-branes "in between" the D5/NS5 iff the [[wedge product]] $H_3 \wedge F_3$ has the form of a "multipole" roughly supported in between these branes.

The following graphics, which shows a 2-dimensional shadow of the situation, qualitatively indicates that and why this is the case: 

<center>
<div style="margin:-40px 10px 10px 0;">
<img src="/nlab/files/FivebraneDipole-230620b.jpg" width="580"></img>
</div>
</center>




Here 

* the strength of the circular lines indicates the [[absolute value]] of the [[flux densities]] $H_3$, $F_3$ (vanishing at infinity and spiked at the locus of the sourcing 5-brane), 

* the little arrows indicate the [[orientation of a vector|orientation]] of the two flux densities, projected to the plane that is being shown

* the little parallelograms indicate the [[orientation]] of the [[wedge product]] $H_3 \wedge F_3$ in the projection to the plane being shown.

(Hence what the graphics is really showing, approximately, is the wedge product of a pair of translates of $dvol_{S^1}$ pulled back to around either puncture of the 2-punctured plane.)

The point is to observe that --- besides the abolute value of the wedge product $F_3 \wedge H_3$ evidently being concentrated near the branes, hence particularly between them when they are close --- the sign of the orientation of the wedge product changes as the transverse coordinate passes through the axis between the branes.

Hence as we solve the differential equation $\mathrm{d} F_5 \,=\, H_3 \wedge F_3$ incrementally by running, say, from the top to the bottom in the above graphics, we see that the absolute value of $F_5$ --- indicated in $\color{red}\text{red shading}$ above ---  fist incrementally picks up positive contributions as we approach the area between the branes, and then dimishies again as we leave that area. In total, the absolute value of the solution $F_5$ will be supported roughly in between the two 5-branes. 

Since $F_5$ is the flux sourced by [[D3-branes]], this means that D3-branes are seen to be "created" in between the 5-branes.

However, from this analysis of the fluxes alone, it does not follow that the D3-branes would disappear as the NS5- and D5-brane "swap positions", as Hanany-Witten would suggest. In fact there is no intrinsic such directedness in the problem in the first place with respect to which one could even speak about the branes "swapping positions".

Hence to see the full Hanany-Witten effect in this case, if it exists, one may have to look beyond the bare fluxes and include also the field of gravity. A suggestion for how this might work is given, for the analogous situation of [[M2-M5 brane bound state|M2-M5 brane]] [[brane intersection|intersections]], in [Hosomichi (2000), §5](#Hosomichi00).


\linebreak  



## Related concepts

[[!include brane bound states -- table]]




## References

The original article:

* {#HananyWitten97} [[Amihay Hanany]], [[Edward Witten]], *Type IIB Superstrings, BPS Monopoles, And Three-Dimensional Gauge Dynamics*, Nucl. Phys.B **492** (1997) 152-190 &lbrack;[arXiv:hep-th/9611230](https://arxiv.org/abs/hep-th/9611230), <a href="https://doi.org/10.1016/S0550-3213(97)80030-2">doi:10.1016/S0550-3213(97)80030-2</a>&rbrack;

Further discussion:

* {#NakatsuEtAl98} Toshio Nakatsu, Kazutoshi Ohta, Takashi Yokono, Yuhsuke Yoshida, *A Proof of Brane Creation via M theory*,  	Mod. Phys. Lett. A **13** (1998) 293-302 &lbrack;[arXiv:hep-th/9711117](https://arxiv.org/abs/hep-th/9711117), [doi:10.1142/S0217732398000358](https://doi.org/10.1142/S0217732398000358)&rbrack;


* {#KubotaZhou00} Takahiro Kubota, Jian-Ge Zhou, *RR charges of D2-branes in group manifold and Hanany-Witten effect*, JHEP 0012 (2000) 030 &lbrack;[arXiv:hep-th/0010170](https://arxiv.org/abs/hep-th/0010170), [doi:10.1088/1126-6708/2000/12/030](https://doi.org/10.1088/1126-6708/2000/12/030)&rbrack;


* {#Marolf01} [[Donald Marolf]], §2 of: *T-duality and the case of the disappearing brane*, JHEP 0106:036 (2001) &lbrack;[arXiv:hep-th/0103098](https://arxiv.org/abs/hep-th/0103098), [doi:10.1088/1126-6708/2001/06/036](https://doi.org/10.1088/1126-6708/2001/06/036)&rbrack;

* {#EtoEtAl05} Minoru Eto, Youichi Isozumi, Muneto Nitta, Keisuke Ohashi, Kazutoshi Ohta, Norisuke Sakai, §3.3 in: *D-brane Construction for Non-Abelian Walls*, Phys.Rev. D **71** (2005) 125006 &lbrack;[arXiv:hep-th/0412024](https://arxiv.org/abs/hep-th/0412024), [doi:10.1103/PhysRevD.71.125006](https://doi.org/10.1103/PhysRevD.71.125006)&rbrack;

* {#Pelc08} [[Oskar Pelc]], , *On the Quantization Constraints for a D3 Brane in the Geometry of NS5 Branes*,  	JHEP 0008 (2000) 030 &lbrack;[arXiv:hep-th/0007100](https://arxiv.org/abs/hep-th/0007100), [doi:10.1088/1126-6708/2000/08/030](https://doi.org/10.1088/1126-6708/2000/08/030)&rbrack;

* {#GangEtAl11} Dongmin Gang, Eunkyung Koh, Kimyeong Lee, Jaemo Park, *ABCD of 3d $\mathcal{N}=8$ and 4 Superconformal Field Theories* &lbrack;[arXiv:1108.3647](https://arxiv.org/abs/1108.3647)&rbrack;

See also:

* Wikipedia, *[Hanany-Witten transition](https://en.wikipedia.org/wiki/Hanany%E2%80%93Witten_transition)*

The case of [[D6-D8 brane bound states]]:

* {#HananyZaffaroni98} [[Amihay Hanany]], [[Alberto Zaffaroni]], §2.4 in: *Chiral Symmetry from Type IIA Branes*, Nucl. Phys. B **509** (1998) 145-168 &lbrack;[arXiv:hep-th/9706047](https://arxiv.org/abs/hep-th/9706047), <a href="https://doi.org/10.1016/S0550-3213(97)00595-6">doi:10.1016/S0550-3213(97)00595-6</a>&rbrack;

* {#BergshoeffLozanoOrtin98} [[Eric Bergshoeff]], [[Yolanda Lozano]], [[Tomas Ortin]], p. 60 of: *Massive Branes*, Nucl. Phys. B **518** (1998) 363-423 &lbrack;[arXiv:hep-th/9712115](https://arxiv.org/abs/hep-th/9712115), <a href="https://doi.org/10.1016/S0550-3213(98)00045-5">doi:10.1016/S0550-3213(98)00045-5</a>&rbrack;

Discussion for [[M2-M5 brane bound state|M2-M5 brane]] [[brane intersection|intersections]]:

* {#Hosomichi00} [[Kazuo Hosomichi]], *On Branes Ending on Branes in Supergravity*, JHEP 0006 (2000) 004 &lbrack;[arXiv:hep-th/0002069](https://arxiv.org/abs/hep-th/0002069), [doi:10.1088/1126-6708/2000/06/004](https://doi.org/10.1088/1126-6708/2000/06/004)&rbrack;


[[!redirects Hanany-Witten effects]]

[[!redirects Hanany-Witten process]]
[[!redirects Hanany-Witten processes]]

[[!redirects Hanany-Witten move]]
[[!redirects Hanany-Witten moves]]

[[!redirects Hanany-Witten transition]]
[[!redirects Hanany-Witten transitions]]


