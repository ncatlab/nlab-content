
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Extremal morphisms
* table of contents
{: toc}

## Definition

An __extremal epimorphism__ (also sometimes called a _[[cover]]_) in a [[category]] $C$ is an [[epimorphism]] $e$ such that if $e = m \circ g$ where $m$ is a [[monomorphism]], then $m$ is an [[isomorphism]].

The dual notion is an __extremal monomorphism__: a monomorphism $m$ such that if $m = g \circ e$ where $e$ is an [[epimorphism]], then $e$ is an isomorphism.


## Remarks

* If $C$ has all [[equalizers]], then the assumption that $e$ is an epimorphism is redundant in the definition -- in this case any morphism admitting no non-trivial factorizations through monomorphisms is automatically epic.

* Any [[strong epimorphism]] is extremal.  The converse is true if $C$ has all [[pullbacks]].

* Any [[regular epimorphism]] is strong, and hence extremal.  The converse is true if $C$ is [[regular category|regular]].

* An [[image|image factorization]][^1] of a morphism $f$ is, by definition, a factorization $f = m \circ e$ where $m$ is a [[monomorphism]] and $e$ is an extremal epimorphism. 

[^1]: Under a default meaning of [[image]] that makes reference to the class $M$ of all monomorphisms. 

Of course, the dual properties are all true of extremal monomorphisms.  (See [[coequalizer]], [[monomorphism]], [[strong monomorphism]], [[pushout]], [[regular monomorphism]], [[coregular category]], [[coimage factorization]], [[epimorphism]].)


## Related concepts

* [[monomorphism]], [[epimorphism]]
* __extremal monomorphism__, __extremal epimorphism__
* [[strong monomorphism]], [[strong epimorphism]]
* [[strict monomorphism]], [[strict epimorphism]]
* [[regular monomorphism]], [[regular epimorphism]]
* [[normal monomorphism]], [[normal epimorphism]]
* [[effective monomorphism]], [[effective epimorphism]]
* [[split monomorphism]], [[split epimorphism]]

## References

* [[Francis Borceux]], Def. 4.3.2 in: *[[Handbook of Categorical Algebra]]* Vol. 1: *Basic Category Theory*, Encyclopedia of Mathematics and its Applications **50** Cambridge University Press (1994) ([doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858))



[[!redirects extremal morphism]]
[[!redirects extremal morphisms]]

[[!redirects extremal epimorphism]]
[[!redirects extremal epimorphisms]]
[[!redirects extremal epi]]
[[!redirects extremal epis]]
[[!redirects extremal epic]]
[[!redirects extremal epics]]

[[!redirects extremal monomorphism]]
[[!redirects extremal monomorphisms]]
[[!redirects extremal mono]]
[[!redirects extremal monos]]
[[!redirects extremal monic]]
[[!redirects extremal monics]]
