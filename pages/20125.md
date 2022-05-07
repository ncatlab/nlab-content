

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Solid state physics
+-- {: .hide}
[[!include solid state physics -- contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

The term _tensor network_ has become popular in [[quantum physics]] for essentially what in [[mathematical physics]] is known as _[[Penrose notation]]_ and in [[monoidal category|monoidal]] [[category theory]] is referred to as _[[string diagrams]]_ (see [BCJ 10](#BCJ10) for a bilingual account).


The term rose to prominence in [[quantum physics]] partly with discussion of [[finite quantum mechanics in terms of dagger-compact categories]] but mainly via its use for representing highly [[entangled states]] in the  discussion of [[renormalization]] of [[non-perturbative effects]] in [[solid state physics]] ([Swingle 09](#Swingle09), [Swingle 13](#Swingle13)) and the resulting discovery of the relation to [[holographic entanglement entropy]] and thus to the [[AdS/CFT correspondence]].

In this context, a _tensor network_ is a _[[string diagram]] [[concept with an attitude|with an attitude]], in that it is (just) a [[string diagram]] (typically regarded in the [[monoidal category]] of [[finite-dimensional vector spaces]], but possibly also in [[super vector spaces]] etc.), but with: 

1. the [[tensor product]] of all its external [[objects]] regarded as a [[space of states]] of a [[quantum system]];

1. the [[element]] in that [[tensor product]] defined by the string diagram regarded as a [[state]] ([[wave function]]) of that quantum system.

For instance, if $\mathfrak{g}$ is a [[metric Lie algebra]] (with [[string diagram]]-notation as shown [there](metric+Lie+algebra#Definition)), and with each [[tensor product]]-power of its [[dual vector space]] regarded as a [[Hilbert space]], hence as a [[space of quantum states]], via the given [[inner product]] on $\mathfrak{g}$, then an example of a _[[tree tensor network state]]_ is the following:

<center>
<img src="https://ncatlab.org/nlab/files/TensorNetworkStateFromMetricLieAlgebra.jpg" width="300">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]


The [[quantum states]] arising this way are generically highly [[entangled state|entangled]]: roughly they are the more entangled the more [[vertices]] there are in the corresponding tensor network.

The following is an example of what is called a [[matrix product state]]:

<center>
<img src="https://ncatlab.org/nlab/files/MatrixProductStateFromMetricLieAlgebra.jpg" width="300">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]


The [[tree tensor network states]] in the form of [[Bruhat-Tits trees]] play a special role in the [[AdS/CFT correspondence]], either as

1. a kind of [[lattice QFT]]-approximation to an actual [[boundary field theory|boundary]] [[CFT]] [[quantum state]], 

1. as the [[p-adic geometry|p-adic geometric]] incarnation of [[anti de Sitter spacetime]] in the [[p-adic AdS/CFT correspondence]],

1. as a reflection of actual [[crystal]]-site quantum states in [[AdS/CFT in solid state physics]]:

<center>
<img src="https://ncatlab.org/nlab/files/BruhatTitsTreeTensorNetworkStateFromMetricLie.jpg" width="300">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

(As in [HMSS 16](p-adic+AdS/CFT+correspondence#HMSS16), [HLM 19](p-adic+AdS/CFT+correspondence#HLM19). But  maybe one wants the Poincar&eacute;-dual networks, instead, as in [HMPS 18](p-adic+AdS/CFT+correspondence#HMPS18)?)

For [[tensor network states]] dual to tesselations of [[hyperbolic space]] and made from [[perfect tensors]] one finds that the [[entanglement entropy]] of the tensor subspace associated with an [[interval]] on the [[boundary]] becomes proportional, for large number of [[vertices]], to the [[hyperbolic space|hyperbolic]] bulk boundary [[length]] of the segment of the tree network that ends on this interval, according to the [[Ryu-Takayanagi formula]] ([PYHP 15, Theorem 2](#PYHP15)). Hence one speaks of _[[holographic entanglement entropy]]_. For more on this see [below](#ForHolographicEntanglementEntropy).


General tensor network states are mixtures of the above examples. For instance in ... is the suggestion that [[BTZ black holes]] are encoded by networks that look like [[Bruhat-Tits trees]] towards the boundaries and like [[matrix product states]] towards the interior:

<center>
<img src="https://ncatlab.org/nlab/files/BTZTensorNetworksStateFromLieAlgebra.jpg" width="350">
</center>

(As in [ESZ 19](p-adic+AdS/CFT+correspondence#ESZ19).)

\linebreak

## For holographic entanglement entropy
 {#ForHolographicEntanglementEntropy}

>  under construction

Appearance in [[renormalization]]:

<center>
<img src="https://ncatlab.org/nlab/files/SwingleRenormalizationTensorNetwork.jpg" width="600"></a>
</center>


> from [Swingle 09](#Swingle09)


Application to [[holographic entanglement entropy]] (...)

<center>
<img src="https://ncatlab.org/nlab/files/BlackHoleTensorNetwork.jpg" width="500"></a>
</center>

> graphics grabbed from [Harlow 18](#Harlow18), see at *[[HaPPY code]]*

<center>
<img src="https://ncatlab.org/nlab/files/AdSRindlerTensorNetwork.jpg" width="500"></a>
</center>

> graphics grabbed from [Harlow 18](#Harlow18), see at *[[HaPPY code]]*

In this context the [[Ryu-Takayanagi formula]] for [[holographic entanglement entropy]] has an exact proof [PYHP 15, Theorem 2](#PYHP15).

## Examples

* [[matrix product state]]

* [[tree tensor network state]]

* [[MERA state]]



## Related concepts

* [[string diagram]]/[[Penrose notation]]

* [[finite quantum mechanics in terms of dagger-compact categories]]

* [[quantum many-body physics]], [[condensed matter physics]]

* [[quantum computing]], [[quantum information theory]]

  [[quantum error correction]]

* [[tensor]], [[tensor product]], [[tensor category]]

* [[neural network]]

[[!include states and observables -- content]]

## References

### General

Review and exposition:


* {#BCJ10} [[Jacob Biamonte]], Stephen R. Clark, Dieter Jaksch, _Categorical Tensor Network States_, AIP Advances 1(4), 042172 (2011) ([arXiv:1012.0531](https://arxiv.org/abs/1012.0531))

* [[Roman Orus]], _A Practical Introduction to Tensor Networks: Matrix Product States and Projected Entangled Pair States_, 	Annals of Physics 349 (2014) 117-158  ([arXiv:1306.2164](https://arxiv.org/abs/1306.2164))

* [[Jens Eisert]], _Entanglement and tensor network states_, Modeling and Simulation 3, 520 (2013) ([arXiv:1308.3318](https://arxiv.org/abs/1308.3318))


* [[Jacob Biamonte]], Ville Bergholm, _Tensor Networks in a Nutshell_, Contemporary Physics ([arxiv:1708.00006](https://arxiv.org/abs/1708.00006))

* Shi-Ju Ran, Emanuele Tirrito, Cheng Peng, Xi Chen, [[Luca Tagliacozzo]], Gang Su, Maciej Lewenstein, _Tensor Network Contractions -- Methods and Applications to Quantum Many-Body Systems_, Lecture Notes in Physics, Springer (2020) ([arXiv:1708.09213](https://arxiv.org/abs/1708.09213), [doi:10.1007/978-3-030-34489-4](https://link.springer.com/book/10.1007/978-3-030-34489-4))

* [[Roman Orus]], _Tensor networks for complex quantum systems_, Nature Reviews Physics 1, 538-550 (2019) ([arXiv:1812.04011](https://arxiv.org/abs/1812.04011), [doi:10.1038/s42254-019-0086-7](https://doi.org/10.1038/s42254-019-0086-7))

* {#Biamonte19} [[Jacob Biamonte]], _Lectures on Quantum Tensor Networks_ ([arXiv:1912.10049](https://arxiv.org/abs/1912.10049))

With [[global symmetry]]:

* Sukhwinder Singh, Robert N. C. Pfeifer, [[Guifre Vidal]], _Tensor network decompositions in the presence of a global symmetry_, Phys. Rev. A82:050301, 2010 ([arXiv:0907.2994](https://arxiv.org/abs/0907.2994))

* Sukhwinder Singh, Robert N. C. Pfeifer, [[Guifre Vidal]], _Tensor network states and algorithms in the presence of a global $U(1)$ symmetry_, Phys. Rev. B 83, 115125 (2011) ([arXix:1008.4774](https://arxiv.org/abs/1008.4774))

* {#SinghVidal12} Sukhwinder Singh, [[Guifre Vidal]], _Tensor network states and algorithms in the presence of a global $SU(2)$ symmetry_, Phys. Rev. B 86, 195114 (2012) ([arXiv:1208.3919](https://arxiv.org/abs/1208.3919))


Further resources:

* [Tensor Network Initiative](https://www.perimeterinstitute.ca/research/research-initiatives/tensor-networks-initiative)

* [tensornetwork.org](https://tensornetwork.org/)

### Application in solid state physics

Discussion of [[solid state physics]] via [[tensor network states]]:

General:

* [[Jens Eisert]], M. Cramer, M.B. Plenio, _Area laws for the entanglement entropy - a review_, Rev. Mod. Phys. 82, 277 (2010) ([arXiv:0808.3773](https://arxiv.org/abs/0808.3773))


* [[Roman Orus]], _A Practical Introduction to Tensor Networks: Matrix Product States and Projected Entangled Pair States_, 	Annals of Physics 349 (2014) 117-158  ([arXiv:1306.2164](https://arxiv.org/abs/1306.2164))

* [[Jens Eisert]], _Entanglement and tensor network states_, Modeling and Simulation 3, 520 (2013) ([arXiv:1308.3318](https://arxiv.org/abs/1308.3318))


* [[Thorsten B. Wahl]], _Tensor network states for the description of quantum many-body systems_ ([arXiv:1509.05984](https://arxiv.org/abs/1509.05984))


Concrete materials:

* A. Kshetrimayum, C. Balz, B. Lake, [[Jens Eisert]], _Tensor network investigation of the double layer Kagome compound $Ca_{10} Cr_{7} O_{28}$_ ([arXiv:1904.00028](https://arxiv.org/abs/1904.00028))


### Relation to (topological) phases of matter

Classification of ([[topological phases of matter|topological]]) [[phases of matter]] via [[tensor network states]]:

* C. Wille, O. Buerschaper, [[Jens Eisert]], _Fermionic topological quantum states as tensor networks_, Phys. Rev. B 95, 245127 (2017) ([arXiv:1609.02574](https://arxiv.org/abs/1609.02574))

* Andreas Bauer, [[Jens Eisert]], Carolin Wille, _Towards a mathematical formalism for classifying phases of matter_ ([arXiv:1903.05413](https://arxiv.org/abs/1903.05413))



### In holographic entanglement entropy

The use of [[tensor networks]] as a tool in [[holographic entanglement entropy]] goes back to

* {#Swingle09} [[Brian Swingle]], _Entanglement Renormalization and Holography_, Phys. Rev. D 86, 065007 (2012) ([arXiv:0905.1317](https://arxiv.org/abs/0905.1317))

* {#Swingle12} [[Brian Swingle]], _Constructing holographic spacetimes using entanglement renormalization_ ([arXiv:1209.3304](https://arxiv.org/abs/1209.3304), [spire:1185813](http://inspirehep.net/record/1185813))

Review in

* [[Frank Verstraete]], J. I. Cirac, V. Murg, _Matrix Product States, Projected Entangled Pair States, and variational renormalization group methods for quantum spin systems_, Adv. Phys. 57,143 (2008) ([arXiv:0907.2796](https://arxiv.org/abs/0907.2796))

### In the $p$-adic AdS/CFT correspondence

Tensor networks associated with [[Bruhat-Tits trees]] in [[p-adic AdS/CFT correspondence]]:


* [[Matthew Heydeman]], [[Matilde Marcolli]], [[Ingmar Saberi]], [[Bogdan Stoica]], _Tensor networks, $p$-adic fields, and algebraic curves: arithmetic and the $AdS_3/CFT_2$ correspondence_ ([arXiv:1605.07639](https://arxiv.org/abs/1605.07639))

* Arpan Bhattacharyya, Ling-Yan Hung, Yang Lei, Wei Li, _Tensor network and ($p$-adic) AdS/CFT_, JHEP 1801 (2018) 139 ([arXiv:1703.05445](https://arxiv.org/abs/1703.05445))

* Ling-Yan Hung, Wei Li, Charles M. Melby-Thompson, _$p$-adic CFT is a holographic tensor network_ ([arXiv:1902.01411](https://arxiv.org/abs/1902.01411))


* Lin Chen, Xirong Liu, Ling-Yan Hung, _Emergent Einstein Equation in p-adic CFT Tensor Networks_ ([arXiv:2102.12022](https://arxiv.org/abs/2102.12022))

* Lin Chen, Xirong Liu, Ling-Yan Hung, _Bending the Bruhat-Tits Tree I:Tensor Network and Emergent Einstein Equations_ ([arXiv:2102.12023](https://arxiv.org/abs/2102.12023))

* Lin Chen, Xirong Liu, Ling-Yan Hung, _Bending the Bruhat-Tits Tree II: the p-adic BTZ Black hole and Local Diffeomorephism on the Bruhat-Tits Tree_ ([arXiv:2102.12024](https://arxiv.org/abs/2102.12024))






Discussion of [[BTZ black holes]] via [[tensor networks]] in the [[p-adic AdS/CFT correspondence]]:

* Matthew Heydeman, [[Matilde Marcolli]], Sarthak Parikh, [[Ingmar Saberi]], _Nonarchimedean Holographic Entropy from Networks of Perfect Tensors_ ([arXiv:1812.04057](https://arxiv.org/abs/1812.04057))


See also

* [[Alexander Jahn]], [[Zoltán Zimborás]], [[Jens Eisert]], _Central charges of aperiodic holographic tensor network models_ ([arXiv:1911.03485](https://arxiv.org/abs/1911.03485))

  ([[quasicrystal]] boundary states)

* [[Alexander Jahn]], [[Zoltán Zimborás]], [[Jens Eisert]], _Tensor network models of AdS/qCFT_ ([arXiv:2004.04173](https://arxiv.org/abs/2004.04173))




### As quantum error correcting codes

Further interpretation of [[tensor networks]] in terms of [[quantum error correcting codes]]:

* Andrew J. Ferris, David Poulin, *Tensor Networks and Quantum Error Correction*, Phys. Rev. Lett. 113, 030501 (2014) ([arXiv:1312.4578](https://arxiv.org/abs/1312.4578))

and specifically in the [[HaPPY code]] modelling [[holographic entanglement entropy]]:

* {#ADH14} [[Ahmed Almheiri]], [[Xi Dong]], [[Daniel Harlow]], _Bulk Locality and Quantum Error Correction in AdS/CFT_, JHEP 1504:163,2015 ([arXiv:1411.7041](https://arxiv.org/abs/1411.7041))

* {#PYHP15} Fernando Pastawski, Beni Yoshida, [[Daniel Harlow]], [[John Preskill]], _Holographic quantum error-correcting codes: Toy models for the bulk/boundary correspondence_, JHEP 06 (2015) 149 ([arXiv:1503.06237](https://arxiv.org/abs/1503.06237))

reviewed in

* {#Harlow18} [[Daniel Harlow]], _TASI Lectures on the Emergence of Bulk Physics in AdS/CFT_ ([arXiv:1802.01040](https://arxiv.org/abs/1802.01040))

Generalization to the [[Majorana dimer code]]:

* [[Alexander Jahn]], [[Marek Gluza]], [[Fernando Pastawski]], [[Jens Eisert]], _Majorana dimers and holographic quantum error-correcting codes_, Phys. Rev. Research 1, 033079 (2019) ([arXiv:1905.03268](https://arxiv.org/abs/1905.03268))

reviewed in:

* [[Alexander Jahn]], [[Jens Eisert]], _Holographic tensor network models and quantum error correction: A topical review_ ([arXiv:2102.02619](https://arxiv.org/abs/2102.02619))


Discussion of [[asymptotic boundaries]] of hyperbolic tensor networks as [[quasicrystals]]:

* Latham Boyle, Madeline Dickens, Felix Flicker, _Conformal Quasicrystals and Holography_, Phys. Rev. X 10, 011009 (2020) ([arXiv:1805.02665](https://arxiv.org/abs/1805.02665))

See also

* Ning Bao, [[Geoffrey Penington]], Jonathan Sorce, Aron C. Wall, _Beyond Toy Models: Distilling Tensor Networks in Full AdS/CFT_ ([arXiv:1812.01171](https://arxiv.org/abs/1812.01171))

* Ning Bao, [[Geoffrey Penington]], Jonathan Sorce, Aron C. Wall, _Holographic Tensor Networks in Full AdS/CFT_ ([arXiv:1902.10157](https://arxiv.org/abs/1902.10157))

* {#JGPE19} [[Alexander Jahn]], [[Marek Gluza]], [[Fernando Pastawski, [[Jens Eisert]], _Majorana dimers and holographic quantum error-correcting codes_ ([arXiv:1905.03268](https://arxiv.org/abs/1905.03268)) 

### Relation to spin chains

Relation to [[spin chains]]:

* Mari Carmen Banuls, Michal P. Heller, Karl Jansen, Johannes Knaute, Viktor Svensson, _From spin chains to real-time thermal field theory using tensor networks_ ([arXiv:1912.08836](https://arxiv.org/abs/1912.08836))

### Application to lattice gauge theory

Application to [[lattice gauge theory]]:

* [[Luca Tagliacozzo]], Alessio Celi, Maciej Lewenstein, _Tensor Networks for Lattice Gauge Theories with continuous groups_, Phys. Rev. X 4, 041024 (2014) ([arXiv:1405.4811](https://arxiv.org/abs/1405.4811))

* {#BBCCCDFJLMMRRTVV19} M.C. Bañuls, R. Blatt, J. Catani, A. Celi, J.I. Cirac, M. Dalmonte, L. Fallani, K. Jansen, M. Lewenstein, S. Montangero, C.A. Muschik, B. Reznik, E. Rico, [[Luca Tagliacozzo]], K. Van Acoleyen, [[Frank Verstraete]], U.-J. Wiese, M. Wingate, J. Zakrzewski, P. Zoller: 

  _Simulating Lattice Gauge Theories within Quantum Technologies_ 

  ([arXiv:1911.00003](https://arxiv.org/abs/1911.00003))




### In higher parallel transport

Discussion in relation to [[higher parallel transport]]:

* {#Parzygnat18} [[Arthur Parzygnat]], _Two-dimensional algebra in lattice gauge theory_ ([arXiv:1802.01139](https://arxiv.org/abs/1802.01139))



[[!redirects tensor networks]]

[[!redirects tensor network state]]
[[!redirects tensor network states]]


