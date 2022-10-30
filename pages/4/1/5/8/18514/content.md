

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _causal propagator_ or _Pauli-Jordan distribution_ is a [[distribution]] which encodes the [[Poisson bracket]] on the [[covariant phase space]] of a [[free field|free]] [[local field theory]] (also known as the _[[Peierls bracket]]_).

Specifcally for the [[free field|free]] [[scalar field]] on a [[spacetime]] $\Sigma$, its [[phase space]] is the space $ker(\Box + m^2) \hookrightarrow C^\infty(\Sigma)$ of solutions of the [[Klein-Gordon equation]] (the [[wave equation]] for vanishing [[mass]] $m$). For any  point $x \in \Sigma$ we denote by $\phi(x) \colon ker(\Box + m^2) \to \mathbb{R}$ the point [[evaluation]] [[functional]] which sends $\Phi \in C^\infty(\Sigma)$ to $\Phi(x)$. An [[observable]] of the scalar field is then a [[functional]] of the form $\phi(b) \coloneqq \int b(x) \phi(x) dvol(x)$, for $b$ a [[bump function]] on $\Sigma$. On the algebra of these observables there is a canonical [[Poisson bracket]] pairing defined (also known as the _[[Peierls bracket]]_ see at _[[scalar field]]_ for details), taking $\phi(b_1)$ and $\phi(b_2)$ to a new observable denoted $\{\phi(b_1), \phi(b_2)\}$. While a priori this Poisson bracket is defined only on the "smeared" observables $\phi(b)$, not on the point observables $\phi(x)$, nevertheless it has a [[distributional density|distributional]] [[integral kernel]] $\{\phi(x), \phi(y)\}$ such that

$$
  \{ \phi(b_1), \phi(b_2) \}
  = 
  \int b_1(x) b_2(y) \{\phi(x), \phi(y)\} dvol_{\Sigma}(x) dvol_\Sigma(y)
  \,.
$$

This [[distribution|distributional]] [[integral kernel]] 

$$
  \Delta(x,y) \coloneqq \{\phi(x), \phi(y)\}
$$ 

is the _causal propagator_ or _Pauli-Jordan distribution_ (also "commutator function"). This happens to be a [[fundamental solution]]/[[Green function]] to the [[Klein-Gordon operator]] $\Box + m^2$, whence a "[[propagator]]".

For other [[free fields]] [[field (physics)|fields]] the [[integral kernel]] of their [[Poisson bracket]] is a more complicated expression, but it is typically still an expression in terms of the causal propagator of the scalar field.

What is _causal_ about the causal propagator is that (on [[globally hyperbolic spacetimes]] such as [[Minkowski spacetime]]) its [[support of a distribution|support as a distribution]], is, for one of the two arguments fixed, the union of the [[past causal cone]] and the [[future causal cone]] of that point. On [[globally hyperbolic spacetimes]] the propagator splits, as a distribution, as a sum

$$
  \Delta = \Delta_R - \Delta_A
$$

where the [[retarded propagator]] $\Delta_R$ and the [[advanced propagator]] $\Delta_A$ are such that their [[support of a distribution|support]] is, for fixed second argument, in the [[past causal cone]] and in the [[future causal cone]], respectively.

## Definition

### On Minowski spacetime

### On general globally hyperbolic spacetimes

Let $(X,g)$ be a [[time orientation|time-oriented]] [[globally hyperbolic spacetime]] and let $m \in \mathbb{R}_{\geq 0}$ (the "[[mass]]"). Then the [[Klein-Gordon equation]]

$$
  (\Box_g - m^2) \phi = 0
$$

(a [[partial differential equation]] on [[smooth functions]] $f \in C^\infty(X,\mathbb{R})$ ) has unique advanced and retarded [[Green functions]] $E^{R/A}$, namely [[continuous linear functionals]]

$$
  E^{A/R} 
   \;\colon\;
  C^\infty_c(X)
   \longrightarrow
  C^\infty(X)
$$

(from [[bump functions]] to general [[smooth functions]]) which are [[fundamental solutions]] in that 

$$
  (\Box_g - m^2) \circ E^{A/R} = \delta
  \phantom{AAAA}
  E^{A/R} \circ (\Box_g - m^2) = \delta
$$

and which have advanced/retarded [[support of a distribution]] when viewed (via the [[Schwartz kernel theorem]]) as [[distributions]] on the [[Cartesian product]] manifold $X \times X$

$$
  supp( E^{A/R}) \subset \{ (x_1, x_2) \in X \times X  \;\vert\; x_1 \in J^{\mp} (x_2) \}
 \,.
$$

In fact these two fundamental solutions are related by switching their arguments 

$$
  E^{A/R}(x_1, x_2) = E^{R/A}(x_2, x_1)
  \,.
$$

The differene

$$
  E \;\coloneqq\; E^A - E^R
$$

is called the _causal propagator_ or the _Jordan-Pauli distribution_ ([Jordan-Pauli 27](#JordanPauli27)).

[[!include propagators - table]]


## Properties

The causal propagator yields the [[Peierls bracket]], which is the [[Poisson bracket]] on the [[covariant phase space]] of the [[free field|field]] [[scalar field|scalar]] [[field (physics)|field]]. The [[Moyal deformation quantization]] of this [[covariant phase space]] yields the [[Wick algebra]] of [[quantum observables]] of the free scalar field.


## Related concepts

* [[Feynman propagator]]

* [[Hadamard propagator]]

## References

The causal propagator was first considered (in the context of [[quantum electrodynamics]]) in 

* {#JordanPauli27} [[Pascual Jordan]], [[Wolfgang Pauli]], _Zur Quantenelektrodynamik ladungsfreier Felder_, Zeitschrift f&#252;r Physik 47, 151 (1928)

whence often called the _Jordan-Pauli distribution_.

Textbook discussion for [[free fields]] in [[Minkowski spacetime]] is in

* {#Scharf95} [[Günter Scharf]],  section 2.3 of _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Springer 1995

* [[Günter Scharf]], section 1 of  _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001

(there denoted "$-i D_m(x-y)$" and called the "Jordan-Pauli function").


For more see the references at _[[wave equation]]_.

[[!redirects causal propagators]]

[[!redirects causal Green function]]
[[!redirects causal Green functions]]

[[!redirects Jordan-Pauli distribution]]
[[!redirects Jordan-Pauli distributions]]


[[!redirects Pauli-Jordan distribution]]
[[!redirects Pauli-Jordan distributions]]
