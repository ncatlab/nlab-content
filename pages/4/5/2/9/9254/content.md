
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--



# Topological data analysis
* table of contents
{: toc}

## Idea

\begin{imagefromfile}
    "file_name": "CoCyclesInDataSets-220522.jpg",
    "float": "right",
    "width": 420,
    "unit": "px",
    "margin": {
        "top": -60,
        "bottom": 0,
        "right": 0, 
        "left": 20
    }
\end{imagefromfile}

*Topological data analysis* (TDA) is *qualitative* [[data analysis]] with tools from [[topology]], in particular with tools from *[[algebraic topology]]*. 

This notably includes tools from [[ordinary homology|ordinary]] ([[cohomology theory|co-]])[[homology]]-theory, which in the guise of *[[persistent homology]]* has become the signature method in TDA; but it also includes more general tools of [[homotopy theory]] and [[differential topology]], which have more recently found their way into TDA in the guise of *[[persistent homotopy theory]]* and *[[persistent cohomotopy theory]]*.

Typically, TDA deals with *large* data sets modeled as ([[subsets]] of) [[topological spaces]]. Collections of *data points* appear as *[[cycles]]* in the topological space of data, and *values* of data appear as *[[cocycles]]*.
$\;\;$(graphics from [[schreiber:New Foundations for TDA -- Cohomotopy|SS22]])


### Strategy of persistent topology/homotopy
 {#StrategyOfPersistentHomology}


The strategy of [[persistent homology|persistent homology]]/[[persistent homotopy|homotopy]] in TDA  is to see which chunks ([[subspaces]]) of the data appear to be ([[n-connected topological space|higher]]) [[connected topological space|connected]] when viewed at some resolution (technically: at some [[filtered topological space|filter stage]]) and how much these apparent chunks *persist* as the resolution changes. 
This may be recorded in *[[persistence diagrams]]* (also known as "[[barcodes]]"). The fundamental theorem of the field -- the *[[stability of persistence diagrams|stability theorem]]* -- says that [[persistence diagram|persistent]] ([[cocycle|co-]])[[cycle]]-[[equivalence class|classes]] are indeed a good invariant of data, in that they remain stable under small perturbations of the initial data (e.g. under [[noise]], uncertainty, measurement errors, etc.).

> (usual schematic depiction of a [[Vietoris-Rips complex]] goes here)

The idea then is that those  ([[cocycle|co-]])[[cycles]] which persist for longer (appear as longer bars in the [[barcode]]) reflect relevant structure hidden in the (large) data set. However, it is often unclear (and certainly not part of the mathematical theory) what the significance or *meaning* of persistent cycles is for the practical problem of interpreting data.

### Strategy of persistent cohomology/cohomotopy
 {#StrategyOfPersistentCohomotopy}

\begin{imagefromfile}
    "file_name": "IndicatorFunctionOnData-220523.jpg",
    "float": "right",
    "width": 420,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 0,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

In contrast, [[persistent cohomotopy]] in TDA is the effective answer to a concrete and common question in [[data analysis]]: 

Given a large-[[dimension of a CW-complex|dimensional]] [[topological space|space]] of data, and a small [[natural number|number]] $n$ of ([[real number|real]]) indicator values assigned to each data point with given precision $1/r$, *does _any_ data meet a prescribed target indication precisely?*


A [fundamental theorem](persistent+cohomotopy#GuaranteeThatSolutionsExist) of [[persistent Cohomotopy]] ([Franek & Krčál 2018](persistent+cohomotopy#FranekKrcal18), [2017, p. 5](persistent+cohomotopy#FranekKrcal17), see [here](persistent+cohomotopy#GuaranteeThatSolutionsExist)) shows that (1.) the answer to this question is detected by a certain [[Cohomotopy]]-class and (2.) in a fair range of dimensions, this Cohomotopy class is provably [[computability|computable]], hence the above question is effectively [[decidability|decidable]]. (fig. from [[schreiber:New Foundations for TDA -- Cohomotopy|SS22]])


(Alternatively, with tools from [[persistent homology theory]] an answer to this question is given by the method of *[[well groups]]*, but (1.) it is known that well groups are in general too coarse to provide a complete answer and (2.) despite effort it remains unknown if well groups are actually [[computability|computable]] in relevant cases, see [Franek & Krčál 2016](persistent+cohomotopy#FranekKrcal16).)

If the [[topological space]] $X$ of data may be assumed to be a [[smooth manifold]] (indeed, in typical examples $X$ is itself a large-dimensional [[Cartesian space]]) then persistent cohomotopy may be understood dually via [[Pontryagin's theorem]] as characterizing [[iso-hypersurfaces]] of data (close to a given target indicator) by [[framed cobordism|framed]] [[cobordism theory]] ([Franek & Krčál 2017, p. 8-9](persistent+cohomotopy#FranekKrcal17)). The full implications of this relation for topological data analysis remain to be explored.
  




## Related concepts

* [[computational topology]]

* [[machine learning]]



## References

### General

* [[Gunnar Carlsson]], _Topology and data_, Bull. Amer. Math. Soc. 46 (2009), 255-308 ([doi:10.1090/S0273-0979-09-01249-X](https://doi.org/10.1090/S0273-0979-09-01249-X))

* Afra Zomorodian, _Topological data analysis_, In: _Advances in Applied and Computational Topology_, Proc. Symp. Applied Math vol 70, 2011 ([ams:psapm-70](https://bookstore.ams.org/psapm-70))

* [[Gunnar Carlsson]], _Persistent Homology and Applied Homotopy Theory_, in: [[Handbook of Homotopy Theory]], CRC Press, 2019 ([arXiv:2004.00738](https://arxiv.org/abs/2004.00738))


See also 

* Wikipedia, _[Topological data analysis](http://en.wikipedia.org/wiki/Topological_data_analysis)_

Relation to [[quantum computing]]:

* He-Liang Huang, Xi-Lin Wang, Peter P. Rohde, Yi-Han Luo, You-Wei Zhao, Chang Liu, Li Li, Nai-Le Liu, Chao-Yang Lu, Jian-Wei Pan, _Demonstration of Topological Data Analysis on a Quantum Processor_, Optica 5(2),193(2018) ([arXiv:1801.06316](https://arxiv.org/abs/1801.06316)) 

### Applications

Application of [[topological data analysis]] ([[persistent homology]]) to 

analysis of [[quasicrystals]]:

* Pavlo Solokha et al., *New Quasicrystal Approximant in the Sc–Pd System: From Topological Data Mining to the Bench*, Chem. Mater. 2020, 32, 3, 1064–1079 ([doi:10.1021/acs.chemmater.9b03767](https://doi.org/10.1021/acs.chemmater.9b03767))


analysis of [[cosmological structure formation]]:

* Matteo Biagetti, [[Alex Cole]], [[Gary Shiu]], _The Persistence of Large Scale Structures I: Primordial non-Gaussianity_ ([arXiv:2009.04819](https://arxiv.org/abs/2009.04819))

to analysis of [[phase transitions]]:

* [[Alex Cole]], Gregory J. Loges, [[Gary Shiu]], _Quantitative and Interpretable Order Parameters for Phase Transitions from Persistent Homology_ ([arXiv:2009.14231](https://arxiv.org/abs/2009.14231))



[[!include cohomotopy in topological data analysis -- references]]



[[!redirects topological data analysis]]

[[!redirects TDA]]

