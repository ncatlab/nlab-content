
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



\tableofcontents


## Idea

[[supergravity]] in [[dimension]] 5. 

For $N = 1$ this arises from [[11-dimensional supergravity]] by [[KK-compactification]] on a [[Calabi-Yau manifold]] of complex dimension 3 (see at _[[M-theory on Calabi-Yau manifolds]]_), hence serves as the low-energy [[effective field theory]] of the strong-coupling version of Calabi-Yau compactifications of [[type IIA string theory]] (see [[supersymmetry and Calabi-Yau manifolds]])

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

The theory has a 2-form [[flux density]] $F_2$, locally $F_2 = d A$, with a [[5d Chern-Simons theory]] [[action functional]] locally of the form $\propto \int_X F_2 \wedge F_2 \wedge A$ ([Cremmer 1981, p. 276](#Cremmer81), [Chamseddine & Nicolai 1980 (4)](#ChamseddineNicolai80),  cf. [Castellani-D'Auria-Fre (III.5.70)](#CastellaniDAuriaFre), [Gauntlet, Myers & Townsend  1998, p. 3](#GauntlettMyersTownsend98), [GGHPR 02 (2.1)](#GGHPR02), [Bonetti-Grimm-Hohenegger 13](#BonettiGrimmHohenegger13)). 

Hence the [[bosonic field]] sector of $D=5$ supergravity is [[Einstein-Maxwell theory|Einstein]]-[[Maxwell-Chern-Simons theory|Maxwell]]-[[D=5 Chern-Simons theory|Chern-Simons theory]] in 5D, where the [[equation of motion]] for the [[flux density]] is of the non-linear form

$$
  \mathrm{d} F_3 
    \;=\; 
  F_2 \wedge F_2
  \mathrlap{\,,}
$$

with $F_3 \coloneqq \star F_2$ the [[Hodge dual]] of $F_2$ (cf. [GGHPR 02 (2.2)](#GGHPR02)).

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

(the other Fierz identity (III.5.50a) gives the  cocycle for the [[membrane]] ([[super 2-brane in 5d]]) $\mu_{membrane,5d} \coloneqq \frac{i}{2}\overline{\psi}_A \Gamma_{a b}  \psi \wedge e^a \wedge e^b$, $d \mu_{membrane,5d} = 0$, that appears already in the old [[brane scan]]. )

This is a lower dimensional analogue to the situation for the [[C-field]] $G_4$ (locally $G_4 = d C$) in [[11-dimensional supergravity]], which has a Chern-Simons term locally of the form $\propto \int G_4 \wedge G_4 \wedge C$ and hence the equation of motion

$$
  d G_7 
  \;=\; 
  -\tfrac{1}{2}G_4 \wedge G_4
$$

with $G_7 = \star G_4$.




### Black holes and black (st)rings

The first [[black ring]] solution in 5d sugra was found in ([Elvang-Emparan-Mateos-Reall 04](#ElvangEmparanMateosReall04), [Elvang-Emparan-Mateos-Reall 05](#ElvangEmparanMateosReall05)).

Supersymmetric black holes exist precisely only in dimensions 4 and 5 ([Gauntlett-Myers-Townsend 98](#GauntlettMyersTownsend98)). These play a key role in the discussion of [[black holes in string theory]].

(There are supersymmetric particle-like solutions of $d \gt 5$ supergravity theories that are sometimes called black holes, but these are always singular. There are also supersymmetric black holes in $d = 3$, but
the spacetime in that case is asymptotically [[anti-de Sitter spacetime]] rather than asymptotically flat. Of course, there are non-singular supersymmetric [[black brane]] solutions in various $d \geq 4$ supergravity theories but these are neither 'particle-like' nor, strictly speaking,
asymptotically flat.)

### Relation to 11D supergravity
 {#ViaCYCompactificationOf11dSupergravity}


[[!include analogy between 11D and 5D SuGra -- table]]

Discussion of 5d supergravity as a [[KK-compactification]] of [[11-dimensional supergravity]] on a [[Calabi-Yau manifold]] of complex dimension 3 ([[M-theory on Calabi-Yau manifolds]]):  [Hull & Townsend 1995 p.30-31](#HullTownsend95), [Cadavid, Ceresole, D'Auria & Ferrara 1995](#CadavidCeresoleDAuriaFerrara95) [Ferrara, Khuria & Minasian 1996](#FerraraKhuriaMinasian96), [Ferrara, Minasian & Sagnotti 1996](#FerraraMinasianSagnotti96)). 


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

* [[supergravity]]

  * [[D=2 supergravity]]

  * [[D=3 supergravity]]

  * [[D=4 supergravity]]

  * **D=5 supergravity**

    * [[D=5 Chern-Simons theory]]

    * [[Maxwell-Chern-Simons theory]]

    * [[super 2-brane in 5d]]

  * [[D=6 supergravity]]

  * [[D=7 supergravity]]

  * [[D=8 supergravity]]

  * [[D=9 supergravity]]

  * [[D=10 supergravity]]

  * [[D=11 supergravity]]

    * [[D=11 N=1 supergravity]]

* [[D=5 gravity]]

* [[D=5 Chern-Simons theory]]

* 10-dimensional [[type II supergravity]], [[heterotic supergravity]]



## References

### General

Original discussion:

* {#ChamseddineNicolai80} [[Ali Chamseddine]], [[Hermann Nicolai]]: *Coupling the $SO(2)$ Supergravity Through Dimensional Reduction*, Physics Letters B **96** 1–2 (1980) 89-93 \[<a href="https://doi.org/10.1016/0370-2693(80)90218-X">doi:10.1016/0370-2693(80)90218-X</a>, [[ChamseddineNicolai-SU2SuGra.pdf:file]]\]

  Corrigendum: Phys. Lett. B **785** (2018) 631-632 &lbrack;[arXiv:1808.08955](https://arxiv.org/abs/1808.08955), [doi:10.1016/j.physletb.2018.05.029](https://doi.org/10.1016/j.physletb.2018.05.029)&rbrack;


* {#Cremmer81} [[Eugène Cremmer]]: *Supergravities in 5 Dimensions*, in [[Stephen Hawking]], [[Martin Roček]] (eds.): *Superspace and Supergravity*, Proceedings of Nuffield Workshop 1980, Cambridge University Press (1981) 267-282 &lbrack;[[Cremmer-SuGraIn5D.pdf:file]], [ISBN:9780521239080](https://www.cambridge.org/de/universitypress/subjects/physics/cosmology-relativity-and-gravitation/superspace-and-supergravity-proceedings-nuffield-workshop-cambridge?format=HB&isbn=9780521239080), [inSpire:172773](https://inspirehep.net/literature/172773), [cds:100081](https://cds.cern.ch/record/100081)&rbrack;


* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], chapter III.5 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991) &lbrack;ch III.5: [[CastellaniDAuriaFre-ChIII5.pdf:file]]&rbrack;
  > (via [[D'Auria-Fré formulation of supergravity]])


Further discussion:

* [[William Linch III]], Markus A. Luty, J. Phillips, _Five dimensional supergravity in $N = 1$ superspace_, Phys. Rev. D **68** (2003) 025008 &lbrack;[arXiv:hep-th/0209060](https://arxiv.org/abs/hep-th/0209060)&rbrack;

* {#GGHPR02} [[Jerome Gauntlett]], [[Jan Gutowski]], [[Christopher Hull]], Stathis Pakis, [[Harvey Reall]], _All supersymmetric solutions of minimal supergravity in five dimensions_, Class. Quant. Grav. **20** (2003) 4587-4634 &lbrack;[arXiv:hep-th/0209114](http://arxiv.org/abs/hep-th/0209114), [doi:10.1088/0264-9381/20/21/005](https://doi.org/10.1088/0264-9381/20/21/005)&rbrack;

* Sorin Cucu, _From M-theory to $D=5$ supergravity and duality-symmetric theories_ &lbrack;[arXiv:hep-th/0310105](http://arxiv.org/abs/hep-th/0310105)&rbrack;

* [[Eric Bergshoeff]], Sorin Cucu, Tim de Wit, Jos Gheerardyn, Stefan Vandoren, [[Antoine Van Proeyen]], _$N=2$ supergravity in five dimensions revisited_ &lbrack;[arXiv:hep-th/0403045](http://arxiv.org/abs/hep-th/0403045)&rbrack;

* Gerard Clement: *The symmetries of five-dimensional minimal supergravity reduced to three dimensions*, J. Math. Phys. **49** (2008) 042503 &lbrack;[arXiv:0710.1192](https://arxiv.org/abs/0710.1192), [doi:10.1063/1.2907863](https://doi.org/10.1063/1.2907863)&rbrack; Erratum-ibid. **49** (2008) 079901 &lbrack;[doi:10.1063/1.2963308](https://doi.org/10.1063/1.2963308)&rbrack;


* [[Katrin Becker]], [[Melanie Becker]], [[Daniel Butter]], [[William Linch III]], Stephen Randall: *Five-dimensional Supergravity in $N = 1/2$ Superspace*, J. High Energ. Phys. **2020** 98 (2020) &lbrack;[arXiv:1909.09208](https://arxiv.org/abs/1909.09208), <a href="https://doi.org/10.1007/JHEP03(2020)098">doi:10.1007/JHEP03(2020)098</a>&rbrack;

* Edoardo Lauria, [[Antoine Van Proeyen]], _$\mathcal{N}=2$ Supergravity in $D=4,5,6$ Dimensions_ &lbrack;[arXiv:2004.11433](https://arxiv.org/abs/2004.11433)&rbrack;

Construction of 5d [[gauged supergravity]] via [[D'Auria-Fré formulation of supergravity]]:

* {#ACFG01} [[Laura Andrianopoli]], Francesco Cordaro, [[Pietro Fré]], Leonardo Gualtieri, _Non-Semisimple Gaugings of $D=5$ $\mathcal{N}=8$ Supergravity and FDA.s_, Class. Quant. Grav. **18** (2001) 395-414 &lbrack;[arXiv:hep-th/0009048](http://arxiv.org/abs/hep-th/0009048), [doi:10.1088/0264-9381/18/3/303](https://doi.org/10.1088/0264-9381/18/3/303)&rbrack;

* [[Laura Andrianopoli]], Francesco Cordaro, [[Pietro Fré]], _Non-Semisimple Gaugings of $D=5$ $\mathcal{N}=8$ Supergravity_, Fortsch.Phys. **49** (2001) 511-518 &lbrack;[arXiv:hep-th/0012203](http://arxiv.org/abs/hep-th/0012203)&rbrack;


See also:

* [[Sheldon Katz]], Hee-Cheol Kim, Houri-Christina Tarazi, [[Cumrun Vafa]]: *Swampland Constraints on $5d$ $\mathcal{N}=1$ Supergravity &lbrack;[arXiv:2004.14401](https://arxiv.org/abs/2004.14401)&rbrack;

* Andrew Beckett, [[José Figueroa-O'Farrill]]: *Killing superalgebras for lorentzian five-manifolds* &lbrack;[arxiv:2105.05775](https://arxiv.org/abs/2105.05775)&rbrack;

* Soumya Adhikari, Bindusar Sahoo: *$\mathcal{N}=2$ conformal supergravity in five dimensions* &lbrack;[arXiv:2312.01879](https://arxiv.org/abs/2312.01879)&rbrack;

* Edoardo Colombo, Vasil Dimitrov, Dario Martelli, Alberto Zaffaroni: *Patch-wise localization with Chern-Simons forms in five dimensional supergravity* &lbrack;[arXiv:2511.13824](https://arxiv.org/abs/2511.13824)&rbrack;




[[!include 11D Sugra on CY3 -- references]]



Further reduction to [[D=3 supergravity]]:

* Gerard Clement: *The symmetries of five-dimensional minimal supergravity reduced to three dimensions*, J. Math. Phys. **49** (2008) 042503 &lbrack;[arXiv:0710.1192](https://arxiv.org/abs/0710.1192), [doi:10.1063/1.2907863](https://doi.org/10.1063/1.2907863)&rbrack;



### Via type II theory

Embedding into [[type II supergravity]]:

* Arnaud Baguet, [[Olaf Hohm]], [[Henning Samtleben]], _Consistent Type IIB Reductions to Maximal 5D Supergravity_ &lbrack;[arXiv:1506.01385](https://arxiv.org/abs/1506.01385)&rbrack;

* Christopher Couzens, Niall T. Macpherson, Achilleas Passias: *A plethora of Type IIA embeddings for   minimal supergravity*,  J. High Energ. Phys. **2023** 47 (2023) &lbrack;[arXiv:2209.15540](https://arxiv.org/abs/2209.15540), <a href="https://doi.org/10.1007/JHEP01(2023)047">doi:10.1007/JHEP01(2023)047</a>&rbrack;


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


### Black hole and black (st)ring solutions
 {#ReferencesBlackHolesAndBlackStrings}

Discussion of lifts of 4d [[black holes]] to 5d black holes and [[black rings]], and embedding as [[black holes in string theory]]:

* {#GauntlettMyersTownsend98} [[Jerome Gauntlett]], [[Robert C. Myers]], [[Paul Townsend]], *Black Holes of $D=5$ Supergravity*, Class.Quant.Grav. **16** (1999) 1-21 &lbrack;[arXiv:hep-th/9810204](http://arxiv.org/abs/hep-th/9810204), [doi:10.1088/0264-9381/16/1/001](https://doi.org/10.1088/0264-9381/16/1/001)&rbrack;

* {#ElvangEmparanMateosReall04} [[Henriette Elvang]], [[Roberto Emparan]], [[David Mateos]], [[Harvey Reall]], _A supersymmetric black ring_, Phys. Rev. Lett. **93** 211302 (2004) ([arXiv:hep-th/0407065](http://arxiv.org/abs/hep-th/0407065))

* {#ElvangEmparanMateosReall05} [[Henriette Elvang]], [[Roberto Emparan]], [[David Mateos]], [[Harvey Reall]], _Supersymmetric 4D Rotating Black Holes from 5D Black Rings_, JHEP0508:042 (2005) &lbrack;[arXiv:hep-th/0504125](http://arxiv.org/abs/hep-th/0504125)&rbrack;

* [[Iosif Bena]], [[Per Kraus]], _Microscopic description of black rings in AdS/CFT_ JHEP 12 (2004) 070 ([hep-th/0408186](http://arxiv.org/abs/hep-th/0408186))

* [[Iosif Bena]], [[Per Kraus]], _Microstates of the D1-D5-KK system_ Phys. Rev. D72 (2005) 025007 ([hep-th/0503053](http://arxiv.org/abs/hep-th/0503053))

* Jutta Kunz, Francisco Navarro-Lerida: *$D=5$ Einstein-Maxwell-Chern-Simons Black Holes*, Phys. Rev. Lett. **96** (2006) 081101 &lbrack;[arXiv;hep-th/0510250](https://arxiv.org/abs/hep-th/0510250), [doi:10.1103/PhysRevLett.96.081101](https://doi.org/10.1103/PhysRevLett.96.081101)&rbrack;

* [[Davide Gaiotto]], [[Andrew Strominger]], [[Xi Yin]], _5D black rings and 4D black holes_ JHEP 02 (2006) 023 ([hep-th/0504126](http://arxiv.org/abs/hep-th/0504126))

* [[Davide Gaiotto]], [[Andrew Strominger]], [[Xi Yin]], _New connections between 4D and 5D black holes_, JHEP 02 (2006) 024 ([hep-th/0503217](https://arxiv.org/abs/hep-th/0503217))

* Alejandra Castro, Joshua L. Davis, [[Per Kraus]], Finn Larsen, _String Theory Effects on Five-Dimensional Black Hole Physics_, International Journal of Modern Physics A **23** 05, (2008) 613-691 &lbrack;[arXiv:0801.1863](http://arxiv.org/abs/0801.1863), [doi:10.1142/S0217751X08039724](https://doi.org/10.1142/S0217751X08039724)&rbrack;

* Pierre Heidmann, Paolo Pani, [[Jorge E. Santos]]: *Asymptotically Flat Rotating Topological Stars* &lbrack;[arXiv:2510.05200](https://arxiv.org/abs/2510.05200)&rbrack;



Review:

* [[Per Kraus]]: _Stringy black holes in five dimensions_ (2007) &lbrack;[[Kraus-Stringy5dBH.pdf:file]]&rbrack;

* Hari K. Kunduri, James Lucietti: *[Five dimensional Einstein–Maxwell–Chern–Simons theory](https://www.emis.de/journals/LRG/Articles/lrr-2013-8/articlese6.html#x9-360006.3)*, section 6.3 in: *[Classification of Near-Horizon Geometries of Extremal Black Holes](https://www.emis.de/journals/LRG/Articles/lrr-2013-8/title.html)*, Living Rev. Relativity, **16** 8 (2013) &lbrack;[doi:10.12942/lrr-2013-8](https://doi.org/10.12942/lrr-2013-8)&rbrack;


Further [[defect branes]]:

* Eun Kyung Park, Pyung Seong Kwon, *NS-branes in 5d brane world models*, Phys. Rev. D82:046001, 2010 ([arXiv:1007.1290](https://arxiv.org/abs/1007.1290), [doi:10.1103/PhysRevD.82.046001](https://doi.org/10.1103/PhysRevD.82.046001))

* Minkyu Park, [[Masaki Shigemori]], _Codimension-2 Solutions in Five-Dimensional Supergravity_, JHEP 1510 (2015) 011 ([arXiv:1505.05169](http://arxiv.org/abs/1505.05169))

* [[Masaki Shigemori]], *Interpolating between multi-center microstate geometries*, JHEP 09 (2021) 010 ([arXiv:2105.11639](https://arxiv.org/abs/2105.11639))

See also:

* Alexandru Dima, Pierre Heidmann, Marco Melis, Paolo Pani, Gela Patashuri: *The Great Impersonation: $\mathcal{W}$-Solitons as Prototypical Black Hole Microstates* &lbrack;[arXiv:2509.18245](https://arxiv.org/abs/2509.18245)&rbrack;

On [[black strings]] in [[D=5 gravity]]/[[D=5 supergravity]] from [[M5-branes]] [[wrapped brane|wrapped]] on [[4-manifolds]]:

* [[David Kastor]], Section 3 of: _From wrapped M-branes to Calabi-Yau black holes and strings_, JHEP 0307 (2003) 040 &lbrack;[arXiv:hep-th/0305261](https://arxiv.org/abs/hep-th/0305261)&rbrack;

On [[anti de Sitter spacetime|AdS]] [[near horizon geometry]] of [[black holes]] and [[black strings]] in 5D supergravity:

* {#FujiiKemmokuMizoguchi99} Akira Fujii, Ryuji Kemmoku: *$D=5$ Simple Supergravity on $AdS_2 \times S^3$*, Phys. Lett. B **459** (1999) 137-144 &lbrack;[arXiv:hep-th/9903231](https://arxiv.org/abs/hep-th/9903231), [doi:10.1088/0264-9381/16/3/006](https://doi.org/10.1088/0264-9381/16/3/006)&rbrack;

* {#FujiiKemmokuMizoguchi00} Akira Fujii, Ryuji Kemmoku, [[Shun'ya Mizoguchi]]: *$D=5$ Simple Supergravity on $AdS_{3} \times S^{2}$ and $N=4$ Superconformal Field Theory*, Nucl. Phys. B **574** (2000) 691-718  &lbrack;[arXiv:hep-th/9811147](https://arxiv.org/abs/hep-th/9811147), <a href="https://doi.org/10.1016/S0550-3213(00)00018-3">doi:10.1016/S0550-3213(00)00018-3</a>&rbrack;




[[!redirects 5d supergravity]]
[[!redirects 5D supergravity]]
[[!redirects 5-dimensional supergravity]]




