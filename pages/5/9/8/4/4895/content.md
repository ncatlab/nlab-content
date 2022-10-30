
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
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

In [[quantum field theory]] what has come to be known as the _holographic principle_ is the fact that the [[partition function]]s of some [[quantum field theories]] of [[dimension]] $n$ may be identified with [[state]] of QFTs in dimension $n + 1$:



## Examples

### Poisson $\sigma$-model / quantum mechanics

Ordinary [[quantum mechanics]] induced by [[quantization]] of a [[Poisson manifold]] -- which may be regarded as a 1-dimensional QFT -- is holographically dual to the 2-dimensional [[Poisson sigma-model]] 
(implicitly observed by ([Kontsevich](#Kontsevich)) made explicit by ([CattaneoFelder](#CattaneoFelder)).

### A-model / quantum mechanics

Similarly the [[A-model]] on certain [[D-brane]]s gives a holographic description of ordinary [[quantum mechanics]]. ([Witten](#WittenAModel)).

See

* [[quantization via the A-model]]

### Chern-Simons theory / WZW-model

3-dimensional Chern-Simons theory for a group $G$ is holographically dual to the 2-dimensional [[WZW-model]].

### Higher dimensional Chern-Simons theory / Self-dual higher gauge theory
 {#HigherDimCSAndSelfDualQFT}

#### Idea and examples

Generally, [[higher dimensional Chern-Simons theory]]
in dimension $4k+3$ (for $k \in \mathbb{N}$) is holographically related to [[self-dual higher gauge theory]] in dimension $4k+2$ (at least in the abelian case). 

* $(k=0)$: ordinary 3-dimensional [[Chern-Simons theory]] is related to a [[string]] [[sigma-model]] on its boundary;

* $(k=1)$: 7-dimensional Chern-Simons theory is related to a [[fivebrane]] model on its boundary;

* $(k=2)$: 11-dimensional Chern-Simons theory is related to a parts of a [[type II string theory]] on its bounday (or that of the space-filling 9-[[brane]], if one wishes) ([BelovMoore](#BelovMoore)).


#### Some details

We indicate why [[higher dimensional Chern-Simons theory]] is -- if holographically related to anything -- holographically related to [[self-dual higher gauge theory]].

The [[phase space]] of [[higher dimensional Chern-Simons theory]] in [[dimension]] $4k+3$ on $\Sigma \times \mathbb{R}$ can be identified with the space of [[curvature|flat]] $2k+1$-forms on $\Sigma$. The [[presymplectic form]] on this space is given by the pairing

$$
  (\delta B_1, \delta B_2) \mapsto
  \int_\Sigma \delta B_1 \wedge \delta B_2
  \,.
$$

The [[geometric quantization]] of the theory requires that we choose a polarization of the [[complexification]] of this space (split the space of forms into "coordinates" and their "canonical momenta"). 

One way to achieve this is to choose a [[conformal structure]] on $\Sigma$. The corresponding [[Hodge star operator]]

$$
  \star : \Omega^{2k+1}(\Sigma) \to \Omega^{2k+1}(\Sigma)
$$

provides the polarization by splitting into self-dual and anti-self-dual forms: 

notice that (by the formulas at [[Hodge star operator]]) we have on mid-dimensional forms

$$
  \star \star B = (-1)^{(2k+1)(4k+3)} B
  = - B
  \,.
$$

Therefore it provides a [[complex structure]] on $\Omega^{2k+1}(\Sigma) \otimes \mathbb{C}$.

We see that the symplectic structure on the space of forms can equivalently be rewritten as

$$
  \begin{aligned}
    \int_X B_1 \wedge B_2
    & = - \int_X B_1 \wedge \star \star B_2 
  \end{aligned}
  \,.
$$

Here on the right now the [[Hodge star operator|Hodge inner product]] of $B_1$ with $\star B_2$ appears, which is invariant under applying the Hodge star to both arguments.

We then decompose $\Omega^{2k+1}(\Sigma)$ into the $\pm i$-[[eigenspace]]s of $\star$: say $B \in \Omega^{2k+1}(\Sigma)$ is  _imaginary self-dual_ if

$$
  \star B = i B
$$

and _imaginary anti-self-dual_ if

$$
  \star B = - i B
  \,.
$$

Then for imaginary self-dual $B_1$ and $B_2$ we find that the symplectic pairing is

$$
  \begin{aligned}
    (B_1, B_2)
    &=
    -i \int_X B_1 \wedge \star B_2
    \\
    & =
    -i \int_X (\star B_1) \wedge \star (\star B_2)
    \\
    & =    
    +i \int_X B_1 \wedge \star B_2
  \end{aligned} 
  \,.
$$

Therefore indeed the symplectic pairing vanishes on the self-dual and on the anti-selfdual forms. Evidently these provide a decomposition into [[Lagrangian subspace]]s.


Therefore a [[state]] of higher Chern-Simons theory on $\Sigma$ may locally be thought of as a function of the self-dual forms on $\Sigma$. Under holography this is (therefore) identified with the [[correlator]] of a [[self-dual higher gauge theory]] on $\Sigma$.

(...)


### Ads/CFT

Conjecturally, [[type II string theory]] on a [[anti-de Sitter space]] background is holographically dual to [[super Yang-Mills theory]] on the asymptotic boundary.

See [[AdS/CFT correspondence]].



## Related concepts

* [[holographic principle of higher category theory]]


## References

### Self-dual higher gauge fields and higher abelian Chern-Simons

The idea of describing [[self-dual higher gauge theory]] by abelian Chern-Simons theory in one dimension higher originates in 

* [[Edward Witten]], _Five-brane effective action in M-Theory_, J. Geom. Phys. __22__ (1997), no. 2, 103&#8211;133, [hep-th/9610234](http://arxiv.org/abs/hep-th/9610234)

* [[Edward Witten]], _Duality relations among topological effects in string theory_, J. High Energy Phys. 2000, no. 5, Paper 31, 31 pp. [arXiv:hep-th/9912086](http://arxiv.org/abs/hep-th/9912086), [doi](http://dx.doi.org/10.1088/1126-6708/2000/05/031)

More discussion of the general principle is in 

* Dmitriy Belov, [[Greg Moore]], _Holographic action for the self-dual field_, [arXiv:hep-th/0605038](http://arxiv.org/abs/hep-th/0605038)
 {#BelovMoore}

A quick exposition of the basic idea is in

* [[Jacques Distler]], _Actions for self-dual gauge fields_ ([blog](http://golem.ph.utexas.edu/~distler/blog/archives/000809.html))

The application of this to the description of type II [[string theory]] in 10-dimensions to 11-dimensional Chern-Simons theory is in the followup 

* Dmitriy Belov, [[Greg Moore]], _Type II Actions from 11-Dimensional Chern-Simons Theories_ ([arXiv](http://arxiv.org/abs/hep-th/0611020))

### Poisson $\sigma$-model/A-model and quantum mechanics

* [[Maxim Kontsevich]], ...
 {#Kontsevich}

* [[Alberto Cattaneo]], [[Giovanni Felder]], ...
 {#CattaneoFelder}

* [[Edward Witten]], ...
 {#WittenAModel}

### For Chern-Simons theory / 2d CFT

3-dimensional [[Chern-Simons theory]] in the context of holography is discussed for instance in

* Victor O. Rivelles, _Holographic Principle and AdS/CFT Correspondence_ ([arXiv](http://arxiv.org/abs/hep-th/9912139))

* [[Anton Kapustin]], [[Natalia Saulina]], _Surface operators in 3d TFT and 2d Rational CFT_ in [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ AMS, 2011
* R. Bousso, _The holographic principle_, Rev. Mod. Phys. __74__ (2002) 825-874, [MR2003m:83048](http://www.ams.org/mathscinet-getitem?mr=1925130), [doi](http://link.aps.org/doi/10.1103/RevModPhys.74.825)

### General abstract formulation

An identification of boundary conditions and [[QFT with defects|defects]] as [[natural transformation]]s between higher dimensional [[FQFT]]s is discussed in

* [[Chris Schommer-Pries]], _Topological defects and classifying local topological field theories in low dimension_ ([[SchommerPriesDefects.pdf:file]])
{#SchommerPries}

See [[holographic principle of higher category theory]] for more on this.