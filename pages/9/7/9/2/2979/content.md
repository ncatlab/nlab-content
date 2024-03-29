
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Normal (mono/epi)morphisms
* table of contents
{: toc}


## Idea

The concept of _normal monomorphism_ generalizes the concept of _[[normal subgroup]] inclusions_.

One often considers [[regular monomorphisms]] and [[regular epimorphisms]].  In the theory of [[abelian categories]], one often equivalently uses _normal_ monomorphisms and epimorphisms.  In general, the concept makes sense in a category with [[zero morphisms]], that is in a [[category enriched]] over [[pointed sets]].


## Definition

A [[monomorphism]] $f\colon A \to B$ is __normal__ if it is the [[kernel]] of some morphism $g\colon B \to C$, that is if it is the [[equalizer]] of $g$ and the [[zero morphisms]] $0_{B,C}\colon B \to C$.

An [[epimorphism]] $f\colon B \to A$ is __normal__ if it is the [[cokernel]] of some morphism $g\colon C \to B$, that is if it is the [[coequalizer]] of $g$ and the [[zero morphism]] $0_{C,B}\colon C \to B$.

Note that a normal monomorphism in $C$ is the same as a normal epimorphism in the [[opposite category]] $C^{op}$, and vice versa.

A [[category]] is __normal__ if every monomorphism is normal; it is __conormal__ if every epimorphism is normal, and it is __binormal__ if it is both normal and conormal.  Note that $C$ is normal if and only if $C^{op}$ is conormal, and vice versa.


## Examples

The [[inclusion function]] of a [[subgroup]] into a [[group]] is normal if and only if the subgroup is [[normal subgroup|normal]]; this is the origin of the terminology for normal monomorphisms.

Every normal monomorphism or epimorphism is clearly regular; the converse holds in any [[Ab-enriched category]] (the equalizer of $f$ and $g$ is the kernel of $f-g$).

Every [[abelian category]] must be binormal; this is one of the axioms in a common definition of abelian category.

## Related concepts

* [[normal]]

## References

Discussion of [[normalizer]] constructions for monomorphisms is in 

* {#Gray14} James Richard Andrew Gray, _Normalizers, centralizers and action representability in semiabelian categories_, Applied Categorical Structures 22(5-6), 981&#8211;1007, 2014.


[[!redirects normal monomorphisms]]
[[!redirects normal epimorphism]]
[[!redirects normal epimorphisms]]
[[!redirects normal category]]
[[!redirects conormal category]]
[[!redirects binormal category]]
[[!redirects normal categories]]
[[!redirects conormal categories]]
[[!redirects binormal categories]]
