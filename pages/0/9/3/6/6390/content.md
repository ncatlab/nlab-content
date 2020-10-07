
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
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

The _spinning relativistic particle_ is a variant of the plain [[relativistic particle]] which has an "internal degree of freedom" called [[spin]]: it is a _[[spinor]]_ , a [[fermion]]. Examples that appear in the [[standard model of particle physics]] are [[electron]]s, and [[quarks]].

As a 1-dimensional [[sigma-model]], the _spinning_ relativistic particle is like the [[relativistic particle]] but with [[fermion field]]s on the [[worldline]]. This worldline action always happens to have worldline [[supersymmetry]], entirely independent of whether there is any supersymmetry on [[target space|target]] [[spacetime]].


## Properties

### Worldline supersymmetry
 {#WorldlineSupersymmetry}

We discuss how spinning particles automatically have [[supersymmetry]] in their [[worldline formalism]]. For more see the [references below](#WorldlineSupersymmtryReferences) for more and see also at _[string theory FAQ -- Does string theory predict supersymmetry?](string+theory+FAQ#DoesSTPredictSupersymmetry)_.

In the [[Polyakov action]]-formulation the [[action functional]] of the [[relativistic particle]] [[sigma model]] on the 1-dimensional [[worldline]] is actually 1-dimensional [[gravity]] coupled to "worldline matter fields", where the latter are the embedding fields $\phi : \mathbb{R} \to X$ into the [[target space]].

It turns out that the generalization of this 1-dimensional gravity action to [[supergravity]] yields the action functional that describes ordinary Dirac [[spinors]] -- spinning particles like [[electron]]s -- propagating on [[target space]] $X$. See the [references on worldline supersymmetry](#WorldlineSupersymmtryReferences) below.

The worldline supersymmetry of fermions comes down to the fact that their [[Hamiltonian]](-constraint) operator $H$ has a square root: the 
[[Dirac operator]] $D$. Its defining equations

$$
  [D,D] = 2 D^2 = H\,,\;\;\; [H,H] = 0\;,\;\; [D,H] = 0
$$

characterize the $d = 1$ [[translation super-Lie algebra]].


For appreciating this fact it is important to keep the ingredients of [[sigma-model]] theory sorted out correctly: a supersymmetric theory on the worldline describes a spinning particle on some [[target space|spacetime]] coupled to some [[background gauge field]]s. That background geometry need not have a "global supersymmetry" (a covariant constant spinor), hence under [[second quantization]] the [[perturbation theory]] _on target space_ induced by the worldline theory need not have any global supersymmetries (in particular no superpartners to the effective particle excitations). What will happen, though, is that the full target space theory induced under [[second quantization]] will be a [[supergravity]] theory on target space. Some of its solutions may have covariantly constant spinors (and hence global supersymmetry), but generically they will not, just like the generic solution to ordinary [[Einstein equations]] does not have a [[Killing vector]]. 


### Paritition function

[[!include genera and partition functions - table]]


## History

That some [[particle]]s have a property called [[spinor|spin]] was found in 1922 in the [[Stern-Gerlach experiment]]. 

## Related concepts

* [[fermion]], [[spinor]]

* [[sigma model]], [[brane]]

  * [[relativistic particle]], **spinning particle**, [[superparticle]]

    * [[A-hat genus]], [[(1,1)-dimensional Euclidean field theories and K-theory]]

  * [[string]], [[spinning string]], [[superstring]]

    [string theory FAQ -- Does string theory predict supersymmetry?](string%20theory%20FAQ#DoesSTPredictSupersymmetry)

  * [[membrane]]


## References

### General 

Discussion of worldline dynamics of spinning particles in background fields is for instance in:

* J.W. van Holten, _Relativistic Dynamics of Spin in Strong
External Fields_([arXiv:hep-th/9303124](http://arxiv.org/abs/hep-th/9303124))

* A. Pomeranskii, R A Sen'kov, I.B. Khriplovich, _Spinning relativistic particles in external fields_ Acta Physica Polonica B Proceedings Supplement Vol. 1 (2008) ([pdf](http://iopscience.iop.org/1063-7869/43/10/R03))

* Krzysztof Andrzejewski, Cezary Gonera, Joanna Goner, Piotr Kosinski, Pawel Maslanka, _Spinning particles, coadjoint orbits and Hamiltonian formalism_ ([arXiv:2008.09478](https://arxiv.org/abs/2008.09478))

Discussion that cancellation of the [[quantum anomaly]] of the spinning particle precisely requires [[Spin-structure]] on its [[target spacetime]]:

* {#Witten85} [[Edward Witten]], _Global anomalies in string theory_, in: W. Bardeen and A. White (eds.). _Symposium on Anomalies, Geometry, Topology_, pp. 61&#8211;99. World Scientific, 1985  ([[WittenGlobalAnomaliesInStringTheory.pdf:file]], [spire:214913](https://inspirehep.net/literature/214913))


### Worldline supersymmetry
 {#WorldlineSupersymmtryReferences}

Among the early references that describe the observation that the supersymmetric extension of the worldline theory of the [[relativistic particle]] describes ordinary Dirac [[fermion]]s are

* F.A. Berezin and M.S. Marinov, Ann. Phys. (NY) 104 (1977), 336

* L. Brink, P. Di Vecchia and P. Howe, Nucl. Phys. B118 (1977), 76

* R. Casalbuoni, Phys. Lett. B62 (1976), 49

* A. Barducci, R. Casalbuoni and L. Lusanna, Nuov. Cim. 35A (1976), 377
Nucl. Phys. B124 (1977), 93; id. 521


A survey of constructions of [[worldline]] supersymmetric action functional for spinning particles in various [[background gauge field|background fields]] is given in

* J. van Holten, _$D = 1$ Supergravity and Spinning Particles_ ([pdf](http://www.iaea.org/inis/collection/NCLCollectionStore/_Public/28/002/28002527.pdf))

An argument that for arbitrary backgrounds the spinning particle's worldline action is supersymmetric is given in 

* Darius Gagn&#233;, _Worldline Supersymmetry and Dimensional Reduction_ ([arXiv:hep-th/9604149](http://arxiv.org/abs/hep-th/9604149))

Textbook surveys of worline supersymmetry include

the beginning of section 14.1.1 in 

* Tom&#225;s Ort&#237;n, _Gravity and strings_ Cambridge University Press (2004)

Derivation of the supersymmetric [[worldline]] action of the spinning particle in the _[[worldline formalism]]_ of [[QFT]] [[scattering amplitudes]] is around (3.6) of 

* [[Matthew Strassler]], _Field Theory Without Feynman Diagrams: One-Loop Effective Actions_, Nucl. Phys. B385:145-184,1992 ([arXiv:hep-ph/9205205](http://arxiv.org/abs/hep-ph/9205205))

See also

* Rachel H. Rietdijk, _Spinning particles in general relativity_ Theoretical and Mathematical Physics, Vol. 98, No. 3 (1994)

also p. 194 of

* Warren Siegel, _Fields_ ([arXiv:hep-th/9912205](http://arxiv.org/abs/hep-th/9912205))

There, first exercise IIIB1.3 gives the action expanded out in all components, and then the following exercise IIIB1.4 gives the reformulation in [[superfield formalism]] which makes manifest that the action is invariant under worldline [[supersymmetry]].

See also

* Roberto Casalbuoni, Joaquim Gomis, Kiyoshi Kamimura, Giorgio Longhi, _Space-time Vector Supersymmetry and Massive Spinning Particle_ ([web](http://www.mendeley.com/research/spacetime-vector-supersymmetry-and-massive-spinning-particle/))


[[!redirects spinning particles]]

[[!redirects worldline supersymmetry]]