
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
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

What is called the _A-model_ [[topological string]] is the 2-dimensional [[topological conformal field theory]] corresponding to the [[Calabi–Yau category]] called the [[Fukaya category]] of a [[symplectic manifold]] $(X,\omega)$. This is the [[Poisson sigma-model]] of the underlying [[Poisson manifold]] after appropriate [[gauge fixing]] ([AKSZ 97, p 19](#AKSZ)). The A-model on $X$ is effectively the [[Gromov–Witten theory]] of $X$.

The A-model arose in formal [[physics]] from considerations of [[string theory|superstring]]-propagation on [[Calabi-Yau spaces]]: it may be motivated by considering the [[vertex operator algebra]] of the 2d[[CFT|SCFT]] given by the [[supersymmetric sigma-model]] with [[target space]] $X$ and then deforming it such that one of the super-[[Virasoro algebra|Virasoro]] generators squares to $0$. The resulting "topologically twisted" algebra may then be read as being the [[BRST complex]] of a [[TCFT]].

One can also define an A-model for [[Landau-Ginzburg model|Landau–Ginzburg models]]. The category of [[D-brane|D-branes]] for the corresponding [[open string]] theory is given by the [[Fukaya–Seidel category]].

By [[homological mirror symmetry]], the A-model is dual to the  [[B-model]].

## Properties

### Lagrangian

The [[action functional]] of the A-model is that associated by [[AKSZ theory]] to a Lagrangian [[submanifold]] in a [[target space|target]] [[symplectic Lie n-algebroid]] which is the [[Poisson Lie algebroid]] of a [[symplectic manifold]].

See the _[references on Lagrangian formulation](#LagrangianLit)_.

### Boundary theory / holography

On [[coisotropic submanifold|coisotropic]] [[branes]] in symplectic target manifolds that arise by complexification of [[phase spaces]], the boundary [[path integral]] of the A-model computes the [[quantization]] of that phase space. For details see

* [[quantization via the A-model]].

and

* [[holographic principle]].

### Second quantization / effective background field theory
 {#SecondQuantization}

The [[second quantization]] [[effective field theory|effective]] background field theory defined by the [[perturbation series]] of the A-model string has been argued to be [[Chern-Simons theory]]. ([Witten 92](#Witten92), [Costello 06](#Costello06))

For more on this see at _[TCFT -- Worldsheet and effective background theories](http://ncatlab.org/nlab/show/TCFT#ActionFunctionals)_. A related mechanism is that of _[[world sheets for world sheets]]_.

## Related concepts

* [[schreiber:∞-Chern-Simons theory]]

* [[sigma-model]]

  * [[AKSZ sigma-model]]

    * [[Poisson sigma-model]]

      * **A-model**, [[B-model]]

      * [[half-twisted model]]

    * [[Courant sigma-model]]

      * [[Chern-Simons theory]]

  * [[topological membrane]]

* [[topologically twisted D=4 super Yang-Mills theory]]

* [[Landau-Ginzburg model]]

[[!include gauge theory from AdS-CFT -- table]]


## References

### General

The A-model was first conceived in

* [[Edward Witten]], _Topological sigma models_, Commun. Math. Phys. __118__ (1988) 411--449, [euclid](http://projecteuclid.org/euclid.cmp/1104162092), [MR90b:81080](http://www.ams.org/mathscinet-getitem?mr=0958805)

An early review is in 

* [[Edward Witten]]. _Mirror manifolds and topological field theory_, in: Essays on mirror manifolds, pp. 120&#8211;-158. Int. Press, Hong Kong, 1992. ([arXiv:hep-th/9112056](http://arxiv.org/abs/hep-th/9112056)).


The motivation from the point of view of [[string theory]] is reviewed for instance in

* [[Paul Aspinwall]], _D-Branes on Calabi-Yau Manifolds_ ([arXiv:hep-th/0403166](http://arxiv.org/abs/hep-th/0403166))


A summary of these two reviews is in 

* H. Lee, _Review of topological field theory and homological mirror symmetry_ ([pdf](http://people.maths.ox.ac.uk/leeh/files/CYMSmini.pdf))


### Action functional {#LagrangianLit}

That the A-model [[Lagrangian]] arises in [[AKSZ theory]] by [[gauge fixing]] the [[Poisson sigma-model]] was observed in

* {#AKSZ} M. Alexandrov, [[Maxim Kontsevich|M. Kontsevich]], [[Albert Schwarz|A. Schwarz]], O. Zaboronsky, around page 19 in _The geometry of the master equation and topological quantum field theory_, Int. J. Modern Phys. A 12(7):1405--1429, 1997

with more details in 

* {#BonechiCattaneoIraso16} Francesco Bonechi, [[Alberto Cattaneo]], Riccardo Iraso, _Comparing Poisson Sigma Model with A-model_ ([arXiv:1607.03411](http://arxiv.org/abs/1607.03411))

Review and further discussion includes

* Francesco Bonechi, [[Maxim Zabzine]], section 5.3 of _Poisson sigma model on the sphere_ ([arXiv:0706.3164](http://arxiv.org/abs/0706.3164))

Also

* [[Noriaki Ikeda]], _Deformation of graded (Batalin-Volkvisky) Structures_, in Dito, Lu, Maeda, [[Alan Weinstein]] (eds.) _Poisson geometry in mathematics and physics_ Contemp. Math. 450, AMS (2008) 

Discussion of how the [[second quantization]] [[effective field theory]] given by the A-model [[perturbation series]] is [[Chern-Simons theory]] is in

* [[Edward Witten]], _Chern-Simons Gauge Theory As A String Theory_, Prog.Math. 133 (1995) 637-678 ([arXiv:hep-th/9207094](http://arxiv.org/abs/hep-th/9207094))
 {#Witten92}

* [[Kevin Costello]], _Topological conformal field theories and gauge theories_ ([arXiv:math/0605647](http://arxiv.org/abs/math/0605647))
 {#Costello06}

formalizing at least aspects of the observations in


[[!redirects A-model]]
[[!redirects A-models]]