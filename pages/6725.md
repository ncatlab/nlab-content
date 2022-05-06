
> This entry is about the conjectured relation ([[duality in string theory|duality]]) between [[M-theory]] at [[MO9]]-planes and [[heterotic string theory]] on these. For the relation of [[M-theory]] [[KK-compactification|KK-compactified]] on a [[K3-surface]] and [[heterotic string theory]] on a [[3-torus]] see instead at _[[duality between M/F-theory and heterotic string theory]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Duality in string theory
+-- {: .hide}
[[!include duality in string theory -- contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

There is an observation by [Ho&#345;ava--Witten 95](#HoravaWitten95), [Ho&#345;ava--Witten 96](#HoravaWitten96) which suggests that [[M-theory]] on an  [[cyclic group of order 2|Z/2]]-[[orbifold]] (actually a [[higher orientifold]]) of the form $X_{10} \times (S^1 \slash \mathbb{Z}_2))$ in "[[duality in string theory|dual]]" to [[heterotic string theory]] on its [[boundary]] ([[fixed point]]) "[[M9-brane]]". Therefore one also speaks of "heterotic [[M-theory]]" ([Ovrut 02](#Ovrut02)). 

<center>
<img src="https://ncatlab.org/nlab/files/M2BraneEndingOnM9.jpg" width="500">
</center>

> from [Kashima 00](#Kashima00)

In the above the circle factor is taken to be the [[circle]] [[fiber]] over the 10d [[type IIA string theory|type IIA]] [[spacetime]]. 

If instead one considers another of the spatial dimensions to be compactified on $S^1\sslash \mathbb{Z}_2$, then, after [[T-duality]] ([[F-theory]]) result is supposed to be [[type I string theory]]. In this case the intersection of the [[M2-brane]] with the [[M9-brane]] (the latter now wrapping the M-theory circle fiber) is called the _[[E-string]]_.

More in detail:

One considers the [[KK-compactification]] of [[M-theory]] on a [[cyclic group of order 2|Z/2]]-[[orbifold]] of a [[torus]], hence of the [[Cartesian product]] of two [[circles]] 

$$  
  \array{
    & S^1_A &\times& S^1_B
    \\
    \text{radius}: &  R_{11} && R_{10}
  }
$$

such that the reduction on the first factor $S^1_A$ corresponds to the [[duality between M-theory and type IIA string theory]], hence so that subsequent [[T-duality]] along the second factor yields [[type IIB string theory]] (in its [[F-theory]]-incarnation). Now the diffeomorphism which exchanges the two circle factors and hence should be a symmetry of M-theory is interpreted as [[S-duality]] in [[type II string theory]]:

$$
  IIB \overset{S}{\leftrightarrow} IIB
$$

<center>
<img src="https://ncatlab.org/nlab/files/HoaravaWittenCompactifications.jpg" width="500">  
</center>


> graphics taken from [Horava-Witten 95, p. 15](#HoravaWitten95) 

If one considers this situation additionally with a $\mathbb{Z}/2\mathbb{Z}$-[[orbifold]] quotient of the first circle factor, one obtains the [[duality between M-theory and heterotic string theory]] ([[Horava-Witten theory]]). If instead one performs it on the second circle factor, one obtains [[type I string theory]].

Here in both cases the [[involution]] [[action]] is by [[reflection]] of the circle at a line through its center. Hence if we identify $S^1 \simeq \mathbb{R} / \mathbb{Z}$ then the action is by multiplication by /1 on the [[real line]].

In summary:

M-theory on

* $(S^1_A \sslash \mathbb{Z}_2 ) \times S^1_B$ yields [[heterotic string theory]]

* $S^1_A \times \left( S^1_B \sslash \mathbb{Z}_2 \right)$ yields [[type I string theory]]

Hence the [[S-duality]] that swaps the two circle factors corresponds to _[[duality between type I and heterotic string theory]]_. 



$$
  \array{
     HE 
       &\overset{KK/\mathbb{Z}^A_2}{\leftrightarrow}& 
     M 
       &\overset{KK/\mathbb{Z}^B_2}{\leftrightarrow}& 
     I'
     \\
     \mathllap{T}\updownarrow
     &&  && 
     \updownarrow \mathrlap{T}  
     \\
     HO 
     && \underset{\phantom{A}S\phantom{A}}{\leftrightarrow} && 
     I
  }
$$

<center>
<img src="https://ncatlab.org/nlab/files/HoravaWittenCompactificationsII.jpg" width="500">  
</center>

> graphics taken from [Horava-Witten 95, p. 16](#HoravaWitten95) 


### Duality between M-theory and heterotic string theory

Here each of the two copies of the heterotic gauge theory is a "[[hidden sector]]" with respect to the other.

The orbifold equivariance condition of the [[supergravity C-field]] is that discussed at _[[orientifold]]_ (there for the [[B-field]]). Therefore it has to vanish at the two fixed fixed points of the $\mathbb{Z}_2$-action. Thereby the quantization condition

$$
  [2G_4] = 2 [c_2] - [\frac{1}{2} p_1]
$$ 

on the [[supergravity C-field]] becomes the condition for the [[Green-Schwarz mechanism]] of the [[heterotic string theory]] on the "boundary" (the orbifold fixed points).

### Duality between M-theory and type I string theory

[[duality between M-theory and type I string theory]]

originally suggested in ([Horava-Witten 95, section 3](#HoravaWitten95))

Further evidence is reviewed in [APT 98](#APT98)

### Duality between heterotic and type I string theory

[[duality between heterotic and type I string theory]]

via [[S-duality]] in the [[F-theory]]-picture...

## Related concepts

* [[duality between F-theory and heterotic string theory]]

[[!include KK-compactifications of M-theory -- table]]


## Properties

### Boundary conditions
 {#BoundaryConditions}

The [[supergravity C-field]] $\hat G_4$ is supposed to vanish, and _differentially_ vanish at the boundary in the HW model, meaning that also the local connection 3-form $C_3$ vanishes there. The argument is roughly as follows (similar for as in [Falkowski, section 3.1](#Falkowski)).


The [[higher dimensional Chern-Simons theory|higher Chern-Simons term]] 

$$
  C_3 \mapsto C_3 \wedge G_4 \wedge G_4
$$

in the [[Lagrangian]] of [[11-dimensional supergravity]] is supposed to be well-defined on fields on the [[orbifold]] and hence is to be $\mathbb{Z}_2$-invariant. 

Let $\iota_{11}$ be the canonical vector field along the circle factor. Then the component of $G \wedge G$ which is annihilated by the contraction $\iota_{11}$ is necessarily even, so the component $d x^{11}\wedge \iota_11 C_3$ is also even. It follows that also $d x^{11}\wedge \iota_11 G_4$ is even. 

Moreover, the kinetic term

$$
  C \mapsto G \wedge \star G
$$

is to be invariant. With the above this now implies that the components of $G$ annihiliated by $\iota_{11}$ is odd, because so is the mixed component of the [[metric]] tensor.

This finally implies that the restriction of $C_3$ to the orbifold fixed points has to be closed.

## Related concepts

* [[duality in string theory]]

  * [[duality between F-theory and heterotic string theory]]

* [[11-dimensional supergravity]]

* [[M-theory]], [[heterotic string theory]]

* [[M9-brane]]


## References

### General

The original articles are

* {#HoravaWitten95} [[Petr Hořava]], [[Edward Witten]], _Heterotic and Type I string dynamics from eleven dimensions_, Nucl. Phys. B460 (1996) 506 ([arXiv:hep-th/9510209](http://arxiv.org/abs/hep-th/9510209))

* [[Edward Witten]], _Strong Coupling Expansion Of Calabi-Yau Compactification_, Nucl. Phys.B 471:135-158, 1996 ([arXiv:hep-th/9602070](https://arxiv.org/abs/hep-th/9602070))

* {#HoravaWitten96} [[Petr Hořava]], [[Edward Witten]],  _Eleven dimensional supergravity on a manifold with boundary_, Nucl. Phys. B475 (1996) 94 ([arXiv:hep-th/9603142](http://arxiv.org/abs/hep-th/9603142))
 

Review is in 

* [[Piyush Kumar]], _Ho&#345;ava-Witten theory_ (2004) ([pdf](http://theory.uchicago.edu/~sethi/Teaching/P484-W2004/hwitten.pdf))

* [[Paul Townsend]], _Four Lectures on M-Theory_ ([arXiv:hep-th/9612121](http://arxiv.org/abs/hep-th/9612121)). 

* {#Ovrut02} [[Burt Ovrut]], _Lectures on Heterotic M-Theory_, TASI 2001. 2004. 359-407  ([arXiv:hep-th/0201032](http://arxiv.org/abs/hep-th/0201032), [doi:10.1142/9789812702821_0007](https://doi.org/10.1142/9789812702821_0007))

* {#Falkowski} [[Adam Falkowski]], section 3 of _Five dimensional locally supersymmetric theories with branes_, Master Thesis, Warsaw ([[FalkowskiLecture.pdf:file]])

The [[black brane|black]] [[M2-brane]] solution in HW-theory, supposedly yielding the [[black brane|black]] [[heterotic string]] at the intersection with the [[M9-brane]] is discussed in

* {#LalakLukasOvrut97} Zygmunt Lalak, Andr&eacute; Lukas, [[Burt Ovrut]], _Soliton Solutions of M-theory on an Orbifold_, Phys. Lett. B425 (1998) 59-70 ([arXiv:hep-th/9709214](https://arxiv.org/abs/hep-th/9709214))

* {#Kashima00} Ken Kashima, _The M2-brane Solution of Heterotic M-theory with the Gauss-Bonnet $R^2$ terms_, Prog.Theor.Phys. 105 (2001) 301-321 ([arXiv:hep-th/0010286](https://arxiv.org/abs/hep-th/0010286))

More on the [[Green-Schwarz mechanism]] in [[Hořava-Witten theory]]:

* E. Dudas, J. Mourad, _On the strongly coupled heterotic string_, Phys. Lett. B400 (1997) 71-79 ([arXiv:hep-th/9701048](https://arxiv.org/abs/hep-th/9701048))

* [[Adel Bilal]], Jean-Pierre Derendinger, Roger Sauser, _M-Theory on $S^1/\mathbb{Z}_2$: New Facts from a Careful Analysis_, Nucl. Phys. B576 (2000) 347-374 ([arXiv:hep-th/9912150](https://arxiv.org/abs/hep-th/9912150))


* Ian G Moss, _A new look at anomaly cancellation in heterotic M-theory_, Phys. Lett. B637 (2006) 93-96 ([arXiv:hep-th/0508227](https://arxiv.org/abs/hep-th/0508227))

* Sergio Lukic, [[Gregory Moore]], _Flux corrections to anomaly cancellation in M-theory on a manifold with boundary_ ([arXiv:hep-th/0702160](https://arxiv.org/abs/hep-th/0702160))

* Ian G Moss, _Higher order terms in an improved heterotic M theory_, JHEP 0811:067, 2008 ([arXiv:0810.1662](https://arxiv.org/abs/0810.1662))




* [[Fei Han]], [[Kefeng Liu]], [[Weiping Zhang]], _Anomaly Cancellation and Modularity. II: $E_8 \times E_8$ case_, Sci. China Math. 60, 985–994 (2017) ([arXiv:1209.4540](https://arxiv.org/abs/1209.4540), [doi:10.1007/s11425-016-9034-1](https://doi.org/10.1007/s11425-016-9034-1))



Explicit discussion of [[worldvolume]] [[CFT]] of the [[M2-branes]] ending on the HW fixed points and becoming [[heterotic strings]] is discussed, via the [[BLG model]], in 

* {#Lambert15} [[Neil Lambert]], _Heterotic M2-branes_, Physics Letters B Volume 749, 7 October 2015, Pages 363&#8211;367 ([arXiv:1507.07931](http://arxiv.org/abs/1507.07931))


After [[KK-reduction]] to [[5d supergravity]] there is a corresponding 5d mechanism, see the references [there](5-dimensional+supergravity#ReferencesHWCompactification).


Disucussion of the [[duality between heterotic and type I string theory]] includes

* {#APT98} I. Antoniadis, H. Partouche, T.R. Taylor, _Lectures on Heterotic-Type I Duality_, Nucl.Phys.Proc.Suppl. 61A (1998) 58-71; Nucl.Phys.Proc.Suppl. 67 (1998) 3-1

Discussion of [[string phenomenology]] in Horava-Witten theory:

* {#Ovrut18} [[Burt Ovrut]], _Vacuum Constraints for Realistic Heterotic M-Theories_, Symmetry 2018, 10(12), 723 ([arXiv:1811.08892](https://arxiv.org/abs/1811.08892), [doi:10.3390/sym10120723](https://doi.org/10.3390/sym10120723))

### Phenomenology

Discussion of [[phenomenology]]/[[string phenomenology]] for the [[heterotic M-theory]], relating to the [[standard model of particle physics]]:


* {#DOPW99} [[Ron Donagi]], [[Burt Ovrut]], [[Tony Pantev]], [[Daniel Waldram]], _Standard Models from Heterotic M-theory_, Adv. Theor. Math. Phys. 5 (2002) 93-137 ([arXiv:hep-th/9912208](https://arxiv.org/abs/hep-th/9912208))

* {#DOPW00} [[Ron Donagi]], [[Burt Ovrut]], [[Tony Pantev]], [[Daniel Waldram]], _Standard Model Vacua in Heterotic M-Theory_, talk at [Strings '99](http://strings99.aei.mpg.de/), Potsdam, Germany, 19 - 24 Jul 1999 ([arXiv:hep-th/0001101](https://arxiv.org/abs/hep-th/0001101))



### Gaugino condensation and supersymmetry breaking
 {#ReferencesGauginoCondensation}

Discussion of [[gaugino condensation]] and [[supersymmetry breaking]] in Horava-Witten theory, where the two heterotic [[MO9-branes]] provide a natural mechanism for [[supersymmetry breaking]] on one (the physical brane) by gaugino condensation on the other (the "dark sector" brane):

lecture notes:

* {#Nilles04} [[Hans-Peter Nilles]], _Gaugino Condensation and SUSY Breakdown_, Lectures at Cargese School of Physics and Cosmology, Cargese, France, August 2003 ([arXiv:hep-th/0402022](https://arxiv.org/abs/hep-th/0402022))

original articles:

* I. Antoniadis, M. Quiros, _On the M-theory description of gaugino condensation_, Phys.Lett. B416 (1998) 327-333 ([arXiv:hep-th/9707208](https://arxiv.org/abs/hep-th/9707208))

* I. Antoniadis, M. Quiros, _Supersymmetry breaking in M-theory and gaugino condensation_, Nucl.Phys. B505 (1997) 109-122 ([arXiv:hep-th/9705037](https://arxiv.org/abs/hep-th/9705037))

* [[André Lukas]], [[Burt Ovrut]], [[Daniel Waldram]], _Gaugino condensation in M theory on $S^1/Z_2$_, Phys. Rev. D 57, 7529 (1998) ([arXiv:hep-th/9711197](https://arxiv.org/abs/hep-th/9711197), [doi:10.1103/PhysRevD.57.7529](https://doi.org/10.1103/PhysRevD.57.7529))

* [[André Lukas]], [[Burt Ovrut]], [[Daniel Waldram]], _Five-Branes and Supersymmetry Breaking in M-Theory_, JHEP 9904:009, 1999 ([arXiv:hep-th/9901017](https://arxiv.org/abs/hep-th/9901017))

specifically for [[M-theory on S1/G_HW times H/G_ADE]]:

* Zygmunt Lalak, Steven Thomas, _Gaugino Condensation, Moduli Potentials and Supersymmetry Breaking in M-Theory Models_, Nuclear Physics B
Volume 515, Issues 1–2, 30 March 1998, Pages 55-72
Nuclear Physics B ([hep-th/9707223](https://arxiv.org/abs/hep-th/9707223), <a href="https://doi.org/10.1016/S0550-3213(97)00784-0">doi:10.1016/S0550-3213(97)00784-0</a>)


### Generalization to M-theory on $S^1/G_{HW} \times \mathbb{H}/G_{ADE}$

Generalization to [[M-theory on S1/G_HW times H/G_ADE]]:

* Zygmunt Lalak, Steven Thomas, _Gaugino Condensation, Moduli Potentials and Supersymmetry Breaking in M-Theory Models_ ([hep-th/9707223](https://arxiv.org/abs/hep-th/9707223))

* V. Kaplunovsky, [[Jacob Sonnenschein]],[[Stefan Theisen]], S. Yankielowicz, _On the Duality between Perturbative Heterotic Orbifolds and M-Theory on $T^4/Z_N$_ ([arXiv:hep-th/9912144](https://arxiv.org/abs/hep-th/9912144))

* {#GKSTY02} E. Gorbatov, V.S. Kaplunovsky, J. Sonnenschein, [[Stefan Theisen]], S. Yankielowicz, _On Heterotic Orbifolds, M Theory and Type I' Brane Engineering_, JHEP 0205:015, 2002 ([arXiv:hep-th/0108135](https://arxiv.org/abs/hep-th/0108135))

* {#GaiottoTomasiello14} [[Davide Gaiotto]], [[Alessandro Tomasiello]], _Holography for $(1,0)$ theories in six dimensions_, JHEP12(2014)003 ([arXiv:1404.0711](https://arxiv.org/abs/1404.0711))



* {#DHTV14} Michele Del Zotto, [[Jonathan Heckman]], [[Alessandro Tomasiello]], [[Cumrun Vafa]], Section 6 of: _6d Conformal Matter_, JHEP02(2015)054 ([arXiv:1407.6359](https://arxiv.org/abs/1407.6359))

* {#HSS18} [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]], Example 2.2.7 of: _[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]_, CMP (2019) ([arXiv:1805.05987](https://arxiv.org/abs/1805.05987), [doi:10.1007/s00220-019-03442-3](http://link.springer.com/article/10.1007/s00220-019-03442-3))

### For 7d supergravity

Discussion for [[7d supergravity]]:

* {#GherghettaKehagias02} Tony Gherghetta, [[Alex Kehagias]], _Anomaly Cancellation in Seven-Dimensional Supergravity with a Boundary_, Phys.Rev. **D68** (2003), 065019, ([arXiv:hep-th/0212060](http://arxiv.org/abs/hep-th/0212060))

* Spyros D. Avramis, [[Alex Kehagias]], _Gauged $D=7$ Supergravity on the $S^1/\mathbb{Z}_2$ Orbifold_ ([arXiv:hep-th/0407221](https://arxiv.org/abs/hep-th/0407221))

* T.G. Pugh, [[Ergin Sezgin]], [[Kellogg Stelle]], _$D=7$ / $D=6$ Heterotic Supergravity with Gauged R-Symmetry_ ([arXiv:1008.0726](https://arxiv.org/abs/1008.0726))



[[!redirects Hořava-Witten theory]]
[[!redirects Hořava–Witten theory]]
[[!redirects Hořava--Witten theory]]
[[!redirects Horava-Witten theory]]
[[!redirects Horava–Witten theory]]
[[!redirects Horava--Witten theory]]

[[!redirects heterotic M-theory]]

[[!redirects duality between M-theory and heterotic string theory]]
[[!redirects duality between heterotic string theory and M-theory]]

[[!redirects duality heterotic string theory and M-theory]]


[[!redirects duality between M-theory and type I string theory]]
[[!redirects duality between type I string theory and M-theory]]

[[!redirects HET - M]]
[[!redirects HET - M duality]]

[[!redirects M - HET]]
[[!redirects M - HET duality]]

