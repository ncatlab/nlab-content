


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[perturbative quantum field theory]] one way to construct an [[S-matrix]] $\mathcal{S}$ via [[renormalization|("re"-)normalization]] of [[time-ordered products]]/[[Feynman amplitudes]] is to consider a sequence of [[UV cutoffs]] $\Lambda$ with corresponding [[effective S-matrices]] $\mathcal{S}_\Lambda$ and then form the [[limit of a sequence|limit]] as $\Lambda \to \infty$, which exists if in the course one applies suitable [[interaction vertex redefinitions]] $\mathcal{Z}_\Lambda$

$$
  \mathcal{S}(g S_{int} + j A) = \underset{\Lambda \to \infty}{\lim} (\mathcal{S}_\Lambda \circ \mathcal{Z}_\Lambda)(g S_{int} + j A)
$$

(See at _[[effective QFT]]_ [this prop.](effective+quantum+field+theory#UVRegularization)).

This may be read as saying that as one "removes the UV-cutoff" the original [[interaction]] [[action functional]] $g S_{int} + j A$ is to be corrected by "counterterm-[[interactions]]"

$$
  S_{counter, \Lambda}
  \;\coloneqq\:
  \left(
    \mathcal{Z}_\Lambda - id
  \right)
  \left(
    g S_{int} + j A
  \right)
  \,.
$$

## Details

See at _[[effective action]]_ around [this remark](effective+quantum+field+theory#TermCounter).

## References

The rigorous formulation of [[renormalization|("re"-)normalization]] via [[UV cutoff]] and counterterms in [[causal perturbation theory]]/[[perturbative QFT]] is due to

* {#BrunettiDuetschFredenhagen09} [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], section 5.2 of _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](https://arxiv.org/abs/0901.2038))

* {#Duetsch10} [[Michael Dütsch]], _Connection between the renormalization groups of Stückelberg-Petermann and Wilson_, Confluentes Mathematici, Vol. 4, No. 1 (2012) 12400014 ([arXiv:1012.5604](https://arxiv.org/abs/1012.5604))

* {#DuetschFredenhagenKellerRejzner14} [[Michael Dütsch]], [[Klaus Fredenhagen]], [[Kai Keller]], [[Katarzyna Rejzner]], appendix A of _Dimensional Regularization in Position Space, and a Forest Formula for Epstein-Glaser Renormalization_, J. Math. Phy. 55(12), 122303 (2014) ([arXiv:1311.5424](https://arxiv.org/abs/1311.5424))


reviewed in

* {#Duetsch18} [[Michael Dütsch]], section 3.8 of _[[From classical field theory to perturbative quantum field theory]]_, 2018


See also

* [[Kevin Costello]], section 8 _Renormalisation and the Batalin-Vilkovisky formalism_ ([arXiv:0706.1533](http://arxiv.org/abs/0706.1533)) 

[[!redirects counterterms]]

[[!redirects counter-term]]
[[!redirects counter-terms]]
