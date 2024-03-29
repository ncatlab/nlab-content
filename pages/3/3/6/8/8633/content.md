
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

Under the [interpretation of modules as generalized vector bundles](http://ncatlab.org/nlab/show/module#RelationToVectorBundlesInIntroduction) a [[module]] being _locally free_ corresponds to the corresponding [[bundle]] being _locally trivial bundle_, hence a [[fiber bundle]].

Since a _trivial bundle_ corresponds to a [[free module]], a _locally free module_ is such that its [[localization of a module|localization]] to any [[maximal ideal]] is a [[free module]].


## Definition

+-- {: .num_defn #LocallyFreeModule}
###### Definition

An $R$-module $N$ over a [[Noetherian ring]] $R$ is called a **locally free module** if there is a [[Zariski topology|cover]] by [[ideals]] $I \hookrightarrow R$ such that the [[localization of a module|localization]] $N_I$ is a [[free module]] over the [[localization of a ring|localization]] $R_I$. 

=--

+-- {: .num_defn #StalkwiseFreeModule}
###### Definition

For $R$ a [[commutative ring]], an $R$-[[module]] $N$ is called a **stalkwise free module** if for every [[maximal ideal]] $I \hookrightarrow R$ the [[localization of a module|localization]] $N_I$ is a [[free module]] over the [[localization of a ring|localization]] $R_I$. 

=--


## Properties


+-- {: .num_prop}
###### Proposition

Let $R$ be a ring and $N \in R$[[Mod]].

The following are equivalent

1. $N$ is [[finitely generated module|finitely generated]] and [[projective module|projective]],

1. $N$ is locally free, def. \ref{LocallyFreeModule} and locally finitely generated.

=--

For instance ([Clark, theorem 7.20](#Clark)).

+-- {: .num_prop #ForFinitelyGeneratedFlatIsLocallyFree}
###### Proposition

For $R$ a [[Noetherian ring]] and $N$ a [[finitely generated module]] over $R$, $N$ is a locally free module precisely if it is a [[flat module]].

=--

By [Raynaud-Gruson, 3.4.6 (part I)](#RaynaudGruson)


## References

* Pete Clark, _Commutative algebra_ ([pdf](http://math.uga.edu/~pete/integral.pdf))
 {#Clark}

* Michel Raynaud, Laurent Gruson, _Crit&#232;res de platitude et de projectivit&#233;_, Techniques de "platification" d'un module. Invent. Math. 13 (1971), 1&#8211;89.
 {#RaynaudGruson}

[[!redirects locally free modules]]
