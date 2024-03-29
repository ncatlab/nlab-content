
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# The Legendre transformation
* table of contents
{: toc}

## Idea

The _Legendre transformation_ is an operation on [[convex function]]s from a real [[normed vector space]] to the [[real line]]; it is one of the cornerstones of [[convex analysis]]. The space of arguments changes accordingly.


## Definition
 {#Definition}

Two [[differentiable functions]] $f, \tilde f \;\colon\; \mathbb{R} \to \mathbb{R}$ on the [[real line]] are said to be _Legendre transforms_ of each other, if their [[derivatives]] $D f, D\tilde f \;\colon\; \mathbb{R} \to \mathbb{R}$ are [[inverse functions]] of each other:

$$
  \label{DerivativesOfLegendreTransformsAreInverseFunctions}
  D f \circ D \tilde f = id 
  \phantom{AAA}
  D \tilde f \circ D f = id 
$$

## In classical mechanics -- Hamiltonians and Lagrangians

The main application of and the historical root of the notion of Legendre transform (in [[differential geometry]]) is in [[classical physics]] and its formalization by [[symplectic geometry]]. In [[classical mechanics]], the [[Hamiltonian]] function $H$ is a Legendre transform of the [[Lagrangian]] $L$ and vice versa. 

When one formalizes [[classical mechanics]] as the [[local prequantum field theory]] given by [[prequantized Lagrangian correspondences]], then the Legendre transform is exhibited by the lift from a [[Lagrangian correspondence]] to a [[prequantized Lagrangian correspondence]]. For more on this see at _[The classical action, the Legendre transform and Prequantized Lagrangian correspondences](prequantized+Lagrangian+correspondence#HamiltonianTrajectoriesAndPrequantizedLagrangianCorrespondences)_.
 
In many dimensions, hybrid versions are possible. When the physics of the system is given by the [[variational calculus|variational principle]], then the Legendre transform of an extremal quantity is a conserved quantity. In [[thermodynamics]], we can have some quantities set to be fixed (some candidates: entropy $S$, temperature $T$, pressure $P$, volume $V$, magnetization $M$); this dictates the choice of variables and quantity which is extremized as well as which one takes the role of conserved energy. Some of the standard choices are enthalpy $H$, Helmholtz free energy $F$, Gibbs free energy $G$, internal energy $U$, etc. 

See also [wikipedia:Legendre transformation](http://ncatlab.org/nlab/edit/Legendre+transformation) and [wikipedia:Legendre-Fenchel transformation](http://en.wikipedia.org/wiki/Legendre-Fenchel_transformation); the two wikipedia articles have much detail in certain specific approaches and cases, but also miss some of the basic ones to be balanced. 


### Via prequantized Lagrangian correspondences

See at _[[prequantized Lagrangian correspondence]]_.


### In multisymplectic geometry

See at _[multisymplectic geometry -- de Donder-Weyl-hamilton equations of motion](multisymplectic+geometry#DonderWeylHamiltonFieldEquations)_.


## Related concepts

* [[canonical coordinates]], [[canonical momenta]]

[[!include Hamiltonian and Lagrangian -- table]]

* [[Relation with Fourier transform]]

... tropical

## References 

The concept is named after [[Adrien-Marie Legendre]].

Reviews include

* Torontowiki: [Legendre Transformation](http://wiki.math.toronto.edu/TorontoMathWiki/index.php/Legendre_Transformation)

See also

* Wikipedia, _[Legendre transformation](https://en.wikipedia.org/wiki/Legendre_transformation)_

Discussion of Legendre transformation in the context of [[Lie algebroids]] is in:

* Paulette Liberman, _Lie algebroids and mechanics_ ([ps](http://emis.math.ecnu.edu.cn/journals/AM/96-3/liber.ps))

* Jorge Cortes et al, _A survey of Lagrangian mechanics and control on Lie algebroids and Lie groupoids_ ([arxiv](https://arxiv.org/abs/math-ph/0511009))

* Juan Carlos Marrero, _Nonholonomic mechanics: a Lie algebroid perspective_ ([pdf talk notes](http://www.gmcnetwork.org/files/eia08/talks/Talk-Santiago08-JuanCarlosMarrero.pdf))


category: physics

[[!redirects Legendre transform]]
[[!redirects Legendre transforms]]
[[!redirects Legendre transformation]]
[[!redirects Legendre transformations]]
[[!redirects Legendre transfomation]]
