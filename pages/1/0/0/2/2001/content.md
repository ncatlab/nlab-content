
#Contents#
* table of contents
{:toc}

## Definition

A [[homomorphism]] of (not necessarily commutative nor unital) [[rings]] $u:R\to S$ is __flat__ if the [[extension of scalars]] (= [[inverse image]]) [[functor]] $u^*:{}_R Mod\to {}_S Mod$, $M\mapsto S\otimes_R M$ is an [[exact functor|exact]] [[additive functor]]. 

Recall that every [[extension of scalars]] functor for [[modules]] is cocontinuous and a fortiori admits a [[right adjoint]]. Hence this definition is in an agreement with the more general notion of a [[flat functor]] in category and topos theory.

If one pictures a morphism as a family over its [[codomain]], then for many purposes good families are flat (e.g. in [[deformation theory]]). 



**Flat modules:** A right $R$-module $M_R$ is **flat** if the functor ${}_R N\mapsto M \otimes_R N$ from the category of left $R$-modules to the category [[Ab]] of abelian groups is exact. 

A morphism $f:X\to Y$ of [[schemes]] is **flat** if the induced map on [[stalks]] is a flat morphism of (commutative unital) rings. 

A morphism of schemes is **faithfully flat** if it is flat and [[epimorphism|epi]].

## Flat topologies

Given a base scheme $S$, the [[slice category]] $Sch/S$ of [[relative schemes]] over $S$ is equipped with several _flat [[Grothendieck topologies]]_. 

These are the [[Grothendieck topologies]] in which covers consist of flat morphisms which set-theoretically cover the target scheme with some additional finiteness conditions. The usual choices are the [[fppf topology|fppf]] (fr. _fid&#232;lement plat de presentation finie_, 'faithfully flat and of finite presentation') and [[fpqc topology|fpqc]] (fr. _fid&#232;lement plat et quasicompact_, 'faithfully flat and quasicompact') topologies.  Cf. [wikipedia:flat topology](http://en.wikipedia.org/wiki/Flat_topology)


## Related concepts

* [[étale morphism of schemes]], [[formally étale morphism of schemes]]


## References
The standard reference is [[EGA IV]]. See also [[flat morphism in derived geometry]]. 


[[!redirects flat morphisms]]
[[!redirects flat topology]]
[[!redirects flat morphism of schemes]]

[[!redirects faithfully flat]]


[[!redirects faithfully flat morphism]]
[[!redirects faithfully flat morphisms]]

[[!redirects faithfully flat morphism of schemes]]
[[!redirects faithfully flat morphisms of schemes]]

