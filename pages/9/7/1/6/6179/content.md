
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Duality in string theory
+-- {: .hide}
[[!include duality in string theory -- contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Langlands correspondence
+--{: .hide}
[[!include Langlands correspondence -- contents
]]
=--
=--
=--



The term _S-duality_ can mean two different things:

* in [[mathematics]] it is short for _[[Spanier-Whitehead duality]]_ : [[dual object|monoidal duality]] in the [[stable homotopy category]];

* in [[physics]] it denotes a certain equivalence between [[quantum field theories]], this is what we discuss below

--

#Contents#
* tabe of contents
{:toc}

## Idea

In the original and restricted sense, _S-duality_ refers to the conjectured [[Montonen-Olive duality]] auto-[[equivalence]] of ([[super Yang-Mills theory|super]]) [[Yang-Mills theory]] in 4 dimensions under which the [[coupling constant]] is inverted, and more generally under which the combined [[coupling constant]] and [[theta angle]] tranform under an action of the [[modular group]]. At least for [[super Yang-Mills theory]] this conjecture can be argued for in detail. 

There is also a [[duality in string theory]] called _S-duality_. Specifically in [[type IIB superstring theory]]/[[F-theory]] this is given by an action of the [[modular group]] on the [[axio-dilaton]], hence is, via the proportionality of the dilaton to the [[string coupling constant]], again a weak-strong coupling duality.

Indeed, at least for [[super Yang-Mills theory]] Montonen-Olive S-duality may be understood as a special case of the [[duality in string theory|string duality]] ([Witten 95a](#Witten95a), [Witten 95b](#Witten95b)): one may understand [[N=2 D=4 super Yang-Mills theory]] as the [[KK-compactification]] of the [[M5-brane]] [[6d (2,0)-superconformal QFT]] on the [[F-theory]] torus ([Johnson 97](#Johnson97)) to get the [[D3-brane]] worldvolume theory, and the remnant [[modular group]] action on the compactified torus is supposed to be the 4d Montonen-Olive S-duality ([Witten 07](#Witten07)).

### In (super) Yang-Mills theory

#### General idea

In its original form, S-duality refers to **Montonen-Olive duality** , which is about the following phenomenon:

The [[Lagrangian]] of [[Yang-Mills theory]] has two summands, 

$$
  S_{YM} : \nabla \mapsto \int_X \frac{1}{e^2} \langle F_\nabla \wedge \star F_\nabla\rangle
   + \int_{X} i \theta \langle F_\nabla \wedge F_\nabla \rangle
  \,,
$$

each pairing the [[curvature]] 2-form with itself in an [[invariant polynomial]], but the first involving the [[Hodge star operator]] dual, and the second not. One can combine the coefficients $\frac{1}{e^2}$ and $i \theta$ into a single _[[complex number|complex]] [[coupling constant]]_

$$
  \tau = \frac{\theta}{2 \pi} +  \frac{4 \pi i}{e^2}
  \,.
$$

Montonen-Olive duality asserts that the quantum field theories induced from one such parameter value and another one obtained from it by an [[action]] of [[SL(2,Z)]] on the [[upper half plane]] are equivalent.

This is actually not quite true for ordinary Yang-Mills theory, but seems to be true for [[N=2 D=4 super Yang-Mills theory]].


#### From compactification of the 6d (2,0)-SCFT and AGT correspondence
 {#ForSYMFromCompactification}

In ([Witten 95a](#Witten95a), [Witten 95b](#Witten95b), [Witten 07](#Witten07)) it was suggested that the above S-duality of [[N=2 D=4 super Yang-Mills theory]] may be understood geometrically by regarding the super Yang-Mills theory as the [[Kaluza-Klein compactification]] of the [[6d (2,0)-superconformal QFT]] -- that instead of a [[gauge field]] given by a [[principal bundle]] with [[connection on a bundle|connection]] involves a [[principal 2-bundle]] with [[connection on a 2-bundle|2-connection]] -- on a [[complex torus]]. The $SL(2,\mathbb{Z})$-invariance of the resulting 4-dimensional theory is then the [[modular group]] remnant of the conformal invariance of the 6-dimensional theory under conformal transformations of that torus.

Moreover, Witten has suggested that this S-duality secretly drives a host of other subtle phenomena, notably that the [[geometric Langlands duality]] (see there for more) is just an aspect of a special case of this.

The [[AGT correspondence]] refines this further and regards the [[6d (2,0)-superconformal QFT]] as something like a "[[2d SCFT]] with values in 4d super-Yang-Mills theories". This way the whole [[mapping class group]] of general 2d [[Riemann surfaces]] acts as a generalized S-duality on 4d super-Yang-Mills theory

### In string theory

In [[string theory]], S-duality is supposed to apply to whole string theories and make [[type II string theory]] be S-dual to itself and make  [[heterotic string theory]] be S-dual to [[type I string theory]].

#### Type IIB S-duality
 {#InTypeIIB}

##### General idea

[[Type IIB string theory]] is obtained by [[KK-compactification]] of [[M-theory]] on a [[torus]] bundle followed by [[T-duality|T-dualizing]] one of the torus cycles. This perspective -- referred to as [[F-theory]] -- exhibits the [[axio-dilaton]] of type IIB string theory as the fiber of an [[elliptic fibration]] (essentially the torus bundle that M-theory was compactified on ([Johnson 97](#Johnson97))).

The [[modular group]] acts on this [[elliptic fibration]], and this is S-duality for type IIB-strings. In particular the transformation $\tau \mapsto - \frac{1}{\tau}$ inverts the type II coupling constant.  See at _[[F-theory]]_ for more.

The type IIB [[F1-string]] and the [[D1-brane]] appear this way by [[double dimensional reduction]] from the [[M2-brane]] wrapping (either) one of the two cycles of the compactifying torus. S-duality mixes these strings by the evident [[modular group]] action on the $(p,q)\in \mathbb{Z}^2$ labels of the 
[[(p,q)-strings]]. Here at least part of the S-duality action on $(p,q)$-strings may be seen as a system of autoequivalences of the [[super L-infinity algebras]] which defines the [[extended super spacetime]] constituted by the type II superstring ([Bandos 00](Bandos00), [FSS 13, section 4.3](#FSS13)).

Similarly the [[D5-brane]] and the [[NS5-brane]] are the [[double dimensional reduction]] of the [[M5-brane]] wrapping one of the two cycles of the compactifying torus, and hence the S-duality modular group also acts on $(p,q)$-5-branes, exchanging them.

Finally, the [[D3-brane]] is instead the [[double dimensional reduction]] of the [[M5-brane]], wrapping _both_ compactifying dimensions. Accordingly the worldvolume theory of the D3, which is [[super Yang-Mills theory]] in $d = 4$ has an S-self-duality. That is supposed to be the [[Montonen-Olive duality]] discussed above, which is thereby unified with type IIB S-duality. 

##### Cohomological nature of type II fields under S-duality
 {#CohomologicalNatureOfTypeIIFieldsUnderSDuality}

While [[F-theory]] does capture much of this [[non-perturbative effect|non-perturbative]] S-duality, there currently remains a puzzle as to the correct [[differential cohomology]] nature of all the fields under S-duality: by the above S-duality mixes the [[Kalb-Ramond field]] $\hat B_{NS}$ with the degree-3 component $\hat B_{RR}$ of the [[RR-field]]. But the best available description of the fine-structure of these fields is (see also at _[[orientifold]]_) that $\hat B_{NS}$ is a [[cocycle]] in ([[twisted cohomology|twisted]]) [[ordinary differential cohomology]] while $\hat B_{RR}$ is (only) one component of a cocycle in ([[twisted cohomology|twisted]]) [[KU]] (or really: [[KR-theory]]). 

This issue was first highlighted in ([DMW 00, section 11](#DMW00)). In ([DFM 03, section 9](supergravity+C-field#DFM)) it was observed that taking into account the [[cubical structure in M-theory]] on the [[higher dimensional Chern-Simons theory|11-dimensional Chern-Simons term]] of the [[supergravity C-field]] the conceptual mismatch is alleviated, but not quite resolved. See also ([BEJVS 05](#BEJVS05))

On the other hand, as discussed at _[[cubical structure in M-theory]]_, this structure plausibly relates to a [[generalized cohomology theory]] beyond [[ordinary cohomology]] and beyond [[K-theory]], namely to [[elliptic cohomology]]/[[tmf]]. Hints like this led in
([KrizSati 05](#KrizSati05)) to the [[conjecture]] that the right [[cohomology theory]] to capture the S-duality of [[type II superstring theory|type IIB]]/[[F-theory]] is [[modular equivariant elliptic cohomology]].


#### Heterotic/type I duality

> Something substantial should go here, for the moment the following is copied from a discussion forum comment by some Olof [here](http://physics.stackexchange.com/a/65546/5603):

For the Het/I relation, the first observation is that the massless spectra of the two models agree. Moreover, if we make the identification
$$
G^I_{\mu\nu} = e^{-\Phi_h} G^h_{\mu\nu} , \qquad
\Phi^I = - \Phi^h , \qquad
\tilde{F}^I_3 = \tilde{H}^h_3 , \qquad
A^I_1 = A^h_1
$$
the low energy effective supergravity actions of the two models match. Since the [[string coupling constants]] $g_s^I$ and $g_s^h$ are given as the expectation values of the exponentials of the dilatons $\exp(\Phi^I)$ and $\exp(\Phi^h)$, respectively, the above equations relates the type-I theory at strong coupling to the heterotic theory at weak coupling:
$$
g^I_s = \frac{1}{g^h_s} .
$$
From the relative scaling of the metric in (1) we also see that the string length in the two theories are related by
$$
l^I_s = l^h_s \sqrt{g^h_s}.
$$

As a non-perturbative check we can consider the tension of the type-I D1 brane. The brane is a BPS object, so for all values of the coupling $g_s^I$ the tension is given by the same formula
$$
T^I_{D1} = \frac{1}{g_s^I} \frac{1}{2\pi\left(l^I_s\right)^2} = \frac{g^h_s}{2\pi\left(l^h_s\sqrt{g^h_s}\right)^2} = \frac{1}{2\pi\left(l^h_s\right)^2}
$$ 
where I've used relations (2) and (3). But this is equal to the tension of the fundamental heterotic string
$$
T^h_{F1} = \frac{1}{2\pi\left(l^h_s\right)^2}.
$$
This indicates that it is sensible to identify the strong coupling limit of the type-I D1 brane with the heterotic string.

#### For type IIA

A priori [[type IIA superstring theory]] does not have S-duality, but by compactifying [[M-theory]] on a torus one can sort of read off what the non-perturbative additions to type IIA should be that make it have S-duality after all, see

* Gottfried Curio, Boris Kors, [[Dieter Lüst]], _Fluxes and Branes in Type II Vacua and M-theory Geometry with G(2) and Spin(7) Holonomy_, Nucl.Phys.B636:197-224,2002 ([arXiv:hep-th/0111165](http://arxiv.org/abs/hep-th/0111165))




## Overview

[[!include heterotic S-duality -- table]]

[[!include gauge theory from AdS-CFT -- table]]

## Related concepts

* [[Yang-Mills theory]]

* [[topologically twisted D=4 super Yang-Mills theory]]

[[duality in physics]], [[duality in string theory]]

* **S-duality**

  * [[electro-magnetic duality]]

    * [[Montonen-Olive duality]]

  * [[Seiberg duality]]

  * [[geometric Langlands correspondence]]

  * [[quantum geometric Langlands correspondence]]

* [[duality in string theory]]

  * [[T-duality]], [[U-duality]]

  * [[AdS/CFT correspondence]]

* [[type II string theory]], [[F-theory]]

  * [[(p,q)-string]]

  * [[modular equivariant elliptic cohomology]]
  


## References

* [[Mike Duff]], chapter 6 of _[[The World in Eleven Dimensions]]: Supgergravity, Supermembranes and M-theory_, IoP (1999)

### In (super-)Yang-Mills theory
 {#ReferencesInSYM}

It was originally noticed in

* {#GNO77} [[Peter Goddard]], [[Jean Nuyts]], [[David Olive]], *Gauge Theories And Magnetic Charge*, Nucl. Phys. B **125** (1977) 1-28 &lbrack;<a href="https://doi.org/10.1016/0550-3213(77)90221-8">doi:10.1016/0550-3213(77)90221-8</a>, [spire:111435](https://inspirehep.net/literature/111435)&rbrack;

that where [[electric charge]] in [[Yang-Mills theory]] takes values in the [[weight lattice]] of the [[gauge group]], then [[magnetic charge]] takes values in the lattice of what is now called the [[Langlands dual group]].

This led to the electric/magnetic duality conjecture formulation in

* [[Claus Montonen]], [[David Olive]], _Magnetic Monopoles As Gauge Particles?_ Phys. Lett. B72 (1977) 117-120.

According to ([Kapustin-Witten 06, pages 3-4](#KapustinWitten06)) the observaton that the Montonen-Olive dual charge group coincides with the [[Langlands dual group]] is due to 

* {#Atiyah77} [[Michael Atiyah]], private communication to [[Edward Witten]], 1977

Discussion of the duality for abelian gauge theory ([[electromagnetism]]) is is

* [[Edward Witten]], _On S-duality in abelian gauge theory_ Selecta Mathematica, (2):383-410, 1995 ([arXiv:hep-th/9505186](http://arxiv.org/abs/hep-th/9505186))

* Jose Barbon, _Generalized abelian S-duality and coset constructions_, Nuclear Physics B, 452(1):313-330, 1995 ([arXiv:hep-th/9506137](http://arxiv.org/abs/hep-th/9506137))

* Gerald Kelnhofer, _Functional integration and gauge ambiguities in generalized abelian gauge theories_ J. Geom. Physics, 59:1017-1035, 200

See also the references at _[[electro-magnetic duality]]_.

The insight that the Montonen-Olive duality works more naturally in [[super Yang-Mills theory]] is due to

* [[David Olive]], [[Edward Witten]], _Supersymmetry Algebras That Include Topological Charges_, Phys. Lett. B78 (1978) 97-101.

and that it works particularly for [[N=4 D=4 super Yang-Mills theory]] is due to

* H. Osborn, _Topological Charges For $N = 4$ Supersymmetric Gauge Theories And Monopoles Of Spin 1_, Phys. Lett. B83 (1979) 321-326.

with further computations in

* [[Cumrun Vafa]], [[Edward Witten]], _A Strong Coupling Test of S-Duality_, Nucl. Phys. B **431** (1994) 3-77 &lbrack;[arXiv:hep-th/9408074](http://arxiv.org/abs/hep-th/9408074)&rbrack;

The observation that the $\mathbb{Z}_2$ electric/magnetic duality extends to an $SL(2,\mathbb{Z})$-action in this case is due to 

* [[John Cardy]], E. Rabinovici, _Phase Structure Of Zp Models In The Presence Of A Theta Parameter_, Nucl. Phys. B205 (1982) 1-16; 

* [[John Cardy]], _Duality And The Theta Parameter In Abelian Lattice Models_, Nucl. Phys. B205 (1982) 17-26.

* A. Shapere and [[Frank Wilczek]], _Selfdual Models With Theta Terms_, Nucl. Phys. B320 (1989) 669-695.

The understanding of this $SL(2,\mathbb{Z})$-symmetry as a remnant conformal transformation on a 6-dimensional [[principal 2-bundle]]-theory -- the [[6d (2,0)-superconformal QFT]] -- compactified on a torus is described in 

* {#Witten95a} [[Edward Witten]], pages 4-5 of _Some Comments On String Dynamics_, Proceedings of _String95_ ([arXiv:hepth/9507121](http://arxiv.org/abs/hepth/9507121))

* {#Witten95b} [[Edward Witten]], _On S-Duality in Abelian Gauge Theory_ ([arXiv:hep-th/9505186](http://arxiv.org/abs/hep-th/9505186))

* {#Witten07} [[Edward Witten]], _[[Conformal field theory in four and six dimensions]]_ ([arXiv:0712.0157](http://arxiv.org/abs/0712.0157))

On an [[algorithm]] for constructing [[S-duality|S-dual]] [[quiver gauge theories]]:

* Chiung Hwang, [[Sara Pasquetti]], Matteo Sacchi, *Rethinking mirror symmetry as a local duality on fields*, Phys. Rev. D **106** (2022) 105014 &lbrack;[arXiv:2110.11362](https://arxiv.org/abs/2110.11362), [doi:10.1103/PhysRevD.106.105014](https://doi.org/10.1103/PhysRevD.106.105014)&rbrack;


* Riccardo Comi, Chiung Hwang, Fabio Marino, [[Sara Pasquetti]], Matteo Sacchi, *The $SL(2, \mathbb{Z})$ dualization algorithm at work* &lbrack;[arXiv:2212.10571](https://arxiv.org/abs/2212.10571)&rbrack;




### In type II superstring theory

The suggestion of an $SL(2,\mathbb{Z})$-duality action in [[type II superstring theory]] goes back to

* [[John Schwarz]], [[Ashoke Sen]], _Duality Symmetries Of $4D$ Heterotic Strings_, Phys. Lett. 312B (1993) 105-114, 

* [[Ashoke Sen]], _Dyon - Monopole Bound States, Self-Dual Harmonic Forms on the Multi-Monopole Moduli Space, and $SL(2,\mathbb{Z})$ Invariance in String Theory_ ([arXiv:hep-th/9402032](http://arxiv.org/abs/hep-th/9402032))


_Duality Symmetric Actions_, Nucl. Phys. B411 (1994) 35-63 ([arXiv:hep-th/9304154](http://arxiv.org/abs/hep-th/9304154))

* [[Chris Hull]], [[Paul Townsend]], _Unity of Superstring Dualities_, Nucl. Phys. B438:109-137,1995 ([arXiv:hep-th/9410167](http://arxiv.org/abs/hep-th/9410167))

* [[John Schwarz]], _An $SL(2,\mathbb{Z})$ Multiplet of Type IIB Superstrings_, Phys.Lett. B360 (1995) 13-18; Erratum-ibid. B364 (1995) 252 ([arXiv:hep-th/9508143](http://arxiv.org/abs/hep-th/9508143))

The geometric understanding of S-duality in [[type II superstring theory]] via [[M-theory]]/[[F-theory]] goes maybe back to

* {#Johnson97} [[Clifford Johnson]], _From M-theory to F-theory, with Branes_, Nucl.Phys. B507 (1997) 227-244 ([arXiv:hep-th/9706155](http://arxiv.org/abs/hep-th/9706155))

A textbook account is in 

* {#West12} [[Peter West]], section 17.3 of _[[Introduction to Strings and Branes]]_, Cambridge University Press 2012


A [[2-loop]] test is in 

* [[Eric D'Hoker]], Michael Gutperle, [[Duong Phong]], _Two-loop superstrings and S-duality_, Nucl.Phys. B 722 (2005) 81-118 ([arXiv:hep-th/0503180](http://arxiv.org/abs/hep-th/0503180))


S-duality acting on the [[worldsheet]] theory if [[(p,q)-strings]] is discussed for instance in 

* {#Bandos00} [[Igor Bandos]], _Superembedding Approach and S-Duality. A unified description of superstring and super-D1-brane_, Nucl. Phys. B **599** 197-227 (2001) ([arXiv:hep-th/0008249](http://arxiv.org/abs/hep-th/0008249))

Closely related to this, S-duality in [[type II string theory]] as an operation on the [[extended super spacetime]] [[super L-infinity algebra]] is 

* {#FSS13} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], section 4.3 of _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_ ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))


The cohomological problem of the type II S-duality action on the 3-form flux was originally highlighted in

* {#DMW00} D. Diaconescu, [[Gregory Moore]], [[Edward Witten]], _$E_8$ Gauge Theory, and a Derivation of K-Theory from M-Theory_, Adv.Theor.Math.Phys.6:1031-1134 2003 ([arXiv:hep-th/0005090](http://arxiv.org/abs/hep-th/0005090))

The conjecture that with combined targetspace/worldsheet modular transformations the type IIB S-duality is reflected in [[modular equivariant elliptic cohomology]] is due to 

* {#KrizSati05} [[Igor Kriz]], [[Hisham Sati]], _Type II string theory and modularity_, JHEP 0508 (2005) 038 ([arXiv:hep-th/0501060](http://arxiv.org/abs/hep-th/0501060))


See also

* {#BEJVS05} [[Peter Bouwknegt]], [[Jarah Evslin]], [[Branislav Jurco]], [[Mathai Varghese]], [[Hisham Sati]], _Flux Compactifications on Projective Spaces and The S-Duality Puzzle_, Adv.Theor.Math.Phys. 10 (2006) 345-394 ([arXiv:hep-th/0501110](http://arxiv.org/abs/hep-th/0501110))

Discussion of [[Montonen-Olive duality]] in [[D=4 super Yang-Mills theory]] via [[ABJM-model]] as [[D3-brane]] model after [[double dimensional reduction]] followed by [[T-duality]]:

* [[Koji Hashimoto]], Ta-Sheng Tai, [[Seiji Terashima]], _Toward a Proof of Montonen-Olive Duality via Multiple M2-branes_, JHEP 0904:025, 2009 ([arxiv:0809.2137](https://arxiv.org/abs/0809.2137))

See also:


* Surya Raghavendran, Philsang Yoo, _Twisted S-Duality_ ([arxiv:1910.13653](https://arxiv.org/abs/1910.13653))

### In heterotic string theory

In [[heterotic supergravity]] with [[higher curvature corrections]]:

* [[Mohammad R. Garousi]]: *S-duality in higher-derivative corrections of heterotic supergravity* &lbrack;[arXiv:2502.00357](https://arxiv.org/abs/2502.00357)&rbrack;



### Relation to geometric Langlands duality

The relation of S-duality to [[geometric Langlands duality]] was understood in

* {#KapustinWitten06} [[Anton Kapustin]], [[Edward Witten]], _Electric-Magnetic Duality And The Geometric Langlands Program_ , Communications in number theory and physics, Volume 1, Number 1, 1&#8211;236 (2007) ([arXiv:hep-th/0604151](http://arxiv.org/abs/hep-th/0604151))

Exposition:

* [[Edward Frenkel]],  _What Do Fermat's Last Theorem and Electro-magnetic Duality Have in Common?_ KITP talk 2011 ([web](http://online.kitp.ucsb.edu/online/bblunch/frenkel/))

[[!redirects S-dualities]]

[[!redirects Montonen-Olive duality]]

[[!redirects complexified coupling constant]]
