
#Contents#
* table of contents
{:toc}

## Idea

In [[quantum field theory]] and [[statistical physics]], a _single trace operator_ is an [[observable]]/[[correlator]] on [[square matrix]]- or rather [[adjoint representation]]-valued [[scalar fields]]/[[random variables]] $\{\phi_i\}_{i \in I}$ which is built from the elementary [[field observables]] $\mathbf{\Phi}_i$ as a [[trace]] over the [[matrix product]] of a finite string of them:

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

If the [[field (physics)|fields]] $\phi_i$ indeed take values in the [[adjoint representation]] of a given [[gauge group]], then the [[trace]] in the expression (eq:ASingleTraceObservable) ensures that this [[observable]] is [[gauge invariant]]. More general [[gauge invariant]] [[observables]] are hence _multi-trace operators_ which are [[linear combinations]] of products of single-trace observables.




## Properties

### Relation to strings under AdS/CFT

Single trace operators/observables in [[conformal field theories]] such as [[super Yang-Mills theories]] play a special role in the [[AdS-CFT correspondence]], under which they correspond to single [[string]] excitations on the [[AdS spacetime|AdS]]-[[supergravity]] side of the correspondence, where, curiously, the "string of characters/letters" in the argument of the trace gets literally mapped to a [[superstring]] in [[spacetime]] (see the references [below](#ReferencesRelationToStringExcitations)).

From [Polyakov 02](#Polyakov02), referring to gauge fields and their single trace operators as _letter_ and _words_, respectively:

> The picture which slowly arises from the above considerations is that of the space-time gradually disappearing in the regions of large curvature. The natural description in this case is provided by a gauge theory in which the basic objects are the texts formed from the gauge-invariant words. The theory provides us with the expectation values assigned to the various texts, words and sentences.


> These expectation values can be calculated either from the gauge theory or from the strongly coupled 2d sigma model. The coupling in this model is proportional to the target space curvature. This target space can be interpreted as a usual continuous space-time only when the curvature is small. As we increase the coupling, this interpretation becomes more and more fuzzy and finally completely meaningless. 

From [Berenstein-Maldacena-Nastase 02](#BerensteinMaldacenaNastase02), who write $Z$ for the elementary [[field observables]] ("letters") $\mathbf{\Phi}$ above:

> In summary, the "string of $Z$s" becomes the physical string and that each $Z$ carries one unit of $J$ which is one unit of $p_+$. Locality along the worldsheet of the string comes from the fact that planar diagrams allow only contractions of neighboring operators. So the Yang Mills theory gives a string bit model (see $[23]$) where each bit is a $Z$ operator. 

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


## References

### General

(...)

### Relation to string excitations under AdS/CFT
 {#ReferencesRelationToStringExcitations}

Relation of single trace operators to [[superstring]] excitations under the [[AdS-CFT correspondence]]:

* {#Polyakov02} [[Alexander Polyakov]], _Gauge Fields and Space-Time_, Int. J. Mod. Phys. A17S1 (2002) 119-136 ([arXiv:hep-th/0110196](https://arxiv.org/abs/hep-th/0110196))


* {#BerensteinMaldacenaNastase02} [[David Berenstein]], [[Juan Maldacena]], [[Horatiu Nastase]], _Strings in flat space and pp waves from $\mathcal{N} = 4$ Super Yang Mills_, JHEP 0204 (2002) 013 ([arXiv:hep-th/0202021](https://arxiv.org/abs/hep-th/0202021))

* {#Kruczenski04} Martin Kruczenski, _Spiky strings and single trace operators in gauge theories_, JHEP 0508:014, 2005 ([arXiv:hep-th/0410226](https://arxiv.org/abs/hep-th/0410226))

(...)

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

