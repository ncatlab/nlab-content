+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

A _quantum lattice system_ is a [[quantum mechanical system]] whose [[states]]/[[observables]] are arise from basic states/observables assigned to each vertex of some [[lattice]], such as $\mathbb{Z}^d$.

Quantum lattice systems are of relevance in [[solid state physics]], where the lattice typically corresponds to an actual physical lattice of [[atoms]], or as approximations to continuous structures, as in [[lattice gauge theory]].

## Description in AQFT

In the context of [[AQFT]] the typical discussion of a quantum lattice system proceeds as follows.

For $\mathbf{L}$ a [[lattice]], let $P_f(\mathbf{L})$ be its [[poset]] of [[finite set|finite subsets]]. 

Typically there is associated with each lattice site $x \in \mathbf{L}$ a [[Hilbert space]] $\mathcal{H}_x$, typically finite dimensional, $\mathcal{H}_x \simeq \mathbb{C}^d$, representing finitely many physical degrees of freedom at that site (for instance [[spin]] polarizations of a partical). The Hilbert space associated to some $\Lambda \in P_f(\mathbf{L})$ is then typically the [[tensor product]] $\mathcal{H}_\Lambda \coloneqq \otimes_{x \in \Lambda} \mathcal{H}_x$, and hence the corresponding [[algebra of observables]] is that of [[bounded operators]] $\mathcal{A}_\Lambda \coloneqq \mathcal{B}(\mathcal{H}_\Lambda)$.

The complete algebra of observables is then the [[colimit]]/[[inductive limit]]

$$
  \mathcal{A} \coloneqq \underset{\longrightarrow_{\Lambda}}{\lim} \mathcal{A}_\Lambda
  \,.
$$

in the [[category]] of [[C-star algebras]], which is the [[norm]]-closure of the [[union]] of all these algebras. If we call each $\mathcal{A}_{\Lambda}$ a _local algebra_, then this is the algebra of those observables that can be approximated to arbitrary precision in norm by a local algebra. This is called a [[uniformly hyperfinite algebra]].

Next, there is typically for each $\Lambda \in P_f(\mathbf{L})$ a [[Hamiltonian]] $H_\Lambda$ with $\exp(i t H) \in \mathcal{A}_\Lambda$ for all $t \in \mathbb{R}$. Under suitable (subtle) conditions (e.g. [Bratteli-Robinson, part I, chapter 6.2](#BratteliRobinson)) the 1-parameter time evolution $\mathbb{R} \to \mathrm{Aut}(\mathcal{A}_\Lambda)$ induced by this unitary extends to an suitably continuous family of automorphisms of $\mathcal{A}$ (this is no longer given in general by an [[inner automorphism]] even though for each finite $\Lambda$ it is).

## Related concepts

* [[harmonic oscillator]]

* [[hydrogen atom]]

## References

Detailed discussion of quantum lattice systems in [[statistical physics]] formulated with [[AQFT]] tools is in 

* O. Bratteli, D. Robinson, _Operator algebras and quantum statistical mechanics_ Texts and monographs in physics, Springer, New York (part I 1987, part II 1997)
 {#BratteliRobinson}

[[!redirects quantum lattice systems]]
