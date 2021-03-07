[[!redirects 5-dimensional supergravity]]
[[!redirects 5-dimensional supergravity]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

[[supergravity]] in [[dimension]] 5. For $N = 1$ this arises from [[11-dimensional supergravity]] by [[KK-compactification]] on a [[Calabi-Yau manifold]] of complex dimension 3 (see at _[[M-theory on Calabi-Yau manifolds]]_), hence serves as the low-energy [[effective field theory]] of the strong-coupling version of Calabi-Yau compactifications of [[type IIA string theory]] (see [[supersymmetry and Calabi-Yau manifolds]])

$$
  \array{
    11d \; SuGra\; on\; S^1 \times Y_6 \times X_4
      &\longrightarrow&
    5d \; SuGra\; on\; S^1 \times X_4 && strong \; coupling
    \\
    \downarrow && \downarrow
    \\
    10d\; tpye \;IIA\; Sugra\; on \; Y_6 \times X_4
      &\longrightarrow&
    10d\; Sugra\; on \; X_4 && weak \; coupling    
  }
$$

## Properties

### 5d Chern-Simons term
 {#5dChernSimonsTerm}

This theory has a 2-form field strength $F_2$, locally $F_2 = d A$, with a [[5d Chern-Simons theory]] [[action functional]] locally of the form $\propto \int_X F_2 \wedge F_2 \wedge A$ (e.g. [Castellani-D'Auria-Fre (III.5.70)](#CastellaniDAuriaFre), [Gauntlet-Myers-Townsend  98, p. 3](#GauntlettMyersTownsend98), [GGHPR 02 (2.1)](#GGHPR02), [Bonetti-Grimm-Hohenegger 13](#BonettiGrimmHohenegger13)). Hence its [[equation of motion]] is of the non-linear form

$$
  d F_3 = F_2 \wedge F_2
$$

with $F_3 \coloneqq \star F_2$ the [[Hodge dual]] of $F_2$ ([GGHPR 02 (2.2)](#GGHPR02)).

This is reflected in the corresponding cochains on [[super Minkowski spacetime]]

$$
  \mu_{D0,5d} = \overline{\psi}_A \psi_A
  \phantom{AAA} 
  \mu_{string,5d} = \overline{\psi}_A\Gamma_a \psi_A  \wedge e^a
$$

satisfying

$$
  d \mu_{string,5d} = \mu_{D0,5d} \wedge \mu_{D0,5d}
  \,.
$$

due to the [[Fierz identity]] in [Castellani-D'Auria-Fré 91 (III.5.50a)](#CastellaniDAuriaFre), [this example](Fierz+identity#QuadraticFierzIdentitiesIn5d):

\begin{imagefromfile}
  "file_name": "FierzIdentitiesForBraneCocyclesIn5d.png",
  "width": 600
\end{imagefromfile}

(the other Fierz identity (III.5.50a) gives the [[membrane]] cocycle $\mu_{membrane,5d} \coloneqq \frac{i}{2}\overline{\psi}_A \Gamma_{a b}  \psi \wedge e^a \wedge e^b$, $d \mu_{membrane,5d} = 0$, that appears already in the old [[brane scan]]. )

This is a lower dimensional analogue to the situation for the [[C-field]] $G_4$ (locally $G_4 = d C$) in [[11-dimensional supergravity]], which has a Chern-Simons term locally of the form $\propto \int G_4 \wedge G_4 \wedge C$ and hence the equation of motion

$$
  d G_7 
  \;=\; 
  -\tfrac{1}{2}G_4 \wedge G_4
$$

with $G_7 = \star G_4$.




### Black holes and black rings

The first [[black ring]] solution in 5d sugra was found in ([Elvang-Emparan-Mateos-Reall 04](#ElvangEmparanMateosReall04), [Elvang-Emparan-Mateos-Reall 05](#ElvangEmparanMateosReall05)).

Supersymmetric black holes exist precisely only in dimensions 4 and 5 ([Gauntlett-Myers-Townsend 98](#GauntlettMyersTownsend98)). These play a key role in the discussion of [[black holes in string theory]].

(There are supersymmetric particle-like solutions of $d \gt 5$ supergravity theories that are sometimes called black holes, but these are always singular. There are also supersymmetric black holes in $d = 3$, but
the spacetime in that case is asymptotically [[anti-de Sitter spacetime]] rather than asymptotically flat. Of course, there are non-singular supersymmetric [[black brane]] solutions in various $d \geq 4$ supergravity theories but these are neither 'particle-like' nor, strictly speaking,
asymptotically flat.)

### Via Calabi-Yau compactification of 11d supergravity
 {#ViaCYCompactificationOf11dSupergravity}

Discussion of 5d supegravity as a [[KK-compactification]] of [[11-dimensional supergravity]] on a [[Calabi-Yau manifold]] of complex dimension 3 ([[M-theory on Calabi-Yau manifolds]]) is discussed in

([Hull-Townsend 95, p.30-31](#HullTownsend95), [Cadavid-Ceresole-D'Auria-Ferrara 95](#CadavidCeresoleDAuriaFerrara95) [Ferrara-Khuria-Minasian 96](#FerraraKhuriaMinasian96), [Ferrara-Minasian-Sagnotti 96](#FerraraMinasianSagnotti96)). See also ([Mizoguchi-Ohta 98](#MizoguchiOhta98)).


### U-duality

[[!include U-duality -- table]]


### $N = 2$ supersymmetry

Consider super Lie algebra cocoycles on $N =2$ 5d [[super-Minkowski spacetime]] (as in the [[brane scan]]).

With the notation as used at _[super Minkowski spacetime -- Canonical coordinates](super%20Minkowski%20spacetime#CanonicalCoordinates)_, there are now two copies of spinor-valued 1-forms, denoted $\psi_1$ and $\psi_2$. We use indices of the form $A,B, \cdots$ for these. Then the non-trivial bit of the [[Chevalley-Eilenberg algebra]] differential for $N = 2$, $d = 5$ [[super Minkowski spacetime]] is

$$
  d_{CE} e^a = - \tfrac{i}{2} \overline{\psi}_A \wedge \Gamma^a \psi_A
$$

where summation over repeated indices is understood.


There is a [[Fierz identity]]

$$
  \overline{\psi}_A \wedge \psi_A \wedge \overline{\psi}_B \wedge \psi_B
  \;=\;
  \overline{\psi}_A \wedge \Gamma_a \psi_A
  \wedge \overline{\psi}_B \wedge \Gamma^a \psi_B
  \,.
$$

([Castellani-D'Auria-Fr&#233; (III.5.50a)](#CastellaniDAuriaFre))

This implies that

$$
  d_{CE} (\overline{\psi}_A \Gamma^a \psi_A \wedge e_a)
  \;\propto\;
  (\overline{\psi}_A \wedge \Gamma^a \psi_A)
    \wedge
  (\overline{\psi}_B \wedge \Gamma^a \psi_B)
  \,.
$$

There is a 4-cocycle of the form

$$
  \mu_2 
    =
  \epsilon^{A B} \overline{\psi}_A \wedge \Gamma^{a b} \psi_B 
  \wedge e_a \wedge e_b
  \,.
$$

([Castellani-D'Auria-Fr&#233; (III.5.50b), (III.5.53c)](#CastellaniDAuriaFre))


## Related concepts

* [[D=5 gravity]]

* [[D=5 Chern-Simons theory]]

* [[11-dimensional supergravity]] 

* 10-dimensional [[type II supergravity]], [[heterotic supergravity]]

* [[7-dimensional supergravity]]

* **5-dimensional supergravity**

* [[4-dimensional supergravity]]

* [[3-dimensional supergravity]]

## References

Construction of 5d [[gauged supergravity]] via [[D'Auria-Fré formulation of supergravity]] is in 

* {#ACFG01} Laura Andrianopoli, Francesco Cordaro, [[Pietro Fré]], Leonardo Gualtieri, _Non-Semisimple Gaugings of D=5 N=8 Supergravity and FDA.s_, Class.Quant.Grav. 18 (2001) 395-414 ([arXiv:hep-th/0009048](http://arxiv.org/abs/hep-th/0009048))

surveyed in

* Laura Andrianopoli, Francesco Cordaro, [[Pietro Fré]], _Non-Semisimple Gaugings of D=5 N=8 Supergravity_, Fortsch.Phys.49:511-518,2001 ([arXiv:hep-th/0012203](http://arxiv.org/abs/hep-th/0012203))

### General

General discussion includes

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], chapter III.5 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

  (in [[D'Auria-Fre formulation of supergravity]])

* [[William Linch III]], Markus A. Luty, J. Phillips, _Five dimensional supergravity in $N = 1$ superspace_, Phys.Rev.D68:025008,2003 ([arXiv:hep-th/0209060](https://arxiv.org/abs/hep-th/0209060))

* {#GGHPR02} [[Jerome Gauntlett]], [[Jan Gutowski]], [[Christopher Hull]], Stathis Pakis, [[Harvey Reall]], _All supersymmetric solutions of minimal supergravity in five dimensions_, Class.Quant.Grav. 20 (2003) 4587-4634 ([arXiv:hep-th/0209114](http://arxiv.org/abs/hep-th/0209114))

* Sorin Cucu, _From M-theory to D=5 supergravity and duality-symmetric theories_ ([arXiv:hep-th/0310105](http://arxiv.org/abs/hep-th/0310105))

* [[Eric Bergshoeff]], Sorin Cucu, Tim de Wit, Jos Gheerardyn, Stefan Vandoren, [[Antoine Van Proeyen]], _$N=2$ supergravity in five dimensions revisited_ ([arXiv:hep-th/0403045](http://arxiv.org/abs/hep-th/0403045))

* [[Katrin Becker]], [[Melanie Becker]], Daniel Butter, [[William Linch III]], Stephen Randall, _Five-dimensional Supergravity in N = 1/2 Superspace_ ([arXiv:1909.09208](https://arxiv.org/abs/1909.09208))

* Edoardo Lauria, [[Antoine Van Proeyen]], _$\mathcal{N}=2$ Supergravity in $D=4,5,6$ Dimensions_ ([arXiv:2004.11433](https://arxiv.org/abs/2004.11433))


### Via M-theory on Calabi-Yau 3-folds

Discussion via [[KK-compactification]] as [[M-theory on Calabi-Yau manifolds]] includes

* {#HullTownsend95} [[Chris Hull]], [[Paul Townsend]], pages 30 and 31 of _Unity of Superstring Dualities_, Nucl.Phys.B438:109-137,1995 ([arXiv:hep-th/9410167](https://arxiv.org/abs/hep-th/9410167))

* {CadavidCeresoleDAuriaFerrara95} A.C. Cadavid, A. Ceresole, [[Riccardo D'Auria]], [[Sergio Ferrara]], _11-Dimensional Supergravity Compactified on Calabi-Yau Threefolds_ ([arXiv:hep-th/9506144](https://arxiv.org/abs/hep-th/9506144))

* {#FerraraKhuriaMinasian96} [[Sergio Ferrara]], Ramzi R. Khuria,  [[Ruben Minasian]], _M-theory on a Calabi-Yau manifold_, Phys.Lett.B375:81-88,1996 ([arXiv:hep-th/9602102](https://arxiv.org/abs/hep-th/9602102))

* {#FerraraMinasianSagnotti96} [[Sergio Ferrara]], [[Ruben Minasian]], [[Augusto Sagnotti]], _Low-Energy Analysis of M and F Theories on Calabi-Yau Threefolds_, Nucl.Phys. B474 (1996) 323-342 ([arXiv:hep-th/9604097](https://arxiv.org/abs/hep-th/9604097))

* {#MizoguchiOhta98} S. Mizoguchi, N. Ohta, _More on the Similarity between $D=5$ Simple Supergravity and M Theory_, Phys.Lett. B441 (1998) 123-132 ([arXiv:hep-th/9807111](https://arxiv.org/abs/hep-th/9807111))


Further discussion of the [[5d Chern-Simons theory|5d Chern-Simons term]] includes

* {#BonettiGrimmHohenegger13} Federico Bonetti, [[Thomas Grimm]], [[Stefan Hohenegger]], _One-loop Chern-Simons terms in five dimensions_ ([arXiv:1302.2918](http://arxiv.org/abs/1302.2918)) 

(one-loop corrections).

### Via type IIB theory

* Arnaud Baguet, [[Olaf Hohm]], [[Henning Samtleben]], _Consistent Type IIB Reductions to Maximal 5D Supergravity_ ([arXiv:1506.01385](https://arxiv.org/abs/1506.01385))

### Gauged sugra
 {#ReferencesGauged}

The maximal 5d [[gauged supergravity]] was first constructed in 

*  M. Pernici, K. Pilch, [[Peter van Nieuwenhuizen]], _Gauged $N=8$ $D=5$ Supergravity_, Nucl.Phys. B259 (1985) 460 ([spire](https://inspirehep.net/record/16067?ln=en))

* [[Murat Günaydin]], [[L. J. Romans]] and [[Nicholas Warner]], _Gauged $N = 8$ Supergravity in Five Dimensions_, Phys. Lett. 154B, (1985) 268 ([spire:207663](http://inspirehep.net/record/207663), <a href="https://doi.org/10.1016/0370-2693(85)90361-2">doi:10.1016/0370-2693(85)90361-2</a>)

* [[Murat Günaydin]], [[L. J. Romans]] and [[Nicholas Warner]], _Compact and Non&#8211;Compact Gauged Supergravity Theories in Five Dimensions_, Nucl. Phys. B272 (1986) 598 ([spire:219727](http://inspirehep.net/record/219727), <a href="https://doi.org/10.1016/0550-3213(86)90237-3">doi:10.1016/0550-3213(86)90237-3</a>)

See ([ACFG 01](#ACFG01)).

* [[Murat Gunaydin]], Marco Zagermann, _The Gauging of Five-dimensional, $N=2$ Maxwell-Einstein Supergravity Theories coupled to Tensor Multiplets_,  	Nucl.Phys.B572:131-150,2000 ([arXiv:hep-th/9912027](https://arxiv.org/abs/hep-th/9912027))

* [[Murat Gunaydin]], Marco Zagermann, _The Vacua of 5d, $N=2$ Gauged Yang-Mills/Einstein/Tensor Supergravity: Abelian Case_, Phys.Rev.D62:044028,2000 ([arXiv:hep-th/0002228](http://arxiv.org/abs/hep-th/0002228))

* A. Ceresole, [[Gianguido Dall'Agata]], _General matter coupled $N=2$, $D=5$ gauged supergravity_, Nucl.Phys. B585 (2000) 143-170 ([arXiv:hep-th/0004111](http://arxiv.org/abs/hep-th/0004111))

* [[John Ellis]], [[Murat Gunaydin]], Marco Zagermann, _Options for Gauge Groups in Five-Dimensional Supergravity_, JHEP 0111:024,2001 ([arXiv:hep-th/0108094](http://arxiv.org/abs/hep-th/0108094))


### Horava-Witten compactification
 {#ReferencesHWCompactification}

Discussion of [[KK-compactification]] on $S^1/(\mathbb{Z}/2)$-orbifolds (the version of [[Horava-Witten theory]] after dimensional reduction) is discussed in

* Filipe Paccetti Correia, Michael G. Schmidt, Zurab Tavartkiladze, _4D Superfield Reduction of 5D Orbifold SUGRA and Heterotic M-theory_ ([arXiv:hep-th/0602173](https://arxiv.org/abs/hep-th/0602173))

### Black hole solutions

Discussion of lifts of 4d black holes to 5d black holes and [[black rings]] and embedding as [[black holes in string theory]] includes

* {#GauntlettMyersTownsend98} [[Jerome Gauntlett]], R.C. Myers, [[Paul Townsend]], _Black Holes of D=5 Supergravity_, Class.Quant.Grav.16:1-21,1999 ([arXiv:hep-th/9810204](http://arxiv.org/abs/hep-th/9810204))

* {#ElvangEmparanMateosReall04} [[Henriette Elvang]], [[Roberto Emparan]], [[David Mateos]], [[Harvey Reall]], _A supersymmetric black ring_, Phys. Rev. Lett. 93:211302,2004 ([arXiv:hep-th/0407065](http://arxiv.org/abs/hep-th/0407065))

* {#ElvangEmparanMateosReall05} [[Henriette Elvang]], [[Roberto Emparan]], [[David Mateos]], [[Harvey Reall]], _Supersymmetric 4D Rotating Black Holes from 5D Black Rings_, JHEP0508:042,2005 ([arXiv:hep-th/0504125](http://arxiv.org/abs/hep-th/0504125))


* [[Iosif Bena]], [[Per Kraus]], _Microscopic description of black rings in AdS/CFT_ JHEP 12 (2004) 070 ([hep-th/0408186](http://arxiv.org/abs/hep-th/0408186))

* [[Iosif Bena]], [[Per Kraus]], _Microstates of the D1-D5-KK system_ Phys. Rev. D72 (2005) 025007 ([hep-th/0503053](http://arxiv.org/abs/hep-th/0503053))

* [[Davide Gaiotto]], [[Andrew Strominger]], [[Xi Yin]], _5D black rings and 4D black holes_ JHEP 02 (2006) 023 ([hep-th/0504126](http://arxiv.org/abs/hep-th/0504126))

* [[Davide Gaiotto]], [[Andrew Strominger]], [[Xi Yin]], _New connections between 4D and 5D black holes_, JHEP 02 (2006) 024 ([hep-th/0503217](https://arxiv.org/abs/hep-th/0503217))

* Alejandra Castro, Joshua L. Davis, [[Per Kraus]], Finn Larsen, _String Theory Effects on Five-Dimensional Black Hole Physics_ ([arXiv:0801.1863](http://arxiv.org/abs/0801.1863))

* Minkyu Park, Masaki Shigemori, _Codimension-2 Solutions in Five-Dimensional Supergravity_, JHEP 1510 (2015) 011 ([arXiv:1505.05169](http://arxiv.org/abs/1505.05169))

Review includes

* [[Per Kraus]], _Lectures on black holes and the $AdS_3$/$CFT_2$ correspondence_ ([arXiv:hep-th/0609074](http://arxiv.org/abs/hep-th/0609074))

  _Stringy black holes in five dimensions_, 2007 ([pdf slides](http://hep.ps.uci.edu/~arajaram/Irvine.07.pdf))

[[!redirects 5d supergravity]]