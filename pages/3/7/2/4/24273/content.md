
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


#Contents#
* table of contents
{:toc}

## Idea


In *topological machine learning* one tries to combine methods from both [[topological data analysis]] and [[machine learning]] for application to [[data analysis]].

A popular approach (originating around [RHBK15](#RHBK15), [KHNL15](#KHNL15)) is to use [[persistent homology]] as a pre-processing stage and train [[neural networks]] not on full data sets, but on their [[persistence diagram]]/[[barcode]] (which may  still be a large amount of data), by making these amenable to [[kernel methods]].

## References

On feeding [[persistence diagrams]] into [[machine learning]]-algorithms by equipping them with [[kernel method|kernels]]:

* {#RHBK15} Jan Reininghaus, [[Stefan Huber]], Ulrich Bauer, Roland Kwitt, *A Stable Multi-Scale Kernel for Topological Machine Learning*, NIPS'15: Proceedings of the 28th International Conference on Neural Information Processing System, **2** (2015 3070–3078  $[$[arXiv:1412.6821](https://arxiv.org/abs/1412.6821)$]$

* {#KHNL15} Roland Kwitt, [[Stefan Huber]], Marc Niethammer, Weili Lin, [[Ulrich Bauer]], *Statistical Topological Data Analysis -- A Kernel Perspective*, in: *Advances in Neural Information Processing Systems*  (NIPS 2015) $[$[ISBN:9781510825024](https://proceedings.neurips.cc/paper/2015), [doi:10.5555/2969442.2969582](https://dl.acm.org/doi/10.5555/2969442.2969582)$]$


* {#RSL} [[Bastian Rieck]], Filip Sadlo, Heike Leitte, *Topological Machine Learning with Persistence Indicator Functions*,  In: *Topological Methods in Data Analysis and Visualization V* TopoInVis (2017) 87-101 Mathematics and Visualization. Springer, $[$[arXiv:1907.13496](https://arxiv.org/abs/1907.13496), [doi:10.1007/978-3-030-43036-8_6](https://doi.org/10.1007/978-3-030-43036-8_6)$]$

* Raphael Reinauer, Matteo Caorsi, Nicolas Berkouk, *Persformer: A Transformer Architecture for Topological Machine Learning* $[$[arXiv:2112.15210](https://arxiv.org/abs/2112.15210)$]$



Review:

* Felix Hensel, Michael Moor, [[Bastian Rieck]], *A Survey of Topological Machine Learning Methods*, Front. Artif. Intell., **26** (2021) $[$[doi:10.3389/frai.2021.681108](https://doi.org/10.3389/frai.2021.681108), [[HenselMoorRieck-TopologicalMachineLearning.pdf:file]]$]$

See also:

* [[Stefan Huber]], *Topological machine learning* ([webpage](https://www.sthu.org/research/topmachinelearning/))

