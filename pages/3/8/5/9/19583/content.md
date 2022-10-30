

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
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

From [Maldacena-Stanford 16](#MaldacenaStanford16):

> Studies of [[AdS-CFT|holography]] have been hampered by the lack of a simple solvable model that can capture features of [[Einstein gravity]].  The simplest model, which is a single matrix [[quantum mechanics]], does not appear to lead to [[black holes]]. $\mathcal{N} = 4$ [[N=4 D=4 super Yang-Mills theory|super Yang Mills]] at strong ’t Hooft [[coupling constant|coupling]] certainly leads to [[black holes]], and exact results are known at [[large N limit|large N]] for many anomalous dimensions and some [[vacuum amplitude|vacuum]] [[correlation functions]], but at [[thermal quantum field theory|finite temperature]] the theory is difficult to study.

> A system that reproduces some of the dynamics of [[black holes]] should be [[interacting quantum field theory|interacting]], but we might hope for a model with interactions that are simple enough that it is still reasonable solvable.

> [[Alexei Kitaev|Kitaev]] has proposed to study a quantum mechanical model of $N$ [[Majorana spinor|Majorana]] [[fermions]] [[interaction|interacting]]  with  random  interactions ([Kitaev 15](#Kitaev15)).   It is a simple variant of a model introduced by [[Subir Sachdev|Sachdev]] and Ye ([Sachdev-Ye 93](#SachdevYe93)), which was first  discussed in relation to [[AdS-CFT|holography]] in ([Sachdev 10](#Sachdev10)).

From [Maldacena 18](#Maldacena18):

> The SYK model gives us a glimpse into the interior of an [[extremal black hole]]... That's the feature of SYK that I find most interesting... It is a feature this model has, that I think no other model has

## Definition
 {#Definition}

Let $\mathcal{J}_{i j k l}$ be [[random variables]] with [[expectation values]] $E[\mathcal{J}_{i j k l}]=0$ and $E[\mathcal{J}_{i j k l}^2]=\frac{6J^2}{N^3}$. 

The [[Lagrangian density]] defining the SYK model is this:

$$
L = \frac{1}{2} \sum_{i=1}^N \chi_i \partial_t \chi_i - \frac{1}{4!} \sum_{i,j,k,l=1}^N \mathcal{J}_{i j k l} \chi_i \chi_j \chi_k \chi_l
$$

## Related concepts

* [[Jackiw-Teitelboim gravity]]

* [[AdS-CFT in condensed matter physics]]

* [[AdS-CFT correspondence]]

* [[BFSS matrix model]]

## References

### General

Review includes

* {#Sachdev18} [[Subir Sachdev]], _The SYK model_, talk at [Aspen Center for Physics](https://www.aspenphys.org/), 2018 ([pdf](http://qpt.physics.harvard.edu/talks/aspen_tutorial18.pdf))

* {#Rosenhaus19} Vladimir Rosenhaus, _An introduction to the SYK model_,  Journal of Physics A: Mathematical and Theoretical, Volume 52, Number 32 ([arrXiv:1807.03334](https://arxiv.org/abs/1807.03334), [doi:10.1088/1751-8121/ab2ce1](https://iopscience.iop.org/article/10.1088/1751-8121/ab2ce1))

The model is due to

* {#SachdevYe93} [[Subir Sachdev]], Jinwu Ye, _Gapless Spin-Fluid Ground State in a Random Quantum Heisenberg Magnet_, Phys. Rev. Lett. 70:3339, 1993 ([arXiv:cond-mat/9212030](https://arxiv.org/abs/cond-mat/9212030))


* {#Kitaev15} [[Alexei Kitaev]], _A simple model of quantum holography_, Talks at KITP, April 7, 2015 and May 27, 2015. ([part I](#http://online.kitp.ucsb.edu/online/entangled15/kitaev/), [part II](http://online.kitp.ucsb.edu/online/entangled15/kitaev2/))

with further discussion in

* {#MaldacenaStanford16} [[Juan Maldacena]], Douglas Stanford, _Comments on the Sachdev-Ye-Kitaev model_ ([arXiv:1604.07818](https://arxiv.org/abs/1604.07818))


Further developments in

* Biao Lian, S. L. Sondhi, [[Zhenbin Yang]], _The chiral SYK model_ ([arXiv:1906.03308](https://arxiv.org/abs/1906.03308))

* Alexandre Streicher, _SYK Correlators for All Energies_ ([arxiv:1911.10171](https://arxiv.org/abs/1911.10171))


See also 

* Wikipedia, _[SYK model of non-Fermi liquids and black holes](https://en.wikipedia.org/wiki/Subir_Sachdev#SYK_model_of_non-Fermi_liquids_and_black_holes)_


### In AdS/CFT and string theory

Discussion in view of [[AdS-CFT duality]], specifically [[AdS-CFT in condensed matter physics]], includes:

* {#Sachdev10} [[Subir Sachdev]], _Holographic metals and the fractionalized Fermi liquid_, Phys. Rev. Lett. 105:151602, 2010 ([arXiv:1006.3794](https://arxiv.org/abs/1006.3794))

* {#Maldacena18} [[Juan Maldacena]], _Toy models for black holes II_, talk at PiTP 2018 _From QBits to spacetime_ ([recording](https://video.ias.edu/PiTP/2018/0726-JuanMaldacena))

Relation to [[black holes in string theory]] and [[random matrix theory]]:

* Jordan S. Cotler, Guy Gur-Ari, Masanori Hanada, [[Joseph Polchinski]], Phil Saad, [[Stephen Shenker]], [[Douglas Stanford]], Alexandre Streicher, Masaki Tezuka, _Black Holes and Random Matrices_,  JHEP 1705:118, 2017 ([arXiv:1611.04650](https://arxiv.org/abs/1611.04650))


### In terms of weight systems on chord diagrams
 {#ReferencesViaWeightSystems}

Discussion of ([[Lie algebra weight system|Lie algebra]]-)[[weight systems]] on [[chord diagrams]] encoding [[SYK model]] [[single trace observables]]:

(for more see at [[weight systems on chord diagrams in physics]])

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

[[!redirects Sachdev-Ye-Kitaev model]]

[[!redirects SYK model]]
[[!redirects SYK models]]

[[!redirects SYK-model]]
[[!redirects SYK-models]]


