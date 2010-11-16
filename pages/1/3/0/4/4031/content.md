
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _algebraic Kan complex_ is an [[algebraic definition of higher categories|algebraic definition of]] [[∞-groupoid]]s.

It builds on the classical [[geometric definition of higher categories|geometric definition]] of $\infty$-groupoids in terms of [[Kan complex]]es. A Kan complex is like an algebraic $\infty$-groupoid in which we have forgotten what precisely the [[composition]] operation and what the [[inverse]]s are, and only know that they do exist. This becomes an _algebraic model_ for $\infty$-groupoids by adding the specific choices of composites back in. 

The nontrivial apsect of the definition of algebraic Kan complexes is that they do still [[presentable (∞,1)-category|present]] the full [[(∞,1)-category]] [[∞Grpd]]. Notably the [[homotopy hypothesis]] is true for algebraic Kan complexes.

## Definition



An **algebraic Kan complex** is a [[Kan complex]] equipped with a _choice_ of [[horn]] fillers for all horns.

A morphism of algebraic Kan complexes is a morphism of the underlying Kan complexes that sends chosen fillers to chosen fillers.

This defines the category $Alg Kan$ of algebraic Kan complexes.

For more see the section [Algebraic  fibrant models for higher categories](http://ncatlab.org/nlab/show/model+structure+on+algebraic+fibrant+objects#AlgebaicHigherCategories) at [[model structure on algebraic fibrant objects]].

A slight variant of this definition is that of a [[simplicial T-complex]].


## Properties

### Monadicity

The category $Alg Kan$ is the category of algebras over a [[monad]]

$$
  sSet \stackrel{\leftarrow}{\to}  Alg sSet
  \,.
$$

This means that algebraic Kan complexes are formally an _algebraic model_ for higher categories.

See [[model structure on algebraic fibrant objects]] for details.

### Homomtopy hypothesis-theorem

The [[homotopy hypothesis]] is true for algebraic Kan complexes: 

there is a [[model category]] structure on $Alg Kan$ -- the [[model structure on algebraic fibrant objects]] -- and a [[Quillen equivalence]] to the standard [[model structure on simplicial sets]].

Moreover, there is a direct [[Quillen equivalence]]

$$
  \Pi_\infty : Top \stackrel{\leftarrow}{\to} AlgKan : |-|
  \,,
$$

to the standard [[model structure on topological spaces]], where the [[left adjoint]] $|-|$ is [[geometric realization]] of the underlying Kan complexes and $\Pi_\infty$ is a version of the [[fundamental ∞-groupoid]]-functor with values in algebraic Kan complexes. 

See <a href="http://ncatlab.org/nlab/show/homotopy+hypothesis#ForKanComplexes">homotopy hypothesis -- for algebraic Kan complexes</a> for details.

## References

* [[Thomas Nikolaus]], _Algebraic models for higher categories_ ([arXiv](http://arxiv.org/abs/1003.1342))
{#Nikolaus}

[[!redirects algebraic Kan complex]]
[[!redirects algebraic Kan complexes]]
