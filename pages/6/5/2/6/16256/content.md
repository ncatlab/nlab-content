
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

### General

In the context of [[Kaluza-Klein theory]] where an [[electromagnetic field]] in [[Einstein-Maxwell theory]] in [[dimension]] $d$ is modeled by a configuration of pure Einstein [[gravity]] in dimension $d+1$, a _Kaluza-Klein monopole_ is a configuration of gravity in dimension $d+1$ which in dimension $d$ looks like a magnetic [[monopole]] ([Sorkin 83](#Sorkin83), [Gross-Perry 83](#GrossPerry83)).

### In supergravity

This situation is of particular interest in the reduction of [[11-dimensional supergravity]] (or [[M-theory]], where one also speaks of the [[M-brane|MK6-brane]]) where the Kaluza-Klein magnetic monopole charge is interpreted as [[D6-brane]] charge under [[duality between M-theory and type IIA string theory]].

The _Kaluza-Klein monopole_ ([Han-Koh 85](#HanKoh85)) is one type of solution of the [[equations of motion]] of [[11-dimensional supergravity]]. It is given by the [[product]] $N_4\times \mathbb{R}^{11-5,1}$ of Euclidean [[Taub-NUT spacetime]] with [[Minkowski spacetime]]. Upon [[Kaluza-Klein compactification]] this looks like a [[monopole]], whence the name. (For discussion as an [[ADE-singularity]] see [IMSY 98, section 9](#IMSY98), [Asano 00, section 3](#Asano00).)


Upon [[KK-compactification]] on a 6-dimensional [[fiber]], with the 11d KK-monopole / [[D6-brane]] completely [[wrapped brane|wrapping]] the fiber, the KK-monopole in [[11d supergravity]] becomes the KK-monopole in [[5d supergravity]]. Further compactifying on a circle leads to a [[black hole]] in 4d, incarnated as a D0/D6 bound state (e.g. [Nelson 93](#Nelson93)).

[[!include KK-monopole geometries -- table]]

## Properties

(For the moment the following is all about the KK-monopoles in [[11d supergravity]]/[[M-theory]].)

### Far-horizon geometry
 {#NearHorizonGeometry}

We discuss the [[far horizon geometry]] of coincident MK6-branes.

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


### Relation to the D6-brane in type IIA string theory 
 {#RelationToTheD6Brane}

Under the relation between [[M-theory]] and [[type IIA superstring theory]] an [[ADE orbifold]] of the 11d KK-monopole  corresponds to [[D6-branes]] combined with [[O6-planes]] ([Townsend 95, p. 6](#Townsend95), [Atiyah-Witten 01, p. 17-18](#AtiyahWitten01) see also e.g. [Berglund-Brandhuber 02, around p. 15](#BerglundBrandhuber02)). 

By ([Townsend 95, (1)](#Townsend95), [Sen 97c (1)-(4)](#Sen97c)) the 11d [[spacetime]] describing the KK-monopole lift of a plain single D6 brane is   $\mathbb{R}^{6,1}\times \mathbb{R}^3\times S^1$ with [[metric tensor]] away from the origin of the $\mathbb{R}^3$-factor (which is the locus of the lifted D6/monopole) being  

$$
  d s_{11}^2 =
  - d t^2 
  + d s_{\mathbb{R}^6}^2
  + (1+\mu/r) d s_{\mathbb{R}^3}^2
  + (1+ \mu/r)^{-1} (d x^{11} - A_i d x^i)^2
  \,,
$$

where 

* $A = A_i d x^i$ is any 3-form on $\mathbb{R}^3$ satisfying $d_{\mathbb{R}^3} A = \star d (1-\mu/r)$;

* $r$ denotes the distance in $\mathbb{R}^3$ from the origin.

* $\mu$ is the [[charge]] of the monopole.

<div style="float:left;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/TaubNUT.png" width="300">
</div>


Away from $\{0\} \in \mathbb{R}^3$ this gives a [[circle bundle]] with [[first Chern class]] measured by the integral of $R_0 \coloneqq d A$ (the [[RR-field]] of the [[D0-brane]]) over any [[sphere]] surrounding the singular locus in $\mathbb{R}^3 - \{0\}$. By the [[electric-magnetic duality]] between [[D0-branes]] and [[D6-branes]] (due to the [[self-dual higher gauge theory|self-duality]] of the [[RR-field]]) this means, from the 10-dimensional perspective, that at $0 \in \mathbb{R}^3$ a [[D6-brane]] is located.

> graphics grabbed from [Acharya-Gukov 04](#AcharyaGukov04)


Notice that the circle bundle away from its degeneration locus as a bundle over $S^2 \hookrightarrow \mathbb{R}^3 -\{0\}$ is necessarily of the form $S^3 \to S^2$, a multiple of the [[complex Hopf fibration]] (see also [Atiyah-Maldacena-Vafa 00, p. 10](#AtiyahMaldacenaVafa00)).

Discussion as an [[ADE singularity|A-type ADE singularity]] is in ([Sen 97c, section 2](#Sen97c)).  Generalization to [[ADE singularity|D-type singularities]] and hence D6-branes in [[orientifolds]] is in ([Sen 97c ,section 3](#Sen97c)). 
Discussion as the [[fixed point]] of the [[circle group]]-[[action]] on the M-theory circle fibers is in ([Townsend 95, p. 6](#Townsend95), [Atiyah-Witten 01, pages 17-18](#AtiyahWitten01)). Witten emphasizes that it is important that the location of the D6 is not just a [[cyclic group]] [[orbifold]] singularity but really a [[circle group]]-[[action]] [[fixed point]] [[conical singularity]]:

> {#Witten01OnConicalSingularity} Chiral fermions arise when the locus of A&#8722;D&#8722;E singularities passes through isolated points at which X has an isolated conical singularity that is not just an orbifold singularity ([Witten 01, p. 2](#Witten01)).
  
Discussion dealing carefully with the perspective where the locus of the [[D6-brane]] is not taken out is in ([Gaillard-Schmude 09](#GaillardSchmude09)).

For more on this see at _[D6-brane -- Relation to other branes](D6-brane#RelationToOtherBranes)_ and at _[[M-theory lift of gauge enhancement on D6-branes]]_.


### Relation to the D7-brane in type IIB string theory/F-theory

Under further [[T-duality]] to [[type IIB superstring theory]]/[[F-theory]] these D6-branes  become the [[D7-branes]].

[[!include F-branes -- table]]

### Other Brane charges (?)

In ([Hull 97](#Hull97)) it was argued that the KK-monopole in [[11-dimensional supergravity]] is the object which carries the 6-form charge [[Poincaré duality|Poincaré dual]] to the time-component of the 5-form charge of the [[M5-brane]] as appearing in the [[M-theory super Lie algebra]] via

$$
  \wedge^5 (\mathbb{R}^{10,1})^\ast
  \simeq
  \wedge^5 (\mathbb{R}^{10})^\ast \oplus \wedge^6 \mathbb{R}^{10}
  \,.
$$


(The same kind of relation identifies the time-component of the [[M2-brane]] charge with the charge of the [[M9-brane]], see there.)


## Related concepts

* [[M-brane]]

* [[Taub-NUT spacetime]]

* [[gravitational instanton]]


## References

### In 5d gravity

Original articles:

* {#Sorkin83} [[Rafael Sorkin]], _Kaluza-Klein monopole_, Phys. Rev. Lett. 51 (1983) 87 ([doi:10.1103/PhysRevLett.51.87](https://doi.org/10.1103/PhysRevLett.51.87))

* {#GrossPerry83} [[David Gross]], [[Malcolm Perry]], _Magnetic Monopoles in Kaluza-Klein Theories_,  Nucl. Phys. B226 (1983) 29 (<a href="https://doi.org/10.1016/0550-3213(83)90462-5">doi:10.1016/0550-3213(83)90462-5</a>)

* {#Ruback86} P. J. Ruback, _The motion of Kaluza-Klein monopoles_, Comm. Math. Phys. Volume 107, Number 1 (1986), 93-102 ([euclid:1104115933](https://projecteuclid.org/euclid.cmp/1104115933))

* A. L. Cavalcanti de Oliveira, E. R. Bezerra de Mello, _Kaluza-Klein Magnetic Monopole in Five-Dimensional Global Monopole Spacetime_, Class. Quant. Grav. 21 (2004) 1685-1694 ([arXiv:hep-th/0309189](http://arxiv.org/abs/hep-th/0309189))

Review includes

* Emre Sakarya, _Kaluza-Klein monopole_, 2007 ([pdf](https://inspirehep.net/record/875942/files/875942.pdf))

Discussion of [[topological T-duality]] for KK-monopoles is in

* {#Pande06} Ashwin S. Pande, _Topological T-duality and Kaluza-Klein Monopoles_, Adv. Theor. Math. Phys., 12, (2007), pp 185-215 ([arXiv:math-ph/0612034](https://arxiv.org/abs/math-ph/0612034))


### In 11d supergravity

#### Original articles

* {#HanKoh85} Seung Kee Han, I. G. Koh, _$N = 4$ Remaining Supersymmetry in Kaluza-Klein Monopole Background in D=11 Supergravity Theory_, Phys.Rev. D31 (1985) 2503, in [[Michael Duff]] (ed.), _[[The World in Eleven Dimensions]]_ 57-60 ([doi:10.1103/PhysRevD.31.2503](https://doi.org/10.1103/PhysRevD.31.2503), [spire:204521](http://inspirehep.net/record/204521))

* {#Townsend95} [[Paul Townsend]], _The eleven-dimensional supermembrane revisited_, Phys. Lett. B350:184-187, 1995 ([arXiv:hep-th/9501068](http://arxiv.org/abs/hep-th/9501068))

* {#Hull97} [[Chris Hull]], _Gravitational Duality, Branes and Charges_, Nucl.Phys. B509 (1998) 216-251 ([arXiv:hep-th/9705162](http://arxiv.org/abs/hep-th/9705162))

* {#Sen97a} [[Ashoke Sen]], _Kaluza-Klein Dyons in String Theory_, Phys. Rev. Lett. 79:1619-1621, 1997 ([arXiv:hep-th/9705212](http://arxiv.org/abs/hep-th/9705212))

* {#Sen97b} [[Ashoke Sen]], _Dynamics of Multiple Kaluza-Klein Monopoles in M- and String Theory_, Adv. Theor. Math. Phys. 1:115-126, 1998 ([arXiv:hep-th/9707042](https://arxiv.org/abs/hep-th/9707042))

* {#Sen97c} [[Ashoke Sen]], _A Note on Enhanced Gauge Symmetries in M- and String Theory_, JHEP 9709:001,1997 ([arXiv:hep-th/9707123](http://arxiv.org/abs/hep-th/9707123))

* {#IMSY98} Nissan Itzhaki, [[Juan Maldacena]], Jacob Sonnenschein, Shimon Yankielowicz, _Supergravity and The Large $N$ Limit of Theories With Sixteen Supercharges_, Phys. Rev. D 58, 046004 1998 ([arXiv:hep-th/9802042](https://arxiv.org/abs/hep-th/9802042))

* {#Asano00} Masako Asano, _Compactification and Identification of Branes in the Kaluza-Klein monopole backgrounds_ ([arXiv:hep-th/0003241](https://arxiv.org/abs/hep-th/0003241))

* {#AtiyahMaldacenaVafa00} [[Michael Atiyah]], [[Juan Maldacena]], [[Cumrun Vafa]], _An M-theory Flop as a Large N Duality_, J.Math.Phys.42:3209-3220,2001 ([arXiv:hep-th/0011256](http://arxiv.org/abs/hep-th/0011256))


* {#AtiyahWitten01} [[Michael Atiyah]], [[Edward Witten]] _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([arXiv:hep-th/0107177](http://arxiv.org/abs/hep-th/0107177))



* {#Witten01} [[Edward Witten]], _Anomaly Cancellation On Manifolds Of $G_2$ Holonomy_ ([arXiv:hep-th/0108165](http://arxiv.org/abs/hep-th/0108165))

* {#BerglundBrandhuber02} Per Berglund, Andreas Brandhuber, _Matter From $G_2$ Manifolds_, Nucl.Phys. B641 (2002) 351-375 ([arXivLhep-th/0205184](http://arxiv.org/abs/hep-th/0205184))

* {#GaillardSchmude09} [[Jérôme Gaillard]], [[Johannes Schmude]], _The lift of type IIA supergravity with D6 sources: M-theory with torsion_, JHEP 1002:032,2010 ([arXiv:0908.0305](http://arxiv.org/abs/0908.0305))

Discussion in terms of [[G-structures]]:

* [[Ulf Danielsson]], [[Giuseppe Dibitetto]], Adolfo Guarino, _KK-monopoles and $G$-structures in M-theory/type IIA reductions_, JHEP 1502 (2015) 096 ([arXiv:1411.0575](https://arxiv.org/abs/1411.0575))

#### Review

* [[Clifford Johnson]], section 10.5 of _D-brane primer_ ([arXiv:hep-th/0007170](http://arxiv.org/abs/hep-th/0007170))

* [[Katrin Becker]], [[Melanie Becker]], [[John Schwarz]], p. 333 of _String Theory and M-Theory: A Modern Introduction_, 2007


* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], section 6.3.3 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012

* {#AcharyaGukov04} [[Bobby Acharya]], [[Sergei Gukov]], p. 45 of _M theory and Singularities of Exceptional Holonomy Manifolds_, Phys.Rept.392:121-189,2004 ([arXiv:hep-th/0409191](http://arxiv.org/abs/hep-th/0409191))

### Relation to black holes

Relation to [[black holes in string theory]]

* {#Nelson93} William Nelson, _Kaluza-Klein Black Holes in String Theory_, Phys.Rev.D49:5302-5306,1994 ([arXiv:hep-th/9312058](http://arxiv.org/abs/hep-th/9312058))


[[!redirects Kaluza-Klein monopoles]]

[[!redirects KK monopole]]
[[!redirects KK monopoles]]

[[!redirects KK-monopole]]
[[!redirects KK-monopoles]]

[[!redirects MK6]]
[[!redirects MK6-brane]]
[[!redirects MK6-branes]]
