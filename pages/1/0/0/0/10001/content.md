
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

A deformation of [[super Yang-Mills theory]] that yields a [[topological field theory]] in 4 [[dimensions]]. This is in higher dimensional analogy to how the [[topological string]]-[[topological twist|twisting]] of the [[superstring]] yields the topological [[A-model]] and [[B-model]] 2d topological field theories.

### For $N = 4$ supersymmetry

Given [[N=4 D=4 super Yang-Mills theory]], the twisting is induced by a choice of [[subgroup]] inclusion of the [[special orthogonal group]] $SO(4)$ into the [[R-symmetry]] group $SO(6)$. Then choose a [[supersymmetry]] $Q$ which is invariant under the resulting combined action of $SO(4)$ on [[spacetime]] and via [[R-symmetry]] and consider the subspace of [[quantum states]]/[[quantum observables]] which are in the [[kernel]] of $Q$. This subspace defines a [[topological field theory]] which is called the corresponding twisted topological super Yang-Mills theory.

Before the twisting super [[Yang-Mills theory]] depends on the complex [[coupling constant]] 

$$
  \tau = \frac{\theta}{2\pi} + \frac{4 \pi i }{g_{YM}^2}
$$ 

(with $\theta$ the _[[theta angle]]_), after the twisting there is an additional complex parameter $t$ encoding the choice of topological supercharge. The twisted theory however only depends on the combination

$$
  \Psi \coloneqq \frac{\theta}{2 \pi}  + 
  \frac{4 \pi i}{g_{YM}^2} 
  \frac{t - t^{-1}}{t + t^{-1}}
  \,.
$$

([Witten 11, p. 29](#Witten11))

The resulting [[4d TQFT]] is also called the _[[Kapustin-Witten TQFT]]_.

### For $N = 2$ supersymmetry

For [[N=2 D=4 super Yang-Mills theory]] the twisting follows the same idea, but is a little but more intricate ([Witten 11, section 5.1.1](#Witten11))

### Table of relations via holographic, compactifications and twists

[[!include gauge theory from AdS-CFT -- table]]


## Formalization
 {#Formalization}

A formalization of the topological twisting in the framework of [[perturbation theory|perturbative]] [[BV-quantization]] of field theory via [[factorization algebras]] of local [[quantum observables]] is proposed in ([Costello 11, section 15, 16, ...](#Costello11)).

The definition there essentially amounts to saying that a choice of topological twisting is a choice of [[action]] of the [[semidirect product]] [[supergroup]]

$$
  \mathbb{G}_m \ltimes \Pi \mathbb{G}_{ad}
$$

of the [[multiplicative group]] acting on the odd-shifted [[additive group]] via the given [[super Poincare Lie algebra]]. 

We notice that this group is the [automorphism group of the odd line](odd%20line#TheAutomorphismSuperGroup)

$$
  \mathbf{Aut}(\mathbb{R}^{0|1}) \simeq \mathbb{G}_m \ltimes \Pi \mathbb{G}_{ad}
$$

for which it is well known that an [[action]] of it is equivalent to a choice of [[differential]] $Q$ and corresponding grading. 

This chosen differential $Q$ among the supersymmetry generators in the [[super Poincare Lie algebra]] is the choice of what in the physics literature is called the twisting "BRST operator".

The twisted theory itself is then defined to be given by the [[factorization algebra]] of observables which is essentially the [[homotopy fixed points]] of this $\mathbf{Aut}(\mathbb{R}^{0|1})$-[[infinity-action]].




## Related concepts

* [[topological Yang-Mills theory]]

* [[topological twist]]

* [[D=4 Yang-Mills theory]]

* [[N=1 D=4 super Yang-Mills theory]]

* [[N=2 D=4 super Yang-Mills theory]]

* [[N=4 D=3 super Yang-Mills theory]]

* [[N=4 D=4 super Yang-Mills theory]] 

* [[D=5 super Yang-Mills theory]]

* [[S-duality]], [[geometric Langlands duality]]

* [[chiral ring]], [[quantum cohomology]]

## References
  {#References}

The idea of topological twisting of [[supersymmetry|supersymmetric]] quantum field theory goes back to 

* [[Edward Witten]], _Topological quantum field theory_, Comm. Math. Phys. Volume 117, Number 3 (1988), 353-386 ([Euclid](http://projecteuclid.org/euclid.cmp/1104161738))

often referred to as "[[cohomological field theory]]"

* {#Witten91} [[Edward Witten]], _Introduction to cohomological field theory_, InternationalJournal of Modern Physics A, Vol. 6,No 6 (1991) 2775-2792 ([[WittenCQFT.pdf:file]])

where it is [[N=2 D=4 super Yang-Mills theory]] that is twisted and related to [[Donaldson theory]]. 

A superspace formulation that makes the form of the Lagrangian more transparent is in:

* James Horne. *Superspace versions of topological theories.* Nuclear Physics B 318, no. 1 (1989): 22-52. ([doi](https://doi.org/10.1016/0550-3213(89)90046-1))

A geometric interpretation and derivation of the Lagrangian using [[equivariant de Rham cohomology]] is in:

* [[Michael Atiyah]], [[Lisa Jeffrey]]. *Topological Lagrangians and cohomology.* Journal of Geometry and Physics 7, no. 1 (1990): 119-136. ([doi](https://doi.org/10.1016/0393-0440(90)90023-V))

based on the results in

* [[Varghese Mathai]], [[Daniel Quillen]]. *Superconnections, Thom classes and equivariant differential forms*. Topology 25, 85 (1986)  (<a href="https://doi.org/10.1016/0040-9383(86)90007-8">doi:10.1016/0040-9383(86)90007-8</a>)



The analogous twisting of [[N=4 D=4 super Yang-Mills theory]] is due to 

* [[Cumrun Vafa]], [[Edward Witten]], _A Strong Coupling Test of S-Duality_, Nucl. Phys. B **431** (1994) 3-77 &lbrack;[arXiv:hep-th/9408074](http://arxiv.org/abs/hep-th/9408074)&rbrack;

This *Vafa-Witten theory* reviewed and further developed in:

* Zhi-Cong Ong, [[Meng-Chwan Tan]], *Vafa-Witten Theory: Invariants, Floer Homologies, Higgs Bundles, a Geometric Langlands Correspondence, and Categorification* &lbrack;[arXiv:2203.17115](https://arxiv.org/abs/2203.17115)&rbrack;


The $N=4$-case and  one of the possible $N=2$-twists yield [[instanton]] invariants captured by the [[Seiberg-Witten theory]] generalization of [[Donaldson theory]]. Another variant of the $N=2$ twist was described in 

* Neil Marcus, _The other topological twisting of N=4 Yang-Mills_, Nucl.Phys. B452 (1995) 331-345 ([arXiv:hep-th/9506002](http://arxiv.org/abs/hep-th/9506002))

and yields a geometric interpretation of the [[geometric Langlands correspondence]], as found in

* [[Anton Kapustin]], [[Edward Witten]], _Electric-Magnetic Duality And The Geometric Langlands Program_ ([arXiv:hep-th/0604151](http://arxiv.org/abs/hep-th/0604151))

A detailed analysis of the three twists of the $N=4$ theory is in 

* Carlos Lozano, _Duality in Topological Quantum Field Theories_, PhD thesis ([arXiv:hep-th/9907123](http://arxiv.org/abs/hep-th/9907123))

Discussion of generalization of the twisting to [[quantum field theory on curved spacetime]] is in 

* [[Jeong-Hyuck Park]], [[Dimitrios Tsimpis]], _Topological twisting of conformal supercharges_, Nucl. Phys. B776:405-430, 2007 ([arXiv:hep-th/0610159](http://arxiv.org/abs/hep-th/0610159))

Section 2.2.1 of 

* {#Witten11} [[Edward Witten]], _Fivebranes and knots_ ([arXiv:1101.3216](http://arxiv.org/abs/1101.3216))
 

briefly recalls the topological twisting of [[N=4 D=4 super Yang-Mills theory]]. Section 5.1.1 there discusses the twisting of [[N=2 D=4 super Yang-Mills theory]] (induced from the [[6d (2,0)-superconformal QFT]] on the [[M5-brane]]), which was introduced in section 3.1.2 of

* [[Davide Gaiotto]], [[Gregory Moore]] and [[Andrew Neitzke]], _Wall-crossing, Hitchin Systems, and the WKB Approximation_, ([arXiv:0907.3987](http://arxiv.org/abs/0907.3987))

For more on this see the references listed at _[N=2 D=4 super Yang-Mills theory -- References -- Construction from 5-branes](N%3D2+D%3D4+super+Yang-Mills+theory#ReferencesConstructionFrom5Branes)_.

More mathematically formalized discussion of topologically twisted supersymmetric theories in the framework of [[BV-BRST formalism]] [[perturbation theory]] (and with an eye towards the [[factorization algebra]] formulation) is in

* {#Costello11} [[Kevin Costello]], *Notes on supersymmetric and holomorphic field theories in dimension 2 and 4*, talk at *[Geometric and Algebraic Structures in Mathematics](https://www.math.stonybrook.edu/dennisfest/)*, Stony Brook (2011) &lbrack;[arXiv:1111.4234](https://arxiv.org/abs/1111.4234)&rbrack;
 
More in

* {#ElliottSafronov18} [[Chris Elliott]], [[Pavel Safronov]], _Topological twists of supersymmetric observables_ ([arXiv:1805.10806](https://arxiv.org/abs/1805.10806))

In

* [[Kevin Costello]], _Supersymmetric gauge theory and the Yangian_ ([arXiv:1303.2632](http://arxiv.org/abs/1303.2632))

is discussed that the holomorphically twisted $N=1$ theory is controled by the [[Yangian]] in analogy to how [[Chern-Simons theory]] is controled by a [[quantum group]].

[[!redirects topologically twisted D=4 super Yang-Mills theories]]

[[!redirects topologically twisted super Yang-Mills theory]]
[[!redirects topologically twisted super Yang-Mills theories]]

[[!redirects topologically twisted N=2 D=4 super Yang-Mills theory]]
[[!redirects topologically twisted N=2 D=4 super Yang-Mills theories]]

[[!redirects topologically twisted N=4 D=4 super Yang-Mills theory]]
[[!redirects topologically twisted N=4 D=4 super Yang-Mills theories]]

[[!redirects Vafa-Witten theory]]
