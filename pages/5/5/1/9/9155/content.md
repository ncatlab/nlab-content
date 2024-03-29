
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

A central aspect of [[quantum field theory]] usually desired or demanded or expected of _fundamental_ QFTs is that it is _local_ in the rough sense that 

* there is no "action at a distance", but all influences propagate (on a [[Lorentzian manifold]]) at some finite speed (that of light, usually);

* phenomena of large scale [[spacetime]]/[[worldvolume]] are entirely determined by phenomena on smaller scales;

* (space-like) separated regions of [[spacetime]] behave like [independent subsystems](quantum+mechanics#Subsystems) ([[causal locality]]).

In some [[effective quantum field theories]] locality may be violated, if fundamental local processes are averaged out to a single non-local macroscopic process, but for _fundamental_ physics of the [[observable universe]] it is thought to hold.

### Formalization in quantum field theory

Locality is formalized in the two main axiomatizations of quantum field theory as follows.

* In [[AQFT]] the [[algebras of observables]] are required to form a _[[local net]]_ meaning that 

  1. there is one such algebra assigned to each suitable subset of spacetime, compatible with inclusion of such subsets, 

  1. that under these inclusions algebras associated to spacelike separated regions commute with each other.

  Often in the literature the term "local quantum field theory" is meant to refer specifically to these [[AQFT]] axioms (some authors use the terms synonymously, dating from a time when this was the only axiomatization of quantum field theory considered.)

* In [[FQFT]] locality is encoded in the [[functor]]-property of the functor on the [[category of cobordisms]]: being a functor means that the assignment to a cobordism $\Sigma$ is obtained by composing the assignments to any decomposition of $\Sigma$ into small cobordisms. In particular, in _[[extended quantum field theory]]_ (now also sometimes called "fully localized" QFT) this is [[(infinity,n)-functor|n-functorial]] meaning that this gluing condition holds in all dimensions and in all directions.

### Formalization in pre-quantum field theory

There are also properties of locality in _[[prequantum field theory]]_.

A _[[Lagrangian density]]_ is called a _[[local Lagrangian]]_ if it "depends only on finitely many [[derivatives]] of the [[field (physics)|fields]]" at any point of spacetime, which formally means that it is a [[variational bicomplex|horizontal differential form]] on the [[jet bundle]] of the [[field bundle]]. Local Lagrangian densities are expected to yield local quantum field theories under [[quantization]]. This is the case at least in [[perturbative quantum field theory]] formalized via [[causal perturbation theory]]/[[perturbative AQFT]], see at _[[S-matrix]]_ the section _[Quantum observables and retarded products](S-matrix#QuantumObservables)_


## Related concepts

* [[microcausality]], [[Einstein causality]]

* [[cluster decomposition]]

* [[Lagrangian quantum field theory]]

* [[algebraic quantum field theory]]

* [[perturbative algebraic quantum field theory]]

## References

* _[[schreiber:Local prequantum field theory]]_

On [[local field theory|locality]] of [[extended functorial field theory|extended]] [[functorial field theory]]:

* [[Daniel Grady]], [[Dmitri Pavlov]], _Extended field theories are local_ ([arXiv:2011.01208](https://arxiv.org/abs/2011.01208))


Steps towards a local version of [[BV-formalism]] are undertaken in 

* [[Alberto Cattaneo]], [[Pavel Mnev]], [[Nicolai Reshetikhin]], _Classical BV theories on manifolds with boundary_ ([arXiv:1201.0290](http://arxiv.org/abs/1201.0290))

* [[Alberto Cattaneo]], [[Pavel Mnev]], [[Nicolai Reshetikhin]], _Classical and quantum Lagrangian field theories with boundary_ ([arXiv:1207.0239](http://arxiv.org/abs/1207.0239))

* [[Alberto Cattaneo]], [[Pavel Mnev]], [[Nicolai Reshetikhin]], _Perturbative quantum gauge theories on manifolds with boundary_ ([arXiv:1507.01221](http://arxiv.org/abs/1507.01221))

 

[[!redirects local quantum field theories]]



[[!redirects local field theory]]
[[!redirects local field theories]]

[[!redirects local QFT]]
[[!redirects local QFTs]]

[[!redirects local Lagrangian field theory]]
[[!redirects local Lagrangian field theories]]
