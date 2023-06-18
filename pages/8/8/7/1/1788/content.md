

## Idea

In [[string theory]], what has come to be known as the *Hanany-Witten-effect* or *-process* or *-move* is the rough idea that 

"*Moving an [[NS5-brane]] across a [[D-brane|$D (2p+\sigma)$-brane]] creates a [[D-brane|$D (2p-2 + \sigma)$-brane]] [[intersecting branes|stretching between]] the two*".

(Here $\sigma = 0$ in [[type IIA string theory]] and $\sigma=1$ in [[type IIB string theory]].)

Something like this was informally argued in [Hanany & Witten (1997)](#HanayWitten97). Later authors have
tried offer illustration of what is meant to be happening here, as follows:


[Marolf (2001)](#Marolf01):

<center>
<img src="/nlab/files/Marolf-HananyWittenEffect.jpg" width="440"></img>
</center>

[Eto et al (2005)](#EtoEtAl05):

<center>
<img src="/nlab/files/EtoEtAl-HananyWittenEffect.jpg" width="720"></img>
</center>

[Pelc (2008)](#Pelc08):

<center>
<img src="/nlab/files/Pelc-HananyWittenEffect.jpg" width="480"></img>
</center>

[Marolf (2001)](#Marolf01) suggested that the Hanany-Witten effect may be understood entirely as a consequence of the famous ([[pregeometric RR-field|pregeometric]]) [[Bianchi identity]] for the [[RR-field]]-[[fluxes]] $F_{8-2p-\sigma}$ sourced by the [[D-branes]], which is twisted by the [[B-field]]-[[flux]] $H_3$ sourced by [[NS5-branes]]:

\[
  \label{GeneralBianchiIdentity}
  \mathrm{d}
  F_{8-2p-\sigma}
  \;=\;
  H_3 \wedge F_{8-(2p+2)-\sigma}
\]

and offered an argument in prose &lbrack;[Marolf (2001) pp. 3](#Marolf01)&rbrack;. 

[Below](#D6StretchingBetweenNS5AndD8) we spell out this approach in more detail for the case $p = 6$, which is particularly clear-cut. It may be illustrated, fairly accurately, as follows:

\linebreak

\linebreak


\[
  \label{IllustrationFluxDensitityofD6OnD8}
\]
<center>
<div style="margin:-60px 10px 10px 0;">
<img src="/nlab/files/FluxesOfD6BetweenNS5AndD8-230618.jpg" width="650"></img>
</div>
</center>



## Examples

### D6 stretching between NS5 and D8
 {#D6StretchingBetweenNS5AndD8}

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


## References

* {#HanayWitten97} [[Amihay Hanany]], [[Edward Witten]], *Type IIB Superstrings, BPS Monopoles, And Three-Dimensional Gauge Dynamics*, Nucl. Phys.B **492** (1997) 152-190 &lbrack;[arXiv:hep-th/9611230](https://arxiv.org/abs/hep-th/9611230), <a href="https://doi.org/10.1016/S0550-3213(97)80030-2">doi:10.1016/S0550-3213(97)80030-2</a>&rbrack;


* {#KubotaZhou00} Takahiro Kubota, Jian-Ge Zhou, *RR charges of D2-branes in group manifold and Hanany-Witten effect*, JHEP 0012 (2000) 030 &lbrack;[arXiv:hep-th/0010170](https://arxiv.org/abs/hep-th/0010170), [doi:10.1088/1126-6708/2000/12/030](https://doi.org/10.1088/1126-6708/2000/12/030)&rbrack;


* {#Marolf01} [[Donald Marolf]], §2 of: *T-duality and the case of the disappearing brane*, JHEP 0106:036 (2001) &lbrack;[arXiv:hep-th/0103098](https://arxiv.org/abs/hep-th/0103098), [doi:10.1088/1126-6708/2001/06/036](https://doi.org/10.1088/1126-6708/2001/06/036)&rbrack;

* {#EtoEtAl05} Minoru Eto, Youichi Isozumi, Muneto Nitta, Keisuke Ohashi, Kazutoshi Ohta, Norisuke Sakai, *D-brane Construction for Non-Abelian Walls*, Phys.Rev. D **71** (2005) 125006 &lbrack;[arXiv:hep-th/0412024](https://arxiv.org/abs/hep-th/0412024), [doi:10.1103/PhysRevD.71.125006](https://doi.org/10.1103/PhysRevD.71.125006)&rbrack;

* {#Pelc08} [[Oskar Pelc]], , *On the Quantization Constraints for a D3 Brane in the Geometry of NS5 Branes*,  	JHEP 0008 (2000) 030 &lbrack;[arXiv:hep-th/0007100](https://arxiv.org/abs/hep-th/0007100), [doi:10.1088/1126-6708/2000/08/030](https://doi.org/10.1088/1126-6708/2000/08/030)&rbrack;



