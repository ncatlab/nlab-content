
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Kapustin-Witten TQFT_ is the [[4d TQFT]] obtained by  [[topologically twisted super Yang-Mills theory|topological twisting]] from  [[N=4 D=4 super Yang-Mills theory]] on a 4-dimensional manifold of the form $M=\Sigma\times C$, where $\Sigma$ is a Riemann surface possibly with boundary and $C$ is a Riemann surface of genus $g\geq 2$. Its [[S-duality]] is supposed to encode, as a special case, [[geometric Langlands duality]] for the Riemann surface $C$.

Upon [[Kaluza-Klein mechanism|compactification]] on $C$ (i.e. $C$ is taken to be much smaller than $\Sigma$) down to 2d the resulting effective field theory on $\Sigma$ reproduces, at certain parameters, the [[A-model]] and the [[B-model]] whose target as a [[sigma model]] is the Hitchin moduli space $\mathcal{M}_{H}(G)$, where $G$ is the gauge group of the theory.

The Hitchin moduli space is a [[hyperkähler manifold]]. In complex structure $I$ it can be seen as the moduli space of Higgs bundles on $C$, and in complex structures $J$ and $K$ it can be seen as the moduli space of $G$-local systems on $C$. This is a form of [[nonabelian Hodge theory]].

S-duality manifests as mirror symmetry between $\mathcal{M}_{H}(G)$ and $\mathcal{M}_{H}({}^{L}G)$ where ${}^{L}G$ is the Langlands dual group of $G$. It exchanges B-branes on $\mathcal{M}_{H}({}^{L}G)$ in complex structure $J$ with A-branes on $\mathcal{M}_{H}(G)$ with complex structure $J$. It also exchanges [[Wilson loop]] operators and [['t Hooft operators]] (which correspond to [[Hecke correspondences]]).

The connection to the geometric Langlands correspondence may now be made more explicit as follows. We start with a zerobrane (a B-brane) $\mathcal{B}$ on $\mathcal{M}_{H}({}^{L}G)$ in complex structure $J$, which is an eigenbrane for the Wilson loop operators, corresponding to a local system on $C$. S-duality gives us an A-brane $\mathcal{A}$ on $\mathcal{M}_{H}(G)$ in complex structure $K$, which is an eigenbrane for the 't Hooft operators. Now we perform a hyperkahler rotation and consider $\mathcal{A}$ as an A-brane on $\mathcal{M}_{H}(G)$, in complex structure $I$. Let $\mathcal{A}_{cc}$ be the canonical isotropic brane on $\mathcal{M}_{H}(G)$. The sheafification of $\mathrm{Hom}(\mathcal{A}_{cc},\mathcal{A})$ gives us a [[D-module]] for the sheaf of differential operators given by the sheafification of $\mathrm{Hom}(\mathcal{A}_{cc},\mathcal{A}_{cc})$ (see also the related topic of [[quantization via the A-model]]). The resulting D-module is expected to be the [[Hecke eigensheaf]] predicted by the geometric Langlands correspondence.

[[!include gauge theory from AdS-CFT -- table]]

## Related concepts

* [[geometric Langlands duality]]

* [[A-model]], [[B-model]]

* [[quantization via the A-model]]

## References

The TQFT was introduced in 

* [[Anton Kapustin]], [[Edward Witten]], _Electric-Magnetic Duality And The Geometric Langlands Program_ , Communications in number theory and physics, Volume 1, Number 1, 1&#8211;236 (2007) ([arXiv:hep-th/0604151](http://arxiv.org/abs/hep-th/0604151))
 {#KapustinWitten}

Reviews include 

* [[Anton Kapustin]], _Langlands Duality and Topological Field Theory_ (2007) ([pdf](http://www.icmat.es/seminarios/langlands/school/handouts/kapustin.pdf))

* [[Edward Frenkel]], _Gauge Theory and Langlands Duality_ (2009) ([arXiv:0906.2747](https://arxiv.org/abs/0906.2747))

* [[Edward Witten]], _Mirror Symmetry, Hitchin's Equations, and Langlands Duality_ (2009) ([arXiv:0802.0999](https://arxiv.org/abs/0802.0999))

The link between mirror symmetry and geometric Langlands was explored in the earlier paper

* [[Tamas Hausel]], [[Michael Thaddeus]], _Mirror Symmetry, Langlands Duality, and the Hitchin System_ ([arXiv:0205236](https://arxiv.org/abs/math/0205236))

The 0-1-2 [[extended QFT]] version of $GL$-twisted [[N=4 D=4 super Yang-Mills theory]] is considered in 

* [[David Ben-Zvi]], [[David Nadler]], _The Character Theory of a Complex Group_ ([arXiv:0904.1247](http://arxiv.org/abs/0904.1247))

A discussion formalized in [[BV quantization]] of [[factorization algebras]] is in 

* [[Kevin Costello]], _Notes on supersymmetric and holomorphic field theories in dimension 2 and 4_ ([pdf](http://www.math.northwestern.edu/~costello/sullivan.pdf))