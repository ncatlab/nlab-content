
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{: toc}

## Idea 
 {#Idea}

*Persistent homology* is the study of [[sequences]] of [[linear maps]] between [[vector spaces]]

$$
  \cdots 
   \xrightarrow{\;}
  V_i 
    \xrightarrow{\phi_i} 
  V_{i + 1}
    \xrightarrow{\phi_{i + 1}}
  V_{i + 2}
    \xrightarrow{\phi_{i + 2}}
  \cdots
  \,,
$$

under the aspect of which elements ([[vectors]]) $v_i \in V_i$ "persist" (ie. remain non-[[zero]]) under which number of iterations of these linear maps. One then refers to these sequences as *[[persistence modules]]* (hence a [[concept with an attitude]]).

In the archetypical applications of interest, these vector spaces are [[ordinary homology|ordinary]] [[homology groups]] $V_i \,=\, H_n(X_i)$ (over a given [[ground field]]) of [[topological spaces]] $X_i$ which themselves are stages 

$$ 
  \cdots \hookrightarrow X_i \xhookrightarrow{\iota_i} X_{i+ 1} \xhookrightarrow{\iota_{i + 1}} X_{i + 2} \xhookrightarrow{} \cdots \xhookrightarrow{x} X
$$ 

of a [[filtered topological space]], and one is interested in deducing "relevant" properties of this filtration by finding those [[homology]] [[cycles]] which stand out as persisting over a large range of steps.

This question, in turn, has been motivated from problems in [[topological data analysis]], where sequences of spaces $X_i$ arise as coarse-grained versions, at varying stages of resolution $i$ (say as measured in some ambient [[metric space]]) of a given [[discrete space|discrete set]] of data points. In this example, the more the homology cycles *persist* as the resolution $i$ is varied, the more one is willing to assume that they signal relevant structure that is hidden in the data, while cycles that do not persist for long would be interpreted as irrelevant noise effects. 

Of course, these simple basic ideas may be (and still are being) refined and generalized in a number of ways. 

A particularly important generalization turns out to be that from [[linear order|directed 1-dimensional]] sequences of linear maps to arbitrary [[zigzags]] of these, then called *[[zigzag persistence modules]]*. Again, this is naturally motivated in the case of homology groups of a [[filtered topological space]], where one may form the sequence of [[cospans]] 

$$
  \cdots \leftarrow X_i \to X_i \cup X_{i + 1} \leftarrow X_{i + 1} \to X_{i + 1} \cup X_{i + 2} \leftarrow \cdots
$$ 

of inclusions into [[unions]] of consecutive filter stages. 

Seen in this generality,  the notion of finite-length [[zigzag persistence modules]] happens to coincide with that of [[ADE classification|A-type]] [[quiver representations]], a fruitful coincidence that serves to bring well-developed tools of [[quiver]]-[[representation theory]] to bear on persistent homology theory.

In particular, the founding result of [[quiver representation theory]] -- namely  [[Gabriel's theorem]] -- serves, in hindsight, to establish the formal notion of persistence itself: The theorem implies (see [there](Gabriel's+theorem#ATypeQuivers)) that every ([[zigzag persistence|zigzag]]) [[persistence module]] is the [[direct sum]] of *interval modules* $I_{a,b}$, namely those which are [[zero]] except over the [[interval]] $i \in [a,b]$, where they are given by the [[identity]] on the [[ground field]] (the latter regarded as the [[dimension of a vector space|1-dimensional]] [[vector space]] over itself). 

Hence the canonical [[linear basis]]-elements of these interval modules $I_{a,b}$ are exactly the persistent cycles which *persist from $a$ to $b$*, so that [[Gabriel's theorem]] guarantees that any (zigzag) persistence module may be completely decomposed into (the [[linear span]] of) these elements. Numerous generalizations of this theorem exist (taking it out of the context of [[quiver]]-theory) and show that this state of affairs remains true notably when one allows the indices $i$ to be taken from sets with [[infinite set|infinite]] [[cardinality]].

In other words, the [[isomorphism class]] of any (zigzag) persistence module is equivalently encoded in a [[multiset]] of intervals. These multisets are known as *[[barcodes]]* (due to the evident graphical representation of a multiset of intervals) or as *[[persistence diagrams]]* (the latter usually when $[a,b]$ is regarded as a point $(a,b) \in \mathbb{R}^2$ in the [[plane]]). These [[persistence diagrams]] are meant to be the [[invariants]] of interest in persistent homology theory. 

Besides the foundational theorem that guarantees the existence of persistence diagrams, the fundamental theorem of persistent homology has come to be the *[[stability of persistence diagrams|stability theorem]]*: This says that [[persistence diagrams]] are indeed *useful invariants*, namely in that they remain "stable" under small variations (think: noise, measurement errors) of input data such as the above topological filter stages $X_i$. 

For example, as one changes a little the [[metric]] with which to produce the topological space $X_i$ of coarse grained data at resolution stage $i$, the homology groups $H(X_i)$ may change dramatically, but the [[stability of persistence diagrams|stability theorem]] ensures that effect on the [[persistence diagram]] remains small. 

It is in this way that persistent homology may be used, in particular, to produce robust invariants of noisy data, which has made it the archetypical tool in [[topological data analysis]].

\linebreak




## Properties 
 {#Properties}


* [[stability of persistence diagrams]]

  ([Cohen-Steiner, Edelsbrunner & Harer 2007](#CohenSteinerEdelsbrunnerHarer07))

* [[diamond principle]]

  (Carlsson et al.)

## Software

One can compute intervals for homological features algorithmically over field coefficients and software packages are available for this purpose. See for instance [Perseus](http://www.sas.upenn.edu/~vnanda/perseus). The principal algorithm is based on bringing the filtered complex to its **canonical form** by upper-triangular matrices from ([Barannikov1994, §2.1] (https://www.researchgate.net/profile/Serguei_Barannikov/publication/267672645_The_Framed_Morse_complex_and_its_invariants/links/5970e947458515fa8de6e724/The-Framed-Morse-complex-and-its-invariants.pdf))

## Related concepts

* [[persistence module]]

* [[persistence diagram]]

* [[well group]]

* [[topological data analysis]]

* [[persistent homotopy theory]]

* [[computational topology]]

* [[quiver representation]], [[Gabriel's theorem]]

## References

### General

Introduction and survey:

* [[Robert Ghrist]], _Barcodes: The Persistent Topology of Data_, Bull. Amer. Math. Soc. 45 (2008), 61-75 ([doi:10.1090/S0273-0979-07-01191-3](https://doi.org/10.1090/S0273-0979-07-01191-3), [pdf](https://www.math.upenn.edu/~ghrist/preprints/barcodes.pdf))

* [[Herbert Edelsbrunner]], [[John Harer]], *Persistent homology -- a survey*, in: *Surveys on Discrete and Computational Geometry: Twenty Years Later*, Contemporary Mathematics *453* (2008) $[$[doi:10.1090/conm/453](http://dx.doi.org/10.1090/conm/453)$]$

* [[Gunnar Carlsson]], *Topology and data*, Bull. Amer. Math. Soc. 46 (2009), no. 2, 255-308 $[$[doi:10.1090/S0273-0979-09-01249-X](https://doi.org/10.1090/S0273-0979-09-01249-X)$]$

* [[Herbert Edelsbrunner]], [[Dmitriy Morozov]], *Persistent homology: theory and practice*, in: *European Congress of Mathematics Kraków, 2–7 July, 2012* EMS $[$[doi:10.4171/120-1/3](https://www.ems-ph.org/books/show_abstract.php?proj_nr=170&vol=1&rank=3), [pdf](http://mrzv.org/publications/persistent-homology-theory-practice/ecm)$]$

Review with emphasis of [[zigzag persistence]] with relation to [[quiver representation theory]]:

* [[Steve Y. Oudot]], *Persistence Theory: From Quiver Representations to Data Analysis*, Mathematical Surveys and Monographs **209** AMS (2015) $[$[pdf](https://geometrica.saclay.inria.fr/team/Steve.Oudot/books/o-pt-fqrtda-15/surv-209.pdf), [ISBN:978-1-4704-3443-4](https://bookstore.ams.org/surv-209/)$]$

* [[Gunnar Carlsson]], *Persistent Homology and Applied Homotopy Theory*, in: [[Handbook of Homotopy Theory]], CRC Press (2019) $[$[arXiv:2004.00738](https://arxiv.org/abs/2004.00738), [doi:10.1201/9781351251624](https://doi.org/10.1201/9781351251624)$]$


See also

* [[Tim Porter]], _Observing Information: Applied Computational Topology_ 2008 ([[ACT-OIT.pdf|Slides:file]])

* Bei Wang, _Topological Data Analysis_, Lecture 2010 ([[WangTopologicalDataAnalysis.pdf:file]])

* Wikipedia, _[Persistent homology](https://en.wikipedia.org/wiki/Persistent_homology)_

The concept of persistent homology originates around:

* [[Herbert Edelsbrunner]], D. Letscher, and A. Zomorodian, *Topological persistence and simplification*, Discrete & Computational Geometry, **28** (2002) 511–533 $[$[doi:10.1007/s00454-002-2885-2](https://doi.org/10.1007/s00454-002-2885-2)$]$

The generalization to "[[zigzag persistence]]" with relation to [[ADE-classification|A-type]] [[quiver representation]]-theory is due to:

* {#CarlssonDeSilva10} [[Gunnar Carlsson]], [[Vin de Silva]], *Zigzag Persistence*, Found Comput Math **10** (2010) 367–405 $[$[arXiv:0812.0197](https://arxiv.org/abs/0812.0197), [doi:10.1007/s10208-010-9066-0](https://doi.org/10.1007/s10208-010-9066-0)$]$

and specifically for [[level sets]]:

* [[Gunnar Carlsson]], [[Vin de Silva]], [[Dmitriy Morozov]], *Zigzag persistent homology and real-valued functions*, in: *SCG '09: Proceedings of the twenty-fifth annual symposium on Computational geometry (2009) 247–256 $[$[doi:10.1145/1542362.1542408](https://doi.org/10.1145/1542362.1542408)$]$

* [[Gunnar Carlsson]], [[Vin de Silva]], [[Sara Kališnik]], [[Dmitriy Morozov]], *Parametrized Homology via Zigzag Persistence*, Algebr. Geom. Topol. **19** (2019) 657-700 $[$[arXiv:1604.03596](https://arxiv.org/abs/1604.03596), [doi:10.2140/agt.2019.19.657](https://doi.org/10.2140/agt.2019.19.657)$]$

The [[stability of persistence diagrams|stability result]] is due to:

* {#CohenSteinerEdelsbrunnerHarer07} [[David Cohen-Steiner]], [[Herbert Edelsbrunner]], [[John Harer]], *Stability of Persistence Diagrams*, Discrete & Computational Geometry **37** (2007) 103–120 $[$[doi:10.1007/s00454-006-1276-5](https://doi.org/10.1007/s00454-006-1276-5)$]$

Bar-codes were introduced under the name of *canonical forms invariants of filtered complexes* in 

*  Serguei Barannikov, _Framed Morse complex and its invariants_, [pdf](https://www.researchgate.net/profile/Serguei_Barannikov/publication/267672645_The_Framed_Morse_complex_and_its_invariants/links/5970e947458515fa8de6e724/The-Framed-Morse-complex-and-its-invariants.pdf) Advances in Soviet Mathematics __21__ 93–115 (1994)

See also

* A. Zomorodian, [[Gunnar Carlsson]], *Computing persistent homology*, Discrete Comput. Geom. __33__, 249&#8211;274 (2005) ([doi:10.1007/s00454-004-1146-y](https://doi.org/10.1007/s00454-004-1146-y))

* [[Gunnar Carlsson]], V. de Silva, _Zigzag persistence_ ([arXiv:0812.0197](http://arxiv.org/abs/0812.0197))


* Robert J. Adler, Omer Bobrowski, Matthew S. Borman, Eliran Subag, Shmuel Weinberger, _Persistent homology for random fields and complexes_ Institute of Mathematical Statistics Collections __6__:124&#8211;143, 2010 ([arxiv/1003.1001](http://arxiv.org/abs/1003.1001))

* Pawe&#322; D&#322;otko, Hubert Wagner, _Computing homology and persistent homology using iterated Morse decomposition_ ([arxiv/1210.1429](http://arxiv.org/abs/1210.1429))

* [[Robert MacPherson]], Benjamin Schweinhart, _Measuring shape with topology_, J. Math. Phys. __53__, 073516 (2012) ([doi:10.1063/1.4737391](http://dx.doi.org/10.1063/1.4737391))

* Robert J. Adler, Omer Bobrowski, Shmuel Weinberger, _Crackle: the persistent homology of noise_, [arxiv/1301.1466](http://arxiv.org/abs/1301.1466)

*  D. Le Peutrec, N. Nier, C. Viterbo, _Precise Arrhenius Law for p-forms: The Witten Laplacian and Morse–Barannikov Complex_, Annales Henri Poincaré __14__ (3): 567–610 (2013) [doi](https://10.1007/s00023-012-0193-9)

* Ulrich Bauer, Michael Kerber, Jan Reininghaus, _Clear and compress: computing persistent homology in chunks_, [arxiv/1303.0477](http://arxiv.org/abs/1303.0477)

* [[Sara Kališnik]], _Persistent homology and duality_, 2013 ([pdf](http://www.matknjiz.si/doktorati/2013/Kalisnik-14521-4.pdf), [[KalisnikPersistent.pdf:file]])

* Francisco Belch&#237; Guillam&#243;n, Aniceto Murillo Mas, _A-infinity persistence_, [arxiv/1403.2395](http://arxiv.org/abs/1403.2395)

* Jo&#227;o Pita Costa, Mikael Vejdemo Johansson, Primo&#382; &#352;kraba, _Variable sets over an algebra of lifetimes: a contribution of lattice theory to the study of computational topology_, [arxiv/1409.8613](http://arxiv.org/abs/1409.8613)

* Genki Kusano, Kenji Fukumizu, Yasuaki Hiraoka, _Persistence weighted Gaussian kernel for topological data analysis_, [arxiv/1601.01741](http://arxiv.org/abs/1601.01741)

* Heather A. Harrington, Nina Otter, Hal Schenck, [[Ulrike Tillmann]], _Stratifying multiparameter persistent homology_, [arxiv/1708.07390](https://arxiv.org/abs/1708.07390)

* {#BerkoukGinotOudot19} [[Nicolas Berkouk]], [[Grégory Ginot]], [[Steve Oudot]], *Level-sets persistence and sheaf theory* $[$[arXiv:1907.09759](https://arxiv.org/abs/1907.09759)$]$



The following paper uses persistent homology to single out features relevant for training [[neural networks]]:

* Jean-Baptiste Bardin, Gard Spreemann, [[Kathryn Hess]], _Topological exploration of artificial neuronal network dynamics_, [arxiv/1810.01747](https://arxiv.org/abs/1810.01747)

Application to [[topological data analysis]] in [[cosmological structure formation]]:

* Matteo Biagetti, [[Alex Cole]], [[Gary Shiu]], _The Persistence of Large Scale Structures I: Primordial non-Gaussianity_ ([arXiv:2009.04819](https://arxiv.org/abs/2009.04819))

Application of [[topological data analysis]] ([[persistent homology]]) to analysis of [[phase transitions]]:

* [[Alex Cole]], Gregory J. Loges, [[Gary Shiu]], _Quantitative and Interpretable Order Parameters for Phase Transitions from Persistent Homology_ ([arXiv:2009.14231](https://arxiv.org/abs/2009.14231))



[[!include cohomotopy in topological data analysis -- references]]



### Further variants

See also

* [[Robert MacPherson]], Amit Patel, _Persistent Local Systems_ ([arXiv:1805.02539](https://arxiv.org/abs/1805.02539))



category: topology, applications

[[!redirects persistent homology]]
[[!redirects persistent homology theory]]

[[!redirects persistence module]]
[[!redirects persistence modules]]

