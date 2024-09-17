
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
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

U-duality is a kind of [[duality in string theory]].

The [[KK-compactifications]] of [[11-dimensional supergravity]] to lower dimensional [[gauged supergravity]] theories have global/local [[gauge groups]] given by [[split real forms]] of the $E$-series of the [[exceptional Lie groups]].

Here the [[compact space|compact]] [[exceptional Lie groups]] form a series [[E8]],[[E7]], [[E6]]

$$
  E_8, E_7, E_6
$$

which is usefully thought of to continue as

$$
  E_5 \coloneqq Spin(10), E_4 \coloneqq SU(5), E_3 \coloneqq SU(3) \times SU(2)
  \,.
$$

(Notice that $E_4$, $E_5$ and $E_6$ are also the traditional choices for [[phenomenology|phenomenologically]] realistic [[grand unified theories]], see there for more.)

The [[split real forms]] of this are traditionally written

$$
  E_{8(8)}, E_{7(7)}, E_{6(6)}
$$

and one sets

$$
  E_{5(5)} \coloneqq Spin(5,5), E_{4(4)} \coloneqq SL(5, \mathbb{R}), 
  E_{3(3)} \coloneqq SL(3, \mathbb{R}) \times SL(2, \mathbb{R})
  \,.
$$

For instance the [[scalar fields]] in the field [[supermultiplet]] of $3 \leq d \leq 11$-dimensional supergravity have [[moduli spaces]] parameterized by the [[homogeneous spaces]] 

$$
  E_{n(n)}/ K_n
$$

for 

$$
  n = 11 - d
  \,,
$$

where $K_n$ is the [[maximal compact subgroup]] of $E_{n(n)}$:

$$
  K_8 \simeq Spin(16), K_7 \simeq SU(8), K_6 \simeq Sp(4)
$$

$$
  K_5 \simeq Spin(5) \times Spin(5), 
  K_4 \simeq Spin(5),
  K_3 \simeq SU(2) \times SO(2)
  \,.
$$

Therefore $E_{n(n)}$ acts as a [[global symmetry]] on the supergravity fields and more generally certain [[subgroups]] of it are "gauged" (have [[gauge fields]]) in [[gauged supergravity]] version.

So for instance maximal [[3d supergravity]] has global (and in fact also local, see there) gauge group given by (the [[split real form]] of) [[E8]].

This is no longer verbatim true for their [[UV-completion]] by the corresponding [[Kaluza-Klein mechanism|compactifications]] of [[string theory]] (e.g. [[type II string theory]] for [[type II supergravity]], etc.). Instead, on these a [[discrete group|discrete subgroup]]

$$
  E_{n(n)}(\mathbb{Z}) \hookrightarrow E_{n(n)}
$$

acts as global symmetry. This is called the **U-duality** group of the supergravity theory.

It has been argued that this pattern should continue in some way further to the remaining values $0 \leq d \lt 3$,
with "[[Kac-Moody groups]]" [[E9]], [[E10]], [[E11]] corresponding to the [[Kac-Moody algebras]]

$$
  \mathfrak{e}_9, \mathfrak{e}_10, \mathfrak{e}_{11}
  \,.
$$

Continuing in the other direction to $d = 10$ ($n = 1$) connects to the [[T-duality]] group $O(d,d,\mathbb{Z})$ of [[type II string theory]].

[[!include U-duality -- table]]


More generally, there is a "[[magic pyramid]]" of super-[[Einstein-Yang-Mills theories]]  and their U-duality groups.

## Properties

### Relation to T-duality and S-duality

U-duality may be understood as being the combination of [[T-duality]] for the compactification torus and [[S-duality]] of [[type IIB superstring theory]]. see ([West 12, section 17.5.4](#West12)).

## Related concepts

* [[embedding tensor]], [[tensor hierarchy]]

* [[exceptional field theory]]

* [[duality in string theory]]

  * [[T-duality]]

  * [[S-duality]]

  * **U-duality**

* [[M-theory on G₂-manifolds]]

* [[magic pyramid]]

* [[mysterious duality]]

## References
 {#References}

### General

The hidden [[E7]]-symmetry of the [[KK-compactification]] of [[11-dimensional supergravity]] on a 7-dimensional fiber to maximal $N = 8$ [[4d supergravity]] was first noticed in

* {#CremmerJulia78} [[Eugene Cremmer]], [[Bernard Julia]], _The $N = 8$ supergravity theory. I. The Lagrangian_, Phys. Lett. 80B (1978) 48

* {#CremmerJulia79} [[Eugene Cremmer]], [[Bernard Julia]], _The $SO(8)$ Supergravity_, Nucl. Phys. B 159 (1979) 141 ([spire](http://inspirehep.net/record/140465?ln=en)) 

and more generally in 

* [[Bernard de Wit]], [[Hermann Nicolai]], _D = 11 Supergravity With Local SU(8) Invariance_, Nucl. Phys. B 274, 363 (1986) ([spire](http://inspirehep.net/record/227409?ln=en)),  _Local SU(8) invariance in $d = 11$ supergravity_ ([spire](http://inspirehep.net/record/218601?ln=en))

The further U-duality groups for compactifications of 11d SuGra including [[E6]], [[E7]], [[E8]] were identified in

* [[Eugene Cremmer]], _Supergravities in 5 dimensions_, in Hawking, Rocek (eds.) _Superspace and Supergravity_, Cambridge University Press 1981

* [[Bernard Julia]], _Group Disintegrations_, in Hawking, Rocek (eds.) _Superspace and Supergravity_, Cambridge University Press 1981

Review:

* [Obers-Pioline 98, section 4.2](#ObersPioline98)

* [[Bernard de Wit]], [[Hermann Nicolai]]: *Hidden Symmetries, Central Charges and All That*, Class. Quant. Grav. **18** (2001) 3095-3112 &lbrack;[arXiv:hep-th/0011239](https://arxiv.org/abs/hep-th/0011239), [doi:10.1088/0264-9381/18/16/302](https://doi.org/10.1088/0264-9381/18/16/302)&rbrack;

* [[Pietro Fré]], Floriana Gargiulo, Ksenya Rulik, Mario Trigiante, _The general pattern of Kac Moody extensions in supergravity and the issue of cosmic billiards_, Nucl.Phys. B741 (2006) 42-82 &lbrack;[arXiv:hep-th/0507249](http://arxiv.org/abs/hep-th/0507249)&rbrack;



The concept and terminology of U-duality in string theory/M-theory originates in 

* {#HullTownsend94} [[Chris Hull]], [[Paul Townsend]], _Unity of Superstring Dualities_ Nucl.Phys.B438:109-137 (1995) ([arXiv:hep-th/9410167](http://arxiv.org/abs/hep-th/9410167))

A textbook account is in 

* {#West12} [[Peter West]], section 17.3 of _[[Introduction to Strings and Branes]]_, Cambridge University Press 2012

Systematization of U-duality via the relation between [[supersymmetry and division algebras]] and the [[Freudenthal magic square]] is due to

* {#BorstenDuffHughesNagy13} [[Leron Borsten]], [[Michael Duff]], [[Mia J. Hughes]], [[Silvia Nagy]], *A magic square from Yang-Mills squared*, Phys. Rev. Lett. **112** (2014) 131601  &lbrack;[arXiv:1301.4176](http://arxiv.org/abs/1301.4176)&rbrack;

* {#ABDHN} [[Alexandros Anastasiou]], [[Leron Borsten]], [[Michael Duff]], [[Mia J. Hughes]], [[Silvia Nagy]], *A magic pyramid of supergravities*, JHEP (2014) 178 &lbrack;[arXiv:1312.6523](http://arxiv.org/abs/1312.6523)&rbrack;


Quick surveys include

* [[Jacques Distler]], _Split real forms_ ([blog post](http://golem.ph.utexas.edu/~distler/blog/archives/001213.html)).

Reviews focusing on [[gauged supergravity]] and the non-discrete duality groups include

* {#Samtleben08} [[Henning Samtleben]], _Lectures on Gauged Supergravity and Flux Compactifications_ ([arXiv:0808.4076](http://arxiv.org/abs/0808.4076))

with slides in

* {#Samtleben07} [[Henning Samtleben]], _Gauged supergravity and U-duality_, 2007  ([pdf](http://www.desy.de/uni-th/stringth/ggfl/talks/Samtleben.pdf))

Reviews with more [[M-theory]] lore include

* {#ObersPioline98} [[Niels Obers]], [[Boris Pioline]], *U-duality and M-Theory*, Phys. Rept. **318** (1999) 113-225 &lbrack;[arXiv:hep-th/9809039](https://arxiv.org/abs/hep-th/9809039), <a href="https://doi.org/10.1016/S0370-1573(99)00004-6">doi:10.1016/S0370-1573(99)00004-6</a>&rbrack;


* Shun'ya Mizoguchi, Germar Schroeder, _On Discrete U-duality in M-theory_, Class.Quant.Grav. 17 (2000) 835-870 ([arXiv:hep-th/9909150](http://arxiv.org/abs/hep-th/9909150))

* {#Roest04} Diederik Roest, _M-theory and Gauged Supergravities_, Fortsch.Phys.53:119-230,2005 ([arXiv:hep-th/0408175](http://arxiv.org/abs/hep-th/0408175))



Discussion in line with the [[F-theory]] perspective on the $SL(2,\mathbb{Z})$-[[S-duality]] -- namely "[[F'-theory]]" -- is in 

* {#KumarVafa96} Alok Kumar, [[Cumrun Vafa]], _U-Manifolds_, Phys.Lett. B396 (1997) 85-90 ([arXiv:hep-th/9611007](http://arxiv.org/abs/hep-th/9611007))

Discussion of [[11-dimensional supergravity]] in a form that exhibits the higher U-duality groups already before [[KK-compactification]], via a kind of [[exceptional generalized geometry]],is in 

* {#HohmSamtleben13} [[Olaf Hohm]], [[Henning Samtleben]], _Exceptional Form of $D=11$ Supergravity_, Phys. Rev. Lett. 111, 231601 (2013) ([arXiv:1308.1673](http://arxiv.org/abs/1308.1673))

Review of [[U-duality]] and [[exceptional generalized geometry]]  in [[KK-compactification]] of [[D=11 supergravity]]:

* [[Henning Samtleben]], *11D Supergravity and Hidden Symmetries*, in *[[Handbook of Quantum Gravity]]*, Springer (2023) &lbrack;[arXiv:2303.12682](https://arxiv.org/abs/2303.12682)&rbrack;


On U-duality (and possibly [[mysterious duality]]) via [[Hypothesis H]] as [[automorphisms]] of [[iterated loop space|iterated]] ([[Sullivan model of loop space|rational]]) [[cyclic loop spaces]] of the ([[rational n-sphere|rational]]) [[4-sphere]]:

* [[Hisham Sati]], [[Alexander Voronov]], *Mysterious Triality and Rational Homotopy Theory*, Comm. Math. Phys. **400** (2023) 1915-1960 &lbrack;[arXiv:2111.14810](https://arxiv.org/abs/2111.14810), [doi:10.1007/s00220-023-04643-7](https://doi.org/10.1007/s00220-023-04643-7)&rbrack;

* [[Hisham Sati]], [[Alexander Voronov]], *Mysterious Triality and M-Theory* &lbrack;[arXiv:2212.13968](https://arxiv.org/abs/2212.13968)&rbrack;

* {#SatiVoronov24} [[Hisham Sati]], [[Alexander A. Voronov]]: *Mysterious Triality and the Exceptional Symmetry of Loop Spaces* &lbrack;[arXiv:2408.13337](https://arxiv.org/abs/2408.13337)&rbrack;


review in:

* {#Voronov21} [[Alexander Voronov]] (joint with [[Hisham Sati]]), *Mysterious Duality*, talk at Texas Tech 2021 ([abstract pdf](https://www.math.ttu.edu/~lhoang/PureMath/abstract-2021-03-15-Voronov.pdf) [[Voronov_MysteriousAbstract.pdf:file]], [slides pdf](https://www.math.ttu.edu/~lhoang/PureMath/Slides-2021-03-15-Voronov.pdf), [[Voronov_MysteriousSlides.pdf:file]])

* [[Alexander Voronov]]: *The $E_k$ symmetry of dimensional reductions of M-theory*, talk at *[M-Theory and Mathematics 2023](/nlab/show/M-Theory+and+Mathematics#2023)*, NYU Abu Dhabi (2023) &lbrack;[web](/nlab/show/M-Theory+and+Mathematics#Voronov2023)&rbrack;



### $n=3$

The case of $SL(3,\mathbb{Z}) \times SL(2,\mathbb{Z})$ in [[8d supergravity]] is discussed in 

* {#LiuMinasian97} [[James Liu]], [[Ruben Minasian]], _U-branes and $T^3$ fibrations_, Nucl.Phys. B510 (1998) 538-554 ([arXiv:hep-th/9707125](http://arxiv.org/abs/hep-th/9707125))

### $n=4$

The case of $SL(5,\mathbb{Z})$ in [[7d supergravity]] from [[M-theory]] is discussed in

* {#Rozali97} [[Moshe Rozali]], _Matrix Theory and U-Duality in Seven Dimensions_, Phys.Lett. B400 (1997) 260-264 ([arXiv:hep-th/9702136](http://arxiv.org/abs/hep-th/9702136))

### $n=7$


The $E_{7(7)}$-symmetry was first discussed in 

* [[Bernard de Wit]], [[Hermann Nicolai]], _$D = 11$ Supergravity With Local $SU(8)$ Invariance_, Nucl. Phys. B 274, 363 (1986)


### $n=8$


The case of $E_{8(8)}$ is discussed in

* [[Hermann Nicolai]], _$D = 11$ Supergravity with Local $SO(16)$ Invariance_ , Phys. Lett. B 187, 316 (1987).

* K. Koepsell, [[Hermann Nicolai]], [[Henning Samtleben]], _An exceptional geometry for $d = 11$
supergravity?_, Class. Quant. Grav. 17, 3689 (2000) ([arXiv:hep-th/0006034](http://arxiv.org/abs/hep-th/0006034)).


### $n=9$


The case of [[E9]] is discussed in

* {#EHKNT07} [[François Englert]], Laurent Houart, [[Axel Kleinschmidt]], [[Hermann Nicolai]], Nassiba Tabti, _An E9 multiplet of BPS states_, JHEP 0705:065,2007 ([arXiv:hep-th/0703285](http://arxiv.org/abs/hep-th/0703285))


### $n=10$
 {#Referencesn10}

The case of [[E10]] is discussed for [[boson|bosonic]] degrees of freedom in 

* [[Thibault Damour]], [[Marc Henneaux]], [[Hermann Nicolai]], _$E(10)$ and a 'small tension expansion' of M
theory_, Phys. Rev. Lett. 89, 221601 (2002) ([arXiv:hep-th/0207267](http://arxiv.org/abs/hep-th/0207267));

* [[Axel Kleinschmidt]], [[Hermann Nicolai]], _$E(10)$ and $SO(9,9)$ invariant supergravity_, JHEP 0407,
041 (2004) ([arXiv:hep-th/0407101](http://arxiv.org/abs/hep-th/0407101))

and for fermionic degrees of freedom in [[supergravity|supersymmetric]] [[quantum cosmology]] in 

* {#Damour14} [[Thibault Damour]], _Quantum supersymmetric Bianchi IX  Cosmology and its hidden Kac-Moody Structure_, talk at [Gravitation, Solitons and Symmetries](http://www.lestudium-ias.com/#!registration-conference-21-may-gibbons/ci2z) ([[DamourSQC14.pdf:file]])

Review includes

* {#Nicolai08} [[Hermann Nicolai]], _Wonders of $E_{10}$ and $K(E_{10})$_ (2008) ([pdf](http://ipht.cea.fr/Pisp/pierre.vanhove/Paris08/talk_PDF/nicolai.pdf))

* {#Nicolai14} [[Hermann Nicolai]], _On Exceptional Geometry and Supergravity_, talk at [Gravitation, Solitons and Symmetries](http://www.lestudium-ias.com/#!registration-conference-21-may-gibbons/ci2z) ([[NicolaiTalk14.pdf:file]])

Discussion of [[phenomenology]]:

* [[Axel Kleinschmidt]], [[Hermann Nicolai]], _Standard model fermions and $K(E_{10})$_ ([arXiv:1504.01586](https://arxiv.org/abs/1504.01586))

* {#MeissnerNicolai18a} Krzysztof A. Meissner, [[Hermann Nicolai]], _Standard Model Fermions and Infinite-Dimensional R-Symmetries_, Phys. Rev. Lett. 121, 091601 (2018) ([arXiv:1804.09606](https://arxiv.org/abs/1804.09606))

* {#MeissnerNicolai18b} Krzysztof A. Meissner, [[Hermann Nicolai]], _Planck Mass Charged Gravitino Dark Matter_, Phys. Rev. D 100, 035001 (2019) ([arXiv:1809.01441](https://arxiv.org/abs/1809.01441))




### $n=11$


The case of of [[E11]] is discussed in 

* [[Peter West]], _$E_{11}$ and M-theory_, Class. Quant. Grav. 18, 4443 (2001) ([arXiv:hep-th/0104081](http://arxiv.org/abs/hep-th/0104081)).

* {#West16} [[Peter West]], _A brief review of E theory_ ([arXiv:1609.06863](http://arxiv.org/abs/1609.06863))

### Further details

A careful discussion of the [[topology]] of the [[Kac-Moody group|Kac-Moody]] U-duality groups is in 

* [[Arjan Keurentjes]], _The topology of U-duality (sub-)groups_ ([arXiv:hep-th/0309106](http://arxiv.org/abs/hep-th/0309106))

* [[Arjan Keurentjes]], _U-duality (sub-)groups and their topology_ ([arXiv:hep-th/0312134](http://arxiv.org/abs/hep-th/0312134))

A discussion in the context of [[generalized complex geometry]] / [[exceptional generalized complex geometry]] is in 

* Paulo Pires Pacheco, [[Daniel Waldram]], _M-theory, exceptional generalised geometry and superpotentials_ ([arXiv:0804.1362](http://arxiv.org/abs/0804.1362))

* Nicholas Houston, _Supergravity and Generalized Geometry_ Thesis (2010) ([pdf](https://workspace.imperial.ac.uk/theoreticalphysics/Public/MSc/Dissertations/2010/Nicholas%20Houston%20Dissertation.pdf))


General discussion of the [[Kac-Moody groups]] arising in this context is for instance in 

* Philipp Fleig, [[Axel Kleinschmidt]], _Eisenstein series for infinite-dimensional U-duality groups_ ([arXiv:1204.3043](http://arxiv.org/abs/1204.3043), [[Kleinschmidt12.pdf:file]])

### Relation to automorphic forms

String theory [[partition functions]] as [[automorphic forms]] for U-duality groups are discussed in 

* {#GRV10} [[Michael Green]], Jorge G. Russo, Pierre Vanhove, _Automorphic properties of low energy string amplitudes in various dimensions_ ([arXiv:1001.2535](http://arxiv.org/abs/1001.2535))

[[!redirects U-duality]]
[[!redirects U-duality groups]]

