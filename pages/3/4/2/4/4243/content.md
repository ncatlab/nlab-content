
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

* [[Edward Witten]], _Topological sigma models_, Commun. Math. Phys. **118** (1988) 411--449, &lbrack;[doi:10.1007/BF01466725](https://doi.org/10.1007/BF01466725), [MR90b:81080](https://www.ams.org/mathscinet-getitem?mr=0958805)&rbrack;

An early review is in 

* [[Edward Witten]]. _Mirror manifolds and topological field theory_, in: Essays on mirror manifolds, pp. 120&#8211;-158. Int. Press, Hong Kong, 1992. ([arXiv:hep-th/9112056](http://arxiv.org/abs/hep-th/9112056)).


The motivation from the point of view of [[string theory]] is reviewed for instance in

* [[Paul Aspinwall]], _D-Branes on Calabi-Yau Manifolds_, In _Theoretical Advanced Study Institute in Elementary Particle Physics (TASI 2003): Recent Trends in String Theory_, pages 1-152, Boulder, USA, June 2-27, 2003. &lbrack;[arXiv:hep-th/0403166](https://arxiv.org/abs/hep-th/0403166), [doi:10.1142/9789812775108_0001](https://doi.org/10.1142/9789812775108_0001)&rbrack;


A summary of these two reviews is in 

* H. Lee, _Review of topological field theory and homological mirror symmetry_ ([pdf](http://people.maths.ox.ac.uk/leeh/files/CYMSmini.pdf))


### Action functional {#LagrangianLit}

That the A-model [[Lagrangian]] arises in [[AKSZ theory]] by [[gauge fixing]] the [[Poisson sigma-model]] was observed in

* {#AKSZ} M. Alexandrov, [[Maxim Kontsevich|M. Kontsevich]], [[Albert Schwarz|A. Schwarz]], O. Zaboronsky, _The geometry of the master equation and topological quantum field theory_, Int. J. Modern Phys. A **12** 7 (1997) 1405--1429 &lbrack;[arXiv:hep-th/9502010](https://arxiv.org/abs/hep-th/9502010), [doi:10.1142/S0217751X97001031](https://doi.org/10.1142/S0217751X97001031)&rbrack;

with more details in 

* {#BonechiCattaneoIraso16} Francesco Bonechi, [[Alberto Cattaneo]], Riccardo Iraso, _Comparing Poisson Sigma Model with A-model_, JHEP **10** (2016) 133 &lbrack;[arXiv:1607.03411](https://arxiv.org/abs/1607.03411), [doi:10.1007/JHEP10(2016)133](https://doi.org/10.1007/JHEP10(2016)133)&rbrack;

Review and further discussion includes

* Francesco Bonechi, [[Maxim Zabzine]], _Poisson sigma model on the sphere_, Commun.Math.Phys. **285** (2009) 1033-1063 &lbrack;[arXiv:0706.3164](https://arxiv.org/abs/0706.3164), [doi:10.1007/s00220-008-0615-1](https://doi.org/10.1007/s00220-008-0615-1)&rbrack;

Also

* [[Noriaki Ikeda]], _Deformation of graded (Batalin-Volkvisky) Structures_, in Dito, Lu, Maeda, [[Alan Weinstein]] (eds.) _Poisson geometry in mathematics and physics_ Contemp. Math. 450, AMS (2008) 

Discussion of how the [[second quantization]] [[effective field theory]] given by the A-model [[perturbation series]] is [[Chern-Simons theory]] is in

* [[Edward Witten]], _Chern-Simons Gauge Theory As A String Theory_, Prog.Math. **133** (1995) 637-678 &lbrack;[arXiv:hep-th/9207094](https://arxiv.org/abs/hep-th/9207094), [doi:10.1007/978-3-0348-9217-9_28](https://doi.org/10.1007/978-3-0348-9217-9_28)&rbrack;
 {#Witten92}

* [[Kevin Costello]], _Topological conformal field theories and gauge theories_, Geom.Topol. **11** 3 (2007) 1539-1579 &lbrack;[arXiv:math/0605647](https://arxiv.org/abs/math/0605647), [doi:10.2140/gt.2007.11.1539](https://doi.org/10.2140/gt.2007.11.1539)&rbrack;
 {#Costello06}

formalizing at least aspects of the observations in


[[!redirects A-model]]
[[!redirects A-models]]