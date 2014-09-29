
{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
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

This entry discusses the [[quantization]] of the [[prequantum field theory|prequantum]] data of standard 3d [[Chern-Simons theory]] (induced from a suitable [[Lie group]] and [[invariant polynomial]]/[[second Chern class]] [[action functional]]) to a [[3d TQFT]].

The steps involved in the [[geometric quantization]] of [[Chern-Simons theory]] are indicated at _[Chern-Simons theory -- Geometic quantization](Chern-Simons+theory#GeometricQuantization)_.

It was long expected that the resulting [[3d TQFT]] is that given by the [[Reshetikhin-Turaev model]], which is a kind of state sum model that produces an [[FQFT]] from the data of a [[modular tensor category]], such as the category of [[positive energy representations]] of the [[loop group]] of $G$, or else of a [[quantum group]]. 

More recently all the ingredients of a proof that this is indeed equivalently the result of the [[geometric quantization]] are appearing ([Andersen 12](#Andersen12)). See also ([MO discussion](#MODiscussion)).

## General idea
 {#GeneralIdea}

> under construction

There are plenty of technical details involved in the quantization of Chern-Simons theory and all that is subsumed by it (such as the [[Wilson loop]] [[quantum observables]] and the [[Jones polynomial]] [[knot invariants]] they gives rise to, and such as the [[WZW model]], its [[modular functor]] and the [[equivariant elliptic cohomology]] that it induces), but there is also a neat general story controlling it. Here we try to sketch that general story at a rough level in order to provide orientation.

### Space of Chern-Simons quantum states 

Chern-Simons [[action functional]]

$$
  \exp(\tfrac{i}{\hbar}S_{CS}) \colon \mathbf{Fields}_{CS} \longrightarrow \mathbf{B}^{n+1} U(1)_{conn}
$$

given a [[closed manifold]] $\Sigma_n$ then choice of [[complex structure]] $\mathbf{\Sigma}_n$ on $\Sigma_n$ is supposed to naturally induce a [[complex structure]] on the space of (on-shell) fields over $\Sigma_n$

$$
  \mathbf{Fields}_{CS}(\mathbf{\Sigma}_n)
$$

Moreover, [[transgression]] of $\exp(\tfrac{i}{\hbar}S)$ to $\mathbf{Fields}_{CS}(\Sigma)$ is supposed to yield a [[holomorphic line bundle]] with connection with respect to that complex structure

$$
  \exp(\tfrac{i}{\hbar}S(\mathbf{\Sigma}_n))
  \colon
  \mathbf{Fields}_{CS}(\mathbf{\Sigma}_n)
  \longrightarrow
  \mathbf{B}U(1)_{conn} 
  \,.
$$

This is the [[prequantum line bundle]] of the Chern-Simons theory, already equipped with a [[Kähler polarization]].

Accordingly, the [[geometric quantization]] of the CS action functional assigns to $\Sigma_n$ the [[Hilbert space]] $\mathcal{H}_{\mathbf{\Sigma}}$ of holomorphic sections of $\exp(\tfrac{i}{\hbar}S(\mathbf{\Sigma}_n))$.

As the complex structure $\mathbf{\Sigma}_n$ on $\Sigma_n$ varies over the [[moduli stack of complex structures]] $\mathcal{M}_{\Sigma}$, these vector spaces $\mathcal{H}_{\mathbf{\Sigma}_n}$ form a [[vector bundle]] with projective flat connection (the _[[Hitchin connection]]_) on the moduli stack

$$
  \array{
    \mathcal{H}
    \\
    \downarrow
    \\
    \mathcal{M}_{\Sigma}
  }
$$

The assignment

$$
  \Sigma_n \mapsto \mathcal{H}_{\Sigma}
$$

natural in [[diffeomorphisms]] of $\Sigma$ is called the _[[modular functor]]_, this we focus on more [below](#ModularFunctorAndEquivariantEllipticCohomology)


One such section $\Psi$ is to be singled out. For instance if $\exp(\tfrac{i}{\hbar}S(\Sigma_n))$ is a [[theta characteristic]] then there is up to scale a unique holomorphic section. This singling-out is formalized by the [[FRS-formalism]]. See there for more.

### Space of WZW-model pre-correlators 

Under the [[AdS3-CFT2 and CS-WZW correspondence]] the states of Chern-Simons theory also correspond to [[partition functions]] of the [[gauged WZW model]] and hence to [[generating functions]] for [[correlation functions]] of the actual [[WZW model]].

The [[field (physics)|fields]] $\mathbf{Fields}(\Sigma_n)$ may also be thought of as the [[sources]] of a (higher) [[gauged WZW model]] on $\Sigma$. 

The [[holographic principle]] says that the [[quantum state]]/[[wavefunction]] 

$$
  \Psi \in \Gamma(\mathbf{Fields}_{CS}(\mathbf{\Sigma}_n), L)
$$ 

is also the [[generating function]] for the [[correlators]] of the [[WZW model]] on $\Sigma_n$, meaning that its [[functional derivatives]] 

+-- {: bluebox}

$$
  \frac{\delta}{\delta A^{a_1}(z_1)}
  \cdots 
  \frac{\delta}{\delta A^{a_n}(z_n)}
  \Psi
  =
  \left\langle J^{a_1}(z_1) \cdots J^{a_n}(z_n) \right\rangle
$$

=--

with respect to the Chern-Simons-[[field (physics)|fields]], hence the WZW [[sources]],  are the [[n-point functions]] of the WZW model for [[current algebra]] insertions, as indicated


(e.g. [Gaw&#281;dzki 99 (4.23), 5.1](#Gawedzki99))

### Modular functor and equivariant elliptic cohomology
 {#ModularFunctorAndEquivariantEllipticCohomology}

Side remark: discussion of [[equivariant elliptic cohomology]] (see there ar _[interpretation in QFT](equivariant+elliptic+cohomology#InterpretationInQuantumFieldTheory)_) says that this construction refines from equipping $\Sigma$ with [[complex structure]] to equipping it with [[arithmetic geometry|arithmetic structure]]. Hence for $\Sigma$ a [[torus]] it refines from structures of [[elliptic curves]] over the complex numbers to general arithmetic elliptic curves (over the [[integers]]) and in fact to [[derived elliptic curves]] (over the [[sphere spectrum]]). Hence eventually the theory of [[geometric quantization]] needs to be refined to admit [[polarizations]] in [[arithmetic geometry]]. See at _[[differential cohesion and idelic structure]]_ for more on this.



## Related concepts

* [[Donaldson-Uhlenbeck-Yau theorem]]

* [[Narasimhan-Seshadri theorem]]

* [[Harder-Narasimhan theorem]]



* [[equivariant elliptic cohomology]]

## References
 {#References}

Basics are recalled for instance in

* Fernando Falceto, [[Krzysztof Gaw?dzki]], _Chern-Simons States at Genus One_, Commun.Math.Phys. 159 (1994) 549-580 ([arXiv:hep-th/9211003](http://arxiv.org/abs/hep-th/9211003))

* {#Gawedzki99} [[Krzysztof Gaw?dzki]], _Conformal field theory: a case study_ in Y. Nutku, C. Saclioglu, T. Turgut (eds.) _Frontier in Physics_ 102, Perseus Publishing (2000) ([hep-th/9904145](http://xxx.lanl.gov/abs/hep-th/9904145))

* Yasuhiro Abe, _Application of abelian holonomy formalism to the elementary theory of numbers_ ([arXiv:1005.4299](http://arxiv.org/abs/1005.4299))


Explicit proof that in particular the [[modular functor]] in the [[Reshetikhin-Turaev model]] is equivalent to that induced from [[geometric quantization]] (via relating the [[Hitchin connection]] to bundles of [[conformal blocks]]) is at least partially in

* {#Laszlo98} [[Yves Laszlo]] _Hitchin's and WZW connection are the same_, J. Differential Geom. 49 (1998), no. 3, 547&#8211;576 ([pdf](http://www.emis.de/journals/NYJM/JDG/archive/vol.49/3_5.pdf))


* [[Jørgen Andersen]], K. Ueno, _Abelian Conformal Field theories and Determinant Bundles_, International Journal of Mathematics, 18 919 - 993 (2007). 

* [[Jørgen Andersen]], K. Ueno, _Geometric Construction of Modular Functors from Conformal Field Theory_, Journal of Knot theory and its Ramifications, 16 127 -- 202, (2007). 

* [[Jørgen Andersen]], K. Ueno, _Modular functors are determined by their genus zero data_, Journal of Quantum Topology ([arXiv:math/0611087](http://arxiv.org/abs/math/0611087))

Culminating in

* [[Jørgen Andersen]], K. Ueno, _Construction of the Reshetikhin-Turaev TQFT via Conformal Field Theory_ ([arXiv:1110.5027](http://arxiv.org/abs/1110.5027))

* {#Andersen12} [[Jørgen Andersen]], _A geometric formula for the Witten-Reshetikhin-Turaev Quantum Invariants and some applications_ ([arXiv:1206.2785](http://arxiv.org/abs/1206.2785))
 
For discussion of the state of the proof see also

* MO, _[Why hasn't anyone proved that the two standard approaches to quantizing Chern-Simons theory are equivalent?](http://mathoverflow.net/questions/86792/why-hasnt-anyone-proved-that-the-two-standard-approaches-to-quantizing-chern-si)_
 {#MODiscussion}

Another approach is

* [[Daniel Freed]], [[Mike Hopkins]], [[Constantin Teleman]], [[Jacob Lurie]], _[TQFT from compact Lie groups -- 3d Chern-Simons as a fully extended TQFT](http://ncatlab.org/nlab/show/Topological+Quantum+Field+Theories+from+Compact+Lie+Groups#3dCSFullyExtended)_.

[[!redirects quantization of Chern-Simons theory]]