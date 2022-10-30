

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
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

An [[observable]] in [[quantum physics]].

## Definition in geometric quantization

We consider the notion of quantum observables in the the context of [[geometric quantization]]. See also [[quantum operator (in geometric quantization)]].

### On a symplectic manifold
 {#OnASymplecticManifold}

Let $(X, \omega)$ be a ([[presymplectic manifold|pre]]-)[[symplectic manifold]], thought of as the [[phase space]] of a [[classical mechanics|physical system]].

Assume that $\omega$ is prequantizabe (integral) and let $\nabla : X \to \mathbf{B} U(1)_{conn}$ be a
[[prequantum bundle]] $E \to X$ [[connection on a bundle|with connection]] for $\omega$, hence with [[curvature]] $F_\nabla = \omega$. Write $\Gamma_X(E)$ for the space of smooth [[sections]] of the [[associated bundle|associated]] [[complex line bundle]]. This is  the _prequantum space of states_.


+-- {: .num_defn}
###### Definition

For $f \in C^\infty(X, \mathbb{C})$ a function on phase space, the corresponding **pre-quantum operator** is the linear map on prequantum states

$$
  \hat f : \Gamma_X(E) \to \Gamma_X(E)
$$

given by

$$
  \psi \mapsto -i \nabla_{v_f} \psi + f \cdot \psi
  \,,
$$

where 

* $v_f$ is the [[Hamiltonian vector field]]
corresponding to $f$;

* $\nabla_{v_f} : \Gamma_X(E) \to \Gamma_X(E)$ is the [[covariant derivative]] of sections along $v_f$ for the given choice of prequantum connection;

* $f \cdot (-) : \Gamma_X(E) \to \Gamma_X(E)$ is the operation of degreewise multiplication pf sections.

=--

+-- {: .num_remark}
###### Remark

In terms of [[schreiber:Higher geometric prequantum theory]] we may, as discussed there, identify the [[Poisson bracket]] [[Lie algebra]] $\mathfrak{Poisson}(X,\omega)$ with the Lie algebra of the group of automorphism $\exp(O) \colon \nabla \stackrel{\simeq}{\to} \nabla$ regarded in the [[slice (∞,1)-topos|slice]] over $\mathbf{B}U(1)_{conn}$. Moreover, the space of sections is equivalently the space of maps $\Psi \colon \nabla \to \mathbb{C}//U(1)_{conn}$ in the slice from $\nabla$ into the differential refinement of the smooth universal line bundle $\mathbb{C}//U(1) \to \mathbf{B}U(1)$. In this formulation the action of prequantum operators is just the precomposition action

$$
  \widehat{\exp(O)} \colon (\nabla \stackrel{\Psi}{\to} \mathbb{C}//U(1)_{conn})
  \mapsto 
  (\nabla \stackrel{exp(O)}{\to} \nabla \stackrel{\Psi}{\to} \mathbb{C}//U(1)_{conn})
  \,.
$$

=--

Now after a choice of [[polarization]] a [[quantum state]] is a prequantum [[wave function]] which is covariantly constant along the [[Lagrangian submanifolds]] of the foliation. Not all prequantum operators will respect the space of such quantum states inside all quantum states. Those that do become genuine quantum operators.

+-- {: .num_defn #GeometricQuantumOperator}
###### Definition

Let $\mathcal{P}$ be a [[polarization]] of the [[symplectic manifold]] $(X,\omega)$. then a [[quantum state]] or [[wavefunction]] is a prequantum state $\psi$ such that $\nabla \Psi$ vanishes along the [[leaves]] of the polarization. 

A **quantum operator** is a prequantum operator which preserves quantum states among all prequantum states.

=--

+-- {: .num_prop}
###### Proposition

A prequantum operator given by a [[Hamiltonian]] function $f$ with [[Hamiltonian vector field]] $v_f$ is a quantum operator, def. \ref{GeometricQuantumOperator}, with respect to a given [[polarization]] $\mathcal{P}$ precisely if its flow preserves $\mathcal{P}$, hence precisely if

$$
  [v_f, \mathcal{P}] \subset \mathcal{P}
  \,.
$$

=--

+-- {: .num_example}
###### Example

Over a phase space which is a [[cotangent bundle]] and with respect to the corresponding canonical vertical polarization, a Hamiltonian function is a quantum operator precisely if it is at most linear in the [[canonical momenta]].

=--

See for instance ([Blau, around p. 35](#Blau))

### On an $n$-plectic smooth $\infty$-groupoid

(...)

## Related concepts

* [[observable]]

* [[Hamiltonian operator]]

* [[effect algebra]]

## References

See the references at [[geometric quantization]].

Relevant lecture notes include

* [[Matthias Blau]], _Symplectic Geometry and Geometric Quantization_ ([[BlauGeometricQuantization.pdf:file]])
 {#Blau}


[[!redirects quantum observables]]

[[!redirects quantum operator]]
[[!redirects quantum operators]]

