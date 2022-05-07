
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{: toc}

##Idea 

Persistent homology is a [[homology theory]] adapted to a [[computation|computational]] context, for instance, in analysis of large data sets. It keeps track of homology classes which stay 'persistent' when the approximate image of a space gets refined to higher resolutions.  


## More detail

We suppose given a 'data cloud of samples', $P\subset \mathbb{R}^m$, from some space $X$, yielding a [[simplicial complex]] $S_\rho(X)$ for each $\rho \gt 0$ via one of the family of simplicial complex approximation methods that are listed below (TO BE ADDED).  For these, the important idea to retain is that if $\rho \lt \rho^\prime$, then 

$$S_\rho(X) \hookrightarrow S_{\rho^\prime}(X),$$

so we get a 'filtration structure' on the complex.

The idea of *persistent homology* is to look for features that persist for some range of parameter values.  Typically a feature, such as a hole, will initially not be observed, then will appear, and after a range of values of the parameter it will disappear again. A typical feature will be a [[Betti number]] of the complex, $S_\rho(X)$, which then will vary with the parameter $\rho$.



## Software

One can compute intervals for homological features algorithmically over field coefficients and software packages are available for this purpose. See for instance [Perseus](http://www.sas.upenn.edu/~vnanda/perseus). The principal algorithm is based on bringing the filtered complex to its **canonical form** by upper-triangular matrices from ([Barannikov1994, §2.1] (https://www.researchgate.net/profile/Serguei_Barannikov/publication/267672645_The_Framed_Morse_complex_and_its_invariants/links/5970e947458515fa8de6e724/The-Framed-Morse-complex-and-its-invariants.pdf))

## Related concepts

* [[persistence module]]

* [[well group]]

* [[topological data analysis]]

* [[computational topology]]


## References

### General

Introduction and survey




* [[Robert Ghrist]], _Barcodes: The Persistent Topology of Data_, Bull. Amer. Math. Soc. 45 (2008), 61-75 ([doi:10.1090/S0273-0979-07-01191-3](https://doi.org/10.1090/S0273-0979-07-01191-3), [pdf](https://www.math.upenn.edu/~ghrist/preprints/barcodes.pdf))

* [[Gunnar Carlsson]], _Topology and data_, Bull. Amer. Math. Soc. 46 (2009), no. 2, 255-308 ([doi:10.1090/S0273-0979-09-01249-X](https://doi.org/10.1090/S0273-0979-09-01249-X))

* [[Gunnar Carlsson]], _Persistent Homology and Applied Homotopy Theory_, in: [[Handbook of Homotopy Theory]], CRC Press, 2019 ([arXiv:2004.00738](https://arxiv.org/abs/2004.00738))


See also

* [[Tim Porter]], _Observing Information: Applied Computational Topology_ 2008 ([[ACT-OIT.pdf|Slides:file]])

* Bei Wang, _Topological Data Analysis_, Lecture 2010 ([[WangTopologicalDataAnalysis.pdf:file]])

* Wikipedia, _[Persistent homology](https://en.wikipedia.org/wiki/Persistent_homology)_



Bar-codes were discovered under the name of _canonical forms invariants of filtered complexes_ in 

*  Serguei Barannikov, _Framed Morse complex and its invariants_, [pdf](https://www.researchgate.net/profile/Serguei_Barannikov/publication/267672645_The_Framed_Morse_complex_and_its_invariants/links/5970e947458515fa8de6e724/The-Framed-Morse-complex-and-its-invariants.pdf) Advances in Soviet Mathematics __21__ 93–115 (1994)

See also

* A. Zomorodian, [[Gunnar Carlsson]], _Computing persistent homology_, Discrete Comput. Geom. __33__, 249&#8211;274 (2005) ([doi:10.1007/s00454-004-1146-y](https://doi.org/10.1007/s00454-004-1146-y))

* [[Gunnar Carlsson]], V. de Silva, _Zigzag persistence_ ([arXiv:0812.0197](http://arxiv.org/abs/0812.0197))


* Robert J. Adler, Omer Bobrowski, Matthew S. Borman, Eliran Subag, Shmuel Weinberger, _Persistent homology for random fields and complexes_ Institute of Mathematical Statistics Collections __6__:124&#8211;143, 2010 ([arxiv/1003.1001](http://arxiv.org/abs/1003.1001))

* Pawe&#322; D&#322;otko, Hubert Wagner, _Computing homology and persistent homology using iterated Morse decomposition_ ([arxiv/1210.1429](http://arxiv.org/abs/1210.1429))

* [[Robert MacPherson]], Benjamin Schweinhart, _Measuring shape with topology_, J. Math. Phys. __53__, 073516 (2012) ([doi:10.1063/1.4737391](http://dx.doi.org/10.1063/1.4737391))

* Robert J. Adler, Omer Bobrowski, Shmuel Weinberger, _Crackle: the persistent homology of noise_, [arxiv/1301.1466](http://arxiv.org/abs/1301.1466)

*  D. Le Peutrec, N. Nier, C. Viterbo, _Precise Arrhenius Law for p-forms: The Witten Laplacian and Morse–Barannikov Complex_, Annales Henri Poincaré __14__ (3): 567–610 (2013) [doi](https://10.1007/s00023-012-0193-9)

* Ulrich Bauer, Michael Kerber, Jan Reininghaus, _Clear and compress: computing persistent homology in chunks_, [arxiv/1303.0477](http://arxiv.org/abs/1303.0477)

* Sara Kališnik, _Persistent homology and duality_, 2013 ([pdf](http://www.matknjiz.si/doktorati/2013/Kalisnik-14521-4.pdf), [[KalisnikPersistent.pdf:file]])

* Francisco Belch&#237; Guillam&#243;n, Aniceto Murillo Mas, _A-infinity persistence_, [arxiv/1403.2395](http://arxiv.org/abs/1403.2395)

* Jo&#227;o Pita Costa, Mikael Vejdemo Johansson, Primo&#382; &#352;kraba, _Variable sets over an algebra of lifetimes: a contribution of lattice theory to the study of computational topology_, [arxiv/1409.8613](http://arxiv.org/abs/1409.8613)

* Genki Kusano, Kenji Fukumizu, Yasuaki Hiraoka, _Persistence weighted Gaussian kernel for topological data analysis_, [arxiv/1601.01741](http://arxiv.org/abs/1601.01741)

* Heather A. Harrington, Nina Otter, Hal Schenck, [[Ulrike Tillmann]], _Stratifying multiparameter persistent homology_, [arxiv/1708.07390](https://arxiv.org/abs/1708.07390)

* H. Edelsbrunner, D. Morozov, _Persistent homology: theory and practice_ [pdf](http://mrzv.org/publications/persistent-homology-theory-practice/ecm)

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