
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Phyiscs
+--{: .hide}
[[!include physicscontents]]
=--
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
=--
=--



> This is a sub-entry of [[sigma-model]]. See there for background and context.

***

#Contents#
* table of contents
{:toc}

## Exposition of second-quantization of sigma-models

Low dimensional $\sigma$-models that describe the dynamics of [[particle]]s --  or generally [[brane]]s -- propagating in a [[target space]] $X$ subject to the forces exerted by a [[background field]], such as discussed [above](#ExpositionClassical), are just the first ingredient in a description of the quantum physics _on [[target space]] $X$_ : one is interested in describing a [[quantum field theory]] (or possibly some higher analog, such as a _[[string field theory]]_ ) on $X$, such that the original branes described by the $\sigma$-model are _quanta_ of the fields on $X$. The $\sigma$-model quantum field theory on the [[worldvolumes]] $\Sigma$ is supposed to induce, in turn, another quantum field theory, or something similar, but now on $X$. This process -- or its idea -- goes by the name _[[second quantization]]_ . We shall try to indicate below in which sense this should indeed be a direct iteration of the ("first") quantization of the original $\sigma$-model itself, as described [above](ExpositionQuantization). But we will (have to) be more vague and schematic than before.

Assume now that we started with a classical $\sigma$-model and have quantized it to obtain the [[FQFT|functorial QFT]] 

$$
  Z : Bord_n^S \to Vect
  \,,
$$

which we take here to be 1-categorical (un-[[extended quantum field theory|extended]]), not to overburden the discussion. Assume also for simplicity that the corresponding [[target space]] is of the form $X = Y \times \mathbb{R}$, where the second factor is the time-axis. 

Using this, we define a space of [[state]]s of the _second quantization_  to be the _Fock space_

$$
  \begin{aligned}
    Sym^\bullet(\oplus_{[\Sigma_{n-1}]} Z(\Sigma_{n-1}) )
    & :=
    Sym^\bullet( \mathcal{V} )
    \\
    & \simeq   
    \mathbf{1}
    \oplus 
    \mathcal{V}
    \oplus
    (\mathcal{V} \otimes \mathcal{V})_{sym}
    \oplus
    (\mathcal{V} \otimes \mathcal{V} \otimes \mathcal{V})_{sym}
    \cdots
  \end{aligned}
  \,,
$$

the free commutative [[tensor algebra]] over the vector space $\mathcal{V}$ of [[state]]s of the given single [[particle]], [[string]] or, generally, [[brane]]. This has a contribution for each equivalence class $[\Sigma_{n-1}]$ of connected shapes $\Sigma_{n-1}$ of this brane. For instance for $n = 1$ there is just the point $\Sigma_0 = *$, but for the [[string]] with $n = 2$ there is one contribution from the closed string $\Sigma_1 = S^1$ and one contribution from the open string $\Sigma_1 = [0,1]$; and in turn several contributions of this type if the open string carries boundary [[D-brane]] labels. (In the presence of [[fermion]]s the vector spaces appearing here are [[super vector space]]s and the Fock space construction is the corresponding [[super algebra]] version.)

This space of states is that of a quantum theory whose _classical_ field configurations are given by _many_ states of the original quantum $\sigma$-model. We therefore say that the original brane of shape $\Sigma_{n-1}$ is a _quantum_ or a _single excitation_ of the field theory that it induces on target space $X$: where the original $\sigma$-model describes the dynamics of a single brane on $X$, its second quantization describes the dynamics of many and interacting copies of that brane.

Of course $Sym^\bullet(-) : Vect \to Vect$ is a [[functor]]. This is traditionally stated as the notorious slogan "second quantization is a functor", usually meant to state a contrast with first quantization. Notice however, firstly, that the ("first") quantization of $\sigma$-models -- at least for the version discussed [above](#ExpositionQuantization) -- also is a functor (what is not functorial is the quantization of a random [[Poisson manifold]], but $\sigma$-models carry much more structure than that), and, secondly, that the $Sym^\bullet$-construction is at best half of what second quantization is about: the other half is the description of the _interaction_ of the many branes:

for $X = Y \times (-t,t)$ a piece of target space, the would-be second quantized theory on $X$ should assign a morphism

$$
  S : Sym^\bullet(\mathcal{V}) \to Sym^\bullet(\mathcal{V})
$$

between the space of states of the incoming [[space]] $Y$, to the outgoing space $Y$, here taken to be the same. Usually one assumes here $t = \infty$ and calls $S$ the _[[S-matrix]]_ of the theory, where "S" is for _scattering_ : for $(v^{in}_1 \otimes \dots v^{in}_r) \in Sym^r \mathcal{V}$ the state of $r$ incoming brane quanta and $(v^{out}_1 \otimes \dots v^{out}_s) \in Sym^s \mathcal{V}$ a state of $s$ outgoing brane quanta, the [[matrix]] element

$$
  \left( \left(v^{out}_1 \otimes \dots v^{out}_s\right) , S \left(v^{in}_1 \otimes \dots v^{in}_r\right) \right)
$$

(using an [[inner product space]]-structure on $\mathcal{V}$) is the [[probability amplitude]] for $r$-many branes in the given states propagating through $X$, interacting among each other, thereby transmuting into other states -- hence _scattering off each other_ --  and eventually emerging again in the state $(v^{out}_1 \otimes \dots v^{out}_s)$.

The idea is that this scattering happens in all possible ways that it can happen, with each way weighted by the probability amplitude for it to happen as seen by the quantum $\sigma$-model $Z$: the S-matrix is taken to be given by an expression like

$$
  S 
  :=
  \int_{\Sigma_n \in Bord^S_n}
  Z(\Sigma)
  \,\,
  d\mu(\Sigma)
  \,,
$$

and called the brane _perturbation series_ . For instance the _[[Feynman perturbation series]]_ for $n = 1$, or the _[[string perturbation series]]_ for $n = 2$: we sum over all possible $S$-structured [[cobordism]]s $\Sigma$ -- each representing an interaction "channel" for branes of shape $\partial_{in} \Sigma$ to scatter into shape $\partial_{out} \Sigma$ -- the linear maps $S(\Sigma) : \mathcal{V}_{\partial_{in} \Sigma} \to \mathcal{V}_{\partial_{out} \Sigma}$ weighted by some [[measure]] $d\mu(\Sigma)$, and all regarded as giving one single endomorphism on $Sym^\bullet(\mathcal{V})$ in the evident way.

Except for simple cases, plenty of technical subtleties may have to be taken care of here in order to get anything close to being well defined. For instance there is an [[integral]] over some suitably compactified [[moduli space]] of $S$-structured cobordisms involved. For sufficiently simple but still nontrivial $\sigma$-models this has been made fully precise (for instance for $n = 1$ in standard QFT perturbation theory with [[renormalization]] or for $n = 2$ in the example of [[Gromov-Witten theory]], discussed [above](GWTheory)), and intuition and motivation is drawn from these cases, but in full generality it remains an open problem to fully realize this idea. 

This [[S-matrix]]-construction provides at least the rudiments of a quantum field theory on target space $X$ obtained by second quantization of a $\sigma$-model describing brane dynamics on $X$. 

In application to phenomenological physics we think of $X$ here as our [[spacetime]]. Everything that is measured in particle accelerator experiments is explained with such a construction for $n = 1$. Everything that perturbative [[string theory]] hypothesizes is a refinement of this theory relevant at energies not visible in current accelerator experiments is described with such a construction for $n = 2$. A little bit of investigation has gone into exploring the $n = 3$-case. In principle one could investigate this further for $n \geq 4$.  but so far the jump in complexity given by the step from $n = 1$ to $n = 2$ has kept mankind busy enough. There is already an intricate interrelation of quantum field theories showing up at this level. For instance the second quantization of the 2-dimensional [A-model string](#GWTheory) $\sigma$-model (see there) has be shown to be [[Chern-Simons theory]], which we have seen, [above](#SigmaCS), may itself be understood as a 3-dimensional $\sigma$-model. The second quantization of the non-topological string $\sigma$-model is more complicated but follows this pattern. It contains even [[Yang-Mills theory]] and [[gravity]], and this is what has driven much of the interest in this structure.

Given the evident importance of the "brane perturbation series" or "second quantization" of $\sigma$-models it would be desireable to have a more general abstract and systematic description of it, in the spirit of the [above discussion](#ExpositionQuantization) of general abstract first quantization. Here is an observation that might be suggestive:

we had amplified that the input data for a classical ("0-quantized") $\sigma$-model is a [[background field]] on a target space $X$. At least in nice cases this background field is entirely encoded in its [[higher parallel transport]] and [[holonomy]]-assignment, which is a map

$$
  tra_\nabla : Bord_n(X) \to n Vect
$$

from $n$-dimensional bordisms _in_ $X$ to [[n-vector space]]s (we had mostly discussed an equivalent characteristic morphism $\nabla : X \to \mathbf{B}^n U(1)_{conn}$ and should eventually discuss in more detail how both perspectives are related...). 

The process of ("first") quantization of this $\sigma$-model involves _some_ kind of extension of this functor through the projection to abstract cobordisms

$$
  \array{
    Bord_n^S(X) &\stackrel{tra_\nabla}{\to}& Vect
    \\
    \downarrow & \nearrow_{Z_\nabla}
    \\
    Bord_n^S 
  }
$$

given by the [[path integral]] 

$$
  Z_\nabla :=  \int_{\gamma \in Bord^S_n} tra_\nabla(\gamma) \;\; d \mu(\gamma)
$$

over all trajectories $\gamma : \Sigma \to X$ of given shape $\Sigma$. We saw that second quantization reads in this $Z_\nabla$, in turn, and from the perturbation series

$$
  S := \int_{\Sigma \in Bord^S_n} Z(\Sigma) \; d \mu(\Sigma)
$$

produces a target space quantum field theory. Hence apparently there is a pattern of iterated path integrals, the first over morphisms in $Bord_n^S(X)$, the second over morphisms in $Bord_n^S$:

* classical (0-quantized) $\sigma$-model ([[higher parallel transport]] of [[background gauge field]]): 

  $$
    tra_\nabla : Bord_n^S(X) \to n Vect
    \,;
  $$

* quantum (1st quantized) $\sigma$-model ([[FQFT]]): 

  $$
    Z_\nabla = \int_{\gamma \in Bord^S_n(X)} tra_\nabla(\gamma) \, 
      d\mu(\gamma) : Bord_n^S \to n Vect
    \,;
  $$

* second quantized model ([[S-matrix]]): 

  $$
    S = \int_{\Sigma \in Bord^S_n} Z_\nabla(\Sigma)\, d\mu(\Sigma)
    \,.
  $$

Remember that these formulas are to be taken with a grain of salt. Quite some additional effort is in general needed to make them well-defined. Already in the well-understood case $n = 1$ the [[path integral]] in the expression for $Z_\nabla$ needs attention, then the single terms in the expression for $S$ may still need [[renormalization]] and after all that the sum still may need [[resummation]], at least for models richer than for instance the $\infty$-Dijkgraaf-Witten theories, for which all integrals reduce to finite sums. 
