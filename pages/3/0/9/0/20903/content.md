
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[quantum field theory]] and [[statistical physics]], a _single trace operator_ is an [[observable]]/[[correlator]] on [[square matrix]]- or rather [[adjoint representation]]-valued [[scalar fields]]/[[random variables]] $\{\phi_i\}_{i \in I}$ (notationally subsuming [[derivatives]] of fields) which is built from the elementary [[field observables]] $\mathbf{\Phi}_i$ as a [[trace]] over the [[matrix product]] of a finite string of them:

\[
  \label{ASingleTraceObservable}
  \mathcal{O}_{i_1, \cdots i_n}
  \;=\;
  Tr\big(
   \mathbf{\Phi}_{i_1}
   \cdot
   \mathbf{\Phi}_{i_2}
    \cdot
    \cdots
    \cdot
   \mathbf{\Phi}_{i_n}
  \big)
\]

or more generally as [[linear combinations]] thereof.

If the [[field (physics)|fields]] $\phi_i$ indeed take values in the [[adjoint representation]] of a given [[gauge group]], then the [[trace]] in the expression (eq:ASingleTraceObservable) ensures that this [[observable]] is [[gauge invariant]]. More general [[gauge invariant]] [[observables]] are hence _[[multi-trace operators]]_ which are [[linear combinations]] of products of single-trace observables (i.e. [[polynomials]] of single-trace observables).



## Properties

### Correspondence to strings under AdS/CFT
 {#CorrespondenceToStringsUnderAdSCFT}

Single trace operators/observables in [[conformal field theories]] such as [[super Yang-Mills theories]] play a special role in the [[AdS-CFT correspondence]]: They correspond to single [[string]] excitations on the [[AdS spacetime|AdS]]-[[supergravity]] side of the correspondence, where, curiously, the "string of characters/letters" in the argument of the trace gets literally mapped to a [[superstring]] in [[spacetime]] (see the references [below](#ReferencesRelationToStringExcitations)).

From [Polyakov 02](#Polyakov02), referring to gauge fields and their single trace operators as _letter_ and _words_, respectively:

> The picture which slowly arises from the above considerations is that of the space-time gradually disappearing in the regions of large curvature. The natural description in this case is provided by a gauge theory in which the basic objects are the texts formed from the gauge-invariant words. The theory provides us with the expectation values assigned to the various texts, words and sentences.


> These expectation values can be calculated either from the gauge theory or from the strongly coupled 2d sigma model. The coupling in this model is proportional to the target space curvature. This target space can be interpreted as a usual continuous space-time only when the curvature is small. As we increase the coupling, this interpretation becomes more and more fuzzy and finally completely meaningless. 

From [Berenstein-Maldacena-Nastase 02](#BerensteinMaldacenaNastase02), who write $Z$ for the elementary [[field observables]] ("letters") $\mathbf{\Phi}$ above:

> In summary, the "string of $Z$s" becomes the physical string and that each $Z$ carries one unit of $J$ which is one unit of $p_+$. Locality along the worldsheet of the string comes from the fact that planar diagrams allow only contractions of neighboring operators. So the Yang Mills theory gives a [[string bit model]] where each bit is a $Z$ operator. 

On the [[CFT]] side these _[[BMN operators]]_ of fixed length (of "letters") are usefully identified as  [[spin chains]] which, with the [[dilatation operator]] regarded as their [[Hamiltonian]], are [[integrable systems]] ([Minahan-Zarembo 02](#MinahanZarembo02), [Beisert-Staudacher 03](#BeisertStaudacher03)).

This integrability allows a detailed matching between 

* [[single trace operators]]/[[BMN operators]] in [[D=4 N=4 super Yang-Mills theory]] 

* the [[classical field theory|classical]] [[Green-Schwarz superstring]] on [[anti de Sitter spacetime|AdS5]] $\times$ [[5-sphere|S5]]

under [[AdS/CFT duality]] ([Beisert-Frolov-Staudacher-Tseytlin 03](#BeisertFrolovStaudacherTseytlin03), ...). For review see [BBGK 04](#BBGK04), [Beisert et al. 10](#BeisertEtAl10).

(...)

### Relation to weight systems on chord diagrams

For [[field (physics)|fields]] $\phi$ valued in a [[Lie algebra representations]] $C \in \mathfrak{g}Mod$ of a [[metric Lie algebra]], with $\{\phi_a\}$ a [[linear basis]] for $C$ and $\{\phi^a\}$ denoting the dual basis, those single trace operators involving only metric pairs of fields, such as

$$
  \mathcal{O}
  \;\coloneqq\;
  Tr_C
  \big(
    \mathbf{\Phi}_{a_1}
    \cdot
    \mathbf{\Phi}_{a_2}
    \cdot
    \mathbf{\Phi}^{a_1}
    \cdot
    \mathbf{\Phi}^{a_2}
  \big)
$$

(using [[Einstein summation convention]]) are equivalently values of [[Lie algebra weight systems]] on the [[chord diagram]] that expresses the index pairing.

Such binary pairings inside the trace are induced notably after statistical averaging in  the [[SYK model]] and related systems, and has been argued to appear generically for [[AdS/CFT|dual]] [[observables]] of [[black hole thermodynamics]] ([Berkooz-Narayan-Simón 18, Section 2.1](#BerkoozNarayanSimon18)). 

For more on this see at _[[weight systems on chord diagrams in physics]]_.

## Examples

### Shape of D$p$ $\bot$ D$(p+2)$-fuzzy funnels
  {#SingleTraceObservablesAsWeightSystemsOnChordDiagrams}


<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/WeightSystemsAsShapeObservabesOnFuzzySphere.jpg" width="400">
</div>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

We discuss how the [[single trace observables]] on the [[fuzzy 2-sphere]]-sections  of [[Dp-D(p+2) brane intersection]] [[fuzzy funnels]] are given by [[su(2)]]-[[Lie algebra weight systems]] on [[chord diagrams]] (following [Ramgoolam-Spence-Thomas 04](#RamgoolamSpenceThomas04), [McNamara-Papageorgakis 05](#McNamaraPapageorgakis05), see [McNamara 06, Section 4](#McNamara06) for review).

\linebreak


While in the commutative [[large N limit]], all powers of the [[radius]] function on the [[fuzzy 2-sphere]] are equal

$$
  \underset{N\to \infty}{\lim}
  \int_{S^2_N} R^{2 k}
  \;=\;  
  4 \pi 
  \,;
$$

for [[finite number|finite]] $N$ there is an ordering ambiguity: In fact, the number of functions on the [[fuzzy 2-sphere]] at [[finite number|finite]] $N$ that all go to the same function $R^{2k}$ in the [[large N limit]] grows rapidly with $k$.

At $k = 1$ there is the single radius observable (eq:RadiusOfFuzzy2Sphere)

$$
  \int_{S^2_N} R^2 
  \;=\; 
  \int_{S^2_N}
  \underset{i}{\sum} X_i \cdot X_i
  \;=\;
  4 \pi \tfrac{ N }{ \sqrt{N^2 -1} }
$$

At $k = 2$ there are, under the integral (eq:FuzzyS2Integration), two radius observables:

1. $ \int_{S^2_N} \underset{i,j}{\sum} X_i X_i X_j X_j$

1. $\int_{S^2_N} \underset{i,j}{\sum} X_i X_j X_j X_i$

(Here we are using that under the integral/trace, a [[cyclic permutation]] of the factors in the integrand does not change the result).

Similarly for higher $k$, where the number of possible orderings increases rapidly. The [[combinatorics]] that appears here is familiar in [[knot theory]]:

Every ordering of operators, up to cyclic permutation, in the [[single trace observable]] $Tr(R^2)^n$ is encoded in a [[chord diagram]] and the value of the corresponding [[single trace observable]] is the value of the [[su(2)]]-[[Lie algebra weight system]] on this chord diagram.


## Related concepts

* [[string bit model]]

* [[multi-trace operator]]

## References

### General

(...)

### Correspondence to string excitations under AdS/CFT
 {#ReferencesRelationToStringExcitations}

The correspondence of single trace operators to [[superstring]] excitations under the [[AdS-CFT correspondence]] originates with these articles:

* {#Polyakov02} [[Alexander Polyakov]], _Gauge Fields and Space-Time_, Int. J. Mod. Phys. A17S1 (2002) 119-136 ([arXiv:hep-th/0110196](https://arxiv.org/abs/hep-th/0110196))


* {#BerensteinMaldacenaNastase02} [[David Berenstein]], [[Juan Maldacena]], [[Horatiu Nastase]], _Strings in flat space and pp waves from $\mathcal{N} = 4$ Super Yang Mills_, JHEP 0204 (2002) 013 ([arXiv:hep-th/0202021](https://arxiv.org/abs/hep-th/0202021))

  (whence "[[BMN operators]]")

* [[Steven Gubser]], [[Igor Klebanov]], [[Alexander Polyakov]], _A semi-classical limit of the gauge/string correspondence_, Nucl. Phys. B636 (2002) 99-114 ([arXiv:hep-th/0204051](https://arxiv.org/abs/hep-th/0204051))


* {#Kruczenski04} [[Martin Kruczenski]], _Spiky strings and single trace operators in gauge theories_, JHEP 0508:014, 2005 ([arXiv:hep-th/0410226](https://arxiv.org/abs/hep-th/0410226))

The identification of the relevant [[single trace operators]] with [[integrable system|integrable]] [[spin chains]] is due to

* {#MinahanZarembo02}  J. A. Minahan, [[Konstantin Zarembo]], _The Bethe-Ansatz for $\mathcal{N} = 4$ Super Yang-Mills_, JHEP 0303 (2003) 013 ([arXiv:hep-th/0212208](https://arxiv.org/abs/hep-th/0212208))

* {#BeisertStaudacher03} [[Niklas Beisert]], [[Matthias Staudacher]], _The $\mathcal{N}=4$ SYM Integrable Super Spin Chain_,  Nucl. Phys. B 670:439-463, 2003 ([arXiv:hep-th/0307042](https://arxiv.org/abs/hep-th/0307042))

which led to more detailed matching of [[single trace operators]] to rotating string excitations in

* {#BeisertFrolovStaudacherTseytlin03} [[Niklas Beisert]], [[Sergey Frolov]], [[Matthias Staudacher]], [[Arkady Tseytlin]], _Precision Spectroscopy of AdS/CFT_, JHEP 0310:037, 2003 ([arXiv:hep-th/0308117](https://arxiv.org/abs/hep-th/0308117))

Review includes

* {#BBGK04} A. V. Belitsky, [[Volker Braun]], A. S. Gorsky, G. P. Korchemsky, _Integrability in QCD and beyond_, Int. J. Mod. Phys. A19:4715-4788, 2004 ([arXiv:hep-th/0407232](https://arxiv.org/abs/hep-th/0407232))

* {#BeisertEtAl10} [[Niklas Beisert]], [[Luis Alday]], [[Radu Roiban]], [[Sakura Schafer-Nameki]], [[Matthias Staudacher]], [[Alessandro Torrielli]], [[Arkady Tseytlin]], et. al., _Review of AdS/CFT Integrability: An Overview_, Lett. Math. Phys. 99, 3 (2012) ([arXiv:1012.3982](https://arxiv.org/abs/1012.3982))

### Relation to weight systems on chord diagrams

A general relation between [[single trace operators]] for [[observables]] on [[black hole thermodynamics]] and [[Lie algebra weight systems]] on [[chord diagrams]] (though not using the term "weight system") is proposed in

* {#BerkoozNarayanSimon18} [[Micha Berkooz]], [[Prithvi Narayan]], [[Joan Simón]], Section 2.1 of: _Chord diagrams, exact correlators in spin glasses and black hole bulk reconstruction_, JHEP 08 (2018) 192 ([arxiv:1806.04380](https://arxiv.org/abs/1806.04380))

For more on this see at _[[weight systems on chord diagrams in physics]]_.

#### For JT-gravity/SYK model

Discussion of ([[Lie algebra weight system|Lie algebra]]-)[[weight systems]] on [[chord diagrams]] encoding [[SYK model]] [[single trace observables]]:


* Antonio M. García-García, Yiyang Jia, Jacobus J. M. Verbaarschot, _Exact moments of the Sachdev-Ye-Kitaev model up to order $1/N^2$_, JHEP 04 (2018) 146 ([arXiv:1801.02696](https://arxiv.org/abs/1801.02696))

* [[Micha Berkooz]], Prithvi Narayan, [[Joan Simón]], _Chord diagrams, exact correlators in spin glasses and black hole bulk reconstruction_, JHEP 08 (2018) 192 ([arxiv:1806.04380](https://arxiv.org/abs/1806.04380))


following:

* László Erdős, Dominik Schröder, _Phase Transition in the Density of States of Quantum Spin Glasses_, D. Math Phys Anal Geom (2014) 17: 9164 ([arXiv:1407.1552](https://arxiv.org/abs/1407.1552))

which in turn follows

* Philippe Flajolet, Marc Noy, _Analytic Combinatorics of Chord Diagrams_, pages 191–201 in Daniel Krob, Alexander A. Mikhalev,and Alexander V. Mikhalev, (eds.), _Formal Power Series and Algebraic Combinatorics_, Springer 2000 ([doi:10.1007/978-3-662-04166-6_17](https://doi.org/10.1007/978-3-662-04166-6_17))

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/ChordDiagramHolographic.jpg" width="400">
</div>

With emphasis on [[AdS-CFT|holographic content]]:

* [[Micha Berkooz]], Mikhail Isachenkov, Vladimir Narovlansky, Genis Torrents, Section 5 of: _Towards a full solution of the large $N$ double-scaled SYK model_, JHEP 03 (2019) 079 ([arxiv:1811.02584](https://arxiv.org/abs/1811.02584))

* Vladimir Narovlansky, Slide 23 (of 28) of: _Towards a Solution of Large $N$ Double-Scaled SYK_, 2019 ([[NarovlanskySYK19.pdf:file]])

and specifically in relation to [[Jackiw-Teitelboim gravity]]: 

* [[Andreas Blommaert]], [[Thomas Mertens]], [[Henri Verschelde]], _The Schwarzian Theory - A Wilson Line Perspective_, JHEP 1812 (2018) 022 ([arXiv:1806.07765](https://arxiv.org/abs/1806.07765))

* [[Andreas Blommaert]], [[Thomas Mertens]], [[Henri Verschelde]], _Fine Structure of Jackiw-Teitelboim Quantum Gravity_, JHEP 1909 (2019) 066 ([arXiv:1812.00918](https://arxiv.org/abs/1812.00918))

#### For D$p$-D$(p+2)$-brane intersections

Discussion of [[weight systems]] on [[chord diagrams]] as [[single trace observables]] on the [[fuzzy funnel]]/[[fuzzy sphere]] [[non-commutative geometry]] of [[Dp-D(p+2)-brane intersections]] ([hence](Dp-Dp+2-brane+bound+states#ReferencesRelationToMonopoles)
[[Yang-Mills monopoles]]):

* [[Sanyaje Ramgoolam]], [[Bill Spence]], S. Thomas, Section 3.2 of: _Resolving brane collapse with $1/N$ corrections in non-Abelian DBI_, Nucl. Phys. B703 (2004) 236-276 ([arxiv:hep-th/0405256](https://arxiv.org/abs/hep-th/0405256))

* [[Simon McNamara]], [[Constantinos Papageorgakis]], [[Sanyaje Ramgoolam]], [[Bill Spence]], Appendix A of: _Finite $N$ effects on the collapse of fuzzy spheres_, JHEP 0605:060, 2006 ([arxiv:hep-th/0512145](https://arxiv.org/abs/hep-th/0512145))

* [[Simon McNamara]], Section 4 of: _Twistor Inspired Methods in Perturbative FieldTheory and Fuzzy Funnels_, 2006 ([spire:1351861](http://inspirehep.net/record/1351861), [pdf](https://strings.ph.qmul.ac.uk/sites/default/files/Mcnamaraphd.pdf), [[McNamara06.pdf:file]])

* [[Constantinos Papageorgakis]], p. 161-162 of: _On matrix D-brane dynamics and fuzzy spheres_, 2006 ([[Papageorgakis06.pdf:file]])




[[!redirects single trace operators]]

[[!redirects single-trace operator]]
[[!redirects single-trace operator]]

[[!redirects single trace observable]]
[[!redirects single trace observables]]

[[!redirects single-trace observable]]
[[!redirects single-trace observables]]

[[!redirects BMN operator]]
[[!redirects BMN operators]]


