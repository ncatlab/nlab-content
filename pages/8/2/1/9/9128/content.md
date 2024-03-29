+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

### General idea

In [[physics]] the term _theory_ or _physical theory_ traditionally refers, somewhat vaguely, to a given set of notions and rules, usually formulated in the language of [[mathematics]], that describe how some [[physical system]] or class of physical systems behaves. Typically these systems are highly idealized, in that the theories describe only certain aspects.

Often a given such theory depends on many free parameters. When a choice of such parameters is made or the range of the parameters is being restricted one tends to call the result a _[[model (in theoretical physics)]]_. For more on this see _[Theories and their Models](#TheoriesAndTheirModels)_ below.

The most accurate general theory of fundamental physics known is _[[Einstein gravity]]_ and _[[quantum field theory]]_. The best available choices of parameters in this general theory that make it fit the specifics of the observed world ([[phenomenology]]) are [[model (in theoretical physics)|models]] which accordingly are called the _standard models_: there is the _[[standard model of particle physics]]_ and the _[[standard model of cosmology]]_.

### Formalization

Beware that, therefore, the use of the terms _theory_ and _model_ in [[physics]] is _different_ from the same terms as used in [[logic]] (see at [[theory (logic)]] and [[model (logic)]]). 

But most theories of fundamental physics (and many theories of effective physics such as [[solid state physics]])  fit into a pattern that can be [[axiom|axiomatized]] at least to some extent: 

these physical theories are specified by a ([[local Lagrangian|local]]/[[extended Lagrangian|extended]]) [[Lagrangian]] on a space of [[field (physics)|fields]] over a given [[spacetime]]/[[worldvolume]] [[manifold]] $X$, hence by an [[action functional]]

$$
  S \;\colon\; [X, \mathbf{Fields}]_{\mathbf{H}} \to U(1)
  \,.
$$

In particular the corresponding [[classical field theory]] has as its "space of models" the [[critical locus]] 

$$
  \underset{\phi \in [X, \mathbf{Fields}]_{\mathbf{H}}}{\sum}
  ( \mathbf{d} S_\phi \simeq 0 )
$$

of such an [[action functional]], the space of solutions of the [[Euler-Lagrange equations]]. A point in this space is a single "physically realizable" configuration of [[field (physics)|fields]] in this theory, disregarding [[quantum field theory]]-corrections, and a small-parameter subspace is often referred to as "a model" of the theory.

In this perspective of classical field theory, two different action functionals on different spaces of fields but with [[equivalence|equivalent]] [[critical loci]] are regarded as "equivalent physical theories". One often sees the term "classically equivalent" for this notion used in the literature.

But the full [[quantum field theory]] determined by a [[Lagrangian]]/[[action functional]] depends on more than just the [[critical locus]], which is just something like the lowest order approximation to the quantum theory (in a sense that can be made precise, for instance in [[deformation quantization]] in terms of [[power series]] developments in [[Planck's constant]].)

## Examples



### General principles

One broad way of classifying physical theories is by the extent to which they take [[quantum physics]] into account. We have

* [[classical field theory]]

* [[prequantum field theory]]

* [[quantum field theory]]

Here [[quantum field theory]] is the most refined framework, which underlies the [[standard model of particle physics]]. 

The notion of quantum field theory, fundamental as it is, is quite flexible and in particular it naturally captures the concept that a given quantum field theory only describes phenomena that occur below a certain [[energy]] range and treats all phenomena at higher energy as the average over an unspecified more refined theory. This is the notion of

* [[effective quantum field theory]].

Crucially, [[Einstein gravity]] is not known to have a formulation as a _fundamental_ quantum field theory with finitely many unspecified parameters ([[renormalization|renormalizable]]).  But it may well be a [[effective quantum field theory]], the approximation to a more refined physical theory valid at higher energies. (This is the issue of [[quantum gravity]].) A proposal for a physical theory that achieves this is called _[[string theory]]_.

### Types of theories

* [[free field theory]]

* [[gauge theory]]

### The fundamental phenomenological theories

* [[gravity]], [[Yang-Mills theory]]

* [[Einstein-Maxwell theory]]

* [[Einstein-Yang-Mills theory]]

* [[Einstein-Maxwell-Yang-Mills-Dirac-Higgs theory]]

[[!include standard model of fundamental physics - table]]

### Theories and their models
 {#TheoriesAndTheirModels}

+-- {: .num_example}
###### Example

The [[classical field theory]] of [[gravity]] is a physical theory which asserts that [[spacetime]] is modeled by a [[pseudo-Riemannian manifold]] equipped with certain further [[force]] and [[matter]] [[field (physics)|fields]], such that this data satisfies [[Einstein equations]]. But if one furthermore specifies a particular such pseudo-Riemannian manifold etc. one may call this a _model_ of [[gravity]]/[[cosmology]]. The _[[FRW model]]_ is an example: here one specifies that the given pseudo-Riemannian metric and the [[matter]] [[field (physics)|field]] content is _homogenous_ and _isotropic_. This is highly restrictive but still does not single out a unique solution. The remaining parameter is $k \in \{-1,0,1\}$, determining whether in this solution space has negative, positive or vanishing constant curvature.

=--

## Related concepts

* [[model (physics)]], [[experiment]], [[coordination]]

* [[theory of everything]]

* [[computable physics]]

* [[mathematical physics]]

* [string theory FAQ -- How do physical theories generally make predictions, anyway?](http://ncatlab.org/nlab/show/string+theory+FAQ#AsideHowToPhysicalTheorieyGenerallyMakePredictionsAnyway)

## References

* [[James Wells]], _Lexicon of Theory Qualities_ ([pdf](http://www-personal.umich.edu/~jwells/prms/prm8.pdf))


[[!redirects theories (physics)]]

[[!redirects physical theory]]
[[!redirects physical theories]]

[[!redirects theory in physics]]
[[!redirects theories in physics]]

[[!redirects theory of physics]]
[[!redirects theories of physics]]
