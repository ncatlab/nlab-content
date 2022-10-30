

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

+-- {: .num_prop #CompatibiltyOfFlowWithPolarization}
###### Proposition

A prequantum operator given by a [[Hamiltonian]] function $f$ with [[Hamiltonian vector field]] $v_f$ is a quantum operator, def. \ref{GeometricQuantumOperator}, with respect to a given [[polarization]] $\mathcal{P}$ precisely if its flow preserves $\mathcal{P}$, hence precisely if

$$
  [v_f, \mathcal{P}] \subset \mathcal{P}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

If $\mathcal{P}$ is a [[Kähler polarization]] then its underlying [[almost complex structure]] it induces a [[spin^c structure]], as discussed there. If $ \rho \colon G \to QuantMorph(X,\nabla)$ is a [[Hamiltonian action]] (a homomorphism to the [[quantomorphism group]]) such that each prequantum operator $\rho(g)$ is a quantum operator in that it preserves the polarization, by prop. \ref{CompatibiltyOfFlowWithPolarization}, then the corresponding [[spin^c structure]] is $G$-invariant. Accordingly the [[index]] of the [[spin^c Dirac operator]] which gives the [geometric quantization by cohomological quantization](http://ncatlab.org/nlab/show/geometric%20quantization#AsIndexOfSpinCDiracOperator) exists not just in [[K-theory]], where it yields the [[space of quantum states]], but even in $G$-[[equivariant K-theory]], exhibiting a [[representation]] of $G$ on the Hilbert space. This is the action of the quantum observables given by $\rho$ from the point of view of cohomological quantization.

=--

+-- {: .num_example}
###### Example

Over a phase space which is a [[cotangent bundle]] and with respect to the corresponding canonical vertical polarization, a Hamiltonian function is a quantum operator precisely if it is at most linear in the [[canonical momenta]].

=--

See for instance ([Blau, around p. 35](#Blau))




### On an $n$-plectic smooth $\infty$-groupoid

(...)

### Irreducible representations and superselection sectors

The [[space of quantum states]] forms a linear [[representation]] of a given [[algebra of observables]]. The decomposition of that into [[irreducible representations]] is physically the decomposition into [[superselection sectors]].

## Related concepts

* [[observable]]

* [[Jordan algebra]], [[Bohr topos]]

* [[effect algebra]]

* [[Hamiltonian operator]]


## References

See the references at [[geometric quantization]].

Standard facts are recalled for instance around p. 35 of

* [[Matthias Blau]], _Symplectic Geometry and Geometric Quantization_ ([[BlauGeometricQuantization.pdf:file]])
 {#Blau}

Computation of quantum observables by [[index]] maps in [[equivariant K-theory]] is in (see specifically around p. 8 and 9)


* [[Michèle Vergne]], _Geometric quantization and equivariant cohomology_ ([pdf](http://www.math.jussieu.fr/~vergne/pageperso/articles/CONGEURO.pdf))

[[!redirects quantum observables]]

[[!redirects quantum operator]]
[[!redirects quantum operators]]

