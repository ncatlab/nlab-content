
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

What is called _Bohmian mechanics_ or _de Broglie-Bohm theory_ is a rewriting of the [[Schrödinger equation]] of [[quantum mechanics]] in a way that makes it look -- away from the [[zero locus]] of its solutions -- like discribing a [[diffusion]] process subject to an unusual (for ordinary diffusion) potential. There is a [[stochastic process]] modelling this diffusion ([Nelson 66](#Nelson66)) and the point of view expressed by _Bohmian mechanics_ is to regard this as a [[hidden variable theory]] of [[quantum mechanics]].

Specifically, for the simple [[mechanical system]] of a [[particle]] of [[mass]] $m$ propagating on the [[real line]] $\mathbb{R}$ and subject to a [[potential]] $V \in C^\infty(\mathbb{R})$, the [[Schrödinger equation]] is the [[differential equation]] on [[complex number|complex]]-valued [[functions]] $\Psi \colon \mathbb{R}\times \mathbb{R} \to \mathbb{C}$ given by

$$
  i \hbar
  \frac{\partial}{\partial t}
  \Psi
  =
  \frac{\hbar^2}{2m}
  \frac{\partial^2}{\partial^2 x} \Psi
  + 
  V \Psi
  \,,
$$

where $\hbar$ denotes [[Planck's constant]].

By the nature of [[complex numbers]] and by the discussion at _[[phase and phase space in physics]]_, it is natural to parameterize $\Psi$ -- away from its [[zero locus]] -- by a [[complex phase]] function

$$
  S \;\colon\; \mathbb{R}\times \mathbb{R} \longrightarrow \mathbb{R}
$$

and an [[absolute value]] function $\sqrt{\rho}$

$$
  \sqrt{\rho} \;\colon\; \mathbb{R}\times \mathbb{R} \longrightarrow \mathbb{R}
$$

which is positive, $\sqrt{\rho} \gt 0$, as

$$
  \Psi 
    \coloneqq 
  \exp\left(\frac{i}{\hbar} S / \hbar\right) \sqrt{\rho}
  \,.
$$

Entering this Ansatz into the above [[Schrödinger equation]], that [[complex number|complex]] equation becomes equivalent to the following two [[real number|real]] equations:

$$
  \frac{\partial}{\partial t} S
  = 
  - 
  \frac{1}{2m} \left(\frac{\partial}{\partial x}S\right)^2
  - 
  V
  + 
  \frac{\hbar^2}{2m} \frac{1}{\sqrt{\rho}}\frac{\partial^2}{\partial^2 x} \sqrt{\rho}
$$

and

$$
  \frac{\partial}{\partial t} \rho
  = 
  -
  \frac{\partial}{\partial x}
  \left(
    \frac{1}{m} \left(\frac{\partial}{\partial x}S\right) \rho
  \right)
  \,.
$$

Now in this form one may notice a similarity of the form of these two equations with other equations from [[classical mechanics]] and [[statistical mechanics]]:

1. The first equation is similar to the [[Hamilton-Jacobi equation]] that expresses the classical [[action functional]] $S$ and the [[canonical momentum]]

   $$
     p \coloneqq \frac{\partial}{\partial x} S
   $$

   except that in addition to the ordinary [[potential energy]] $V$ there is an additional term

   $$
    Q 
      \coloneq
    \frac{\hbar^2}{2m} \frac{1}{\sqrt{\rho}}\frac{\partial^2}{\partial^2 x} \sqrt{\rho}
   $$

   which is unlike what may appear in an ordinary [[Hamilton-Jacobi equation]]. The perspective of Bohmian mechanics is to regard this as a correction of [[quantum physics]] to classical [[Hamilton-Jacobi theory]], it is then called the _quantum potential_. Notice that unlike ordinary potentials, this "quantum potential" is a function of the density that is subject to the potential. (Notice that this works only away from the [[zero locus]] of $\rho$.)

1. The second equation has the form of the [[continuity equation]] of the [[flow]] expressed by $\frac{1}{m}p$.

The perspective of Bohmian mechanics is to regard this equivalent rewriting of the [[Schrödinger equation]] as providing a [[hidden variable theory]] formulation of [[quantum mechanics]].

The bulk of the discussion of Bohmian mechanics in the literature revolves around [[philosophy|philosophical]] implications of this perspective, e.g. ([Stanford Enc. Philosph](#SEP)).

## Related concepts

* [[interpretation of quantum mechanics]]

## References

Named after:

* [[David Bohm]], *A Suggested Interpretation of the Quantum Theory in Terms of "Hidden" Variables. I*, Phys. Rev. **85** (1952) 166 &lbrack;[doi:10.1103/PhysRev.85.166](https://doi.org/10.1103/PhysRev.85.166)&rbrack;

* [[David Bohm]], *A Suggested Interpretation of the Quantum Theory in Terms of "Hidden" Variables. II*, Phys. Rev. **85** (1952) 180 &lbrack;[doi:10.1103/PhysRev.85.180](https://doi.org/10.1103/PhysRev.85.180)&rbrack;


See also:

* Wikipedia, *[De Broglie–Bohm theory](https://en.wikipedia.org/wiki/De_Broglie–Bohm_theory)*

* {#SEP} Stanford Encyclopedia of Philosophy, _[Bohmian mechanics](http://plato.stanford.edu/entries/qm-bohm/)_
  

The formulation of the exotic diffusion process described by the phase part of the Schr&#246;dinger equation as a [[stochastic process]] is due to 

* {#Nelson66} [[Edward Nelson]], _Derivation of the Schr&#246;dinger equation from Newtonian mechanics_, Phys. Rev. 150, 1079&#8211;1085, 1966
  

* [[Edward Nelson]], _Quantum Fluctuations_, Princeton University Press, Princeton. 1985

A review of this relating to Bohmian mechanics:

* Guido Bacciagaluppi, _A Conceptual Introduction to Nelson's
Mechanics_ &lbrack;[pdf](http://philsci-archive.pitt.edu/8853/1/Nelson-revised.pdf)&rbrack;

The surreal trajectory problem is pointed out in

* B.-G. Englert, M. O. Scully, G. S&#252;ssmann, H. Walther, *Surrealistic Bohm trajectories*, Z. Naturforsch. **47**a  (1992) 1175-1186

The following two articles offer solution to the surreal trajectory problem:

* D. H. Mahler et al. _Experimental nonlocal and surreal Bohmian trajectories_, Science Advances __2__:2, e1501466 (2016) &lbrack;[doi:10.1126/sciadv.1501466](https://doi.org/10.1126/sciadv.1501466)&rbrack;

* B. J. Hiley, R. Callaghan, O. Maroney, Quantum trajectories, real, surreal or an approximation to a deeper process? &lbrack;[quant-ph/0010020](http://arxiv.org/abs/quant-ph/0010020)&rbrack;

category: physics

[[!redirects pilot-wave theory]]
[[!redirects Bohmian quantum mechanics]]