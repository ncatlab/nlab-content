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
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

What are called _tree tensor network states_ (TTN states) in [[quantum physics]] (specifically in [[solid state physics]] and in [[AdS/CFT]]) are those [[tensor network states]] of the form of [[tree]], often considered of fixed valence.

For example, given a [[metric Lie algebra]] $\mathfrak{g}$ (with [[string diagram]]-notation as discussed [there](metric+Lie+algebra#Definition)) its [[Lie bracket]]-[[tensor]] $f \coloneqq [-,-] \in \mathfrak{g}^\ast \otimes \mathfrak{g}^\ast \otimes \mathfrak{g}$ gives rise to tree tensor network of the following form:

<center>
<img src="https://ncatlab.org/nlab/files/TensorNetworkStateFromMetricLieAlgebra.jpg" width="300">
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

## Related concepts

[[!include states and observables -- content]]



## References

### General

For more see the references at _[[tensor network state]]_.

* Shi-Ju Ran, Emanuele Tirrito, Cheng Peng, Xi Chen, Luca Tagliacozzo, Gang Su, Maciej Lewenstein, Section 2.3.3 of: _Tensor Network Contractions_, Lecture Notes in Physics, Springer (2020) ([arXiv:1708.09213](https://arxiv.org/abs/1708.09213), [doi:10.1007/978-3-030-34489-4](https://link.springer.com/book/10.1007/978-3-030-34489-4))


### Application in solid state physics

Application in [[solid state physics]]:

* Valentin Murg, Örs Legeza, Reinhard M. Noack, [[Frank Verstraete]], _Simulating Strongly Correlated Quantum Systems with Tree Tensor Networks_, Phys. Rev. B 82, 205105 (2010) ([arXiv:1006.3095](https://arxiv.org/abs/1006.3095))

### Application in quantum chemistry 

For application in [[quantum chemistry]]:

* Naoki Nakatani, Garnet Kin-Lic Chan, _Efficient Tree Tensor Network States (TTNS) for Quantum Chemistry: Generalizations of the Density Matrix Renormalization Group Algorithm_, J. Chem. Phys. 138, 134113 (2013) ([arXiv:1302.2298](https://arxiv.org/abs/1302.2298))

* Klaas Gunst, [[Frank Verstraete]], Sebastian Wouters, Örs Legeza, Dimitri Van Neck, _T3NS: three-legged tree tensor network states_, Chem. Theory Comput. 2018, 14, 4, 2026-2033 ([arXiv:1801.09998](https://arxiv.org/abs/1801.09998))


* Henrik R. Larsson, _Computing vibrational eigenstates with tree tensor network states (TTNS)_, J. Chem. Phys. 151, 204102 (2019) ([arXiv:1909.13831](https://arxiv.org/abs/1909.13831))

### Application in machine learning

Application in [[machine learning]]:

* Ding Liu, Shi-Ju Ran, Peter Wittek, Cheng Peng, Raul Blázquez García, Gang Su, Maciej Lewenstein, _Machine Learning by Unitary Tensor Network of Hierarchical Tree Structure_, New Journal of Physics, 21, 073059 (2019) ([arXiv:1710.04833](https://arxiv.org/abs/1710.04833))

* Song Cheng, Lei Wang, Tao Xiang, Pan Zhang, _Tree Tensor Networks for Generative Modeling_, Phys. Rev. B 99, 155131 (2019) ([arXiv:1901.02217](https://arxiv.org/abs/1901.02217))

[[!redirects tree tensor network states]]

[[!redirects tree tensor network]]
[[!redirects tree tensor networks]]




