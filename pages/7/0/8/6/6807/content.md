
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

The _BFSS matrix model_ ([Banks-Fischler-Shenker-Susskind 96](#BanksFischlerShenkerSusskind96), [Seiberg 97](#Seiberg97)) is the description of the [[worldline]] dynamics of interacting  [[D0-branes]]. In the [[large N limit]] of a large number of [[D0-branes]] this is  supposed to encode the [[non-perturbative quantum field theory|strong coupling limit]] of [[type IIA string theory]] known as _[[M-theory]]_  at least in certain corners of its [[moduli space]].

The BFSS model is a limiting case of the _[[BMN matrix model]]_, which improves on some of its shortcomings (see the [Open problems](#OpenProblems) below).

The BFSS matrix model was argued to arise in several seemingly rather different (but apparently secretly equivalent) ways: 

1. as the [[worldline]] theory of a large number of [[D0-branes]] in [[type IIA string theory]], 

1. as the [[Kaluza-Klein compactification]] of [[10d super Yang-Mills theory]] to 1+0 space dimensions, 

1. {#AsM2Regularization} as a certain non-commutative regularization  of the [[light-cone gauge quantization]] of the [[Green-Schwarz sigma-model]] for the [[M2-brane]] ([Nicolai-Helling 98](#NicolaiHelling98), [Dasgupta-Nicolai-Plefka 02](#DasguptaNicolaiPlefka02)). 

   In this picture matrix blocks around the diagonal correspond to blobs of [[membrane]], while off-diagonal matrix elements correspond to thin tubes of membrane connecting these blobs.

<center>
<img src="https://ncatlab.org/nlab/files/MatrixMembrane.jpg" width="500">
</center>

> graphics grabbed from [Dasgupta-Nicolai-Plefka 02](#DasguptaNicolaiPlefka02)

In any case, the BFSS matrix model ends up being a [[quantum mechanics|quantum mechanical]] system whose bosonic degrees of freedom are a set of 9+1 large [[matrices]]. These play the role of would-be [[coordinate functions]] and their [[eigenvalues]] may be interpreted as points in a [[non-commutative geometry|non-commutative]] [[spacetime]] thus defined.

There is also the [[IKKT matrix model]], which takes this one step further by reducing one dimension further down to [[D(-1)-branes]] in [[type IIB string theory]]. 

See also at _[[membrane matrix model]]_.

## Open problems
 {#OpenProblems}

### General

In the 90s there was much excitement about the BFSS model, as people hoped it might provide a definition of [[M-theory]]. It is from these times that [[Edward Witten]] changed the original suggestion that "M" is for "magic, mystery and membrane" to the suggestion that it is for "magic, mystery and matrix". (See [Witten's 2014 Kyoto prize speech](M-theory#Witten14), last paragraph.) 

However, while the BFSS matrix model clearly sees something M-theoretic, just as clearly it is not the full answer. Notably it needs for its definition an ambient asympototic Minkowski background, a light cone limit and a peculiar scaling of [[string coupling]] over [[string length]], all of which means that it pertains to a particular corner of a full theory. 

From [Nicolai-Helling 98, p. 2](#NicolaiHelling98):

> Despite the recent excitement, however, we do not think that M(atrix) theory and the $d= 11$ supermembrane in their present incarnation are already the final answer in the search for M-Theory, even though they probably are important pieces of the puzzle. There are still too many ingredients missing that we would expect the final theory to possess. For one thing, we would expect a true theory of quantum gravity to exhibit certain pregeometrical features corresponding to a “dissolution” of space-time and the emergence of some kind of non-commutative geometry at short distances; although the matrix model does achieve that to some extent by replacing commuting coordinates by non-commuting matrices, it seems to us that a still more radical departure from conventional ideas about space and time may be required in order to arrive at a truly background independent formulation (the matrix model “lives” in nine _flat_ transverse dimensions only). Furthermore, there should exist some huge and so far completely hidden symmetries generalizing not only the duality symmetries of extended supergravity and string theory, but also the principles underlying general relativity.

From [Mohammed-Murugan-Nastase 10, p. 6](#MohammedMuruganNastase10):

>  If Matrix theory is to correctly describe M-theory (and its dimensional reduction to type IIA string theory) then it should
be able to describe all D−branes in the theory and not just D2−branes. For example, a D4−brane wrapping an $S^4$ was found in [9], following the earlier works of [10, 11], but the solution is not without several unresolved subtleties. In general, finding the complete spectrum of D−branes from Matrix
theory remains a very difficult problem. The D2− and D4−branes already found are reductions to
ten dimensions of M2− and M5−branes, and while they are a minimum necessary for the spectrum of M-theory, they are by no means sufficient. Indeed, we would also need to find a D6−brane, coming from an eleven dimensional KK monopole, and a D8−brane.

Then, even assuming that all the crucial [[generalized (Eilenberg-Steenrod) cohomology|cohomological]] aspects of [[D-brane]] and [[M-brane]] charges (in [[twisted differential K-theory]], [[twisted cohomotopy]] etc.) are secretly encoded in the matrix model, somehow, none of this is manifest, making the matrix model spit out numbers about a conceptually elusive theory in close analogy to how [[lattice QCD]] produces numbers without informing us about the actual conceptual nature of [[confinement|confined]] [[hadron]] physics.



A similar assessment has been given by [[Greg Moore]], from pages 43-44 of his _[[Physical Mathematics and the Future]]_ ([here](Physical+Mathematics+and+the+Future#AGoodStartWasGivenByTheMatrixTheory)):

> A good start $[$with defining M-theory$]$ was given by the Matrix theory approach of Banks, Fischler, Shenker and Susskind. We have every reason to expect that this theory produces the correct scattering amplitudes of modes in the 11-dimensional supergravity multiplet in 11-dimensional Minkowski space - even at energies sufficiently large that black holes should be created. (This latter phenomenon has never been explicitly demonstrated). But Matrix theory is only a beginning and does not give us the whole picture of M-theory. The program ran into increasing technical difficulties when more complicated compactifications were investigated. (For example, compactification on a six-dimensional torus is not very well understood at all. $[$...$]$). Moreover, to my mind, as it has thus far been practiced it has an important flaw: It has not led to much significant new mathematics.

> If history is a good guide, then we should expect that anything as profound and far-reaching as a fully satisfactory formulation of M-theory is surely going to lead to new and novel mathematics. Regrettably, it is a problem the community seems to have put aside - temporarily. But, ultimately, Physical Mathematics must return to this grand issue.

### Ground state
 {#ProblemsGroundState}

There are furcher technical open issues, such as the open question whether the theory has a decent ground state the way it needs to have to make sense (see the references [below](#ReferencesGroundStateProblem)).

## Related concepts

[[!include brane matrix models -- content]]


* [[SYK model]]

* [[Myers effect]]

## References
 {#References}

### General

First inkling of [[matrix models]] from the [[large N limit]] of [[QCD]]:

* {#EguchiKawai82} [[Tohru Eguchi]], [[Hikaru Kawai]], _Reduction of Dynamical Degrees of Freedom in the Large-$N$ Gauge Theory_, Phys. Rev. Lett. 48, 1063 (1982) ([spire:176459](http://inspirehep.net/record/176459), [doi:10.1103/PhysRevLett.48.1063](https://doi.org/10.1103/PhysRevLett.48.1063))

* A. Gonzalez-Arroyo, M. Okawa, _A twisted model for large $N$ lattice gauge theory_, Physics Letters B Volume 120, Issues 1–3, 6 January 1983, Pages 174-178 (<a href="https://doi.org/10.1016/0370-2693(83)90647-0">doi:10.1016/0370-2693(83)90647-0</a>)

* A. Gonzalez-Arroyo, M. Okawa, _Twisted-Eguchi-Kawai model: A reduced model for large-
$N$ lattice gauge theory_, Phys. Rev. D 27, 2397 (1983) ([doi:10.1103/PhysRevD.27.2397](https://doi.org/10.1103/PhysRevD.27.2397))


The original articles on the BFSS matrix model:

* {#BanksFischlerShenkerSusskind96} [[Tom Banks]], [[Willy Fischler]], [[Stephen Shenker]], [[Leonard Susskind]], _M Theory As A Matrix Model: A Conjecture_,  Phys. Rev. D55 (1997). ([arXiv:hep-th/9610043](http://arxiv.org/abs/hep-th/9610043))

* [[Leonard Susskind]], _Another Conjecture about M(atrix) Theory_ ([arXiv:hep-th/9704080](https://arxiv.org/abs/hep-th/9704080)) 

  (argument for [[small N limit|small N]]-validity)

* {#Sen97} [[Ashoke Sen]], _D0 Branes on $T^n$ and Matrix Theory_, Adv. Theor. Math. Phys.2:51-59, 1998 ([arXiv:hep-th/9709220](https://arxiv.org/abs/hep-th/9709220))

* {#Seiberg97} [[Nathan Seiberg]], _Why is the Matrix Model Correct?_, Phys. Rev. Lett. 79:3577-3580, 1997 ([arXiv:hep-th/9710009](https://arxiv.org/abs/hep-th/9710009))


Review includes

* [[Tom Banks]], _Matrix Theory_, Nucl.Phys.Proc.Suppl. 67 (1998) 180-224 ([arXiv:hep-th/9710231](https://arxiv.org/abs/hep-th/9710231))

* [[Washington Taylor]], _M(atrix) Theory: Matrix Quantum Mechanics as a Fundamental Theory_, Rev. Mod. Phys. 73:419-462, 2001 ([arXiv:hep-th/0101126](https://arxiv.org/abs/hep-th/0101126))

* {#Ydri18} [[Badis Ydri]], _Review of M(atrix)-Theory, Type IIB Matrix Model and Matrix String Theory_ ([arXiv:1708.00734](https://arxiv.org/abs/1708.00734)), published as: _Matrix Models of String Theory_, IOP 2018 ([ISBN:978-0-7503-1726-9](https://iopscience.iop.org/book/978-0-7503-1726-9))

A review of further developments is in 

* [[David Berenstein]], _Classical dynamics and thermalization in holographic matrix models_, talk at Leiden, October 2012 ([pdf](http://www.lorentzcenter.nl/lc/web/2012/514/presentations/Berenstein.pdf))

See also

* [[Paul Townsend]], _M(embrane) theory on $T^0$_, Nucl. Phys. Proc. Suppl. 68:11-16, 1998 ([arXiv:hep-th/9708034](http://arxiv.org/abs/hep-th/9708034))

Discussion as a solution to the open problem of defining [[M-theory]] is in 

* {#Moore14} [[Gregory Moore]], section 12 p. 43-44 _[[Physical Mathematics and the Future]]_ talk at [Strings 2014](http://physics.princeton.edu/strings2014/)  ([talk slides](http://physics.princeton.edu/strings2014/slides/Moore.pdf), [companion text pdf](http://www.physics.rutgers.edu/~gmoore/PhysicalMathematicsAndFuture.pdf), [[MooreVisionTalk2014.pdf:file]])

where it says:

> {#AGoodStartWasGivenByTheMatrixTheory} A good start was given by the [[BFSS matrix model|Matrix theory]] approach of [[Tom Banks|Banks]], [[Willy Fischler|Fischler]], Shenker and [[Leonard Susskind|Susskind]]. We have every reason to expect that this theory produces the correct [[scattering amplitudes]] of modes in the [[11-dimensional supergravity]] multiplet in 11-dimensional [[Minkowski space]] - even at energies sufficiently large that [[black holes]] should be created. (This latter phenomenon has never been explicitly demonstrated). But Matrix theory is only a beginning and does not give us the whole picture of [[M-theory]]. The program ran into increasing technical difficulties when more complicated compactifications were investigated. (For example, compactification on a six-dimensional torus is not very well understood at all. $[...]$). Moreover, to my mind, as it has thus far been practiced it has an important flaw: It has not led to much significant new mathematics. 

> If history is a good guide, then we should expect that anything as profound and far-reaching as a fully satisfactory formulation of [[M-theory]] is surely going to lead to new and novel mathematics. Regrettably, it is a problem the community seems to have put aside - temporarily. But, ultimately, Physical Mathematics must return to this grand issue.





Derivation from [[open string field theory]] is discussed in

* [[Taejin Lee]], _Covariant Open String Field Theory on Multiple D$p$-Branes_ ([arXiv:1703.06402](https://arxiv.org/abs/1703.06402))




Relation to the [[6d (2,0)-supersymmetric QFT]]:

* [[Micha Berkooz]], [[Moshe Rozali]], [[Nathan Seiberg]], _Matrix Description of M-theory on $T^3$ and $T^5$_ ([arXiv:hep-th/9704089](http://arxiv.org/abs/hep-th/9704089))




[[!include quantization of M2-brane on Minkowski spacetime to BFSS matrix model -- references]]

See also in relation to the [[ABJM model]]:

* {#MohammedMuruganNastase10} Asadig Mohammed, Jeff Murugan, [[Horatiu Nastase]], _Looking for a Matrix model of ABJM_, Phys. Rev. D82:086004, 2010 ([arXiv:1003.2599](https://arxiv.org/abs/1003.2599))



### Relation to M5-branes

Discussion of [[light cone longitudal]] [[M5-branes]] in the [[BFSS matrix model]] (for [[light cone transversal]] M5-s see at _[[BMN matrix model]]_):

* [[Tom Banks]], [[Nathan Seiberg]], [[Stephen Shenker]], _Branes from Matrices_, Nucl. Phys. B490:91-106, 1997 ([arXiv:hep-th/9612157](https://arxiv.org/abs/hep-th/9612157))


* Judith Castelino, Sangmin Lee, [[Washington Taylor]], _Longitudinal 5-branes as 4-spheres in Matrix theory_, Nucl. Phys. B526:334-350, 1998 ([arXiv:hep-th/9712105](https://arxiv.org/abs/hep-th/9712105))

  (introducing the [[fuzzy 4-sphere]])

Discussion of a [[BFSS matrix model|BFSS-like]] [[matrix model]] for [[MK6-branes]]:

* [[Amihay Hanany]], Gilad Lifschytz, _M(atrix) Theory on $T^6$ and a m(atrix) Theory Description of KK Monopoles_, Nucl. Phys. B519:195-213, 1998 ([arXiv:hep-th/9708037](https://arxiv.org/abs/hep-th/9708037))


### Ground state problem
  {#ReferencesGroundStateProblem}

There remains the problem of existence of a sensible ground state of the BFSS model. 

* [[Bernard de Wit]], M. Luscher, [[Hermann Nicolai]], _The Supermembrane Is Unstable_, Nucl.Phys. B320 (1989) 135-159 ([spire:266584](http://inspirehep.net/record/266584), <a href="https://doi.org/10.1016/0550-3213(89)90214-9">doi:10.1016/0550-3213(89)90214-9</a>)
 

For a new attempt at solving this problem, and for pointers to previous attempts see

* L. Boulton, M.P. Garcia del Moral, A. Restuccia, _The ground state of the D=11 supermembrane and matrix models on compact regions_, Nuclear Physics B
Volume 910, September 2016, Pages 665-684 ([arXiv:1504.04071](https://arxiv.org/abs/1504.04071))

* L. Boulton, M.P. Garcia del Moral, A. Restuccia, _Measure of the potential valleys of the supermembrane theory_, Physics Letters B
Volume 797, 2019, 134873 ([arXiv:1811.05758](https://arxiv.org/abs/1811.05758))

### Graviton scattering
 {#ReferencesGravitonScattering}

Computation of [[graviton]] [[scattering amplitudes]]:

* [[Katrin Becker]], [[Melanie Becker]], _A Two-Loop Test of M(atrix) Theory_, Nucl.Phys. B506 (1997) 48-60 ([arXiv:hep-th/9705091](https://arxiv.org/abs/hep-th/9705091))

* [[Katrin Becker]], [[Melanie Becker]], [[Joseph Polchinski]], [[Arkady Tseytlin]], _Higher Order Graviton Scattering in M(atrix) Theory_, Phys.Rev.D56:3174-3178,1997 ([arXiv:hep-th/9706072](https://arxiv.org/abs/hep-th/9706072))

* also [Kabat-Taylor 97](#KabatTaylor97)

* M. Fabbrichesi, _Graviton scattering in matrix theory and supergravity_, in: Ceresole A., Kounnas C., [[Dieter Lüst]], [[Stefan Theisen]] (eds.) _Quantum Aspects of Gauge Theories, Supersymmetry and Unification_, Lecture Notes in Physics, vol 525. Springer, Berlin, Heidelberg ([arXiv:hep-th/9811204](https://arxiv.org/abs/hep-th/9811204))

* Robert Helling, [[Jan Plefka]], Marco Serone, Andrew Waldron, _Three-graviton scattering in M-theory_, Nuclear Physics B Volume 559, Issues 1–2, 18 October 1999, Pages 184-204 ([arXiv:hep-th/9905183](https://arxiv.org/abs/hep-th/9905183))

* Robert Echols, _M-theory, supergravity and the matrix model: Graviton scattering and non-renormalization theorems_, PhD thesis, 1999 [pdf](https://web.calpoly.edu/~rechols/phys403/mythesis.pdf)

### Black holes

Relation to [[black holes in string theory]]:

* [[Tom Banks]], [[Willy Fischler]], [[Igor Klebanov]], [[Leonard Susskind]],  _Schwarzschild Black Holes from Matrix Theory_, Phys.Rev.Lett.80:226-229,1998 ([arXiv:hep-th/9709091](https://arxiv.org/abs/hep-th/9709091))

* [[Tom Banks]], [[Willy Fischler]], [[Igor Klebanov]], [[Leonard Susskind]], _Schwarzchild Black Holes in Matrix Theory II_, JHEP 9801:008,1998 ([arXiv:hep-th/9711005](https://arxiv.org/abs/hep-th/9711005))  

* [[Igor Klebanov]], [[Leonard Susskind]], _Schwarzschild Black Holes in Various Dimensions from Matrix Theory_, Phys.Lett.B416:62-66,1998 ([arXiv:hep-th/9709108](https://arxiv.org/abs/hep-th/9709108))

* Edi Halyo, _Six Dimensional Schwarzschild Black Holes in M(atrix) Theory_ ([arXiv:hep-th/9709225](https://arxiv.org/abs/hep-th/9709225))

* [[Gary Horowitz]], [[Emil Martinec]], _Comments on Black Holes in Matrix Theory_, Phys. Rev. D 57, 4935 (1998) ([arXiv:hep-th/9710217](https://arxiv.org/abs/hep-th/9710217))

* {#KabatTaylor97} Daniel Kabat, [[Washington Taylor]], _Spherical membranes in Matrix theory_, Adv.Theor.Math.Phys.2:181-206,1998 ([arXiv:hep-th/9711078](https://arxiv.org/abs/hep-th/9711078)) 

* Yoshifumi Hyakutake, _Black Hole and Fuzzy Objects in BFSS Matrix Model_ 
([arXiv:1801.07869](https://arxiv.org/abs/1801.07869))

* {#DuSahakian18} Haoxing Du, Vatche Sahakian, _Emergent geometry from stochastic dynamics, or Hawking evaporation in M(atrix) theory_ ([arXiv:1812.05020](https://arxiv.org/abs/1812.05020))

  (combination with [[random matrix theory]])


### Relation to lattice gauge theory

Relation to [[lattice gauge theory]] and numerical tests of [[AdS/CFT]]:


* {#Joseph15} Anosh Joseph, _Review of Lattice Supersymmetry and Gauge-Gravity Duality_
([arXiv:1509.01440](https://arxiv.org/abs/1509.01440))

* Veselin G. Filev, Denjoe O'Connor, _The BFSS model on the lattice_, JHEP 1605 (2016) 167 ([arXiv:1506.01366](https://arxiv.org/abs/1506.01366))


* {#Hanada16} Masanori Hanada, _What lattice theorists can do for superstring/M-theory_,  International Journal of Modern Physics AVol. 31, No. 22, 1643006 (2016)  ([arXiv:1604.05421](https://arxiv.org/abs/1604.05421))

### Holography

On [[AdS/CFT]] in the form of [[AdS2/CFT1]] with the [[BFSS matrix model]] on the CFT side and [[black hole in string theory|black hole-like solutions]] in [[type IIA supergravity]] on the AdS side:

* [[Juan Maldacena]], Alexey Milekhin, _To gauge or not to gauge?_, JHEP 04 (2018) 084 ([arxiv:1802.00428](https://arxiv.org/abs/1802.00428))

and concerning the analog of its [[holographic entanglement entropy]]:

* Tarek Anous, Joanna L. Karczmarek, Eric Mintun, [[Mark Van Raamsdonk]], Benson Way, _Areas and entropies in BFSS/gravity duality_ ([arXiv:1911.11145](https://arxiv.org/abs/1911.11145))




[[!redirects BFSS model]]
