
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
 {#Idea}

This entry discusses the full ([[non-perturbative quantum field theory|non-perturbative]]) [[quantization]] of the [[prequantum field theory|prequantum]] data of standard 3d [[Chern-Simons theory]] (induced from a suitable [[Lie group]] and [[invariant polynomial]]/[[second Chern class]] [[action functional]]) to a [[3d TQFT]].

(For the [[perturbative QFT|perturbative quantization]] of [[Chern-Simons theory]] see [there](Chern-Simons+theory#PerturbativeQuantization)).

Existing literature knows three sectors of this problem, which overlap but do not coincide

1. [[path integral quantization]]. This may be made precise sense of in [[perturbation theory]] where it involves lots of interesting structure such as [[analytic torsion]] ([Witten 89](Chern-Simons#theory#Witten89)). However, being just [[perturbation theory]] it is just an approximation to the full answer.

1. [[geometric quantization]] yields the full (non-perturbative quantization) in [[codimension]] 1, but does not say anything about codimension 0.

1. The [[Reshetikhin-Turaev construction]] produces a [[3d TQFT]] from algebraic data that is naturally associated with the prequantum data defining Chern-Simons theory (such as the category of [[positive energy representations]] of the [[loop group]] of the given [[gauge group]] $G$, or else of a [[quantum group]] [Sawin 06](#Sawin06)), but it is not a priori clear that this 3d quantum field theory is genuinely the result of quantizing the Chern-Simons [[action functional]].

The known relation between the second and the third point here is the following:

That the complex-geometric [[modular functor]] obtained from [[geometric quantization]] of Chern-Simons theory as in ([Axelrod-Pietra-Witten 91](#AxelrodPietraWitten91), [Hitchin 90](#Hitchin90)) coincides with that of [[conformal blocks]] of the [[WZW model]] was shown in ([Laszlo 98](#Laszlo98),see also [Andersen 11](#Andersen11), [Andersen 12](#Andersen12)).
That this in turn indeed satisfies the required [[sewing law]] (and hence really is a modular functor in the strong sense) was shown in ([Tsuchiya-Ueno-Yamada](#TsuchiyaUenoYamada)). By [deprojectivization](modular%20functor#TopologicalLift) these constructions yield a topological modular functor of the form also obtained from the [[Reshetikhin-Turaev construction]].

These (topological) modular functors are fixed by their [[genus]]-0 data ([Andersen-Ueno 06](#AndersenUeno06)) which is equivalently the datum of a (weakly) [[modular tensor category]]. Hence for matching [[geometric quantization]] of 3d Chern-Simons theory to the [[Reshetikhin-Turaev construction]] one has to match the [[modular tensor categories]] obtained from the [[conformal blocks]] of the [[WZW model]] in genus-0 to that associated with the coresponding [[quantum groups]]. This works ([Ostrik 14](#Ostrik14)).

## Something more

> random notes, needs to be brought into shape

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

Discussion of [[equivariant elliptic cohomology]] (see there at _[interpretation in QFT](equivariant+elliptic+cohomology#InterpretationInQuantumFieldTheory)_) shows that the construction of the [[modular functor]] refines from equipping $\Sigma$ with [[complex structure]] to equipping it with [[arithmetic geometry|arithmetic structure]]. Hence for $\Sigma$ a [[torus]] it refines from structures of [[elliptic curves]] over the complex numbers to general arithmetic elliptic curves (over the [[integers]]) and in fact to [[derived elliptic curves]] (over the [[sphere spectrum]]). Hence eventually the theory of [[geometric quantization]] needs to be refined to admit [[polarizations]] in [[arithmetic geometry]]. See at _[[differential cohesion and idelic structure]]_ for more on this.



## Related concepts

* [[Donaldson-Uhlenbeck-Yau theorem]]

* [[Narasimhan-Seshadri theorem]]

* [[Harder-Narasimhan theorem]]



* [[equivariant elliptic cohomology]]

## References
 {#References}

### Non-perturbative geometric quantization
  {#ReferencesNonPerturbative}

Discussion of [[non-perturbative QFT|non-perturbative]] [[geometric quantization]] of [[Chern-Simons theory]]:

Basics are recalled for instance in

* Fernando Falceto, [[Krzysztof Gawedzki]], _Chern-Simons States at Genus One_, Commun.Math.Phys. 159 (1994) 549-580 ([arXiv:hep-th/9211003](http://arxiv.org/abs/hep-th/9211003))

* {#Gawedzki99} [[Krzysztof Gawedzki]], _Conformal field theory: a case study_ in Y. Nutku, C. Saclioglu, T. Turgut (eds.) _Frontier in Physics_ 102, Perseus Publishing (2000) ([hep-th/9904145](http://xxx.lanl.gov/abs/hep-th/9904145))

* Yasuhiro Abe, _Application of abelian holonomy formalism to the elementary theory of numbers_ ([arXiv:1005.4299](http://arxiv.org/abs/1005.4299))

The [[geometric quantization]] of 3d CS theory in codimension 1 is due to 

* {#AxelrodPietraWitten91} [[Scott Axelrod]], S. Della Pietra, [[Edward Witten]], _Geometric quantization of Chern-Simons gauge theory_, Jour. Diff. Geom. 33 (1991), 787-902.  ([EUCLID](http://projecteuclid.org/euclid.jdg/1214446565))

* {#Hitchin90} [[Nigel Hitchin]], _Flat connections and geometric quantization_, : Comm. Math. Phys. Volume 131, Number 2 (1990), 347-380. ([Euclid](http://projecteuclid.org/euclid.cmp/1104200841))

(see also at _[[Hitchin connection]]_).

The [[3d TQFT]] candidate for quantum CS theory in the form of the [[Reshetikhin-Turaev construction]] and the corresponding [[modular tensor category]] data is discussed in

* {#ReshetikhinTuraev91} Reshetikhin; Turaev, _Invariants of 3-manifolds via link polynomials and quantum groups_. Invent. Math. 103 (1991), no. 3, 547&#8211;597. ([pdf](http://mathlab.snu.ac.kr/~top/quantum/article/Reshetikhin01.pdf))

* {#BakalovKirillov} B. Bakalov & [[Alexandre Kirillov]], _Lectures on tensor categories and modular functors_ AMS, University Lecture Series, (2000) ([web](http://www.math.sunysb.edu/~kirillov/tensor/tensor.html)). 

* {#Sawin06} [[Stephen Sawin]], _Quantum groups at roots of unity and modularity_ J. Knot Theory Ramifications 15 (2006), no. 10, 1245&#8211;1277 ([arXiv:0308281](http://arxiv.org/abs/math/0308281))

* {#Ostrik14} [[Victor Ostrik]], _[MO comment August 2014](http://mathoverflow.net/a/178304/381)_

The relation between the [[modular functor]] obtained from the [[conformal blocks]] of the [[WZW model]] and from geometric quantization of CS theory is discussed in

* {#Laszlo98} [[Yves Laszlo]] _Hitchin's and WZW connection are the same_, J. Differential Geom. 49 (1998), no. 3, 547&#8211;576 ([pdf](http://www.emis.de/journals/NYJM/JDG/archive/vol.49/3_5.pdf))


* {#TsuchiyaUenoYamada} Tsuchiya; K Ueno; Yamada, _Conformal field theory on universal family of stable curves with gauge symmetries_, Integrable systems in quantum field theory and statistical mechanics, 459&#8211;566. 


* {#AndersenUeno06} [[Jørgen Andersen]], K. Ueno, _Modular functors are determined by their genus zero data_, Journal of Quantum Topology ([arXiv:math/0611087](http://arxiv.org/abs/math/0611087))

Discussion specific to [[special unitary group|special unitary]] [[gauge group]] is in

* [[Jørgen Andersen]], K. Ueno, _Abelian Conformal Field theories and Determinant Bundles_, International Journal of Mathematics, 18 919 - 993 (2007). 

* [[Jørgen Andersen]], K. Ueno, _Geometric Construction of Modular Functors from Conformal Field Theory_, Journal of Knot theory and its Ramifications, 16 127 -- 202, (2007). 


* {#Andersen11} [[Jørgen Andersen]], K. Ueno, _Construction of the Reshetikhin-Turaev TQFT via Conformal Field Theory_ ([arXiv:1110.5027](http://arxiv.org/abs/1110.5027))

* {#Andersen12} [[Jørgen Andersen]], _A geometric formula for the Witten-Reshetikhin-Turaev Quantum Invariants and some applications_ ([arXiv:1206.2785](http://arxiv.org/abs/1206.2785))
 
For discussion of the state of the proof see also

* {#MODiscussion} MO, _[Why hasn't anyone proved that the two standard approaches to quantizing Chern-Simons theory are equivalent?](http://mathoverflow.net/questions/86792/why-hasnt-anyone-proved-that-the-two-standard-approaches-to-quantizing-chern-si)_
 
and in particular [this reply](http://mathoverflow.net/a/185401/381) by [[Andre Henriques]].

Detailed review in the case of abelian Chern-Simons theory includes

* Spencer D. Stirling, _Abelian Chern-Simons theory with toral gauge group, modular tensor categories, and group categories_ ([arXiv:http://arxiv.org/abs/0807.2857v1](http://arxiv.org/abs/0807.2857))

Discussion in terms of [[Weyl quantization]] of [[Wilson lines]] and details on the role of [[theta functions]] is in

Discussion of [[quantization of Chern-Simons theory]] in terms of [[Weyl quantization]] and [[skein relations]] is in

* [[Jørgen Andersen]], _Deformation quantization and geometric quantization of abelian moduli spaces_, Commun. Math. Phys., 255 (2005), 727&#8211;745

* {#GelcaUribe02} [[Razvan Gelca]], [[Alejandro Uribe]], _The Weyl quantization and the quantum group quantization of the moduli space of flat SU(2)-connections on the torus are the same_, 	Commun.Math.Phys. 233 (2003) 493-512 ([arXiv:math-ph/0201059](http://arxiv.org/abs/math-ph/0201059))

* {#GelcaUribe10a} [[Razvan Gelca]], [[Alejandro Uribe]], _From classical theta functions to topological quantum field theory_  ([arXiv:1006.3252](http://arxiv.org/abs/1006.3252), [slides pdf](http://www.math.ttu.edu/~rgelca/berk.pdf))

* {#GelcaUribe10b} [[Razvan Gelca]], [[Alejandro Uribe]], _Quantum mechanics and non-abelian theta functions for the gauge group $SU(2)$_ ([arXiv:1007.2010](http://arxiv.org/abs/1007.2010))


Another approach is

* [[Daniel Freed]], [[Mike Hopkins]], [[Constantin Teleman]], [[Jacob Lurie]], _[TQFT from compact Lie groups -- 3d Chern-Simons as a fully extended TQFT](http://ncatlab.org/nlab/show/Topological+Quantum+Field+Theories+from+Compact+Lie+Groups#3dCSFullyExtended)_.


[[!include perturbative quantization of Chern-Simons theory -- references]]




[[!redirects quantization of Chern-Simons theory]]

[[!redirects perturbative quantization of 3d Chern-Simons theory]]