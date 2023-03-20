
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Broadly, by *deformation quantization* one means notions of [[quantization]] of [[Poisson manifolds]] $\big(X, \{-,-\}\big)$ in terms of [[sequences]] of [[noncommutative algebra|non-commutative]] [[algebras]] $A_{\hbar}$ parameterized by specific admissible (formal) values of [[Planck's constant]] $\hbar$ including $\hbar = 0$, where $A_0 = C^\infty(X)$ is the ordinary commutative [[algebra of functions]] on the [[underlying]] [[smooth manifold]]. The idea is that $A_{\hbar}$ is the [[algebra of observables]] of the corresponding [[quantum system]] at that value of $\hbar$, arising from "deforming" the commutative product of $A_0$ in a way that increases with $\hbar$ and is [[infinitesimal|infinitesimally]] controlled by the given [[Poisson bracket]] $\{-,-\}$.

Deformation quantization is often taken by default to refer to the historically first notion of

* **[[formal deformation quantization]]**,

where $\hbar$ is just a formal [[variable]] (i.e. an [[infinitesimal]], but not an actual [[number]]) and the [[underlying]] [[vector space]] of all algebras in question is that of [[formal power series]] in $\hbar$.

One might naively imagine that the [[formal power series]] appearing in [[formal deformation quantization]] have a finite [[radius of convergence]] $\epsilon \in \mathbb{R}_+$ thus yielding actual (non-formal) deformation quantizations for $\hbar \lt \epsilon$, but in practice this happens rarely (see reference [here](C*+algebraic+deformation+quantization#ConvergingFormalDeformationQuantization)). Indeed, [[geometric quantization]] makes manifest that [[prequantization]] conditions typically force admissible values of [[Planck's constant|$\hbar$]] to form a [[discrete space|discrete]] [[subspace]] of $\mathbb{R}_+$ with only an [[accumulation point]] at $\hbar = 0$ (namely, in [[geometric quantization]] the inverse $1/\hbar$ is typically constrained to come in [[natural number|integral]] multiples).

Therefore, beyond formal deformation quantization there are notions of 

* **[[strict deformation quantizations]]**

where $\hbar$ is allowed to take discrete [[positive number|positive]] [[real numbers|real values]] with an [[accumulation point]] at $\hbar = 0$, and where to each such value is associated an actual [[C*-algebra]]-[[algebra of observables|of observables]].

In its focus on [[algebras of observables]] the notion of deformation quantization is roughly dual to *[[geometric quantization]]*, which primarily constructs the [[spaces of quantum states]]. In special sitations both notions are compatible, but in general there is a large amount of ambiguity in [[quantization]], between but also within the different approaches.

## Related entries

* [[geometric quantization]]

* algebraic quantization

  * [[formal deformation quantization]]

  * [[strict deformation quantization]]

[[!redirects deformation quantizations]]

